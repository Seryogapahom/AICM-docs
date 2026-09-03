# Knowledge Candidate — макро/новости: как публично читают календарь

ACCESS: 2026-09-03 (Europe/Zurich, UTC+2)
СТАТУС: Knowledge Candidate. Не Foundation. Не канон AICM. Не предиктор. Не слот механизма ≥60%. Не вход.
СЛОЙ: инкремент `from-grok/2026-09-03-crowd-layer.md` (журнал ожидание vs факт). Не новый ритм 10:00. Не второй Радченко. Не Дуглас. L0–L2 не трогать. Архив штаба в from-grok/. Live-торговля нет.
МЕТОД: открытый HTML/OA, без логина, X не звали.

**Честная рамка.** Предсказать ЧИСЛО релиза (NFP/CPI) и предсказать РЕАКЦИЮ рынка на сюрприз vs консенсус — разные задачи. В открытых текстах (Fed event-study, вендор PiT, nowcast FAQ) фонды чаще моделируют *surprise*, не «угадать принт». P&L не обещать. n мало → `INSUFFICIENT_SAMPLE`. Слои не клеить.

Уже снято (одна строка, не пересказ): календарь FOMC/BEA, три рамки новостей, Lucca–Moench — `razvedka/2026-08-30-market-context-open.md`. Журнал толпы ожидание/факт 4h/1d — `from-grok/2026-09-03-crowd-layer.md`.

---

## 1. Как фонды (публично) читают календарь

Не внутренности Citadel/Two Sigma: только то, что на странице.

**До принта = предупреждение, не вход.**
- Календарь ведущих стран говорит *когда* (FOMC 8×/год; ECB/BoE/BoJ — официальные даты; PBOC — не тот же ритм: LPR ~20-е число месяца + ежедневные OMO). Не торговое правило.
- Консенсус/nowcast говорит *что уже в цене как ожидание*. Bloomberg PiT (маркетинг, 7 May 2026): «macro strategies are fundamentally driven by expectation formation and the market’s response to new information»; три слоя данных — forward calendar / actuals+surveys / intraday changes of consensus.
- Узкое окно вокруг релиза нужно потому, что дневное окно смешивает макро-релиз и ответ ЦБ в тот же день (GSS: FOMC после employment report).

**После принта = подтверждение, не вход.**
- Сюрприз = факт − ожидание (опрос) **или** внутридневной сдвиг фьючерсов ставки (Kuttner/GSS) — это не одно и то же.
- Реакция 15m–4h–1d — журнал: совпало ли ожидание толпы / консенсус / nowcast с фактом и с ценой. Стык с crowd-layer, не замена. Гипотеза «подтверждение намерений» = расхождение ожидание толпы vs сюрприз vs цена; не if/then.
- Три рамки из market-context держать: (а) новости двигают, (б) новости не определяют тренд, (в) цена уже в ожидании. Победителя не выбирать.

Официальные календари (слой данных, не правила входа):
- FOMC: https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm — ACCESS 2026-09-03; 8 встреч; minutes +3 weeks; след. 15–16 Sep 2026 (SEP).
- ECB GC: https://www.ecb.europa.eu/press/calendars/mgcgc/html/index.en.html — ACCESS 2026-09-03; след. 9–10 Sep 2026 Berlin + press conference.
- BoE MPC: https://www.bankofengland.co.uk/monetary-policy/upcoming-mpc-dates — ACCESS 2026-09-03; след. 17 Sep 2026; Bank Rate на странице 3.75%.
- BoJ MPM: https://www.boj.or.jp/en/mopo/mpmsche_minu/index.htm + PDF расписания 31 Jul 2025 https://www.boj.or.jp/en/mopo/mpmsche_minu/m_ref/mref250731a.pdf — 8 MPM/год; след. 17–18 Sep 2026 (HTML BoJ в этом прогоне timeout; даты из PDF/индекса поиска).
- PBOC EN: https://www.pbc.gov.cn/en/3688006/index.html — ACCESS 2026-09-03; LPR announcement 20 Aug 2026 на главной; отдельного «8 дат как FOMC» нет. Не Investing.com.

---

## 2. Четыре открытых механизма (не энциклопедия)

