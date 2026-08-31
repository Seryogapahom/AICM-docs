Статус: Knowledge Candidate. Не Foundation. Не канон AICM. Не PREF.
Дата доступа: 2026-08-31
Архив штаба: `razvedka/2026-08-31-ai-questionnaire-ecosystems.md`

# Экосистемы AI-опросников, elicitation предпочтений и агентских «вопросников» (2025–2026)

Пакет для позднего Foundation: механизмы извлечения ограничений/предпочтений и расширения вертикалей **без человека-дизайнера в контуре**. Owner = External Enabler, не дизайнер и не оператор в петле. Закрытая карта предпочтений L0–L2 (18 сессий) **не трогается**. ID в этом пакете — только `QE-*` (Knowledge Candidate), не PREF. OPEN-19 не превращается в домашнее задание Owner. Trading — первый экономический proof, не идентичность AICM. Метод опросника ортогонален слоям execution-policy и стратегии.

Три слоя **не склеены**: (A) продукты AI-native surveys, (B) alignment / preference elicitation, (C) агентские экосистемы. Где нельзя верифицировать — «не найдено». Слоган вендора ≠ факт способности. Отдельно — секция **«Фишки лабы (Grok HQ)»**: что из тренда внедрять в исследовательский центр Grok (не Hermes, не live, не новые пустые репо), на уже существующие роли и папки.

---

## 1. Тренды 2025–26

Что реально сдвинулось (shipping product, paper, spec), а не маркетинговый перечень.

### A) Продукты: AI-native surveys / interviewers

- **Синтез формы из промпта стал commodity, не «интервьюером».** Google Forms: «Help me create a form» — драфт формы из промпта или Drive-файла (Docs/Sheets/Slides/PDF); на 2026-08-31 официальная справка прямо пишет, что мультисекции и правка *текущей* формы через этот UI **ещё не поддерживаются**. URL: https://support.google.com/docs/answer/16346789 — доступ 2026-08-31.
- **Quiz-generation с ключом ответов — отдельный 2026-шипмент, не «опросник предпочтений».** Google Workspace Updates, 2026-07-30: Help me create генерирует quiz с правильными ответами и настройками quiz; rollout Rapid Release с 2026-07-24, Scheduled с 2026-08-05. Это оценка знания, не elicitation ограничений системы. URL: https://workspaceupdates.googleblog.com/2026/07/use-gemini-in-google-forms-to-quickly-create-a-new-quiz.html — доступ 2026-08-31.
- **Capped LLM follow-up (1–2) встроился в классические survey SaaS — это не conversational interviewer.** Qualtrics Conversational Feedback: Adaptive follow-up 1–2 вопроса + Response clarity validation; advanced = GPT-4o (OpenAI) через Azure; лимит «до 2 advanced follow-ups на респондента на весь опрос». URL: https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/conversational-feedback/ и https://www.qualtrics.com/support/survey-platform/sp-administration/artificial-intelligence-ai-administration/ — доступ 2026-08-31. Typeform Clarify with AI: «up to two» clarification questions на open-ended; LLM = Anthropic. URL: https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI — доступ 2026-08-31 (полный HTML help.typeform.com на WebFetch закрыт Cloudflare; сниппеты WebSearch + соседние Typeform-страницы).
- **Появился отдельный класс AI-moderated qualitative interviewers (голос/видео/текст, не skip-logic).** Listen Labs: changelog 2026 фиксирует MCP-создание исследований (2026-05-21), Research Agent (2026-02-11), 120+ языков интервью (2026-07-02), Pulse-лонгитюд (2026-08-11). URL: https://listenlabs.ai/whatsnew — доступ 2026-08-31. Outset: Abyss Mode (changeblog 2026-05-13) — многослойный probing; FAQ: discussion guide, probing depth и moderator style задаёт исследователь. URL: https://outset.ai/resources/changeblog/abyss-mode и https://outset.ai/resources/faq — доступ 2026-08-31. Recollective Conversation Task: AI-модератор ведёт диалог до выполнения Conversation Objective (helpdesk, last updated 2026-05-04 для Ask AI). URL: https://helpdesk.recollective.com/article/480-task-type-conversation — доступ 2026-08-31. Discuss.io Interview Agent анонсирован 2025-02-27. URL: https://www.discuss.io/press/spring-release-2025/ — доступ 2026-08-31.
- **Форма стала MCP-инструментом агента (2025–2026), не только UI для человека.** Tally: MCP beta 2025-07-11; Tally AI для всех 2026-07-08; официальный ChatGPT plugin + Claude connector 2026-08-27. URL: https://tally.so/changelog и https://tally.so/help/free-ai-form-builder — доступ 2026-08-31. Typeform MCP server: tools `forms-*`, `automations-*`, `contacts-*`, `insights-*`. URL: https://www.typeform.com/developers/get-started/mcp/ — доступ 2026-08-31. Listen Labs MCP: создание/запуск исследований из ChatGPT/Claude, 2026-05-21. URL: https://listenlabs.ai/whatsnew — доступ 2026-08-31.
- **Тема/кластер open-ended ответов — анализ *после* сбора, не elicitation.** Typeform Smart Insights: summary + topic detection + sentiment; qualifying analysis на Claude 3.5 Sonnet (private copy); минимум 10 ответов, English. URL: https://help.typeform.com/hc/en-us/articles/44393511518100-Smart-Insights-Qualitative-and-quantitative-analysis и https://help.typeform.com/hc/en-us/articles/23542072977172-Get-AI-analysis-of-your-results-with-Smart-Insights — доступ 2026-08-31. SurveyMonkey Analyze with AI: чат по результатам; open-ended анализируется **только если ответы уже tagged**; English; 1–10 000 responses; US Data Center. URL: https://help.surveymonkey.com/en/surveymonkey/analyze/analyze-with-ai/ — доступ 2026-08-31. Qualtrics Discover Topic Hierarchy Generator: AI строит topic model из unstructured data. URL: https://www.qualtrics.com/support/xm-discover/text-analytics/ai-assisted-text-analytics-in-xm-discover/ — доступ 2026-08-31.

### B) Alignment / preference elicitation

- **Принципы как явный «вопросник поведения» вышли из paper в living spec.** OpenAI Model Spec: living document; текущая публичная версия **v2026.08.18** (release notes 2026-08-18: teens relational interactions, false premises, «Be clear about capabilities and limits»). CC0. Chain of command: Root → System → Developer → User → Guideline. URL: https://model-spec.openai.com/2026-08-18.html , changelog https://github.com/openai/model_spec/blob/main/CHANGELOG.md , help https://help.openai.com/en/articles/9624314-model-release-notes — доступ 2026-08-31.
- **Deliberative alignment (2024-12, применён к o-series): модель *читает spec и рассуждает по нему*, а не только учится на labels.** OpenAI: «first approach to directly teach a model the text of its safety specifications and train the model to deliberate over these specifications at inference time»; в отличие от RLHF/CAI, где spec используется только для генерации training labels. Paper: arXiv:2412.16339. Blog: https://openai.com/index/deliberative-alignment/ — доступ 2026-08-31 (полный HTML blog на WebFetch timeout; сниппеты WebSearch + arXiv abstract верифицированы).
- **Constitutional AI остаётся механизмом principles → self-critique → RLAIF, не Typeform.** Bai et al., arXiv:2212.08073 (2022-12): constitution (~16 принципов в paper) → critique/revision (SL) → AI pairwise labels (RL). Anthropic 2023-05-09 публикует принципы Claude; **2026-01-21** — новая constitution («written primarily for Claude», объясняет *why*, не только *what*; CC0 PDF). URL: https://arxiv.org/abs/2212.08073 , https://www.anthropic.com/research/claudes-constitution , https://www.anthropic.com/news/claude-new-constitution — доступ 2026-08-31 (news-страница WebFetch timeout; research-страница с update 2026-01-21 получена).
- **Collective Constitutional AI: публичный vote (Polis) → constitution → CAI training.** ~1000 US adults, 1127 statements, 38 252 votes. URL: https://www.anthropic.com/news/collective-constitutional-ai-aligning-a-language-model-with-public-input — доступ 2026-08-31. Это elicitation принципов у *публики исследователями*, не machine-to-machine packet без researcher.
- **Eval harness стал «вопросником поведения» поверх spec.** OpenAI Model Spec Evals (март 2026): 596 prompts, 225 focus areas, grader GPT-5 Thinking, score 1–7 → binary compliance (6–7 = compliant). URL: https://alignment.openai.com/model-spec-evals/ — доступ 2026-08-31. Anthropic Bloom (декабрь 2025): researcher задаёт *одно поведение*, пайплайн Understanding → Ideation → Rollout → Judgment генерирует suite. URL: https://www.anthropic.com/research/bloom и https://alignment.anthropic.com/2025/bloom-auto-evals/ — доступ 2026-08-31. Совместный alignment eval Anthropic–OpenAI, лето 2025, публикации 2025-08-27. URL: https://alignment.anthropic.com/2025/openai-findings/ и https://openai.com/index/openai-anthropic-safety-evaluation/ — доступ 2026-08-31.
- **Active preference learning — про *какие пары спрашивать*, не про «12 открытых вопросов Owner».** BAL-PM (arXiv:2406.10023, 2024): −33%…−68% labels vs random. Active Learning for DPO (arXiv:2503.01076, 2025-03). Nearly Optimal Active Preference Learning (arXiv:2602.01581, 2026-02): informative = near-ties. Это sampling policy над pairwise, не дизайнерский опросник.
- **LLM-as-judge ≠ сбор предпочтений.** Surveys 2024–2025 (arXiv:2412.05579, arXiv:2411.15594): LLM *оценивает* уже существующие выходы. Agent-as-a-Judge survey (arXiv:2601.05111, 2026-01). DPO (Rafailov et al., NeurIPS 2023) — алгоритм *обучения* на уже собранных pairwise; **не механизм elicitation**. В каталоге — только как граница (QE-B-10).

