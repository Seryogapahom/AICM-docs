# Слой макро-сценария (до релиза → факт → реакция)

Статус: Knowledge Candidate. Не Foundation. Не PREF. Не канон AICM.
Дата: 2026-09-03 (вечер Europe/Zurich)
Источник: предпочтение Владельца в чате штаба (~23:52 Zurich): макро ведущих стран, предупреждение/подтверждение, исторический тест, наиболее вероятный сценарий до релиза, открытые модели фондов для будущего ML.
Слой рядом: `from-grok/2026-09-03-crowd-layer.md` (толпа) и `from-grok/2026-09-03-macro-news-fund-mechanisms.md` (как публично читают календарь). Не замена. Не второй Радченко. Не Дуглас.

Не вход. Не live. Не клеить с EWP / объёмом / SMC / листингами. Не слот доски `mehanizmy.md`, пока нет честного WR на истории.

## Честная рамка (как фонды, публично)

Предсказать **число** релиза и предсказать **реакцию** цены на сюрприз — две разные задачи. В открытых текстах (GSS/USMPD, GDPNow, PiT consensus) фонды моделируют surprise = факт − ожидание, затем окно 15m–4h. «Угадать принт лучше консенсуса» — отдельный счёт, и он часто близок к 50%. Лаборатория считает оба счёта и не обещает P&L.

До принта = предупреждение. После = сверка. Не «купили, потому что NFP».

## Что делает слой

1. **Календарь ведущих стран** (только high-impact, не 40 строк шума): US NFP/CPI/PCE/FOMC; EZ ECB + flash HICP; UK BoE + CPI; JP BoJ + CPI; CN NBS PMI + PBOC LPR. Даты — с официальных страниц, не Investing как источник истины.
2. **Сценарий до релиза** (за 24h…30min): `BEAT` / `MISS` / `INLINE` / `UNKNOWN`. Источник: публичный survey-median + nowcast-прокси (ADP/claims/ISM employment / Fed nowcast, если есть). Не LLM-догадка. Нет числа → `UNKNOWN`, не выдумывать.
3. **Факт после релиза:** actual, surprise = actual − consensus, совпал ли сценарий.
4. **Реакция:** BTCUSDT (K-0, 1h) окна 1h / 4h / 1d. Знак реакции **не замораживать**, пока event-study не покажет устойчивое направление. Сначала измерить.
5. **Предупреждение (можно заморозить сразу, не вход):** если high-impact в окне ±2h от метки t — демо-вход по P1–P5 **запрещён**, даже если if/then паттерна сработал. Это подсказка риска события, не сигнал.

## if/then сценария принта (M1-PRINT, заморожен)

```
IF событие из watchlist с известным t_release
AND за T-24h…T-30min есть публичный consensus (median survey) с URL и временем снятия
AND есть nowcast_proxy в тех же единицах
THEN
  IF nowcast_proxy > consensus + band → scenario = BEAT
  IF nowcast_proxy < consensus − band → scenario = MISS
  ELSE scenario = INLINE
ELSE scenario = UNKNOWN

После t_release:
  surprise = actual − consensus
  print_hit = (BEAT и surprise>+band) или (MISS и surprise<−band) или (INLINE и |surprise|≤band)
  UNKNOWN не считается в WR
```

Band для NFP: ±20k занятых (заморожен, не крутить после первого прогона). Другие релизы — свой band в карточке события, до факта.

Метрика print: WR = print_hit / n при n≥20, иначе `INSUFFICIENT_SAMPLE`. Это не слот пяти механизмов.

## if/then реакции (M1-REACT) — сначала измерить

Не замораживать «NFP beat → BTC вниз». На истории K-0:

```
Для каждого NFP t в покрытии K-0 (бар 1h, содержащий 12:30 UTC / 08:30 ET):
  r_1h, r_4h, r_1d = доходность close после t vs close бара до t
  bucket = BEAT / MISS / INLINE по тому же band
Сдать: n, mean r, доля |r_1h|≥0.3% по bucket.
Карту «сюрприз → сторона BTC» заморозить только если в одном bucket n≥20 и знак mean устойчив vs соседнего.
```

Пока карта не заморожена — реакция пишется в журнал, не торгуется.

## Watchlist (типичное время Europe/Zurich, зима UTC+1 / лето UTC+2)

| Страна | Событие | Типично Zurich | Официальный якорь |
|---|---|---|---|
| US | NFP / CPI / PCE | 14:30 | BLS / BEA (не скрейпить BLS-бота) |
| US | FOMC statement | 20:00 | federalreserve.gov календарь |
| EZ | ECB rate + presser | 14:15 / 14:45 | ecb.europa.eu |
| UK | BoE Bank Rate | 13:00 | bankofengland.co.uk |
| JP | BoJ MPM | по календарю BoJ | boj.or.jp |
| CN | NBS PMI / LPR | PMI ~03:00; LPR ~20-е | stats.gov.cn / pbc.gov.cn |

Нет события в горизонте 48h — карточку дня не плодить.

## Карточка события `from-grok/macro/YYYY-MM-DD-<id>.md`

Обязательные поля до релиза: событие, t_release Zurich, consensus+URL, nowcast_proxy+URL, band, scenario, «не вход».
После: actual+URL, surprise, print_hit да/нет, r_1h/r_4h BTCUSDT, совпало ли с толпой дня, паттерн P1–P5 в окне (да/нет, не гибрид).

## Фичи для будущего ML (имена, не обучение)

`surprise`, `surprise_z`, `scenario_prior`, `print_hit`, `r_1h`, `r_4h`, dummy страны/типа, dummy окна statement vs presser, vintage as-of. FRED Content не использовать для обучения моделей (ToS). ALFRED vintages — для журнала as-of, не для train dump.

Похожие открытые механизмы (не внедрять как бренд): USMPD (SF Fed), GDPNow / NY Fed nowcast, SPF Philadelphia, Kalshi/Polymarket/CME FedWatch как implied-odds **если страница открыта без ключа**. RavenPack/TRNA — категория полей (relevance/novelty), не коннектор.

## Ритм

| Когда | Что |
|---|---|
| 10:00 будни | Если в 48h есть high-impact — карточка сценария до релиза. Иначе молчать. |
| После релиза / 14:00 | Факт + реакция. |
| Отдельный прогон | M1-REACT event-study на K-0 (Тестер), не в слот P1. |

## Запреты

Не live-бот новостей. Не «предсказали и купили». Не мемкоин. Не ключи. Не скрейп BLS. Не клеить Эллиотт+макро в одно правило. Не открывать L0–L2.
