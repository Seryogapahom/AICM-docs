# NFP actual + survey archive (M1-REACT)

Статус: Knowledge Candidate. Разведка URL. Не Foundation. Не вход. Не ряд actual/consensus в git.
Слой: `from-grok/macro/2026-09-03-m1-eventstudy.md`
Снимок: **2026-09-03 23:58 CEST / Europe/Zurich**
Задача: публичный архив пар **actual + survey/forecast** (не FRED PAYEMS-only). BLS не скрейпить. FRED dump в git не класть.

Нужно для event-study: на каждую пятницу NFP — first-print actual и дорелизный consensus в тех же единицах (тыс. занятых, m/m). Нет пары → строка выкидывается.

## Вердикт (коротко)

Лучший **открытый HTML** с колонками Actual / Previous / Consensus на живой странице: **Trading Economics** Non Farm Payrolls. Второй кандидат с меткой Consensus+Actual на event-page: **FXStreet**. **Econoday** даёт Prior / Consensus / Consensus Range / Actual на карточке релиза (проверено на Nov 2025). **Investing.com** в индексе показывает Actual / Forecast / Previous, но live GET этой сессии = **403**. **ALFRED PAYEMS** = vintages actual **без** survey — **недостаточно одно**.

Ни один из HTML-календарей не даёт свободной лицензии на выгрузку в репозиторий. Для прогона Тестера: читать с URL, не коммитить ряд.

## 1. Trading Economics — лучший открытый HTML-кандидат

- URL: https://tradingeconomics.com/united-states/non-farm-payrolls
- Колонки на живой странице (fetch 2026-09-03): Calendar GMT | Reference | Actual | Previous | **Consensus** | TEForecast
- Пример строк: 2026-08-07 Jul Actual −23K Previous 20K Consensus 80K; 2026-09-04 Aug Actual *(пусто)* Previous −23K Consensus **56K** TEForecast 42.0K
- Что это за consensus: страница API календаря пишет «Survey consensus figures are provided displaying the **average** forecast among a representative group of economists» (не median). URL: https://tradingeconomics.com/calendar/api
- TEForecast = их ARIMA/analyst, **не** street survey — для M1-REACT не подставлять вместо Consensus.
- License/ToS: https://tradingeconomics.com/terms.aspx — «limited, personal, nontransferable, revocable license to analyse data»; API коммерческий (https://tradingeconomics.com/api/). Дамп в git / redistrib — нет.
- Usable for event-study: **YES** как публичный просмотр пар actual/consensus. **NO** как git-источник. API — если штаб купит лицензию.

## 2. FXStreet Economic Calendar (event NFP)

