# Развёртывание лаборатории как сменного контейнера

```
Статус: Knowledge Candidate. Не Foundation. Не канон AICM. Не PREF. Не контейнер Hermes.
Дата: 2026-08-31
Источник: приказ Владельца 2026-08-31 («взять и полностью развернуть»; обновлять при новом внедрении) + shtab/2026-08-31-lab-as-container.md (LAB-C-01…14) + razvedka/2026-08-31-research-center-as-container.md (LC-01…16) + AGENTS.md
Provenance: контракт штаба и съём runtime. Образ в этой сессии не собирали и не гоняли. Версии userland ниже — то, что реально стоит на текущем хосте лаборатории (Python 3.13.5, gh 2.46.0, git 2.47.3); тег образа — кандидат, не прогон.
```

**Не live. Не Bitget. Не ключи в образе. Не 8 микросервисов. Не LangGraph/CrewAI/Letta/MAF как identity. L0–L2 закрыты.**

Это **живой runbook**. Любое новое внедрение, которое меняет I/O, роли, зависимости или секреты, **в том же инкременте** правит этот файл (LAB-D-12). Индекс: `shtab/celi.md` пункт 8.

ID `LAB-D-*` — пункты поставки. Не путать с `LAB-C-*` (контракт) и `LC-*` (съём runtime). Не PREF.

## 1. Что значит «полностью развернуть»

**LAB-D-01.** Поставка = **один** исследовательский центр:

| Слой | Что это | Куда |
|---|---|---|
| A. Склад | приватный `Seryogapahom/AICM-docs` (`AGENTS.md` + папки) | bind-mount, не слои образа |
| B. Userland | Python + git + gh + curl + jq | OCI-образ (LC-01, LC-04) |
| C. Процессы ролей | 8 ролей как процессы/очередь пакетов, не 8 контейнеров | внутри runtime хоста |
| D. Адаптер хоста | сегодня Grok Bot (чат, MCP, X read-only); завтра — любой хост с тем же I/O | **не** копируется в образ и **не** identity AICM |

«Взял и поднял» = A + B + этот файл + секреты снаружи. Слой C исполняет **хост моделей/агентов**, который читает `AGENTS.md`. Слой D сменяем (LAB-C-04, LC-02).

**LAB-D-02.** Это не включение live, не повышение KC в PREF, не playbook Hermes, не `docker compose` на 8 ботов.

## 2. Состав поставки (BOM)

### 2.1 Репозиторий (обязателен)

Клон или уже существующий checkout `Seryogapahom/AICM-docs`, ветка `main`.

Минимум дерева:

```
AGENTS.md
README.md
shtab/          ramka.md  celi.md  plan-cikl-2.md
                2026-08-31-lab-as-container.md
                2026-08-31-lab-deploy.md          ← этот файл
razvedka/       + novinki/
sverki/
kontury/
kanon/          + sessions/
```

Закон записи: `AGENTS.md`. Очередь: `shtab/celi.md`. Freeze: `shtab/ramka.md`.

### 2.2 Userland образа (кандидат)

Текущий хост лабы (факт сессии 2026-08-31, не бенчмарк):

| Пакет | Факт на хосте | В образе |
|---|---|---|
| Python | 3.13.5 | тег `python:3.13-slim-bookworm` (кандидат) |
| git | 2.47.3 | `apt git` |
| gh | 2.46.0 (Debian 2.46.0-3) | `gh` ≥ 2.46, GitHub CLI |
| curl | есть | `apt curl ca-certificates` |
| jq | есть | `apt jq` |

**Не класть в образ:** LangGraph, CrewAI, Letta, MAF, Nautilus, Freqtrade, Jesse, Hummingbot, ключи, PAT, `.env`, пакеты `razvedka/`.

Nautilus — не дом (уже пробовали в основной системе). Replay-only только с гипотезой отличия до кода.

### 2.3 Секреты (только Enabler, только runtime env / secret mount)

Имена, не значения. В слои не печь (LC-03).

| Имя | Зачем | Кто даёт |
|---|---|---|
| `GH_TOKEN` | запись архива в `Seryogapahom/AICM-docs` (PAT, сейчас repo-scoped) | Владелец как Enabler |
| `TZ` | циклы 09:00 / 10:00 в Europe/Zurich | ставить `Europe/Zurich` |
| X / MCP | read-only `@acapitalmanager`; GitHub connector | адаптер хоста, не образ |

