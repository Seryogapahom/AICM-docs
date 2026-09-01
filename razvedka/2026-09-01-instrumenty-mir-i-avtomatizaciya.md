# Knowledge Candidate — инструменты мира и автоматизации (WI)

```
Статус: Knowledge Candidate. Не Foundation. Не PREF. Не WORLD-PREF. Не Hermes. Не QE.
Дата: 2026-09-01
Серия ID: WI-01…28
Штамп штаба: принято в архив как полка кандидатов. Не внедрение. S01–S02 не reopen. S03 не закрыт. Enabler не нужен.
Связанный источник карты мира: razvedka/2026-09-01-aicm-world-preferences-lineage.md (WMAP-2026-08-31)
Анкеты: не дублирует razvedka/2026-08-31-ai-questionnaire-ecosystems.md (инкремент QE за сутки пустой)
```

**Не канон. Не PREF. Не выбор города (S04). Не визуальный язык (S06). Не токеномика (S07).**

Все hint ниже — предложения лаборатории, не решения.

## Knowledge Candidate — World / Interface tools (WI)

**Класс документа:** Knowledge Candidate / lab hint  
**Не является:** Foundation, PREF, решением World-PREF, реализацией Hermes, каталогом опросников QE-/HQ-  
**Серия ID:** WI-01… (не пересекается с QE-, HQ-, LAB-C-, LC-, LAB-D-)  
**Заказчик:** AICM HQ (Stabschef)  
**Дата доступа к источникам:** 2026-09-01  
**Горизонт фактов:** реально существующие продукты/спеки 2025–2026  
**Назначение:** автоматизация **и** интерфейс (viewport на операционную правду). Не «ещё один опросник».  
**Архивный слот (предложение имени файла):** `razvedka/2026-09-01-instrumenty-mir-i-avtomatizaciya.md`

Все AICM-hint ниже — **предложения лаборатории, не решения**. S01–S02 закрыты и не переоткрываются. S03 открыт (следующий). S04–S07 позже.

---

## 0. Как читать пакет

- Инструмент = **кандидат знания**, не идентичность AICM и не vendor-stack.
- Мир AICM растёт синхронно с системой; web — ранний viewport; семантика раньше визуальной метафоры; каноническая идентичность с несколькими проекциями; progressive disclosure; операционная реальность ≠ атмосфера ≠ история.
- MCP здесь — **allowlist портов инструментов**, не SaaS-идентичность AICM.
- Версии указаны только если они стоят на странице релиза/npm/TR на дату доступа. Если страница не дала номера — номер не выдуман.
- Опросниковый каталог `razvedka/2026-08-31-ai-questionnaire-ecosystems.md` (QE-A/B/C, HQ-01..08) **не дублируется**.

### Инкремент по опросникам vs 2026-08-31

Интервал — одни сутки. Отдельного нового опросникового продукта, который менял бы QE-/HQ-каталог, **не обнаружено**. Этот пакет про world/interface/automation, не про questionnaires.

### Закрытый мир (не противоречить, не переспрашивать)

Цифровая операционная среда; правда раньше зрелища; web как ранний viewport; путь к 2.5D/3D/immersive; реальные агенты как будущие обитатели; human-readable drill-down; systematic growth; standalone package discipline; open-ended карта без финальной схемы; event-backed emergent growth; domain-agnostic capability grammar; operational reality vs atmosphere vs history; chronology / memory-places / self-documentation; semantic reason before visual metaphor; canonical identity + multiple projections; progressive disclosure и scale legibility; evolutionary restructuring без стирания lineage; small extensible conceptual core; semantic continuity across views/clients.

S03 (NEXT, не закрывать): persistent agent identity across versions/models/roles; inhabitants/teams/orgs; presence; biography/achievements/evidence; lineage merge/split/retirement; owner/agent interaction within governance.

---

## 1. Идентичность / присутствие / биография / орг-карта агентов

### WI-01 — W3C Decentralized Identifiers (DIDs) v1.1
- **URL:** https://www.w3.org/TR/did-1.1/  
- **Лицензия:** W3C Software and Document License (спецификация, не продукт)  
- **OSS / SaaS:** открытый стандарт  
- **Проверено 2026-09-01:** Candidate Recommendation Snapshot, **05 March 2026**. На дату доступа **ещё не W3C Recommendation**. Комментарии принимались минимум до 05 April 2026. Снимок: https://www.w3.org/TR/2026/CR-did-1.1-20260305/

DID — стабильный идентификатор субъекта (человек, агент, сервис), который резолвится в DID Document: ключи, методы проверки, service endpoints, без обязательного «профиля личности» внутри идентификатора. Это не каталог агентов, не UI мира и не блокчейн-обязанность: метод `did:web` живёт на обычном HTTPS и не требует токеномики. Это не Verifiable Credentials сами по себе (VC — отдельные утверждения, которые можно повесить на DID). Для AICM это грамматический кандидат канонической идентичности обитателя, переживающей смену модели, роли и версии рантайма — ровно тема S03, ещё не закрытая. Ledger-якорение DID **не** предлагается: оно тащит spectacle и tokenomics, закрытые на S07. Практический hint: канонический ID агента + проекции (каталог, карта, след), а не «аватар как идентичность».

- **AICM hint (proposal):** S03 persistent identity / lineage; каноническая идентичность с несколькими проекциями.  
- **Риск:** выбор DID-метода с ledger/tokenomics; путать DID с «паспортом личности»; принимать CR за Recommendation.