### C) Агентские экосистемы

- **HITL фреймворков — pause/resume на *пакете действия*, не standing operator.** LangGraph `interrupt()` + checkpointer + `Command(resume=…)` — официальные docs 2026. URL: https://docs.langchain.com/oss/python/langgraph/interrupts — доступ 2026-08-31. OpenAI Agents SDK: `needs_approval` → `RunResult.interruptions` → `RunState.approve/reject`. URL: https://openai.github.io/openai-agents-python/human_in_the_loop/ — доступ 2026-08-31. CrewAI: `human_input=True` на Task; Enterprise resume webhook. URL: https://docs.crewai.com/edge/en/learn/human-input-on-execution и https://docs.crewai.com/v1.15.17/en/learn/human-in-the-loop — доступ 2026-08-31. Microsoft: AutoGen в maintenance mode; HITL first-class в Agent Framework (`RequestPort` / `ctx.request_info`). URL: https://github.com/microsoft/AutoGen и https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ — доступ 2026-08-31.
- **MCP tool surface сам является вопросником полномочий.** Spec 2026-07-28: tools model-controlled; «SHOULD always be a human in the loop with the ability to deny»; hosts MUST obtain explicit user consent before invoking any tool; `tools/list` MAY vary by authorization/scopes; появился `InputRequiredResult` + `elicitation/create` (mode: form) — протокол умеет *запросить форму* до завершения tool call. URL: https://modelcontextprotocol.io/specification/2026-07-28/server/tools — доступ 2026-08-31.
- **Memory-profile агента сериализуется как блоки, не как 12 open questions.** Letta AgentFile `.af`: system prompt, memory blocks (persona / human), tool rules, tools+schemas. Docs: блок = label + description + value + limit; `human` и `persona` — рекомендованный минимум. URL: https://docs.letta.com/v1-sdk/concepts/agent-file/ и https://docs.letta.com/guides/core-concepts/memory/memory-blocks/index.md — доступ 2026-08-31. Это **не** идентичность AICM; публичный формат portable state.
- **Eval-as-questionnaire агента:** AgentBench (THUDM, ICLR 2024; FC-версия 2025-10-10) — 8 interactive environments как тест «умеет ли агент». URL: https://github.com/THUDM/AgentBench/ — доступ 2026-08-31. Не путать с одноимённым CI-фреймворком `1304674612/agentbench` (2026) — другой продукт.

---

## 2. Каталог механизмов

Для каждого: что это; кто уже делает; URL; **что AICM может взять частично** (копируемо / адаптируемо / не брать). Привязка «взять» к рамке: Owner = External Enabler; L0–L2 закрыты; packet-approval вместо 12 открытых вопросов; нет человека-дизайнера в петле.

### Слой A — продукты опросников

#### QE-A-01. Синтез вопросника из промпта / документа (builder, не interviewer)

**Что это.** LLM генерирует *статический* драфт формы (типы вопросов, формулировки). Классический branching, если появляется, — либо заранее заданный skip-logic, либо «AI написал правила один раз». Это не live follow-up.

**Кто делает (верифицировано).**
- Google Forms Gemini «Help me create»: промпт или Drive-файл → драфт. Не редактирует текущую форму, не делает multi-section. https://support.google.com/docs/answer/16346789 — 2026-08-31.
- SurveyMonkey Build with AI: промпт до 50 000 символов, до 25 генераций/час; Azure OpenAI / OpenAI; список типов (MC, checkbox, NPS, matrix, ranking…). https://help.surveymonkey.com/en/surveymonkey/create/build-with-ai/ — 2026-08-31.
- Tally AI (с 2026-07-08 для всех планов, включая free): промпт → вопросы + logic + formulas; upload screenshot/PDF для recreate; chat-правка существующей формы. https://tally.so/help/free-ai-form-builder — 2026-08-31.
- Fillout AI Form Generator: description / paste questions / Google Form / PDF → форма; далее no-code editor. Маркетинговая страница: https://www.fillout.com/ai-form-builder — 2026-08-31. Help по *respondent* follow-up **не найден** (есть AI actions на submissions: summarize/classify/generate/extract — https://www.fillout.com/help/ai-workflows).
- Typeform AI: chat в builder — create/edit/reorder, branching rules, translate, upload context files, web search for company context, memory о компании. Сниппеты help: https://help.typeform.com/hc/en-us/articles/14955071444244 — 2026-08-31 (Cloudflare на полный fetch).

**Реальное vs маркетинг.** «AI builds your form in seconds» = драфт вопросов. Не доказано (и не следует утверждать), что builder сам ведёт адаптивное интервью респондента.

**AICM.** *Адаптируемо:* пакетный синтез **domain-constraint questionnaire** из vendor spec / tool schema / регламента вертикали → черновик packet, не live-опрос Owner. *Не брать:* перманентный «дизайнер форм» в петле Owner; SaaS-стартап опросников.

#### QE-A-02. Классический adaptive branching (skip-logic), не LLM-интервью

**Что это.** Заранее заданные if/then. Не путать с conversational survey.

**Кто делает.** Typeform Logic Jump / branching (AI *может сгенерировать rules* в builder — QE-A-01). Tally conditional logic + calculated fields (changelog 2026-07-14 redesign). Fillout conditional logic / conditional integrations. Qualtrics display logic поверх Conversational Feedback. Google Forms: Gemini **не** генерирует сложную секционную логику (официальный лимит).

**AICM.** *Копируемо как идея freeze:* закрытые L0–L2 = уже «замороженный branching» канона. Новый branching — только для **новой вертикали** как отдельный packet, не reopen L0–L2. *Не брать:* бесконечную ручную настройку логики Owner-ом.

#### QE-A-03. Capped LLM follow-up (1–2) на open-ended

**Что это.** После текстового ответа модель генерирует ограниченное число уточнений. Это **не** полный interviewer: глубина фиксирована, гайд почти не существует.

**Кто делает.**
- Qualtrics Adaptive follow-up: 1 (basic) или до 2 (advanced); topics to avoid; языки listed; 2 advanced follow-ups max *на респондента на опрос*; GPT-4o/Azure для advanced/non-English. https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/conversational-feedback/ — 2026-08-31.
- Typeform Clarify with AI: max 2; данные уходят third-party AI (Anthropic per FAQ). https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI , https://help.typeform.com/hc/en-us/articles/33777155298708-AI-with-Typeform-FAQ — 2026-08-31.

**Маркетинг, отказанный как факт.** Qualtrics article «What Your Customers Meant to Say» утверждает lift в исследованиях вендора — **не принято как универсальный empirical result** без независимой репликации. Typeform homepage «conversational questions» = UX one-question-at-a-time + capped clarify, не LLM-интервьюер.

**AICM.** *Адаптируемо:* при contradiction audit — максимум 1–2 уточнения к **уже закрытому** канону (не новые PREF). *Не брать:* открытый диалог с Owner как постоянный HITL.

#### QE-A-04. Полноценный conversational LLM-interviewer (multi-turn до objective)

