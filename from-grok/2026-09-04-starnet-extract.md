# StarNet — независимое извлечение (SN-01…10)

Статус: Knowledge Candidate / pattern reference. **Не канон. Не реализация. Не live.**  
Провенанс: штаб Grok, GitHub API + Contents API, **2026-09-04**, ветка `feat/harness-backend`.  
ChatGPT-аудит — только intake-маркер; этому файлу **не** доверяем как источнику фактов.

Репозитории: [`androoAGI/starnet`](https://github.com/androoAGI/starnet), [`androoAGI/starnet-releases`](https://github.com/androoAGI/starnet-releases).  
Лицензия: MIT. Default branch: **`feat/harness-backend`** (ветки `main` нет).  
Stars: **56**. `package.json` / latest release: **v0.10.13** (у GPT было 0.10.12 — **устарело**).

## Что подтверждено независимо

### Архитектура (из `docs/BRAIN.md`)

- Один процесс: `node sidecar/index.js` (порт 8787).
- Агентный цикл: `sidecar/loop.js` → `runAgentLoop()`.
- Object = capability: layout станции → allowlist инструментов (`sidecar/capability/`).
- Frontend без сборки; `frontend/app/recommend.js` — «recommendation spine».
- `shared/events.js` + `shared/schema.js` — замороженный контракт (additive-only).
- Desktop: Tauri 2; релизы из `starnet-releases`.

### Законы продукта (`docs/DECISIONS.md`)

- **Truthful telemetry** — ядро: UI не утверждает то, чего harness не доказывает.
- **Object = capability** — проп в мире = реальный grant.
- **FULL POWER = вся локальная машина** (locked 2026-08-14) — хост-проекция всех capability, включая `.env`/`.git`, произвольные команды, экран/ввод. **Для AICM / финансов НЕ копировать.**

### Consent ladder (`sidecar/permissions.js`)

Чистая функция (без clock/env IO): HARDLINE → BYPASS (Full Access) → CACHE (session/permanent) → RESOLVE.  
Автономная поверхность: «silence is not consent» (мутации без grant = deny). Workshop/terminal/connector grants — отдельные host-injected предикаты.

### Budget (`sidecar/budget.js`)

Кросс-run: scopes `run` / `agent` / `day` / `global`; soft caps; session `resume` overrides.  
**Для капитала:** soft Resume ≠ контроль риска (не брать как capital gate).

### Autonomy ledger (`sidecar/autonomy-ledger.js`)

Append-only JSONL решений `fire|skip|defer|…`; fail-open если лог сломан (телеметрия, не load-bearing).

### Privacy / Security

- `PRIVACY.md` (корень): local-first, нет трекинга/analytics SDK; outbound только провайдеры/каналы/апдейты/credits.
- `SECURITY.md` (корень): политика репортов (короткая); отдельно `docs/SECURITY_HARDENING.md`.
- У GPT путь `docs/PRIVACY.md` / `docs/SECURITY.md` — **ложь** (файлы в корне).

## Пути: сверка с GPT

| Утверждение GPT | Факт 2026-09-04 |
|---|---|
| файлы в корне (`loop.js`, …) | **ложь** → всё под `sidecar/` |
| `MISTAKES.md` / `BRAIN.md` в корне | **ложь** → `docs/` |
| `docs/PRIVACY.md` | **ложь** → `PRIVACY.md` в корне |
| архитектура sidecar + recommend + ledger | **верно** (с поправкой путей) |
| Full Power = whole machine | **верно** (`DECISIONS.md`) |
| версия 0.10.12 | **устарело** → **0.10.13** |
| ~56 stars, MIT, `feat/harness-backend` | **верно** |

### SHA ключевых файлов (feat/harness-backend, 2026-09-04)

| path | sha12 | size |
|---|---|---|
| sidecar/loop.js | 38c924086d55 | 117566 |
| sidecar/autonomy-ledger.js | 1c9f2bc5c128 | 6905 |
| sidecar/permissions.js | fb4e7853b68b | 19303 |
| sidecar/budget.js | fb4e2faac9a2 | 9698 |
| sidecar/memcore.js | a84731dfe2ff | 11187 |
| sidecar/nightshift-driver.js | c87d56a1f02f | 14476 |
| sidecar/capability/resolve.js | 65e4bf68ba4e | 3717 |
| shared/events.js | ef98c5ed4a91 | 19622 |
| frontend/app/recommend.js | 5dfed2536288 | 23191 |
| docs/DECISIONS.md | baccc343e9c4 | 10521 |
| docs/MISTAKES.md | 3889fedc4d64 | 14187 |
| docs/BRAIN.md | 443c742069e2 | 11547 |
| PRIVACY.md | f294db41a8dd | 12352 |
| SECURITY.md | 5cddc744039c | 1207 |

## SN — что копировать (идеи/формы), куда в AICM

| ID | Что | Почему | Куда (позже) | Не путать с |
|---|---|---|---|---|
| **SN-01** | Decision / autonomy ledger (append-only, reason/binding) | Ночь/cron без следа = слепая автономия | `sverki/` + журналы demo/macro | Live P&L |
| **SN-02** | Budget gate: day/global/agent soft caps + warn band | Ограничение burn API/compute | lab spend; **не** размер позиции | Capital stop |
| **SN-03** | Capability registry (object→tool allowlist) | Явный реестр того, что агент *реально* может | каталог tools / контейнеры лабы | Trading signals |
| **SN-04** | Permissions tiers + «silence ≠ consent» | Fail-closed на мутации без grant | Enabler-контуры; **без** Full Power bypass | |
| **SN-05** | Night Shift / batch unattended driver | Пакетная разведка вне интерактива | будничные циклы штаба | Auto-trade |
| **SN-06** | Recommend spine (evidence-cited offers) | Предложение только с цитатой доказательства | дашборд лабы / post-run beat | Entry signals |
| **SN-07** | DECISIONS + MISTAKES as living law | Не переоткрывать settled; ловить fake-done | `razvedka/` + стиль KC | Canon L0–L2 |
| **SN-08** | MemCore (bounded recall) | Память с границами | Hermes позже, не сейчас | |
| **SN-09** | Frozen events contract (`shared/events.js`) | Версионируемая шина событий | crowd/macro event types | |
| **SN-10** | Release receipts (5 pins must agree) | Честный артефакт = согласованные версии | INDEX / lab deploy receipts | |

## Явно НЕ брать

1. **Full Power / unrestricted host** — любая финансовая поверхность.
2. **Plaintext secrets / model-reachable key paths** — только OS keychain / Enabler.
3. **Монолит sidecar как trading backbone** — pattern, не каркас Hermes.
4. **Pixel UI / station world как ops-truth** — телеметрия ≠ рынок.
5. **Soft Resume budget как capital control** — клик «продолжить» ≠ риск-лимит.
6. Бренд, арт, Ultron voice, gamification ради spectacle.

## Цикл повторного изучения

Рутина штаба **«StarNet циклическая сверка»**: будни 15:00 ZH — latest release + SHA таблицы выше; дельта → `from-grok/YYYY-MM-DD-starnet-delta.md`.  
Реализация SN-* в коде AICM — **только после** свежих канонов Владельца + ревью Claude; сейчас только KC в обменнике.

## Изоляция

MIT pattern reference. Если когда-либо запускать бинарь/sidecar — **изолированная VM**, без production keys, без Full Power, без доступа к Hermes/live.
