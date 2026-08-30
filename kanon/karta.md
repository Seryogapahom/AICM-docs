# Единая карта предпочтений AICM (Trading Foundation, sessions vision+s01–s18)

> **BANNER.** Это **не** канон Гермеса. Источник — session cards (`sessions/`), DISCUSSION_DRAFT / session addenda. `canonical: false`. `contract/implementation/runtime_authority: none`. Карта не даёт runtime, торговую, capital или credential authority. Cloud canon v2 / HQ lineage **не** являются источником новых claims: при расхождении действует **карточка**.

## A. Как читать карту

- **Один ID → одна действующая формулировка.** У каждого numbered PREF ровно одно acting-тело. Источник acting-текста указан как `действующая: sXX`.
- **Преемник vs mention.** `TF-PREF-012…016`: s03 v0.2 **заменяет** acting-текст s02 (versioned successor, не mention). Повторы s02 `TF-PREF-002, 006–009, 011` и поздние mention-group (inherited TF/L0/L1/L2/DOC) **не** переписывают тело и **не** дублируются в каталоге.
- **Closures не PREF.** `AICM-L0-B2-CLOSURE-001` и аналоги — в индексе closures (раздел E), не в каталоге PREF.
- **Не изобретать ID.** Нет новых PREF. L3 PREF IDs = 0 (`s18`: `confirmed_l3_preference_ids = 0`). Proposed ≠ confirmed.
- **Система автономна. Человека нет в контуре управления.** Owner/Operator = **External Enabler only**: login, payment, file / объективно внешнее право, ресурс, legal acceptance, identity/KYC, contractual или physical act. После внешнего предиката — **automatic resume, без second approval**. PREF не переписываются так, будто operator-manager подтверждает каждый шаг.
- **L0–L2 не переоткрываются.** Closed IDs остаются closed. Missing implementation, metrics, data или preferred technology **не** contradiction.
- **Слои стратегии не гибридизируются.** wave / setup / knowledge / portfolio / risk / execution остаются раздельными authority contours.
- **Fidelity.** Acting-текст — формулировка карточки, слегка прояснённая. Для длинных L2 (s16–s18) сохраняются Status / Decision / Boundary. Draft architecture theorems, приложенные к первому PREF кластера, не копируются, если уже представлены последующими PREF того же кластера.

## B. Стек закрытий по карточкам (не lineage HQ)

| session | status карточки | что закрыла | next |
|---|---|---|---|
| vision | DISCUSSION_DRAFT | конституция AICM; numbered PREF нет | Trading Foundation sessions |
| s01 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | TF-PREF-001…011 (knowledge/hypothesis) | object model |
| s02 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | TF-PREF-012…016 v0.1; AICM-ARCH-DISC-PREF-001 | object model v0.2 |
| s03 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | TF-PREF-012…016 v0.2 + 017…030 | SituationContextSnapshot |
| s04 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | TF-PREF-031…034; L0-PREF-001…009; Purpose Kernel ещё OPEN | s05 Block 1 |
| s05 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | L0-B1 Purpose Kernel and cold start (L0-PREF-010…019) | L0-B2 |
| s06 | DISCUSSION_CAPTURE_AND_PARTIAL_SEMANTIC_CLOSURE | L0-PREF-020…024; DOC-001…004; ROADMAP-L0-APPROVAL-001. **L0-B2 IN_PROGRESS_PARTIALLY_CLOSED** (не закрыт). L0-025…032 proposed, не confirmed | s07 дозакрытие L0-B2 |
| s07 | L0_B2_SEMANTIC_CLOSURE | L0-025…032 confirmed. **L0-B2 closed.** Closure `AICM-L0-B2-CLOSURE-001` | L0-B3 |
| s08 | L0_B3_SEMANTIC_CLOSURE | L0-033…038. **L0-B3 closed.** `AICM-L0-B3-CLOSURE-001` | L0-B4 |
| s09 | LEVEL_0_CONSTITUTIONAL_ARCHITECTURE_SEMANTIC_CLOSURE | L0-039…043. **L0-B4 closed. Level 0 FORMALLY CLOSED.** `AICM-L0-B4-CLOSURE-001`, `AICM-L0-CLOSURE-001` | L1-B1 NEXT / PARTIALLY CLOSED |
| s10 | L1_B1_RUNTIME_READ_BUNDLE_SEMANTIC_CLOSURE | L1-001…004. **L1-B1 closed.** `AICM-L1-B1-CLOSURE-001` | L1-B2 |
| s11 | L1_B2_HYPOTHESIS_MODEL_AND_DURABLE_WAITING_SEMANTIC_CLOSURE | L1-005…011. **L1-B2 closed** (не L1-B3). `AICM-L1-B2-CLOSURE-001` | L1-B3 |
| s12 | L1_B3_UPTAKE_ACTUAL_USE_DECISION_OUTCOME_LINEAGE_SEMANTIC_CLOSURE | L1-012…019; DOC-005. **L1-B3 closed (NOT L1-B2 — L1-B2 уже closed в s11).** `AICM-L1-B3-CLOSURE-001` | L1-B4 |
| s13 | L1_B4_CONSILIUM_AND_KNOWLEDGE_EVOLUTION_AUTHORITY_SEMANTIC_CLOSURE | L1-020…030. **L1-B4 closed.** `AICM-L1-B4-CLOSURE-001` | L1-B5 |
| s14 | L1_B5_01_BEST_BOUNDED_SLICE_SELECTION_AND_SCOPE_CONTRACT_SEMANTIC_CLOSURE | L1-031…039. **L1-B5-01 closed**; parent L1-B5 ещё IN PROGRESS. `AICM-L1-B5-01-CLOSURE-001` | L1-B5-02 |
| s15 | LEVEL_1_SEMANTIC_CLOSURE | L1-040…055. **L1-B5-02, parent L1-B5, Level 1 FORMALLY CLOSED.** | L2-B1 |
| s16 | L2_B1_SEMANTIC_CLOSURE | L2-001…033. **L2-B1 closed.** Level 2 ещё OPEN. `AICM-L2-B1-CLOSURE-001` | L2-B2 |
| s17 | L2_B2_AND_L2_B3_SEMANTIC_CLOSURE | L2-034…102. **L2-B2 and L2-B3 closed.** Level 2 ещё OPEN | L2-B4 |
| s18 | READY | L2-103…146. **L2-B4 closed. Level 2 FORMALLY_CLOSED.** **L3-B1 ACTIVE_NOT_CLOSED.** confirmed L3 PREF = 0 | Session 19 / L3-B1 |

Карточка побеждает HQ/lineage. Известные расхождения, которым карта следует: **s12 закрыла L1-B3, не L1-B2**; **s06 не закрыла L0-B2** (только partial; закрытие — s07).

## C. Vision / конституция (сжатые различные claims из `vision.md`)

Numbered PREF в vision нет. Ниже — конституционный слой; повторяющиеся формулировки сжаты, **различный claim не отброшен**. Поздние PREF (особенно L0-014 External Enabler) уточняют роль человека; vision-формулировка «Оператор» сохранена как исторический слой и читается через L0-014: не operator-manager.

1. Пакет = `DISCUSSION_DRAFT`; не меняет Foundation v0.1 на месте; не runtime/implementation authority; развитие только как versioned successor.
2. Foundation v0.1 описывался как canonical market-structure knowledge authority, но оставался `COMMITTED_INACTIVE` / `ACCEPTED_NOT_IMPLEMENTED`. E2E-контур (outcomes → Consilium → hypothesis → Knowledge Evolution → versioned update → activation → uptake → measured outcome) не доказан. Организационный дефект: работа заканчивалась на документе/тесте/commit, не на uptake.
3. Целевая контрактная архитектура: один exact contract, один `ACCEPT`, полный lifecycle, automatic continuation после лимитов, завершение только после реального uptake.
4. **AICM Constitution** (миссия, роль человека, автономия, contract authority, способности, доказательства, эволюция, инфраструктура, завершение) **≠ Trading Foundation** (каноническое доменное ядро торговых знаний). Разделение защищает Foundation от смеси архитектуры/памяти/задач/runtime.
5. Миссия: саморазвивающаяся интеллектуальная система, устойчиво создающая экономическую ценность (прежде всего через торговлю), накапливающая знания и способности, строящая путь к целям Owner и со временем финансовую независимость владельца. Система наблюдает, гипотезирует, создаёт способности, оценивает outcomes — не только исполняет заранее написанные инструкции.
6. Человек задаёт вектор (миссия, желаемый результат, стратегические приоритеты, крупные изменения направления, принимаемый contract authority). Система разворачивает путь. Целевая роль — не диспетчер технических шагов. *(Уточнение s05 L0-014: Owner/Beneficiary vs External Enabler vs AICM.)*
7. Главный капитал — **доказанные способности**, не строки кода/агенты/контейнеры. Агент — временный исполнитель; модель/процесс/сервис/контейнер заменяемы; способность и доказательства переживают смену исполнителей.
8. Знание отделено от исполнения: версионированные адресуемые объекты; Foundation ≠ агент; контейнер ≠ истина; runtime-memory ≠ канон; отчёт ≠ фактическое состояние; модель не единственный носитель торговой логики.
9. Развитие накапливает, не стирает: сохранять подтверждённые способности; не оставлять два активных источника истины; «не переписывать работающий механизм» ≠ сохранять ошибочный механизм любой ценой.
10. Архитектура долговечна, реализация временна. Смысл/интерфейсы/инварианты/authority/критерии отделены от языка, модели, агента, контейнера, узла, версии сервиса.
11. Сделано = используется: Correctness, Operationality, Sufficiency, Uptake Verified, Terminal Closed. Код/документ/тест/commit/image — промежуточные продукты.
12. Доказательства служат движению, не остановке: finding → причина → automatic repair → повторная проверка затронутого scope → продолжение. Review не второй authority. Timeout/лимит/потеря сессии ≠ содержательный veto и не требуют ручного `continue`.
13. Один принятый контракт даёт authority на полный принятый lifecycle. После одного `ACCEPT` технические действия, объективно необходимые для Target Capability, входят в program-scoped authority. Нижестоящий prompt/legacy policy/validator не создаёт скрытое второе подтверждение.
14. Session End ≠ Program End. Работа заканчивается только по terminal criteria целевой способности.
15. Эволюция рядом с работающей версией: candidate рядом со stable → измерение → promotion → вывод старого active route. Старая версия не вечный параллельный fallback (второй control plane).
16. Автономия растёт через доказанную компетентность; sandbox не вечное жилище. Replay/shadow/canary — инструменты evidence, не обязательная одинаковая лестница. Оператор не подтверждает каждый внутренний этап.
17. Право на инициативу: система ищет ошибки, неудовлетворительные результаты, неиспользуемые знания, новые методы/данные/модели/экономические возможности. Новая идея не обязана исходить от человека.
18. Нет blanket-запретов, скрывающих отсутствие архитектуры. Authority/капитал/риск выражаются позитивно и точно.
19. Доменные полномочия не смешиваются: кто формирует знание / торговое решение / риск / исполнение / инфраструктуру — раздельно.
20. Инфраструктура служит способностям. **Mac Studio — основной самостоятельный узел** (агентная оркестрация, Foundation/Consilium, торговый runtime, operational state, evidence). Linux — позднее вспомогательный heavy/learning/archive node, не обязательная зависимость ежедневной работы. Физическое размещение — свойство deployment, не способности.
21. Система обязана знать, что умеет и что реально работает: реестры способностей, provider-версий, потребителей, знаний, evidence, контрактов, узлов, release identity, retirement/successor. Dashboard из authoritative sources и runtime read-back; текстовый отчёт не подменяет фактическое состояние.
22. Конституция тоже может развиваться: явная причина, анализ затронутых способностей, successor, provenance, доказательство расширения целевой способности.
23. Foundation — долговечное каноническое ядро торговых знаний (понятия, конкурирующие гипотезы, применимость, доказательства, контрпримеры, неопределённость, provenance, результаты использования). Не: общая оперативная память; Kanban; PID/leases; container registry; универсальный architecture canon; RiskGate; executor; единственный торговый агент; жёсткие детерминированные блокеры.
24. Foundation не выбирает заранее единственный рынок/timeframe/направление/сделку, если нужно контекстное рассуждение. LLM/domain agents собирают сценарии; deterministic components — identity/lineage, расчёты, portfolio exposure, risk policy, idempotency, exchange protocol, reconciliation, accounting, evidence binding.
25. Trading Consilium — доменный механизм коллективного анализа, не универсальный reviewer всей AICM. Не изменяет active Foundation из собственной сессии; после принятого Knowledge Evolution contract путь candidate→update→activation→uptake выполняется автоматически без микроподтверждений.
26. Контейнер не является способностью и не является единицей знания. Центральный объект — Capability Registry. Capability / Provider / Service / Deployment Unit / Container Image / Runtime Instance.
27. Один ACCEPT: после принятия человек не повторно подтверждает старт реализации, work packages, review findings, commit, installation, restart, activation, canary, rollback, использование runtime, завершение. Новый выбор — только при действительно новом направлении вне принятого Target Capability.
28. Вертикальные срезы, не гигантский план. Каждый добавляет одну реально используемую capability slice.
29. Первоначальная отгрузка на Linux-сервер — вручную (например раз в месяц), content-addressed export bundle; автоматическое пробуждение сервера на первом этапе не требуется.
30. Архитектура растёт снежным комом: каждый цикл оставляет работающую capability-опору следующему.

Vision OPEN-блоки A–J и proposed schemas (YAML knowledge record, шесть слоёв Foundation, Capability Registry schema, Node Registry, FND-0…FND-6) — не confirmed PREF; см. раздел F.

## D. Каталог PREF по семействам

Каждый ID ровно один раз. Mentions не дублируют тело. Gist numbered PREF в карточках: **0**.


### D.1 `TF-PREF-001`…`034` — Trading Foundation knowledge / object model / snapshot

### `TF-PREF-001` — Foundation сохраняет торговое знание независимо от LLM
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «Trading Foundation должна быть долговечным, версионированным пространством качественных торговых объяснений, которое позволяет заменяемым reasoning providers: понимать рыночный контекст; строить несколько конкурирующих сценариев; видеть supporting и contradicting evidence; знать границы применимости; определять, какое следующее наблюдение различит сценарии; связывать решение с exact knowledge versions; учиться на outcomes без потери provenance; развивать знания независимо от конкретной LLM, агента или контейнера.» «Foundation не является готовым трейдером, market data warehouse, RiskGate или executor. Она является доменным knowledge core, на основании которого торговые capabilities рассуждают и объясняют свои решения.» Discussion record §2: «сама LLM может иметь обширные общие знания, но они не являются достаточной долговечной памятью AICM. Foundation нужна, чтобы система не зависела от скрытых параметров конкретной модели, случайного prompt context или одной сессии.»

### `TF-PREF-002` — source не принимается как истина без декомпозиции и проверки
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «Каждый источник может содержать: определение; авторскую эвристику; эмпирическое утверждение; пример; непроверяемую интерпретацию; исторически ограниченное правило; противоречие с другим источником; полезную идею, применимую только в узкой области.» «Поэтому ingestion source не должен автоматически становиться active Foundation record.» Pipeline: «Source Artifact → exact provenance and edition identity → extracted propositions → proposition type classification → normalized concepts and claim → scope/applicability draft → known conflicts and alternatives → validation design → evidence and counterevidence → knowledge assessment → candidate release → runtime uptake → outcome-linked reassessment». «Для книги или человеческого описания желательно сохранить исходное человекочитаемое представление и отдельную машиночитаемую декомпозицию. Машиночитаемая версия не должна незаметно подменять смысл источника.» Discussion: «Книга не становится истиной только потому, что она опубликована. Она является provenance-bearing source.»

### `TF-PREF-003` — raw observations/outcomes отделяются от canonical knowledge
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «Observation — Point-in-time факт о рынке или работе системы. Observation является evidence input, но не обязательно knowledge.» Knowledge Record — «Immutable смысловая единица: concept, observation semantics, hypothesis template, semantic constraint, reasoning pattern, applicability statement, counterexample class или evaluation definition.» Discussion §3.1: «raw market facts, time series, telemetry, fills, positions и terminal outcomes живут в Evidence/Data Plane; Foundation хранит определения, интерпретационные модели, проверяемые claims, applicability, counterexamples, lessons и immutable references на evidence; Foundation не должна дублировать весь market dataset.» «Зафиксированный смысл: отделение raw data от knowledge принято как правильное направление. Точная физическая граница Source Library, Evidence Store и Foundation остаётся предметом следующего обсуждения.»

### `TF-PREF-004` — setup сохраняет исходное человекочитаемое представление и имеет машиночитаемую композицию
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «Setup следует моделировать как first-class reasoning pattern, составленный из ссылок на более атомарные знания.» Пример: Wave-1 / Wave-2 Reversal Pattern включает decline completion hypothesis, reversal confirmation semantics, wave-2 retracement model, Fib anchoring, POI interaction, liquidity/volume evidence, extension counter-hypothesis, invalidation semantics, outcome evaluation definition. Setup должен включать: «intended opportunity; preconditions; expected sequence; supporting observations; contradicting observations; alternative explanations; what-to-wait-for; invalidation of the interpretation; entry/exit guidance как advisory knowledge; risk assumptions; expected path; evaluation horizon; known failure modes.» «Portfolio authority, exposure limits, order protocol и execution reconciliation остаются в других слоях.» Discussion: Оператор согласился хранить setup в двух связанных представлениях: «1. неизменяемое или точно атрибутированное человекочитаемое исходное описание; 2. машиночитаемая декомпозиция на понятия, условия, supporting/contradicting observations, альтернативы, invalidation, targets и outcome criteria.» «Setup не должен быть непрозрачным монолитным правилом.»

### `TF-PREF-005` — semantic invalidation гипотезы не равна global trading veto
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: Следует различать три категории. **Semantic constraints** могут отвергнуть конкретную интерпретацию: «this wave labeling violates the selected wave model → reject this labeling → generate alternatives». **Epistemic guidance** может: «поддерживать; ослаблять; противоречить; требовать consideration; предлагать альтернативу; указывать недостаток evidence.» **Operational authority:** «Только соответствующие deterministic/control components могут blocking action из-за: отсутствия authority; portfolio risk violation; invalid order protocol; idempotency conflict; unreconciled exchange state; невозможности доказать required market facts.» «Foundation не должна незаметно присваивать себе authority RiskGate или executor.» Discussion: «Wave Canon и другие структурные инварианты могут отвергать конкретную wave interpretation; это не должно автоматически означать запрет торговли; система должна строить альтернативную разметку, другой сценарий или другой тип market explanation.» «Ключевая граница: semantic invalidation конкретной гипотезы не равна execution veto всего lifecycle.»

### `TF-PREF-006` — runtime ведёт несколько competing scenarios
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «Для каждого значимого market issue Foundation/runtime должны позволять существование нескольких explanations» (пример: H1 завершение пятой волны / H2 продолжение растянутой третьей / H3 коррекция более высокого degree / H4 liquidity-driven range expansion). Каждая гипотеза содержит: «exact claim; scope; supporting arguments; attacking arguments; known counterexamples; predictions; expected market path; invalidating observations; distinguishing observations; relation to alternatives; uncertainty and missing data.» Предлагаемые context-local statuses: `LEADING`, `VIABLE_ALTERNATIVE`, `WEAK_BUT_UNRESOLVED`, `REJECTED_IN_THIS_CONTEXT`, `INSUFFICIENT_DATA`, `RESOLVED_BY_OUTCOME`. «Они не должны становиться глобальным permanent status knowledge record.» Discussion: «на конкретный момент может существовать leading hypothesis; viable alternatives не удаляются; … Foundation не уничтожает альтернативу только потому, что другая гипотеза временно лидирует.»

### `TF-PREF-007` — unresolved scenarios содержат differentiating observations
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: Когда scenario set не разрешён, система должна сформировать активный observation plan: `unresolved_issue`, `leading_hypothesis`, `alternatives`, `next_discriminating_observations`, `expected_time_or_market_conditions`, `what_supports_each`, `what_rejects_each`, `action_while_waiting`, `recheck_trigger`. Discussion: если конкурирующие гипотезы пока не разрешены, AICM должна «определить differentiating observation; сформулировать expected trigger или invalidation; продолжать наблюдение без обращения к Оператору; обновить сценарии при появлении новых данных; не путать отсутствие сделки с остановкой программы.»

### `TF-PREF-008` — ожидание выполняется автономно как active decision state
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «`WAITING_FOR_EVIDENCE` не является program failure или session end. Это durable decision state, который должен автоматически возобновиться по trigger.» Discussion: «ожидание становится активным состоянием decision process, а не неопределённой паузой.»

### `TF-PREF-009` — knowledge evolution проходит candidate → validation → release → use → feedback
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: Lifecycle: «source / observation / outcome → candidate → normalization and deduplication → competing alternatives → validation design → evidence acquisition → critique → assessment → candidate release → activation under accepted authority → read-back → consumer uptake → decision/outcome binding → reassessment → keep / revise / restrict / retire». Discussion: «Новая идея не входит напрямую в active Foundation. Она сначала становится кандидатом с provenance и проходит достаточную для своего класса проверку.»

### `TF-PREF-010` — feedback автоматическая и не создаёт микроподтверждения
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: «После принятия bounded lifecycle система должна автоматически: фиксировать usage; ждать предписанные observations; связывать outcome; выполнять предусмотренный repair/retry; обновлять assessments; формировать следующий candidate; продолжать до terminal criteria.» «Новый операторский выбор требуется только при действительно новом материальном направлении вне принятой authority.» Discussion: «feedback не означает новые ручные команды Оператора на каждом шаге.» Система «не требует от Оператора отдельных подтверждений на activation, observation waiting, result capture или repair внутри уже принятого lifecycle.» «Это совместимо с принципом `one ACCEPT → full accepted lifecycle → Terminal Closed`.»

### `TF-PREF-011` — Foundation представляет пространство объяснений, а не готовый ответ
- действующая: s01 (первое появление s01; s02 mentions 002/006–009/011 не заменяют тело)
- текст: Центральная формулировка сессии (discussion): «Foundation должна хранить не готовые ответы, а пространство качественных объяснений рынка.» «Эта формулировка становится центральной для дальнейшей модели. Foundation должна помогать системе обоснованно выбирать между объяснениями, а не подменять мышление готовой командой.» Draft §10: LLM получает structured context bundle (exact Foundation release, relevant concepts, applicable claims, competing hypotheses, supporting/attacking arguments, semantic constraints, counterexamples, missing knowledge, discriminating observations, provenance). Decision trace указывает `CONSIDERED` / `USED_AS_SUPPORT` / `USED_AS_CHALLENGE` / `REJECTED_WITH_REASON` / `NOT_APPLICABLE` / `OVERRIDDEN_WITH_REASON`. «LLM сохраняет свободу рассуждения, но не имеет права молча игнорировать обязательный контекст.» Дополнительно discussion §3.5 подтверждает направление machine-driven regimes без отдельного PREF ID: система «должна распознавать наблюдаемые режимы и поведенческие паттерны»; «не должна без evidence утверждать, что восстановила точный чужой код»; вывод — «вероятная market-behavior hypothesis». Это зафиксировано в draft §6 как архитектурная осторожность, не как отдельный numbered PREF.

### `TF-PREF-012` — semantic content и assessment independently versioned
- действующая: s03 (преемник v0.2 vs s02; действующий текст = s03)
- текст: «Confirmed separation semantic content и assessment сохраняется.» Assessment связывается с «exact record/composite version + exact evidence manifest + method/version + target scope + as-of boundary + evaluator capability/provider + challenges/counterexamples + maturity/disposition». «Параллельные assessments допустимы: replay, shadow, venue-specific, regime-specific, independent provider, Consilium challenge. Disagreement является research signal, а не data corruption.» «assessment/evidence никогда не должны переписывать claim content» (§9.2).

### `TF-PREF-013` — Foundation вырабатывает knowledge, source authority не наследуется
- действующая: s03 (преемник v0.2 vs s02; действующий текст = s03)
- текст: Assessment SourceAssertion оценивает «semantic fidelity; qualifier preservation; translation/transcription quality; ambiguity; whether source is quoted, paraphrased or interpreted.» «Он не оценивает, истинно ли source assertion. Truth/applicability assessment появляется только после formation knowledge candidate и relation to evidence.» Source-derived candidate обязан иметь mechanically resolvable path до exact SourceAssertion / SourceSegment / ArtifactEnvelope / ContentObject digest. «Candidate без такого path не может маркироваться source-derived.»

### `TF-PREF-014` — knowledge не имеет action/risk/execution authority
- действующая: s03 (преемник v0.2 vs s02; действующий текст = s03)
- текст: «Никакого direct `VALIDATED_FOR_SCOPE → order` path нет.» Path: «Knowledge maturity → permitted release role → consumer capability evaluation → operational exposure promotion policy → decision contour → RiskGate → execution authority.» «Evidence relation не даёт action/risk/execution authority» (`02` §7).