### WI-02 — AGNTCY Identity Service + Agent Directory
- **URL:** https://agntcy.org/ · Identity: https://github.com/agntcy/identity-service · docs: https://identity-docs.outshift.com/docs/intro/ · SaaS-проба: https://agent-identity.outshift.com/  
- **Лицензия репо identity-service:** Apache-2.0 (GitHub, 2026-09-01)  
- **OSS / SaaS:** OSS-стек (LF Projects) + hosted Identity у Outshift/Cisco  
- **Проверено 2026-09-01:** проект публично жив; репозиторий `agntcy/identity-service` создан 2025-09-18, Apache-2.0; PoC TBAC открыт 2026-04. Версию «GA продукта» на дату доступа не фиксируем — это молодой стек.

AGNTCY позиционирует «Internet of Agents»: directory (обнаружение), identity (бейджи/VC), messaging, observability. Identity Service регистрирует MCP-серверы, A2A-агентов и OASF-сущности, проверяет бейджи, навешивает Task-Based Access Control. Это не мир AICM и не Foundation: это **намёк на каталог обитателей и портов**, который можно изучать, не принимая Cisco/Outshift как идентичность системы. Directory — federated registry, не org-chart HQ. Hosted SaaS — удобная проба, не operational truth. Для S03 полезны идеи: бейдж ≠ биография; issuer/accountability; capability metadata отдельно от presence.

- **AICM hint (proposal):** S03 inhabitants/orgs/identity; MCP как allowlist-порт (не SaaS-id).  
- **Риск:** vendor-identity (Cisco/Outshift/LF branding); cloud-only hosted path; смешать directory с PREF.

### WI-03 — Backstage Software Catalog
- **URL:** https://backstage.io/docs/features/software-catalog/ · репо: https://github.com/backstage/backstage  
- **Лицензия:** Apache-2.0 (CNCF Incubation)  
- **OSS / SaaS:** OSS; коммерческие обёртки (Spotify Portal и др.) отдельно  
- **Проверено 2026-09-01:** релиз **v1.54.6** (2026-08-28). Каталог — YAML-метаданные в git, сущности Component/API/Resource/User/Group, ownership, TechDocs.

Backstage — внутренний каталог софта и владельцев, не игровой мир и не CMDB всего предприятия. Сущность описывается файлом рядом с кодом; каталог собирает, показывает ownership, связи, документы. Это близко к «орг-карте обитателей + каноническая карточка», если агент/пайплайн/viewport считать Component с owner-ом. Это не presence-протокол и не биография: нет встроенной «жизни агента», есть metadata + plugins. Spotify Portal — SaaS-надстройка, её не ставить идентичностью. Для AICM: карточка обитателя как catalog entity, drill-down в TechDocs, ownership как governance, **без** принятия IDP-UX Spotify как языка мира.

- **AICM hint (proposal):** S03 org/inhabitants; S01 human-readable drill-down; self-documentation.  
- **Риск:** IDP-vendor lock (Spotify plugins); YAML-каталог ≠ operational twin; раздуть Backstage до «всего AICM».

