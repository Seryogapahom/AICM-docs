# Knowledge Candidate: AI-экосистемы анкет (три несклеенных слоя)

**Статус: Knowledge Candidate. Не Foundation. Не канон AICM. Не PREF.**  
**Дата доступа: 2026-08-31**  
**Автор роли:** Разведчик (лаборатория Grok HQ).  
**Адресат:** штаб лаборатории Grok (research center). Не Hermes. Не live. Не торговый контур как личность.  
**ID карточек:** `QE-A-*` / `QE-B-*` / `QE-C-*` — идентификаторы Knowledge Candidate, **не** PREF. PREF-ID не изобретались. L0–L2 не трогать. GitHub пишет штаб. Владелец не вызывался. OPEN-19 не становится домашним заданием Владельца.
**Архив штаба:** [`razvedka/2026-08-31-ai-questionnaire-ecosystems.md`](2026-08-31-ai-questionnaire-ecosystems.md).

Три слоя **не склеивать** в один продукт «AI-анкета AICM»:

- **A)** коммерческие продукты сбора данных 2025–26;
- **B)** alignment / elicitation предпочтений (статьи и specs);
- **C)** agent-экосистемы (публичные доки памяти, eval, skills).

Каждый слой — отдельный каталог. Фишки лабы мапятся на **уже существующие** роли и папки, без новых ботов.

---

## 1. Шапка: что это / чем это НЕ является

**Что это.** Разведывательный пакет по экосистемам «вопрос → ответ → спецификация поведения». Для лаборатории: украсть *паттерны* (ветвление вместо 12 открытых вопросов; пакет-штамп вместо HITL-оператора; реестр кандидатов с provenance), не украсть *продукт* и не сделать Владельца дизайнером анкеты.

**Чем это НЕ является.**

- Это **не** PREF, не переоткрытие L0–L2, не домашняя работа Владельца, не OPEN-19-как-опросник.
- Это **не** стартап опросов и не «стать Typeform».
- Это **не** рекомендация ставить CrewAI / Letta / LangGraph / Qualtrics Experience Agents как идентичность AICM.
- Это **не** live-торговля и не Hermes.
- Слои A, B, C **не** являются одним продуктом. Совпадение слова «questionnaire» — путаница ярлыка.

Рамка лаборатории (не цитата вендора): опрос как постоянный человек-в-контуре запрещён. Гейт — пакет-штамп файла разведки, не 12 открытых вопросов Владельцу.

---

## 2. Тренды 2025–26 (реальный сдвиг vs маркетинг)

Каждый буллет — факт с URL. Маркетинг отделён.

1. **Синтез вопросов при *создании* формы стал commodity; LLM-интервьюер *во время* заполнения — нет.** Typeform AI, Tally AI, Fillout AI Form Builder, SurveyMonkey Build with AI, Gemini в Google Forms генерируют черновик формы из промпта. Это builder, не interviewer.  
   URL: https://www.typeform.com/ai/ · https://tally.so/help/free-ai-form-builder · https://www.fillout.com/help/ai-forms · https://www.surveymonkey.com/newsroom/surveymonkey-announces-ai-generated-surveys/ · https://support.google.com/docs/answer/16346789 · Дата доступа: 2026-08-31

2. **Адаптивное follow-up в формах узкое и зажато лимитами, не «конституция диалога».** Typeform Clarify with AI: максимум **две** уточняющие генерации после open-end; поведение AI **нельзя** кастомизировать; skip logic на сам Clarify **нельзя**. Qualtrics branching — классический Survey Flow (правила), не LLM. SurveyMonkey Advanced Branching — rule builder.  
   URL: https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI · https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/survey-flow-overview/ · https://help.surveymonkey.com/en/surveymonkey/create/advanced-branching/ · Дата доступа: 2026-08-31

3. **Настоящий LLM-интервьюер живёт в отдельном рынке qualitative research, не в form-builder.** Outset: AI-moderated interviews, smart follow-ups, synthesis; маркетинг «minutes / hours», не formal export-to-spec. Strella: AI-moderated interviews, probe deeper. Это **не** слой B (alignment) и **не** AICM-идентичность.  
   URL: https://outset.ai/platform · https://www.strella.io/ · Дата доступа: 2026-08-31

4. **Кластеризация ответов — NLP/темы, не «спека поведения».** Qualtrics Text iQ: topics, recommended topics, sentiment; отдельно Automated Text Analytics строит topic hierarchy. Typeform: Qualitative Analysis / Smart Insights (темы и sentiment). **Export-to-spec (constitution / Model Spec) как продукт — не найдено.**  
   URL: https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/text-iq/topics-in-text-iq/ · https://www.qualtrics.com/support/omnichannel-listening/text-analytics-xm/ai-powered-topic-models/ · https://www.typeform.com/ai/ · Дата доступа: 2026-08-31