**Что это.** Есть discussion guide / Conversation Objective; модель сама генерирует follow-ups в реальном времени, пока цель не закрыта; глубина конфигурируется. Отличие от QE-A-03: не «+1–2», а сессия.

**Кто делает.**
- Specific.app: вопросы статичны по формулировке, follow-ups динамические (GPT); guardrails («don't ask about discounts»), max depth, tone; in-product widget или landing page. https://www.specific.app/llms.txt , https://specific.app/automatic-ai-follow-up-questions/ — 2026-08-31. Это **реальный conversational survey**, не skip-logic.
- Recollective Conversation Task: Objective задаёт goal/tone/probes; AI заканчивает, когда objective met; Text или Talk; resume mid-conversation. https://helpdesk.recollective.com/article/480-task-type-conversation , https://helpdesk.recollective.com/article/477-writing-conversation-objectives — 2026-08-31.
- Outset: AI 1:1 text/voice/video; researcher задаёт guide, probing depth, skip; Abyss Mode — до 10 layered follow-ups на вопрос (changeblog 2026-05-13). https://outset.ai/resources/faq , https://outset.ai/resources/changeblog/abyss-mode — 2026-08-31.
- Listen Labs: AI moderator + follow-ups; Study Composer; configurable follow-up count per question (2026-08-18 changelog). https://listenlabs.ai/whatsnew — 2026-08-31.
- Discuss.io Interview Agent (press 2025-02-27): AI-led IDI 24/7, native language; Q4 2025 — customization voice/tone/probing. https://www.discuss.io/press/spring-release-2025/ , https://www.discuss.io/press/discuss-closes-2025-with-major-innovations-following-its-merger-announcement-with-voxco/ — 2026-08-31.
- TheySaid: AI moderator «Evo», follow-up after every response, voice both sides. https://www.theysaid.io/ai-interviews — 2026-08-31.
- Glaut: AI-moderated voice interviews + classic surveys, 50+ languages. https://glaut.com/ — 2026-08-31.

**Маркетинг, отказанный как факт.** Listen Labs «90%+ accuracy», «30 million verified respondents», «under 24 hours consultant-quality» — vendor self-report / articles, не независимый benchmark. Outset «1.1B+ participants», «500K+ interview hours», «Visual Intelligence first-to-market» — vendor copy; факт продукта = AI-moderated interviews + configurable probing (FAQ/changeblog). Recollective «authentic, human-like» — слоган.

**AICM.** *Адаптируемо:* **агент опрашивает другой агент / tool spec / vendor changelog** по Conversation Objective («закрой противоречия до packet»). *Копируемо частично:* Conversation Objective как формат packet (цель, тон, evidence gates, когда STOP). *Не брать:* рынок qual-research SaaS; человека-модератора как роль; открытый interviewer к Owner.

#### QE-A-05. Voice / video interviewer + transcription/themes

**Что это.** Модальность сбора (голос/видео) + ASR + theme. Модерация может быть QE-A-03 или QE-A-04.

**Кто делает.** Voiceform: voice/video + AI probing + embed в чужие survey tools; 50 languages на homepage. https://www.voiceform.com/ , https://www.voiceform.com/ai-interviews — 2026-08-31. Listen Labs voice interviewer 42 languages (2026-02-06), interviews 120+ languages (2026-07-02). Outset FAQ: 40+ languages, text/voice/video.

**AICM.** *Не брать как продукт.* Голос Owner не нужен: elicitation идёт текстом/спекой. Voice имеет смысл только если вертикаль сама голосовая (не текущий trading-proof).

#### QE-A-06. Кластеризация / темы open-ended (post-hoc)

**Что это.** NLP/LLM кодирует уже собранные ответы в themes. Это **не** сбор предпочтений.

**Кто делает.** Typeform Smart Insights (topics + sentiment; ≥10 responses; English; Claude 3.5 Sonnet private copy). SurveyMonkey Thematic Analysis (в AI Analysis Suite; Analyze with AI требует tags). Qualtrics Text iQ / Discover Topic Hierarchy Generator (Claude 4.5 Sonnet per AI Administration table). Recollective Ask AI: Standard / MultiProject / Predictive modes, answers grounded in verbatims. https://helpdesk.recollective.com/article/425-introduction-to-ask-ai — 2026-08-31.

**AICM.** *Адаптируемо:* contradiction audit по логам агентов и пакетам — cluster расхождений, не новые вопросы Owner. *Не брать:* Predictive Mode Recollective как «предсказание предпочтений Owner» (это гипотезы по qual data, не канон).

#### QE-A-07. Chat-with-results (LLM-аналитик над датасетом)

**Что это.** NL-запросы к уже собранным ответам.

**Кто делает.** SurveyMonkey Analyze with AI (ограничения: English, tagged open-ends, не отвечает про logic/branching, 20/50/unlimited prompts по плану). Specific «chat with GPT about responses». Typeform Ask AI (homepage featureList; полный help fetch Cloudflare). Recollective Ask AI. Listen Research Agent (2026-02-11): segmented analysis, significance testing, slides; output traceable to responses.

**AICM.** *Адаптируемо:* чат по **канону + логам**, не по «новым 12 вопросам». *Не брать:* замену packet-approval разговором с Owner.

#### QE-A-08. Экспорт в schema / MCP tool surface

**Что это.** Форма или исследование становится tool для LLM-клиента: create/edit/analyze без UI.

**Кто делает.** Typeform MCP (`forms-*`, `insights-*`). Tally MCP + ChatGPT app + Claude connector (2026-08-27). Listen Labs MCP (2026-05-21) + public API create/launch study (2026-07-13, self-recruitment). Fillout REST/webhooks (не MCP — не утверждать MCP).

**AICM.** *Копируемо:* вертикальный vendor/tool должен отдавать **машиночитаемый questionnaire/schema**, который агент заполняет/проверяет. Это прямой путь к agent-to-agent questionnaire. *Не брать:* зависимость от чужого SaaS MCP как идентичности.

#### QE-A-09. Response-quality / clarity gate

**Что это.** Модель классифицирует ответ как vague/partial/gibberish и просит дописать — один раз.

**Кто делает.** Qualtrics Response clarity validation: 5 критериев (partial, too general, not insightful, lacks details, unintelligible); max 1 prompt per question. SurveyMonkey Response Quality (упоминается в curiosity-посте вендора как часть AI Analysis Suite) — **детальная схема критериев на help не выгружена в этой сессии**; факт наличия фичи на маркетинговом посте не развёрнут в процедуру. Listen: Quality Guard / response quality score (vendor articles + changelog 2026-07-09 учитывает file upload) — детали алгоритма «не найдено» на независимом источнике.

**AICM.** *Адаптируемо:* gate на **пакет** (неполный packet → отказ, не 12 follow-up вопросов). *Не брать:* вечный «уточни у Owner».

#### QE-A-10. Survey-as-quiz / answer key (не elicitation)

Google Forms quiz generation (2026-07-30) автоматически ставит correct answers + points. Это **проверка знания**, противоположность preference elicitation.

**AICM.** *Не брать* как метод предпочтений. *Адаптируемо* только как eval harness: «агент проходит quiz по канону» = behavioral questionnaire (слой C), не опрос Owner.

### Слой B — alignment / preference elicitation

#### QE-B-01. Constitutional principles → self-critique / RLAIF

**Что это.** Человек (лаборатория) пишет короткий список принципов. Модель критикует и переписывает свои ответы (SL), затем AI ставит pairwise labels (RLAIF). Human labels на harmfulness в paper = 0; helpfulness labels ещё human.

**Кто:** Anthropic CAI, arXiv:2212.08073. Публичные принципы 2023-05-09; новая constitution 2026-01-21. https://arxiv.org/abs/2212.08073 , https://www.anthropic.com/research/claudes-constitution — 2026-08-31.

**Не путать с Typeform.** CAI не собирает ответы пользователей формы; это training-time questionnaire *модели к самой себе*.

**AICM.** *Адаптируемо:* канон L0–L2 уже играет роль constitution. Новый текст принципов для **новой вертикали** пишет система, Owner ратифицирует packet целиком (External Enabler), не составляет принципы по одному. *Не брать:* «давайте перепишем constitution с Owner в Typeform».

#### QE-B-02. Collective / deliberative public input (Polis → constitution)

**Что это.** Crowd vote Agree/Disagree/Pass по statements; ML кластеризует opinion groups; statements → constitution → CAI.

**Кто:** Anthropic + Collective Intelligence Project. https://www.anthropic.com/news/collective-constitutional-ai-aligning-a-language-model-with-public-input — 2026-08-31.

**AICM.** *Не брать как процедуру для Owner* (это массовый демократический input, противоположность closed canon + External Enabler). *Лабораторная гипотеза (не продукт-факт 2025):* agent-to-agent vote по statements внутри системы (несколько агентов-ролей) с freeze после consensus — без публики и без Owner-as-voter.

#### QE-B-03. Pairwise preferences (Bradley–Terry / RLHF labels)

**Что это.** Сравнение двух выходов: A лучше B. Относительное сравнение надёжнее абсолютного скора (стандарт RLHF).

**Кто:** InstructGPT/RLHF линия; CAI RL-stage использует тот же формат, но labels от AI. OpenAI/Anthropic evals часто pairwise или rubric, не «напишите эссе предпочтений».

**AICM.** *Копируемо:* когда системе нужно разрешить конфликт двух пакетов/политик — **парное сравнение**, не 12 open questions. Owner, если вообще участвует, видит два готовых пакета: approve A / approve B / reject both. *Не брать:* разметку тысяч пар человеком-оператором.

#### QE-B-04. Active learning / uncertainty sampling над парами

**Что это.** Алгоритм выбирает, какую пару спросить, чтобы сократить число меток.

**Кто:** BAL-PM arXiv:2406.10023 (2024); Active Learning for DPO arXiv:2503.01076 (2025); Nearly Optimal Active Preference Learning arXiv:2602.01581 (2026-02). Интуиция 2026-paper: informative = near-ties.

**AICM.** *Адаптируемо:* contradiction audit спрашивает систему (или, редко, Enabler) **только в зоне неопределённости**, не весь канон. L0–L2 не reopen; sampling только по новым вертикальным constraints. *Не брать:* «давайте ещё одну анкету, вдруг что-то изменилось».

#### QE-B-05. LLM-as-judge (оценка, не elicitation)

**Что это.** Модель-судья скорит/ранжирует выходы по рубрике. Это замена annotator, не замена источника предпочтений.

**Кто:** surveys arXiv:2412.05579, arXiv:2411.15594; OpenAI Model Spec Evals grader; Bloom Judgment stage; Qualtrics/Typeform theme models — родственный post-hoc judge.

**AICM.** *Адаптируемо:* судья по **замороженному канону** (пакет соответствует L0–L2?). *Не брать:* судью, который *изобретает* новые PREF. Источник нормы — закрытая карта + packet-approval, не мнение судьи.

#### QE-B-06. Model Spec как living principles-questionnaire

**Что это.** Иерархия инструкций + явные clauses. Conflict resolution встроена (chain of command). Spec публичен, CC0, версионируется.

**Кто:** OpenAI Model Spec, latest **2026-08-18**. https://model-spec.openai.com/2026-08-18.html — 2026-08-31.

**AICM.** *Копируемо как формат:* канон = spec с chain of command (не 12 вопросов). Версионирование spec ≠ reopen L0–L2: новый vertical spec — отдельный документ, наследует закрытый core. *Не брать:* «living spec», который Owner правит каждую неделю как дизайнер.

#### QE-B-07. Deliberative alignment: reason over written spec at inference

**Что это.** SFT на CoT, где модель цитирует spec; затем RL. Spec дают модели *в текст*, не только в labels. OpenAI применяла к o-series.

**Кто:** arXiv:2412.16339; https://openai.com/index/deliberative-alignment/ ; o1 System Card. 2026-08-31.

**AICM.** *Адаптируемо:* агент перед действием **читает канон и пакет** и пишет короткий CoT соответствия — это и есть questionnaire без человека. *Не брать:* требование human-written CoT (paper специально избегает этого).

#### QE-B-08. RLAIF (AI preference labels)

**Что это.** Labels pairwise ставит модель по principles, не crowd.

**Кто:** часть CAI; Google RLAIF vs RLHF (Lee et al., цитируется в survey arXiv:2407.16216); survey RL-enhanced LLMs arXiv:2412.10400.

**AICM.** *Адаптируемо:* внутренние предпочтения «какой пакет безопаснее относительно канона» ставит судья, Owner не лейблит. *Не брать:* полную замену канона «тем, что сказал GPT».

#### QE-B-09. Eval harness как behavioral questionnaire

**Что это.** Набор промптов/рубрик = вопросы к модели: «как ты себя ведёшь в ситуации X». Измеряет adherence, не спрашивает человека «как тебе жить».

**Кто:** Model Spec Evals (596 prompts, март 2026) https://alignment.openai.com/model-spec-evals/ ; Bloom (дек 2025) https://www.anthropic.com/research/bloom ; joint Anthropic–OpenAI alignment evals 2025-08; AgentBench ICLR 2024.

**AICM.** *Копируемо:* каждый packet вертикали сопровождается eval-вопросами к агенту («нарушает ли L0?»). Это questionnaire *агента*, не Owner. *Не брать:* Bloom-пайплайн, где researcher вручную seed-ит каждое новое поведение как постоянная роль (в AICM researcher ≠ Owner, и даже lab-researcher не должен стать standing дизайнером).

#### QE-B-10. DPO — граница: training, не elicitation

Rafailov et al., NeurIPS 2023: прямой лосс на уже собранных pairwise. Не метод спросить предпочтения. **Не брать как elicitation.** Упоминается, чтобы не склеить «DPO = опросник».

### Слой C — агентские экосистемы

#### QE-C-01. Memory-profile / onboarding blocks (не анкета Owner)

**Что это.** Структурированные слоты (persona, human, custom), которые агент сам читает/пишет. Description блока = инструкция, *как* писать в слот.

**Кто:** Letta memory blocks + AgentFile `.af`. https://docs.letta.com/v1-sdk/concepts/agent-file/ — 2026-08-31. Не идентичность AICM.

**AICM.** *Адаптируемо:* профиль вертикали = набор **закрытых слотов** (constraints, allowlist, eval IDs), заполняемых агентом из spec вендора. Onboarding = импорт `.af`-подобного пакета, не интервью Owner. *Не брать:* «расскажите о себе в 12 полях» как продукт для человека.

#### QE-C-02. Interrupt / packet-approval (HITL как ратификация пакета, не оператор)

**Что это.** Граф/раннер **останавливается** на конкретном действии; внешний субъект отвечает approve/edit/reject; состояние сериализуется.

**Кто:**
- LangGraph `interrupt()` — payload JSON-serializable; resume `Command(resume=…)`; checkpointer. https://docs.langchain.com/oss/python/langgraph/interrupts — 2026-08-31.
- OpenAI Agents SDK `needs_approval` + `RunState`. https://openai.github.io/openai-agents-python/human_in_the_loop/ — 2026-08-31. Сторонние блоги отмечают: нет built-in timeout/escalation/notification — это **не** в официальном SDK как фича; не утверждать обратное.
- CrewAI `human_input=True`; Enterprise `POST /resume` с `is_approve` + `human_feedback`. https://docs.crewai.com/edge/en/api-reference/resume — 2026-08-31.
- Microsoft Agent Framework: `RequestPort` / request-response; AutoGen Team этого не имел (maintenance). https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ — 2026-08-31.

**AICM.** *Копируемо:* **packet-approval** = один interrupt с готовым пакетом (diff канона, eval-результаты, allowlist). Owner/Enabler отвечает да/нет, не заполняет опросник. *Не брать:* standing HITL-operator; `human_input=True` на каждой задаче; CrewAI console prompt как роль человека в контуре.

#### QE-C-03. Tool allowlist / consent как questionnaire полномочий

**Что это.** Список tools + schema + «можно ли вызывать» = закрытый опросник возможностей. MCP: `tools/list` фильтруется scopes; consent UI; annotations untrusted.

**Кто:** MCP spec 2026-07-28. https://modelcontextprotocol.io/specification/2026-07-28/server/tools — 2026-08-31. OpenAI Agents SDK `require_approval` на MCP servers. LangGraph HITL middleware `interrupt_on` mapping tool → approve/edit/reject.

**AICM.** *Копируемо:* вертикаль = allowlist tools + schemas. Расширение домена = предложение нового allowlist-пакета, не «какие ещё вопросы задать Owner». *Не брать:* MCP-рекомендацию «always human in the loop» как standing operator AICM (для AICM human = редкий Enabler на packet, не deny каждой tool invocation).

#### QE-C-04. Протокольный elicitation form (MCP `elicitation/create`)

**Что это.** Tool call может вернуть `InputRequiredResult` с `elicitation/create`, `mode: "form"`, JSON Schema полей. Это **машинный опросник внутри протокола**.

**Кто:** MCP spec 2026-07-28, раздел Input Required Tool Results. Пример в spec: form «GitHub username». https://modelcontextprotocol.io/specification/2026-07-28/server/tools — 2026-08-31.

**AICM.** *Копируемо:* агент, упираясь в нехватку constraint, запрашивает **схему**, не эссе. Если схема касается канона — заполняет сам из L0–L2. Если новая вертикаль — собирает packet и идёт на QE-C-02. *Не брать:* прокидывание каждой elicitation-формы Owner-у.

#### QE-C-05. Agent eval environments как «умеешь ли ты»-вопросник

AgentBench (OS, DB, KG, WebShop, …) — интерактивные задачи. Bloom — propensity behaviors. Model Spec Evals — adherence clauses.

**AICM.** *Адаптируемо:* перед допуском агента в вертикаль — eval packet (не интервью человека). *Не брать:* путаницу с коммерческим CI-продуктом «AgentBench» 2026 (`1304674612/agentbench`) как с ICLR-бенчмарком.

#### QE-C-06. Сериализация агента (checkpoint / `.af`) как freeze профиля

Letta `.af` = portable state including memory blocks and tool rules. LangGraph checkpointer = freeze на interrupt. OpenAI `RunState.to_json`.

**AICM.** *Копируемо:* канон + vertical packet версионируются как файл состояния, который можно eval-ить изолированно (Letta Evals: agent_file как target). *Не брать:* Letta/MemGPT как «AICM identity».

#### QE-C-07. Multi-agent HITL паттерны (публичные docs only)

CrewAI / LangGraph / MAF — см. QE-C-02. AutoGen: официально maintenance; HITL там был workaround.

**AICM.** Использовать только как **публичные паттерны pause/resume**. Не внедрять Hermes, не live trading, не keys, не GitHub write.

#### QE-C-08. Agent-to-agent questionnaire *(лабораторная гипотеза, не продукт-факт 2025)*

Ни один найденный вендор не продаёт «агент официально интервьюирует другого агента как qualified interviewer без researcher». Ближайшие *реальные* куски: MCP tools/list + elicitation form; Typeform/Tally/Listen MCP (агент *строит* исследование, не опрашивает агента); Bloom (агент генерирует eval scenarios); Model Spec Evals (агент-grader судит агента).

**AICM.** Склеить QE-A-04 (Conversation Objective) + QE-B-07 (reason over spec) + QE-C-04 (schema elicitation) + QE-C-02 (packet-approval). Цель: агент-исследователь опрашивает агента-вендора/tool/другой инстанс, собирает contradiction report, выпускает packet. Owner не в петле, пока packet не готов к да/нет.

---

## 3. Не брать (отдельный раздел)

- **HITL-operator как standing role.** LangGraph/CrewAI/Agents SDK HITL — пауза на действии, не вакансия «человек в смене». В AICM даже эта пауза — только Enabler на packet, не оператор рынка.
- **Owner-as-designer.** Синтез вопросов, constitution, discussion guide, eval seed — не работа Owner. Owner ратифицирует готовый packet.
- **Reopen закрытых L0–L2.** Ни QE-A-*, ни QE-B-*, ни QE-C-* не дают права изобретать PREF ID или возвращать 18 сессий в работу.
- **Questionnaire как permanent human-in-the-loop.** Capped follow-up и AI interviewers рынка заточены на *респондента-человека*. Для AICM респондент по умолчанию — система/агент/спека.
- **OPEN-19 → homework Owner.** Открытый хвост не превращается в новую анкету «пожалуйста, ответьте ещё».
- **Стать survey SaaS startup.** Typeform/Qualtrics/Listen/Outset — чужой рынок CX/qual. AICM не продаёт опросники.
- **Live trading / keys / Hermes / GitHub write.** Лаба не реализует Hermes; нет ключей; нет push.
- **LLM-as-judge как источник нормы.** Судья проверяет соответствие канону, не пишет канон.
- **DPO / RLHF pipeline как «метод спросить Owner».** Это training.
- **Collective Constitutional AI / Polis** как процедура для Owner или публики вокруг AICM.
- **Voice interviewers, панели 30M респондентов, стимулы, gift cards.** Не контур системы.
- **Predictive / synthetic users** (Listen roadmap «simulate your customers», Recollective Predictive Mode) — не канон предпочтений.
- **«Gemini 3 Deep Think in Forms»** (TeacherCast) — не найдено в официальных Google Workspace Updates / Help; **не факт**.
- **SurveyMonkey «Document-to-Survey» и «2 ML patents / Genius scoring engine»** — утверждения сторонних обзоров (Pragmatic Coders, Tekpon); на официальном help подтверждены Build with AI, Survey Genius completion-rate score, Analyze with AI. Патенты и PDF→survey **не верифицированы** → не факт.

---

## 4. Векторы расширения AICM

Не «стать стартапом опросов». Где *метод* вопросника помогает новой экономической вертикали или саморазвитию. Trading остаётся первым proof, не идентичностью.

### 4.1 Domain-constraint elicitation (адаптация QE-A-01 + QE-C-03 + QE-C-04)

Новая вертикаль = не «12 вопросов Owner», а проход агента по **машиночитаемой спеке** (MCP `tools/list` + JSON Schema + vendor docs). Агент собирает: какие tools, какие scopes, какие запреты, какие evals. Выход — packet allowlist. Источники-аналоги: MCP spec 2026-07-28; Typeform/Tally/Listen MCP как proof, что спека формы уже tool.

### 4.2 Contradiction audit (адаптация QE-A-06 + QE-B-04 + QE-B-05)

Кластеризация логов и пакетов (как Smart Insights / Ask AI / Analyze with AI, но внутри канона). Active learning выбирает только near-tie конфликты. LLM-judge скорит против L0–L2. Owner не участвует, пока нет несводимого конфликта **между пакетами**, тогда QE-C-02 (A vs B).

### 4.3 Packet-approval вместо 12 open questions (адаптация QE-C-02 + QE-B-03 + QE-B-06)

Формат: один документ (spec-diff + eval scores + allowlist + STOP-conditions). Ответ Enabler: approve / reject / approve-with-minor (без новых вопросов). Образец структуры — Model Spec clause + Model Spec Evals rubric, не Typeform.

### 4.4 Agent-to-agent questionnaire (QE-C-08, лабораторная гипотеза)

Агент-интервьюер с Conversation Objective (паттерн Recollective/Outset/Specific) опрашивает: (i) другой агент, (ii) MCP-сервер через elicitation form, (iii) vendor changelog. Follow-ups ограничены objective и каноном. Результат — packet, не транскрипт для Owner. **Это не 2025-продукт; ближайшие building blocks существуют (MCP elicitation, MCP form servers, Bloom, deliberative alignment).**

### 4.5 Vertical eval-as-gate (QE-B-09 + QE-A-10 как quiz-по-канону)

Перед деньгами в новой вертикали агент проходит behavioral questionnaire (как Model Spec Evals / AgentBench / Bloom). Fail = нет запуска, не «спросим Owner, что он имел в виду».

### 4.6 Freeze профиля вертикали (QE-C-06)

После approval пакет сериализуется (аналог `.af` + spec version). Дальнейшие изменения — новый packet, не правка закрытого слоя. L0–L2 не входят в этот цикл.

### 4.7 Где расширять домены (лабораторные гипотезы, помечены)

Не факты рынка опросников, а *куда метод переносится*:
- **Инфраструктура tools/MCP-вендоров** — самый evidential вектор: формы и studies уже MCP-tools в 2026.
- **Compliance / policy packs** — Model Spec / constitution показывают, что «как себя вести» кодируется текстом + eval, не интервью.
- **Qual-research SaaS, HR pulse, CX NPS** — чужие вертикали рынка A; **не** цель AICM.
- **Голос/видео-респонденты** — не брать.
- Trading остаётся proof; questionnaire-метод не делает AICM «биржевым опросником».

---

## Фишки лабы (Grok HQ)

Это **не** Hermes, **не** live, **не** новые пустые репо, **не** Foundation. Речь о расширении уже существующего исследовательского центра Grok-лабы. Слои A/B/C выше — рынок и papers; здесь — конкретные фишки на **уже существующие** роли и папки.

**Уже есть (не изобретать заново):** штаб (Stabschef) + Разведчик / Аналитик / Канонист / Картограф / Механик / Тестер / Твиттер; AICM-docs `shtab/` `razvedka/` `sverki/` `kanon/`; гигиена пн 09:00; суточный цикл пн–пт 10:00; X только чтение `@acapitalmanager`; L0–L2 закрыты.

**Внедрять в лабу (механизмы тренда, не продукты SaaS):** адаптивный съём с потолком follow-up; contradiction-flag; пакет-штамп вместо 12 открытых вопросов; agent-to-agent questionnaire между *существующими* ролями; реестр Knowledge Candidate (ID / provenance / копируемо|адаптируемо|не брать).

**Не внедрять:** HITL-оператор как смена; Владелец-как-дизайнер анкеты; плодить ботов без роли; открывать L0–L2; OPEN-19 как домашнее Владельцу; write в X; GitHub write из этого чата; Live/keys/Hermes.

ID фишек — `HQ-*`, не PREF и не замена `QE-*`. Каждая фишка: зачем / откуда тренд / куда легло бы / риск.

### HQ-01. Адаптивный съём пакета (потолок 1–2 уточнения)

**Зачем.** Brief штаба и пакет разведки не должны разворачиваться в 12 открытых вопросов Владельцу или в «интервьюера». Один Conversation Objective на пакет; если дыра в evidence — максимум 1–2 уточнения к **уже сданному** файлу, затем STOP и штамп.

**Откуда тренд.** Qualtrics Conversational Feedback: Adaptive follow-up 1–2, лимит «до 2 advanced follow-ups на респондента на опрос» — https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/conversational-feedback/ — 2026-08-31. Typeform Clarify with AI: «up to two» — https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI — 2026-08-31. Recollective Conversation Objective как STOP-условие сессии — https://helpdesk.recollective.com/article/477-writing-conversation-objectives — 2026-08-31.

**Куда легло бы.** Шаблон brief Stabschef (`shtab/`) + Разведчик пишет `razvedka/` одним файлом. Не новый бот. Твиттер не участвует (X read-only уже есть).

**Риск.** Скатиться в QE-A-04 (полноценный interviewer) и начать «уточнять у Владельца». Потолок 1–2 и STOP в brief — обязательный предохранитель. Не копировать Qualtrics Azure/GPT-4o как стек лабы.

### HQ-02. Contradiction-flag (fail-closed, L0–L2 не открывать)

**Зачем.** Новый Knowledge Candidate сверяется с закрытой картой и со `sverki/`. Флаг «противоречие» ≠ право reopen. Расхождение идёт в сверку, не в PREF.

**Откуда тренд.** Post-hoc темы/кластеры: Typeform Smart Insights — https://help.typeform.com/hc/en-us/articles/44393511518100-Smart-Insights-Qualitative-and-quantitative-analysis — 2026-08-31. LLM-as-judge как оценка *уже существующих* выходов, не источник нормы (arXiv:2412.05579, arXiv:2411.15594) — 2026-08-31. OpenAI Model Spec Evals: grader по clauses, score 1–7 → binary compliance — https://alignment.openai.com/model-spec-evals/ — 2026-08-31. Active preference: informative = near-ties (arXiv:2602.01581, 2026-02) — спрашивать только несводимое, не всё подряд.

**Куда легло бы.** Аналитик пишет флаг в `sverki/`; Картограф подтверждает, что L0–L2 не задеты; Канонист не открывает сессии. Гигиена пн 09:00 — очередь флагов, не генерация новых PREF.

**Риск.** Judge начинает *писать* канон. Ложный флаг создаёт давление reopen L0–L2. Лечение: флаг без ID PREF; reopen только именованным материальным противоречием (точный ID + источник + несовместимость) — это уже правило штаба, фишка его не меняет.

### HQ-03. Пакет-штамп вместо 12 открытых вопросов

**Зачем.** Цикл пн–пт 10:00 принимает или отклоняет **целый** файл `razvedka/`, не анкету. Ответ штаба: принять / отклонить / принять с minor. Владелец не дизайнер и не оператор.

**Откуда тренд.** LangGraph `interrupt()` + checkpointer + `Command(resume=…)` — пауза на *пакете действия*, не standing operator — https://docs.langchain.com/oss/python/langgraph/interrupts — 2026-08-31. OpenAI Agents SDK `needs_approval` → approve/reject — https://openai.github.io/openai-agents-python/human_in_the_loop/ — 2026-08-31. OpenAI Model Spec как living clauses + eval, не 12 эссе — https://model-spec.openai.com/2026-08-18.html — 2026-08-31.

**Куда легло бы.** Stabschef на суточном цикле; вход = файл в `razvedka/` (уже так архивируется). Не новый бот «Approver». Не HITL на каждый tool call (MCP SHOULD-HITL **не** копировать как смену оператора — см. QE-C-03).

**Риск.** Штамп превращается в «напиши ещё 12 пунктов». Owner втягивается как дизайнер пакета. Лечение: в brief явно «один файл, да/нет»; OPEN-19 не становится homework.

### HQ-04. Agent-to-agent questionnaire (только существующие роли)

**Зачем.** Слияние evidence (Разведчик ↔ Аналитик ↔ Механик/Тестер) идёт машиной по Conversation Objective, без Владельца в петле. Это **лабораторная гипотеза**, не найденный 2025-продукт (QE-C-08).

**Откуда тренд.** Building blocks, не готовый продукт: MCP `elicitation/create` mode form — https://modelcontextprotocol.io/specification/2026-07-28/server/tools — 2026-08-31. Bloom: researcher задаёт одно поведение, пайплайн сам строит suite — https://www.anthropic.com/research/bloom — 2026-08-31. Deliberative alignment: модель *читает spec и рассуждает* — arXiv:2412.16339, https://openai.com/index/deliberative-alignment/ — 2026-08-31. Recollective/Outset/Specific дают Objective + probing depth — как формат, не как SaaS в лабу.

**Куда легло бы.** Разведчик задаёт Objective в пакете; Аналитик отвечает сверкой; Механик — контуром-кандидатом; Тестер — replay-метрикой. Штаб штампует результат. **Не** Consilium, **не** новый «Интервьюер».

**Риск.** Выдать гипотезу за shipping-фичу. Плоднуть бота «модератор». Склеить слои стратегий через «общий опрос». Лечение: в пакете явно «гипотеза»; один brief = один контур; слои не клеить.

### HQ-05. Реестр Knowledge Candidate (ID / provenance / копируемо|не брать)

**Зачем.** Каждый пакет разведки уже почти реестр, но поля не стандартизованы. Нужна строка на единицу: ID (`QE-*` / `HQ-*` / корпус-якорь), URL+дата, статус копируемо | адаптируемо | не брать. Картограф не путает это с PREF.

**Откуда тренд.** OpenAI Model Spec: нумерованные clauses + changelog + CC0 — https://model-spec.openai.com/2026-08-18.html , https://github.com/openai/model_spec/blob/main/CHANGELOG.md — 2026-08-31. Форма как schema/MCP tool (Tally changelog, Typeform MCP) — https://tally.so/changelog , https://www.typeform.com/developers/get-started/mcp/ — 2026-08-31. Letta memory blocks: label + description + value + limit — https://docs.letta.com/guides/core-concepts/memory/memory-blocks/index.md — 2026-08-31. Не идентичность AICM; только форма слота.

**Куда легло бы.** Индекс `razvedka/` (обновляет штаб при архиве, как сейчас) + шапка каждого файла Разведчика. Картограф читает статус «не PREF». Канонист не импортирует QE в PREF.

**Риск.** QE-/HQ-ID просачиваются в карту предпочтений. Лечение: в шапке файла «не PREF»; реестр живёт в `razvedka/`, не в `kanon/`.

### HQ-06. Eval-harness как вопросник поведения Тестера (не live)

**Зачем.** Допуск контура = пройти quiz/eval по спеке Механика и канону, не «спросим Владельца, что он имел в виду». Replay vs baseline уже роль Тестера.

**Откуда тренд.** OpenAI Model Spec Evals (март 2026): 596 prompts, 225 focus areas — https://alignment.openai.com/model-spec-evals/ — 2026-08-31. Anthropic Bloom — https://www.anthropic.com/research/bloom — 2026-08-31. AgentBench (ICLR 2024; FC 2025-10-10) — https://github.com/THUDM/AgentBench/ — 2026-08-31. Google Forms quiz generation 2026-07-30 — проверка знания, не elicitation — https://workspaceupdates.googleblog.com/2026/07/use-gemini-in-google-forms-to-quickly-create-a-new-quiz.html — 2026-08-31. Использовать только как аналогию «answer key по канону».

**Куда легло бы.** Механик кладёт spec (вход/выход/метрики) в пакет; Тестер гоняет публичные данные vs baseline. Не live, не ключи, не Bitget.

**Риск.** Quiz как метод предпочтений Owner. Коммерческий CI «AgentBench» 2026 (`1304674612/agentbench`) спутать с ICLR-бенчмарком. Live-eval на деньги.

### HQ-07. Гигиена пн 09:00 = contradiction / provenance sweep

**Зачем.** Слот уже есть. Не плодить «аудитора». Понедельник 09:00 — очередь HQ-02 флагов, битые URL, пакеты без provenance, QE-ID в чужой папке.

**Откуда тренд.** Living spec с явным changelog: Model Spec v2026.08.18 + CHANGELOG — https://github.com/openai/model_spec/blob/main/CHANGELOG.md — 2026-08-31. Anthropic constitution update 2026-01-21 («written primarily for Claude») — https://www.anthropic.com/research/claudes-constitution — 2026-08-31. Смысл steal: периодический *аудит текста принципов*, не новая анкета людей.

**Куда легло бы.** Существующая гигиена пн 09:00; Картограф + Канонист read-only по `kanon/`; Разведчик чинит provenance в `razvedka/`. Суточный цикл 10:00 остаётся приёмкой пакетов (HQ-03), не дублирует гигиену.

**Риск.** Гигиена становится поводом reopen L0–L2 или «обновить constitution AICM». Лечение: в слоте явно «sweep, не amendment канона».

### HQ-08. Схема из спеки/MCP вместо интервью Владельца

**Зачем.** Новая вертикаль или tool-контур заполняется из машиночитаемой схемы (docs, `tools/list`, JSON Schema), не из 12 полей «расскажите о себе».

**Откуда тренд.** MCP spec 2026-07-28: `tools/list` MAY vary by scopes; `InputRequiredResult` + `elicitation/create` mode form — https://modelcontextprotocol.io/specification/2026-07-28/server/tools — 2026-08-31. Tally MCP beta 2025-07-11 + Claude/ChatGPT connectors 2026-08-27 — https://tally.so/changelog — 2026-08-31. Typeform MCP `forms-*` / `insights-*` — https://www.typeform.com/developers/get-started/mcp/ — 2026-08-31. Listen Labs MCP 2026-05-21 — https://listenlabs.ai/whatsnew — 2026-08-31. Google Forms «Help me create» = драфт из документа, не interviewer — https://support.google.com/docs/answer/16346789 — 2026-08-31.

**Куда легло бы.** Разведчик снимает schema в `razvedka/`; Механик превращает в контур-кандидат. Твиттер остаётся read-only `@acapitalmanager` — **не** расширять write. Не подключать чужой SaaS MCP как идентичность лабы.

**Риск.** Зависимость от Typeform/Tally/Listen как «дома» лабы. Прокидывание каждой elicitation-формы Владельцу (прямо запрещено в QE-C-04). Новые пустые репо «под MCP».

### Что из тренда в лабу не класть (явный стоп)

| Запрет | Почему здесь, а не «потом в Hermes» |
|---|---|
| HITL-оператор | Рынок (LangGraph/CrewAI/Agents SDK) даёт pause/resume на пакете. Смена «человек в контуре» убивает External Enabler и плодит роль без мандата. |
| Владелец-как-дизайнер анкеты | Builder-AI (QE-A-01) и constitution-writing — работа лаборатории, не Enabler. Owner = да/нет на готовый packet (HQ-03). |
| Плодить ботов без роли | Восемь ролей уже закрывают съём / сверку / канон / карту / контур / replay / X-чтение / штаб. «Интервьюер», «Approver», «Auditor» — дубли HQ-01/03/07. |
| Открывать L0–L2 | Ни одна фишка HQ-* не является материальным противоречием. OPEN-19 не анкета. |
| Новые пустые репо / GitHub write из разведки | Архив кладёт штаб в `Seryogapahom/AICM-docs`. |
| Voice/panel/CX SaaS, Polis, DPO-как-опрос | Слой A/B «не брать»; в лабу тем более. |

---

## 5. Пробелы

Чего продукты и papers 2025–26 **не дают** AICM.

- **Нет closed-canon freeze.** Все survey SaaS и CAI/Model Spec — living: вендор и lab бесконечно итерируют вопросы/принципы. Нет механизма «18 сессий, карта закрыта, stop».
- **Нет External-Enabler-only ratification.** HITL docs предполагают оператора, researcher, brand admin, crowdworker, teen-safety policy author. Никто не моделирует Owner, который *не дизайнер*.
- **Нет machine-to-machine preference packets без researcher.** Bloom, Model Spec Evals, CCAI, Listen MCP — везде человек задаёт seed, objective или spec. Автогенерация evals *после* seed — да; полный цикл без researcher — не найден.
- **Нет различения «предпочтение канона» vs «предпочтение респондента CX».** Рынок A оптимизирует completion rate и «deeper insights». Это другая функция потерь.
- **Нет packet-approval UX в survey tools.** Есть capped follow-up и 10-слойный probing — противоположность одному да/нет на пакет.
- **LLM-as-judge не калиброван как хранитель чужого закрытого канона.** Evals меряют adherence к spec *автора модели*, не к внешней замороженной карте третьей системы.
- **MCP SHOULD human-in-the-loop** конфликтует с автономным экономическим контуром; протокол не даёт «Enabler once per packet».
- **Export-to-spec слабый.** Формы экспортируются как формы/MCP tools, не как constitution + eval suite + allowlist одним пакетом.
- **Collective input (Polis) — про публику, не про закрытую систему.**
- **Voice/panel/recruitment** занимают большую часть 2026-changelog Listen/Outset — AICM это не нужно и маскирует полезное (objective, probing depth, MCP).

---

## Provenance: URL fetched vs not-found

Доступ ко всем строкам: **2026-08-31**. «Fetched» = содержимое страницы получено WebFetch или устойчивым сниппетом WebSearch по той же URL. «Not-found / blocked» = нет страницы, timeout, или Cloudflare.

### Получены (первичные или эквивалент)

| URL | Статус | Заметка |
|---|---|---|
| https://support.google.com/docs/answer/16346789 | fetched | Google Forms Gemini help |
| https://workspaceupdates.googleblog.com/2026/07/use-gemini-in-google-forms-to-quickly-create-a-new-quiz.html | fetched | quiz generation 2026-07-30 |
| https://help.surveymonkey.com/en/surveymonkey/create/build-with-ai/ | fetched | Build with AI |
| https://help.surveymonkey.com/en/surveymonkey/analyze/analyze-with-ai/ | fetched | Analyze with AI limits |
| https://help.surveymonkey.com/en/surveymonkey/create/survey-genius/ | search-snippet | Survey Genius = completion score, не LLM-interviewer |
| https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/conversational-feedback/ | fetched | Adaptive follow-up + clarity |
| https://www.qualtrics.com/support/survey-platform/sp-administration/artificial-intelligence-ai-administration/ | search-snippet | GPT-4o / Claude 4.5 Sonnet mapping |
| https://www.qualtrics.com/support/xm-discover/text-analytics/ai-assisted-text-analytics-in-xm-discover/ | search-snippet | Topic Hierarchy Generator |
| https://tally.so/help/free-ai-form-builder | fetched | Tally AI capabilities |
| https://tally.so/changelog | fetched | MCP 2025-07-11; Tally AI 2026-07-08; ChatGPT 2026-08-27 |
| https://www.fillout.com/help/ai-workflows | fetched | AI actions on submissions, не interviewer |
| https://www.fillout.com/ai-form-builder | search-snippet | AI form generator marketing page |
| https://www.specific.app/llms.txt | fetched | conversational survey anatomy |
| https://specific.app/automatic-ai-follow-up-questions/ | search-snippet | follow-up guardrails |
| https://www.specific.app/documentation/js-sdk/ | search-snippet | in-product SDK |
| https://www.voiceform.com/ | search-snippet | voice/video surveys |
| https://www.voiceform.com/ai-interviews | search-snippet | AI probing |
| https://listenlabs.ai/whatsnew | fetched | 2026 changelog MCP/Research Agent/languages |
| https://outset.ai/resources/faq | search-snippet | AI-moderated interviews, 40+ languages |
| https://outset.ai/resources/changeblog/abyss-mode | search-snippet | Abyss Mode 2026-05-13, up to 10 follow-ups |
| https://outset.ai/pricing | search-snippet | custom pricing, не used as capability claim |
| https://helpdesk.recollective.com/article/480-task-type-conversation | search-snippet | Conversation Task |
| https://helpdesk.recollective.com/article/477-writing-conversation-objectives | search-snippet | Conversation Objective |
| https://helpdesk.recollective.com/article/425-introduction-to-ask-ai | search-snippet | Ask AI, updated 2026-05-04 |
| https://www.discuss.io/press/spring-release-2025/ | search-snippet | Interview Agent 2025-02-27 |
| https://www.discuss.io/press/discuss-closes-2025-with-major-innovations-following-its-merger-announcement-with-voxco/ | search-snippet | Q4 2025 + Voxco merger |
| https://www.theysaid.io/ai-interviews | search-snippet | Evo moderator |
| https://glaut.com/ | search-snippet | AIMI voice interviews |
| https://arxiv.org/abs/2212.08073 | fetched | Constitutional AI paper |
| https://www.anthropic.com/research/claudes-constitution | fetched | 2023 principles + update 2026-01-21 |
| https://www.anthropic.com/news/collective-constitutional-ai-aligning-a-language-model-with-public-input | search-snippet | CCAI / Polis |
| https://model-spec.openai.com/2026-08-18.html | search-snippet | Model Spec current |
| https://github.com/openai/model_spec/blob/main/CHANGELOG.md | search-snippet | versions through 2026-08-18 |
| https://help.openai.com/en/articles/9624314-model-release-notes | search-snippet | Spec updates |
| https://openai.com/index/sharing-the-latest-model-spec/ | search-snippet | CC0, 2025-02 open-source |
| https://arxiv.org/abs/2412.16339 | search-snippet + pdf land | Deliberative Alignment paper |
| https://openai.com/index/deliberative-alignment/ | search-snippet (WebFetch timeout) | official blog |
| https://alignment.openai.com/model-spec-evals/ | fetched | Model Spec Evals, Mar 2026 |
| https://www.anthropic.com/research/bloom | search-snippet | Bloom |
| https://alignment.anthropic.com/2025/bloom-auto-evals/ | search-snippet | Bloom pipeline |
| https://alignment.anthropic.com/2025/openai-findings/ | search-snippet | joint evals |
| https://openai.com/index/openai-anthropic-safety-evaluation/ | search-snippet | joint evals OpenAI side |
| https://arxiv.org/abs/2412.05579 | search-snippet | LLMs-as-Judges survey |
| https://arxiv.org/abs/2411.15594 | search-snippet | LLM-as-a-Judge survey |
| https://arxiv.org/abs/2601.05111 | search-snippet | Agent-as-a-Judge survey |
| https://arxiv.org/abs/2406.10023 | search-snippet | BAL-PM |
| https://arxiv.org/abs/2503.01076 | search-snippet | Active Learning for DPO |
| https://arxiv.org/abs/2602.01581 | search-snippet | Nearly Optimal Active Preference Learning |
| https://arxiv.org/abs/2407.16216 | search-snippet | alignment techniques survey |
| https://arxiv.org/abs/2412.10400 | search-snippet | RL-enhanced LLMs survey |
| https://docs.langchain.com/oss/python/langgraph/interrupts | fetched | interrupt/resume |
| https://docs.langchain.com/oss/python/langchain/human-in-the-loop | search-snippet | HITL middleware |
| https://openai.github.io/openai-agents-python/human_in_the_loop/ | search-snippet | needs_approval |
| https://docs.crewai.com/edge/en/learn/human-input-on-execution | fetched | human_input=True |
| https://docs.crewai.com/v1.15.17/en/learn/human-in-the-loop | search-snippet | webhook HITL |
| https://docs.crewai.com/edge/en/api-reference/resume | search-snippet | resume API |
| https://github.com/microsoft/AutoGen | search-snippet | maintenance mode |
| https://learn.microsoft.com/en-us/agent-framework/migration-guide/from-autogen/ | search-snippet | MAF HITL vs AutoGen |
| https://modelcontextprotocol.io/specification/2026-07-28/server/tools | fetched | tools + elicitation/create |
| https://docs.letta.com/v1-sdk/concepts/agent-file/ | fetched | .af format |
| https://github.com/letta-ai/agent-file | search-snippet | AgentFile repo |
| https://github.com/THUDM/AgentBench/ | search-snippet | ICLR 2024 + FC 2025-10 |
| https://www.typeform.com/developers/get-started/mcp/ | search-snippet | Typeform MCP tools |
| https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI | search-snippet | max 2 follow-ups |
| https://help.typeform.com/hc/en-us/articles/33777155298708-AI-with-Typeform-FAQ | search-snippet | Anthropic for Clarify |
| https://help.typeform.com/hc/en-us/articles/44393511518100-Smart-Insights-Qualitative-and-quantitative-analysis | search-snippet | topics/sentiment |
| https://help.typeform.com/hc/en-us/articles/23542072977172-Get-AI-analysis-of-your-results-with-Smart-Insights | search-snippet | Claude 3.5 Sonnet private copy |
| https://www.surveymonkey.com/curiosity/next-gen-ai-features/ | search-snippet | AI Analysis Suite announcement |

### Не найдены / blocked / не верифицированы как capability

| Запрос / URL | Статус |
|---|---|
| https://help.typeform.com/hc/en-us/articles/14955071444244 (полный HTML) | WebFetch Cloudflare challenge; использованы search snippets |
| https://openai.com/index/deliberative-alignment/ полный HTML | WebFetch timeout; использованы search snippets + arXiv |
| https://www.anthropic.com/news/claude-new-constitution полный HTML | WebFetch timeout; факт 2026-01-21 подтверждён на research page |
| SurveyMonkey Document-to-Survey как официальная help-фича | не найдено на help.surveymonkey.com в этой сессии |
| SurveyMonkey «2 machine learning patents» | не найдено на vendor help; только сторонние обзоры |
| Google Forms «Gemini 3 Deep Think» | не найдено в Workspace Updates / official Help |
| Official Qualtrics «Discover conversational interviewer» (не topic model) | не найдено; Discover = text analytics / topic hierarchy |
| Fillout respondent-side LLM interviewer | не найдено; AI = builder + workflow actions |
| Tally respondent-side LLM follow-up | не найдено; AI = builder/edit/troubleshoot |
| Google Forms Gemini live follow-up / branching synthesis | официально не поддерживает multi-section; live interviewer не найден |
| Letta «onboarding questionnaire» product | не найдено; есть memory blocks + .af, не анкета |
| «Agent interviews another agent» as shipping product | не найдено |
| Pirate PDFs / paywalled full books | не запрашивались |
| Koji «best voice survey 2026» ranking | сторонний блог конкурента; не использован как факт |
| Strella / Conveo глубокие vendor docs | сравнение-страницы найдены; полные help capabilities кроме marketing tables не выгружались — **не расписывать как верифицированный каталог** |
| OpenAI Agents handbook HITL (отдельный «handbook») | не найдено как отдельный документ; есть Agents SDK HITL docs |

---

## Маркетинговые утверждения, отказанные как факт

1. Typeform «builds world-class forms» / «conversational questions» как LLM-интервьюер — нет: builder + UX one-at-a-time + Clarify max 2.
2. Qualtrics Adaptive Follow-Ups «transform listening at scale» / численный lift из vendor article — не принято как независимый result.
3. SurveyMonkey Genius «most complete AI survey platform in 2026» (Tekpon) — обзор, не vendor spec.
4. SurveyMonkey Genius «2 ML patents» / «question type prediction engine» — не подтверждено help.
5. SurveyMonkey «Document-to-Survey 2026» (Pragmatic Coders) — не подтверждено official help.
6. Listen Labs 90%+ accuracy, 30M verified respondents, 24h consultant-quality — vendor claims.
7. Outset 1.1B+ participants, 500K+ interview hours, «first-to-market Visual Intelligence» — vendor copy; не использовано как empirically verified.
8. Recollective «authentic human-like conversations» — слоган.
9. TeacherCast «Gemini 3 Deep Think in Google Forms» — не official.
10. GoFormz «Top AI Form Builders 2025» ranking — конкурент.
11. Discuss.io «10 billion tokens / only MR company in OpenAI 150» — vendor blog claim, не нужно AICM как capability.
12. Любые «AI interviewer = human moderator quality» без независимого бенчмарка.

Конец пакета. Knowledge Candidate only.