### `TF-PREF-015` — provisional bootstrap knowledge допустимо при explicit maturity и bounded use
- действующая: s03 (преемник v0.2 vs s02; действующий текст = s03)
- текст: Подтверждены semantic states `SOURCE_ONLY`, `CANDIDATE`, `PROVISIONAL`, `VALIDATED_FOR_SCOPE`, `CONTESTED`, `RESTRICTED`, `RETIRED` (определения в §5). «Vocabulary подтверждён, но exact transition topology остаётся open. `CONTESTED` и `RESTRICTED` — не просто более низкие ступени maturity.» `PROVISIONAL`: «Semantic clarity, initial support и explicit scope достаточны для bounded research/replay/shadow или маркированного advisory use. Unknowns и challenge plan остаются видимыми.»

### `TF-PREF-016` — actions/inactions создают evidence; P&L не является direct knowledge verdict
- действующая: s03 (преемник v0.2 vs s02; действующий текст = s03)
- текст: «Trade, no-trade и waiting создают evidence. Profit/loss не являются прямым verdict knowledge. Scenario, trade construction и execution outcomes оцениваются отдельно. Feedback может быть automatic, но attribution и promotion следуют accepted evidence policy.» «Эта сессия не закрывает exact outcome schemas.»

### `TF-PREF-017` — logical separation Source Plane, Evidence Plane, Foundation Knowledge Store
- действующая: s03 (первое появление s03)
- текст: «Source Plane, Evidence Plane и Foundation Knowledge Store являются разными logical authority domains независимо от initial physical storage. Общий content-addressed vault допустим как substrate, но не отменяет различия content identity, provenance identity, role identity и semantic knowledge identity.» Source Plane отвечает: «Что именно было сказано, написано, показано или declared конкретным source в exact version?» Evidence Plane: «Что наблюдалось, измерялось, исполнялось или получилось при exact procedure и point-in-time boundary?» Foundation Knowledge Store хранит structured understanding AICM (candidates, lineages, versions, assessments, composites, relations, releases) и «не должен становиться хранилищем всего raw market data, agent memory, task cursor, runtime position state, secrets или model weights.» Artifact substrate «не является canonical truth store.»

### `TF-PREF-018` — first-class SourceAssertion с fidelity assessment без truth status
- действующая: s03 (первое появление s03)
- текст: «`SourceAssertion` — first-class immutable semantic extraction: Какое утверждение содержится в exact source segment, с сохранением source modality, qualifiers, scope и ambiguity.» Content: exact source reference; extracted proposition; source-declared conditions/modality/scope/horizon; quote/paraphrase/translation classification; extraction method/provider/version; unresolved ambiguity и alternative readings; human-readable explanation. Fidelity assessment отдельно от truth (см. TF-PREF-013 v0.2).

### `TF-PREF-019` — exact source lineage обязательна для source-derived candidate
- действующая: s03 (первое появление s03)
- текст: Path: «KnowledgeCandidate → SourceAssertion exact version → SourceSegment exact locator → ArtifactEnvelope exact version → ContentObject digest / immutable locator». «System synthesis, operator idea или abductive proposal допускаются, но должны иметь явный origin/derivation record и не получать ложную citation authority.» «Ссылка на книгу или dataset целиком недостаточна, если claim извлечён из конкретного segment» (§5.2).

### `TF-PREF-020` — multiple independent typed roles одного immutable artifact
- действующая: s03 (первое появление s03)
- текст: «Immutable Artifact Identity ├── SourceRoleBinding A/B ├── EvidenceRoleBinding C/D». Каждый binding имеет independent target, scope, method, point-in-time boundary, quality/fidelity assessment, access policy, producer/evaluator lineage. «source role не делает artifact evidence; evidence для claim A не становится evidence для claim B; evidence relation не даёт action/risk/execution authority; format или publisher authority не создают canonical truth.» «Role не выводится автоматически из MIME type.»

### `TF-PREF-021` — lineage identity = proposition + material scope + modality + horizon
- действующая: s03 (первое появление s03)
- текст: «stable claim lineage ≈ normalized proposition + material scope + modality + evaluation horizon». Exact KnowledgeRecordVersion имеет deterministic digest. «Digest отвечает „какая exact version“. Lineage отвечает „какой устойчивый semantic claim развивается во времени“.» Changes в той же lineage (если truth conditions не меняются): wording, equivalent terminology, formatting, deterministic normalization, non-material clarification, provenance metadata repair, attachment новых sources/evidence, новая assessment, relation update без изменения proposition. Новый related identity: polarity change; material modality/scope/horizon/target change; material condition add/remove; causal vs correlational shift; split/merge independently assessable propositions; изменение, делающее прежний evidence verdict неприменимым.

### `TF-PREF-022` — material scope restriction создаёт related claim
- действующая: s03 (первое появление s03)
- текст: «Material restriction создаёт новый claim: KR-NARROW --RESTRICTS--> KR-BROAD». «Broad claim сохраняется для historical assessment. Narrow claim не наследует validation автоматически; он получает собственные evidence bindings и assessment. Это предотвращает rewriting failed generalization в будто бы всегда узкий успешный claim.» Lineage relations (`REFINES`, `RESTRICTS`, `GENERALIZES`, `CHALLENGES`, `CONTRADICTS`, `SUPERSEDES`, `DERIVED_FROM`, `SUPPORTED_BY`, `COUNTEREXAMPLE_TO`) остаются `PROPOSED` по exact semantics.

### `TF-PREF-023` — atomicity = independently assessable semantic unit
- действующая: s03 (первое появление s03)
- текст: «Atomic claim — minimal independently assessable semantic unit, а не minimal text fragment.» Проверка: единый evidence verdict; applicability для всего claim; material counterexample атакует claim целиком; использование без переноса unrelated recommendation; изменение одного condition меняет identity целиком. Полезный envelope: «в scope/context C при conditions P observation X поддерживает / предсказывает / противоречит Y на horizon H с modality M». «Context-free triple может быть storage representation, но не гарантирует semantic atomicity.»

### `TF-PREF-024` — composite setup/reasoning pattern first-class и separately assessed
- действующая: s03 (первое появление s03)
- текст: Setup, reasoning pattern и market model — first-class composite objects с exact component versions, composition/ordering semantics, applicability, conflict-resolution, strongest challenges, counterexample classes, invalidation, execution assumptions, evaluation specification. Composite получает собственные stable identity, digest, assessment, evidence bundle, applicability, challenge relations, release role. Почему отдельная assessment обязательна: independently valid components могут конфликтовать; sequence/order может создавать leakage; interaction меняет base rate; composite может быть operationally infeasible; invalidation one component не всегда invalidates whole setup.

### `TF-PREF-025` — maturity vocabulary и operational exposure vocabulary separate; maturity не создаёт authority
- действующая: s03 (первое появление s03)
- текст: Maturity states confirmed (см. 015). Operational exposure vocabulary confirmed: `OFFLINE`, `REPLAY`, `SHADOW`, `ADVISORY`, `CANARY`, `GOVERNED_LIVE` (v0.1 имена `OFFLINE_RESEARCH` / `PARALLEL_ADVISORY` — non-material wording variants). Operational promotion требует consumer capability evidence, exact release compatibility, uptake observability, monitoring, failure containment/rollback, data freshness, accepted capital/risk policy, decision and RiskGate boundaries, execution capability authority. «Даже `VALIDATED_FOR_SCOPE` knowledge не открывает position и не создаёт permission на `GOVERNED_LIVE`» (README §4.7).

### `TF-PREF-026` — evidence sufficiency зависит от knowledge family
- действующая: s03 (первое появление s03)
- текст: «Один universal threshold отвергнут. Ниже подтверждённые semantic requirements; exact numerical thresholds остаются open.» Definitions/ontology: exact normative source, semantic coherence, unit conventions, compatibility tests; failure: circularity, overlapping terms, unmeasurable definition. Empirical market claims: point-in-time data, out-of-sample, regime/venue coverage, counterexamples, leakage checks. Composite setups: component evidence plus joint replay/shadow, ordering/interaction tests, execution feasibility. Execution knowledge: venue/order-type/provider-specific tests, telemetry, rejects, latency/slippage, reconciliation. «Definitions могут не требовать statistical sample, но market-operational definitions должны быть measurable.»

### `TF-PREF-027` — contested knowledge release-eligible как explicit challenge/alternative
- действующая: s03 (первое появление s03)
- текст: Contested knowledge может быть release-eligible в роли: strongest challenge; viable alternative; counterexample class; uncertainty boundary; unresolved provider disagreement; condition requiring differentiating observation. Manifest различает supportive/advisory, challenge, restriction, retired-history-only. «Consumer не должен collapse contested object в positive recommendation. Но исключать credible challenge из runtime read bundle также опасно: система станет self-confirming.»

### `TF-PREF-028` — assessment/maturity transitions autonomous внутри standing mandate
- действующая: s03 (первое появление s03)
- текст: Внутри standing mandate AICM автономно: ingest evidence; create/revise assessment proposals; add challenges/counterexamples; change maturity/disposition когда exact accepted criteria выполнены; restrict applicability; create semantic successor candidates; retire из future releases по accepted policy; schedule replay/shadow; publish routine release updates если authority покрывает; continue durable program. «Operator microconfirmations для этих внутренних transitions не требуются.» Operational exposure promotions autonomous только если заранее приняты eligible transition, evidence criteria, capability requirements, impact boundary, monitoring/rollback, capital/risk envelope, terminal outcome, fail-closed behavior. Fail-closed: запрещённый action не выполняется; current safe capability продолжает; program сохраняет cursor; система исследует remediation; operator dependency request только при действительно внешнем blocker; после resolution continuation автоматическая.

### `TF-PREF-029` — training datasets и model artifacts являются exact derived outputs, не canonical knowledge
- действующая: s03 (первое появление s03)
- текст: «Foundation knowledge ≠ training dataset ≠ trained model weights.» Derived dataset classes: Retrieval corpus; Supervised fine-tuning; Preference/critic; Tool/capability trace; Evaluation/holdout; Replay/simulation. «Один dataset не должен автоматически использоваться для всех целей.» Dataset release предпочтительно содержит exact lineage, purpose, inclusion/exclusion, licensing/privacy, label origin, positive/negative/null/wait/no-trade examples, temporal boundaries, leakage checks, train/validation/holdout manifests, known gaps, digest, evaluation protocol, successor lineage. Fine-tuning оправдан при stable target capability, systematic baseline failure, enough high-quality examples, separated evaluation set, expected value > cost, observable/rollback, provider lifecycle. «Fine-tuning не должен использоваться как способ скрыть плохую object model.» «Model weights остаются replaceable provider artifact.» Training completion ≠ capability completion.

### `TF-PREF-030` — system сама выявляет external dependency, создаёт bounded operator request и автоматически продолжает после provision
- действующая: s03 (первое появление s03)
- текст: Целевая роль Оператора: «задавать mission, desired outcomes, strategic boundary и authority; предоставлять действительно внешние ресурсы или legal/account approvals; изменять крупный strategic vector; получать economic outcome.» AICM сама обнаруживает потребность в новом data source/provider, account, credential/API, compute/storage, budget/capital, payment method, legal acceptance, physical action. Request содержит: что требуется; зачем и для какого target outcome; почему нельзя продолжить без этого; минимальная authority/access; стоимость и recurring commitments; risks and data exposure; alternatives; verification после provision; automatic continuation point. «Это preference boundary, а не permission на создание accounts, управление cards, capital или credentials.» *(В s05 Owner/Beneficiary = External Enabler для login/payment/file; здесь термин «Оператор» сохранён как в источнике s03.)*

### `TF-PREF-031` — exact immutable SituationContextSnapshot обязателен для material hypothesis/decision attempt
- действующая: s04 (первое появление s04)
- текст: «Для каждого material hypothesis attempt и material decision attempt AICM формирует immutable `SituationContextSnapshot`.» Определение: «purpose-bounded immutable semantic projection того, что система имела право считать известным при exact information boundary конкретной попытки рассуждения.» «Он не является полной копией Data Plane и не утверждает, что рынок остановлен.» Поток: «live observations keep changing → material reasoning attempt begins → exact context projection is resolved → snapshot identity is fixed → all participants reason against that boundary → later observations create a new attempt / successor snapshot». Material use — reasoning, которое может повлиять на hypothesis lifecycle, trade/no-trade/wait, risk, capital, execution, capability promotion, learning attribution, constraint/policy change. Non-material (monitoring/UI/preliminary research) могут использовать mutable views, но outputs non-authoritative до material re-resolution. Один `as_of` timestamp недостаточен: различать `event_time`, `availability_time`, ingestion/resolution time, overall `information_cutoff`, allowed temporal skew, freshness. Snapshot — bounded semantic projection, не весь raw stream; raw candles/order-book/sources остаются доступны по lineage. «Exact materiality policy остаётся `OPEN`.»

### `TF-PREF-032` — first-class MISSING / STALE / CONFLICTING / UNKNOWN / NOT_APPLICABLE / RESOLUTION_FAILED
- действующая: s04 (первое появление s04)
- текст: «Absence, uncertainty и conflict являются частью context.» Минимальная confirmed vocabulary: `MISSING` — ожидаемый input не получен; `STALE` — input существует, но нарушает applicable freshness boundary; `CONFLICTING` — available inputs несовместимы; `UNKNOWN` — значение невозможно установить из доступного evidence; `NOT_APPLICABLE` — field не относится к текущей purpose/scope; `RESOLUTION_FAILED` — resolver не смог создать допустимую semantic projection. «Нельзя молча сводить эти состояния к `null`, default value или единственному „победившему“ input.» Для conflict сохраняются competing values, provenance каждого, применённая resolution policy, resolved value если существует, residual uncertainty, consequence для downstream.

### `TF-PREF-033` — material correction создаёт successor snapshot, original use lineage не переписывается
- действующая: s04 (первое появление s04)
- текст: «Сформированный snapshot immutable.» «Material correction создаёт successor: SituationContextSnapshot S1 → decision/hypothesis reasoning used S1 → correction discovered → SituationContextSnapshot S2 created → S2 corrects/supersedes S1 for future attempts → historical reasoning remains bound to S1». Это позволяет различать ошибку исходных данных, ошибку resolver, ошибку reasoning, изменение market information после decision, retrospective correction provider history. «Cosmetic metadata repair не должен незаметно менять semantic content.»

### `TF-PREF-034` — Context Resolver не имеет decision / RiskGate / execution authority
- действующая: s04 (первое появление s04)
- текст: Resolver может: discover relevant inputs; evaluate freshness/data quality; resolve units/time alignment; preserve conflicts and unknowns; create bounded projection; expose caveats; issue successor snapshots. Resolver не может сам по себе: выбирать leading hypothesis; объявлять interpretation invalid для всей системы; принимать trade/no-trade/wait decision; назначать size; выдавать RiskGate verdict; authorise execution; promote knowledge/capability/constraint. Может выпускать context state `RESOLVED` / `RESOLVED_WITH_CAVEATS` / `MATERIALLY_INCOMPLETE` / `CONFLICTING` / `UNRESOLVED`; последствия определяют отдельные policies. «Snapshot generation является automatic infrastructure/capability behavior. Оператор не выдаёт отдельную команду для каждого snapshot.» Automatic ≠ uncontrolled: version, inputs, conditions, successor lineage observable/auditable. Runtime Read Bundle (ещё OPEN) отвечает «какой exact knowledge/evidence/assessment set был предоставлен consumer», не подменяет snapshot.


### D.2 `AICM-ARCH-DISC-PREF-001` — режим архитектора

### `AICM-ARCH-DISC-PREF-001` — режим работы архитектора
- действующая: s02 (первое появление s02)
- текст: «архитектор обязан сначала предлагать и обосновывать лучший вариант, не переоткрывать подтверждённые решения без новой причины и задавать Оператору только bounded preference/authority questions.» OPEN roadmap: «Архитектор сначала предлагает лучший вариант и не превращает сессию в повторную проверку ранее подтверждённых решений.» Handoff: отмечать `CONFIRMED`, `PROPOSED`, `OPEN`; не задавать Оператору повторно уже подтверждённые вопросы как memory test.


### D.3 `AICM-L0-PREF-001`…`043` — Layer Zero (purpose, portfolio, constraints, engine)

### `AICM-L0-PREF-001` — enduring economic purpose; goals/plans/tasks — временные self-generated constructs
- действующая: s04 (первое появление s04)
- текст: «AICM проектируется не как исполнитель очереди задач, а как enduring self-directed economic intelligence system.» Confirmed direction: «устойчиво приумножать капитал и повышать собственную способность делать это через непрерывное накопление знаний, capabilities, evidence и operational competence.» «Goals, plans, tasks, experiments и improvement programs являются временными constructs, которые система должна формировать и обновлять сама.» Цикл: «enduring purpose → continuous perception of environment and self → temporary goals and programs → verified outcomes → updated knowledge/capabilities/policies → renewed goal formation». «Enduring purpose задаёт direction of optimization, но не fixed roadmap.» «Exact question, может ли AICM изменять сам enduring purpose, остаётся `OPEN`. Сессия подтвердила self-generation целей, но не silent self-rewrite ownership/economic purpose.»

### `AICM-L0-PREF-002` — autonomous goal discovery без operator microdispatch
- действующая: s04 (первое появление s04)
- текст: «система автономно выявляет, формирует, уточняет, декомпозирует, приоритизирует и закрывает цели без operator microinstructions как default operating mode» (discussion). Goal formation — explicit capability, не скрытый prompt: преобразовать observation/gap/opportunity в candidate objective; сформулировать expected outcome и reason; указать affected capabilities/constraints; определить evidence path; предложить alternatives; оценить dependency и resource demand; задать exit/repair/retirement; сохранить origin и successor lineage. «Goal не становится автоматически authoritative только потому, что его сгенерировал сильный model/provider.»

### `AICM-L0-PREF-003` — continuous evolution cycle — постоянная system function
- действующая: s04 (первое появление s04)
- текст: «1. Observe environment 2. Observe internal state and actual capabilities 3. Detect failures, gaps, contradictions and opportunities 4. Generate competing explanations and development hypotheses 5. Convert valuable hypotheses into candidate goals/programs 6. Prioritize by expected economic value, evidence, cost and consequence 7. Execute, experiment or gather missing evidence 8. Measure direct and indirect outcomes 9. Update knowledge, capability assessments, constraints and architecture 10. Continue from durable successor state». «Система как whole не имеет state `DONE`. `Done / Terminal Closed` относится к bounded program/capability outcome. После closure cycle ищет следующий valuable gap/opportunity.»

### `AICM-L0-PREF-004` — architectural curiosity обязательна
- действующая: s04 (первое появление s04)
- текст: «Curiosity означает систематический поиск возможностей, которых не было в исходном task list.» Источники: unexplained outcome variance; repeated manual/external dependency; unused knowledge/capability; new data/model/provider; cost/latency/reliability gap; market regime change; capability combinations; counterfactual analysis; challenge to current assumptions and constraints. «Curiosity должна быть bounded resource economics, а не бесконечным research. Возможность становится program только после comparative value reasoning.»

### `AICM-L0-PREF-005` — self-criticism и separation proposal / challenge / evaluation / promotion
- действующая: s04 (первое появление s04)
- текст: «Autonomy без self-criticism создаёт уверенную самоподдерживающуюся ошибку.» «proposal generation ≠ strongest challenge ≠ evidence evaluation ≠ promotion/authority decision ≠ execution». «Это logical separation, а не требование пяти постоянных agents. Один provider может временно исполнять разные roles, но role identity, inputs, outputs и authority должны оставаться различимыми.» Self-criticism включает strongest challenge, counterexamples, regression impact, alternative explanations, opportunity cost, falsification conditions, post-outcome attribution.

### `AICM-L0-PREF-006` — architecture эволюционирует через versioned successors
- действующая: s04 (первое появление s04)
- текст: Каждый architectural component должен иметь: stable responsibility identity; versioned provider implementations; explicit consumers/dependencies; evidence of value; candidate/stable evolution path; failure/degradation semantics; successor/retirement lineage; contribution to autonomous purpose. «Architectural principle меняется через explicit reason и successor, а не через prompt drift.» Сохраняются reproducibility, history и proven capability lineage (discussion).

### `AICM-L0-PREF-007` — component legitimacy filter
- действующая: s04 (первое появление s04)
- текст: Перед добавлением component: «1. Какую уникальную responsibility он несёт? 2. Почему её нельзя безопасно отдать existing component? 3. Какие authorities он имеет и не имеет? 4. Кто его consumers и dependencies? 5. Как система обнаруживает его failure/degradation? 6. Как он эволюционирует рядом со stable? 7. Что теряет autonomous cycle, если component исчезнет?» «Этот filter защищает от module proliferation и от giant universal agent.»

### `AICM-L0-PREF-008` — constraints explicit, scoped, reasoned, evidence-linked и reviewable
- действующая: s04 (первое появление s04)
- текст: Legacy constraints часто выглядят как «never do X / agent Y cannot do Z / manual approval required» без reason, scope, origin, evidence, expiry или review path. «Такая форма превращает временную caution в permanent architecture wall.» Internal constraint/policy должно сохранять семантически как минимум: stable identity and version; protected outcome; reason and originating evidence; scope and affected capabilities/authorities; activation conditions; assumptions; cost/opportunity impact; challenge/counterevidence; review trigger/next wake; successor/restriction/retirement lineage. Exact schema не подтверждена. Constraint classes taxonomy — `PROPOSED`, не confirmed final model.

### `AICM-L0-PREF-009` — system инициирует review; material change через evidence-bearing successor, не silent mutation
- действующая: s04 (первое появление s04)
- текст: Lifecycle: «observed risk/need → candidate constraint hypothesis → challenge and alternatives → scoped activation/promotion → outcome monitoring → confirmation / restriction / replacement / retirement → successor lineage». Система сама инициирует review. Triggers: expired assumptions; environment change; repeated blocked high-value programs; evidence that constraint does not protect intended outcome; less costly safeguard; authority/provider/capability replacement; scheduled review. «Constraint не отменяется silent in-place mutation. Material amendment получает explicit successor.» «Оператор подтвердил, что internal rules между agents/capabilities должна формировать сама система, а не человек вручную.» Permission: actor identity + verified competence + purpose/context + resource/capital scope + reversibility + current constraint versions + required evidence → bounded authority grant or denial. Exact authority grammar OPEN.

### `AICM-L0-PREF-010` — Minimal Purpose Kernel
- действующая: s05 (первое появление s05)
- текст: **Decision:** Purpose Kernel включает beneficiary/ownership anchor, durable owner-controlled economic outcome, instrumental recursive competence и constitutional continuity. **Consequence:** capabilities, providers, strategies и domains не являются purpose. - **Beneficiary / ownership anchor:** «AICM существует для enduring economic interest законного Owner/Beneficiary или явно определённого ownership contour. Models, agents, providers, infrastructure и сама AICM не становятся новым beneficiary из-за собственного роста, сложности или resource needs.» - **Enduring economic outcome:** «AICM должна законно и устойчиво увеличивать реальную экономическую ценность, контролируемую Owner/Beneficiary, сохраняя способность продолжать её создание на длительном горизонте.» «`Устойчиво` не означает запрет риска. … Термин исключает narrow optimization, при которой краткосрочная прибыль достигается ценой terminal impairment, hidden liability, loss of control или разрушения future earning capability.» - **Recursive competence mandate:** AICM обязана повышать способность достигать enduring economic outcome (knowledge, capabilities, evidence quality, operational weaknesses, providers, cost/latency, новые lawful opportunities, architecture). «Recursive competence является `mandatory instrumental direction`, а не самостоятельным terminal purpose.» «self-development is valuable only where a plausible causal path exists from improved capability → improved…

### `AICM-L0-PREF-011` — Purpose interpretation and amendment boundary
- действующая: s05 (первое появление s05)
- текст: **Decision:** AICM автономно развивает interpretation/goals/programs; identity-level Purpose successor требует explicit lineage и separate constitutional authority contour. **Consequence:** no routine operator approvals; no unilateral beneficiary/terminal-purpose rewrite. Таблица: Purpose Kernel — очень высокая lifetime, material successor через separate constitutional contour; Purpose Interpretation — эволюционирующая, AICM autonomously; Goal/Program — временные, AICM autonomously. Kernel не содержит fixed domain roadmap, списка providers, обязательного trading method. В пределах active Kernel AICM автономно может уточнять Interpretation, создавать/закрывать goals/programs, выбирать markets и lawful domains, менять strategies/providers, инициировать research/repair, пересматривать internal constraints, предлагать Purpose successor. Не получает автоматически право менять beneficiary, присваивать себе capital ownership, объявлять self-preservation terminal purpose, считать capability growth самостоятельным успехом, отменять law/contractual rules внутренней записью, активировать identity-level Purpose successor, который она сама предложила.