5. **Alignment 2022–26, который ещё цитируют как практику: принципы *в тексте*, pairwise, LLM-as-judge, spec как опросник поведения модели.** Constitutional AI (Anthropic, 2022): конституция из ~16 принципов, RLAIF, без human labels на harm. Deliberative alignment (OpenAI, 2024): модель *читает* safety spec в CoT. Model Spec (2024-05-08 → 2026-08-18): принципы с уровнями власти. LLM-as-judge (Zheng et al., 2023): >80% agreement с людьми.  
   URL: https://arxiv.org/abs/2212.08073 · https://arxiv.org/abs/2412.16339 · https://cdn.openai.com/spec/model-spec-2024-05-08.html · https://model-spec.openai.com/2026-08-18.html · https://arxiv.org/abs/2306.05685 · Дата доступа: 2026-08-31

6. **Агенты: память = captured prefs; eval harness = questionnaire поведения; skills = onboarding-folder.** Letta/MemGPT: persona/human blocks в core memory. Anthropic Skills: «like putting together an onboarding guide for a new hire». LangSmith / OpenAI Evals: rubric + dataset. OpenAI Evals **deprecated**: read-only 2026-10-31, shutdown 2026-11-30. CrewAI: unified Memory, LLM infers scope.  
   URL: https://arxiv.org/abs/2310.08560 · https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills · https://docs.langchain.com/langsmith/llm-as-judge · https://developers.openai.com/api/docs/guides/evals · https://docs.crewai.com/edge/en/concepts/memory · Дата доступа: 2026-08-31

7. **Маркетинг «autonomous agent inside the survey» ≠ HITL-свободный контур.** Qualtrics Experience Agents: support docs — embed в survey flow к text-entry; ticketing actions **approved by a human agent before being sent/performed**. Маркетинг-страница пишет «act instantly» / «make-goods within guardrails». Не склеивать.  
   URL: https://www.qualtrics.com/support/experience-agents/experience-agents-overview/ · https://www.qualtrics.com/platform/experience-agents/ · Дата доступа: 2026-08-31

---

## 3. Каталог QE-*

Легенда статуса: **copyable** (факт/паттерн можно цитировать как есть) · **adaptable** (украсть идею в лабу, не продукт) · **не брать** (в контур AICM / на Владельца / как identity).

Слои не мержить.

### Слой A — продукты сбора (2025–26)

#### QE-A-01 — Typeform AI (builder + Clarify, не interviewer)

- **Что:** Промпт → форма; Retained Memory / Extended Thinking / File Uploads / Web Search / MCP; schema.org featureList: AI Form Builder, Ask AI, Qualitative/Quantitative Analysis, Clarify with AI. Clarify: до **двух** персонализированных уточнений после open-end; «you cannot directly customize the AI's behavior»; logic/skip на Clarify нельзя.
- **Кто:** Typeform S.L. (Barcelona).
- **URL:** https://www.typeform.com/ai/ · https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI · Дата доступа: 2026-08-31
- **Короткая цитата:** «The Clarify with AI question type uses generative AI to generate up to two personalized clarification questions based on your respondent's initial answer».
- **Статус:** **adaptable** (лимит follow-up + packet вместо бесконечного диалога) · **не брать** как продукт-идентичность и как HITL-интервьюер Владельца.
- **Реальное vs маркетинг:** «world-class forms at the drop of a prompt» — builder. Clarify — узкий probe, не constitutional interviewer. Skills / Landing Pages на странице — **Coming Soon** (не считать shipped).

#### QE-A-02 — Qualtrics Survey Flow + Branch Logic (правила, не LLM)

- **Что:** Survey Flow: branches, embedded data, randomizers, Text Sentiment–Topic branch, Experience Agent element. Branch Logic: условия на ответы / embedded data / Device / GeoIP / Quotas.
- **Кто:** Qualtrics.
- **URL:** https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/survey-flow-overview/ · https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/branch-logic/ · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (ветвление пакета вместо 12 open questions) · **не брать** как XM-платформу AICM.
- **Реальное vs маркетинг:** это зрелый rule engine. Не «LLM сам ведёт анкету».

#### QE-A-03 — Qualtrics Experience Agents (in-survey close-the-loop)

- **Что:** Agent Studio: Customer Service (embed в survey/website) и Ticketing. Survey agent цепляется к text-entry в Survey Flow; нужен New Survey Taking Experience. Ticketing: draft email / third-party / ticket actions — **approved by a human agent before** send/perform. Feature gated (pricing plan / Preview / implementation services).
- **Кто:** Qualtrics XM.
- **URL:** https://www.qualtrics.com/support/experience-agents/experience-agents-overview/ · https://www.qualtrics.com/platform/experience-agents/ · Дата доступа: 2026-08-31
- **Короткая цитата (support, не маркетинг):** «These are approved by a human agent before being sent to the customer.»
- **Статус:** **не брать** (HITL-оператор + live close-the-loop). Паттерн «агент внутри потока» — не копировать в Owner-контур.

#### QE-A-04 — Qualtrics Text iQ / Automated Text Analytics (кластеризация)

- **Что:** Text iQ: topics, recommended topics, hierarchical topics, sentiment (Advanced). Automated Text Analytics: «Let Qualtrics AI build it» — AI topic hierarchy. Text iQ и Automated Text Analytics **не** на одном поле одновременно (support).
- **Кто:** Qualtrics.
- **URL:** https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/text-iq/topics-in-text-iq/ · https://www.qualtrics.com/support/omnichannel-listening/text-analytics-xm/ai-powered-topic-models/ · Дата доступа: 2026-08-31
- **Статус:** **copyable** как факт «темы ≠ spec» · **не брать** как CX-стек лабы.
- **Пробел:** превращение тем в constitution / Model Spec — **не найдено**.