### WI-04 — OpenTelemetry (traces как evidence)
- **URL:** https://opentelemetry.io · spec: https://github.com/open-telemetry/opentelemetry-specification · GenAI conventions: https://github.com/open-telemetry/semantic-conventions-genai  
- **Лицензия:** Apache-2.0  
- **OSS / SaaS:** OSS (CNCF); бэкенды (Jaeger/Tempo/облака) сменны  
- **Проверено 2026-09-01:** спецификация и SDK живы. В **июне 2026** (`semantic-conventions` v1.42.0, 2026-06-12) `gen_ai.*` вынесены в отдельный репо; на июль–август 2026 **ни один GenAI-атрибут не Stable** (Development). PR Audit Logging (OTEP/spec PR #5059) — **Development**, не shipped-сигнал. Номер «последней spec» здесь не фиксируем без тега, который мы сами открыли на TR.

OTel — транспорт и корреляция: trace_id/span_id, логи, метрики. Это **не** биография агента и не память. Это кандидат слоя *evidence*: «это действие произошло, вот след». GenAI semantic conventions описывают invoke_agent / execute_tool, но схема ещё плывёт — нельзя делать канон AICM на `gen_ai.*`. Audit-signal с подписями — черновик; operational traces ≠ compliance receipt. Hint: каноническая идентичность ссылается на trace как на доказательство достижения, а не наоборот.

- **AICM hint (proposal):** S03 biography/achievements/evidence; S02 chronology; позже S05 freshness.  
- **Риск:** принять experimental GenAI semconv за стандарт; vendor-backend (Datadog и т.п.) как «память мира»; sampling убивает evidence.

### WI-05 — Activity Streams 2.0 + ActivityPub
- **URL:** https://www.w3.org/TR/activitystreams-core/ · https://www.w3.org/TR/activitypub/ · репо протокола: https://github.com/w3c/activitypub  
- **Лицензия:** W3C Recommendation (стандарт)  
- **OSS / SaaS:** открытый протокол; реализации разнообразны  
- **Проверено 2026-09-01:** AS2 и ActivityPub остаются W3C Recommendation (AS2; AP от 23 January 2018). Social Web WG переутверждена в январе 2026 (чартер до 31 January 2028); в марте–апреле 2026 WG взяла drafts на maintenance. FEP-82f6 Actor Statuses — **DRAFT** (получен 2025-05-12; финализация ожидалась ~2026-03-18, на дату доступа стандартного presence в Fediverse нет).

AS2 — JSON-LD словарь действий (Create/Update/Follow/Announce) и акторов. ActivityPub добавляет inbox/outbox. Это кандидат **activity stream обитателя** и слабого presence, не карта мира и не DID. FEP-82f6 показывает, что «статус на профиле» ещё не стандарт — не закрывать S03 этим. Не строить AICM как Mastodon. Полезно: лента достижений/событий как first-class feed, отдельный от operational twin и от атмосферы.

- **AICM hint (proposal):** S03 presence/biography; S02 chronology / memory-places.  
- **Риск:** соцсеть-spectacle; путать федерацию с истиной; строить identity на незакрытом FEP.

---

## 2. Progressive disclosure / multi-scale / knowledge canvas

### WI-06 — XYFlow / React Flow
- **URL:** https://reactflow.dev/ · https://xyflow.com · npm: https://www.npmjs.com/package/@xyflow/react  
- **Лицензия ядра:** MIT; Pro-примеры — отдельная xyflow Pro License  
- **OSS / SaaS:** OSS-библиотека + платный Pro-контент  
- **Проверено 2026-09-01:** `@xyflow/react` **12.11.5**, npm updated **2026-08-25**. Terms of Use страница xyflow помечена last updated **April 29, 2026**.

Библиотека node-based UI: граф сущностей, zoom/pan, кастомные ноды, свернуть/развернуть. Это не база знаний и не карта Земли. Это сменный web-viewport для **семантического графа** (агенты, пайплайны, зависимости) с progressive disclosure. Pro-подписка не нужна для ядра. Не делать React Flow «языком мира» (S06 закрыт позже): это проекция, не канон.

- **AICM hint (proposal):** S01 viewport / drill-down; позже S04 search/jump/zoom как граф, не как город.  
- **Риск:** UI-lock на React; Pro-примеры как скрытый vendor; зрелище графа вместо семантики.

### WI-07 — Excalidraw
- **URL:** https://excalidraw.com · https://github.com/excalidraw/excalidraw · npm: https://www.npmjs.com/package/@excalidraw/excalidraw  
- **Лицензия редактора:** MIT  
- **OSS / SaaS:** OSS embed + hosted excalidraw.com + платный Excalidraw+  
- **Проверено 2026-09-01:** GitHub-релиз **v0.18.1** (2026-04-20); npm `@excalidraw/excalidraw` **0.18.1**.

Ручной infinite whiteboard, JSON-формат `.excalidraw`, embed через npm. Это **атмосфера/скетч**, не operational truth. Закрытый мир требует: операционная реальность vs атмосфера vs история — раздельно. Excalidraw годится как слой набросков поверх канона, не как хранилище близнецов. Hosted excalidraw.com ≠ self-host. Не ставить hand-drawn aesthetic визуальным языком AICM (S06).

- **AICM hint (proposal):** S01 web viewport (вторичная проекция); не S02-истина.  
- **Риск:** spectacle; SaaS+; скетч как «карта мира».

### WI-08 — tldraw SDK
- **URL:** https://tldraw.dev · лицензия: https://tldraw.dev/community/license · ключи: https://tldraw.dev/sdk-features/license-key  
- **Лицензия:** tldraw License (source available, **не OSI OSS**). Старые 1.x — MIT (заморожены); часть pre-2.x — Apache-2.0 (заморожены).  
- **OSS / SaaS:** source-available SDK; production требует trial/hobby/commercial key  
- **Проверено 2026-09-01:** docs: default terms = только development; production — trial 100 дней / commercial / hobby с watermark. Ключ проверяется на клиенте.

Сильный infinite canvas для React, но **не** свободный кирпич пакета AICM. Hobby оставляет watermark («made with tldraw») — spectacle. Trial пингует сервера лицензии. Это hint «как выглядит progressive canvas», не кандидат Foundation. Предпочесть MIT XYFlow/Excalidraw, если нужен embed без ключа.

- **AICM hint (proposal):** только как референс UX для S01 disclosure; не порт идентичности.  
- **Риск:** vendor license lock; watermark; production-key; не OSS.

### WI-09 — Observable Framework
- **URL:** https://observablehq.com/framework/ · npm: https://www.npmjs.com/package/@observablehq/framework  
- **Лицензия:** ISC (npm)  
- **OSS / SaaS:** OSS static site generator; Observable Cloud **DEPRECATED** (docs 2026-09-01)  
- **Проверено 2026-09-01:** npm **1.13.4**, GitHub tag v1.13.4 (**2026-03-02**); npm updated **2026-04-06**.

SSG для data apps: Markdown + JS + data loaders на любом языке, статическая сборка, DuckDB/Plot/D3 на клиенте. Это не canvas-whiteboard и не близнец. Это web-first **читаемый drill-down** и self-documentation операционных срезов. Cloud deprecated — плюс к standalone discipline: хостить статику самим. Не путать с Observable Notebooks/Canvases (SaaS).

- **AICM hint (proposal):** S01 viewport; S02 self-documentation; ingest → статические снимки правды.  
- **Риск:** JS-эстетика как visual language; остатки Observable Cloud; notebooks SaaS.

### WI-10 — deck.gl (и kepler.gl как сосед)
- **URL:** https://deck.gl · https://github.com/visgl/deck.gl · kepler: https://docs.kepler.gl/  
- **Лицензия deck.gl:** MIT  
- **OSS / SaaS:** OSS (vis.gl / OpenJS)  
- **Проверено 2026-09-01:** deck.gl **9.3.6** (changelog **2026-07-02**; npm 9.3.6 на дату доступа). kepler.gl **3.2.6** (2026-03-16) стабилен; **3.3.0-alpha.3** (2026-07-12) — переход на deck.gl 9, не GA.

GPU-слои для больших гео/абстрактных наборов: точки, дуги, grid, tiles. Это масштабируемый viewport, не «город AICM» (S04 не закрывать). kepler — explorer поверх deck.gl, удобен людям, но 3.3 ещё alpha. Не выбирать visual language. Не путать lon/lat с топологией мира: гео — одна проекция канона.

- **AICM hint (proposal):** S01 multi-scale map; позже S04 zoom без решения «город vs campus».  
- **Риск:** geo-spectacle; Mapbox-ключ как lock-in; alpha kepler 3.3 в проде.

### WI-11 — Infinity Maps
- **URL:** https://infinitymaps.io/en/imapping-method/ · тариф Unlimited: https://infinitymaps.io/en/product/unlimited-subscription-yearly/  
- **Лицензия:** проприетарный SaaS (Infinity Maps GmbH, DE)  
- **OSS / SaaS:** SaaS; Enterprise — cloud **или** локальная установка (заявлено в публичных обзорах тарифов)  
- **Проверено 2026-09-01:** сайт жив; yearly Unlimited **149,99€ incl. VAT / year**. Бесплатный план ограничен картами/карточками. Исходников OSS нет.

Единственная коммерческая реализация iMapping: бесконечный nested zoom, карточки в карточках, связи. Класс «Infinity Maps» полезен как **референс scale legibility**, не как стек AICM. Данные в чужом облаке (DE) противоречат standalone package discipline, пока нет своей установки. Не закрывать S04 «вложенные миры» покупкой SaaS.

- **AICM hint (proposal):** референс UX для S01/S04 nested disclosure; не Foundation.  
- **Риск:** cloud-only default; vendor lock; нет OSS-экспорта как канона (JSON export — не идентичность).

### WI-12 — Obsidian Canvas
- **URL:** https://obsidian.md  
- **Лицензия:** проприетарный бинарь; личное/коммерческое использование бесплатно по публичному FAQ; Sync/Publish — подписка; commercial license поощряется (~$50/user/year, без жёсткого enforcement в публичном FAQ)  
- **OSS / SaaS:** не OSS; local-first файлы Markdown  
- **Проверено 2026-09-01:** продукт жив; Canvas — штатная бесконечная доска. Точный номер публичного релиза с сайта Obsidian здесь не фиксируем (вторичные обзоры расходятся: public vs Catalyst). Logseq как canvas **не берём в основной каталог**: split OG (Whiteboard, без фич с Dec 2025) vs DB (Whiteboard нет natively).

Obsidian Canvas — локальные `.canvas` + Markdown, хорош как human thinking surface. Это не operational twin и не агентный org-chart. Local-first близок к package discipline, но проприетарный клиент не должен стать viewport-идентичностью AICM. Плагины (в т.ч. Excalidraw) — ещё один lock на экосистему.

- **AICM hint (proposal):** личная лаборатория S01/S02; не клиент мира.  
- **Риск:** proprietary client; plugin-lock; путать vault с каноном.

---

## 3. Digital twin / operational world / entity graph

### WI-13 — Eclipse Ditto
- **URL:** https://eclipse.dev/ditto/ · репо: https://github.com/eclipse-ditto/ditto · 3.9.6 notes: https://eclipse.dev/ditto/release_notes_396.html  
- **Лицензия:** EPL-2.0  
- **OSS / SaaS:** OSS (Eclipse IoT)  
- **Проверено 2026-09-01:** **3.9.6** выпущена **2026-07-28** (bugfix после 3.9.5); Helm chart appVersion 3.9.6. 3.9.0 (2026-05-13) — WoT Discovery, namespace-scoped policies.

Digital twin: вещь (Thing) с атрибутами, features, политиками, событиями — виртуальный двойник физического/логического объекта. Это **viewport на операционную правду**, не game world. Не метавселенная. Для AICM: паттерн «канонический объект + проекции + политика», live-состояние отдельно от истории. Java/Akka-операционка тяжёлая для маленького пакета — hint архитектуры, не обязательный runtime.

- **AICM hint (proposal):** operational reality vs history; ingest; позже S05 permissions/freshness.  
- **Риск:** IoT-vendor gravity (Bosch и др.); тяжелый кластер; twin как «игра».

### WI-14 — TerminusDB
- **URL:** https://terminusdb.org/ · https://github.com/terminusdb/terminusdb · Enterprise: https://terminusdb.org/docs/enterprise/  
- **Лицензия ядра:** Apache-2.0; Enterprise (DFRNT TwinfoxDB) — коммерческое  
- **OSS / SaaS:** OSS graph+document DB + git-for-data; cloud/enterprise отдельно  
- **Проверено 2026-09-01:** сайт: v12 вышла **2025-12-08**; GitHub latest **v12.0.7** (**2026-08-10**). README «Project Overview (Updated May 2026)».

Схема, документы, граф, коммиты данных как git. Это ближе к **канону сущностей с lineage**, чем vis-canvas. Не игровой мир. DFRNT Enterprise — аддитивный, не меняет OSS-поведение, но vendor. High-precision math / temporal reasoning заявлены для industrial/finance — релевантно экономической разведке как **данные**, не live trading. Не ставить Terminus идентичностью AICM.

- **AICM hint (proposal):** канонический граф; S02 chronology (коммиты); ingest.  
- **Риск:** DFRNT enterprise lock; Prolog-стек как скрытая сложность; git-for-data ≠ wiki людей.

### WI-15 — NetBox
- **URL:** https://github.com/netbox-community/netbox · https://netboxlabs.com/products/netbox/  
- **Лицензия ядра:** Apache-2.0; часть add-on NetBox Labs — Polyform Shield (source-available)  
- **OSS / SaaS:** OSS Community + Cloud/Enterprise  
- **Проверено 2026-09-01:** стабильный **v4.6.9** (**2026-08-25**); **v4.7.0-beta2** (2026-08-26) не для продакшена.

Source of truth для сети: сайты, устройства, IP, кабели — intended state, не discovery. Урок для AICM: **CMDB-подобная модель + API**, человеческий UI, плагины. Не universal CMDB и не мир агентов. Не ServiceNow. Домен — сети; перенос паттерна (entity, desired state, ownership) важнее установки NetBox как HQ.

- **AICM hint (proposal):** operational viewport; S01 drill-down; позже S05 intended vs observed.  
- **Риск:** NetBox Labs add-on license; принять сетевой метафорой весь мир (S04).

### WI-16 — Apache AGE
- **URL:** https://age.apache.org/ · https://github.com/apache/age  
- **Лицензия:** Apache-2.0  
- **OSS / SaaS:** OSS PostgreSQL extension  
- **Проверено 2026-09-01:** тег **`PG18/v1.8.0-rc0`** опубликован **2026-07-09** — это **RC**, не утверждаем GA 1.8.0. Репозиторий заявляет поддержку Postgres 11–18.

openCypher поверх Postgres: вершины/рёбра рядом с реляционными таблицами. Кандидат **entity graph без отдельного Neo4j**. Не viewport. Не закрытый S04 spatial topology. RC нельзя ставить в Foundation. SQL/PGQ в будущем Postgres — наблюдать, не ждать.

- **AICM hint (proposal):** канонический граф в уже принятом Postgres-контуре (если появится); ingest.  
- **Риск:** RC; Cypher-lock vs SQL; путать граф хранения с картой мира.

---

## 4. Self-documentation / chronology / memory-places

### WI-17 — Wiki.js
- **URL:** https://js.wiki/ · https://github.com/requarks/wiki · релизы: https://docs.requarks.io/releases  
- **Лицензия:** AGPL-3.0  
- **OSS / SaaS:** self-host OSS  
- **Проверено 2026-09-01:** stable **2.5.314** (**2026-05-01**). **3.0 — alpha**, beta без ETA.

Wiki с опциональным Git-storage: страницы как Markdown, двухсторонний sync с git. Self-documentation и человеческая история решений. AGPL обязывает при network-distribution — учитывать package discipline. 3.0 не готов: не строить на alpha. Git здесь — хроника текста, не evidence агента.

- **AICM hint (proposal):** S02 self-documentation / chronology.  
- **Риск:** AGPL; застрять на 2.x vs 3.0; wiki как «истина» вместо twin.

### WI-18 — Evidence (evidence.dev)
- **URL:** https://evidence.dev · docs: https://docs.evidence.dev/ · https://github.com/evidence-dev/evidence  
- **Лицензия ядра:** MIT; Evidence Studio — hosted  
- **OSS / SaaS:** OSS Core (static) + Studio  
- **Проверено 2026-09-01:** репозиторий MIT, активен; Core vs Studio явно разделены в docs.

BI-as-code: SQL внутри Markdown → статический отчёт. Близко к Observable Framework, но отчёт/метрика, не произвольный canvas. Agent-ready в маркетинге 2026 — не принимать «Evidence Agent» идентичностью. Self-host Core совместим со standalone discipline.

- **AICM hint (proposal):** S02 self-doc; S01 drill-down чисел; не S03 identity.  
- **Риск:** Studio SaaS; warehouse-lock; «AI agent» маркетинга.

### WI-19 — vis-timeline
- **URL:** https://visjs.github.io/vis-timeline/ · https://github.com/visjs/vis-timeline · npm: https://www.npmjs.com/package/vis-timeline  
- **Лицензия:** Apache-2.0 OR MIT  
- **OSS / SaaS:** OSS библиотека  
- **Проверено 2026-09-01:** npm **8.5.4**, updated **2026-08-12**.

Интерактивная лента событий/интервалов. Это **проекция хронологии**, не хранилище памяти. Канон событий должен жить отдельно (логи, git, lineage); timeline — сменный вид. Не TimelineJS-нарратив как propaganda-spectacle.

- **AICM hint (proposal):** S02 chronology viewport.  
- **Риск:** UI как единственная история; vis.js community bus-factor.

### WI-20 — OpenLineage
- **URL:** https://openlineage.io · https://github.com/OpenLineage/OpenLineage · docs 1.52.0: https://openlineage.io/docs/  
- **Лицензия:** Apache-2.0  
- **OSS / SaaS:** открытый стандарт + библиотеки; бэкенды сменны  
- **Проверено 2026-09-01:** релиз **1.52.0** (**2026-07-23**). Marquez (reference UI) на дату доступа имеет **замедленный cadence** относительно спеки (публичные обзоры: последний артефакт 0.51.1 / 2025-03; не делать Marquez обязательным).

Стандарт событий lineage: Job / Dataset / Run. Кандидат **хроники производства знания** (пайплайны разведки), не org-chart агентов. Marquez не равен OpenLineage. Не data-catalog SaaS (DataHub Cloud и т.п.) как идентичность.

- **AICM hint (proposal):** S02 lineage/chronology; ingest; позже S05 freshness.  
- **Риск:** мёртвый reference-backend; путать data lineage с agent lineage (S03).

---

## 5. Автоматизация позади мира

### WI-21 — Model Context Protocol (MCP) spec 2026-07-28
- **URL:** https://modelcontextprotocol.io/specification/2026-07-28 · анонс: https://blog.modelcontextprotocol.io/posts/2026-07-28/ · LICENSE: https://github.com/modelcontextprotocol/modelcontextprotocol/blob/HEAD/LICENSE  
- **Лицензия:** переход MIT → Apache-2.0 для новых вкладов; docs (не spec) CC-BY-4.0; часть старого кода может оставаться MIT  
- **OSS / SaaS:** открытый протокол (LF Projects); серверы бывают любые  
- **Проверено 2026-09-01:** спецификация **2026-07-28** выпущена; stateless core, `server/discover`, заголовки `Mcp-Method`/`Mcp-Name`, Multi Round-Trip, deprecation Roots/Sampling/Logging ≥12 месяцев. Это **не продукт-SaaS**.

MCP — JSON-RPC порты инструментов. Для AICM: **allowlist tool ports**, через которые мир узнаёт о событиях и действия уходят в автоматизацию. Не идентичность агента (это S03/DID/каталог). Не «MCP Cloud». Stateless 2026 ломает session-id — учитывать при лабораторных адаптерах, не внедряя как Foundation.

- **AICM hint (proposal):** automation / ingest; tool ports; не identity.  
- **Риск:** SaaS MCP-магазины как lock-in; спутать server identity с agent identity; HITL-эскалации как скрытый owner-bot.

### WI-22 — Temporal
- **URL:** https://docs.temporal.io · https://github.com/temporalio/temporal · v1.31.2: https://github.com/temporalio/temporal/releases/tag/v1.31.2  
- **Лицензия сервера:** MIT  
- **OSS / SaaS:** OSS self-host + Temporal Cloud  
- **Проверено 2026-09-01:** server **v1.31.2** (**2026-07-08**), в т.ч. CVE-2026-5724.

Durable execution: workflow переживает падение воркера. Кандидат **event-backed growth и долгих разведциклов** позади мира, не UI. Cloud не нужен для hint. Не «агентский фреймворк» и не LangGraph. Сложность ops — цена; для лаборатории достаточно понять паттерн, не ставить кластер как AICM.

- **AICM hint (proposal):** automation / event-backed growth.  
- **Риск:** Cloud lock; workflow как скрытая идентичность агента; ops-тяжесть.

### WI-23 — NATS Server + JetStream
- **URL:** https://nats.io · https://github.com/nats-io/nats-server  
- **Лицензия:** Apache-2.0 (CNCF). Спор Synadia/BSL 2025 публично закрыт сохранением Apache-2.0 у nats-server.  
- **OSS / SaaS:** OSS binary; Synadia Cloud отдельно  
- **Проверено 2026-09-01:** **v2.14.6** (**2026-08-27**); v2.15.0-preview.1 — не GA.

Лёгкая шина: pub/sub, request/reply, JetStream persistence, KV. Кандидат **событийного роста мира** (событие → появление/изменение места), не Kafka-монолит. Не идентичность. Помнить 2025 license scare как риск single-vendor maintainer, даже при нынешнем Apache-2.0.

- **AICM hint (proposal):** event-backed growth; ingest.  
- **Риск:** Synadia relicensing memory; Cloud; путать шину с каноном.

---

## 6. Web-first 2.5D/3D viewports (S04/S06/S07 — не выбирать язык сейчас)

### WI-24 — Three.js
- **URL:** https://threejs.org/ · https://github.com/mrdoob/three.js · npm: https://www.npmjs.com/package/three  
- **Лицензия:** MIT  
- **OSS / SaaS:** OSS  
- **Проверено 2026-09-01:** сайт **r185**; npm **0.185.1** updated **2026-07-01**. WebXR через `WebXRManager`.

Сменный 3D/WebGPU viewport. Не мир, не metaverse, не tokenomics. Канон остаётся семантическим; Three.js — одна проекция. CSS3D/SVG addons — путь 2.5D без «игры».

- **AICM hint (proposal):** позже S04/S06/S07 как replaceable engine.  
- **Риск:** visual-language lock; game-feel; WebXR раньше срока.

### WI-25 — Babylon.js
- **URL:** https://www.babylonjs.com · npm: https://www.npmjs.com/package/@babylonjs/core  
- **Лицензия:** Apache-2.0  
- **OSS / SaaS:** OSS  
- **Проверено 2026-09-01:** `@babylonjs/core` **9.23.0** updated **2026-08-27**.

Более «движковый» стек, чем Three: сцены, XR, физика. Тот же статус: кандидат двигателя, не решение S06. Не ставить playground.babylonjs.com операционным миром.

- **AICM hint (proposal):** later replaceable 3D viewport.  
- **Риск:** engine identity; XR-spectacle.

### WI-26 — CesiumJS
- **URL:** https://cesium.com/platform/cesiumjs/ · npm: https://www.npmjs.com/package/cesium · релиз: https://github.com/CesiumGS/cesium/releases/tag/1.144  
- **Лицензия библиотеки:** Apache-2.0  
- **OSS / SaaS:** OSS движок; **Cesium ion** — облачные 3D-tiles/токены  
- **Проверено 2026-09-01:** **1.144.0** (**2026-08-03/04**). Quickstart по-прежнему предлагает `Cesium.Ion.defaultAccessToken`.

Глобус, terrain, 3D Tiles — если когда-нибудь понадобится гео-проекция экономической картины. Не город агентов. Ion-токен не должен стать зависимостью канона: библиотека работает и без ion, ion — удобство/данные.

- **AICM hint (proposal):** later S04 geo-topology как одна проекция.  
- **Риск:** ion cloud lock; «глобус = мир AICM».

### WI-27 — WebXR Device API
- **URL:** https://www.w3.org/TR/webxr/ · практика: Three `WebXRManager`, Babylon XR  
- **Лицензия:** W3C spec  
- **OSS / SaaS:** стандарт браузера  
- **Проверено 2026-09-01:** API реально поддерживается движками WI-24/25. Отдельный «номер продукта» не применим. S07 (immersive/metaverse) **не закрывать** и не внедрять.

Стандарт сессии VR/AR в браузере. Кандидат будущего immersive viewport при сохранённой семантической непрерывности. Не причина строить метавселенную сейчас. Не tokenomics, не аватар-маркетплейс.

- **AICM hint (proposal):** только later S07; путь от web viewport.  
- **Риск:** premature immersive; hardware lock; spectacle.

---

## 7. Свежие 2026-новинки (не опросники)

### WI-28 — Langfuse
- **URL:** https://langfuse.com · OSS handbook: https://langfuse.com/handbook/chapters/open-source · press: https://langfuse.com/press  
- **Лицензия:** MIT ядро; `/ee` (SCIM, расширенный audit, retention) — коммерческое  
- **OSS / SaaS:** self-host MIT + Cloud  
- **Проверено 2026-09-01:** ClickHouse **приобрёл** Langfuse **январь 2026**; публично обещают сохранить MIT/self-host. Номер «v4 GA» не фиксируем. OTel-ориентированные SDK упоминаются в пресс-таймлайне 2025–2026.

Трейсы, evals, промпты, датасеты — **качество и след агентных циклов**, не память-идентичность и не мир. Полезно как лаборатория evidence/evals до S03-биографии. Не ставить Langfuse Cloud каноном. Не путать с Mem0/Letta (память как SaaS-id — в стоп-листе). ClickHouse-acquisition — наблюдать license drift.

- **AICM hint (proposal):** S03 evidence; evals; не identity, не viewport.  
- **Риск:** Cloud; EE-модули; vendor после M&A; HITL annotation queues как owner-bot.

---

## 8. Стоп-лист (плохая посадка на AICM)

Одна строка «почему» — чтобы HQ не тащил это в World/Hermes.

| # | Что | Почему стоп |
|---|-----|-------------|
| 1 | LangGraph / LangChain как «AICM» | Запрет vendor-stack identity; граф рантайма ≠ канон мира |
| 2 | CrewAI | То же: ролевая оркестрация как подмена обитателей S03 |
| 3 | Letta / MemGPT | Прямой запрет как identity; память-продукт ≠ persistent agent |
| 4 | Microsoft Agent Framework (MAF) | Запрет vendor identity; облачный гравитационный колодец |
| 5 | Bitget / любой live CEX-trading | Запрет live trading; не viewport данных |
| 6 | Decentraland / The Sandbox / Roblox / Second Life | Metaverse-spectacle; tokenomics; не operational truth |
| 7 | Unity / Unreal как первый клиент | Ломает web-first и replaceable viewport; engine-lock S06 |
| 8 | Virtuals Protocol и agent-coins | Premature tokenomics (S07); идентичность = токен |
| 9 | n8n как «мозг AICM» | Fair-code + HITL-SaaS gravity; автоматизация не идентичность |
| 10 | ServiceNow / Salesforce CMDB | Enterprise SaaS lock; не standalone package |
| 11 | Miro / FigJam / Lucid | Canvas-SaaS как ложная карта мира |
| 12 | Mem0 Platform / Zep Cloud как слой памяти AICM | Memory-as-SaaS identity; канон уходит к вендору |
| 13 | OpenAI GPT Store / Custom GPTs | Чужой каталог обитателей; нет канонической идентичности HQ |
| 14 | Logseq DB/OG как world canvas | Split 2025–2026: OG без фич, DB без native Whiteboard — нестабильный субстрат |

---

## 9. Сводка hint → слоты (не решения)

| Слот | WI (proposal) |
|------|----------------|
| S03 identity / org / presence / evidence | WI-01 DID, WI-02 AGNTCY, WI-03 Backstage, WI-04 OTel, WI-05 AS2/AP, WI-28 Langfuse |
| S01 web viewport / disclosure | WI-06 React Flow, WI-07 Excalidraw, WI-09 Observable Framework, WI-10 deck.gl |
| S02 chronology / self-doc | WI-17 Wiki.js, WI-18 Evidence, WI-19 vis-timeline, WI-20 OpenLineage, WI-14 коммиты |
| Operational twin / entity graph | WI-13 Ditto, WI-14 TerminusDB, WI-15 NetBox, WI-16 AGE |
| Automation / events / tool ports | WI-21 MCP, WI-22 Temporal, WI-23 NATS |
| Later S04/S06/S07 (не выбирать) | WI-10, WI-11 (референс), WI-24…27 |
| Референс only / опасный embed | WI-08 tldraw, WI-11 Infinity Maps, WI-12 Obsidian |

---

## 10. Provenance (доступ 2026-09-01)

| WI | Источник | Что подтверждено |
|----|----------|------------------|
| WI-01 | https://www.w3.org/TR/did-1.1/ · https://www.w3.org/TR/2026/CR-did-1.1-20260305/ | CR Snapshot 05 Mar 2026, ещё не Rec |
| WI-02 | https://agntcy.org/ · https://github.com/agntcy/identity-service · https://identity-docs.outshift.com/docs/intro/ | Apache-2.0 identity-service; hosted Outshift |
| WI-03 | https://backstage.io/docs/features/software-catalog/ · https://github.com/backstage/backstage/releases/tag/v1.54.6 | Apache-2.0, v1.54.6 (2026-08-28) |
| WI-04 | https://opentelemetry.io · https://github.com/open-telemetry/semantic-conventions-genai · https://github.com/open-telemetry/opentelemetry-specification/pull/5059 | Apache-2.0; GenAI conv. Development; Audit PR Development |
| WI-05 | https://www.w3.org/TR/activitystreams-core/ · https://www.w3.org/TR/activitypub/ · https://lists.w3.org/Archives/Public/public-socialweb/2026Jan/0000.html | Rec + WG recharter Jan 2026; FEP-82f6 draft |
| WI-06 | https://www.npmjs.com/package/@xyflow/react · https://reactflow.dev/ · https://xyflow.com/terms-of-use | MIT, 12.11.5, npm 2026-08-25 |
| WI-07 | https://www.npmjs.com/package/@excalidraw/excalidraw · https://github.com/excalidraw/excalidraw | MIT, v0.18.1 (2026-04-20) |
| WI-08 | https://tldraw.dev/community/license · https://tldraw.dev/sdk-features/license-key | не OSS; production key |
| WI-09 | https://observablehq.com/framework/ · https://www.npmjs.com/package/@observablehq/framework · https://github.com/observablehq/framework/releases/tag/v1.13.4 | ISC, 1.13.4 (2026-03-02); Cloud DEPRECATED |
| WI-10 | https://www.npmjs.com/package/deck.gl · https://github.com/visgl/deck.gl/blob/v9.3.6/CHANGELOG.md · https://docs.kepler.gl/changelog | deck.gl 9.3.6 (2026-07-02); kepler 3.3.0-alpha.3 (2026-07-12) |
| WI-11 | https://infinitymaps.io/en/imapping-method/ · https://infinitymaps.io/en/product/unlimited-subscription-yearly/ | SaaS жив, 149,99€/year Unlimited |
| WI-12 | https://obsidian.md | proprietary Canvas; Logseq split: https://logseq.io/page/b2ad9ce1-9cb7-4436-8083-54cb4516d324/df4dc09d-0a12-4c87-904e-22a9bf4c350a |
| WI-13 | https://eclipse.dev/ditto/release_notes_396.html · https://github.com/eclipse-ditto/ditto | EPL-2.0, 3.9.6 (2026-07-28) |
| WI-14 | https://terminusdb.org/ · https://github.com/terminusdb/terminusdb/releases | Apache-2.0, v12.0.7 (2026-08-10) |
| WI-15 | https://github.com/netbox-community/netbox/releases/tag/v4.6.9 | Apache-2.0 core, v4.6.9 (2026-08-25) |
| WI-16 | https://github.com/apache/age/releases/tag/PG18%2Fv1.8.0-rc0 · https://age.apache.org/ | Apache-2.0, **RC** 1.8.0-rc0 (2026-07-09) |
| WI-17 | https://docs.requarks.io/releases · https://github.com/requarks/wiki | AGPL-3.0, 2.5.314 (2026-05-01); 3.0 alpha |
| WI-18 | https://docs.evidence.dev/ · https://github.com/evidence-dev/evidence | MIT Core |
| WI-19 | https://www.npmjs.com/package/vis-timeline | Apache-2.0 OR MIT, 8.5.4 (npm 2026-08-12) |
| WI-20 | https://github.com/OpenLineage/OpenLineage/releases/tag/1.52.0 · https://openlineage.io/docs/ | Apache-2.0, 1.52.0 (2026-07-23) |
| WI-21 | https://modelcontextprotocol.io/specification/2026-07-28 · https://blog.modelcontextprotocol.io/posts/2026-07-28/ | spec 2026-07-28; license transition |
| WI-22 | https://github.com/temporalio/temporal/releases/tag/v1.31.2 | MIT, v1.31.2 (2026-07-08) |
| WI-23 | https://github.com/nats-io/nats-server/releases · https://pkg.go.dev/github.com/nats-io/nats-server/v2 | Apache-2.0, v2.14.6 (2026-08-27) |
| WI-24 | https://threejs.org/ · https://www.npmjs.com/package/three | MIT, r185 / 0.185.1 (2026-07-01) |
| WI-25 | https://www.npmjs.com/package/@babylonjs/core | Apache-2.0, 9.23.0 (2026-08-27) |
| WI-26 | https://github.com/CesiumGS/cesium/releases/tag/1.144 · https://www.npmjs.com/package/cesium | Apache-2.0, 1.144.0 (2026-08-03/04) |
| WI-27 | https://www.w3.org/TR/webxr/ | W3C WebXR Device API |
| WI-28 | https://langfuse.com/handbook/chapters/open-source · https://langfuse.com/press | MIT core; ClickHouse M&A Jan 2026 |

**Страницы, которые при прямом fetch не отдали тело в этом прогоне:** `https://www.w3.org/TR/did-1.1/` — timeout у fetch-провайдера; статус CR подтверждён повторным web-index и зеркалом https://www.w3.org/TR/did/upcoming/. Это **не 404**.

**404 на дату доступа:** не зафиксированы для URL из таблицы выше.

---

## 11. Чего пакет сознательно не делает

- Не переоткрывает S01–S02 и не закрывает S03–S07.
- Не предлагает LangGraph/CrewAI/Letta/MAF как AICM.
- Не предлагает live trading / Bitget.
- Не выбирает visual language и не строит metaverse.
- Не дублирует QE/HQ опросниковый каталог.
- Не является Foundation, PREF или Hermes-имплементацией.

**Конец пакета WI.**