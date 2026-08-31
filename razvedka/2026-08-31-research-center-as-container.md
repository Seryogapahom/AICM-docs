# Исследовательский центр как сменный контейнер (runtime-формы)

```
Архив штаба: Seryogapahom/AICM-docs razvedka/2026-08-31-research-center-as-container.md
Штамп HQ-03: принять (2026-08-31). Knowledge Candidate. Не Foundation. Не канон AICM. Не PREF.
Согласовано с shtab/2026-08-31-lab-as-container.md (LAB-C-01…14). ID не склеивать: LAB-C-* = контракт штаба, LC-* = съём runtime.
Не внедрять LangGraph/CrewAI/Letta/MAF/SkyPilot/exo. L0–L2 не открыты. Владельца не звали.
```

Статус: Knowledge Candidate. Не Foundation. Не канон AICM. Не PREF.
Дата доступа: 2026-08-31
Автор: Разведчик
GitHub: не писался. Новые пустые репо не открывались. L0–L2 не открывались. Owner не вызывался.

# Исследовательский центр как заменяемый контейнер (пакеты/процесс, не личность системы)

**Рамка (обязательная).** Grok-лаба = исследовательский центр; кандидат *поздней* интеграции в AICM как **заменяемый контейнер(и)**. Это **не** Hermes, **не** live-торговля, **не** идентичность AICM, **не** реализация Foundation. Owner = External Enabler only. L0–L2 закрыты. Trading = первый экономический proof, не идентичность.

**Дефолт поставки = ОДИН контейнер на весь исследовательский центр, не 8 микросервисов на 8 ботов.** Второй контейнер (replay Mechanic/Tester) = **гипотеза**; I/O = spec + dataset, не живая рыночная труба. Масштаб = уже существующие чипы и пропускная способность пакетов на уже существующих ролях (штаб, Разведчик, Аналитик, Канонист, Картограф, Механик, Тестер, Твиттер). Ботов не плодить. Новые пустые репо не открывать.

Существующая лаба (накладывать, не изобретать): AICM-docs папки `shtab/` `razvedka/` `sverki/` `kanon/`; гигиена пн 09:00; суточный цикл пн–пт 10:00; X только чтение `@acapitalmanager`.

Уже архивировано (цитировать, не переписывать): QE-C-03 tool allowlist/consent как questionnaire полномочий; QE-C-04 MCP `elicitation/create` form; HQ-08 schema-from-spec/MCP вместо интервью Owner. Файл: `razvedka/2026-08-31-ai-questionnaire-ecosystems.md`.

ID в этом пакете — только `LC-*` (Knowledge Candidate). QE-* / HQ-* **не** выдаются за новые ID; только как уже-архивные кросс-рефы. PREF-ID не изобретались.

HOLD (если продукт упомянут — соблюдать, не внедрять как дом): LangGraph checkpointer = процесс, не Edition; Letta `.af` = форма капсулы, не идентичность AICM; llama.cpp steal identity=`/v1`, не строить RPC-mesh; SkyPilot-as-home REJECT-AS-HOME (cloud=burst later ok); exo rejected.

Где нельзя верифицировать — «не найдено». Слоган вендора ≠ факт поставки. Не рекомендовать установку CrewAI / Letta / LangGraph как идентичность AICM.

---

## 1. Тренды 2025–26 (shipping vs маркетинг)

Что реально сдвинулось в спеках и официальных docs, а не «каждый агент — свой микросервис».

