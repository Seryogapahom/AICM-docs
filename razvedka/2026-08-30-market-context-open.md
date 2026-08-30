# Контекст рынка — открытый пакет
ACCESS: 2026-08-30 (Europe/Zurich)
СТАТУС: Knowledge Candidate. Не Foundation. Не канон AICM. Не Consilium.
НАЗНАЧЕНИЕ: недостающий слой «наоборот» к пакету Андреева (цена/структура, новости не оценивает) и к рамке Frost/Prechter (новости не двигают цены). Кандидат для *будущего* Consilium. L0–L2 не трогать.
МЕТОД: только открытый HTML/OA. Школы, VIP, полные книги, серые PDF, YouTube Хедлайнеров — не источники этого файла.
НЕ СДЕЛАНО: торговая система не писалась; слежка не внедрялась; бэктест не запускался. Видео `miWQ3VLcLH4` (снова Андреев) и `koTINvlf6fw` (гость, штаб снимает отдельно) пакет не подменяют. Имя гостя второго эфира в открытых страницах этого среза **не всплыло**.

Сырьё:
- `razvedka/_draft-mktctx-select.md`
- `razvedka/_draft-mktctx-news-sessions.md`
- `razvedka/_draft-mktctx-links-tools.md`

---

## 1. Как выбирают актив (не все графики подряд)

Повторяющийся каркас с бирж/регулятора/брокеров: сначала **tradability** — войти/выйти без существенного сдвига цены.

| Что фильтруют | Откуда (открыто 2026-08-30) |
|---|---|
| Ликвидность = скорость сделки без hefty fee / без влияния на цену | SEC investor.gov glossary https://www.investor.gov/introduction-investing/investing-basics/glossary/liquidity-or-marketability |
| Контрактный месяц и время суток по volume; OI как «деньги в контракте» | CME volume / OI / depth: https://www.cmegroup.com/education/courses/introduction-to-futures/what-is-volume |
| ADV/ADTV, спред, глубина как часть *selecting securities* | IBKR Campus ADTV / spread / depth |
| ETF: ADV ≠ вся ликвидность; secondary vs primary/basket | Nasdaq/Vanguard https://www.nasdaq.com/articles/abcs-etf-liquidity |
| Вселенная раньше стратегии; dollar-volume; anti-flicker границы | QuantRocket Lecture 29 (CC-BY 4.0) |
| Почему этот тикер: RS vs индекс/сектор; top-down сектор→индустрия→акция | ChartSchool Price Relative, SCTR (фильтр при слишком многих сигналах), Sector Summary, Faber first-cut top-3 sectors |

Investopedia 12 rules (intraday): liquidity + «правильная» vol + движение vs сектор; порог «≥1 млн shares/day» — правило **этой** статьи, не универсальный. Beta как коэффициент на открытых страницах среза **не** разобрана.

**Не закон AICM.** Это фильтр вселенной, не вход.

---

## 2. Как ищут сделку: сетап, фильтр, ожидание vs вход

Явное разделение universe/filter ≠ entry на открытых страницах: SCTR «filter when too many signals»; Fidelity screener = candidate list; QuantRocket universe ≠ strategy; Faber = first cut.

Setup vs trigger (ChartSchool MACD zero-line + swings): индикаторный cross = hint; ждать swing break; mid-range = «jumped the gun»; иногда price trigger важнее ждать cross. Fidelity TA: mixed indicator signals — не форсировать. Investopedia 12 rules: селективность 2–3 сделки; step aside в чужом режиме; «If the conditions don't provide a suitable environment… save your money and wait.»

Слова «A+ setups», «confluence», «сидеть на руках» **дословно на успешно открытых URL не встречены** (Investopedia confluence/5-step и BabyPips — 402/Cloudflare).

**Не система входа AICM.**

---

## 3. Новости и календарь

Официальные календари описывают **что за релиз и когда**, не как торговать:
- FOMC: https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm (8 встреч/год; 2026 dates; minutes +3 weeks)
- BEA: https://www.bea.gov/news/schedule (GDP/PIO, обычно 8:30)
- BLS HTML в этом прогоне **bot-block**; календарь — кандидат URL, не снятый HTML

**Кто использует:** Investopedia «How to Trade the News»; BabyPips calendar (избегать event risk, slippage); CME FX (FOMC 8× как listed mover); NY session BabyPips — «attractive for news traders»; SF Fed USMPD — press conference теперь главный HF policy-news.

**Кто игнорирует / дисконтирует:** EWI free HTML https://www.elliottwave.com/articles/another-wall-street-myth-laid-to-rest/ — «Economic news – good or bad – doesn’t govern the trend» (не книга Frost/Prechter); CMC «buy the rumor, sell the news» — prices move ahead, **not a reliable strategy**; Lucca–Moench: pre-FOMC equity drift есть, **другие** US macros такого drift не дают.

**Ловушки, которые страницы называют:** fade the news; BTRSTN reversal; spread widening (BabyPips: EURUSD 2→20 pips на unemployment); slippage; first-spike lies (NFP 2011); pre-FOMC thin book (BIS WP 1079); Friday flatten. Фраза **«fake breakout»** на открытых страницах среза не встречена. Straddle — paywall BabyPips, не верифицирован.