#### QE-A-05 — SurveyMonkey Genius / Build with AI

- **Что:** Newsroom 2023-10-25: Build with AI — часть линейки SurveyMonkey Genius®; GPT-3 + «20+ years of SurveyMonkey data»; генерация опроса из описания, бесплатно всем пользователям на дату анонса. Advanced Branching / Skip Logic — **rule-based**, не LLM-interviewer. Лендинг https://www.surveymonkey.com/mp/surveymonkey-genius/ — **fetch timeout 2026-08-31**; живые capabilities 2026 с этой страницы **не подтверждены**.
- **Кто:** SurveyMonkey (Momentive).
- **URL:** https://www.surveymonkey.com/newsroom/surveymonkey-announces-ai-generated-surveys/ · https://help.surveymonkey.com/en/surveymonkey/create/advanced-branching/ · Дата доступа: 2026-08-31
- **Статус:** **copyable** (факт 2023 Build with AI) · **не брать** как «Genius 2026 полный стек» без свежего fetch лендинга.
- **Реальное vs маркетинг:** вторичные обзоры 2026 (Zonka и др.) пишут bias detection / sentiment — **не поднимать в канон без primary page**.

#### QE-A-06 — Google Forms + Gemini

- **Что:** Help me create a form / quiz из промпта или Drive-файла; Suggest questions: 2–4 вопроса, если в форме уже ≥2; quiz помечает answers/points. Workspace Updates 2025-08-06: rollout Suggest questions с 5/19 Aug 2025. Ограничения help: **не** создаёт multi-section; **не** редактирует текущую форму (заменяет черновиком). Классический skip logic есть на продукт-странице Forms («Add logic to show relevant questions») — это не Gemini-interviewer. Eligible Workspace/AI plans; desktop.
- **Кто:** Google Workspace.
- **URL:** https://support.google.com/docs/answer/16346789 · https://workspaceupdates.googleblog.com/2025/08/gemini-google-forms-suggest-questions.html · https://workspace.google.com/products/forms/ · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (синтез пакета вопросов из существующего корпуса, не 12 вопросов Владельцу) · **не брать** как канал сбора лабы.

#### QE-A-07 — Tally AI + MCP

- **Что:** Четыре способности в редакторе: build from prompt (включая logic/formulas), edit, brand, troubleshoot. Free на всех планах, opt-in. «Your forms and submissions are never used to train AI models.» MCP / Claude connector / ChatGPT app: create, edit, analyze submissions. Классический conditional logic / calculator / hidden fields — rule engine, не LLM-at-runtime.
- **Кто:** Tally (Belgium, GDPR, hosted in Europe).
- **URL:** https://tally.so/ · https://tally.so/help/free-ai-form-builder · https://tally.so/help/claude-connector · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (агент↔форма как tool, не Owner) · **не брать** как identity.

#### QE-A-08 — Fillout AI Form Builder / «AI agent» баннер

- **Что:** Help: prompt / import questions / import from Google Forms, Typeform, Jotform, SurveyMonkey, Tally, Paperform / PDF → форма. Page logic — rule graph; «Set up page logic with AI» = Form Agent помогает настроить branching. Homepage 2026-08-31: баннер «New Fillout AI agent». Это **builder-agent**, не voice interviewer.
- **Кто:** Fillout.
- **URL:** https://www.fillout.com/ · https://www.fillout.com/help/ai-forms · https://www.fillout.com/help/page-logic · Дата доступа: 2026-08-31
- **Статус:** **copyable** (импорт чужой анкеты → структура) · **не брать** как live-агент.

#### QE-A-09 — Conversational / voice interviewers (Outset, Strella)

- **Что:** Отдельный рынок. Outset: AI interviewer «asking smart follow-ups, clarifying context in real time, and synthesizing results instantly»; recruit + synthesis; SOC 2 / GDPR / HIPAA claimed; synthetic users для теста гайда. Strella: AI-moderated interviews, «adapt questions in real-time», 46+ languages (маркетинг сайта).
- **Кто:** Parnassus Labs, Inc. (Outset); Strella.
- **URL:** https://outset.ai/platform · https://www.strella.io/ · Дата доступа: 2026-08-31
- **Статус:** **не брать** как AICM-identity и как Owner-interview. **adaptable** только идея «probe вместо 12 open questions» — внутри ролей Разведчик↔Аналитик, не человек-в-контуре.
- **Export-to-spec:** **не найдено** на fetched-страницах.

---

### Слой B — alignment / preference elicitation (исследования, не вендор-маркетинг)

#### QE-B-01 — Constitutional AI (Anthropic, 2022)