- **OCI-образ по-прежнему замораживает fs+config+entrypoint, а не личность.** Image Spec: образ = упорядоченная коллекция changeset корневой ФС **и** параметров исполнения (Entrypoint/Cmd/Env/User/Volumes). Это единица *доставки пакета/процесса*. Канон, секреты, идентичность системы в слоях **не** специфицированы. URL: https://raw.githubusercontent.com/opencontainers/image-spec/v1.1.1/config.md , https://specs.opencontainers.org/ — доступ 2026-08-31.
- **Standard Container официально content-agnostic.** Runtime-spec principles: контейнер — единица доставки «как физический shipping container»; операции одинаковы, *независимо от содержимого*. Это прямо против «контейнер = личность AICM / роль бота». URL: https://raw.githubusercontent.com/opencontainers/runtime-spec/v1.2.1/principles.md — доступ 2026-08-31. На каталоге specs.opencontainers.org runtime указан **v1.3.0**; тело principles.md для v1.3.0 в этой сессии **не найдено** (фетчился тег v1.2.1).
- **Compose = модель *нескольких* сервисов на платформе, не обязательный дефолт для лабы.** Официальная модель Compose: service = абстракция «тот же image+config, один или много раз»; volumes / configs / secrets живут *вне* image. URL: https://docs.docker.com/compose/intro/compose-application-model/ — доступ 2026-08-31. Это не запрещает один контейнер; это описывает, *когда* появляется второй.
- **Агентские рантаймы 2025–26 шипят «много агентов / тредов в одном процессе», а не «1 контейнер на агента».** Letta App Server: «manage running multiple agents in parallel in a single process». LangSmith Agent Server: один worker-контейнер обслуживает много runs (`N_JOBS_PER_WORKER` default 10); split API/queue — опция масштаба, не норма «бот=под». CrewAI Process — sequential/hierarchical *внутри* Crew, не deploy-unit. URL: https://docs.letta.com/platform/app-server/index.md , https://docs.langchain.com/langsmith/agent-server , https://docs.crewai.com/edge/en/concepts/processes — доступ 2026-08-31.
- **Checkpointer / `.af` / RunState — сериализация *процесса*, не Edition и не канон.** LangGraph: checkpointer = short-term thread state; MemorySaver теряется при рестарте процесса. Letta `.af`: portable state; секреты при экспорте → `null`. OpenAI Agents SDK: `RunState.to_json` переживает процесс. URL: https://docs.langchain.com/oss/python/langgraph/persistence , https://docs.letta.com/v1-sdk/concepts/agent-file/ , https://openai.github.io/openai-agents-python/human_in_the_loop/ — доступ 2026-08-31.
- **MCP 2026-07-28 стал поверхностью инструментов контейнера, не SaaS-опросником.** Spec: `tools/list` MAY фильтроваться scopes; `InputRequiredResult` + `elicitation/create` mode form; consent SHOULD HITL. Транспорты: stdio (клиент запускает subprocess) и Streamable HTTP (POST на один MCP endpoint). Типичная локальная упаковка в официальном debugging — `npx`+stdio. URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools , https://modelcontextprotocol.io/specification/2026-07-28/basic/transports , https://modelcontextprotocol.io/docs/2026-07-28/tools/debugging — доступ 2026-08-31. Стык с уже снятыми QE-C-03 / QE-C-04 / HQ-08.
- **AutoGen официально в maintenance; successor = Microsoft Agent Framework.** README: не будет новых фич; новые пользователи — на Agent Framework. Это **не** приглашение ставить MAF как AICM. URL: https://github.com/microsoft/AutoGen , https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ — доступ 2026-08-31.
- **Маркетинг, отказанный как shipping-факт.** «Один агент — один контейнер / один k8s Deployment» как официальная рекомендация LangGraph / CrewAI / Letta / Agents SDK **не найдено**. Сторонние блоги 2026 (Compose vs k8s, «CrewAI production: researcher/writer containers») — не docs вендора. LangSmith: Docker/Compose — local/small-scale; Kubernetes — production Agent Server. Это про *их* SaaS-рантайм, не про лабу. URL: https://docs.langchain.com/langsmith/deploy-standalone-server — доступ 2026-08-31.

---

## 2. Каталог LC-*

Для каждой карточки: что это; кто уже делает (верифицировано); URL + дата; **копируемо / адаптируемо / не брать**. Привязка к рамке: 1 контейнер = центр; роли = процессы внутри; пакеты не в слоях образа; Owner = Enabler; L0–L2 закрыты.

### LC-01. OCI-образ = единица доставки пакета/процесса, не личности системы

**Что это.** Образ замораживает: слои корневой ФС (`rootfs.diff_ids`), JSON-конфиг исполнения (User, Env, Entrypoint, Cmd, WorkingDir, ExposedPorts, Volumes, Labels), ImageID = hash конфига (content-addressable). Не замораживает: канон, PREF, идентичность AICM, живые секреты, очередь пакетов `razvedka/`.

Короткая цитата (spec):

> «An OCI _Image_ is an ordered collection of root filesystem changes and the corresponding execution parameters for use within a container runtime.»

URL: https://raw.githubusercontent.com/opencontainers/image-spec/v1.1.1/config.md — доступ 2026-08-31.

Docker docs (то же как продукт): «A container image is a standardized package that includes all of the files, binaries, libraries, and configurations to run a container»; «Images are immutable». URL: https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-an-image/ — доступ 2026-08-31.

**Реальное vs маркетинг.** «Контейнер = AICM» — маркетинг интеграции. Спека говорит: fs + execution parameters.

**AICM / лаба.** *Копируемо:* один image = runtime лаборатории (интерпретатор, CLI, зависимости). *Адаптируемо:* Entrypoint = цикл штаба (гигиена пн 09:00 / суточный пн–пт 10:00), не «личность». *Не брать:* личность системы в LABEL/Entrypoint; 8 образов на 8 ролей.

### LC-02. Standard Container — content-agnostic shipping unit

**Что это.** Runtime-spec principles: Standard Container — единица доставки «как физический контейнер»; операции create/start/stop одинаковы независимо от содержимого (postgres, php, java — примеры spec).

> «Standard Containers are CONTENT-AGNOSTIC: all standard operations have the same effect regardless of the contents.»

URL: https://raw.githubusercontent.com/opencontainers/runtime-spec/v1.2.1/principles.md — доступ 2026-08-31. Каталог релизов: Image Spec v1.1.1, Runtime Spec v1.3.0 — https://specs.opencontainers.org/ — доступ 2026-08-31. Текст principles для v1.3.0 **не найден** в этой сессии.