Три конкурирующие рамки держать рядом, **не выбирать победителя в этом файле:** (а) новости двигают, (б) новости не определяют тренд, (в) цена уже в ожидании.

---

## 4. Связки — наблюдаемые паттерны, не закон

Корреляции DXY–SPX, DXY–BTC, BTC–NDX как одно вечное число **на открытых страницах не найдены.** Не выдумывать.

| Паттерн источника | Число на странице | Оговорка |
|---|---|---|
| Surprise hawkish FOMC → риск-офф | Bauer/Bernanke/Milstein JEP 2023: 10 bp / 10d: SPX **−1.4%**, VIX **+1.6**, HY OAS **+0.31 pp**, USD **+0.3%**; FOMC 1988–2019 | IRF на *сюрприз*, не безусловный r |
| Treasuries как хедж к SPX sell-off нестабилен | BIS Dec 2020: до 2000-х **+2 bp 10y на −1% SPX** (хвост 5-го перцентиля); после 2000 хедж; с 2018 muted | хвост, не everyday r |
| BTC стал equity-like / risk-on | Chicago Fed WP 2026-16: Dow beta **~0.4 → ~1.5** (break ~2020/21); sample Apr 2013–Mar 2026; NASDAQ beta после контроля на Dow ≈ 0; Treasury-*returns* beta ≈ 0 | beta ≠ Pearson r; не «BTC = Nasdaq tech» |
| DXY состав | EUR 57.6% … (Wikipedia/Investopedia) | r(DXY, SPX/BTC) на открытых страницах **нет** |
| VIX = fear gauge | Wikipedia | r(VIX, SPX/BTC) на странице **нет** |

DXY ICE ≠ Fed trade-weighted (DTWEXBGS). Safe-haven USD: Liberty Street 2014 (taper 2013) — модельная декомпозиция, не универсальный r.

---

## 5. Американская сессия vs Азия/Европа

**Почему связано (BIS Triennial Apr 2022, не апгрейдить до 2025/26):** FX $7.5tn/day; USD **88%**; UK 38% + US 19% + SG 9% + HK 7% + JP 4% = 78%; cross-border 62%. Vehicle USD + концентрация desks + cross-border — не «магия американской сессии».

**Тяжёлое окно FX в энциклопедиях:** London–NY overlap **8:00–12:00 ET**. Цифры «50/58%» на BabyPips/Investopedia — **не** BIS overlap %. US afternoon после закрытия Лондона ≠ US morning. USD share: BabyPips 85% vs BIS 88% — для Consilium предпочесть BIS.

CME hours page **не** ранжирует ES по London vs NY. Crypto listed 24/7 (короткие halt); **официальный print** CME CF чаще 16:00 London, часть 16:00 NY. Не утверждать «объём крипты = US hours» — на открытых CME FAQ этого нет.

SEC: extended hours = другая ликвидность, не RTH.

---

## 6. Кандидаты инструментов слежки (не внедрять)

| Кандидат | URL | Заметка |
|---|---|---|
| FOMC calendar | https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm | официальный HTML |
| BEA schedule | https://www.bea.gov/news/schedule | официальный HTML |
| BLS schedule | https://www.bls.gov/schedule/ | bot-block; не скрейпить |
| FRED API | https://fred.stlouisfed.org/docs/api/fred/ | **ToS июнь 2024: запрет AI/ML training и cache/archive API content** — блокер наивного слоя |
| Fed RSS catalog | https://www.federalreserve.gov/feeds/feeds.htm | XML в прогоне HTTP 500 |
| White House RSS | https://www.whitehouse.gov/news/feed/ | открыт 29 Aug 2026 |
| SEC press RSS | https://www.sec.gov/news/pressreleases.rss | открыт; не EDGAR |
| CME FedWatch UI | https://www.cmegroup.com/markets/interest-rates/cme-fedwatch-tool.html | implied futures, не опрос FOMC; API платный |
| CFTC COT / PRE | Friday 15:30 ET; Socrata | главная timeout; не канон positioning→цена |
| GDELT dumps | gdeltproject.org «100% free» | NLP-шум; Cloud = другой платный продукт |
| CoinGecko keyless | ~10–30 calls/min, «not production» | агрегатор |
| Trading Economics | subscription, 2 req/s | не первоисточник BLS/Fed |
| Yahoo / Stooq / Kaiko | scrape запрещён / JS wall / enterprise | **не внедрять** |

FRED-указатели рядов (не вызывать, не архивировать): DTWEXBGS, DGS10, DFII10, BAMLH0A0HYM2, VIXCLS, SP500, NASDAQCOM, DJIA. DXY ICE отдельно от Fed TWI.

---

## Чего нет (дыры пакета)

- Безусловные r(DXY, SPX/BTC), r(BTC, NDX) как константа
- BLS HTML календаря (bots)
- Investopedia VIX / risk-on / confluence (402)
- «A+ setup» / confluence glossary
- Фраза fake breakout
- Объём крипты по US-часам
- Имя гостя `koTINvlf6fw`
