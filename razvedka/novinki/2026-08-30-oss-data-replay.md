# Кандидат: открытый код, данные, replay/бэктест
Статус: Knowledge Candidate. Не Foundation. Не канон AICM. Не реализация Hermes. Не live. Не Bitget-бот.
Дата: 2026-08-30
Назначение: корм для позднейшего razvedka/novinki/. Не внедрять.
Метод: GitHub README/LICENSE + официальные доки, открытый HTML. X не трогали.
Provenance: URL + лицензия если видна. Цифры звёзд/версий — только с открытой страницы ACCESS 2026-08-30.
Слои Андреев/Радченко/Миша/Армен/Клевцов/TE/Zatulyviter — НЕ склеивать и не упоминать как гибрид.

ACCESS: 2026-08-30 (Europe/Zurich). Клонов нет. Датасеты не скачивались. GitHub API — rate limit; звёзды сняты с HTML GitHub (WebFetch).

---

## A. Движки replay / бэктест (код)

### A1. NautilusTrader
- **URL:** https://github.com/NautechSystems/nautilus_trader · доки https://nautilustrader.io/docs/ · каталог данных https://nautilustrader.io/docs/nightly/concepts/data
- **Лицензия:** LGPL-3.0 (LICENSE на master, GNU LGPL v3).
- **Звёзды (GitHub HTML, 2026-08-30):** 28 136.
- **Что делает:** Rust-ядро + Python control plane; одно event-driven ядро на research, детерминированный бэктест и live. Тики, котировки, бары, L1-L3 стакан; ParquetDataCatalog (DataFusion) для replay. Адаптеры CEX/DEX и традиционных площадок.
- **Чем НЕ является:** не готовый бот под одну биржу; не бесплатный дата-вендор. README обещает research-to-live parity — не дом live для AICM.
- **Дыра / ToS / paid:** данные в каталог нужно грузить самому (Binance CSV, Databento DBN и т.п. — лицензии данных отдельные). Nightly-доки may change without notice.