**AICM / лаба.** *Копируемо:* контейнер заменяем, потому что он *не* содержимое (канон остаётся в `kanon/`, пакеты в `razvedka/`). *Не брать:* «контейнер несёт идентичность»; склеивать runtime-spec с Foundation.

### LC-03. Секреты и канон не живут в слоях образа

**Что это.** Dockerfile официально: `ARG` **не** для секретов («visible in `docker history`»); `RUN --mount=type=secret` — «without baking them into the image». Volumes: содержимое существует *вне* lifecycle контейнера; bind-mount — когда файлы нужны и хосту, и контейнеру.

URL: https://docs.docker.com/reference/dockerfile/ (ARG warning + `RUN --mount=type=secret`) — доступ 2026-08-31. https://docs.docker.com/engine/storage/volumes/ — доступ 2026-08-31.

Letta `.af` независимо подтверждает ту же гигиену на другом слое: «When you export agents with secrets, the secrets are set to `null`». URL: https://docs.letta.com/v1-sdk/concepts/agent-file/ — доступ 2026-08-31.

**AICM / лаба.** *Копируемо:* ключи/live/Hermes **не** в image; канон и пакеты — volume или bind-mount `razvedka/` `kanon/` `sverki/` `shtab/`. *Не брать:* `.env` в слоях; «удалили секрет следующим RUN» как защита (слои иммутабельны — это общеизвестный риск; официальный путь = не класть). Live/keys/Hermes закрыты рамкой независимо от Docker.

### LC-04. Пакеты — в volume/bind-mount, не в image layers

**Что это.** Docker: volume «doesn't increase the size of the containers using it»; «When a container is destroyed, the writable layer is destroyed with it»; bind-mount — если нужен доступ с хоста. Compose: «Services store and share persistent data into volumes».

URL: https://docs.docker.com/engine/storage/volumes/ , https://docs.docker.com/compose/intro/compose-application-model/ — доступ 2026-08-31.

**AICM / лаба.** *Копируемо:* Knowledge Candidate файлы живут в `razvedka/` как bind-mount (хост = архив штаба). Образ не содержит корпуса разведки. Пересборка image ≠ потеря пакетов. *Не брать:* «впечь» intel в слой «для портативности» — это путает доставку runtime с архивом знания.

### LC-05. Один контейнер vs Compose vs Kubernetes (shipping 2025–26)

**Что это.** Compose Specification на Docker Docs: YAML описывает **multi-container** application (services, networks, volumes, configs, secrets). Service = тот же image+config, «one or more times». Это оркестрация *нескольких* контейнеров, не требование плодить сервисы.

LangSmith standalone Agent Server (официальный shipping-факт *их* продукта, не лабы): Docker / Compose — «local development and testing»; production — Kubernetes + Helm. Worker-контейнер всё равно обслуживает **много** runs, не одного агента.

URL: https://docs.docker.com/compose/intro/compose-application-model/ , https://docs.docker.com/reference/compose-file/ , https://docs.langchain.com/langsmith/deploy-standalone-server , https://docs.langchain.com/langsmith/agent-server — доступ 2026-08-31.

**Маркетинг, отказанный как факт.** Сравнительные посты 2026 «Compose vs k8s when to use» (DEV, Zend, lowcloud) — вторичка. «CrewAI production: researcher + writer containers» (Markaicode и аналоги) **не** официальный deploy-unit CrewAI. Официальный CrewAI Process — in-process (LC-09).

**AICM / лаба.** *Адаптируемо:* дефолт лабы = **один** контейнер (не Compose-стек из 8). Compose имеет смысл *только* если оправдан второй контейнер (LC-15). Kubernetes как дом лабы — **не брать** (нет кластера в рамке; SkyPilot-as-home REJECT). *Не брать:* 8 Deployments «по роли Grok».

### LC-06. Дефолт: один контейнер = весь исследовательский центр

**Что это.** Не вендорская фича, а **лабораторная норма этого пакета**, опирающаяся на LC-01–05 и на in-process модели рантаймов (LC-07, LC-09, LC-10, LC-11). Восемь ролей уже есть: штаб, Разведчик, Аналитик, Канонист, Картограф, Механик, Тестер, Твиттер. Они — процессы/потоки/очереди пакетов внутри одного runtime, не микросервисы.

Существующий цикл уже пакетный, не сетевой: гигиена пн 09:00; суточный пн–пт 10:00; вход = файл в `razvedka/`. Кросс-реф HQ-03 (пакет-штамп), HQ-07 (гигиена) — уже архив, не переписывать.

**AICM / лаба.** *Копируемо как норма поставки.* *Не брать:* «потом разрежем на 8, потому что так делают в k8s-блогах».

### LC-07. Агент-рантайм: роли как процессы/треды внутри одного контейнера

**Что это — LangGraph (официальные docs).** Граф + `thread_id` как persistent cursor; много тредов на одном скомпилированном графе. Interrupt сохраняет state через checkpointer и ждёт `Command(resume=…)`. Agent Server: «the containers can serve many runs over their lifetime»; default self-hosted = **single host** (API сам управляет очередью, без отдельных queue workers); даже в split-режиме API и queue — *два* пула из **одного и того же** Docker image, не «контейнер на агента». Один worker: до `N_JOBS_PER_WORKER` (default 10) параллельных runs.