- **Что:** Единственный human oversight на harm — список правил («constitution»). SL: sample → self-critique → revision → finetune. RL: AI pairwise eval → preference model → RLAIF. Принципы «of order ten» / в appendix 16 critique-revision principles; выбирались ad hoc для research. Цель — *меньше* human labels, не «Владелец заполняет анкету».
- **Кто:** Bai et al., Anthropic.
- **URL:** https://www.anthropic.com/research/constitutional-ai-harmlessness-from-ai-feedback · https://arxiv.org/abs/2212.08073 · Дата доступа: 2026-08-31
- **Короткая цитата:** «The only human oversight is provided through a list of rules or principles, and so we refer to the method as ‘Constitutional AI’.»
- **Статус:** **copyable** (принципы как короткий typed list) · **adaptable** (critique→revision как сверка KC) · **не брать** как «открыть L0–L2 конституцией Владельца».

#### QE-B-02 — Deliberative alignment (OpenAI, 2024)

- **Что:** Модель *учится тексту* safety spec и *рассуждает* по нему в CoT до ответа. SFT на (prompt, CoT, output) где CoT цитирует spec (context distillation); RL с judge, которому дан spec; CoT скрыт от judge на RL, чтобы не поощрять deceptive CoT. Без human-labeled CoTs/answers. Сравнение в paper: RLHF и CAI используют spec только для *меток*, сам текст spec модели на инференсе не дают.
- **Кто:** Guan et al., OpenAI. Применено к o-series.
- **URL:** https://arxiv.org/abs/2412.16339 · https://openai.com/index/deliberative-alignment/ (fetch timeout 2026-08-31; arxiv **да**) · Дата доступа: 2026-08-31
- **Короткая цитата:** «directly teaches the model safety specifications and trains it to explicitly recall and accurately reason over the specifications before answering.»
- **Статус:** **adaptable** (закрытый L0–L2 как spec, который агент цитирует, а не переписывает) · **не брать** как тренировку новой модели лабой.

#### QE-B-03 — OpenAI Model Spec как «опросник принципов»

- **Что:** Спека желаемого поведения. Черновик 2024-05-08: objectives / rules / defaults; chain of command Platform > Developer > User > Tool. Версия 2026-08-18: Root / System / Developer / User / Guideline / No Authority; CC0; «production models do not yet fully reflect the Model Spec». Это **принципы с приоритетом**, не UX-форма.
- **Кто:** OpenAI.
- **URL:** https://cdn.openai.com/spec/model-spec-2024-05-08.html · https://model-spec.openai.com/2026-08-18.html · Дата доступа: 2026-08-31
- **Статус:** **copyable** (иерархия инструкций, packet как spec) · **не брать** как анкету Владельца. L0–L2 уже закрыты; spec лабы не переоткрывает их.

#### QE-B-04 — Pairwise preferences / RLHF (каркас, не продукт)

- **Что:** Сравнение двух ответов оркулом (человек или AI) → preference model / DPO. CAI явно строится как замена части human harm labels. Deliberative alignment цитирует RLHF как baseline, который *не* даёт модели текст spec.
- **Кто:** Christiano et al. 2017 (цитируется CAI/DA); Ouyang InstructGPT; Bai HH-RLHF 2022.
- **URL:** https://arxiv.org/abs/2212.08073 (CAI related work + method) · https://arxiv.org/abs/2412.16339 §5.1 · Дата доступа: 2026-08-31
- **Прямой fetch Christiano 2017 в этом пакете:** не выполнялся отдельно; факт «pairwise + PM» подтверждён CAI/DA primary papers.
- **Статус:** **copyable** (pairwise merge улик, не 12 open questions) · **не брать** как live-HITL разметку Владельца.

#### QE-B-05 — LLM-as-judge (Zheng et al., 2023)

- **Что:** MT-bench + Chatbot Arena. GPT-4 judge ≈ 80%+ agreement с людьми, «the same level of agreement between humans». Известные сдвиги: position, verbosity, self-enhancement; mitigation: swap positions, reference-guided. Практика 2025–26: LangSmith UI «LLM-as-a-Judge Evaluator» + few-shot human corrections.
- **Кто:** Zheng / Chiang / LMSYS; далее LangChain LangSmith.
- **URL:** https://arxiv.org/abs/2306.05685 · https://docs.langchain.com/langsmith/llm-as-judge · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (Тестер: rubric replay vs baseline) · **не брать** как «судья = Владелец».

#### QE-B-06 — Active learning for preferences

- **Что:** Не спрашивать все пары. Muldrew et al. arXiv:2402.08114 — acquisition по entropy + certainty implicit PM в DPO. Ji et al. arXiv:2402.09401 — APPO/ADPO, «about half of queries». Это **research**, не shipped-продукт форм.
- **URL:** https://arxiv.org/pdf/2402.08114 · https://arxiv.org/html/2402.09401v2 · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (спрашивать только informative contradiction) · **не брать** как новый опросник Владельца.

---

### Слой C — agent ecosystems (только public docs; не identity AICM)

#### QE-C-01 — OpenAI Evals / Agents (eval как questionnaire поведения)

- **Что:** Evals: data_source_config + testing_criteria (string_check и др.); шаблон `{{ item.* }}` / `{{ sample.output_text }}`. Docs прямо: процесс «similar to behavior-driven development». **Deprecation:** read-only 2026-10-31, shutdown 2026-11-30; cookbook указывает Promptfoo. Agents SDK (анонс): Agents, Handoffs, Guardrails, Tracing — оркестрация, не «анкета Владельца».
- **URL:** https://developers.openai.com/api/docs/guides/evals · https://openai.com/index/new-tools-for-building-agents/ · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (harness Тестера, replay vs baseline) · **не брать** платформу OpenAI Evals как зависимость лабы (sunset). Не ставить Agents SDK как личность AICM.

