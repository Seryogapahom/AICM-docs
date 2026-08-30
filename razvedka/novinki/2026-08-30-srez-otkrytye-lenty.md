# Срез новинок — открытые ленты

Статус: Knowledge Candidate. Не Foundation. Не канон AICM.
Дата: 2026-08-30
Источник: открытый HTML / агрегаторы (GitHub Trending, HN, x.ai, Google, Anthropic, MCP, SEC.gov, CoinDesk, Cointelegraph, arXiv). Коннектора X нет.
Provenance: WebSearch + WebFetch без логина. Зеркала X: 403/500/timeout; xcancel C&D 24 Aug. Не live. Не пакеты Андреева/Радченко/Миши/TE/Zatulyviter.

ACCESS: 2026-08-30 (Europe/Zurich)
СТАТУС: Knowledge Candidate. Не канон AICM. Не Foundation. Не Consilium. L0–L2 не трогать.
МЕТОД: открытый HTML / агрегаторы. Коннектора X нет. Не live-торговля.
НЕ БРАЛИ: пакеты Андреева/Радченко, KC-01.

## Доступ (дыры)
Работало (WebSearch + WebFetch, без логина):
- GitHub Trending: https://github.com/trending (HTML снял, звёзды — как на странице ACCESS)
- Hacker News frontpage: https://news.ycombinator.com/news
- Официальные блоги/доки: x.ai, developers.googleblog.com, claude.com/blog, platform.claude.com, blog.modelcontextprotocol.io, modelcontextprotocol.io/development/roadmap
- SEC.gov (правила + press release)
- CoinDesk, Cointelegraph
- arXiv abs + Atom API: https://arxiv.org/abs/2608.12841 и export.arxiv.org
- GitHub releases OpenClaw tag v2026.8.1-beta.3

X / зеркала — блокеры (не обходили логин):
- https://x.com → WebFetch 403 Forbidden
- https://syndication.twitter.com → WebFetch 403 Forbidden
- https://nitter.net → WebFetch 403 Forbidden
- https://nitter.poast.org → WebFetch 500 Internal Server Error
- https://nitter.privacydev.net → WebFetch timeout
- https://xcancel.com → HTML открылся: сервис остановлен. Текст: 24 Aug 2026 20:00 EST письмо cease-and-desist от X Corp.; «The service XCancel is stopped until further notice»
- https://nitter.cz и https://twiiit.com → редиректор Twiiit, «There are currently 1 instances online»; ленты твитов не сняли
- npmjs.com/package/openclaw/v/2026.8.1-beta.3 → timeout (релиз подтверждён с GitHub tag)
- https://agent-plugins.org/ → timeout; spec только из Google Developers Blog

Браузер/десктоп не открывали. В X не логинились.

## Пули (12)

### 1. Grok 4.6 — агентный флагман xAI
- Тип: технология
- Что: 12 Aug 2026 xAI выпустила Grok 4.6: упор на long-running agents, интерактив/визуал, самопроверку на длинных траекториях. Доступ: Cursor, Grok Build, API, OpenRouter/Vercel/Cloudflare. Цена со страницы: $2 / MTok in, $6 / MTok out; fast-вариант «twice the price». Заявлено совпадение с GPT-5.6 Sol на Artificial Analysis Intelligence Index (61 vs 61). Промо «2x included usage» в Cursor/Grok Build — на первую неделю после релиза (к ACCESS уже истекло).
- Provenance: https://x.ai/news/grok-4-6
- Дата источника: 2026-08-12
- Почему AICM: кандидат на рабочую модель длинных агентных сессий (не смена identity)
- Риск / что не верифицировано: бенчмарки — цифры вендора + «competitor figures from system cards»; независимый прогон не снимали