Нет: live-биржи, Bitget, FRED, cookie браузера, session Grok.

### 2.4 Тома

| Mount | Внутри контейнера | Зачем |
|---|---|---|
| checkout AICM-docs | `/archive` | пакеты, канон-почва, очередь; переживает пересборку образа |
| (опц.) secret file | `/run/secrets/gh_token` | вместо env, если хост так умеет |

Пакеты **не** в image layers (LC-04).

## 3. Рецепт образа (кандидат, не прогон)

Сохранить как `Dockerfile` рядом с checkout **или** собрать из stdin. Новый репозиторий не открывать.

```dockerfile
# Кандидат userland исследовательского центра. Не Hermes. Не identity AICM.
# Образ в сессии 2026-08-31 не собирали.
FROM python:3.13-slim-bookworm

ENV TZ=Europe/Zurich \
    LANG=C.UTF-8 \
    PIP_DISABLE_PIP_VERSION_CHECK=1 \
    PYTHONDONTWRITEBYTECODE=1

RUN apt-get update && apt-get install -y --no-install-recommends \
      ca-certificates curl git jq \
    && curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg \
         -o /usr/share/keyrings/githubcli-archive-keyring.gpg \
    && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" \
         > /etc/apt/sources.list.d/github-cli.list \
    && apt-get update && apt-get install -y --no-install-recommends gh \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /archive
VOLUME ["/archive"]

# Роли запускает хост агентов, не этот entrypoint.
# Userland только держит инструменты архива.
CMD ["sh", "-c", "test -f /archive/AGENTS.md && gh --version && python3 --version && git --version"]
```

Сборка (из каталога, где лежит Dockerfile):

```sh
docker build -t aicm-lab-research-center:candidate .
```

Запуск:

```sh
docker run --rm \
  -e TZ=Europe/Zurich \
  -e GH_TOKEN \
  -v /path/to/AICM-docs:/archive \
  aicm-lab-research-center:candidate
```

`GH_TOKEN` заранее в окружении Enabler. Не писать токен в командную строку-историю, если можно secret-mount.

Проверка живости (LAB-D-03): внутри есть `/archive/AGENTS.md`, `gh auth status` видит `Seryogapahom/AICM-docs`, дерево как в §2.1. Нет — не «развёрнуто».

## 4. Контракт хоста агентов (слой C+D)

Без этого userland — только CLI. Хост должен уметь:

1. Читать `AGENTS.md` **до** любой записи.
2. Держать роли как процессы (не как 8 контейнеров): Штаб, Разведчик, Аналитик, Твиттер, Механик, Тестер, Канонист, Картограф. Трейдера нет.
3. Писать пакеты только в свои папки, GitHub write — только Штаб.
4. Инструменты: открытый веб; `gh api` к AICM-docs; X read-only если адаптер подключен. MCP — узкий allowlist внутри процесса (LC-13, HQ-08), не Typeform/Letta identity.
5. Циклы: пн 09:00 гигиена + HQ-07; будни 10:00 сбор + один шаг переработки + штамп KC (HQ-03). TZ=`Europe/Zurich`.
6. Владелец = External Enabler (логин, оплата, ссылка). Не дизайнер, не ревьюер, не HITL-оператор рынка.
7. Fail-closed: противоречие → `sverki/`, не rewrite `kanon/` (HQ-02). L0–L2 не открывать.

Сегодня этот хост = Grok Bot. Завтра = runtime AICM. Образ от этого не зависит (LC-02).

## 5. Циклы и cron (не боты)

На хосте, не в образе как identity:

```
0 9 * * 1      гигиена AICM-docs + HQ-07
0 10 * * 1-5   суточный цикл (сбор + один инкремент + LAB-D-12)
```

Cron может жить на хосте-адаптере (как сейчас) или в userland позже. Не плодить контейнер «под cron».

## 6. Второй контейнер (не включать)

**LAB-D-04.** Replay Mechanic/Tester = гипотеза (LAB-C-02, LC-15). Compose/k8s — не дом.

Включать **только** если I/O заморожен: спека из `kontury/` + публичный датасет (URL/хэш) → отчёт vs baseline. Без живой трубы, без ключей, без Bitget. Иначе Тестер остаётся процессом в том же контейнере.

Заготовка compose **не** кладём как рабочий файл: это провоцирует 8 сервисов. Если сплит когда-либо понадобится — отдельный пакет штаба, не этот runbook.