#### QE-C-02 — Anthropic Claude Projects + Agent Skills

- **Что:** Projects: workspace + knowledge + project instructions (tone/role). Help: available including Free (max 5 projects). Skills (2025-10-16): folder + `SKILL.md` (YAML name/description); progressive disclosure; «Building a skill for an agent is like putting together an onboarding guide for a new hire.» Open standard 2025-12-18. Это **ролевой onboarding файл**, не HITL-опрос.
- **URL:** https://support.claude.com/en/articles/9517075-what-are-projects · https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills · https://www.anthropic.com/news/skills · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (skill/инструкция роли = существующий brief штаба, не новый бот) · **не брать** Claude Projects как хранилище PREF.

#### QE-C-03 — LangSmith LLM-as-judge evals

- **Что:** Offline evaluator: prompt + model + variable mapping + feedback schema (boolean / categorical / continuous). Few-shot human corrections вставляются в prompt. Online evals на production traces — **не** для live AICM.
- **URL:** https://docs.langchain.com/langsmith/llm-as-judge · https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge · Дата доступа: 2026-08-31
- **Статус:** **adaptable** (рубрика Тестера) · **не брать** online-on-traces и LangSmith как identity.

#### QE-C-04 — CrewAI unified Memory

- **Что:** Один класс `Memory`; LLM infers scope/categories/importance; composite score semantic+recency+importance; consolidation при similarity ≥ 0.85 (keep/update/delete/insert_new). `Crew(memory=True)` — shared; agent может `scope("/agent/researcher")`. Source + private flags. **Не** «опрос Владельца»; это captured prefs внутри crew.
- **URL:** https://docs.crewai.com/edge/en/concepts/memory · Дата доступа: 2026-08-31
- **Статус:** **не брать** (не ставить CrewAI). **copyable** факт: память агента ≠ анкета человека.

#### QE-C-05 — Letta / MemGPT (profile as captured prefs)

- **Что:** Paper 2023: hierarchical memory, working context для «key facts, preferences»; self-directed function calls. Продукт Letta: memory blocks `persona` / `human` (search snippets docs.letta.com; прямой fetch `.../memory-blocks/index.md` = **404** 2026-08-31). MemFS fetch docs.letta.com/concepts/memfs — в поиске есть, отдельный полный fetch в пакете не фиксировался как 200. Не выдумывать 2026-API.
- **URL:** https://arxiv.org/abs/2310.08560 · Дата доступа: 2026-08-31
- **Статус:** **copyable** (research: prefs живут в блоке памяти агента) · **не брать** runtime Letta как AICM.

#### QE-C-06 — AutoGen memory (2026)

- **Что:** Имя запрошено brief. Прямой fetch актуальных public docs AutoGen memory **не выполнен успешно**. В поисковой выдаче 2026 — «AutoGen superseded by Microsoft Agent Framework». **Не изобретать** карточку продукта.
- **Статус:** **не найдено** как подтверждаемый 2026 primary. Не брать, не ставить.

---

## 4. Не брать (явно)

| Запрет | Почему (факт пакета, не мораль) |
|---|---|
| HITL-оператор | Qualtrics ticketing: human approval before send; OpenAI Evals/LangSmith online traces — человек/дашборд в контуре. Лаба: пакет-штамп, не оператор. |
| Владелец-как-дизайнер анкеты | OPEN-19 не становится questionnaire homework. Владелец = External Enabler only. |
| Открытие L0–L2 | Закрыты. Переоткрытие только именованным материальным противоречием (рамка лабы). Новая технология ≠ противоречие. |
| Опрос как постоянный человек-в-контуре | Clarify/Outset/Strella — рынок qualitative; не цикл Mon–Fri лабы. |
| Плодить ботов без роли | Skills/Projects/Crews — вендорский onboarding. У лабы роли уже есть. |
| Новые пустые репо / GitHub | Черновик сдан на диск лаборатории; в git кладёт штаб. Этот коммит — архив. |
| Hermes / live | Не адресат. Trading = first economic proof, not identity. |
| Склеить A+B+C в «AI-анкету AICM» | Три разных объекта. |
| Ставить CrewAI / Letta / LangGraph / Qualtrics EA как identity | Public docs ≠ install order. |
| Расширять X write | @acapitalmanager read-only. HQ-08 **отброшен**. |

---

## 5. Векторы расширения AICM (кандидаты в Foundation *позже*, не implement now)

Не «стать стартапом опросов». Четыре кражи паттерна:

