# Knowledge Candidate — шесть копируемых макро-механизмов (инкремент)

ACCESS: 2026-09-03, Europe/Zurich.
СТАТУС: Knowledge Candidate. Не Foundation. Не канон. Не вход. Не live.
СЛОЙ: инкремент к `from-grok/2026-09-03-macro-news-fund-mechanisms.md` и операционному контракту `from-grok/2026-09-03-macro-scenario.md`. Не замена M1–M4. Не клеить с EWP / объёмом / флагами.

## Как фонды (публично)

Систематик держит point-in-time ожидание (опрос / nowcast / рыночная плотность), в релиз считает сюрприз = факт − ожидание, часто \(s=(y-E[y])/\sigma\) (Scotti IFDP 1093), смотрит узкое окно цены. Рынок торгует новость, не уровень. Консенсус Bloomberg часто не рационален — на него всё равно реагируют, потому что он публичный. Nowcast ≠ опрос.

BTC: NY Fed sr1052 (2017–2022) почти ортогонален макро, значим только CPI (~5%). Kroner–Mohammed–Vega (март 2026, SSRN 6447644): vol/объём/спреды вспыхивают на FOMC/CPI/labor ~15–30 мин; риск-офф бьёт крипту как акции. Yang–Wang FRL 2026: 41 FOMC, час 14:00–15:00 ET, |ret| BTC 0.66% → 1.25% (Δ 0.59 п.п.). Числа TokenPost «29–30 б.п. на 1σ CPI» в этом прогоне **не** подтверждены — не использовать.

## Шесть копируемых if/then (не бренды)

| id | if/then | публичный источник | K-0 BTCUSDT 1h |
|---|---|---|---|
| MN-1 Standardized surprise | Есть first-print и prior → \(s=(actual-prior)/\sigma_{hist}\); знак s = hawkish/dovish, не «лонг BTC» | Scotti IFDP 1093; Philly Fed RTDSM EMPLOY; ALFRED PAYEMS | да, нужен prior. История Bloomberg-консенсуса — дыра |
| MN-2 Nowcast vs survey | nowcast/ADP выше консенсуса до принта → prior «upside print», не вход; после `nowcast_news = Δnowcast` | GDPNow (MAE 0.77 п.п. 2011:Q3–2025:Q2); NY Fed nowcast; Cleveland inflation; ADP NER ≠ прогноз BLS | частично: ADP→NFP как prior |
| MN-3 Implied-odds prior | T−1 мин: мода/медиана Kalshi (или FedWatch на FOMC) = P(сценарий); контракт не торговать | Kalshi KXPAYROLLS / CPI, close 8:29 ET; payroll с марта 2023 (Diercks FEDS 2026-010); CME FedWatch = Q из FF futures | да с ~2023, n мало |
| MN-4 Vintage first-print | Сюрприз только vs первого числа; ревизии T+1/T+2 — отдельная фича | Philly Fed RTDSM EMPLOY с 1966; ALFRED PAYEMS vintages | да (гигиена). Без vintage replay врёт |
| MN-5 HF event window | timestamp релиза ∈ бар K-0 → ret / \|ret\| / volume vs placebo того же часа; окно фиксировать *до* теста | GSS ~30 мин; USMPD; на 1h грубее — честно писать | да |
| MN-6 Drift vs fade | sign(ret 0..+1h)=sign(+1h..+4h/+1d) → drift, иначе fade; не вход | event-study CAR; Kroner FEDS 2025-022: на high-attention склонны перереагировать | да; FOMC 8/год режет n сильнее NFP 12/год |

WR: MN-1/5 = знак замороженного маппинга vs знак окна (не «угадали число»). MN-2 = знак(nowcast−consensus) vs знак(actual−consensus) — prior принта. MN-3 = модальный бин Kalshi содержит actual (Brier/PIT). MN-6 = drift vs fade. n<20 → `INSUFFICIENT_SAMPLE`.

## M1 freeze (решение штаба 03.09 вечер)

Оставить **NFP** как первый собираемый слой (пайплайн, не «максимальный коэффициент BTC»): следующий принт пт 4 сен 2026 14:30 Zurich; ~12/год; first-print Philly/ALFRED; prior ADP/claims/Kalshi; стык с K-0 без LSEG.

Если позже понадобится ненулевая реакция BTC, а не пайплайн — **CPI** (пт 11 сен, Cleveland nowcast, Kalshi CPI с июня 2021, у sr1052 единственный значимый макро-коэф.). Не переключать без решения штаба. FOMC лучше для vol (Yang–Wang), хуже как первый replay.

Выборка BTC для реакции: **≥2021-01** отдельной ячейкой; pre-2021 не пулить.

## Watchlist (сентябрь 2026, DST)

| событие | Zurich | ближайшее |
|---|---|---|
| US NFP | 14:30 | пт 4 сен |
| US CPI | 14:30 | пт 11 сен |
| US PPI | 14:30 | чт 10 сен |
| FOMC statement | 20:00 | 15–16 сен (SEP) |
| ECB GC | 14:15 / presser 14:45 | 10 сен Berlin |
| BoE MPC | 13:00 | чт 17 сен |
| BoJ MPM | по календарю | 17–18 сен |
| CN NBS PMI | ~03:30 | конец месяца |

Не смотреть: medium-impact Investing, Caixin как замена NBS.

## ML-фичи (имена, не обучение)

`event_id`, `country`, `event_type`, `release_ts_utc`, `actual_firstprint`, `prior_survey`, `prior_nowcast`, `prior_adp`, `prior_kalshi_mode`, `surprise_raw`, `surprise_z`, `revision_t1`, `nowcast_news`, `kalshi_var`, `regime_post2021`, `ret_0_1h`, `ret_1_4h`, `ret_0_1d`, `sign_match_drift`.

Не FRED revised-as-of-today. FRED ToS июнь 2024 — не train ML на FRED. Для обучения позже: Philly RTDSM / ALFRED по их правилам / K-0 / Kalshi API.

## Запреты

Не live. Не вход по твиту. Не «предскажем и купим». Не RavenPack как наш датасет. Не скрейп BLS. Не TokenPost. Не ADP как официальный nowcast BLS. Завтрашний NFP — карточка журнала, не слот ≥60%.

## URL

1. Scotti IFDP 1093 — https://www.federalreserve.gov/pubs/ifdp/2013/1093/ifdp1093.pdf
2. GDPNow — https://www.atlantafed.org/research-and-data/data/gdpnow
3. Benigno & Rosa, sr1052 — https://www.newyorkfed.org/research/staff_reports/sr1052
4. Diercks–Katz–Wright FEDS 2026-010 — https://www.federalreserve.gov/econres/feds/files/2026010pap.pdf
5. BLS Employment Situation schedule — https://www.bls.gov/schedule/news_release/empsit.htm