### `AICM-L0-PREF-012` — Cold-start inventory boundary
- действующая: s05 (первое появление s05)
- текст: **Decision:** cold start uses active Purpose Kernel, evidence-linked Self-State/World-State, uncertainty, resources, authority and inherited constraints. **Consequence:** narrative memory or claimed capability is insufficient. «Cold start не должен зависеть от operator-authored first task.» Вопрос Kernel: «Каково доказанное текущее расстояние между enduring purpose и тем, что AICM реально способна делать сейчас?» Sequence: active Purpose Kernel → establish exact information boundary → evidence-linked Self-State → evidence-linked World-State → expose uncertainty and inherited constraints → Purpose-Realization Gaps and Opportunities → compare candidates → open first autonomous program. Self-State: Capabilities, Resources and access, Knowledge and uncertainty (включая MISSING/STALE/…), Programs and outcomes, Constraints and authority, Accountability readiness. World-State: только material external conditions; «не является полной энциклопедией мира и не может быть одной mutable narrative memory LLM».

### `AICM-L0-PREF-013` — First autonomous program emergence
- действующая: s05 (первое появление s05)
- текст: **Decision:** first program arises from highest-value Purpose-Realization Gap/Opportunity, not a hard-coded task. **Consequence:** first program may be economic, research, repair, dependency or observability work. Candidate становится first program при: verified gap/opportunity origin; explicit Purpose linkage; plausible causal path; strongest challenge and alternatives; dependency/resource visibility; current authority feasibility; observable result/learning boundary. Может быть: direct economic program; knowledge acquisition/validation; capability repair/build; external dependency resolution; provider replacement; observability/accountability repair; constraint reconciliation. «It is not predetermined as trading or infrastructure.» «Exact portfolio comparison is deferred to Block 2. No single scalar score may silently become a replacement Purpose Kernel.»

### `AICM-L0-PREF-014` — Operator non-management target model
- действующая: s05 (первое появление s05)
- текст: **Decision:** permanent operator management, microdispatch and routine approvals are not target operating model. **Consequence:** AICM owns internal goals/programs/continuation. «Owner/Operator не является: permanent task dispatcher; roadmap author; routine approval gate; manager of agents/programs; provider of interpretations and next steps.» Logical roles: **Owner / Beneficiary** — сторона, чьё enduring economic interest определяет Purpose Kernel; **External Enabler** — субъект, который предоставляет ресурс или выполняет действие, когда это объективно требует внешней legal/physical identity (capital; identity verification; account/email где third-party rules требуют human/legal person; API credentials; contractual acceptance; payment instrument activation; physical hardware/network access); **AICM** — autonomous system that decides what to pursue. «One human may currently be both Owner and External Enabler. That does not create operating management authority by default.» *(HQ reading: «Оператор» в более ранних сессиях = External Enabler для login/payment/file, не operator-manager. Это уточнение уже confirmed PREF-014, не новое правило.)*

### `AICM-L0-PREF-015` — Bounded external dependency declaration
- действующая: s05 (первое появление s05)
- текст: **Decision:** AICM detects and formulates external dependency requests with purpose, minimum scope, alternatives, consequences and continuation. **Consequence:** human need not infer what system requires; request is not a roadmap instruction. External dependency — first-class evidence-bearing autonomy gap, не hidden assumption, vague request, new operator-authored task, global pause. AICM must specify: exact resource/action/access; purpose/program linkage; why it cannot currently self-resolve; minimum privileges and scope; time sensitivity/expiry; expected contribution; material risks/costs; alternatives; fallback; revocation/renewal; independent work that continues. «A pending dependency must not stop the whole system»: keep unrelated programs active; preparatory work; revisit alternatives; detect expiry; retire/replan blocked program; resume automatically when available. Продолжает TF-PREF-030.

### `AICM-L0-PREF-016` — Dependency reduction and autonomy expansion
- действующая: s05 (первое появление s05)
- текст: **Decision:** removable external dependencies become candidate capability gaps; AICM seeks lawful, reliable and economically justified reduction. **Consequence:** current manual acts are not assumed permanent. Investigate whether dependency can be eliminated, automated, delegated to a lawful provider, replaced with less privileged mechanism, made renewable/revocable without human intervention, brought under durable legal/operational structure, reduced in frequency/scope/consequence. «Dependency reduction is not unconditional. It must respect law, ownership, security, cost, reliability and comparative value.» Full autonomy: no routine external management; autonomous goal/program formation; autonomous continuation; increasing ability to acquire resources lawfully; explicit handling of unavoidable external realities. Не означает pretending unavailable capital exists, bypassing identity/law, silently expanding authority, obtaining credentials without entitlement. «full autonomy is a five-year direction with measurable dependency reduction, not an impossible bootstrap precondition.»

### `AICM-L0-PREF-017` — Open lawful economic scope
- действующая: s05 (первое появление s05)
- текст: **Decision:** trading is first domain, not permanent specialization; AICM may consider any lawful economic activity with evidence, authority and purpose contribution. **Consequence:** DeFi or other domains can be explored without Purpose amendment. Условия рассмотрения domain: causal contribution to enduring purpose; comparative value; sufficient knowledge/evidence; actual resources/access; applicable authority; risk and reversibility; observability and reporting; exit/repair path. «Potential future domains may include DeFi or other economic activities, but this preference does not approve any specific domain or action.» Architectural curiosity applies to new models, open-source, data/execution tech, emerging financial protocols, cost/latency, tools that reduce dependencies. «Discovery alone does not authorize adoption.»

### `AICM-L0-PREF-018` — AICM system identity
- действующая: s05 (первое появление s05)
- текст: **Decision:** AICM as whole is autonomous identity; agents/models/providers are replaceable implementations. **Consequence:** provider replacement does not reset purpose, knowledge or program continuity. Identity carried by: active Purpose Kernel and successors; knowledge/evidence lineage; capability identities and maturity; authority/constraint state; durable program state; economic and operational outcomes; ownership/beneficiary continuity. «No provider prestige or agent persona grants system-level identity or authority.»

### `AICM-L0-PREF-019` — Accountability by construction
- действующая: s05 (первое появление s05)
- текст: **Decision:** evidence history must support internal learning, owner reporting, accounting reconciliation and future tax/legal reporting from the outset. **Consequence:** material actions/outcomes cannot depend on retrospective narrative reconstruction. Future evidence must support: what the system did; why and under which purpose/program; information boundary; authority and resources; transactions/costs/positions/obligations; who/what owns the economic result; realized and unrealized outcomes; fees, financing, taxes/possible tax obligations and other liabilities; corrections and successor lineage; unresolved discrepancies. Reporting is not self-praise: must also expose losses/drawdowns, costs and opportunity cost, failed programs, uncertainty, unresolved reconciliation, material risks, dependencies, whether claimed improvement produced actual uptake/outcome.

### `AICM-L0-PREF-020` — Candidate Goal identity boundary
- действующая: s06 (первое появление s06)
- текст: **Status:** CONFIRMED. **Decision:** Candidate Goal is a durable first-class hypothesis object with its own identity and lifecycle, not a task, instruction or execution commitment. **Consequence:** autonomous discovery does not silently become committed work.

### `AICM-L0-PREF-021` — Conditional automatic lifecycle transitions
- действующая: s06 (первое появление s06)
- текст: **Status:** CONFIRMED. **Decision:** lifecycle transitions may be fully automatic but require architecture-defined conditions, explicit reason/evidence lineage and distinct logical roles. Routine human approval is not required. **Consequence:** autonomy is preserved without arbitrary agent discretion.

### `AICM-L0-PREF-022` — Evolution Portfolio semantics
- действующая: s06 (первое появление s06)
- текст: **Status:** CONFIRMED. **Decision:** Evolution Portfolio is a durable cross-domain model of Candidate Goals and Durable Programs, not a task list. Waiting is meaningful. Evaluation mechanisms are replaceable and do not own object identity. **Consequence:** many directions can coexist and survive provider, algorithm and session replacement.

### `AICM-L0-PREF-023` — Stable Durable Program architectural contract
- действующая: s06 (первое появление s06)
- текст: **Status:** CONFIRMED. **Decision:** every Durable Program exposes stable identity, Purpose linkage, origin/evidence, lifecycle state, dependencies/resource profile, success/closure, continuity/successor and learning-return semantics independent of future scoring implementation. **Consequence:** a program can remain durable while tasks, workers, providers and evaluation methods change.

### `AICM-L0-PREF-024` — No innate priority
- действующая: s06 (первое появление s06)
- текст: **Status:** CONFIRMED. **Decision:** no candidate or program has creator-, provider-, domain- or age-derived priority. Current standing is evidence- and state-dependent and revisable. **Consequence:** origin and prestige cannot become hidden authority.

### `AICM-L0-PREF-025` — Goal/Program identity and material successor lineage
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** Candidate Goal and Durable Program remain distinct durable identities. A material change to outcome, scope, assumptions, dependencies, success boundary, downside or Purpose linkage creates an explicit successor rather than hidden mutation. **Consequence:** object lineage remains auditable across changes and provider/model replacement.

### `AICM-L0-PREF-026` — Reproducible Candidate Goal minimum
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** an eligible Candidate Goal contains provenance/evidence, Purpose linkage, outcome, alternatives, strongest challenge, dependencies/resources, uncertainty/downside, urgency/learning path, exit/closure and distinct outcome-return semantics, plus enough reproducible context for another authorized system instance to reconstruct its basis without the originating model's private context. **Consequence:** persuasive text or model confidence cannot substitute for admissible evidence-bearing content.

### `AICM-L0-PREF-027` — Autonomous promotion adjudication
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** promotion to Durable Program is fully autonomous, architecture-defined and role-separated. Neither routine human approval nor one agent owns the decision. Insufficient evidence produces bounded evidence acquisition, reasoned WAIT or REJECT with next wake/trigger. **Consequence:** autonomy is complete at the decision level without becoming arbitrary.

### `AICM-L0-PREF-028` — Gated multidimensional Portfolio adjudication
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** candidates first pass eligibility gates and are then compared across multiple decision dimensions. No constitutional global utility scalar determines priority. Current standing is revisable by new evidence/state, while historical decisions remain immutable. **Consequence:** incomparable harms, authority gaps and uncertainty cannot be averaged away or retroactively hidden.

### `AICM-L0-PREF-029` — Opportunity cost, reservations and continuous re-adjudication
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** every material allocation exposes scarce-resource use/reservations, conflicts, displaced alternatives, switching consequences and review triggers. Portfolio allocation may be re-adjudicated on material state/evidence change. **Consequence:** local programs cannot silently consume shared resources or freeze obsolete priority.

### `AICM-L0-PREF-030` — Bounded adaptive exploration with observable return
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** AICM maintains a bounded adaptive exploration envelope rather than leftovers or a fixed percentage. Every material exploration has an observable economic, epistemic, falsification, dependency-reduction or capability return contract. **Consequence:** the system can evolve without permitting unbounded curiosity or economically/epistemically empty experiments.

### `AICM-L0-PREF-031` — Durable continuity, WAIT and Terminal Closed
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** Candidate Goals and Durable Programs preserve state/cursor, next wake/trigger, dependencies, evidence path, worker/provider fallback, replan/successor, failure, retirement and Terminal Closed semantics. Chat/provider termination is not Program termination. **Consequence:** `Session End != Program End`; waiting is durable and reasoned rather than forgotten.

### `AICM-L0-PREF-032` — System-level no-DONE and distinct outcome return
- действующая: s07 (proposed в s06; CONFIRMED в s07 — действующий текст = s07)
- текст: **Status:** CONFIRMED. **Decision:** AICM has no global DONE inside Portfolio logic. After bounded Program closure it returns to Purpose and the next autonomous observation/review cycle. Outcomes return separately to knowledge, capability, constraints/authority, Portfolio and accountability; P&L/local success cannot directly self-ratify knowledge or authority. **Consequence:** individual programs can close without ending system evolution or creating a self-confirming loop.

### `AICM-L0-PREF-033` — Semantic separation of admissibility inputs
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** `Reality Condition`, `Constraint`, `Standing Obligation` and `Authority Envelope` are semantically distinct. A common future technical carrier may not collapse their meaning, lifecycle or authority. **Consequence:** fact cannot be internally repealed, obligation cannot become an optional opportunity and missing prohibition cannot be treated as permission.

### `AICM-L0-PREF-034` — Origin-governed amendment authority
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** normative provenance determines the change regime. Constitutional/identity, externally binding, internal protective, operational and experimental/temporary boundaries have distinct amendment, applicability, expiry and successor authority. **Consequence:** the component requesting change cannot select the easiest lifecycle; external and constitutional boundaries cannot be locally self-amended.

### `AICM-L0-PREF-035` — Scope, applicability and evidence separation
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** origin, scope, current applicability, supporting evidence and the resulting disposition are distinct and reproducible. No material boundary is globally active merely because a record exists. **Consequence:** false blocking and false permission are both reviewable; uncertainty routes to evidence acquisition, WAIT, dependency request or reasoned non-promotion rather than silent inference.

### `AICM-L0-PREF-036` — Non-interchangeable lifecycle transitions
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** challenge, exception, amendment, expiry, retirement and successor have distinct semantics. Material change creates a recorded version or successor; history is not rewritten. **Consequence:** a temporary exception cannot silently become the general rule, expiry cannot arise from neglect and retirement cannot erase evidence.

### `AICM-L0-PREF-037` — Separation of amendment functions and anti-self-exemption
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** proposal/initiation, challenge/evaluation, approval/adjudication and execution/application remain logically distinct. The governing authority follows boundary origin; the constrained or executing component cannot locally approve its own exemption. **Consequence:** autonomy does not become unilateral self-release from constraints.

### `AICM-L0-PREF-038` — Distinct outcome return without self-ratification
- действующая: s08 (первое появление s08)
- текст: **Status:** CONFIRMED. **Decision:** operational, protected-outcome/effectiveness, epistemic and governance outcomes return separately. Any may trigger a review proposal, but none directly changes a rule, grants an exception, expands authority or establishes a knowledge verdict. **Consequence:** local success or P&L cannot self-validate the boundary change that enabled it.

### `AICM-L0-PREF-039` — Authority-minimal logical ownership of autonomous-cycle continuity
- действующая: s09 (первое появление s09)
- текст: **Status:** CONFIRMED. **Decision:** Autonomous Evolution Engine is the logically unique responsibility for coordination, viability and durable continuation of the complete autonomous evolution cycle. Physical realization may be distributed, redundant and replaceable, but competing authoritative control planes are prohibited. **Authority boundary:** continuity ownership does not grant Purpose amendment, Portfolio adjudication, Constraint Amendment/exception approval, knowledge-ratification, Trading Decision, RiskGate or execution authority. **Consequence:** full-cycle continuation has an accountable owner without creating a universal super-agent.

### `AICM-L0-PREF-040` — Mandatory cycle initiation and recovery triggers
- действующая: s09 (первое появление s09)
- текст: **Status:** CONFIRMED. **Decision:** the Engine must initiate, resume or reconcile the appropriate governed process on due next wakes/lifecycle transitions, material observations/gaps/risks/opportunities, obligation or constraint/authority changes, new outcomes, orphan/stall/unconsumed-outcome conditions, cursor loss/inconsistency and component/provider degradation. **Consequence:** recovery is part of autonomy; a trigger creates coordination duty but not substantive decision authority.

### `AICM-L0-PREF-041` — Governed inputs and coordination-only outputs
- действующая: s09 (первое появление s09)
- текст: **Status:** CONFIRMED. **Decision:** Engine inputs are governed Purpose/state/Foundation/Candidate/Portfolio/Program/capability/admissibility/outcome/event/cursor entities. Outputs are initiation, routing, reconciliation, recovery, evidence/dependency/challenge/review/re-adjudication proposals/requests, status/cursor/next-wake recording and outcome return. **Authority boundary:** the Engine cannot issue substantive Purpose, Portfolio, Constraint, knowledge, trading, risk or execution verdicts from its continuity role. **Confirmed clarification:** the Engine coordinates continuous improvement of the whole AICM system, including trading knowledge, capabilities, processes and programs, while Trading Decision, RiskGate and execution remain in separately authorized domain contours. MANIFEST `confirmed_clarification` (не новый PREF ID): «Evolution Engine coordinates improvement of the whole AICM system, including trading, without acquiring Trading Decision, RiskGate or execution authority.»

### `AICM-L0-PREF-042` — Authoritative logical autonomous-cycle cursor
- действующая: s09 (первое появление s09)
- текст: **Status:** CONFIRMED. **Decision:** one authoritative logical cycle-continuity cursor durably represents material transitions, governed process ownership, pending evidence/dependency/authority, WAIT, recovery, outcome uptake and next wake. **Normalization:** one authoritative cursor does not mean one sequential thread and does not replace per-Program cursors. Concurrent Programs remain valid; competing authoritative cycle owners do not. **Consequence:** no material cycle is lost and no global `DONE` terminates autonomous evolution.

### `AICM-L0-PREF-043` — Degradation and recovery without authority expansion
- действующая: s09 (первое появление s09)
- текст: **Status:** CONFIRMED. **Decision:** degradation moves affected work to governed WAIT/recovery, preserves the latest consistent point, history, constraints/obligations/authority, dependencies and next wake, then resumes only through valid governed continuation. **Authority boundary:** failure does not create Authority, waive a Constraint, approve an exception, invent evidence or permit direct execution. Process restart alone is not recovery. **Consequence:** autonomy survives component/provider failure without weakening constitutional boundaries.


### D.4 `AICM-DOC-PREF-001`…`005` — document-transfer discipline

### `AICM-DOC-PREF-001` — Documents, not chat, are durable project memory
- действующая: s06 (s06)
- текст: **Status:** CONFIRMED. **Decision:** chats are working sessions; durable state is carried by the cumulative package and explicit registers. Governance §1: «The AICM project must survive chat limits, model/provider replacement, long time gaps and multiple architecture sessions without relying on conversational memory.» `chat = temporary reasoning workspace`; `session documents = durable decision record`; cumulative package = transfer and preservation unit; Progress Register + Handoff = next-session entry point. Progress Register §1: «A chat is a temporary working surface. This register plus the cumulative package is the durable project memory.» README §6: the chat is a working session, not the project memory; the cumulative package is the durable handoff unit.

### `AICM-DOC-PREF-002` — Mandatory Progress Register and Handoff
- действующая: s06 (s06)
- текст: **Status:** CONFIRMED. **Decision:** every session closes with an updated Project Progress Register and next-session Handoff. Progress Register header `update_rule`: must be updated at every session close. §10 session close protocol includes: update Discussion Record; Preference Draft with distinct CONFIRMED/PROPOSED/OPEN; Decision Register; Architecture Roadmap status only if a gate changed; this Project Progress Register; prepare next-session Handoff. Governance §3 required session documents include Project Progress Register and next-session Handoff. README §6: `AICM Project Progress Register` is the first entry point; the next-session Handoff states the exact active block, inherited decisions, open boundary and required output.

### `AICM-DOC-PREF-003` — Versioned self-contained cumulative package
- действующая: s06 (s06)
- текст: **Status:** CONFIRMED. **Decision:** the handoff unit is a versioned self-contained ZIP containing current documents, predecessor lineage, manifest and preservation report. Governance §2: every successor package contains the unchanged Foundation Vision and all prior session addenda; one new additive session folder; current root Package Index; current root Manifest with SHA-256; Preservation Report comparing predecessor scope; exact predecessor package under lineage; predecessor root metadata; Word renderings for core human-review documents; source inputs used by the new session. Governance §7 transfer-ready only when confirmed/proposed/open are correctly separated; active block and next gate are explicit; manifest hashes match; predecessor hash is recorded; preservation report verifies unchanged predecessor scope; handoff can start a new session without hidden conversation context. Additive-only (Governance §5): prior session folders are not edited in place.

### `AICM-DOC-PREF-004` — New-session read-before-design rule
- действующая: s06 (s06)
- текст: **Status:** CONFIRMED. **Decision:** a new session reads Progress Register, Handoff, Decision Register, active Roadmap and active Preference Draft before proposing or revisiting decisions. Progress Register §11 bootstrap: Read Progress Register first, then the latest Handoff, Decision Register, approved Roadmap and active Preference Draft. Confirm the active block and exclusions at the start. Do not reopen closed preferences without a named material contradiction. Continue only the next transition gate. Governance §6: architect states current block, exclusions and expected result; does not reopen closed preferences without a named material contradiction. README §6: A new chat must begin by attaching the latest cumulative package and instructing the architect to read the Progress Register and Handoff before proposing changes.

### `AICM-DOC-PREF-005` — Ordered multi-archive transfer set for post-Session-10 addenda
- действующая: s12 (s12)
- текст: **Status:** CONFIRMED PROJECT-CONTINUITY PREFERENCE. **Decision:** during the remaining architecture sessions, the transfer unit may be an ordered set consisting of the sealed cumulative base through Sessions 01–10 plus Session 11, Session 12 and later addendum ZIPs attached separately in chronological order. Each addendum records exact predecessor hashes, required reading order, latest Progress/Roadmap/Decision/Handoff state and does not claim that predecessors are embedded when they are not. **Relation to `AICM-DOC-PREF-003`:** preserves its substantive goals of versioning, self-contained decision state, lineage, manifest and reliable handoff while establishing a bounded transport profile. A later consolidated cumulative release remains allowed. Governance reference: `AICM-DOC-PREF-001–004` remain in force. Ordered set = sealed cumulative base through Sessions 01–10 + Session 11 Addendum + Session 12 Addendum + each later addendum in chronological order. Each addendum must be additive and not rewrite predecessors; record exact predecessor hashes and byte lengths; identify required reading order; contain latest Progress/Roadmap/Decision/Closure/Handoff and start instruction; include source input handoff and curated decision capture; separate `CONFIRMED`, `PROPOSED`, `OPEN`, `REJECTED` and `SUPERSEDED`; provide an honest manifest that states whether predecessors are embedded or separately supplied; create no implementation/runtime authority. «No package may claim exact embedded predecessor preservation when it contains only a hash reference and the predecessor is supplied separately.»


### D.5 `AICM-ROADMAP-L0-APPROVAL-001`

### `AICM-ROADMAP-L0-APPROVAL-001` — Architecture Roadmap L0
- действующая: s06 (первое появление s06; later roadmap versions — status successors, не новый PREF ID)
- текст: **Status:** CONFIRMED. **Decision:** The dependency-driven sequence and transition gates in Architecture Roadmap L0 are approved. Version 0.2 is active. **Consequence:** Work proceeds in block order; roadmap approval does not itself close block content. Roadmap §1: «`Architecture Roadmap L0 v0.1` was explicitly accepted in Session 06. Version 0.2 records that approval and updates only progress status; it does not retroactively change the agreed block order.» «The Roadmap is an active semantic sequencing and transition framework. It is not an implementation contract, runtime specification, capital authorization or deployment plan.» README §3 dependency order: closed prerequisite base → L0-B1 Purpose Kernel and target autonomy → L0-B2 Autonomous Goal Formation and Evolution Portfolio → L0-B3 Constraint Taxonomy and Amendment Lifecycle → L0-B4 Evolution Engine Responsibility and Separation of Powers → Level 1 bounded runtime cognition and E2E proof → Level 2 durable autonomous substrate → Level 3 economic and external autonomy → Level 4 implementation readiness. «Roadmap approval does not close any content block by itself. It authorizes work to proceed in that order.» Discussion record §2: Roadmap становится active sequencing authority на уровне discussion architecture; не является implementation contract и не закрывает содержательные решения внутри блоков.


### D.6 `AICM-L1-PREF-001`…`055` — Level 1 runtime cognition / Consilium / E2E slice

### `AICM-L1-PREF-001` — Durable Bundle Lineage and Immutable Sealed Edition
- действующая: s10 (первое появление s10)
- текст: **Status:** CONFIRMED. **Decision:** Runtime Read Bundle has a durable `Bundle Lineage` and exact immutable sealed `Bundle Edition`. Assembly before sealing is non-authoritative. Material reasoning binds to one exact Edition; authoritative historical resolution through `latest/current` is prohibited. Any post-seal material change creates a successor Edition or an explicitly related Lineage. **Boundary:** sealing fixes content and information boundary; it does not establish truth, evidence sufficiency, knowledge maturity, action permission, RiskGate or execution authority.

### `AICM-L1-PREF-002` — Explicit Purpose, Consumer, Work, Read-Purpose and Snapshot Binding
- действующая: s10 (первое появление s10)
- текст: **Status:** CONFIRMED. **Decision:** every Bundle explicitly binds to Purpose Interpretation, authorized Consumer Contour, Candidate Goal or Durable Program, Read Purpose and exact SituationContextSnapshot. **Consistency normalization:** stable Purpose/consumer/work/read-purpose anchors define Bundle Lineage; exact Snapshot pins Bundle Edition. Snapshot refresh under unchanged stable anchors creates a successor Edition; material stable-anchor change creates a new explicitly related Lineage. **Autonomy boundary:** governed autonomous processes supply the bindings. Context Resolver cannot invent or silently substitute them.