1. **Domain-constraint elicitation** — ветвление/пакет вместо 12 open questions. Источник паттерна: Typeform Clarify (лимит 2), Tally/Fillout/Qualtrics/SurveyMonkey rule branching, Gemini Suggest 2–4. Кандидат в Foundation: шаблон brief штаба, не UX-форма Владельца.
2. **Contradiction audit** — CAI critique/revision; CrewAI consolidation delete-if-contradicted; DA «cite the spec». Кандидат: флаг нового KC против закрытых L0–L2 + `sverki/`. Fail-closed. Не reopen.
3. **Packet-approval** — Model Spec / constitution как *один* артефакт с provenance, не серия вопросов. Кандидат: штамп файла `razvedka/` по понедельничному циклу 10:00.
4. **Agent-to-agent questionnaire** — Skills as onboarding guide; CrewAI scoped memory researcher vs writer; LangSmith dataset+rubric. Кандидат: Разведчик↔Аналитик↔Механик обмениваются карточками QE/KC, не Owner.

Все четыре — **Knowledge Candidates на потом**. Consilium основной системы. Второй Consilium здесь не строим.

---

## 6. Фишки лабы (Grok HQ) — REQUIRED ADDENDUM

Имплант *в лабораторию*, на существующие роли и папки. Не новые боты.

Роли (brief, не выдумывать): штаб (Stabschef) + Разведчик / Аналитик / Канонист / Картограф / Механик / Тестер / Твиттер.  
Папки: AICM-docs `shtab/` `razvedka/` `sverki/` `kanon/`.  
Гигиена Пн 09:00; дневной цикл Пн–Пт 10:00; X read-only @acapitalmanager; L0–L2 closed.

Не имплантировать: HITL-оператор, Owner-as-questionnaire-designer, spawn ботов без роли, открытие L0–L2, расширение X write.

### HQ-01 — Adaptive packet / branching elicitation вместо 12 OPEN questions

- **Зачем:** Снять OPEN-19 с Владельца. Brief штаба задаёт *ветви* (если противоречие с L0–L2 → сверка; если нет URL → «не найдено»), а не 12 пустых полей.
- **Откуда тренд:** Typeform Clarify (max 2, нельзя кастомить) https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI · Tally conditional + AI edit logic https://tally.so/help/free-ai-form-builder · Gemini Suggest 2–4 https://workspaceupdates.googleblog.com/2025/08/gemini-google-forms-suggest-questions.html · Дата доступа: 2026-08-31
- **Как ляжет:** Stabschef — шаблоны brief в `shtab/`. Разведчик исполняет ветки. Владелец не дизайнер.
- **Риск:** Съехать в «Clarify для Owner». Fail: любой follow-up к Владельцу = нарушение рамки.

### HQ-02 — Contradiction-flag нового KC vs закрытые L0–L2 + sverki

- **Зачем:** CAI-style critique без открытия конституции. Новый KC либо совместим, либо идёт в `sverki/` как расхождение. Fail-closed.
- **Откуда тренд:** CAI critique→revision https://arxiv.org/abs/2212.08073 · CrewAI consolidation `delete` if contradicted https://docs.crewai.com/edge/en/concepts/memory · DA «cite the policy» https://arxiv.org/abs/2412.16339 · Дата доступа: 2026-08-31
- **Как ляжет:** Аналитик + Картограф. Канонист не трогает L0–L2. Папки: `sverki/` + индекс в `razvedka/`.
- **Риск:** Назвать «нет данных» противоречием и reopen. Рамка 2026-08-30 это запрещает.

### HQ-03 — Packet-stamp (одобрить весь файл разведки, не 12 вопросов)

- **Зачем:** Model Spec / constitution — один артефакт с датой доступа. Штаб штампует файл, не сессию чата.
- **Откуда тренд:** Model Spec как целый документ https://model-spec.openai.com/2026-08-18.html · CAI constitution list https://arxiv.org/abs/2212.08073 · Дата доступа: 2026-08-31
- **Как ляжет:** Stabschef, цикл Пн 10:00. Файл живёт в `razvedka/` (этот пакет — образец).
- **Риск:** Штамп без provenance table = пустой канон.

### HQ-04 — Agent-to-agent questionnaire (Scout↔Analyst↔Mechanic, не Owner)

- **Зачем:** Слияние улик между ролями. Skills = onboarding guide роли; CrewAI researcher scope vs writer shared — метафора, не install.
- **Откуда тренд:** Anthropic Skills «onboarding guide for a new hire» https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills · CrewAI `memory.scope("/agent/researcher")` https://docs.crewai.com/edge/en/concepts/memory · Дата доступа: 2026-08-31
- **Как ляжет:** Разведчик пишет QE-карточку; Аналитик — расхождения; Механик — «можно ли гейт»; Тестер молчит, пока нет replayable механизма. Owner вне цепочки.
- **Риск:** Начать «crew» из новых ботов. Запрещено.

### HQ-05 — KC registry: ID / provenance / copyable|адаптируемо|не брать

- **Зачем:** Каталог этого файла *и есть* прототип реестра. Без реестра слои A/B/C снова склеятся.
- **Откуда тренд:** CAI github principles list (transparency of bits); LangSmith feedback keys unique across experiments https://docs.langchain.com/langsmith/llm-as-judge · Typeform/Tally feature pages с явным «coming soon» vs shipped · Дата доступа: 2026-08-31
- **Как ляжет:** `razvedka/` + индекс. Картограф ведёт ID. Канонист не повышает KC в `kanon/` без Consilium основной системы.
- **Риск:** Выдать QE-ID за PREF-ID. Баннер файла это запрещает.