### M1. High-frequency event-study / monetary surprise
- **Что:** Сюрприз политики ≠ сырой шаг ставки. GSS (FEDS 2004-66, 1 Nov 2004): окно ~30 мин (10 мин до / 20 мин после); surprise текущего target из fed funds futures с масштабом на оставшиеся дни месяца; два фактора — **target** (текущая ставка) и **path** (форвард-guidance / statement). Один фактор отвергается. Path сильнее двигает длинные Treasuries; statements — не независимый инструмент, а ожидания будущего target. Bauer/Bernanke/Milstein (JEP 2023; PDF draft 8 Dec 2022, michaeldbauer.com): surprise = 1-й PC изменений ED1–ED4 в том же 30-мин окне, шкала 1:1 к ED4; hawkish >0. **Таблица IRF 10 bp / 10d (SPX −1.4% …) уже в market-context — не копировать.** Инкремент: как измеряют, не «на сколько падает SPX». Позже Bauer–Swanson (NBER w29939): surprises коррелируют с публичными макро/финансовыми данными *до* FOMC → ортогонализация («Fed response to news»). USMPD (SF Fed): открытый HF датасет + R-код; окна statement 30m / presser 70m / оба / minutes 30m; источник тиков LSEG.
- **URL:** https://www.federalreserve.gov/pubs/feds/2004/200466/200466pap.pdf · https://www.michaeldbauer.com/files/risk.pdf · https://www.frbsf.org/research-and-insights/data-and-indicators/us-monetary-policy-event-study-database/
- **Дата:** GSS 2004-11-01; Bauer PDF 2022-12-08 / JEP 2023; USMPD updated 2026-08-03. ACCESS 2026-09-03.
- **Почему AICM (кандидат):** журнал «что ждали vs что сказали vs что сделала цена в окне» — предупреждение/сверка, не вход. Dummy типа события (statement / presser / minutes) — фича.
- **Риск:** LSEG Tick History платный; USMPD — производный публичный срез. Не Citadel. Не live.

### M2. Nowcast vs survey consensus
- **Что:** Nowcast ≠ консенсус экономистов. GDPNow (Atlanta Fed): без субъективных правок; 13 субкомпонент как BEA; bridge + DFM + BVAR; код **не** отдают (FAQ), Excel параметров — да; MAE финальных nowcast vs BEA advance 0.77 pp (2011:Q3–2025:Q2). На ACCESS: 2026:Q3 = 4.8%, update 1 Sep 2026, next 3 Sep 2026. NY Fed Staff Nowcast (Liberty Street 8 Sep 2023): DFM; «news» = релиз − *модельный* прогноз, вес через Kalman; weekly Friday; пауза COVID, возобновлён 2023. SPF (Philadelphia Fed): старейший квартальный опрос (с 1968; Fed с 1990); mean/median + индивидуальные ID; документация update 14 Aug 2026. Bloomberg survey median — идея консенсуса «как в терминале ECO»; HTML bloomberg.com/press = 403, текст с PR Newswire 7 May 2026.
- **URL:** https://www.atlantafed.org/research-and-data/data/gdpnow · https://libertystreeteconomics.newyorkfed.org/2023/09/reintroducing-the-new-york-fed-staff-nowcast/ · https://www.philadelphiafed.org/surveys-and-data/real-time-data-research/survey-of-professional-forecasters
- **Дата страниц:** GDPNow 2026-09-01; NY Fed post 2023-09-08; SPF docs 2026-08-14. ACCESS 2026-09-03.
- **Почему AICM (кандидат):** до принта — что *модель/опрос* ждут; после — surprise vs nowcast и vs survey могут разойтись. Не вход.
- **Риск:** GDPNow ≠ прогноз президента Atlanta Fed. Два nowcast расходятся — FAQ прямо: не комментируют разницу. Blue Chip на графике GDPNow — proprietary Wolters Kluwer.

### M3. News analytics как КАТЕГОРИЯ (не коннектор)
- **Что продают (маркетинг):** не «текст новости», а поля **sentiment / relevance / novelty** (+ impact). RavenPack News Analytics: relevance scoring, novelty tracking, impact; таксономия event topics; «70% of the best performing quantitative hedge funds» — **заявление вендора**. Refinitiv/TRNA (LSEG): те же три оси на старых OA PDF (sentiment pos/neu/neg, relevance 0–1, novelty vs prior items) — HTML developers.lseg.com в этом срезе не снимали как продукт-спеку.
- **URL:** https://www.ravenpack.com/products/edge/data/news-analytics · (категория, не ключ)
- **Дата:** ACCESS 2026-09-03; дата статьи на странице не стоит.
- **Почему AICM (кандидат):** знать, *какие поля* индустрия считает фильтром шума (низкая relevance / повтор novelty). Не покупать, не строить «наш RavenPack».
- **Риск:** маркетинг. Не воспроизводимо без лицензии. Не путать с GDELT (уже в market-context как NLP-шум).