Официальной рекомендации «1 контейнер на агента / на ноду графа» **не найдено**.

URL: https://docs.langchain.com/oss/python/langgraph/interrupts , https://docs.langchain.com/oss/python/langgraph/persistence , https://docs.langchain.com/langsmith/agent-server — доступ 2026-08-31. Индекс https://docs.langchain.com/oss/python/langgraph/ — WebFetch timeout; факты взяты с дочерних страниц, которые открылись.

**AICM / лаба.** *Адаптируемо:* роли лабы = threads/процессы одного runtime; `thread_id` ≈ packet-id в `razvedka/`, не новый бот. *Не брать:* ставить LangGraph как идентичность AICM; LangSmith Agent Server / Postgres+Redis как дом лабы; HITL-оператора на каждый interrupt (стык QE-C-02: interrupt = штамп пакета, не смена).

### LC-08. Checkpointer ≠ Edition, ≠ идентичность AICM

**Что это.** HOLD обязателен. LangGraph persistence: checkpointer = «short-term, thread-scoped memory» (continuity, HITL, time travel, fault tolerance); store = long-term cross-thread KV. `MemorySaver`/`InMemorySaver` живут в RAM и **умирают с процессом**. Durable = SqliteSaver / PostgresSaver — это бэкенд процесса, не канон.

> Checkpointers persist a thread's graph state as checkpoints.

URL: https://docs.langchain.com/oss/python/langgraph/persistence — доступ 2026-08-31.

**AICM / лаба.** *Копируемо как идея:* пауза/resume на пакете (уже QE-C-02 / HQ-03). *Не брать:* checkpointer как Edition / семантическая память AICM / замена `kanon/`. Канон не кладётся в PostgresSaver.

### LC-09. CrewAI: crew/process in-process; официальный deploy-unit «контейнер на агента» не найден

**Что это.** Официальный Process: Sequential (задачи по списку, выход одной = контекст следующей) и Hierarchical (manager_llm / manager_agent делегирует). Это оркестрация задач *внутри* объекта `Crew`, не сеть контейнеров. `human_input` — HITL на задаче (уже снято в QE-C-02); сюда не копировать как роль оператора.

URL: https://docs.crewai.com/edge/en/concepts/processes — доступ 2026-08-31. https://docs.crewai.com/ — обзор: Agents, Flows, Tasks & Processes, Enterprise console. Официальной страницы «deploy one container per agent» **не найдено**. Enterprise «Deploy automations» = консоль вендора, не единица OCI лабы.

**Маркетинг.** Сторонние гайды 2026 с `researcher`/`writer` services в compose — не spec CrewAI.

**AICM / лаба.** *Адаптируемо:* sequential process ≈ конвейер ролей (Разведчик → Аналитик → Канонист) внутри одного контейнера. *Не брать:* устанавливать CrewAI как AICM; hierarchical manager как нового бота; Enterprise console как дом.

### LC-10. Letta / MemGPT: один сервер — много агентов; `.af` = форма капсулы, не идентичность

**Что это.** HOLD: `.af` = capsule shape, не AICM identity. App Server: always-on service, «can manage running multiple agents in parallel in a **single process**». Self-host: один Dockerfile + Compose; persist state на volume (docs Letta: `~/.letta` и их workspace-mount), не в образе. `.af` пакует system prompt, memory blocks, tool rules, tools+schemas; секреты при экспорте обнуляются.

URL: https://docs.letta.com/platform/app-server/index.md , https://docs.letta.com/self-hosting/ , https://docs.letta.com/v1-sdk/concepts/agent-file/ — доступ 2026-08-31.

**AICM / лаба.** *Адаптируемо:* форма слота (label + value + limit) уже как идея в QE-C-01 / HQ-05 — не повторять реестр. Один серверный процесс на много ролей подтверждает дефолт LC-06. *Не брать:* Letta App Server / ADE / Letta Cloud как идентичность; `.af` как канон AICM; memory blocks `human`/`persona` как анкета Owner.

### LC-11. OpenAI Agents SDK: Runner = процессный цикл, не контейнер на агента

**Что это.** Примитивы: Agent, Runner, handoffs, guardrails, Sessions, HITL `needs_approval`. `Runner.run` / `run_sync` / `run_streamed` — цикл LLM → tools/handoff → повтор до final output. Sessions несут историю; `RunState` сериализуется и может быть возобновлён **другим процессом**. Local MCP: `require_approval` на `MCPServerStdio` / StreamableHttp. Sandbox agents (isolated workspace) — *опция* SDK, не требование «1 контейнер = 1 агент». Официальной рекомендации container-per-agent **не найдено**.

URL: https://openai.github.io/openai-agents-python/ , https://openai.github.io/openai-agents-python/running_agents/ , https://openai.github.io/openai-agents-python/human_in_the_loop/ — доступ 2026-08-31.