### HQ-06 — Eval-harness как questionnaire поведения Тестера (replay vs baseline, не live HITL)

- **Зачем:** BDD-формулировка ожидаемого поведения контура на истории. Не человек в пятницу.
- **Откуда тренд:** OpenAI Evals «similar to behavior-driven development» https://developers.openai.com/api/docs/guides/evals · LangSmith LLM-as-judge + dataset https://docs.langchain.com/langsmith/llm-as-judge · Zheng et al. agreement https://arxiv.org/abs/2306.05685 · Дата доступа: 2026-08-31
- **Как ляжет:** Тестер. Метрики replay vs baseline. Online-evals / production traces — **не брать**. OpenAI Evals sunset — не строить зависимость.
- **Риск:** HITL-разметка «пока нет датасета» → Владелец. Fail-closed: нет истории = нет eval, idle.

### HQ-07 — Hygiene Пн 09:00 как contradiction/provenance sweep, не новые боты

- **Зачем:** Раз в неделю: битые URL, «не найдено» vs выдумка, флаги HQ-02, штампы без таблицы provenance.
- **Откуда тренд:** DA/CAI требуют цитировать spec; LangSmith few-shot corrections; этот пакет сам фиксирует timeout/404. Дата доступа: 2026-08-31 (метод пакета).
- **Как ляжет:** Stabschef слот Пн 09:00. Разведчик чинит provenance. Аналитик — открытые `sverki/`. Твиттер не трогает (X read-only).
- **Риск:** Превратить гигиену в «еженедельный опрос штаба». Это снова HITL.

**HQ-08 не предлагается.** X @acapitalmanager уже read-only. Write не расширять.

---

## 7. Пробелы

Зафиксировано как **не найдено** / не подтверждено fetch — не заполнять «для полноты».

- **Export-to-spec** (ответы анкеты → constitution / Model Spec) как shipped-фича Typeform / Qualtrics / SurveyMonkey / Google Forms / Tally / Fillout / Outset / Strella — **не найдено**.
- **SurveyMonkey Genius лендинг 2026** (`/mp/surveymonkey-genius/`) — timeout; актуальный состав Genius кроме Build with AI 2023 и rule-branching help — **не подтверждён primary**.
- **LLM-interviewer внутри Google Forms / Tally / Fillout** — **не найден**; у них builder + rule logic.
- **Кастомизация поведения Clarify** — официально нельзя (Typeform help).
- **AutoGen memory 2026 primary docs** — **не найдены** (QE-C-06).
- **Letta memory-blocks canonical URL** — 404 на запрошенном path; продукт-карточка 2026 API не писалась.
- **OpenAI deliberative-alignment blog** — timeout; опирались на arxiv:2412.16339.
- **Microsoft AutoGen successor (Agent Framework) memory** — не фетчился; не описывать.
- **Pairwise UI как продукт форм (не research)** — **не найден** в слое A.
- **Голосовой interviewer Qualtrics / Typeform** как GA — **не найден** на fetched pages (Qualtrics EA = text-entry + ticketing).
- **Русскоязычные primary** по этим продуктам не собирались; пакет на русских формулировках лаборатории, цитаты — EN primary.

---

## 8. Provenance (доступ 2026-08-31)