### 2. Agent Plugins 1.0.0 — общий ящик skills + MCP
- Тип: инструмент
- Что: 6 Aug 2026 Google объявил, что входит Core Maintainer в TSC Agent Plugins 1.0.0 (Amazon, Cursor, Microsoft, OpenAI, Vercel). Формат: каталог с plugin.json + skills/ (спека Agent Skills) + mcp.json; клиентские расширения в reverse-DNS папке. v1 — только package format: нет install/distribution/permissions/sandbox/provenance. Уже в продуктах Google: Agents CLI и Data Agent Kit (BigQuery/Spanner/Cloud SQL как portable plugins).
- Provenance: https://developers.googleblog.com/agent-plugins-package-your-skills-tools-and-more/
- Дата источника: 2026-08-06
- Почему AICM: кандидат упаковки навыков лаборатории без привязки к одному клиенту
- Риск / что не верифицировано: agent-plugins.org не открылся (timeout); совместимые клиенты кроме Google — со слов поста

### 3. MCP roadmap после спеки 2026-07-28
- Тип: инструмент
- Что: Roadmap last updated 2026-08-22. Пять приоритетов на 6–12 мес.: (1) agentic messaging — webhooks/channels вместо polling, mature Tasks SEP-2663; (2) HTTP-native transport, в т.ч. Streamable HTTP over stdio; (3) agent identity — DPoP, Workload Identity Federation, ID-JAG, не pasted API keys; (4) один контракт tools/call + progressive discovery каталога; (5) SDK/codegen из спеки. Явно: «current thinking rather than firm commitments», даты следующего релиза нет. Спека 2026-07-28 уже убрала protocol-level sessions/handshake (SEP-2575/2567).
- Provenance: https://modelcontextprotocol.io/development/roadmap ; https://blog.modelcontextprotocol.io/posts/mcp-roadmap/
- Дата источника: 2026-08-22
- Почему AICM: инфра агентов (identity, push, progressive tools) важнее нового чата
- Риск / что не верифицировано: WG Agent Identity и Core Primitives «forming»; это направление, не поставка

### 4. Anthropic: computer use + Skills API + Files API → GA
- Тип: инструмент
- Что: 20 Aug 2026 computer use, Skills API и Files API стали GA на Claude Platform. Новый browser use (структура страницы + пиксели, не только screenshot). Computer use: несколько действий за ход вместо одного вызова; eligible for HIPAA BAA. Skills: upload/version, грузятся по задаче, исполняются в sandbox Anthropic. Files API: expiration, 5× rate limits, 1 TB storage / org. Skills/Files также Microsoft Foundry; обновлённый computer/browser — «coming soon» на Vertex AI. Цитата клиента (Davide Locatelli): claims workflow 32→13 мин, cost ~−30%, completion 100% — вендорский кейс, не наш замер.
- Provenance: https://claude.com/blog/computer-use-skills-api-files-api
- Дата источника: 2026-08-20
- Почему AICM: законный computer-use / skill-files контур для ценности вне терминала
- Риск / что не верифицировано: latency/cost кейс — одна цитата; browser use исполняет клиент, не Anthropic

### 5. Google ADK: zero-trust для агентов с мутацией стейта
- Тип: ценность-вне-торговли
- Что: 17 Aug 2026 Google описал три слоя вне промпта: (1) подпись каждой write Cloud KMS/HSM; (2) исполнение сгенерированного кода в gVisor (runtime=runsc, network=none); (3) детерминированный semantic gateway + CI-тесты jailbreak/PII. Референс: open-source demo autonomous support/refund agent. Тезис страницы: system prompt ≠ security boundary.
- Provenance: https://developers.googleblog.com/en/build-zero-trust-ai-agents-with-googles-agent-development-kit/
- Дата источника: 2026-08-17
- Почему AICM: паттерн fail-closed вокруг агента, который трогает деньги/БД — не торговый вход
- Риск / что не верифицировано: demo локально на HMAC, не прогоняли; production mapping = GCP



### 6. OpenClaw 2026.8.1-beta.3
- Тип: инструмент
- Что: GitHub pre-release 2026-08-24T04:40:41Z, tag v2026.8.1-beta.3, author steipete.
  GPT-5.6 Sol/Terra/Luna/Ultra reasoning across OpenClaw and Codex runtime.
  First-run setup continues verified model setup into Custodian and optional channels.
  External Gateway lifecycle supervision with verified restart handoff.
  Compact verified SQLite backup and fresh-target restore; durable ingress monitors.
- Дата источника: 2026-08-24
- Provenance: https://github.com/openclaw/openclaw/releases/tag/v2026.8.1-beta.3
- Почему AICM: новое относительно KC-01 — локальный gateway + backup стейта
- Почему AICM: новое относительно KC-01 — локальный gateway + backup стейта