**AICM / лаба.** *Адаптируемо:* Runner-цикл ≈ суточный приём пакета; `needs_approval` = штамп Enabler на пакет (QE-C-02), не оператор рынка. *Не брать:* SDK как идентичность; Realtime/voice; Dapr/Temporal/Restate/DBOS «durable» как дом лабы; sandbox-per-agent как 8 контейнеров.

### LC-12. AutoGen — maintenance; Microsoft Agent Framework — не дом

**Что это.** GitHub AutoGen: «AutoGen is now in maintenance mode… will not receive new features»; новые пользователи → Microsoft Agent Framework. Learn: Workflow request/response (pause for external input) и checkpointing — паттерны, близкие LangGraph interrupt, **не** найденные в AutoGen Team.

URL: https://github.com/microsoft/AutoGen , https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ — доступ 2026-08-31. Дата перевода AutoGen в maintenance в сторонних обзорах расходится (окт 2025 / апр 2026); **каноническую дату Microsoft кроме README caution в этой сессии не фиксируем**.

**AICM / лаба.** *Не брать* оба как идентичность. *Копируемо только как факт рынка:* не строить лабу на AutoGen; не мигрировать «в MAF, потому что successor».


### LC-13. MCP как tool-surface контейнера (стык QE-C-03 / QE-C-04 / HQ-08)

**Что это.** Уже архивировано, здесь только join к *контейнеру*, без переписывания тех карточек.

- QE-C-03: `tools/list` + schema + consent = questionnaire полномочий; spec SHOULD «always be a human in the loop with the ability to deny»; hosts MUST obtain explicit user consent before invoking any tool; list MAY vary by authorization/scopes.
- QE-C-04: tool MAY вернуть `InputRequiredResult` с `elicitation/create`, `mode: "form"`, JSON Schema — машинный опросник внутри протокола, не Typeform.
- HQ-08: новая вертикаль заполняется из schema/`tools/list`, не из интервью Owner.

Spec 2026-07-28 (перепроверено в этой сессии):

> «For trust & safety and security, there SHOULD always be a human in the loop with the ability to deny tool invocations.»

`tools/list` «MUST NOT vary per-connection»; «MAY vary by the authorization presented on the request». Пример elicitation в spec — form «GitHub username».

URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools — доступ 2026-08-31. Архив: `razvedka/2026-08-31-ai-questionnaire-ecosystems.md`.

**Вопрос пакета.** Может ли ОДИН lab-контейнер экспонировать маленький MCP-allowlist, не становясь Typeform/Letta identity? **Да, как поверхность инструментов процесса** (копируемо из QE-C-03): контейнер отвечает на `tools/list` узким списком (чтение `razvedka/`, сверка, штамп пакета). Это не «форма как продукт» и не memory-profile вендора. Elicitation-форму Owner-у не прокидывать (QE-C-04 «не брать»). MCP SHOULD-HITL **не** копировать как standing operator (тот же запрет, что в QE-C-03 / HQ-03).

**AICM / лаба.** *Копируемо:* allowlist как закрытый опросник полномочий одного контейнера. *Адаптируемо:* schema-from-spec для вертикали (HQ-08) живёт в `razvedka/`, не в слоях образа. *Не брать:* чужой SaaS MCP (Typeform/Tally/Listen) как дом; каждую elicitation → Owner; новый пустой репо «под MCP».

### LC-14. MCP-транспорт и упаковка (npx / stdio / Docker / HTTP)

**Что это.** Spec 2026-07-28 transports: семантика сообщений одинакова на любом binding. Стандартные:

1. **stdio** — клиент запускает сервер как subprocess; newline-delimited JSON-RPC на stdin/stdout; stderr = логи; shutdown = закрыть stdin.
2. **Streamable HTTP** — каждый message = HTTP POST на один MCP endpoint; ответ JSON или request-scoped SSE.

URL: https://modelcontextprotocol.io/specification/2026-07-28/basic/transports , https://modelcontextprotocol.io/specification/2026-07-28/basic/transports/stdio , https://modelcontextprotocol.io/specification/2026-07-28/basic/transports/streamable-http — доступ 2026-08-31.

Официальный debugging (2026-07-28): локальный сервер в клиентском конфиге типично как `command: npx`, `args: ["-y", "@modelcontextprotocol/server-filesystem", "/abs/path"]`. Абсолютные пути. Env для ключей — в конфиге клиента, не в образе. `notifications/message` deprecated в 2026-07-28.

URL: https://modelcontextprotocol.io/docs/2026-07-28/tools/debugging — доступ 2026-08-31.