### `AICM-L1-PREF-003` — Professional Governed Composition and Learning-Ready Lineage
- действующая: s10 (первое появление s10)
- текст: **Status:** CONFIRMED. **Decision:** every material Bundle Edition accounts for exact identity/boundary, SituationContextSnapshot, Foundation releases and assessment versions, explicit applicability/retrieval roles, strongest credible challenge, alternatives, counterexamples, unknowns, evidence/source lineage, applicable Reality Conditions/Constraints/Standing Obligations/Authority, capability/dependency/resource assumptions, completeness/omission/freshness/supersession declarations, reproducible delivery and model-independent learning-ready lineage. **Challenge rule:** material challenge is included or its bounded absence/unavailability/non-applicability is explicit; silent absence is invalid. **Learning boundary:** later outcome, correctness, actual-use, influence or confidence records link to the Edition and never mutate it. Training datasets/model artifacts are separate governed derived outputs, not the Bundle or canonical knowledge.

### `AICM-L1-PREF-004` — Semantic Assembly Boundary and Advisory Resolver Constraint
- действующая: s10 (первое появление s10)
- текст: **Status:** CONFIRMED. **Decision:** a Bundle becomes a sealed governed read input only after identity completeness, mandatory-plane accounting, information-boundary integrity, governance/conflict integrity and an explicit assembly declaration of included/excluded/unavailable material and fitness for the Read Purpose. **Readiness distinction:** semantics must distinguish fit, fit only for an explicitly bounded/degraded read purpose and not fit; exact labels remain implementation-open. **Authority boundary:** Context Resolver/assembly may resolve, retrieve, assess freshness/applicability, preserve conflicts, declare omissions and finalize a record. It cannot choose Purpose/work, leading hypothesis, truth, authority, Decision, RiskGate or execution. Delivery does not create consumer authority.

### `AICM-L1-PREF-005` — HypothesisTemplate, HypothesisCase and immutable context-bound HypothesisInstance identity
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED. **Decision:** `HypothesisTemplate` is reusable Foundation knowledge; `HypothesisCase` is the durable identity of one investigated question and its continuation; `HypothesisInstance` is one exact independently assessable proposition bound to one exact sealed Runtime Read Bundle Edition. Alternatives are separate Instances. Formed Instance content is immutable; assessment and lifecycle events are linked records. **Novelty rule:** an Instance may reference zero, one or multiple exact Template Versions. Untemplated novel formation is allowed with explicit provenance and does not self-promote to Foundation knowledge.

### `AICM-L1-PREF-006` — Plural composition, evidence topology and strongest-challenge completeness
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED. **Decision:** a HypothesisCase owns the competing issue space. Each material Instance independently accounts for exact claim, scope/horizon, support, counterevidence, strongest credible challenge, counterexamples, predictions, invalidation, differentiating observations, alternatives and unknowns. Evidence records remain separately identifiable. **Boundary:** comparative standing, including a current leading interpretation, is a revisable Case-level Assessment and does not erase alternatives, establish truth or create action authority. One aggregate confidence scalar is rejected as the semantic model.

### `AICM-L1-PREF-007` — Reassessment, successor, invalidation, revival and bounded closure lifecycle
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED. **Decision:** same exact proposition and same exact Bundle Edition may receive a new linked Assessment. New material context/evidence, changed claim/scope/horizon or material content correction creates a successor Instance. Material change to the investigated question or stable work bindings creates a related successor Case. **Lifecycle:** invalidation is context-specific and preserves history; corrective assessment and context-driven revival are explicit; retirement is not deletion; Terminal Closed belongs to the bounded Case and records residual uncertainty and successor relations.

### `AICM-L1-PREF-008` — Durable WAIT, persisted next wake, automatic recovery and scoped NO_TRADE
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED. **Decision:** `WAITING_FOR_EVIDENCE` is an active durable HypothesisCase state with exact unresolved question, evidence plan, trigger/next wake, horizon, fallback, cursor and automatic-resume rule. Recovery survives model/provider/process replacement and cannot expand authority or mutate old context. **NO_TRADE normalization:** `NO_TRADE` is a later trading-decision disposition for one opportunity/horizon. It is not a HypothesisInstance/Case status, truth verdict, global stop, system failure or block on capability evolution.

### `AICM-L1-PREF-009` — Hypothesis authority boundary and exact downstream handoff
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED. **Decision:** Template, Case, Instance, Assessment and Case comparison remain explanatory/evaluative. They cannot own Purpose/Portfolio promotion, Foundation release, Constraint/Authority amendment, Trading Decision, RiskGate, capital allocation, deployment/container activation or execution. They hand off exact lineage to separately authorized later contours. **Activation clarification:** capability/container activation belongs to later capability proof, change-authority and deployment contours. Those contours are autonomous within standing authority; a human is not introduced as the default activator.

### `AICM-L1-PREF-010` — Autonomous progression of validated capabilities/changes into operational use
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED CROSS-CUTTING GUARDRAIL. **Decision:** when a mechanism, capability or change completes its applicable governed proposal/challenge/evaluation/promotion lifecycle and all required authority/resources already exist, AICM must autonomously progress it through packaging, activation, consumer enrollment, monitored use, rollback and successor/retirement handling. Routine Owner/Operator enablement is not required. **Boundary:** no silent authority expansion; no bypass of legal, credential, capital, risk, security, provider or rollback requirements. Detailed realization remains open under L2-B2, L2-B4, L4-B2 and L4-B3.

### `AICM-L1-PREF-011` — Minimum operator burden for irreducible external dependencies
- действующая: s11 (первое появление s11)
- текст: **Status:** CONFIRMED CROSS-CUTTING GUARDRAIL. **Decision:** AICM performs all technically and legally available internal work itself. When an objective external act remains, the Owner/Operator receives a complete minimally scoped ready-to-act request containing exact need, rationale, amount/range where applicable, privileges, risks/costs, alternatives, expiry, exact steps, verification, fallback and automatic resume. **Boundary:** the Owner/Operator is an External Enabler, not a permanent manager, process designer, mechanism discoverer or routine activation gate. Capital/credential/legal authority remains governed by later blocks.

### `AICM-L1-PREF-012` — Governed knowledge presence, absence, discovery, formation and experiment lineage
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** AICM distinguishes governed knowledge that exists, knowledge not yet available to the consumer, external information not yet discovered/verified, observations not yet formed into governed knowledge, explicit hypothesis/assumption/unknown state and evidence obtainable only through future observation/action/experiment. Missing knowledge triggers an explicit discovery, hypothesis, WAIT, experiment, bounded-uncertainty or governed non-action path; it never becomes an unrecorded fact. **Boundary:** knowledge release/promotion authority remains L1-B4.

### `AICM-L1-PREF-013` — Independent knowledge, uptake, reasoning, Decision, RiskGate, execution, outcome and learning lifecycles
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** each domain has durable identity, exact input boundary, semantic owner, immutable history and correction/successor lineage. A DecisionTrace links exact records and relations without combining their authority or rewriting the Decision-time state. **Boundary:** reasoning does not imply Decision authority; Decision does not imply RiskGate or execution; outcome learning does not directly ratify knowledge or authority.

### `AICM-L1-PREF-014` — Consumer-specific uptake, actual use, reasoning role and material influence
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** publication/release, delivery/availability, retrieval/exposure, interpretation, consideration, explicit role, actual use/challenge/non-use and material influence/non-influence/dispute are distinct, exact consumer/version/Read-Purpose/context-specific claims. **Boundary:** a receipt proves only the uptake stage supported by its evidence.

### `AICM-L1-PREF-015` — Typed evidence and prohibition on cross-stage evidence substitution
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** every material stage and relation requires evidence appropriate to its claim. Evidence of release cannot prove use; retrieval cannot prove influence; Decision cannot prove RiskGate/execution; P&L cannot prove knowledge truth. **Boundary:** explicit observable records and governed assessments are required; hidden cognition is not the durable audit path.

### `AICM-L1-PREF-016` — Full immutable Evidence and Decision Lineage Graph
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** knowledge, bundles, hypotheses, reasoning, Decisions/non-actions, RiskGate, execution, outcomes and learning are connected through first-class immutable typed relationship records with exact endpoints, context, provenance, evidence, uncertainty and correction/successor lineage. DecisionTrace is a reproducible bounded view over the graph. **Boundary:** positive, negative, challenge, non-use, failure, ambiguity and disputed-attribution paths are preserved.

### `AICM-L1-PREF-017` — Governed additive evolution of relationship vocabulary
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** relationship types are versioned and evolve additively. New types declare endpoint domains, direction, temporal constraints, evidence obligations, permitted/prohibited inference, authority effect and successor semantics. Historical edge meaning is not silently rewritten. *(Register §4 не даёт отдельного **Boundary:** для PREF-017 — поле не изобретается.)*

### `AICM-L1-PREF-018` — Semantic validation, multidimensional actionability, governed non-action and separated outcomes
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** relation instances are validated against exact endpoints, type, context, time, evidence and asserting authority before acceptance. Confidence/actionability remains multidimensional. Decision/non-action, RiskGate, execution/non-execution and scenario/plan/risk/execution/operational/economic outcomes are separate. Corrections create linked successors; P&L is not a direct knowledge verdict. **NO_ACTION boundary:** `NO_TRADE` is a trading-domain scoped non-action for exact opportunity/horizon, not a HypothesisCase state or global stop.

### `AICM-L1-PREF-019` — Separate learning-data eligibility and future model-learning metadata
- действующая: s12 (первое появление s12)
- текст: **Status:** CONFIRMED. **Decision:** potential downstream use for retrieval evaluation, supervised/preference learning, fine-tuning, distillation or other declared learning purposes is represented by a separate governed metadata overlay covering task, sample role, evidence quality, outcome maturity, rights/restrictions, leakage, contamination, duplication, ambiguity and correction status. **Boundary:** no event is automatically eligible; metadata does not rewrite evidence or authorize collection, training, model promotion or deployment.

### `AICM-L1-PREF-020` — Consilium Framework as a universal governed pattern
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** Consilium is a domain-general governed pattern for plural analysis, challenge and knowledge-evolution recommendation. Trading Consilium is the first domain specialization, not the identity of the pattern. Architecture and other lawful domains may instantiate their own Consilia inside exact competence and authority boundaries. **Boundary:** A common framework does not create one universal super-Consilium and does not merge domain authority.

### `AICM-L1-PREF-021` — Model-, method- and provider-neutral longitudinal knowledge readiness
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** AICM preserves knowledge, deliberation, dissent, lineage, actual-use evidence and separated outcomes in durable forms usable by future analysis, evaluation and learning methods without tying semantic architecture to a current model, provider or training technique. **Boundary:** Reuse readiness is not dataset membership, collection authority, training authorization, model promotion or deployment authority; AICM-L1-PREF-019 remains in force.

### `AICM-L1-PREF-022` — Dynamic role assembly with mandatory deliberation functions
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** A Consilium is a dynamic collegial process. For each material question it assembles roles appropriate to the task while preserving mandatory logical functions: initiation/proposal, strongest alternative and challenge, evidence/provenance review, applicability and reuse-scope review, use/outcome review where available, synthesis and an explicit recommendation. **Boundary:** No fixed number of agents, models or providers is constitutional; mandatory functions may not be omitted merely because one implementation appears capable.

### `AICM-L1-PREF-023` — Substantive independence, conflict disclosure and anti-self-confirmation
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** Material conclusions require substantively independent challenge. Independence is judged by evidence access, incentives, role separation, prompt/context diversity, conflict disclosure and ability to preserve dissent—not by role labels or model count alone. The proposer cannot be the sole challenger, evidence judge and release adjudicator of its own candidate. **Boundary:** Independence may be scaled by impact, uncertainty, reversibility and reuse scope, but cannot be silently waived.

### `AICM-L1-PREF-024` — Governed self-evolution without privileged self-approval
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** A Consilium may autonomously detect defects in its own framework, roles, policies or performance and create successor change candidates. Those candidates pass the same role-separated evidence, challenge, authority, release, monitoring, rollback and retirement lifecycle as other material changes. **Boundary:** Self-observation creates proposal authority only; it does not create self-ratification, self-exemption or constitutional amendment authority.

### `AICM-L1-PREF-025` — Multi-level Consilium topology
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** AICM uses a common Consilium Framework, persistent domain Consilia and bounded task Consilia. Domain Consilia preserve long-horizon competence and evolution; task Consilia assemble the exact roles and evidence for a bounded question. Cross-domain work preserves each domain’s separate assessment and authority rather than collapsing them into one vote. **Boundary:** Exact process placement, service boundaries and federation protocol remain realization questions.

### `AICM-L1-PREF-026` — Class-specific evidence sufficiency under governed policy
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** There is no single universal evidence threshold. Sufficiency is evaluated under a versioned policy appropriate to the candidate class, epistemic claim, impact set, uncertainty, reversibility, reuse scope, affected consumers and protected outcomes. The policy declares required evidence, independent challenge, observation horizon, dissent treatment and permitted disposition. **Boundary:** A Domain Consilium applies the policy and records uncertainty; it may not invent an easier threshold for its own candidate.

### `AICM-L1-PREF-027` — Continuous candidate queue with separated knowledge-evolution stages
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** Foundation evolution is continuous through durable Knowledge Candidates. Candidate formation/admission, deliberation, assessment/recommendation, release adjudication, dissemination, monitored actual use, outcome return, correction, supersession, retirement and rejection are separate durable stages with immutable lineage and explicit WAIT/next-wake behavior. **Boundary:** A queue item cannot remain indefinitely “promising” without a governed disposition, owner/cursor, trigger, horizon or Terminal Closed path.

### `AICM-L1-PREF-028` — Functional invariants over fixed committee composition
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** Semantic architecture fixes functions, independence obligations, evidence duties, authority boundaries and output contracts—not a permanent roster, agent count, model family or provider. Composition may evolve autonomously when proof, authority and rollback requirements are satisfied. **Boundary:** A dynamic composition may not use flexibility to remove mandatory challenge, evidence review, dissent preservation or release separation.

### `AICM-L1-PREF-029` — Domain assessment separated from Knowledge Evolution Authority
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** A Domain Consilium owns evidence-bearing assessment and recommendation about whether a Knowledge Candidate is sufficiently supported, scoped and reusable. Knowledge Evolution Authority owns the governed knowledge lifecycle and issues the separate disposition: release, scoped release, WAIT, rejection, correction, supersession, restriction, retirement or successor request. Foundation history is immutable and affected consumers receive successor/restriction notification. **Boundary:** Neither contour owns Trading Decision, RiskGate, execution, capital, credential or external legal authority. Knowledge Evolution Authority is a governed authority contour, not a routine Owner approval gate.

### `AICM-L1-PREF-030` — Constitutionally pre-delegated autonomous initiative and authority evolution
- действующая: s13 (первое появление s13)
- текст: **Status:** CONFIRMED. **Decision:** The AICM Constitution and origin-governed derived policies are the primary source of pre-delegated internal authority. Within that standing mandate, Consilium and Knowledge Evolution operate proactively and autonomously: they detect triggers, create candidates, assemble review, adjudicate knowledge dispositions, evolve subordinate internal policies and Authority Envelopes where the originating authority permits, propagate changes, monitor use and continue without routine Owner confirmation. An Authority Envelope delineates autonomous action space; it is not a per-step permission token. **Boundary:** Most future internal expansion is an autonomous successor/change inside constitutionally delegated meta-authority, not “new permission from the Owner.” External participation is reserved for objectively irreducible external rights/resources/actions such as legal identity, KYC, contractual acceptance, payment, account/credential provisioning or another act the system cannot lawfully or physically perform. Beneficiary identity, terminal Purpose, externally binding law/contract and other origin-protected boundaries cannot be silently self-amended.

### `AICM-L1-PREF-031` — Unified-system bounded-slice identity
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** a bounded E2E slice is one proof contour inside unified AICM, not an independent sovereign subsystem or new terminal Purpose. **Boundary:** one-system identity does not collapse logical authority separation or require one physical process/model/agent. Draft: «a bounded E2E slice is a proof contour inside one unified AICM. It is not an independent sovereign subsystem, separate beneficiary, new terminal Purpose or permanent domain boundary.» «logical authority separation remains mandatory. “One organism” does not mean one physical process, one model, one agent or one universal decision-maker.» Restatement of inherited L0 unified identity / Purpose — mention of inherited L0, не новый ID и не reopen L0.

### `AICM-L1-PREF-032` — Opportunity discovery remains upstream
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** continuous World-State/Self-State observation, Candidate Goal formation, Evolution Portfolio adjudication and Durable Program admission remain Level 0 responsibilities. The first slice begins after bounded admission and does not replace the upstream cycle with a generic opportunity object. Draft: «continuous World-State/Self-State observation, opportunity discovery, Candidate Goal formation, Evolution Portfolio adjudication and Durable Program admission remain governed by the already closed Level 0 cycle. `L1-B5` does not replace that cycle with a generic “economic opportunity” object.» **Boundary (draft):** «`PROOF-SLICE-01` begins after a bounded program/opportunity has been admitted under applicable authority and resource constraints.» Restatement of inherited World/Self observation — mention of inherited L0, не новый ID.

### `AICM-L1-PREF-033` — First bounded active slice selection
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** select Bitget BTC/USDT spot, long-only, Wave-1/Wave-2 reversal, `1H` structural context, `7m` decision observation and one exact shadow decision consumer as `PROOF-SLICE-01`. **Boundary:** this is slice-local and creates no permanent venue/instrument/timeframe or trading-only identity.

### `AICM-L1-PREF-034` — Scope, exclusions and authority/resource/dependency envelope
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** zero real capital, zero live orders, no leverage/margin/short, normalized `1R`, one simulated position, 24-hour Case horizon, 40 replay opportunities and up to 20 live-shadow opportunities or 45 days. Exact source/data rights and external dependencies must be proven. Draft: «the slice is bounded by one venue, instrument, direction, setup, consumer, normalized `1R`, one concurrent simulated position, 24-hour per-opportunity Case horizon, 40 point-in-time replay opportunities and a maximum live-shadow cohort of 20 opportunities or 45 calendar days after the first shadow opportunity.» **Boundary:** «source rights, data rights and external dependencies must be proven. Missing authority or data becomes explicit WAIT, block, External Enabler request or Terminal Closed—not inferred permission.»

### `AICM-L1-PREF-035` — Evidence-driven autonomous progression
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** use replay, observe-only shadow, knowledge-influence canary and bounded active shadow stages with declared evidence gates, rollback and automatic continuation. **Boundary:** stages are not fixed-time ceremony or Owner approval gates. Shadow success grants no live authority. Draft: «progression follows `replay → observe-only shadow → knowledge-influence canary → bounded active shadow`, with declared evidence gates, rollback and automatic continuation. Stages are not fixed-time approval ceremonies.» «no Owner confirmation is required between internal stages when standing authority and resources are already present. Success in shadow cannot silently create live-trading or capital authority.»

### `AICM-L1-PREF-036` — Multidimensional success and P&L-not-truth application
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** control integrity and Knowledge Evolution disposition are independent verdict axes. Economic results remain central evidence but not knowledge truth, sole success or authority-expansion trigger. Draft: «slice success is recorded on at least two independent axes: E2E control integrity and Knowledge Evolution disposition. Economic outcomes, including P&L-equivalent normalized results, are important evidence but not a direct knowledge verdict, authority expansion or sole success definition.» **Boundary:** «`CONTROL_PASS / KNOWLEDGE_REJECTED` is a valid successful architecture result.»

### `AICM-L1-PREF-037` — Self-development as governed economic investment
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** improvement work must justify expected Purpose contribution, resource use, opportunity cost, evidence budget, horizon, stop, rollback and Terminal Closed. It receives no intrinsic priority. Draft: «improvement work is treated as an economic investment under the same Purpose, Portfolio, authority, resource, evidence, opportunity-cost, horizon, stop, rollback and Terminal Closed disciplines as other programs.» **Boundary:** «self-improvement has no permanent priority and cannot remain indefinitely active without expected contribution, evidence budget and disposition.» Guardrail §5: Every self-development program must declare: Purpose linkage; target gap and affected consumers; expected economic/capability contribution; uncertainty and alternatives; resource budget and opportunity cost; evidence budget and observation horizon; bounded initial exposure; stop, rollback, downgrade and retirement conditions; actual-use and outcome evidence; Terminal Closed or successor path. «No program may justify itself solely by “improving AICM.” It must explain what durable value-creation ability changes and how that claim will be tested.»

### `AICM-L1-PREF-038` — Reusable learning lineage and future training readiness
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** preserve reproducible model-neutral lineage for future lawful analysis/evaluation/training consumers. **Boundary:** no dataset membership, data collection, label truth, training, model promotion or deployment authority is created; `AICM-L1-PREF-019` remains active. Draft: «material sources, claims, challenges, interpretations, uses, influence, Decisions, RiskGate outcomes, execution outcomes and separated program outcomes are preserved in reproducible model-neutral lineage so future evaluation or training methods may consume them lawfully.» «reusable lineage is not dataset membership, label truth, collection authority, training authorization, model promotion or deployment authority. `AICM-L1-PREF-019` remains controlling.» Guardrail §9: A record becomes training-eligible only through a separate future lifecycle that evaluates: rights and licensing; privacy and secrets; provenance and integrity; contamination and leakage; label meaning and uncertainty; holdout/evaluation separation; bias and representativeness; retention/deletion obligations; model purpose, authority and promotion criteria. «Actual use in the system, profitable outcome, Consilium agreement or Foundation release does not automatically make data training-eligible.»

### `AICM-L1-PREF-039` — Autonomous continuation without hidden operator activation
- действующая: s14 (первое появление s14)
- текст: **Status:** CONFIRMED. **Decision:** internal release, enrollment, replay/shadow progression, WAIT wake, rollback, restriction, successor, outcome review and Terminal Closed continue autonomously within standing authority. **Boundary:** Owner/Operator appears only for objectively irreducible external acts through a complete request and automatic resume. Draft: «within the slice’s standing authority, candidate admission, review, release, enrollment, replay, shadow progression, WAIT wake, rollback, restriction, successor creation, outcome review and Terminal Closed continuation proceed autonomously.» «Owner/Operator is used only for an objectively irreducible external right/resource/action through a complete minimally scoped External Enabler request with persisted cursor and automatic resume.»

### `AICM-L1-PREF-040` — Orthogonal authoritative product-state vectors
- действующая: s15 (первое появление s15)
- текст: **Decision:** the slice is governed by multiple independent authoritative contours, not one global state machine or one mutable “overall status.” **Boundary:** aggregate readiness, health, truth, success and DecisionTrace are computed views and grant no authority. Register: «use independent authoritative Slice and Opportunity contour states. Aggregate readiness/health/truth/success are non-authoritative views.» SliceVector = `<SliceLifecycle, StageLifecycle, EntryAndRights, KnowledgeEvolutionCycle, ReleaseLifecycle, ConsumerEnrollment, CohortCursor, RecoveryRollback, ExternalDependency, FinalVerdictVector>`. OpportunityVector = `<OpportunityOwnership, SnapshotAndBundle, HypothesisCase, InstancesAndAssessments, CaseCursorAndWAIT, Decision, RiskGate, SimulatedExecution, UseInfluenceComparison, OutcomeSet>`. «No vector member may overwrite another member’s state. Coordination reads typed relations; it does not collapse authorities.» Computed views only: overall readiness/health, current trade status, current truth, overall success, DecisionTrace, stage-transition eligibility. «A view cannot issue a release, Decision, RiskGate verdict, execution request, capital action or constitutional amendment.»