- URL события: https://www.fxstreet.com/economic-calendar/event/9cdf56fd-99e4-4026-aa99-2b6c0ca92811
- Колонки на live-странице: **56K Consensus**, Previous **−23K**, блок Historical Data Chart с сериями Dev. / Consensus / Actual
- Описание календаря (https://www.fxstreet.com/economic-calendar): Previous, Actual, Consensus, Deviation ratio
- Отдельный path `/historical-data` → **404** (fetch этой сессии)
- API: https://docs.fxstreet.com/api/calendar — occurrence несёт actual, consensus (коммерческий docs, не бесплатный дамп)
- ToS: прямые URL `/legal/terms-of-use` и `/about-us/terms-and-conditions` и `/info/terms-and-conditions` → 404; текст лицензии **UNKNOWN** (страница не открылась)
- Usable for event-study: **YES** на уровне ручного/лицензированного чтения пар. Историческая **таблица** всех принтов на HTML не подтверждена (только chart + текущий consensus). Не git-дамп.

## 3. Investing.com NFP event 227

- URL: https://www.investing.com/economic-calendar/nonfarm-payrolls-227
- Колонки (поисковый индекс, не live): Release date | Time | **Actual** | **Forecast** | **Previous**. Пример индекса: Sep 04, 2026 (Aug) Forecast 55.00K Previous −23.00K; Aug 07 Actual −23.00K Forecast 85.00K Previous 20.00K
- Live GET этой сессии: **403** (HEAD 200). Число Forecast 55k **не верифицировано** живым fetch.
- ToS: https://cdn.investing.com/about-us/terms_and_conditions.pdf — personal use; **запрещён automated extract/scrape**; «prohibited to use, store, reproduce… without explicit prior written consent»
- Usable for event-study: **YES как человеческий просмотр пар** (если страница открывается в браузере). **NO** scrape, **NO** git dump. Для лаборатории — слабый кандидат из-за ToS + 403.

## 4. Econoday Employment Situation

- Хаб года: https://us.econoday.com/byevent?cust=us&event_id=247&lid=0&year=2026 — определение события, без таблицы всех месяцев в fetch
- Карточка релиза (проверено): https://us.econoday.com/byevent?fid=636606&lid=0&year=2025
  Колонки: **Prior | Consensus | Consensus Range | Actual** (Nonfarm Payrolls − M/M и др.). Пример Nov 2025: Prior 119,000 Consensus 40,000 Range −20,000 to 100,000 Actual 64,000
- Плюс: range → можно сверять band; есть Consensus Outlook prose
- Минус: история — по fid отдельных релизов, не одна выгрузка; 2026-хаб без сводной таблицы в этом fetch
- License/ToS: https://us.econoday.com/legal_notice?cust=us — контент собственность Econoday; «No permission is granted to copy, distribute, modify, post or frame… without express prior written consent». Коммерческий API: https://api.econoday.com/api/api.html ; лицензии: https://www.econoday.com/
- Usable for event-study: **YES** как публичные карточки пар (если штаб читает HTML/купит API). **NO** git dump.

## 5. ALFRED / FRED PAYEMS — недостаточно одно

- ALFRED: https://alfred.stlouisfed.org/ — vintages **actual** (first-print vs later revisions) для PAYEMS
- FRED PAYEMS: https://fred.stlouisfed.org/series/PAYEMS — уровень занятости, не street survey
- Нет колонки forecast/consensus. Для surprise = actual − consensus **не хватает**. Можно стыковать first-print actual **после** того, как survey взят из календаря выше. FRED Content / dump в git — **не делать** (слой уже запретил).

## 6. Не то (чтобы не перепутать)

- Philadelphia Fed SPF (https://www.philadelphiafed.org/surveys-and-data/real-time-data-research/survey-of-professional-forecasters) — **квартальный** survey, не пятничный first-print NFP vs street.
- CoinDesk week-ahead «est. 58K» — не архив пар.
- BLS CES tables — actual only; бот-скрейп BLS запрещён карточкой.

## Рекомендация Тестеру (M1-REACT)

1. Источник пар: **Trading Economics HTML calendar** (Actual + Consensus) как открытый URL; перекрёстно FXStreet event page / Econoday карточка, если строка TE пустая.
2. First-print: не подменять revised PAYEMS из текущего FRED. ALFRED vintages — только для as-of actual, **без** survey.
3. Не класть выгрузку в git. Не scrape Investing (ToS + 403). Не BLS-бот.
4. Покрытие: TE/FXStreet/Econoday HTML не гарантируют n≥20 без ручной инвентаризации — перед прогоном посчитать, сколько пятниц K-0 имеют **оба** поля.

## Сводка usable?

| Источник | URL | actual | forecast/consensus | previous | ToS (видимое) | event-study |
|---|---|---|---|---|---|---|
| Trading Economics | tradingeconomics.com/united-states/non-farm-payrolls | да | Consensus (они: average) | да | personal license; no redistrib; API paid | YES смотреть / NO git |
| FXStreet event | fxstreet.com/economic-calendar/event/9cdf56fd-99e4-4026-aa99-2b6c0ca92811 | да (chart + post-print) | Consensus | да | ToS текст UNKNOWN (404) | YES смотреть; hist table не подтверждена |
| Investing.com 227 | investing.com/economic-calendar/nonfarm-payrolls-227 | да (индекс) | Forecast | да | no scrape/store/reproduce | YES браузер / NO scrape |
| Econoday | us.econoday.com/byevent?event_id=247 | да (карточка) | Consensus + Range | Prior | no copy without consent; API paid | YES карточки / NO git |
| ALFRED PAYEMS | alfred.stlouisfed.org | vintages actual | **нет** | n/a (ревизии) | FRED terms; не dump в git | **NO** одно; только actual as-of |