| # | URL | Слой | Fetched | Комментарий |
|---|---|---|---|---|
| S1 | https://www.typeform.com/ai/ | A | **да** | Builder, MCP, Coming Soon Skills/Landing; schema.org featureList. |
| S2 | https://help.typeform.com/hc/en-us/articles/31042031941780-Clarify-with-AI | A | **да** | Max 2; no customize; no skip on Clarify. |
| S3 | https://help.typeform.com/hc/en-us/articles/35164536449940-FAQ-with-AI | A | поиск, не полный fetch | FAQ-with-AI: Anthropic, max 20 Q&A, no branching on AI replies. Не поднимать выше help Clarify. |
| S4 | https://www.qualtrics.com/ | A | **да** | Маркетинг XM / Experience Agents / synthetic audiences. |
| S5 | https://www.qualtrics.com/platform/experience-agents/ | A | **да** | Маркетинг «act instantly / make-goods». |
| S6 | https://www.qualtrics.com/support/experience-agents/experience-agents-overview/ | A | **да** | Human approval на ticketing actions; Agent Studio; gated. |
| S7 | https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/survey-flow-overview/ | A | **да** | Survey Flow elements. |
| S8 | https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/branch-logic/ | A | поиск+цитаты | Rule branches. |
| S9 | https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/text-iq/topics-in-text-iq/ | A | поиск | Topics / recommended. |
| S10 | https://www.qualtrics.com/support/omnichannel-listening/text-analytics-xm/ai-powered-topic-models/ | A | поиск | AI topic hierarchy; не совмещать с Text iQ. |
| S11 | https://www.surveymonkey.com/mp/surveymonkey-genius/ | A | **нет (timeout)** | Не цитировать состав 2026 с этой страницы. |
| S12 | https://www.surveymonkey.com/newsroom/surveymonkey-announces-ai-generated-surveys/ | A | **да** | Build with AI, 2023-10-25, Genius lineup, GPT-3. |
| S13 | https://help.surveymonkey.com/en/surveymonkey/create/advanced-branching/ | A | поиск | Rule branching. |
| S14 | https://help.surveymonkey.com/en/surveymonkey/create/skip-logic/ | A | поиск | Skip vs Advanced. |
| S15 | https://workspace.google.com/products/forms/ | A | **да** | Logic + Sheets; Gemini на этой странице почти нет. |
| S16 | https://support.google.com/docs/answer/16346789 | A | **да** | Help me create; no multi-section; no edit-in-place. |
| S17 | https://workspaceupdates.googleblog.com/2025/08/gemini-google-forms-suggest-questions.html | A | поиск | Suggest 2–4, Aug 2025 rollout. |
| S18 | https://tally.so/ | A | **да** | Conditional logic, free, GDPR EU. |
| S19 | https://tally.so/help/free-ai-form-builder | A | **да** | 4 abilities; no training on submissions. |
| S20 | https://tally.so/help/claude-connector | A | поиск | MCP create/edit/analyze. |
| S21 | https://www.fillout.com/ | A | **да** | «New Fillout AI agent» banner. |
| S22 | https://www.fillout.com/help/ai-forms | A | **да** | Prompt/import builder. |
| S23 | https://www.fillout.com/help/page-logic | A | поиск | Rule graph + Form Agent для logic. |
| S24 | https://outset.ai/platform | A | **да** | AI-moderated interviews; synthesis; SOC2/GDPR/HIPAA claim. |
| S25 | https://www.strella.io/ | A | поиск | AI-moderated; 46+ languages (маркетинг). |
| S26 | https://www.anthropic.com/research/constitutional-ai-harmlessness-from-ai-feedback | B | **да** | Abstract CAI. |
| S27 | https://arxiv.org/abs/2212.08073 | B | **да** | Full CAI paper (html). |
| S28 | https://arxiv.org/abs/2412.16339 | B | **да** | Deliberative alignment paper. |
| S29 | https://openai.com/index/deliberative-alignment/ | B | **нет (timeout)** | Сниппет поиска использован только как указатель; факты — S28. |
| S30 | https://cdn.openai.com/spec/model-spec-2024-05-08.html | B | **да** | Первый Model Spec. |
| S31 | https://model-spec.openai.com/2026-08-18.html | B | **да** | Актуальная версия на дату доступа. |
| S32 | https://arxiv.org/abs/2306.05685 | B | **да** | LLM-as-judge / MT-bench. |
| S33 | https://arxiv.org/pdf/2402.08114 | B | поиск | Active preference learning DPO. |
| S34 | https://arxiv.org/html/2402.09401v2 | B | поиск | Active queries RLHF/DPO. |
| S35 | https://developers.openai.com/api/docs/guides/evals | C | **да** | Evals API + deprecation 2026-10-31 / 11-30. |
| S36 | https://openai.com/index/new-tools-for-building-agents/ | C | поиск | Agents SDK: handoffs, guardrails, tracing. |
| S37 | https://support.claude.com/en/articles/9517075-what-are-projects | C | поиск | Projects knowledge + instructions. |
| S38 | https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills | C | **да** | Skills = onboarding guide; SKILL.md. |
| S39 | https://www.anthropic.com/news/skills | C | поиск | Skills GA note; open standard 2025-12-18. |
| S40 | https://docs.langchain.com/langsmith/llm-as-judge | C | **да** | UI evaluator + few-shot corrections. |
| S41 | https://docs.langchain.com/langsmith/online-evaluations-llm-as-judge | C | поиск | Online traces — не для лабы. |
| S42 | https://docs.crewai.com/edge/en/concepts/memory | C | **да** | Unified Memory, scopes, consolidation. |
| S43 | https://arxiv.org/abs/2310.08560 | C | **да** | MemGPT paper. |
| S44 | https://docs.letta.com/guides/core-concepts/memory/memory-blocks/index.md | C | **нет (404)** | Не цитировать path как живой. |
| S45 | https://www.prnewswire.com/news-releases/typeform-launches-ai-suite-to-power-smarter-data-collection-302381161.html | A | поиск | Winter '25, 2025-02-20, Clarify. Вторичный PR. |
| — | AutoGen official memory 2026 | C | **не найдено** | QE-C-06. |
| — | Export-to-spec product pages | A | **не найдено** | §7. |

**Пропущено как не-primary / не открывалось:** пиратские PDF; установка фреймворков; GitHub write; Owner call; внутренние PREF.

**404/timeout стартовых URL:** SurveyMonkey Genius лендинг — timeout; OpenAI DA blog — timeout; Letta memory-blocks path — 404. Остальные стартовые из brief, которые фетчились, относятся к названным продуктам/бумагам.

---

## 9. Границы

- **Не канон AICM. Не Foundation. Не PREF. Не live. Не GitHub.**
- Слои A / B / C не склеивать. Фишки HQ не есть «продукт опросов».
- Если источник тонкий или timeout — это сказано в provenance и §7, а не дописано.
- Короткие цитаты только из fetched/quoted primary. Номера страниц книг/paywall **не** выдумывались.
- Лаборатория Grok: находки = Knowledge Candidates с provenance. Сами в Foundation не продвигаются.

Конец пакета. Knowledge Candidate only. L0–L2 not reopened.