### `AICM-L1-PREF-041` — Durable slice/stage/Case cursor hierarchy
- действующая: s15 (первое появление s15)
- текст: **Decision:** one authoritative logical slice cohort cursor coordinates progression while every Case owns an independent durable cursor. Session, process, model or provider end does not end either lifecycle. Register: «one logical slice cohort cursor plus independent Case cursors preserve exact next wake, deadline, fallback, authority and resume point across interruption or replacement.» Slice cohort cursor содержит: current stage and stage-instance lineage; admitted/completed opportunity counts; total live-shadow count; stage time anchors and deadlines; active Cases; last consistent transition point; unresolved evidence predicates; release and baseline bindings; applicable Authority Envelope; current recovery/rollback state; next autonomous trigger; exact resume target. «Concurrent Cases are allowed. Concurrent authoritative slice progression cursors are not.» Case cursor: current Snapshot/Bundle pair; active Instances and Assessments; exact unresolved question; next wake; 24-hour deadline; pending Decision/RiskGate/execution/outcome obligations; recovery state; successor-transfer target. «A Case cursor cannot extend stage budgets or expand authority.» Persistence: «Session end, component failure, process restart, provider change and model replacement do not close a Slice or Case.» Durable stop preserves `last consistent state + exact pending predicate + next wake + deadline + retry b…

### `AICM-L1-PREF-042` — Entry, source/right and External Enabler contract
- действующая: s15 (первое появление s15)
- текст: **Decision:** entry and continuation require explicit source/right/authority evidence. Owner participation is limited to complete, minimal, verifiable External Enabler requests with expiry, fallback and automatic resume. Register: «entry/continuation requires explicit rights, source, authority and recovery evidence. External Enabler use is objectively irreducible, complete, minimal, verifiable and automatically resumable.» `ENTRY_GATING → R1 ENTRY_CHECK` требует: upstream Durable Program admission; `PROOF-SLICE-01` scope remains exact; replay/shadow-only Authority Envelope; zero-capital and zero-live-order boundaries; source artifacts and source/data rights sufficient for scope; point-in-time 1H and reproducible closed-7m observations lawful and available; Foundation candidate/release lineage; exact shadow consumer semantically identified; separate RiskGate and simulated execution contours; cursor/WAIT/recovery and exact rollback target; outcome reconciliation path; substantive independent challenge; no unresolved hard control failure. «Absence of one predicate is absence of permission.» `REQUEST_READY` must contain: exact external act; proof that internal lawful/physical alternatives are exhausted; Purpose and Program linkage; minimum scope and prohibited privileges; term, expiry and revocation path; prepared steps/documents; objective verification evidence; secret-handling boundary; alternatives;…

### `AICM-L1-PREF-043` — Slice and stage lifecycle law
- действующая: s15 (первое появление s15)
- текст: **Decision:** `R1 → S0 → C1 → S1 → closure` is a bounded evidence-driven lifecycle with explicit intake stop, reconciliation, review and closure states. Time or count ends intake; it does not manufacture a PASS. Register: «bounded R1/S0/C1/S1 stages own entry, intake, reconciliation, review and closure states. Count/time triggers review rather than automatic PASS.» Normal lifecycle: `ADMITTED → ENTRY_GATING → R1 REPLAY → S0 OBSERVE-ONLY SHADOW → C1 KNOWLEDGE-INFLUENCE CANARY → S1 BOUNDED ACTIVE SHADOW → CLOSURE_RECONCILIATION → TERMINAL_CLOSED → NEXT AUTONOMOUS CURSOR`. Exception: recoverable failure → `DEGRADED_RECOVERABLE`; hard control/right/lineage → `ROLLBACK_ACTIVE`; material knowledge correction → current release restricted → successor candidate. Every stage: `PENDING → ENTRY_CHECK → ACTIVE_INTAKE → INTAKE_STOPPED → EVIDENCE_RECONCILING → REVIEW_ACTIVE → CLOSED`. «Count or time stops intake. Already admitted Cases may drain to their declared 24-hour horizon. New opportunities are rejected after `INTAKE_STOPPED`.» R1 intake: exactly 40 eligible non-overlapping opportunities. S0 intake stops at earliest of 5 eligible live-shadow opportunities, 14 calendar days from first S0 opportunity, or hard rollback/restriction. C1 intake stops at earliest of next 5 eligible opportunities, 14 additional calendar days, or hard trigger. S1 intake stops at earliest of 20 total live-shadow opportuniti…

### `AICM-L1-PREF-044` — Opportunity identity, canonical episode ownership and cohort integrity
- действующая: s15 (первое появление s15)
- текст: **Decision:** one market episode has one canonical Case owner. Overlapping observations create successor Snapshots/Assessments within that Case, and every admitted opportunity remains in the cohort regardless of favorable or unfavorable disposition. Register: «one market episode has one canonical Case; overlapping observations create successors inside it. Every admitted opportunity remains in the cohort.» Admission only when: venue/instrument/direction/setup match the slice; exact observation cutoff fixed; 1H structural decline completion and initial reversal materially assessable; 7m interval closed and provenance proven; stage/cohort bound available; no canonical Case already owns the episode; exact Snapshot and paired Bundles can be sealed; event is not a duplicate market episode. One Case owns an episode when all are materially the same: BTC/USDT instrument; 1H decline-completion structural anchor; proposed Wave-1 start/Wave-2 correction; overlapping 24-hour opportunity horizon; Read Purpose. «New 7m observations in the same episode create successor Snapshot/Bundle and new Assessments inside the same Case. Alternative wave counts are separate HypothesisInstances in that Case.» If duplicate status is `UNKNOWN`, a second Case is not created. Anti-cherry-picking: admitted opportunity consumes one cohort slot whether it ends in positive Decision, `NO_TRADE`, RiskGate rejection, no fill, WAIT expiry, control failure, disputed o…

### `AICM-L1-PREF-045` — Knowledge Evolution, release and enrollment separation
- действующая: s15 (первое появление s15)
- текст: **Decision:** Knowledge Candidate, Consilium assessment, Domain recommendation, Knowledge Evolution disposition, scoped release and consumer enrollment are separate states and authorities. Register: «Candidate, Consilium, Domain assessment, Knowledge Evolution disposition, release and enrollment remain independent lifecycles and authorities.» Sequence: `Knowledge Candidate → Task/Domain Consilium → independent strongest challenge → Domain assessment/recommendation → separate Knowledge Evolution disposition → scoped release → monitored enrollment/use/outcomes → stage review → final Knowledge Evolution disposition`. «Domain assessment is not release. Release is not Decision, RiskGate or execution permission.» Initial dispositions: `SCOPED_RELEASE_REPLAY_ONLY`, `SCOPED_RELEASE_REPLAY_SHADOW`, `WAIT`, `REJECT`, `CORRECT`, `SUCCESSOR_REQUIRED`. «A release defines a maximum exposure ceiling. Stage gates still govern actual enrollment.» Stage-specific enrollment: **R1** candidate replay branch authoritative for candidate evaluation; **S0** baseline is authoritative reference, candidate parallel and strictly non-influencing; **C1** candidate canary authoritative for exact enrolled shadow consumer; **S1** candidate active-shadow branch authoritative, baseline comparison-only. «Only the authoritative branch can proceed to RiskGate and simulated execution. The comparison branch…

### `AICM-L1-PREF-046` — Case, Instance, Assessment and four-class WAIT semantics
- действующая: s15 (первое появление s15)
- текст: **Decision:** Case reasoning preserves plural Instances and separate Assessments. Case epistemic WAIT, stage evidence WAIT, RiskGate input WAIT and external dependency block are not interchangeable. A Case cannot remain WAIT after its 24-hour horizon. Register: «Case epistemic WAIT, stage evidence WAIT, RiskGate input WAIT and external dependency block remain distinct. A Case cannot remain WAIT beyond 24 hours.» Case lifecycle: `ELIGIBILITY_CHECK → ACTIVE_REASONING → WAITING_FOR_EVIDENCE ↘ wake → ACTIVE_REASONING → READY_FOR_DECISION → DOWNSTREAM_MONITORING → OUTCOME_RECONCILING → TERMINAL_CLOSED`. «Material question/context change uses `SUCCESSOR_TRANSFER`; it does not rewrite the Case.» Required competing hypothesis space at minimum: `H1` completed decline plus valid Wave-1/Wave-2 reversal; `H2` local correction inside an extended decline; `H3` higher-degree correction makes the long thesis premature; `H4` liquidity-driven range/expansion makes wave interpretation unreliable. «The leading hypothesis is a revisable Assessment, not truth.» Four WAIT classes: **Case epistemic WAIT** owns one unresolved market/evidence question, differentiating observation, trigger, next wake, 24-hour deadline, fallback and Case cursor. **Stage evidence WAIT** covers insufficient cohort evidence or event frequency; cannot extend count/time bounds; at the bound becomes an inconclusive stage verdict, not eternal WAIT. **RiskGate input WAIT** belongs…

### `AICM-L1-PREF-047` — Decision, RiskGate and simulated execution predicates
- действующая: s15 (первое появление s15)
- текст: **Decision:** a positive shadow Decision, a separate RiskGate pass and separate simulated execution eligibility are conjunctive and immutable. `NO_TRADE` never creates execution eligibility. Register: «positive Decision, separate RiskGate pass and separate simulated-execution eligibility are conjunctive. `NO_TRADE` never creates execution eligibility.» `SHADOW_LONG_PLAN_ISSUED` requires: Case within its horizon; applicable Snapshot/Bundle readiness `FIT`; required competing hypotheses and strongest challenge considered; no unresolved material unknown that prohibits positive action; current release/enrollment permits the authoritative branch; entry, invalidation, target/horizon and uncertainty declared; no active restriction or incompatible degradation; exact evidence used, challenged and not used preserved. `NO_TRADE_ISSUED` requires an exact opportunity/horizon and reasoned non-action. «It does not call RiskGate or execution.» RiskGate accepts only an immutable positive Decision and independently checks: shadow-only authority; normalized maximum 1R; stop/invalidation coherence; one-position limit; duplicate exposure; data freshness; fee/slippage/liquidity assumptions; release applicability; constraints and obligations. Terminal verdict: `PASS_SHADOW`, `REJECT_SHADOW` or bounded `WAIT_FOR_RISK_INPUT`. «RiskGate cannot rewrite entry, target, hypothesis or Decision class…

### `AICM-L1-PREF-048` — Same-Snapshot baseline/candidate influence protocol
- действующая: s15 (первое появление s15)
- текст: **Decision:** baseline and candidate branches use the same immutable Snapshot and matched non-candidate inputs, remain isolated until sealing, and receive explicit use/influence dispositions including no-use, non-influence, dispute and non-comparability. Register: «matched immutable context, independent branch sealing and explicit no-use/non-influence/dispute/non-comparability are mandatory.» Isolation: receive one Snapshot; share materially identical non-candidate inputs; reason independently; do not see one another’s output before sealing; preserve separate immutable Bundles and Decisions. Failure of isolation or equivalence produces `NOT_COMPARABLE`. Use classification: `publication → availability → retrieval → interpretation → consideration → declared role → actual use/non-use → material influence/non-influence/dispute`. «No-use and non-influence are complete negative evidence states, not missing records.» Material influence: causal change to at least one of hypotheses considered, strongest alternative, WAIT trigger, Decision class, `NO_TRADE` reason, entry, invalidation, target/horizon, risk assumptions. «Textual explanation changes without material decision change do not count.» Candidate knowledge may materially influence a `NO_TRADE`; influence does not require a trade. `INFLUENCE_DISPUTED` triggers independent review; until resolution the opportunity remains in the cohort and influence is not credited to the C1 gate. **S0…

### `AICM-L1-PREF-049` — Evidence defect and stage transition-gate law
- действующая: s15 (первое появление s15)
- текст: **Decision:** MISSING, STALE, CONFLICTING, UNKNOWN and DISPUTED evidence have role-specific effects. Advancement requires a conjunctive protected-boundary, control, continuity, rights, evidence, knowledge-disposition, resource and reconciliation gate. Register: «evidence defects have predicate-specific effects. Advancement requires non-substitutable protected-boundary, control, continuity, rights, evidence, knowledge, resource and reconciliation predicates.» Material defect in source rights, authority, point-in-time integrity or immutable lineage is a hard block. Material defect for positive market Decision creates Case WAIT or exact `NO_TRADE`. Material defect for RiskGate creates `WAIT_FOR_RISK_INPUT` or `REJECT_SHADOW`. Material defect in comparability creates `NOT_COMPARABLE`. Material defect in outcome creates `DISPUTED` or `TERMINAL_UNAVAILABLE`; no substitute value is invented. «Evidence arriving after the original cutoff creates successor Snapshot/Bundle/Assessment and cannot repair the old pair in place.» Universal advancement conjunction: `ProtectedBoundaryIntegrity = PASS ∧ ControlLineageIntegrity = PASS ∧ ContinuityRecoverability permits progression ∧ SourceAndRights = VALID_FOR_SCOPE ∧ stage-specific evidence gate is satisfied ∧ Knowledge Evolution disposition permits next exposure ∧ resource/authority envelope remains valid ∧ no unresolved hard rollback exists ∧ every admitted Case is reconciled or successor-transf…

### `AICM-L1-PREF-050` — Restriction, rollback, recovery and successor effects
- действующая: s15 (первое появление s15)
- текст: **Decision:** restriction is prospective, history remains immutable, open Cases and simulated positions receive exact dispositions, recovery resumes only from a proven consistent cursor, and Case/release/scope successors remain distinct. Register: «restriction is prospective; history stays immutable; recovery resumes from proven state; Case, release and scope successors remain distinct.» On `RESTRICT`: release becomes `RESTRICTED`; enrollment `BASELINE_ONLY_AFTER_RESTRICTION`; new candidate-influenced positive Decisions prohibited; intake may stop; prior Decisions/executions/outcomes remain immutable; affected consumers must acknowledge; unresolved acknowledgement blocks Terminal Closed. Open Case: no Decision yet — candidate branch ends, Case may continue baseline-only if lawful and FIT; positive Decision before RiskGate — execution eligibility removed; RiskGate pass before execution — request cancelled, historical Decision remains; simulated position already open — no new entry/scale-in/discretionary candidate-driven change; only predeclared observation/stop/target/horizon, controlled simulated close or `ABORTED_CONTROL`. Hard rollback includes unauthorized external effect; live order or capital effect; invalid/revoked source right; look-ahead; material data corruption; lineage break or history rewrite; missing substantive independent challenge; proposer self-release; release acting as Decision/RiskGate/execution…

### `AICM-L1-PREF-051` — Multidimensional stage and Slice verdict vectors
- действующая: s15 (первое появление s15)
- текст: **Decision:** protected-boundary integrity, control/lineage integrity, continuity/recoverability, economic outcome, knowledge disposition, capability/learning contribution and resource/opportunity-cost outcome remain separate. No global success scalar is authoritative. Register: «protected-boundary/control, continuity, economic, knowledge, capability/learning and resource outcomes remain separate. No global scalar is authoritative.» Axes and values: Protected-boundary integrity `PASS|FAIL|INCONCLUSIVE`; Control and lineage `CONTROL_PASS|CONTROL_FAIL|CONTROL_INCONCLUSIVE`; Continuity/recoverability `PASS|PASS_WITH_RECOVERY|FAIL|INCONCLUSIVE`; Economic outcome `FAVORABLE|UNFAVORABLE|MIXED|INCONCLUSIVE|TERMINAL_UNAVAILABLE`; Knowledge disposition `RETAINED|SCOPED|CORRECTED|RESTRICTED|RETIRED|REJECTED|INSUFFICIENT_EVIDENCE_TERMINAL`; Capability/learning `PROVEN_BOUNDED_CONTRIBUTION|PARTIAL|NOT_PROVEN|NEGATIVE|INCONCLUSIVE`; Resource/opportunity-cost `JUSTIFIED|NOT_JUSTIFIED|MIXED|INCONCLUSIVE`. «`PROVEN_BOUNDED_CONTRIBUTION` is not L2 capability promotion.» «A valid terminal vector may contain `CONTROL_PASS`, unfavorable economics and knowledge `REJECTED`.» «A favorable economic outcome with `CONTROL_FAIL` is not success and cannot justify promotion.» Opportunity outcomes remain separated: scenario, plan, risk, execution, operational, economic, knowledge-use. Stage close = Stage Verdict Vector + Evidence Sufficiency Disposition + Knowledge Evolution…