## 7. Стоп-лист поставки

| Не делать | Почему |
|---|---|
| 8 образов / 8 Deployments | LC-05, LC-06, LAB-C-01 |
| Печь PAT, `.env`, пакеты, канон в слой | LC-03, LC-04 |
| Ставить CrewAI/Letta/LangGraph/MAF как AICM | LC-07…12 |
| SkyPilot-as-home, exo, RPC-mesh | HOLD |
| Live, Bitget, мемкоин-бот, X write | рамка |
| Новый пустой репо `aicm-lab-image` | PAT только на AICM-docs |
| Playbook / контейнеры Hermes | не эта лаборатория |
| Reopen L0–L2 | нет материального противоречия |
| HITL-оператор / анкета Владельца | HQ-03, Owner = Enabler |
| Считать `docker build` внедрением Foundation | LAB-D-02 |

## 8. Минимальный порядок «взял и поднял»

1. Enabler даёт `GH_TOKEN` (repo `Seryogapahom/AICM-docs`) и при необходимости X/MCP на **хосте-адаптере**.
2. Клонировать склад: `gh repo clone Seryogapahom/AICM-docs` (или mount уже существующего).
3. Прочитать по порядку: `README.md` → `shtab/celi.md` → `shtab/ramka.md` → этот файл → `shtab/2026-08-31-lab-as-container.md` → `razvedka/2026-08-31-research-center-as-container.md`. Не тащить L0–L2 «на всякий случай».
4. Собрать образ из §3 (кандидат). Пока образ не собран — хост Grok уже исполняет роли против того же склада; образ = сменная userland, не условие сегодняшней работы.
5. `docker run` с bind-mount `/archive` и `TZ=Europe/Zurich`.
6. Подключить хост агентов (§4) к `/archive`. Не создавать новых ботов «для масштаба».
7. Прогнать проверку LAB-D-03. Первый рабочий цикл — будни 10:00: один инкремент, не все стратегии.
8. Live не включать. P&L не обещать.

## 9. Протокол обновления (приказ Владельца)

**LAB-D-12.** Этот файл — единственный живой runbook поставки. Штаб обновляет его **в том же инкременте**, если случилось любое из:

- новая роль / смена I/O папки;
- новая зависимость userland (пакет, CLI, версия, без которой развёртывание ломается);
- новый секрет или новый адаптер (имя в таблицу §2.3, значение никогда);
- принят KC, который меняет freeze или стоп-лист;
- сплит порта B (replay) из гипотезы в факт — только отдельным штампом, затем правка §6.

Как писать правку:

1. Не плодить `lab-deploy-v2.md`. Править этот файл, дата в шапке, строка в changelog ниже.
2. Коммит отдельно от пакета разведки: `штаб: поставка — …`.
3. Не выдумывать версии. Нет прогона — писать «кандидат / не собирали».
4. Будни 10:00: если инкремент дня меняет поверхность поставки — штаб **обязан** закрыть день правкой этого файла, иначе инкремент не сдан.
5. Понедельник 09:00: сверка §2.1 с реальным деревом. Дыра в дереве → строка в changelog, не reopen канона.

Changelog:

| Дата | Что изменилось в поставке |
|---|---|
| 2026-08-31 | Первая редакция. Один контейнер. Userland python3.13+git+gh. Секреты снаружи. Образ не собирали. Хост агентов = адаптер (Grok). |

## 10. Связанные пакеты (не склеивать ID)

| Файл | ID | Зачем |
|---|---|---|
| `shtab/2026-08-31-lab-as-container.md` | LAB-C-01…14 | контракт: что копировать |
| `razvedka/2026-08-31-research-center-as-container.md` | LC-01…16 | съём публичных runtime |
| `razvedka/2026-08-31-ai-questionnaire-ecosystems.md` | QE-* / HQ-01…08 | чипы поведения |
| этот файл | LAB-D-* | как поднять и чем обновлять |

## 11. Дыры (не закрывать выдумкой)

- Образ не собирали, не публиковали registry. Тег `python:3.13-slim-bookworm` не прогнан.
- Нет доказанного replay-sidecar.
- Хост агентов (слой D) в AICM ещё не выбран — и не должен выбираться вендором из LC-07…12.
- Mac Studio — ожидаемый хост, не требование этого файла.
- MCP-SaaS не подключать как identity.