- Risk: pre-release beta

### 7. GitHub Trending: skills as distribution unit
- Тип: ценность-вне-торговли
- Что: ACCESS snapshot https://github.com/trending. mvanhorn/last30days-skill 60305 stars (+272 today). K-Dense-AI/scientific-agent-skills 38409 (+1587 today), 165 skills + 100+ scientific DBs. tt-a1i/archify 32969 (+3902). THU-MAIC/OpenMAIC 22955 (+907). punkpeye/awesome-mcp-servers 93114 (+65, catalog not new).
- Provenance: https://github.com/trending ; https://github.com/mvanhorn/last30days-skill ; https://github.com/K-Dense-AI/scientific-agent-skills ; https://github.com/THU-MAIC/OpenMAIC
- Дата источника: ACCESS 2026-08-30 (trending snapshot)
- Почему AICM: packed skills for research/science/docs, не торговый сигнал
- Риск / что не верифицировано: marketing README 190000+ scientists; last30days X still needs X login

### 8. SEC Novel ETFs — окно комментариев закрывается 31 Aug
- Тип: новость рынка
- Что: File S7-2026-24 / Release 33-11426. SEC asks comment on ETFs in crypto, commodities, single-stock, heightened leverage, blockchain, private assets, event contracts. Comments due Aug. 31, 2026. Request for comment, not a rule. Comment file already has Aug letters/meetings (Digital Chamber 27 Aug, Rafferty/K&L 24 Aug).
- Provenance: https://www.sec.gov/rules-regulations/2026/06/s7-2026-24 ; https://www.sec.gov/rules-regulations/public-comments/s7-2026-24
- Дата источника: 2026-07-06 (FR / last reviewed); deadline 2026-08-31
- Почему AICM: calendar risk for novel ETF products, не система входа
- Риск / что не верифицировано: rulemaking outcome unknown; spot BTC/ETH ETFs not cancelled on this page

### 9. SEC предлагает Regulation Crypto Assets
- Тип: новость рынка
- Что: Press 2026-76, Washington D.C., Aug. 18, 2026. Two exemptions from Securities Act s.5: up to $5M over 4 years (one-time); up to $75M each 12-month period (second has financials + ongoing reporting). Principles-based disclosures; antifraud remains. Conditional safe harbor: if conditions met, crypto asset deemed not subject to an investment contract. Preempts state registration for offers under this regulation. File S7-2026-27; comments due Oct. 20, 2026 (FR 21 Aug).
- Provenance: https://www.sec.gov/newsroom/press-releases/2026-76-sec-proposes-new-regulation-crypto-assets ; https://www.sec.gov/rules-regulations/2026/08/s7-2026-27
- Дата источника: 2026-08-18
- Почему AICM: crypto capital-formation regime = background, not an order to trade
- Риск / что не верифицировано: proposed rule; 1.99MB PDF not parsed

### 10. Spot BTC ETF: August inflows, Friday reversal; Hashdex DEFI closed
- Тип: новость рынка
- Что: Cointelegraph 29 Aug: US spot Bitcoin ETFs $201.8M net outflow Friday, end of 9-session inflow streak; August still +$3.3B with one US session left; AUM $97.6B after >$100B Thursday. Outflow leaders: ARKB $114.9M, BITB $49.7M, IBIT $33.4M (Farside). Only Friday inflow: MSBT +$9.3M. ETH ETFs +$102.2M, XRP +$26.2M same day (SoSoValue). CoinDesk 4 Aug: Hashdex liquidates DEFI ($14.7M AUM), first US spot bitcoin ETF closure; last trading day Aug. 17 then sell BTC and cash to shareholders. On 4 Aug IBIT $47.08B vs DEFI $14.7M.
- Provenance: https://cointelegraph.com/markets/bitcoin-etf-end-9-day-inflow-streak-btc-below-78k ; https://www.coindesk.com/business/2026/08/04/first-u-s-spot-bitcoin-etf-to-close-as-inflows-dwindle-investors-chase-ai-returns
- Дата источника: 2026-08-29 and 2026-08-04 (DEFI last trade 2026-08-17)
- Почему AICM: product flow/concentration = liquidity context, not an entry
- Риск / что не верифицировано: SoSoValue/Farside not fetched directly; BTC price widgets on pages drift