### A2. QuantConnect LEAN
- **URL:** https://github.com/QuantConnect/Lean · https://www.quantconnect.com/docs/v2/writing-algorithms/historical-data/history-requests · датасеты CLI https://www.quantconnect.com/docs/v2/lean-cli/datasets/quantconnect
- **Лицензия:** Apache-2.0 (LICENSE на master, Copyright 2014 QuantConnect Corporation).
- **Звёзды:** 21 412.
- **Что делает:** event-driven движок (C#/Python) для бэктеста, research и live. History API: trailing bars, date range, fill-forward, mapping/normalization фьючерсов.
- **Чем НЕ является:** не открытый рынок данных. Engine OSS; Dataset Market — платный слой. Облако QuantConnect — отдельный SaaS.
- **Дыра / ToS / paid:** локальный LEAN без купленных/своих файлов не воспроизводит облачный бэктест. Crypto есть, но дом площадки страница не назначает.

### A3. vectorbt (OSS) vs VectorBT PRO
- **URL OSS:** https://github.com/polakowo/vectorbt · https://vectorbt.dev/ · PRO https://vectorbt.pro/
- **Лицензия OSS:** Apache-2.0 + Commons Clause v1.0 (LICENSE.md на master). SPDX чистого Apache-2.0 нет. Бейдж README: Fair Code. Запрет Sell продукта, чья ценность существенно от функциональности vectorbt. PRO: закрытый репозиторий, членство.
- **Звёзды OSS:** 8 922.
- **Что делает:** векторный бэктест (NumPy/Numba, опционально Rust vectorbt-rust); тысячи конфигов сразу. README: open-source community edition of VectorBT PRO.
- **Чем НЕ является:** не event-driven replay стакана; не live-движок. PRO — не OSS.
- **Дыра / ToS / paid:** Commons Clause режет коммерческий SaaS на базе OSS. Python >=3.11,<3.15 в pyproject.toml.

### A4. backtesting.py
- **URL:** https://github.com/kernc/backtesting.py · https://kernc.github.io/backtesting.py/
- **Лицензия:** AGPL-3.0 (LICENSE.md + setup.py license AGPL-3.0).
- **Звёзды:** 8 915.
- **Что делает:** простой барный бэктест стратегий на Python (OHLCV). Python 3.9+.
- **Чем НЕ является:** не tick/order-book replay; не production matching engine.
- **Дыра / ToS / paid:** AGPL — сеть/сервис обязывает открывать модификации. Данные — свои.

### A5. backtrader
- **URL:** https://github.com/mementum/backtrader
- **Лицензия:** GPL-3.0 (LICENSE на master — GNU GPL v3). README.rst подтверждает GPL-бейдж.
- **Звёзды:** 23 023.
- **Что делает:** классический Python-бэктест + исторические live-адаптеры (IB, Oanda). CSV/pandas-фиды, мульти-дата, Cerebro.
- **Чем НЕ является:** не современный tick-replay стакана. README сам тянет YahooFinanceData — для AICM красный флаг (Yahoo ToS: automated collection forbidden).
- **Дыра / ToS / paid:** GPL-3 copyleft. Last-commit с HTML GitHub в этом прогоне не снят. Не класть Yahoo-фид.

### A6. Jesse
- **URL:** https://github.com/jesse-ai/jesse · https://docs.jesse.trade/
- **Лицензия:** MIT (LICENSE, Copyright 2020 Jesse.Trade).
- **Звёзды:** 8 398.
- **Что делает:** crypto-фреймворк: research, бэктест без look-ahead на нескольких ТФ/символах, optimize (Optuna/Ray), Monte Carlo, self-hosted dashboard; также live.
- **Чем НЕ является:** не нейтральный только-research движок. README: backtesting, optimizing, and live trading.
- **Дыра / ToS / paid:** live-режим не дом AICM. Свечи обычно с биржевого REST (ToS биржи отдельно).

### A7. Freqtrade
- **URL:** https://github.com/freqtrade/freqtrade · бэктест https://www.freqtrade.io/en/stable/backtesting/
- **Лицензия:** GPL-3.0 (LICENSE на develop).
- **Звёзды:** 53 832.
- **Что делает:** open-source crypto trading bot (README) с полноценным freqtrade backtesting, hyperopt, download-data через ccxt. Доки фиксируют допущения (open/high/low внутри свечи, стоп vs ROI, timeframe-detail).
- **Чем НЕ является:** не только бэктест. Это live/dry-run бот; бэктест — модуль. Не класть как дом исполнения.
- **Дыра / ToS / paid:** GPL-3. Disclaimer educational. Список бирж README включает Binance/Bybit/OKX и др. — перечень коннекторов, не выбор дома AICM. Бот под конкретную площадку в этом пакете не строится.

### A8. Microsoft Qlib
- **URL:** https://github.com/microsoft/qlib · https://qlib.readthedocs.io/
- **Лицензия:** MIT (LICENSE на main, Copyright Microsoft Corporation).
- **Звёзды:** 48 101.
- **Что делает:** AI-oriented quant platform (SL / market-dynamics / RL), пайплайн идея-модель-бэктест, в основном акции (CN/US research stack). RD-Agent рядом, не обязателен.
- **Чем НЕ является:** не crypto matching engine; не tick-replay стакана. Не универсальный биржевой бот.
- **Дыра / ToS / paid:** данные Qlib (Yahoo/провайдеры) — отдельные ToS; Yahoo scrape не брать.

### A9. pmorissette/bt
- **URL:** https://github.com/pmorissette/bt
- **Лицензия:** MIT (LICENSE, Copyright 2015 Philippe Morissette).
- **Звёзды:** 2 971.
- **Что делает:** гибкий портфельный бэктест (деревья аллокаций, rebalance), не барный скальп.
- **Чем НЕ является:** не order-book; не crypto-native; не live.
- **Дыра / ToS / paid:** качество = качество входных рядов.

### A10. Zipline Reloaded
- **URL:** https://github.com/stefan-jansen/zipline-reloaded · https://zipline.ml4trading.io
- **Лицензия:** Apache-2.0 (LICENSE на main; Copyright 2018 Quantopian, Inc. в тексте Apache).
- **Звёзды:** 1 931.
- **Что делает:** event-driven Pythonic бэктест (форк Quantopian Zipline), поддерживается stefan-jansen / ML4T.
- **Чем НЕ является:** не Quantopian (закрыт). Не бесплатный US-equity tape. Не tick-L3.
- **Дыра / ToS / paid:** ingest данных — свой; не yfinance.

### A11. Hummingbot — с оговоркой
- **URL:** https://github.com/hummingbot/hummingbot
- **Лицензия:** Apache-2.0 (LICENSE, Copyright 2023 Hummingbot Foundation).
- **Звёзды:** 19 705.
- **Что делает:** live HFT/MM клиент. Strategy V2: BacktestingEngineBase / BacktestingDataProvider гоняет исторические OHLCV-свечи через ту же логику контроллеров (скрипты scripts/backtest_*.py).
- **Чем НЕ является:** не tick/L2 replay. Не класть как nautilus-класс replay стакана. Paper trade не равен historical replay.
- **Дыра / ToS / paid:** официальная страница hummingbot.org/strategies/backtesting/ в прогоне HTTP 404. Описание V2 — код GitHub; канон HTML доков не снят. Live MM — не дом AICM.

---

## B. Открытые / публичные рыночные данные (не FRED-архив, не Yahoo scrape)

### B1. CCXT
- **URL:** https://github.com/ccxt/ccxt
- **Лицензия:** MIT (LICENSE.txt, Copyright 2024 Igor Kroitor).
- **Звёзды:** 43 805.
- **Что делает:** библиотека единого REST/WS API к 100+ площадкам (публичные klines/trades/ticker без ключа на многих; приватное — ключи).
- **Чем НЕ является:** не дата-вендор, не исторический dump, не replay-движок.
- **Дыра / ToS / paid:** ToS каждой площадки отдельно. Rate limits. Не хранить ключи в intel.

### B2. Binance Vision / binance-public-data
- **URL данных:** https://data.binance.vision/ · репо https://github.com/binance/binance-public-data (звёзды 2 471)
- **Лицензия кода репо:** README секция Licence: MIT. Отдельного LICENSE файла на master — 404.
- **Что делает:** официальные daily/monthly zip: spot + USD-M/COIN-M, klines / aggTrades / trades. Spot timestamp с 2025-01-01 — микросекунды. SHA256 CHECKSUM рядом.
- **Чем НЕ является:** не L2 incremental book dump. Не все биржи.
- **Дыра / ToS / paid:** ссылка Terms of Use на data.binance.vision есть; полный текст ToS в прогоне — JS/bot wall (binance.com/terms HTTP 202 пусто; about-legal data-collection terms — JavaScript is disabled). Redistrib/коммерция не прочитаны. Архивы в этом прогоне не качались.

### B3. CoinGecko API (одна строка, без дубля market-context)
- **URL:** https://docs.coingecko.com/reference/introduction · API Terms https://www.coingecko.com/en/api_terms (HTML открыт 2026-08-30)
- **Лицензия данных:** не SPDX; limited licence на API. Кэш не поощряется; если кэш — refresh не реже 24h; terminate → delete Data. Except as expressly permitted — not allowed to duplicate, reproduce, copy, store, derive from or translate any Data.
- **Что делает / чем НЕ:** агрегатор, не лента биржи. Demo limits; not production уже в market-context. Не redistrib как свой tape. Не дублировать пакет календарей.

### B4. Coin Metrics Community
- **URL:** https://docs.coinmetrics.io/packages/coin-metrics-community-data · community API https://community-api.coinmetrics.io/v4 (ключ не нужен)
- **Лицензия (доки, 2026-08-30, индекс GitBook):** CC BY-NC 4.0 (Creative Commons Attribution-NonCommercial).
- **Что делает:** бесплатное подмножество Network/Market Data Pro: community metrics, Atlas 30 дней / limited assets, reference rates — last 7 points на мелких резолюциях. Лимит community: 10 req / 6 s / IP.
- **Чем НЕ является:** не полный Pro tape; не биржевой matching dump.
- **Дыра / ToS / paid:** прямая страница docs.coinmetrics.io/community/data — 404; полный HTML пакета в WebFetch timeout. NC = не коммерция без отдельной лицензии. Pro — paid.

### B5. CryptoDataDownload
- **URL:** https://www.cryptodatadownload.com/ (HTML открыт)
- **Лицензия:** SPDX на данные не видна. FAQ на той же странице: коммерция/academia yes; do not redistribute raw datasets to third parties; enterprise licensing для vendor-redistrib.
- **Что делает:** бесплатные CSV OHLCV (daily/hourly/1m, major venues с 2017, no login). Plus+ 39.99 USD/mo дашборды; API 79.99 USD/mo (112 endpoints); Quant Desk 149.99. Backtest Vault — преформат под MT/NT/TS/AmiBroker/Zipline/LEAN.
- **Чем НЕ является:** не tick L2; не официальный dump биржи. Агрегатор/склад.
- **Дыра / ToS / paid:** gap-fill/zero-gap — paid Plus+. Источник не биржа. Не зеркалить сырые CSV наружу.

### B6. Databento (SDK открыт, данные платные)
- **URL SDK:** https://github.com/databento/databento-python (звёзды 296) · доки https://databento.com/docs/quickstart
- **Лицензия SDK:** Apache-2.0 (LICENSE на master).
- **Что делает:** клиент к MBO/MBP/OHLCV/last sale; DBN; event-driven market replay в доках SDK. Нормализация live=historical.
- **Чем НЕ является:** данные не OA. SDK не датасет.
- **Дыра / ToS / paid:** pricing-страница — JS-заглушка (тарифы в HTML не сняты). Ключ API обязателен. Не путать с бесплатным Vision.

### B7. Bybit public klines
- **URL:** https://bybit-exchange.github.io/docs/v5/market/kline — HTML открыт.
- **Лицензия данных:** SPDX не видна (публичный REST, ToS площадки отдельно, полный ToS в этом прогоне не снимали).
- **Что делает:** GET /v5/market/kline — spot / linear / inverse; interval 1m…M; limit 1-1000 (default 200). Публичная история свечей.
- **Чем НЕ является:** не дом AICM; не L2 dump.
- **Дыра / ToS / paid:** пагинация/глубина истории на странице kline не расписана как полный архив. Rate limit — на других страницах.

### B8. OKX public history candles
- **URL:** https://www.okx.com/docs-v5/en/#order-book-trading-market-data-get-candlesticks-history
- **Лицензия данных:** SPDX не видна.
- **Что делает:** публичный GET /api/v5/market/history-candles?instId=BTC-USDT — Retrieve history candlestick charts from recent years (пример в HTML). Рядом GET /api/v5/market/candles — недавние.
- **Чем НЕ является:** не дом; не tick book.
- **Дыра / ToS / paid:** WebFetch этой якорной URL дал HTTP 500; curl HTML 200 (~5 MB SPA). Параметры limit/after в снятом сниппете таблицы не дочитаны до конца. Не строить клиента исполнения.

### B9. cryptofeed (в основном live)
- **URL:** https://github.com/bmoscon/cryptofeed
- **Лицензия:** не SPDX MIT-чистое: custom notice (copyright Bryant Moscon 2017-2025) + MIT-like disclaimer; бейдж README XFree86; обязательный acknowledgment в end-user docs.
- **Звёзды:** 2 890.
- **Что делает:** нормализованные websocket trades/book/ticker; REST poll если нет WS.
- **Чем НЕ является:** не исторический вендор; не replay-архив.
- **Дыра / ToS / paid:** ToS площадок на live-съём. Не замена Tardis/Vision.

### B10. Public REST одной доп. площадки — не верифицирован
Попытки bitget.com/api-doc/.../Get-History-Candle* редиректят на UTA intro (SPA). Не карточка данных. Freqtrade README перечисляет коннектор — не дом. Клиент исполнения не пишется.

---

## C. Order-book / tick replay (если отдельно от A/B)

### C1. Tardis.dev + tardis-python
- **URL:** https://tardis.dev/ · https://github.com/tardis-dev/tardis-python (звёзды 147) · доки клиента https://docs.tardis.dev/python-client/quickstart (README)
- **Лицензия клиента:** MPL-2.0 (LICENSE tardis-python master).
- **Что делает:** tick-by-tick replay L2/L3, trades, liquidations, funding, options chain; CSV + HTTP /data-feeds; tardis-machine (Docker/NPM) — локальный time-machine. Клиент: tardis_dev.replay.
- **Чем НЕ является:** не бесплатный полный архив. Real-time normalized stream через OSS-клиент к площадкам напрямую — на лендинге: free, no API key. Исторический replay CSV/API — подписка.
- **Дыра / ToS / paid:** лендинг (2026-08-30): Academic/Solo/Pro/Business; Perpetuals Solo 700 USD/мес, All Exchanges Solo 1 200 USD/мес, Business All 6 000 USD/мес; Academic yearly-only; min order 300 USD; By placing an order you agree to Tardis.dev Terms of Service. Tardis Machine replay APIs нет на Academic/Solo (прочерк в таблице). docs.tardis.dev/faq/general — timeout в этом прогоне.

### C2. Nautilus ParquetDataCatalog (указатель, не второй движок)
См. A1. Отдельно: каталог пишет/читает QuoteTick, TradeTick, OrderBookDelta, Depth10, Bar в Parquet; replay в BacktestNode сортирует по ts_init. Загрузчики: Binance order-book CSV, Databento DBN. Данные не прилагаются.

### C3. crypto-lake / lake-api
- **URL:** https://crypto-lake.com/ · https://github.com/crypto-lake/lake-api (звёзды 76) · https://lake-api.readthedocs.io
- **Лицензия SDK:** Apache-2.0 (LICENSE на main).
- **Что делает:** Python API к HF book snapshots (20 уровней), book_delta, trades, 1m candles, OI, funding. Sample: lakeapi.use_sample_data(anonymous_access=True). Полный доступ — paid + AWS credentials.
- **Чем НЕ является:** не OSS-датасет. SDK открыт, склад платный.
- **Дыра / ToS / paid:** sample не равен coverage. Склад в этом прогоне не качался.

### C4. LEAN Dataset Market (указатель)
См. A2. Tick/quote US equity/futures — покупка через CLI. Не путать с Apache-лицензией движка.

---

## Что не брать

- Школы, VIP, серые PDF, ключи площадок, live-клиент как дом исполнения (Freqtrade/Jesse/Hummingbot/Nautilus-live).
- FRED API ToS июнь 2024: нет AI/ML training и нет cache/archive API content (уже в local/intel/2026-08-30-market-context-open.md).
- Yahoo Finance ToS: automated collection forbidden; не yfinance, не backtrader Yahoo-фид.
- Stooq: JS wall, ToS не виден — red flag.
- BLS HTML 403 / bot-block.
- Календари FOMC/BEA/GDELT — другой срез (открытые ленты / market-context), не этот пакет.
- Closed school platforms / Tiger Trade — не OSS.
- pandas/numpy как движок, SkyPilot/exo.
- VectorBT PRO как будто OSS.
- Databento/Tardis/Lake данные как будто бесплатные, потому что SDK Apache/MPL.
- Зеркало сырых CSV CryptoDataDownload / CoinGecko Data.
- Одна площадка как дом; клиент исполнения под неё.
- Склейка слоёв стратегий в один гибрид.

---

## Дыры прогона

| Что | Статус 2026-08-30 |
|---|---|
| GitHub REST API | rate limit; звёзды с HTML WebFetch |
| polakowo/vectorbt/LICENSE (без .md) | 404; лицензия в LICENSE.md |
| kernc/backtesting.py/LICENSE | 404; есть LICENSE.md AGPL |
| Binance Vision полный ToS | JS wall |
| Coin Metrics community HTML | 404 старый путь; GitBook timeout; лицензия CC BY-NC снята с индексной страницы пакета |
| docs.tardis.dev/faq/general | timeout |
| Databento /pricing | JS, тарифы не прочитаны |
| OKX docs WebFetch | HTTP 500; curl 200 |
| history-candle HTML одной доп. площадки | SPA → UTA intro |
| hummingbot.org/strategies/backtesting/ | 404 |
| Last-commit/версия PyPI многих репо | не на бейдже GitHub HTML этого съёма (кроме Nautilus README: Rust 1.97.1, Python 3.12-3.14) |
| X/Twitter | не трогали (метод) |

---

Это каталог-кандидат, не сравнение слоёв стратегий.