### M4. Point-in-time consensus (как вендор продаёт surprise)
- **Что (маркетинг Bloomberg, PR Newswire 7 May 2026):** Economic Releases and Surveys PiT via Data License; >3000 индикаторов, >100 экономик, история с 1997. Три компонента: (1) forward-looking calendar, (2) actuals + consensus + revision history, (3) intraday updates of economist survey *до* релиза. Цитата Jacob: expectation formation + response to new information. Это публичное описание того, что систематик считает look-ahead-free макрослоем — не наш датасет.
- **URL:** https://www.prnewswire.com/news-releases/bloomberg-introduces-point-in-time-economic-data-to-power-quantitative-research-and-strategy-development-302765281.html
- **Дата:** 2026-05-07. ACCESS 2026-09-03. bloomberg.com/company/press/… = 403.
- **Почему AICM (кандидат):** формула журнала = календарь + консенсус-на-момент + факт + ревизия. Совпадает с логикой crowd-layer, на другом источнике ожиданий.
- **Риск:** платный Data License. Не терминал AICM. Не обещать «как у фондов в live».

---

## 3. Исторический тест / будущее ML = только фичи

Не модель. Не обучение. Не live.

**Годится как фича (кандидат на журнал, потом тест; n мало → INSUFFICIENT_SAMPLE):**
- `surprise = actual − consensus` (survey median; не «наш прогноз CPI»)
- `surprise_z = surprise / σ_series` (как CESI в открытых пересказах Bloomberg: weighted historical SD; сам CESI — proprietary, не внедрять)
- dummy: страна; тип релиза (NFP / CPI / GDP advance / FOMC statement / presser / minutes)
- dummy окна: 30m statement vs 70m presser (USMPD)
- vintage / as-of: ALFRED `realtime_start`/`realtime_end` (https://alfred.stlouisfed.org/ ; FRED API realtime_period https://fred.stlouisfed.org/docs/api/fred/realtime_period.html) — что было *известно* на дату T, не revised FRED сегодня
- nowcast_news = nowcast_t − nowcast_{t−1} (определение NY Fed)
- если когда-либо вендор news analytics: фильтр relevance/novelty *до* sentiment (категория M3)

**Не годится:**
- LLM «предскажи CPI» без vintage
- revised ряд как если бы знали в T
- обучение/кэш FRED Content: ToS июнь 2024 запрещает FRED Services/Content/API «in connection with the development or training of any … machine learning … large language models» (страница terms в этом прогоне пустой HTML; зафиксировано поиском + уже в market-context). URL: https://fred.stlouisfed.org/legal/terms/ · анонс https://news.research.stlouisfed.org/2024/06/weve-updated-our-terms-of-use-action-requested/
- arXiv:2505.16136 (abs ACCESS 2026-09-03; дата на abs 24 Aug 2026) — авторские Sharpe 5.87 на GDELT+FinBERT+XGBoost; **не** кандидат стратегии; из фич там полезно только напоминание, что *dispersion/impact* бывают предикторами в чужой работе. Не внедрять. Не P&L.

OSS (не внедрять; не Freqtrade/Jesse — уже oss-data-replay): USMPD R-код на странице SF Fed; MATLAB DFM https://github.com/FRBNY-TimeSeriesAnalysis/Nowcasting (HTML GitHub ACCESS: 234★). GDPNow код закрыт.

---

## 4. Что это даёт AICM (предупреждение)

Журнал на стыке crowd-layer: **консенсус/nowcast до релиза → факт → реакция 15m–4h–1d**. Подтверждение намерений = гипотеза расхождения (толпа vs сюрприз vs цена), не правило входа. 10:00 толпа+листинги без изменений.

---

## 5. Чего не делать

Не live-бот новостей. Не Radchenko+Andreev hybrid. Не «предскажем самую вероятную новость и купим». Не мемкоины, не presale. Не ключи. Не школа.

---

## Инкремент vs уже снятое

| Уже | Этот файл |
|---|---|
| market-context: FOMC/BEA URL, три рамки, Lucca–Moench, IRF Bauer 10d, FRED ToS как блокер, GDELT, BLS bot-block | Как *измеряют* surprise (target/path, PC ED1–4, окно, ортогонализация); nowcast≠survey; вендоры как категория полей; PiT consensus; фичи surprise/σ/vintage; календари ECB/BoE/BoJ/PBOC |
| crowd-layer: ритм 10:00/14:00, карточка ожидание vs факт | Макро-консенсус как *ещё один* столбец ожидания в том же журнале, не второй ритм |
| oss-data-replay: Nautilus/LEAN/Jesse | Только USMPD R + FRBNY Nowcasting MATLAB |

---

## Дыры

- bloomberg.com press 403; сняли PR Newswire 2026-05-07
- FRED `/legal/terms/` curl HTML пустой; запрет AI/ML — по индексу + market-context
- ALFRED homepage timeout; API realtime_period открывался поиском
- BoJ HTML timeout; даты из PDF 31 Jul 2025 / индекс
- BLS schedule bot-block (уже market-context) — не скрейпить
- LSEG News Analytics продукт-HTML не снят; категория по OA PDF/маркетингу RavenPack
- PBOC: нет публичного «календаря 8 дат»; LPR 20 Aug 2026 на EN-главной
- Не открывались внутренности фондов. X не звали.