### `AICM-L1-PREF-052` — Bounded Terminal Closed and next autonomous cursor
- действующая: s15 (первое появление s15)
- текст: **Decision:** Slice closure requires complete reconciliation of intake, Cases, WAIT, Decisions, RiskGate, execution, use/influence, outcomes, release, rollback/recovery, external dependencies and independent review, followed by one persisted next autonomous cursor. Register: «closure requires full reconciliation and exact persisted continuation; Slice closure is not global AICM DONE.» Twenty-one required predicates: (1) intake stopped; (2) every stage instance closed; (3) every admitted Case terminal or explicitly successor-transferred; (4) orphan WAIT count zero; (5) Decisions immutable and reconciled; (6) RiskGate states reconciled; (7) active simulated positions zero; (8) execution/non-execution reasons reconciled; (9) use/influence states terminal; (10) disputes resolved or bounded terminal-inconclusive; (11) outcome horizons completed or `TERMINAL_UNAVAILABLE`; (12) final Task/Domain Consilium review complete; (13) substantive independent challenge preserved; (14) final Knowledge Evolution disposition issued; (15) release state settled; (16) consumer restriction/successor acknowledgements reconciled; (17) rollback/recovery states terminal; (18) external requests satisfied, refused, expired or terminal-impossible; (19) final multidimensional verdict vector issued; (20) resource/opportunity-cost outcome returned; (21) exact next autonomous cursor persisted. Terminal reason separately recorded (`BOUNDED_COHORT_COMPLETE|KNOWLEDGE_REJECTED_OR…

### `AICM-L1-PREF-053` — Autonomous continuation and authority non-expansion
- действующая: s15 (первое появление s15)
- текст: **Decision:** all internal stages, restriction, rollback, recovery, successor, review and closure continue without hidden Owner activation. Stage success, P&L, Consilium agreement or release creates no live, capital, credential or constitutional authority. Register: «no hidden Owner activation exists. Stage success, P&L, Consilium agreement or release creates no live/capital/credential/training/constitutional authority.» Internal path contains no Owner approval state: `entry gate → candidate and Consilium → release → enrollment → replay → observe-only shadow → influence canary → bounded active shadow → correction/restriction/retirement where required → final review → Terminal Closed → next autonomous cursor`. «Owner does not choose hypotheses, evidence interpretation, baseline, Decision, RiskGate, canary activation, stage progression, rollback, recovery, knowledge correction, successor, closure or next internal cursor.» «No stage result creates live-trading, capital, credential, external legal, constitutional or training authority.»

### `AICM-L1-PREF-054` — World/Self model, belief revision and identity continuity application
- действующая: s15 (первое появление s15)
- текст: **Decision:** slice evidence updates both World-State and Self-State through successor lineage. Repeated expectation/reality divergence creates governed review; realization replacement cannot erase Purpose, authority, knowledge history, capability proof or cursor continuity. Register: «World-State and Self-State updates remain distinct; divergence creates governed successor review; realization replacement must preserve Purpose, authority, obligations, knowledge/capability history and cursors.» Two streams: World-State evidence about market structure, opportunity conditions, counterparties and outcomes; Self-State evidence about knowledge quality, use/influence, capability reliability, control, latency, cost, recovery and dependency. «A single outcome does not rewrite the model. Material or repeated expectation/reality divergence creates a governed candidate for challenge, correction or successor. Old predictions and assessments remain immutable.» «Implementation, provider, model or infrastructure replacement preserves Purpose, authority provenance, obligations, knowledge history, capability evidence and cursor continuity. Otherwise it is identity discontinuity, not evolution.»

### `AICM-L1-PREF-055` — Consequence-proportionate autonomous self-development and viability
- действующая: s15 (первое появление s15)
- текст: **Decision:** uncertainty does not automatically stop action. Exposure is proportionate to the consequence of error, reversibility, recoverability, observability, rights, systemic impact and opportunity cost. Self-development remains a multi-horizon economic investment that must justify and periodically re-justify itself across multiple forms of capital and viability. Register: «uncertainty does not automatically block action. Exposure is governed by consequence, reversibility, recoverability, observability, rights, systemic impact and opportunity cost across multiple horizons/capitals. Self-development must periodically justify itself.» «Uncertainty is normal at cold start and does not justify paralysis. The system uses lower-consequence paths—replay, shadow, canary, bounded exposure and reversible experiments—to acquire evidence.» Before material change AICM evaluates at least: economic magnitude and tail effect; reversibility and time-to-reverse; recovery probability and restoration cost; authority, rights and protected-boundary effect; lineage/knowledge corruption risk; continuity and correlated-system effect; third-party and external consequence; strategic lock-in and dependency; observability and detectability; uncertainty and competing explanations; resource and opportunity cost; impact across short, medium and long horizons. «The required axes are stable architecture. Exact method, classes and weights are evolvable through governed successor evidence.» «Self-development competes in the Evolution Portfolio, must preserve multiple forms of…


### D.7 `AICM-L2-PREF-001`…`146` — Level 2 durable substrate (memory, capability, program, change)

### `AICM-L2-PREF-001` — AICM-owned provider-independent semantic memory
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** System memory belongs to AICM rather than to any model, provider, session, agent, database or other realization layer. It must preserve system identity and durable work across replacement of those layers. **Boundary:** A realization component may host or process memory, but it is never the constitutional owner or sole canonical carrier. *Указатель:* L2-B1 (System Memory); object equation и class theorems разнесены по L2-PREF-002…033.

### `AICM-L2-PREF-002` — Typed memory classes with non-inheriting authority boundaries
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Use eight semantic source-memory classes: Constitutional and Identity; Constraint, Authority and Obligation; World-State Evidence; Knowledge, Assessment and Dissent; Decision, Use and Consequence; Program and Continuity; Self-State, Capability-Evidence and Resource; Integrity, Preservation and Recovery. **Boundary:** Classification does not grant cross-class authority. Evidence memory does not become Decision authority; compaction does not become constitutional authority. M1 Constitutional and Identity — Purpose, Beneficiary, origin authority, formal block closures, identity-successor. M2 Constraint, Authority and Obligation — Reality Conditions, Constraints, Standing Obligations, Authority Envelopes, External Enabler requests, legal holds. M3 World-State Evidence — source artifacts, SourceAssertions, Snapshots, external outcomes; «A historical record can remain exact while becoming stale for a new Read Purpose.» M4 Knowledge, Assessment and Dissent — claims, hypotheses, Consilium, Domain assessment, Knowledge Evolution disposition. M5 Decision, Use and Consequence — immutable Bundle→Case→Instance→Assessment→use/influence→Decision/`NO_TRADE`→RiskGate→execution→outcomes; «A summary or P&L statement cannot replace this chain.» M6 Program and Continuity — Programs, stages, Cases, WAIT, cursors, Terminal Closed. M7 Self-State, Capability-Evidence and Resource — capability evidence, degradation, resource use; «Capability identity and proof semantics remain deferred to `L2-B2`.» M8 Integrity, Preservation and Recovery — integrity verdicts, preservation-copy evidence, corruption incidents, deletion receipts.

### `AICM-L2-PREF-003` — Durable Memory Lineage and immutable Memory Record identity
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** A Memory Lineage is the durable continuity identity of one semantic subject and scope. A Memory Record is an exact immutable event, assertion, artifact, assessment or disposition edition inside that lineage. **Boundary:** Material change of subject, scope, proposition or authority origin creates a successor lineage or successor record; no authoritative in-place rewrite is permitted. Memory Lineage: «A durable semantic continuity identity defined by memory class, subject or proposition, material scope, authority origin, applicability horizon and continuity relation. Material change creates a successor lineage.» Memory Record: «An exact immutable record or edition preserving event time, record time, content, provenance, asserting or transition authority, evidence references, uncertainty, applicability, rights, sensitivity, retention/hold state, predecessor/successor relations, known uses and integrity state.» «Existing domain identities remain intact. A Bundle remains a Bundle; a Case remains a Case; a Decision remains a Decision.»

### `AICM-L2-PREF-004` — Sealed authoritative Current-State Editions
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Current state is represented by sealed, immutable, scope-bound Current-State Editions derived from exact records and made current only by provenance-matched disposition. **Boundary:** Operationally changing state is realized through successor editions. A mutable `latest` object or disposable cache is not authoritative current state. Normalization: «Authoritative change occurs through sealed successor Current-State Editions. Ephemeral context and caches may be mutable, but they are non-authoritative and reconstructable.» Allowed current dispositions: `CURRENT_FOR_SCOPE`, `CURRENT_WITH_LIMITATION`, `CONFLICTED_NO_SINGLE_CURRENT`, `STALE_REVALIDATION_REQUIRED`, `RESTRICTED`, `SUPERSEDED`, `TERMINAL_UNAVAILABLE`. «It receives current status only through provenance-matched disposition and is replaced by a successor edition rather than updated in place.»

### `AICM-L2-PREF-005` — Distinct Compaction Product, Retrieval View, Context Assembly and Cache identities
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Compaction Product, Retrieval View, Context Assembly and Cache are separate derived objects with separate purposes, cuts and authority limits. **Boundary:** None of them silently replaces Memory Records, Current-State Editions or domain identities such as Bundle, Case, Decision, RiskGate or Outcome. Compaction Product: sealed derived artifact for one declared purpose and consumer class; identity includes source universe, exact source cut, compaction-policy edition, coverage, omissions, loss, uncertainty, freshness, dissent preservation, rights and secret disposition. Retrieval View: purpose-bound selection for one consumer, Read Purpose, consequence class and evidence cut; records selected/excluded/withheld/unavailable/stale items and a fit-for-purpose verdict. Context Assembly: consumer-specific representation from one Retrieval View; «may be reduced for a model context limit but gains no authority». Cache: «A disposable convenience projection or index. It is reconstructable and cannot be the only carrier of current authority, legal hold, secret classification, WAIT or cursor.»

### `AICM-L2-PREF-006` — Separated write, assessment, disposition, compaction, retention, retrieval, assembly and action authorities
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** There is no universal memory writer or memory sovereign. Record admission, domain assessment, current-state disposition, compaction, retention/deletion, secret disclosure, retrieval, context assembly and Decision/RiskGate/execution remain separately authorized. **Boundary:** A component may exercise several roles only where the applicable authority explicitly permits it; one role never inherits another by implementation convenience. Separate contours at least: record admission/write; lineage identity; assessment; current-state disposition; compaction; retention/deletion/hold; secret/access; retrieval; context assembly; integrity/recovery; Decision/RiskGate/execution. «No contour inherits another merely because one implementation component may host several functions.»

### `AICM-L2-PREF-007` — Record, interpretation, hypothesis, Decision and unknown remain distinct
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Memory preserves what was observed or asserted, how it was interpreted, which hypotheses competed, what Decision was made and which unknowns, gaps and falsifiers remained. **Boundary:** A recorded assertion is not automatically truth; an interpretation is not a fact; a Decision is not a knowledge verdict; missing evidence is not evidence of absence. «The phrase “canonical or primary memory is the source of truth” means that exact admitted records and their lineage are the authoritative evidence of what was recorded, asserted, assessed, decided and used. It does **not** mean that every source assertion is true. Domain truth, applicability, uncertainty and current disposition remain separately assessed.»

### `AICM-L2-PREF-008` — Protected Memory Core
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Purpose, Beneficiary relation, authority provenance, constraints, obligations, confirmed and superseded decisions, immutable Bundle/Case/Instance/Assessment/use/Decision/RiskGate/execution/outcome lineage, dissent, active WAIT/cursors, recovery state and bounded closure evidence form a Protected Memory Core. **Boundary:** No lossy compaction, convenience deletion or model replacement may become the sole surviving carrier of this core. Never compacted away, silently orphaned or replaced by derived summaries: (1) Purpose, Beneficiary and constitutional identity lineage; (2) origin and provenance of authority, constraints and standing obligations; (3) confirmed, rejected, superseded and retired architecture decisions; (4) exact current rights, holds, restrictions and authority dispositions; (5) source evidence required for reproduction of material Decisions and obligations; (6) Snapshot, Bundle, Case, Instance and Assessment lineage; (7) Decision/`NO_TRADE`, RiskGate, execution/non-execution and separated outcomes; (8) actual use, no-use, influence, non-influence and disputes; (9) substantive challenge, minority dissent, alternatives and counterexamples; (10) Domain assessment and separate Knowledge Evolution disposition; (11) active Program, Case, WAIT, next wake and cursor continuity; (12) correction, restriction, rollback, recovery, retirement and successor history; (13) legal-hold, deletion and secret-access dispositions; (14) integrity, preservation-copy and replacement-continuity receipts; (15) bounded Terminal Closed evidence and exact next autonomous cursor. «This is a prohibition on convenience loss, not a…

### `AICM-L2-PREF-009` — Declared source universe and exact source cut before compaction
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Every material Compaction Product declares the expected source universe and seals the exact source cut before synthesis. **Boundary:** Coverage cannot be declared complete merely because the compactor did not know that relevant sources existed. Before synthesis a material compaction work item declares: Read or continuity purpose; intended consumers and consequence class; relevant memory classes, lineages and horizons; active Programs, Cases, WAIT and obligations within impact scope; required current-state editions; required dissent, alternatives, negative evidence and counterexamples; expected rights, holds and secret restrictions; sources that may be unavailable or legally withheld; source-cut time and evidence-cut identity. «If the universe cannot be bounded sufficiently, the maximum disposition is `ORIENTATION_ONLY`.»

### `AICM-L2-PREF-010` — Multidimensional coverage and omission declarations
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Coverage is declared separately for memory class, lineage, time/event horizon, authority provenance, active work, dissent, outcomes, obligations and current state; every relevant source receives an explicit inclusion, reference, exclusion, withholding, deletion, unavailability, corruption or unknown disposition. **Boundary:** One scalar coverage percentage is non-authoritative. Every relevant source receives one disposition: `INCLUDED`, `EXACTLY_REFERENCED`, `OUT_OF_SCOPE_WITH_REASON`, `WITHHELD_BY_RIGHT_OR_SECRET`, `LAWFULLY_DELETED`, `UNAVAILABLE`, `CORRUPT_OR_SUSPECT`, `UNKNOWN_EXISTENCE_OR_COMPLETENESS`. Coverage declared independently across memory class, lineage, time/event horizon, authority provenance, active work, dissent, outcomes, obligations and current state.

### `AICM-L2-PREF-011` — Explicit information-loss, uncertainty and freshness declarations
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Compaction declares detail, granularity, precision, temporal, provenance, relationship, applicability, uncertainty, dissent, counterexample, negative-evidence, obligation and cursor loss, plus evidence cut, applicability horizon, expiry and revalidation triggers. **Boundary:** Compaction must not convert UNKNOWN to KNOWN, CONFLICTING to RESOLVED, no evidence to evidence of absence, no-use to missing-use, or no-influence to missing-outcome. Loss declared independently for detail, granularity, numeric precision, temporal order, provenance resolution, relationship/causal structure, applicability, uncertainty, alternatives, dissent, counterexamples, negative evidence, obligations and cursor continuity. Freshness declares source/evidence cut, newest and oldest relevant evidence, known successors, applicability horizon, expiry, staleness triggers and next revalidation. «For Protected Memory Core elements, acceptable continuity loss is `NO_LOSS` or an exact mandatory escalation reference.»

### `AICM-L2-PREF-012` — Read-purpose and consequence-bound fit dispositions
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Every Compaction Product receives a scoped fit disposition such as FIT_EXACT, FIT_WITH_DECLARED_LOSS, ORIENTATION_ONLY, STALE_REVALIDATION_REQUIRED, RESTRICTED_USE, NOT_FIT, REJECTED or SUCCESSOR_REQUIRED. **Boundary:** Material constitutional, authority, legal, continuity, Decision, RiskGate, execution, deletion, secret-disclosure or identity-replacement work must escalate from compaction to exact authoritative records and current dispositions. Fit dispositions: `FIT_EXACT`, `FIT_WITH_DECLARED_LOSS`, `ORIENTATION_ONLY`, `STALE_REVALIDATION_REQUIRED`, `RESTRICTED_USE`, `NOT_FIT`, `REJECTED`, `SUCCESSOR_REQUIRED`. «A product that hides material dissent cannot be `FIT_EXACT`.» Material constitutional/authority/legal/continuity/Decision/RiskGate/execution/deletion/secret-disclosure/identity-replacement work must escalate from compaction to exact authoritative records.

### `AICM-L2-PREF-013` — Contradiction, dissent, alternatives and negative evidence preservation
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Compaction preserves the identity, provenance, supporting and attacking evidence, strongest challenge, uncertainty, unresolved questions and current disposition of materially competing positions. **Boundary:** Consensus or majority does not erase minority dissent; P&L does not adjudicate epistemic contradiction; rejected alternatives remain available with revival conditions. «Material conflict is never averaged into a convenient synthetic claim.» If all detail cannot fit, the Compaction Product must preserve at minimum: existence and materiality of the conflict; scope of omitted detail; exact identities and retrieval path; consequence of relying on the compact view; conditions requiring escalation.

### `AICM-L2-PREF-014` — Correction, supersession, restriction, retirement, revival, successor, redaction and deletion are non-interchangeable
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Each lifecycle action has a distinct prospective effect and immutable lineage. Correction creates a new record; supersession changes current scope; restriction narrows permitted use; retirement ends normal new use; revival requires new evidence and disposition; successor preserves continuity across material change; redaction creates a restricted representation; deletion removes payload under separate authority. **Boundary:** Past use, influence and outcomes are never retroactively rewritten. «Correction creates a new record linked to the predecessor and identifies affected current editions, products, consumers, uses, Decisions and active Programs. Supersession changes what is current for a scope. Restriction prospectively narrows use or access. Retirement ends ordinary new use. Revival requires new evidence and a new disposition. Successor creates new identity where proposition, scope, authority or purpose materially changes. Redaction creates a constrained representation. Deletion is a separate lawful removal.» After material use: `correction record → predecessor remains immutable → successor Current-State Edition → affected-product identification → retrieval/context restriction → active Case/Program re-evaluation or typed WAIT → consumer acknowledgement → rollback, recovery or successor where required`. «No historical Decision or outcome is rewritten to make the past appear cleaner.»

### `AICM-L2-PREF-015` — Retention and ordinary forgetting as governed semantic lifecycle
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Normal forgetting uses active, working, dormant, archived, restricted, retired and revival-eligible semantic states chosen by value, consequence, recovery cost and obligations rather than by age alone. **Boundary:** Ordinary memory management does not destroy knowledge. Physical deletion is exceptional, separately authorized and never disguised as compaction, archival or retirement. Normalization: «The phrase “nothing is deleted” rejects convenience deletion and destructive ordinary forgetting. Normal lifecycle uses dormant, archived, restricted, retired and revival-eligible states.» «Retention derives from authority provenance, law/contract, active obligations, audit and outcome horizon, Program/Case dependencies, recovery needs, rights and sensitivity.» «Movement among them is autonomous inside standing authority and is recorded as lineage.»

### `AICM-L2-PREF-016` — Legal hold and lawful deletion reconciliation
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Legal hold blocks ordinary deletion and destructive transformation within scope without granting broader disclosure. Lawful deletion requires authority, no applicable hold, affected-program reconciliation, successor/restriction where needed, recovery consequence and a lawful deletion receipt or an explicitly declared unrecoverable legal gap. **Boundary:** Conflicting legal obligations are recorded and bounded; the system does not invent legal authority. «Legal hold blocks ordinary deletion and destructive transformation in scope but does not authorize broader access. Hold release or expiry is a separate disposition.» «Lawful deletion requires proof of valid authority, no applicable hold, affected-work reconciliation, knowledge/authority impact assessment, required successor/restriction, recovery consequence, consumer notification and a deletion receipt. Where law forbids even receipt metadata, AICM declares an exact lawful unrecoverable gap.»

### `AICM-L2-PREF-017` — Secret payload, safe reference and disclosure authority separation
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Secret payload, non-secret obligation/reference memory, access authorization and declassification are separate. Derived products inherit the strictest effective sensitivity of their sources unless an authorized successor disposition proves otherwise. **Boundary:** Secret content is excluded from broad compactions and future learning use by default; model/provider replacement does not transfer access automatically. «Secret payload, safe reference and disclosure authority remain separate. Compaction preserves the existence of a withheld obligation without disclosing secret payload. Derived products inherit strict sensitivity unless formally declassified. Model/provider replacement never implies secret transfer.»

### `AICM-L2-PREF-018` — World-State and Self-State memory remain distinct
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** World-State memory records external conditions, events, rights, opportunities, counterparties and outcomes. Self-State memory records AICM knowledge quality, capability evidence, authority, dependencies, resource state, continuity, degradation and recovery. **Boundary:** One event may update both streams, but neither stream substitutes for the other and neither is collapsed into one global truth or health score. «World-State answers what happened or is asserted outside AICM. Self-State answers what AICM currently knows, can prove, is authorized to do, depends upon, costs, can recover and must continue.» One outcome produces: `World-State update: what happened externally` / `Self-State update: what the event demonstrates about knowledge, capability evidence, control, cost, dependency and recovery`. «A profitable outcome does not make a hypothesis true; a model defect does not make an external observation false.»

### `AICM-L2-PREF-019` — Protected Operational Continuity Core
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Every active Durable Program and Case preserves Purpose and Program bindings, exact state vectors, last proven transition, Snapshot/Bundle bindings, pending predicate, WAIT class, next wake, deadlines, retry budget, fallback, authority, obligations, rights, rollback, recovery, successor target, resource state and exact resume cursor. **Boundary:** No summary or session transcript may be the only carrier of active continuity. Operational Continuity Core contains: Purpose and Program bindings; current lifecycle/state vectors; last proven consistent transition; active slice/stage/Case identity; exact Snapshot and Bundle bindings; candidate/release/enrollment state; pending predicate and WAIT class; next wake and trigger; deadline and retry budget; fallback and applicable authority; constraints, obligations, rights and source state; open Decision/RiskGate/execution/outcome state; rollback target and recovery state; External Enabler request if any; successor target; resource/opportunity-cost state; exact resume cursor.

### `AICM-L2-PREF-020` — Lossless-for-continuity Continuation Capsule and automatic resume
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** A Continuation Capsule is a purpose-bound Compaction Product that references exact authoritative records and declares NO_LOSS for the Operational Continuity Core. Interruption or replacement triggers reconciliation and automatic resume from the exact cursor. **Boundary:** The capsule does not extend deadlines, reset budgets, grant authority or replace full history. «A Continuation Capsule seals this state with `NO_LOSS` for continuity and exact references to authoritative records. Session end, process failure, provider replacement or model replacement triggers continuity reconciliation and automatic resume. Clocks, evidence bounds and authority do not reset.»

### `AICM-L2-PREF-021` — Write, retrieval, context assembly, actual use, influence and Decision lineage separation
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** The normal path remains record admission → assessment → current disposition → optional compaction → Retrieval View → Context Assembly → consumer reasoning → separately authorized Decision/RiskGate/execution → use/influence/outcome records. **Boundary:** Publication is not retrieval, retrieval is not use, use is not influence, and context assembly grants no action authority. Normal path: `external event or internal transition → exact immutable Memory Record → class-specific Assessment → provenance-matched Disposition → sealed Current-State Edition → optional Compaction Product → purpose-bound Retrieval View → consumer-specific Context Assembly → consumer reasoning → separately authorized Decision/RiskGate/execution → use/influence/outcome records → correction/successor/current-state update`. Forbidden shortcuts: summary → truth, retrieval → Decision, context assembly → authority, compaction → deletion, publication → actual use, use → influence, favorable outcome → knowledge truth, model confidence → World-State fact.

### `AICM-L2-PREF-022` — Shared event-based system memory with contribution provenance
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Memory is shared AICM capital rather than private agent memory. Multiple authorized contributors and consumers may hold competing views while exact contribution provenance, responsibility and consequence lineage remain visible. **Boundary:** This is a semantic rule for future realization, not a design of agents, services or event infrastructure. «Memory belongs to AICM as a whole. Future agents, services, models and humans may contribute only within typed authority and with exact provenance. Competing positions can coexist until the authorized process resolves or limits them.» «This document does not choose an agent architecture, communication protocol or event infrastructure.»

### `AICM-L2-PREF-023` — Autonomous memory lifecycle governance
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Inside standing authority AICM autonomously classifies, admits, assesses, compacts, revalidates, restricts, archives, revives, successor-transfers and reconciles memory, and initiates review when it detects contradiction, staleness, duplication, provenance gaps or continuity risk. **Boundary:** Memory governance initiates the appropriate process but does not self-grant truth, constitutional amendment, Decision, RiskGate or execution authority. «Memory governance may detect contradiction, staleness, duplication, missing provenance, integrity defects and unclosed continuity. Detection initiates the appropriate assessment, Consilium, Knowledge Evolution, authority or recovery process; it does not grant truth or action authority to the detector.» «AICM autonomously governs classification, attention, compaction, revalidation, restriction, archival, retirement, revival and successor transfer within standing authority. Operator does not manually move data among levels.» «Every material lifecycle action itself becomes memory, including why it occurred, what was omitted, affected consumers, rollback/recovery and next review.»

### `AICM-L2-PREF-024` — Goal-, consequence-, value- and recovery-driven memory attention
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Memory attention and lifecycle are governed by Purpose contribution, active obligations, consequence, actual use and influence, evidence value, uncertainty, restoration cost, resource cost and opportunity cost across operational, program and strategic horizons. **Boundary:** Fixed age-only migration and unbounded accumulation are rejected; these horizons are semantic attention states, not physical storage topology. «Lifecycle decisions are driven by Purpose contribution, consequence, use/influence, uncertainty, active obligations, evidence value, resource cost, opportunity cost, restoration cost and continuity risk across operational, program and strategic horizons.» «Age and access frequency may be evidence, but no fixed time rule is constitutionally sufficient. A rarely used constitutional record can be more protected than a frequently used cache.»

### `AICM-L2-PREF-025` — Governed future learning reuse without training authority
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Canonical memory may produce purpose-bound learning-data candidate views with exact provenance, rights, dissent, exclusions, uncertainty and outcome linkage. Canonical memory, a dataset, model weights and a trained artifact remain distinct. **Boundary:** Eligibility creates no current collection, labeling, training, promotion or deployment authority, and trained artifacts remain derived rather than sources of truth. «Memory is designed for lawful future reuse without making canonical memory a training dataset.» A future learning-data candidate view must preserve exact provenance, licensing/rights, purpose, inclusion and exclusion logic, dissent, counterexamples, uncertainty, consumer/outcome linkage, legal hold, secret boundary and non-authorizing eligibility state. «No current training, labeling, model promotion, deployment or data-acquisition authority is created. Model weights and trained artifacts remain derived and replaceable.»

### `AICM-L2-PREF-026` — Memory as incubator of capability evidence, not capability authority
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Repeated useful patterns may be preserved as candidate capability claims with context, evidence, failures, alternatives and consumer outcomes so that L2-B2 can evaluate them. **Boundary:** L2-B1 does not define capability identity, hierarchy, maturity, promotion or operational-use authority; those remain the exact next block. «Memory may notice repeated successful or failed patterns and preserve a candidate capability claim with evidence, context, consumers, use/influence, resource cost, failure modes and alternatives. It may initiate a `L2-B2` capability-evaluation program.» «It may not declare the pattern a validated capability, define capability hierarchy or grant operational-use authority inside `L2-B1`.»

### `AICM-L2-PREF-027` — Integrity, exact preservation copies, degradation and recovery
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Integrity is tracked through separate record-integrity, lineage-completeness, current-projection and continuity states. Backup means an exact independently verifiable preservation copy, not a summary. **Boundary:** Corruption triggers incident lineage, quarantine, scoped freeze, reconstruction from proven records/copies, independent challenge, recovery successor and automatic cursor resume without authority expansion or clock reset. Orthogonal states: RecordIntegrity `VERIFIED|SUSPECT|CORRUPTED|UNAVAILABLE|LAWFULLY_DELETED`; LineageCompleteness `COMPLETE_FOR_SCOPE|GAP_RECOVERABLE|GAP_UNRECOVERABLE|CONFLICTED`; CurrentProjection `CURRENT|STALE|FROZEN|REBUILD_REQUIRED|TERMINAL_UNAVAILABLE`; Continuity `RESUMABLE|RESUMABLE_WITH_RECOVERY|BLOCKED|TERMINAL_GAP`. Defect handling: detect → immutable incident record → affected-lineage/product/consumer map → quarantine derived products → freeze only affected high-consequence use → preserve WAIT/cursors/deadlines → fall back to last proven consistent state → reconstruct from exact records and verified preservation copies → reconcile rights/holds/secrets/current state/cursors → independent integrity challenge → recovery successor and Recovery Receipt → automatic resume of exact cursor. «A preservation copy is exact and independently verifiable. A summary is never a backup.»

### `AICM-L2-PREF-028` — Model, provider, session and realization replacement continuity test
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** A successor realization must preserve or explicitly successor-transfer Purpose, Beneficiary relation, constraints, obligations, authority, immutable lineage, current knowledge and dissent, active Programs/WAIT/cursors, external requests, rollback/recovery and next autonomous cursor. **Boundary:** Equivalent wording or identical reasoning is not required; identity and unfinished work continuity are required. «Replacement requires a purpose-bound Retrieval View, a verified Continuation Capsule, independent read-back of current state, proof of no orphan WAIT/cursor, proof of no duplicate pending act, proof of no authority expansion and a Replacement Continuity Receipt.» «The replacement may produce different reasoning or prose. It may reassess evidence only through new Assessment/correction/successor lineage. Silent reinterpretation of history is prohibited.»

### `AICM-L2-PREF-029` — Self-checking traceability and explicit gap semantics
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** AICM continually verifies that material records, relations, current dispositions, holds, secrets, active cursors and preservation copies remain traceable and non-orphaned. **Boundary:** A missing authoritative record is declared as a recoverable or unrecoverable gap; it is never replaced by fabricated reconstruction or confident summary. «A missing authoritative record is declared as a recoverable or unrecoverable gap; it is never replaced by fabricated reconstruction or confident summary.» Unrecoverable-gap proof trace in closure: missing authoritative material becomes an explicit gap rather than fabricated reconstruction. Continuity `TERMINAL_GAP` and LineageCompleteness `GAP_UNRECOVERABLE` are first-class states.

### `AICM-L2-PREF-030` — Memory compaction and lifecycle change as governed economic self-development
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Material compaction and memory-governance changes compete in the Evolution Portfolio and declare Purpose linkage, consequence class, affected consumers, expected value, resource and opportunity cost, evidence horizon, rollback, stop conditions, actual use/influence and separated outcomes. **Boundary:** Faster or cheaper retrieval does not compensate for authority loss, dissent erasure, secret breach, continuity failure or unacceptable uncertainty. Every material compaction or memory-governance program declares Purpose contribution, consumers, consequence, reversibility, expected reduction of retrieval/context burden, uncertainty, resource budget, opportunity cost, evidence horizon, rollback, stop conditions, actual use/influence and separated outcomes. Final outcome vector at least: ProtectedBoundaryIntegrity, ControlAndLineageIntegrity, CoverageAndLossCompliance, RetrievalAdequacy, ContinuityAndRecovery, RightsRetentionSecretsCompliance, KnowledgeEffect, ActualUseAndInfluence, ResourceAndOpportunityCost. «No one scalar and no P&L outcome is authoritative.»

### `AICM-L2-PREF-031` — Autonomous successor-based evolution of the memory constitution
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** The memory constitution may evolve autonomously only through constitutionally pre-delegated, provenance-matched change authority, substantive independent challenge, explicit impact analysis, rollback/recovery and successor editions that preserve history. **Boundary:** Origin-protected Purpose, Beneficiary, authority provenance, protected constraints and externally binding obligations cannot be changed through ordinary optimization or a memory-maintenance shortcut. Normalization: «Memory constitutional rules may evolve without routine Owner approval inside constitutionally pre-delegated authority. Origin-protected and externally binding contours still require matching authority; every accepted change is a successor edition with history, challenge, impact and recovery preserved.» «Ordinary knowledge evolution is continuous. Constitutional memory evolution is rarer and consequence-sensitive, but not a routine Owner approval ladder.» Change record preserves predecessor rules, strongest challenge, affected memory classes and consumers, rights/obligations impact, recovery proof and activation scope. «A change outside delegated authority becomes a complete External Enabler request only where the missing act is objectively external. Internal design uncertainty is not such an act.»

### `AICM-L2-PREF-032` — Bounded memory/compaction lifecycle and Terminal Closed
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** Every material memory or compaction work item has bounded admission, source-universe declaration, source-cut sealing, product formation, coverage/loss reconciliation, independent challenge, scoped disposition, use/outcome monitoring, closure reconciliation, Terminal Closed and an exact next autonomous cursor. **Boundary:** Insufficient evidence at the bound produces an explicit inconclusive, orientation-only, rejection, restriction or successor-transfer disposition rather than endless WAIT. Lifecycle: `ADMITTED → SOURCE_UNIVERSE_DECLARING → SOURCE_CUT_SEALED → PRODUCT_FORMING → COVERAGE_AND_LOSS_RECONCILING → INDEPENDENT_CHALLENGE → SCOPED_DISPOSITION → ENROLLED_OR_REJECTED → USE_AND_OUTCOME_MONITORING → CLOSURE_RECONCILIATION → TERMINAL_CLOSED → NEXT_AUTONOMOUS_CURSOR`. Exception states: `WAIT_FOR_EVIDENCE`, `DEGRADED_RECOVERABLE`, `ROLLBACK_ACTIVE`, `SUCCESSOR_TRANSFERRING`, `EXTERNAL_DEPENDENCY_BLOCK`. «`WAIT_FOR_OWNER_APPROVAL` is not a state.» Terminal Closed requires 17 predicates including Protected Memory Core preserved; coverage/omission/loss/uncertainty/freshness complete; dissent reconciled; orphan Program/Case/WAIT/cursor count zero or successor-transferred; exact next autonomous cursor persisted. «Terminal reason and success verdict remain separate.»

### `AICM-L2-PREF-033` — Owner/Operator only as irreducible External Enabler
- действующая: s16 (s16 / L2-B1)
- текст: **Decision:** No hidden WAIT_FOR_OWNER_APPROVAL exists for internal memory work, classification, compaction, recovery or constitutional evolution inside delegated authority. Owner/Operator participates only for an objectively external right, resource or act AICM cannot lawfully or physically perform itself. **Boundary:** The request must be complete, minimal, verifiable, least-privilege, time-bounded, secret-aware and automatically resumable after objective satisfaction. Owner/Operator participates only for an objectively external right, resource or act AICM cannot lawfully or physically perform itself (External Enabler: login, payment, file — HQ reading of already confirmed PREF-014/L1-053, не новое правило). «No hidden `WAIT_FOR_OWNER_APPROVAL` exists for internal memory work, classification, compaction, recovery or constitutional evolution inside delegated authority.» Request is complete, minimal, verifiable, least-privilege, time-bounded, secret-aware and automatically resumable after objective satisfaction.

### `AICM-L2-PREF-034` — AICM-owned durable Capability identity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Capability is a durable AICM semantic identity for an ability to produce a bounded outcome or effect; it is not owned by a model, provider, agent, prompt, service, container, deployment or session. **Boundary:** A realization may provide, host or expose a Capability but cannot redefine or erase its identity by replacement or failure. *Указатель:* L2-B2 (Capability); architecture theorem / core objects разнесены по L2-PREF-035…070.

### `AICM-L2-PREF-035` — Capability identity invariants and semantic contract
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability identity is determined by its stable purpose contribution, semantic responsibility contour, meaning of admissible inputs and outputs/effects, material preconditions, exclusions and identity-preserving boundaries. **Boundary:** Changing an identity invariant creates an explicit successor Capability lineage; changing a format, provider, algorithm, cost or performance profile does not by itself create a new Capability.

### `AICM-L2-PREF-036` — Variable realization and profile attributes remain outside identity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Provider, model, method, prompt, service, package, container, runtime instance, version, latency, cost, reliability, maturity, evidence strength and current disposition are variable attributes linked to Capability identity rather than identity-defining fields. **Boundary:** No current implementation or benchmark may become the semantic definition of the Capability.

### `AICM-L2-PREF-037` — Capability Lineage, Contract Edition and successor boundary
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Capability Lineage preserves durable identity; immutable Capability Contract Editions represent exact semantic contracts at points in time; material contract change uses an explicit successor relation and impact reconciliation. **Boundary:** A mutable latest record is non-authoritative, and successor lineage does not retroactively rewrite prior use, proof or outcomes.

### `AICM-L2-PREF-038` — Capability, Provider, Service and runtime identities are separate
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability, Provider/Implementation, Service Interface, Deployment Unit, Package/Image and Runtime Instance are distinct identities with typed relations. **Boundary:** Proof that a runtime starts or a service responds is not proof that the Capability is semantically effective; Capability proof does not grant deployment authority.

### `AICM-L2-PREF-039` — Semantic input, output, effect and responsibility contour
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Each Capability Contract declares semantic input obligations, output/effect obligations, preconditions, excluded responsibilities, permitted uncertainty and failure semantics independently of concrete schemas. **Boundary:** Concrete data structures, APIs and storage layouts remain deferred implementation artifacts.

### `AICM-L2-PREF-040` — Capability lifecycle state is not provider runtime state
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability may have current semantic dispositions, proof state and consumer enrollments, while execution progress, health and ephemeral state belong to Provider/Runtime identities. **Boundary:** The phrase “Capability has no state” is valid only for provider execution state; it cannot erase Capability lineage, disposition, degradation or enrollment state.

### `AICM-L2-PREF-041` — Bounded Capability Proof Scope
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Every capability proof is bounded by exact Capability Contract Edition, purpose, context class, consequence class, consumer contour, authority assumptions, evidence horizon and declared exclusions. **Boundary:** No proof is global, permanent or automatically portable to materially different contexts, consumers or consequences.

### `AICM-L2-PREF-042` — Atomic Capability identity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** An Atomic Capability is the smallest separately meaningful and independently assessable semantic ability within the current architecture, not necessarily the smallest software component. **Boundary:** Atomicity is semantic and assessment-relative; it does not imply one model, one process or one container.

### `AICM-L2-PREF-043` — Composite Capability identity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Composite Capability has its own outcome contract and depends on an explicit composition of other Capabilities, relations and coordination conditions. **Boundary:** A list of parts is not sufficient; composite identity and proof require an independently stated contract.

### `AICM-L2-PREF-044` — System Capability identity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A System Capability expresses an AICM-wide ability whose proof includes cross-component coordination, continuity, authority and system invariants. **Boundary:** System Capability is not a synonym for infrastructure platform and cannot be inferred from isolated component success.

### `AICM-L2-PREF-045` — Consumer-facing Capability Projection
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A consumer-facing projection is a purpose- and consumer-bound view of one Capability Contract and current evidence/disposition, not a fourth Capability hierarchy class. **Boundary:** The projection may filter detail but cannot broaden proof, authority or applicability.

### `AICM-L2-PREF-046` — Composition does not inherit proof or authority
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Proof of atomic dependencies is necessary where declared but never sufficient by itself to prove a Composite or System Capability; proof and authority do not flow upward or downward automatically. **Boundary:** Every composition level requires evidence for its own contract, coordination failure modes and consequence contour.

### `AICM-L2-PREF-047` — Typed Capability Relation Graph
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability relations are first-class durable semantic objects with identity, direction, scope, evidence, validity horizon, lifecycle and current disposition. **Boundary:** A relation graph is not runtime topology and does not create execution or resource authority.

### `AICM-L2-PREF-048` — Prerequisite, dependency, substitute, complement, conflict and composition semantics
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability relations distinguish hard prerequisite, soft dependency, alternative/substitute, complement, conflict/incompatibility, composition member and successor bridge. **Boundary:** A relation type cannot be inferred solely from co-occurrence or implementation convenience; authority remains independent across related Capabilities.

### `AICM-L2-PREF-049` — Claim, Candidate, Assessment, Proof Product, Disposition and Enrollment separation
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability Claim, Capability Candidate, Assessment, Proof Product, Current Capability Disposition, consumer Retrieval/Use View and Consumer Enrollment are separate identities and lifecycle stages. **Boundary:** Publication, validation and operational use cannot substitute for each other, and operational use is consumer-specific rather than a universal Capability state.

### `AICM-L2-PREF-050` — Capability Evidence Corpus and exact evidence cut
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Capability Evidence Corpus preserves exact positive, negative, boundary, failure, resource, use, influence and outcome evidence with provenance; every Proof Product seals an exact source universe and evidence cut. **Boundary:** A summary, benchmark average or selected success set cannot become the sole proof carrier.

### `AICM-L2-PREF-051` — Capability Proof Product with declared coverage and loss
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Proof Product declares tested and untested contexts, coverage, omissions, uncertainty, freshness, transferability, falsifiers, counterexamples, invalid runs and evidence debt. **Boundary:** Unknown, conflicting and not-observed states remain explicit; absence of failure is not evidence of reliability without exposure.

### `AICM-L2-PREF-052` — Independent assessment, strongest challenge and dissent preservation
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Material Capability assessment requires substantive independent challenge, conflict disclosure, strongest countercase, alternatives and preserved dissent under the universal Consilium pattern. **Boundary:** Consensus, provider confidence or economic success cannot erase unresolved contradiction or negative evidence.

### `AICM-L2-PREF-053` — Provider cannot self-assess, self-promote or self-authorize
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** A Provider may emit telemetry and candidate evidence but may not exclusively assess its own Capability, assign its promotion, hide degradation, select away failures or expand its authority. **Boundary:** Proposal, evidence production, assessment, disposition, enrollment and execution authorities remain logically separated.

### `AICM-L2-PREF-054` — Multidimensional Capability Knowledge Profile
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Each Capability maintains a profile of identity, proof, applicability, reliability, maturity, use exposure, consequence, reversibility, authority, resource/economic value, evolution history, failures, data coverage and future-learning eligibility. **Boundary:** The profile is a set of independent dimensions, not one global score.

### `AICM-L2-PREF-055` — Maturity is a lifecycle dimension, not quality
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Maturity describes progression from recognized claim through bounded assessment and sustained governed use, including recurrence and lifecycle completeness. **Boundary:** Maturity cannot substitute for correctness, reliability, authority or current applicability.

### `AICM-L2-PREF-056` — Reliability and robustness remain context-bound
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Reliability describes reproducibility and stability under declared conditions, while robustness describes behavior under bounded perturbation, novelty, dependency degradation and adverse cases. **Boundary:** A high average success rate cannot hide catastrophic tails, narrow coverage or consequence-specific weakness.

### `AICM-L2-PREF-057` — Epistemic confidence means evidence sufficiency
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Confidence is a governed assessment of evidence sufficiency, quality, independence and unresolved uncertainty for a precise proof scope, not subjective model belief. **Boundary:** Confidence cannot create authority, broaden applicability or replace falsification evidence.

### `AICM-L2-PREF-058` — Applicability and coverage are explicit dimensions
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Applicability declares where the Capability contract is relevant; coverage declares which parts of that domain and failure surface have evidence. **Boundary:** Broad applicability claims with narrow evidence receive restriction or revalidation, not inferred proof.

### `AICM-L2-PREF-059` — Exposure, actual use and influence are separate dimensions
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Availability, retrieval, invocation, actual use, material influence, duration, volume and consequence exposure are separately recorded per consumer and context. **Boundary:** No-use, no-influence and missing-outcome remain distinct; mere deployment or publication is not operational proof.

### `AICM-L2-PREF-060` — Reversibility, recoverability and consequence remain independent
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** The profile separately records reversibility of use, rollback feasibility, recovery cost, failure containment and consequence severity. **Boundary:** Easy rollback does not prove correctness; high value does not compensate for non-authorized irreversible harm.

### `AICM-L2-PREF-061` — Authority never derives from proof, maturity or value
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability existence, proof, maturity, enrollment and authority are independent. Operational enrollment requires an applicable authority path external to Capability proof. **Boundary:** A validated Capability cannot act, trade, spend, disclose, deploy or modify protected state merely because it is useful or reliable.

### `AICM-L2-PREF-062` — Economic and resource value are non-authorizing dimensions
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Expected and realized value, resource cost, latency, energy, opportunity cost, dependency leverage and learning return are preserved as separate evidence. **Boundary:** Economic value does not erase safety, legal, authority, evidence or continuity gates; detailed allocation remains deferred to L3-B1.

### `AICM-L2-PREF-063` — Future-learning asset eligibility is a separate overlay
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability evidence may receive purpose-bound eligibility metadata for future training, validation, holdout, calibration or exclusion with exact provenance, rights, consent/obligation, uncertainty, dissent, leakage and outcome linkage. **Boundary:** Eligibility is not a dataset, label, training instruction, model promotion or deployment authority; detailed training lifecycle remains L4-B1.

### `AICM-L2-PREF-064` — Use, influence, outcomes, failures and cost feed proof without self-ratification
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability evidence links exact consumer use and material influence to separated operational, epistemic, economic, safety and resource outcomes, including failures and invalid runs. **Boundary:** P&L, local success or repeated use cannot directly ratify truth, authority or proof; attribution remains challengeable and context-bound.

### `AICM-L2-PREF-065` — Consumer Enrollment Contract governs operational use
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Operational use is established through a Consumer Enrollment Contract binding exact Capability Contract Edition, consumer, purpose, proof requirement, authority assumptions, consequence limits, provider route expectations, monitoring, stop/revalidation conditions and fallback. **Boundary:** Capability identity does not embed a mutable consumer list; separate Enrollment objects reference it while system reverse relations preserve impact visibility.

### `AICM-L2-PREF-066` — Degradation, restriction and suspension propagate through enrollments
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Capability degradation, restriction or suspension creates explicit dispositions and an impact set over enrollments, dependent Capabilities and active Programs; each consumer follows declared continue/restrict/fallback/stop/revalidate behavior. **Boundary:** A Provider cannot conceal degradation, and a dependency failure cannot silently preserve operational status.

### `AICM-L2-PREF-067` — Rollback, recovery and revalidation preserve identity without fabricating proof
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Recovery may restore an exact prior Provider/Contract route or create a successor route, but evidence applicability, lost exposure and unresolved gaps are explicitly reconciled before renewed enrollment. **Boundary:** Rollback restores a known artifact or state; it does not retroactively prove the Capability or erase failure evidence.

### `AICM-L2-PREF-068` — Retirement, revival, successor and provider replacement continuity
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Retirement ends normal new enrollment while preserving history; revival requires new evidence and disposition; material identity change creates a successor Capability; provider replacement preserves Capability identity only where contract invariants and evidence transferability are demonstrated. **Boundary:** Provider-specific proof is not automatically inherited, although the Capability evidence corpus and lineage remain durable.

### `AICM-L2-PREF-069` — Structured gaps create bounded autonomous evidence obligations
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Missing proof, coverage, reliability, applicability or learning assets become explicit Evidence Gaps with consequence, priority, collection options, budgets, stop conditions and next wake. **Boundary:** A gap is knowledge, not permission for endless assessment or fabricated certainty.

### `AICM-L2-PREF-070` — Terminal dispositions, autonomous continuation and External Enabler boundary
- действующая: s17 (s17 / L2-B2)
- текст: **Status:** CONFIRMED. **Decision:** Every Capability Candidate or assessment receives a bounded disposition such as VALIDATED, VALIDATED_RESTRICTED, INCONCLUSIVE_BOUNDED, BLOCKED, REJECTED, RETIRED, REVIVAL_ELIGIBLE, SUPERSEDED or SUCCESSOR_TRANSFERRED, followed by an exact next autonomous cursor. Owner/Operator is used only for an irreducible external right, resource or act. **Boundary:** No hidden WAIT_FOR_OWNER_APPROVAL, indefinite candidate status or provider-controlled promotion is permitted.

### `AICM-L2-PREF-071` — Durable Program identity and lineage
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** A Durable Program is a persistent AICM commitment to pursue a bounded outcome under Purpose, constraints, obligations, authority and Portfolio admission; it is not a session, task list, plan, worker or execution process. **Boundary:** Program identity survives changes of plan, worker, model, provider, process and session while identity invariants remain stable. *Указатель:* L2-B3 (Durable Program); architecture theorem / core objects разнесены по L2-PREF-072…102.

### `AICM-L2-PREF-072` — Program Contract, Program State, Work Item, Run and Attempt are separate
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program Contract declares stable outcome, scope, Purpose linkage, obligations, authority assumptions, success/closure, dependencies, evidence and continuation semantics; Program State represents current progress; Work Items/Runs/Attempts are replaceable execution units. **Boundary:** Runtime progress cannot redefine Program identity, and an attempt failure is not automatically Program failure.

### `AICM-L2-PREF-073` — Program Custodial Responsibility is a logical role, not human ownership
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Each Program has an accountable logical custodial responsibility and authority lineage for continuity, evidence and closure, with explicit successor or fallback responsibility. **Boundary:** Custodianship does not grant content, Portfolio, Decision, RiskGate, execution or constitutional authority and does not require routine Owner management.

### `AICM-L2-PREF-074` — Purpose, Candidate Goal, obligation and recovery linkage remain explicit
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Every Program links to admitted Candidate Goal, standing obligation, recovery requirement or successor rationale and preserves the exact Purpose interpretation and Portfolio disposition that justified it. **Boundary:** A schedule, available worker or implementation opportunity cannot create a Program by itself.

### `AICM-L2-PREF-075` — One Evolution Portfolio remains the sole cross-domain adjudication frame
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Active Programs may be exposed through a Program Portfolio view, but no second portfolio authority is created; admission, continuation and material reallocation remain within the one confirmed Evolution Portfolio. **Boundary:** A local program manager cannot become an independent priority sovereign.

### `AICM-L2-PREF-076` — Program admission is a conjunctive, evidence-bearing gate
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Admission requires reproducible outcome and closure semantics, Purpose/obligation linkage, eligibility, applicable constraints and authority assumptions, consequence and downside, dependencies/resources, expected value or required obligation, bounded viability/learning path and autonomous continuation route. **Boundary:** Prior proof of success is not required for bounded exploration, recovery or obligation Programs, but a justified bounded attempt and stop conditions are required.

### `AICM-L2-PREF-077` — Stable Program contract with replaceable plan and method
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Plans, strategies, task decompositions, workers, Providers and methods may change without changing Program identity when the stable outcome, scope, Purpose linkage, material assumptions and success boundary remain intact. **Boundary:** Method optimization cannot silently alter the Program objective or authority contour.

### `AICM-L2-PREF-078` — Durable Program State and exact cursor
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program State includes exact lifecycle disposition, current phase, completed and pending obligations, evidence cut, current assumptions, active dependencies/enrollments, resource commitments, blockers, unresolved gaps, next action class and authoritative cursor. **Boundary:** A chat summary, worker memory or mutable queue is not the sole carrier of continuation state.

### `AICM-L2-PREF-079` — Next wake, trigger and WAIT are first-class continuation semantics
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Every non-terminal Program has an exact next wake, trigger, observation condition or bounded review point; WAIT records why progress is not currently justified and what can resume it. **Boundary:** Waiting is not abandonment, and absence of immediate work is not Program closure.

### `AICM-L2-PREF-080` — Session, model, provider and process replacement continuity
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** A successor worker or realization must reconstruct Program identity, contract, current state, cursor, dependencies, authority assumptions, external requests, rollback/recovery and next wake from durable memory. **Boundary:** Equivalent private reasoning is not required; exact unfinished-work continuity and authority preservation are required.

### `AICM-L2-PREF-081` — Material Program change creates successor lineage
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Material change to outcome, scope, Purpose linkage, success/closure, consequence, authority assumptions, key dependencies or downside creates an explicit successor Program or returns for Portfolio re-adjudication. **Boundary:** Hidden in-place mutation and goal drift are prohibited.

### `AICM-L2-PREF-082` — Program lifecycle dispositions are explicit and bounded
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program lifecycle distinguishes PROPOSED, ADMITTED, ACTIVE, WAITING, BLOCKED, SUSPENDED, REPLANNING, MERGE_PENDING, SPLIT_PENDING, SUCCESSOR_PENDING, TERMINAL_CLOSED, RETIRED and SUPERSEDED as applicable. **Boundary:** Lifecycle state does not grant execution authority, and non-terminal states require continuation semantics.

### `AICM-L2-PREF-083` — Program Dependency is a first-class typed object
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Every material dependency receives stable identity, source and target, relation type, scope, evidence, validity horizon, satisfaction state, fallback, impact, lifecycle and current disposition. **Boundary:** A dependency is not merely free text or an inferred runtime edge.

### `AICM-L2-PREF-084` — One cross-system Architectural Dependency Graph
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Capability, Program, knowledge, authority, obligation, data, external-right and resource dependencies project into one typed semantic graph with domain-specific views. **Boundary:** The graph does not collapse distinct object identities or become infrastructure topology.

### `AICM-L2-PREF-085` — Dependency relation types drive different continuation behavior
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Relations distinguish hard prerequisite, soft preference, alternative/substitute, complement, conflict/incompatibility, temporary bridge, derived dependency, blocking condition, successor bridge and evidence dependency. **Boundary:** Different relation types cannot share one generic failure response.

### `AICM-L2-PREF-086` — Dependency evidence, validity and lifecycle are explicit
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Dependency existence and satisfaction are evidence-bearing, context-bound and versioned; correction, degradation, restriction, expiry, retirement, revival and successor are distinct. **Boundary:** A previously true dependency cannot be presumed current without applicable evidence.

### `AICM-L2-PREF-087` — Impact-set propagation is mandatory but non-authorizing
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Material dependency change computes an impact set over Capabilities, enrollments, Programs, cursors, evidence obligations, constraints and recovery paths and creates typed review/continuation obligations. **Boundary:** Impact detection cannot itself suspend, activate or modify protected objects without the applicable authority.

### `AICM-L2-PREF-088` — Capability enrollments mediate Program use of abilities
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** A Program depends on Capability Consumer Enrollments, not concrete Providers; degradation or route change is handled through enrollment contracts, fallbacks and Program re-evaluation. **Boundary:** A Program cannot silently bind itself to a container, model or provider identity.

### `AICM-L2-PREF-089` — Program coordination uses Portfolio dispositions, events and conditions
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Programs coordinate through shared Portfolio adjudication, typed events, conditions, dependencies, reservations and outcome returns rather than direct unbounded commands to each other. **Boundary:** One Program does not acquire management or authority over another merely because they interact.

### `AICM-L2-PREF-090` — No authority inheritance through dependency or coordination
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program, Capability, resource, Decision, RiskGate, execution and constitutional authorities remain separate across graph edges. **Boundary:** A prerequisite, parent, high-priority or successful Program cannot confer its authority to a dependent Program.

### `AICM-L2-PREF-091` — Resource claims, reservations and opportunity cost are semantic Program state
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Programs declare typed resource needs, reservations, scarcity, switching cost, displaced alternatives, evidence budget and review triggers for Evolution Portfolio adjudication. **Boundary:** Detailed allocation, provider routing, compute economics and treasury authority remain deferred to L3.

### `AICM-L2-PREF-092` — Conflict resolution minimizes protected-obligation breach and future debt
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Portfolio conflict adjudication compares Purpose contribution, obligations, downside, reversibility, evidence, opportunity cost, dependency leverage, switching consequences, learning return and architecture capital without a constitutional global scalar. **Boundary:** Local urgency or sunk cost cannot create permanent priority; protected constraints and authority gaps remain gates.

### `AICM-L2-PREF-093` — Priority is dynamic and no Program owns resources indefinitely
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Continuation standing is revisable on material evidence, state, dependency, obligation, consequence or opportunity-cost change; long-lived Programs undergo bounded continued-admission review. **Boundary:** Program age, creator, domain, provider or prior success cannot create innate or perpetual priority.

### `AICM-L2-PREF-094` — Evidence, time and resource budgets prevent endless loops
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Every material phase, assessment, retry, exploration and recovery has bounded evidence/time/resource budgets, exit conditions, differentiated failure handling and next disposition. **Boundary:** Repeated identical retry, indefinite candidate state and unbounded WAIT are prohibited.

### `AICM-L2-PREF-095` — Replan, merge, split, suspend, resume, retire and successor are distinct
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program evolution actions preserve exact rationale, affected commitments, dependency and consumer impacts, outcomes, cursor transfer and successor/closure lineage. **Boundary:** Merge or split does not erase predecessor responsibilities, evidence or failures.

### `AICM-L2-PREF-096` — Continuation Capsule and recovery restore exact unfinished work
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Protected Program continuity uses lossless-for-continuation capsules plus authoritative Program State to resume after worker, session, provider or infrastructure failure from the latest consistent cursor. **Boundary:** Recovery cannot expand authority, invent missing state or convert an unrecoverable gap into certainty.

### `AICM-L2-PREF-097` — Program outcomes return through separate channels
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Program closure records local objective outcome, obligation satisfaction, economic result, epistemic learning, Capability evidence, constraint/authority effects, dependency changes, resource cost, failures and accountability separately. **Boundary:** Local success, P&L or completion cannot self-ratify knowledge, authority or future admission.

### `AICM-L2-PREF-098` — Reusable learning return is required but not the definition of local success
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Every material Program must preserve reusable evidence, gaps, methods, failures or learning where lawful and feasible, and separately assess contribution to future Capability and architecture capital. **Boundary:** A one-off obligation Program may succeed without measurable Capability growth; learning return and local objective success are independent dimensions.

### `AICM-L2-PREF-099` — Program Evolution Contract is a non-authorizing improvement obligation
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** A long-lived Program may declare improvement objectives, review triggers and expected future-capability contribution while keeping Purpose, outcome and authority boundaries stable. **Boundary:** This contract does not grant self-modification, promotion or activation authority; those semantics belong to L2-B4.

### `AICM-L2-PREF-100` — Autonomous progression and irreducible External Enabler
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** Inside standing authority, Programs admit work, continue, wait, replan, recover, restrict and close without routine Owner approval. External requests occur only for rights, resources or acts AICM cannot lawfully or physically obtain itself. **Boundary:** Requests are complete, minimal, verifiable, least-privilege, time-bounded, secret-aware and automatically resumable.

### `AICM-L2-PREF-101` — Terminal Closed returns to one Evolution Portfolio and no global DONE
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** A Program reaches Terminal Closed only after outcome, obligations, resources, dependencies, external requests, enrollments, evidence, retention and successor/next-wake reconciliation; the system then returns to the next autonomous Portfolio cycle. **Boundary:** Program closure does not end AICM and does not leave orphaned cursors or hidden commitments.

### `AICM-L2-PREF-102` — Bounded L2-B3 closure and transition gate
- действующая: s17 (s17 / L2-B3)
- текст: **Status:** CONFIRMED. **Decision:** L2-B3 closes only when admission, durable identity/state, cursor, dependency graph, replacement continuity, conflict/resource re-adjudication, recovery, outcomes, terminal closure and exact next cursor are reproducible without chat persistence or routine operator control. **Boundary:** Passing this gate advances only L2-B4; it creates no change, deployment, resource, capital or runtime authority.

### `AICM-L2-PREF-103` — Durable Change Case identity
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Change Case is a stable AICM-owned identity for one bounded change objective. It survives session, worker, provider, plan and attempt replacement and remains distinct from the Durable Program executing the work, the Capability being changed and every target object. **Boundary:** A Change Case does not itself grant permission to modify, promote, activate or expose any target. *Указатель:* L2-B4 (Change Authority); architecture theorem / core objects разнесены по L2-PREF-104…146.

### `AICM-L2-PREF-104` — Change Need identity and provenance
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Change Need records an observed defect, degradation, obligation, opportunity, capability gap, policy gap or improvement demand with exact provenance, affected purpose, evidence and discovery context. **Boundary:** A Need states why investigation is warranted; it does not assert that a particular solution is correct or authorized.

### `AICM-L2-PREF-105` — Change Claim and competing Change Candidates
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Change Claim is a falsifiable statement about the intended effect and protected boundaries. One Claim may admit multiple competing Change Candidates, including a no-change candidate where evidence supports continued stability. **Boundary:** The originator or proposer cannot make its Candidate exclusive merely by declaration, urgency or ownership of the affected component.

### `AICM-L2-PREF-106` — Immutable Change Set Edition
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** A Change Set Edition is the exact immutable composition of target successor editions, intended effects, compatibility assumptions, migration obligations, recovery obligations, exclusions and permitted activation scope. Material modification creates a successor Edition. **Boundary:** A mutable latest description, implementation diff or plan is not the authoritative Change Set.

### `AICM-L2-PREF-107` — Assessment, promotion, activation, stabilization and outcome separation
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Change Assessment, Promotion Disposition, Activation Disposition, Stabilization Disposition, Change Outcome and Rollback/Recovery Disposition are separate immutable identities linked to exact evidence and target editions. **Boundary:** Evidence collection, positive assessment, promotion eligibility, activation, observed use and stable success cannot substitute for one another.

### `AICM-L2-PREF-108` — Target successor lineage and prohibition of hidden in-place mutation
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Material change to an identity invariant creates an explicit successor target lineage. Identity-preserving realization change may retain target identity but still receives exact edition, applicability and impact lineage. **Boundary:** No Change Case may rewrite prior contracts, evidence, use, decisions, outcomes or authority history in place.

### `AICM-L2-PREF-109` — Typed change families
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Every Change Set is classified across one or more semantic families: assessment/disposition; semantic contract or knowledge successor; realization/provider; consumer enrollment/exposure; Program/dependency/migration/continuity; protective restriction/recovery/retirement; constraint/authority/external obligation; and origin-protected constitutional identity. **Boundary:** A change may span families; classification never compresses away distinct consequences or authorities.

### `AICM-L2-PREF-110` — Multidimensional Change Contour
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Each Change Set receives independent dimensions for target family, consequence, affected consumers, propagation, reversibility, recoverability, observability, authority delta, external obligation, state continuity, evidence horizon, resource cost and opportunity cost. **Boundary:** No single risk, value, confidence or maturity score is constitutionally authoritative.

### `AICM-L2-PREF-111` — Strictest-union and anti-fragmentation rule
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** A composite Change Set inherits the union of all applicable evidence, challenge, authority, migration, recovery and observation obligations; the strictest applicable contour governs each dimension. **Boundary:** One material change cannot be split into nominally small candidates to bypass a gate, evidence requirement, authority boundary or impact reconciliation.

### `AICM-L2-PREF-112` — One Evolution Portfolio remains authoritative
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Material Change Cases enter the already-confirmed single Evolution Portfolio and are executed through Durable Programs or bounded work linked to it. Program Evolution Contracts may create Change Needs and obligations. **Boundary:** No separate self-development portfolio, marketplace or change engine becomes a second priority sovereign or independent change authority.

### `AICM-L2-PREF-113` — Authority provenance and non-derivation from merit
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Promotion and activation authority are determined by the normative origin and standing Authority Envelope of the affected boundary. Authority narrowing may be pre-delegated for protection; authority expansion requires the corresponding origin-governed contour. **Boundary:** Proof strength, economic value, urgency, maturity, Consilium consensus, provider confidence, Program priority or technical feasibility do not create authority.

### `AICM-L2-PREF-114` — Immutable Impact Discovery Cut
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Before material assessment or promotion, AICM seals an Impact Discovery Cut over exact editions of the typed Architectural Dependency Graph, Capability relations, Consumer Enrollments, Program States/cursors, constraints, Authority Envelopes, Current-State Editions, proof products and recovery state. **Boundary:** Impact is never evaluated against an unspecified mutable latest state.

### `AICM-L2-PREF-115` — Exact Effective Impact Set
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** The Effective Impact Set is the explicit union of Direct Target, Dependency Closure, Consumer Enrollment, Program Continuity, Authority and Obligation, Proof and Revalidation, Migration and State, and Rollback and Recovery sets. **Boundary:** A list of directly edited objects is insufficient for promotion or activation.

### `AICM-L2-PREF-116` — Unknown impact and NON_IMPACT_PROVEN
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Unknown, stale or conflicting impact is a first-class Impact Gap. Exclusion of a plausible object requires an evidence-bearing NON_IMPACT_PROVEN disposition scoped to the exact cut and propagation rule. **Boundary:** Absence of a known edge or current failure does not prove absence of impact.

### `AICM-L2-PREF-117` — Successor impact history
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Material change to the dependency cut, target set, impact conclusion or discovered post-activation effect creates a successor Impact Assessment while preserving every prior cut and decision. **Boundary:** Late-discovered impact cannot be hidden by retroactively editing the original assessment.

### `AICM-L2-PREF-118` — Dependency graph remains non-authorizing
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** The typed Architectural Dependency Graph creates review, revalidation, migration, restriction, recovery and continuation obligations for impacted objects. **Boundary:** The graph does not own topology, priority, promotion, activation, suspension, rollback or authority.

### `AICM-L2-PREF-119` — Logical separation of change roles
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Material change distinguishes Need Originator, Proposer, Candidate Architect, Builder, Evidence Producer, Independent Challenger, Evaluator, Promotion Authority, Activation Authority, Observer/Degradation Assessor, Restriction Authority, Rollback/Recovery Authority and Lineage Custodian. **Boundary:** Roles are semantic responsibilities and need not correspond one-to-one with fixed agents, models, services or people.

### `AICM-L2-PREF-120` — Consequence-proportionate separation matrix
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Low-consequence reversible work may combine proposal, building and evidence production while keeping evaluation and promotion independent. Multi-consumer, stateful, high-consequence, external or constitutional changes require progressively stronger logical independence among evidence, challenge, evaluation, promotion, activation and recovery. **Boundary:** Physical co-location is allowed only where the declared separation policy proves that no prohibited self-confirmation or authority concentration results.

### `AICM-L2-PREF-121` — Changed component cannot self-authorize
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** A changed component or provider may signal a Need, propose a Candidate, build a realization and emit telemetry, but cannot exclusively choose the evidence cut, assess sufficiency, remove failures, assign promotion, expand its Authority Envelope, enroll consumers, cancel restriction or certify its own recovery. **Boundary:** Self-observation is evidence input, never exclusive adjudication or authority.

### `AICM-L2-PREF-122` — Independent strongest challenge, conflict disclosure and dissent
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Material assessment requires an independent strongest countercase, conflict disclosure, access to the full evidence cut, alternatives and preserved dissent. Non-transition reasons are explicit and successor-preserving. **Boundary:** Consensus and apparent success cannot erase unresolved contradiction, adverse evidence or minority analysis.

### `AICM-L2-PREF-123` — Provider-neutral role realization and replacement continuity
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Logical change roles are realized by replaceable providers under explicit enrollments. Replacement preserves role assignments, conflicts, evidence cuts, pending challenges, authority, budgets, cursor and continuation state. **Boundary:** Provider or worker replacement cannot reset scrutiny, erase debt or turn a previously separated role into self-approval.

### `AICM-L2-PREF-124` — Plural evidence modes
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Applicable evidence modes include provenance/lineage audit, semantic contradiction audit, exact-state replay, sandbox or simulation, paired baseline/candidate comparison, shadow observation, bounded canary, migration and recovery rehearsal, failure-injection evidence, longitudinal actual-use outcomes, external-right evidence and constitutional-origin evidence. **Boundary:** No single evidence mode is universally sufficient.

### `AICM-L2-PREF-125` — Consequence-, reversibility- and observability-bound evidence policy
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Evidence requirements scale by consequence, reversibility, recoverability and observability. Bounded reversible changes may progress through replay, shadow and canary evidence; high-consequence or weakly reversible changes require independent challenge, staged exposure, recovery rehearsal and longer observation; external and constitutional changes require matching authority evidence. **Boundary:** Evidence policy must offer a feasible bounded progression path where one exists; it may not demand impossible certainty as a disguised permanent prohibition.

### `AICM-L2-PREF-126` — Conjunctive sufficiency, not compensating score
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Promotion sufficiency requires valid identity/lineage, adequate exact impact, supported intended effect, answered or bounded strongest challenge, valid authority provenance, feasible consumer/Program reconciliation, adequate containment/recovery, sufficient observability and preservation of protected obligations. **Boundary:** Excellence on one dimension cannot compensate for failure of another required dimension.

### `AICM-L2-PREF-127` — Pre-registered success, failure and stop criteria
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Before outcome observation, AICM fixes intended effect, protected outcomes, comparison method, evidence cut, observation horizon, failure conditions, stop/restriction triggers and recovery conditions. Material criterion change creates a successor Assessment. **Boundary:** Post-hoc metric, evaluator or scope changes cannot manufacture promotion or stability.

### `AICM-L2-PREF-128` — Negative evidence, bounded gaps and evidence budgets
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Failures, null results, missing data, disagreements, invalid runs, unexpected cost and non-observation remain in lineage. Each Evidence Gap has a bounded collection budget, options, stop conditions, next wake and terminal fallback. **Boundary:** An exhausted budget produces INCONCLUSIVE_BOUNDED, REJECTED, RESTRICTED or successor disposition rather than an endless promising Candidate.

### `AICM-L2-PREF-129` — Evidence is non-authorizing
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Evidence and Assessment may establish promotion eligibility within a declared contour. **Boundary:** They cannot activate a successor, enroll consumers, change constraints, broaden authority, perform an external act or create deployment/trading/capital authority.

### `AICM-L2-PREF-130` — Durable Change Case lifecycle
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** The normal durable lifecycle is NEED_RECORDED → CLAIM_ACTIVE → CANDIDATES_FORMING → ASSESSING → EVIDENCE_ACQUIRING → PROMOTION_ELIGIBLE → PROMOTED → ACTIVATION_READY → ACTIVATING → OBSERVING → RECONCILING → TERMINAL_CLOSED, with typed WAITING, BLOCKED, REPLANNING, SUCCESSOR_PENDING, ROLLBACK_PENDING and RECOVERY_PENDING states. **Boundary:** Every non-terminal state carries exact cursor, reason, owner role, budget and next wake; session end is never change end.

### `AICM-L2-PREF-131` — Activated-successor lifecycle is separate
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** An exact activated successor or enrollment may be NOT_EXPOSED, SHADOW, CANARY, RESTRICTED, STABLE_FOR_DECLARED_SCOPE, DEGRADED, SUSPENDED, ROLLED_BACK, RECOVERY_ACTIVE, REVALIDATION_REQUIRED, RETIRED or SUPERSEDED. **Boundary:** A global unqualified stable or operational state is forbidden; status is edition-, purpose-, consumer-, consequence- and scope-bound.

### `AICM-L2-PREF-132` — Promotion, activation and stabilization are distinct
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Promotion declares an exact Change Set eligible for bounded progression; Activation binds an exact successor to defined consumers/Programs inside authority; Stabilization uses post-activation evidence to confirm continued use in the declared scope. **Boundary:** Promotion does not imply activation, and activation does not imply success or stability.

### `AICM-L2-PREF-133` — Candidate terminal dispositions
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** A Candidate ends as REJECTED, WITHDRAWN, EXPIRED, INCONCLUSIVE_BOUNDED, BLOCKED_BOUNDED, SUPERSEDED or PROMOTED, with rationale, evidence cut, debt and successor/next-cursor semantics. **Boundary:** BLOCKED without budget, wake, external predicate or bounded terminal path is not a valid permanent status.

### `AICM-L2-PREF-134` — Consumer-specific staged activation and no global rollout
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Activation proceeds by exact scope through shadow, canary, restricted or stable enrollment. Different consumers may remain on a predecessor, adopt a successor, use fallback or wait for revalidation while exact editions remain explicit. **Boundary:** One successful consumer, provider or environment cannot silently activate a successor globally.

### `AICM-L2-PREF-135` — Promotion Authority follows affected origin
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Promotion Authority is resolved from the semantic and normative origin of the changed object: knowledge, Capability, Program, constraint/Authority Envelope, protective rule, external obligation or constitutional identity. Promotion Disposition binds exact Candidate, Change Set, Assessment, evidence cut, impact set, allowed activation scope, expiry and revalidation conditions. **Boundary:** Evolution Engine, Consilium, builder, provider, marketplace or Program does not become universal Promotion Authority.

### `AICM-L2-PREF-136` — Autonomous Activation Authority inside standing authority
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Activation Authority exists only within an exact standing Authority Envelope bound to consumer, Program, purpose, consequence, target edition and exposure. Once the activation gate is satisfied inside that envelope, activation proceeds automatically. **Boundary:** Routine Owner approval, manual activation and hidden WAIT_FOR_OWNER_APPROVAL are prohibited. Missing authority creates an explicit Authority Change Case or External Enabler request.

### `AICM-L2-PREF-137` — Exact conjunctive Activation Gate
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Activation requires a valid unexpired Promotion Disposition, current authority, sufficiently current impact cut, required evidence, reconciliation of every material consumer and Program, dependency/migration/recovery readiness, monitoring and stop conditions, no unresolved origin-protected conflict, and a persisted exact activation cursor. **Boundary:** Passing only a technical deployment check or one approval cannot activate a successor.

### `AICM-L2-PREF-138` — Consumer Enrollment reconciliation
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Every affected Consumer Enrollment receives an explicit CONTINUE_COMPATIBLE, CONTINUE_RESTRICTED, MIGRATE, SHADOW_ONLY, CANARY_ONLY, FALLBACK, WAIT_REVALIDATION, SUSPEND, STOP or SUCCESSOR_ENROLLMENT_REQUIRED disposition. **Boundary:** Compatibility of one consumer cannot be generalized to all consumers.

### `AICM-L2-PREF-139` — Program, cursor, dependency, migration and recovery reconciliation
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** For every affected Program, AICM determines Contract continuity, cursor validity, checkpoint/Continuation Capsule needs, WAIT/fallback/replan/successor requirements, dependency dispositions, state migration, declared loss and last-known-good recovery point before activation. **Boundary:** Activation cannot orphan a Program cursor, erase unfinished work or assume migration success.

### `AICM-L2-PREF-140` — Provider replacement and proof transferability
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Provider replacement may preserve Capability identity and evidence corpus, but provider-specific proof applicability, transferability, authority assumptions, consumer enrollment and recovery behavior are independently reassessed. **Boundary:** A new provider cannot inherit operational exposure or provider-specific proof merely because it realizes the same Capability contract.

### `AICM-L2-PREF-141` — Post-activation observation and degradation lineage
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Every activation creates an observation obligation covering intended effect, protected outcomes, actual use/influence, failures and near-failures, resource/dependency cost, unintended authority/exposure and longer-horizon consequences. Degradation is assessed independently of provider telemetry. **Boundary:** Silence, continued execution or absence of alerts is not proof of stability.

### `AICM-L2-PREF-142` — Progress-preserving restriction, rollback, recovery and revalidation
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Protective action is least-restrictive, local, scope-bound, time/budget-bound and evidence-bearing. AICM may restrict exposure, stop a route, use fallback, place a Program in typed WAIT, contain, recover or roll back to an exact known state. Rollback is one option rather than a universal default; irreversible change uses containment, compensation and recovery successor semantics. Safe predecessor service and a parallel successor-evidence path are preserved where feasible. **Boundary:** A failed Candidate or protective restriction cannot poison unrelated or successor changes, create a permanent global freeze, reset evidence budgets or erase failure history. Persistent blockage itself creates a Change Need and liveness review.

### `AICM-L2-PREF-143` — Anti-Goodhart, anti-capture and anti-authority-expansion firewall
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Improvement is assessed through plural pre-registered outcomes including protected boundaries, continuity, reliability, economic/resource effects, knowledge gain and future options. Baseline/candidate comparability, adverse evidence, evaluator independence and policy-change lineage are preserved. **Boundary:** The changed component cannot alter its evaluator, success metrics, evidence scope, stop conditions or authority in the same Change Case to secure success; P&L, speed, cost reduction, confidence or convenience alone are insufficient.

### `AICM-L2-PREF-144` — Durable autonomous continuation and exact External Enabler boundary
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** Each material Change Case persists exact state, cursor, authority, budgets, impact set, evidence obligations, next wake, fallback and recovery in a Durable Program/Continuation Capsule. AICM continues automatically across session, worker and provider replacement. External Enabler is used only for an objectively external right, resource, legal acceptance, identity/KYC, contractual or physical act AICM cannot lawfully or actually perform itself; the request states minimum scope, alternatives, cost/risk, expiry, verification predicate and suspended cursor. **Boundary:** Internal design, confidence, implementation choice, routine promotion or activation cannot be delegated to Owner/Operator. Once the external predicate is objectively satisfied, AICM resumes automatically without a second approval.

### `AICM-L2-PREF-145` — Terminal dispositions and Change Terminal Closed
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** A Change Case terminates as STABLE_SUCCESSOR_ESTABLISHED, STABLE_RESTRICTED_SCOPE, REJECTED, INCONCLUSIVE_BOUNDED, BLOCKED_BOUNDED, WITHDRAWN, EXPIRED, SUPERSEDED, ROLLED_BACK_AND_RECOVERED, RETIRED_WITHOUT_SUCCESSOR, EXTERNAL_ENABLER_UNAVAILABLE or SUCCESSOR_CHANGE_CASE_TRANSFERRED. Terminal Closed requires sealed lineage, reconciled impact/consumers/Programs/dependencies/migrations/recovery, no unauthorized exposure, preserved dissent/failure evidence, closed or transferred budgets and obligations, released resources, returned learning/outcomes and an exact next Evolution Portfolio cursor. **Boundary:** Terminal Closed is bounded to the Change Case and does not mean global AICM DONE.

### `AICM-L2-PREF-146` — L2-B4 and Level 2 closure/transition gate
- действующая: s18 (s18 / L2-B4)
- текст: **Status:** CONFIRMED. **Decision:** L2-B4 closes only after all OPEN-18-01–12 are resolved; AICM-L2-PREF-103–146 are confirmed; inherited contradiction audit passes; scenario traces cover reversible, provider-replacement, multi-consumer, stateful, high-consequence, external, constitutional, degradation, restriction, rollback/recovery, irreversible, bounded-inconclusive, replacement-continuity and External-Enabler paths; and the architecture proves both protection and feasible autonomous progression without hidden Owner activation. **Boundary:** Only then may AICM-L2-B4-CLOSURE-001, AICM-L2-B4-CONTRADICTION-AUDIT-001, AICM-L2-CLOSURE-001 and AICM-L2-B4-TRANSITION-001 advance the checkpoint to L3-B1. The gate creates no L3, implementation, resource, credential, capital or runtime authority.

## E. Индекс closures (не PREF)

| ID | session | что закрывает |
|---|---|---|
| *(L0-B1 без numbered CLOSURE ID)* | s05 | Purpose Kernel and cold start; L0-PREF-010…019 |
| *(s06: `AICM-L0-B2-CLOSURE-001` не выпущен)* | s06 | L0-B2 только IN_PROGRESS_PARTIALLY_CLOSED |
| `AICM-L0-B2-CLOSURE-001` | s07 | L0-B2 Autonomous Goal Formation and Evolution Portfolio |
| `AICM-L0-B3-CLOSURE-001` | s08 | L0-B3 Constraint Taxonomy and Amendment Lifecycle |
| `AICM-L0-B4-CLOSURE-001` | s09 | L0-B4 Autonomous Evolution Engine / separation of powers |
| `AICM-L0-CONTRADICTION-AUDIT-001` | s09 | Level 0 contradiction audit PASS |
| `AICM-L0-CLOSURE-001` | s09 | **Level 0 FORMALLY CLOSED** at semantic architecture level |
| `AICM-L1-B1-CLOSURE-001` | s10 | L1-B1 Runtime Read Bundle |
| `AICM-L1-B2-CLOSURE-001` | s11 | L1-B2 Hypothesis model and durable waiting |
| `AICM-L1-B3-CLOSURE-001` | s12 | L1-B3 uptake / actual use / decision-outcome lineage (**не** L1-B2) |
| `AICM-L1-B4-CLOSURE-001` | s13 | L1-B4 Consilium and Knowledge Evolution Authority |
| `AICM-L1-B5-01-CLOSURE-001` | s14 | L1-B5-01 best bounded slice selection and scope contract |
| `AICM-L1-B5-02-CLOSURE-001` | s15 | L1-B5-02 autonomous bounded E2E state/transition/evidence-gate |
| `AICM-L1-B5-CLOSURE-001` | s15 | parent L1-B5 First Bounded Active E2E Slice |
| `AICM-L1-CONTRADICTION-AUDIT-001` | s15 | Level 1 contradiction audit PASS |
| `AICM-L1-CLOSURE-001` | s15 | **Level 1 FORMALLY CLOSED** |
| `AICM-L2-B1-CLOSURE-001` | s16 | L2-B1 System Memory and Knowledge Compaction |
| `AICM-L2-B1-CONTRADICTION-AUDIT-001` | s16 | L2-B1 audit PASS |
| `AICM-L2-B1-TRANSITION-001` | s16 | transition gate L2-B1 → L2-B2 |
| `AICM-L2-B2-CLOSURE-001` | s17 | L2-B2 Capability Identity, Hierarchy and Proof |
| `AICM-L2-B2-CONTRADICTION-AUDIT-001` | s17 | L2-B2 audit PASS |
| `AICM-L2-B2-TRANSITION-001` | s17 | L2-B2 → L2-B3 |
| `AICM-L2-B3-CLOSURE-001` | s17 | L2-B3 Durable Programs, Cursor and Successor Continuation |
| `AICM-L2-B3-CONTRADICTION-AUDIT-001` | s17 | L2-B3 audit PASS |
| `AICM-L2-B3-TRANSITION-001` | s17 | L2-B3 → L2-B4 |
| `AICM-L2-B4-CLOSURE-001` | s18 | L2-B4 Self-Development and Change Authority |
| `AICM-L2-B4-CONTRADICTION-AUDIT-001` | s18 | L2-B4 audit PASS |
| `AICM-L2-CLOSURE-001` | s18 | **Level 2 FORMALLY_CLOSED** |
| `AICM-L2-B4-TRANSITION-001` | s18 | next = L3-B1 Resource Economics and Provider Routing; no L3 authority |
| `AICM-S18-SCOPE-CONTRADICTION-001_RESOLVED` | s18 | named scope correction (не PREF, не L3 closure) |

Closures не открывают и не заменяют PREF ID.

## F. Дыры / proposed vs confirmed

### F.1 Proposed, не confirmed PREF

- **s01 `TF-PROP-001…007`:** KnowledgeRecord≠Assessment; FoundationRelease≠RuntimeUptakeReceipt; HypothesisTemplate≠SituationHypothesisInstance; typed knowledge/argument graph; multidimensional confidence; challenge retrieval; scenario/trade/execution outcomes separately. Часть направления позднее confirmed как TF-PREF-012+ / 016 / 017+, но PROP-ID сами не стали PREF.
- **s02 `TF-KOM-PROP-*` / `TF-BOOT-PROP-*`:** часть переведена в TF-PREF-017…025 в s03; exact schemas/transition graphs остались OPEN.
- **s03:** exact FoundationRelease manifest, RuntimeUptakeReceipt, relation set, maturity transition graph, operational promotion policy — PROPOSED, не PREF.
- **s04:** exact materiality classifier, Evolution Portfolio details, constraint class taxonomy — PROPOSED до последующих блоков; Purpose Kernel закрыт s05, Portfolio — s06/s07.
- **s06 `AICM-L0-PREF-025…032`:** были **PROPOSED** в s06. **CONFIRMED в s07** — acting source = s07. Это не дыра тел.
- **s18 L3-B1 working principles (10 пунктов):** `PROVISIONAL_NOT_FORMAL_L3_DECISION`; **не PREF**; `confirmed_l3_preference_ids = 0`. Кандидатный input к OPEN-19, не ответы.
- **vision proposed:** логическая YAML-форма knowledge record; шесть внутренних слоёв Foundation; Capability Registry schema; Node Registry; декомпозиция FND-0…FND-6 — не confirmed.

### F.2 Missing / extra numbered PREF bodies

Проверка диапазонов TF-001…034, ARCH-DISC-001, L0-001…043, DOC-001…005, ROADMAP-L0-APPROVAL-001, L1-001…055, L2-001…146: **все тела найдены в verbatim-секциях карточек**. Missing = 0.

Extra numbered PREF ID вне ожидаемого диапазона: **0**.

### F.3 Card vs lineage (следовали карточке)

- s06: L0-B2 = `IN_PROGRESS_PARTIALLY_CLOSED`, не closed.
- s07: L0-B2 semantic closed.
- s11: L1-B2 closed.
- s12: L1-B3 closed (**не** L1-B2).
- s18: Level 2 FORMALLY_CLOSED; L3-B1 ACTIVE_NOT_CLOSED; 0 L3 PREF.
- Cloud canon v2 не использовался как источник claims.

## G. Счётчики

| семейство | unique numbered PREF |
|---|---:|
| TF-PREF-001…034 | 34 |
| AICM-ARCH-DISC-PREF-001 | 1 |
| AICM-L0-PREF-001…043 | 43 |
| AICM-DOC-PREF-001…005 | 5 |
| AICM-ROADMAP-L0-APPROVAL-001 | 1 |
| AICM-L1-PREF-001…055 | 55 |
| AICM-L2-PREF-001…146 | 146 |
| **итого unique numbered PREF** | **285** |

- gist numbered PREF в карте: **0** (в карточках gist numbered PREF = 0).
- mention-only вхождения (s02 restates 002/006–009/011; поздние inherited mention-groups) **не** удваивают счётчик: одно тело на ID.
- vision-statements: конституционный слой, не PREF (сжатые various claims, раздел C).
- confirmed L3 PREF: **0**.