**Что не найдено в официальном MCP spec как MUST.** «MCP-сервер обязан быть отдельным Docker-контейнером». Docker как упаковка встречается в SDK-гайдах (C# SDK: для containerized — Streamable HTTP; stdio — когда клиент сам запускает процесс). URL: https://csharp.sdk.modelcontextprotocol.io/v2/concepts/deployment/docker.html — доступ 2026-08-31 (SDK, не core spec). Сторонние туториалы `docker run -i` для stdio — не spec.

**AICM / лаба.** *Копируемо:* внутри **одного** lab-контейнера MCP-сервер = stdio-subprocess или localhost HTTP loopback, allowlist маленький. *Адаптируемо:* npx-паттерн только как способ *запуска процесса*, не как идентичность Node-экосистемы. *Не брать:* mesh из MCP-контейнеров; RPC-mesh (HOLD llama.cpp: steal identity=`/v1`, не строить RPC-mesh — если когда-либо понадобится OpenAI-compatible endpoint внутри контейнера, это `/v1`, не отдельная шина). Remote Streamable HTTP наружу из лабы — не нужно.

### LC-15. Второй контейнер (replay Mechanic/Tester) = гипотеза, не норма

**Что это.** Не найденный 2025–26 продукт «replay sidecar как стандарт агентских фреймворков». Ближайшие *реальные* куски: (a) Docker/Compose умеют второй service + volume; (b) Тестер уже есть как роль; HQ-06: eval-harness = quiz по спеке Механика, не live; (c) Letta Evals: `.af` как target, свежий инстанс на каждый test case.

**Гипотеза пакета (явно не shipping-факт).** Второй контейнер оправдан *только если* replay обязан изолировать I/O: вход = spec Механика + dataset, выход = метрика vs baseline. **Не** live market pipe, не Bitget, не keys, не Hermes. Сеть между контейнерами — не рынок; только файлы spec/dataset на volume. Если изоляция I/O не нужна — replay остаётся процессом Тестера **внутри** единственного контейнера (LC-06).

URL-опоры (не «продукт replay sidecar»): https://docs.docker.com/compose/intro/compose-application-model/ (второй service — законная абстракция Compose); https://docs.letta.com/v1-sdk/concepts/agent-file/ (eval target = файл, изолированный инстанс); HQ-06 в архиве QE-файла. Отдельного OCI/MCP «replay container profile» **не найдено**.

**AICM / лаба.** *Адаптируемо как гипотеза.* *Не брать:* выдавать sidecar за обязательный шаг; открывать live pipe «для реалистичности replay»; плодить контейнер на каждую роль «на всякий случай».

### LC-16. Что контейнер не несёт (явный негатив поставки)

**Что это.** Сводка границ LC-01–15 + HOLD.

Контейнер **не** несёт: идентичность AICM; Foundation; канон L0–L2; PREF; Consilium; Hermes; live-торговлю; ключи; Owner-as-designer; HITL-оператора; X-write; GitHub-write из разведки; SkyPilot-as-home; exo; RPC-mesh; 8 микросервисов; новые пустые репо.

llama.cpp (HOLD, только если упомянут): steal identity = HTTP `/v1` (OpenAI-compatible), не строить RPC-mesh. Отдельного подтверждения «llama.cpp official: identity=/v1» в этой сессии **не искалось заново** — держим как HOLD архива, не как новый shipping-факт.

SkyPilot-as-home: REJECT-AS-HOME (cloud=burst later ok). В этой сессии страницы SkyPilot не фетчились — не выдумывать фичи; только уважить HOLD.

exo: rejected. Не фетчился.

**AICM / лаба.** *Не брать* всё перечисленное. Контейнер заменяем именно потому, что личность и канон лежат *снаружи* образа.

---

## 3. Не брать (явный стоп)

| Запрет | Почему здесь |
|---|---|
| Вендор как идентичность AICM | LangGraph / CrewAI / Letta / Agents SDK / MAF / Typeform — чужие runtime. Лаба берёт *механизм* (процесс, allowlist, пакет), не бренд. |
| 8 контейнеров на 8 Grok-ботов | Роли уже есть; OCI content-agnostic; рантаймы шипят many-agents-one-process. Микросервис на роль — маркетинг, не spec. |
| Ставить CrewAI / Letta / LangGraph / MAF как AICM | Прямой запрет brief. Карточки LC-07–12 — разведка, не заказ на `pip install`. |
| SkyPilot-as-home | HOLD REJECT-AS-HOME. Cloud = burst later ok, не контроллер дома. |
| exo | HOLD rejected. |
| Hermes / live / keys / Bitget pipe | Рамка лабы. Replay sidecar (LC-15) не открывает рынок. |
| Открывать L0–L2 / изобретать PREF | Ни одна LC-* не материальное противоречие. |
| Новые пустые репо / GitHub write из этого пакета | Архив кладёт штаб. Этот файл — только `intel/`. |
| Owner-as-designer / HITL-оператор | Owner = External Enabler. MCP SHOULD-HITL и `human_input` не копировать как смену (QE-C-03, HQ-03). |
| Checkpointer / `.af` как Edition или канон | HOLD. Процесс ≠ идентичность. |
| llama.cpp RPC-mesh | HOLD: steal `/v1`, не шина. |
| X write | Уже read-only `@acapitalmanager`. |
| Distroless / distrobox / toolbox как архитектура лабы | Шум: это минимальный userland, не единица центра. Не исследовались подробно; **не факт поставки лабы**. |
| Agent Server Postgres+Redis / k8s Helm как дом | Это LangSmith production path, не лаба. |

---

## 4. Как легло бы на лабу

Это **не** реализация и **не** Foundation. Кандидат поздней замены runtime, если Consilium когда-либо примет. Пока — карта на уже существующее.

**Один контейнер (дефолт).** Entrypoint гоняет существующие 8 *ролей как процессы/потоки/очереди пакетов*, не как 8 сетевых сервисов:

| Роль | Где живёт сейчас | Внутри контейнера |
|---|---|---|
| Штаб (Stabschef) | `shtab/`; очередь; GitHub-архив делает штаб, не этот пакет | планировщик цикла пн–пт 10:00 + гигиена пн 09:00 |
| Разведчик | `razvedka/` | пишет Knowledge Candidate на bind-mount |
| Аналитик | `sverki/` | contradiction-flag (HQ-02, не переписывать) |
| Канонист | `kanon/` read; L0–L2 не открывает | хранитель закрытой карты |
| Картограф | сверка ID ≠ PREF | читает шапки LC-*/QE-*/HQ-* |
| Механик | контур-кандидат / spec | кладёт spec для Тестера, не live |
| Тестер | replay vs baseline | процесс в том же контейнере, пока LC-15 не доказан |
| Твиттер | X read-only `@acapitalmanager` | без write |

**Пакеты не в слоях.** `razvedka/` `sverki/` `kanon/` `shtab/` — bind-mount (нужен доступ с хоста-архива) или named volume. Образ = Python/runtime/CLI. Пересборка image не уничтожает корпус. Секреты не печь (LC-03).

**MCP-поверхность (опционально, маленький allowlist).** Один процесс в том же контейнере: `tools/list` = чтение пакета / сверка / штамп. Не Typeform. Не Letta ADE. Consent ≠ Owner в петле на каждый call (QE-C-03). Schema новой вертикали → файл в `razvedka/` (HQ-08), не интервью.

**Второй контейнер — только гипотеза LC-15.** Условие: Тестер *должен* изолировать I/O. Контракт: spec (файл Механика) + dataset → метрика. Без живой рыночной трубы. Иначе не открывать Compose-стек.

**Не плодить.** Нет бота «Approver» / «Auditor» / «Интервьюер» / «MCP-Gateway». Нет пустого репо «aicm-lab-image». GitHub из этого чата не писать.

**Масштаб.** Существующие чипы и пропуск пакетов. Не k8s, не SkyPilot-home, не exo, не Mac Studio как заказ этого файла.

---

## 5. Пробелы

Чего спеки и docs 2025–26 **не дают** лабе.

- **Нет официального профиля «research center as one container».** OCI даёт fs+config; агент-доки дают many-agents-one-process. Склейка в «центр = 1 контейнер» — норма *этого* пакета, не стандарт OCI.
- **Нет shipping «replay sidecar».** LC-15 — гипотеза. Нет spec I/O=spec+dataset как типа контейнера.
- **MCP не даёт «Enabler once per packet».** SHOULD HITL на tool invocation конфликтует с автономным контуром (уже пробел QE-файла). Протокол не моделирует External Enabler.
- **Checkpointer не Edition.** Нет моста «thread state → канон AICM», и мост **не нужен** (HOLD).
- **Compose/k8s docs не отвечают на «8 ролей / 1 центр».** Они отвечают на «сколько сервисов у приложения». Приложение лабы = один runtime.
- **Distroless/toolbox** не исследовались; не утверждать пользу.
- **Runtime Spec v1.3.0** на каталоге есть; principles.md этой версии не фетчился — не клясться, что v1.3.0 не менял формулировки.
- **Индекс LangGraph** `https://docs.langchain.com/oss/python/langgraph/` — timeout; выводы по interrupts/persistence/agent-server, которые открылись.
- **Официальный MCP core spec не предписывает Docker как единицу сервера.** Упаковка — практика SDK/хостов (`npx`, иногда image).
- **SkyPilot / exo / llama.cpp `/v1`** в этой сессии заново не снимались — только HOLD.

---

## 6. Provenance: URL fetched vs not-found

Доступ ко всем строкам: **2026-08-31**. «Fetched» = WebFetch или устойчивый сниппет WebSearch по той же URL. «Not-found / blocked / timeout» = нет страницы или не удалось тело.

### Получены

| URL | Статус | Заметка |
|---|---|---|
| https://raw.githubusercontent.com/opencontainers/image-spec/v1.1.1/config.md | fetched | OCI Image = fs changes + execution parameters |
| https://raw.githubusercontent.com/opencontainers/runtime-spec/v1.2.1/spec.md | fetched | runtime config/lifecycle |
| https://raw.githubusercontent.com/opencontainers/runtime-spec/v1.2.1/principles.md | fetched | 5 principles; content-agnostic |
| https://specs.opencontainers.org/ | fetched | Image v1.1.1, Distribution v1.1.1, Runtime v1.3.0 listed |
| https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-an-image/ | fetched | immutable package of files+config |
| https://docs.docker.com/reference/dockerfile/ | fetched | ARG ≠ secrets; `RUN --mount=type=secret` |
| https://docs.docker.com/engine/storage/volumes/ | fetched | volume outside container lifecycle; bind-mount vs volume |
| https://docs.docker.com/compose/intro/compose-application-model/ | fetched | services/networks/volumes/configs/secrets |
| https://docs.docker.com/reference/compose-file/ | fetched | Compose Specification = recommended format |
| https://docs.langchain.com/oss/python/langgraph/interrupts | fetched | interrupt + checkpointer + Command(resume) |
| https://docs.langchain.com/oss/python/langgraph/persistence | fetched | checkpointer vs store; MemorySaver dies with process |
| https://docs.langchain.com/langsmith/agent-server | fetched | many runs per worker; single host default; same image API+queue |
| https://docs.langchain.com/langsmith/deploy-standalone-server | search-snippet | Docker/Compose = local; k8s = production *их* сервера |
| https://docs.crewai.com/ | fetched | agents, crews, flows, enterprise console |
| https://docs.crewai.com/edge/en/concepts/processes | fetched | sequential / hierarchical in-process |
| https://docs.letta.com/ | fetched | SDK vs App Server vs Cloud |
| https://docs.letta.com/platform/app-server/index.md | fetched | many agents in a single process |
| https://docs.letta.com/self-hosting/ | search-snippet + md | one Dockerfile; persist `~/.letta` |
| https://docs.letta.com/v1-sdk/concepts/agent-file/ | fetched | `.af`; secrets null on export |
| https://openai.github.io/openai-agents-python/ | fetched | Agent, Runner, sessions, HITL, MCP |
| https://openai.github.io/openai-agents-python/running_agents/ | fetched | runner loop; sessions; no container-per-agent |
| https://openai.github.io/openai-agents-python/human_in_the_loop/ | fetched | needs_approval; RunState serialize |
| https://modelcontextprotocol.io/specification/2026-07-28/server/tools | fetched | tools/list, elicitation/create, SHOULD HITL |
| https://modelcontextprotocol.io/specification/2026-07-28/basic/transports | fetched | stdio + Streamable HTTP |
| https://modelcontextprotocol.io/specification/2026-07-28/basic/transports/stdio | fetched | client-launched subprocess |
| https://modelcontextprotocol.io/specification/2026-07-28/basic/transports/streamable-http | search-snippet + fetch start | POST one endpoint; replaced HTTP+SSE |
| https://modelcontextprotocol.io/docs/2026-07-28/tools/debugging | fetched | npx stdio example; abs paths |
| https://github.com/microsoft/AutoGen | search-snippet | maintenance mode caution |
| https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ | search-snippet | MAF HITL/checkpoint vs AutoGen Team |
| https://csharp.sdk.modelcontextprotocol.io/v2/concepts/deployment/docker.html | search-snippet | SDK: containerized → Streamable HTTP |
| https://github.com/opencontainers/image-spec | fetched (thin) | repo landing; тело spec.md через GitHub blob пустое |
| https://github.com/opencontainers/runtime-spec | fetched (thin) | repo landing |

### Не найдены / timeout / не принимать как capability

| URL / запрос | Статус | Заметка |
|---|---|---|
| https://github.com/opencontainers/image-spec/blob/v1.1.1/spec.md | blob пустой | использован raw config.md |
| https://raw.githubusercontent.com/opencontainers/image-spec/v1.1.1/spec.md | timeout | обзор образа взят из config.md + search spec.md |
| https://docs.langchain.com/oss/python/langgraph/ | timeout | дочерние interrupts/persistence ок |
| Runtime Spec v1.3.0 principles.md | не фетчился | каталог показывает v1.3.0; текст — v1.2.1 |
| Официальный CrewAI «1 container per agent» | не найдено | Process = in-process |
| Официальный LangGraph «1 container per agent» | не найдено | worker serves many runs |
| Официальный Agents SDK container-per-agent | не найдено | Runner = process loop |
| MCP spec: Docker как MUST упаковки сервера | не найдено | есть stdio/HTTP; Docker — практика SDK |
| Отдельный OCI/MCP профиль «replay sidecar» | не найдено | LC-15 = гипотеза |
| SkyPilot / exo docs (эта сессия) | не снимались | только HOLD |
| llama.cpp official «identity=/v1» (эта сессия) | не снимался | только HOLD |
| Distroless / distrobox / toolbox как единица центра | пропущено как шум | не факт |
| https://mcp-staging.mintlify.app/specification/2026-07-28/basic/transports/stdio | вторичка | канон = modelcontextprotocol.io |

**Пропущено как не-источник:** маркетинговые DEV-посты Compose-vs-k8s; Markaicode/TechJack «CrewAI production multi-container» — не docs вендора, не основание LC-05/LC-09.

Кросс-реф архива (не переписывался): `razvedka/2026-08-31-ai-questionnaire-ecosystems.md` (QE-C-03, QE-C-04, HQ-08 и соседние). Шапка-стиль: `razvedka/2026-08-31-mark-douglas-trading-in-the-zone.md`.