### 11. [СЛУХ] AQuA — recursive research-agents for factors/models
- Тип: слух-стратегия
- Что: arXiv 2608.12841 v2 (cs.CL/cs.AI), Princeton/Ant/Stanford. Two SEPARATE systems (no shared memory/state): Part I formulaic factors on crypto 5m, combined IC ~0.190; Part II hybrid time-series on US equities 30m, per-stock IC +0.0843, threshold L/S Sharpe up to +2.50 @ 2bp two-leg, walk-forward ~+2.0, positive every year 2021-2025. Design: sealed sandbox (splits/features/labels/evaluator human-authored; agent only DSL/config diff). Authors: metrics are simulated, not live-validated; one market/horizon per part; human operator required.
- Provenance: https://arxiv.org/abs/2608.12841 ; https://export.arxiv.org/api/query?id_list=2608.12841
- Дата источника: published 2026-08-13; updated 2026-08-17 (v2)
- Почему AICM: rumor about research-loop + fail-closed evaluator — not an AICM entry system
- Риск / что не верифицировано: paper/backtest; factor expressions withheld; not reproduced; not canon, not live

### 12. [СЛУХ] Clarity Act ~10% in 2026; cycle top = Korea can buy ETF
- Тип: слух-стратегия
- Что: CoinDesk 17 Aug: Galaxy Research head Alex Thorn on 14 Aug cut odds Clarity Act becomes law in 2026 to roughly 10% (from 75% in May); prediction markets ~17%. Cloture vote set for Sep. 15; observers expect another delay. CoinDesk live 27 Aug cites CryptoQuant CEO Ki Young Ju (X post, tweet itself not opened): final leg of cycle when Korea gets spot BTC ETF access; top = regional bank employee recommends ETF to a granny. Access narrative, not a setup.
- Provenance: https://www.coindesk.com/markets/2026/08/17/bitcoin-tracks-equity-bounce-but-usd390-million-etf-outflow-week-keeps-bulls-on-back-foot ; https://www.coindesk.com/business/2026/08/27/live-updates-bitcoin-etf-inflows-hit-eight-straight-days-as-august-tops-usd3-billion
- Дата источника: 2026-08-17 (Thorn); 2026-08-27 (Ju via CoinDesk)
- Почему AICM: rumor on regulatory calendar and geography of access — watch candidate, not an entry
- Риск / что не верифицировано: Thorn/Ju primary posts are X; we did not open them (403 / dead mirrors); CoinDesk paraphrase only

## Что устарело / шум (кратко)
- Claude Opus 5 (platform.claude.com): released 2026-07-24, ID claude-opus-5, 1M ctx, $5/$25, thinking on by default — still Anthropic flagship, but July; skipped to avoid model-catalog bloat.
- LangGraph/CrewAI/AutoGen/Symphony roundups (alicelabs, presenc, agent-harness) overlap KC-01 checkpointers; skipped.
- GitHub trending noise: ghidra, checkstyle, zod, heretic, crawl4ai — old or off-mandate.
- HN frontpage ACCESS: RISC-V in CPython, Tencent Hy4 preview, California Linux age-verification exemption — Hy4 was HN title only, tencent.com not fetched.
- CoinDesk 27 Aug live: Nvidia/Schwab/SOL session noise; Schwab SOL/AVAX/LINK coming months left out (no listing date).
- OMS / ACP / OAMP memory specs on GitHub — not an August release; not confused with KC-01 PAM.

## Не делать
- Do not touch L0-L2. No hybrid waves+news.
- No live trading, no keys, no X-login bypass.
- Do not treat AQuA Sharpe/IC as an entry system.
- Do not canonize Agent Plugins / MCP roadmap / OpenClaw beta without a separate staff order.
- Do not duplicate KC-01 (Letta, LangGraph checkpointers, PAM, llama.cpp RPC, SkyPilot, MLX, Team of Rivals, verify-gated completion).
- Do not retell Andreev / Hedliners / Radchenko / Frost-Prechter / open Elliott / market-context-open.md.
