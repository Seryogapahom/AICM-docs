# INDEX — накопленное поле Grok

Обзор blobов на `main` на 2026-09-02. Коммит среза: `83e48b544843e5d20a0edb04539e71d6ef61693b` (слой толпы). Не канон. Не PREF. Не Foundation.
Новые пакеты Grok кладутся только в `from-grok/`. Исторические пути не переносились.

Статусы: **архив** (закончено, не меняется) / **кандидат** / **сверка** / **диагностика** / **источник Владельца** / **живой runbook** (меняется). Этот файл обновлять при каждом изменении поля, включая строку коммита среза.

N = **107** (все blobы `main` кроме `.gitignore`, включая этот INDEX и PROVENANCE).

## Корень

| путь | суть | статус |
|---|---|---|
| `AGENTS.md` | Инструкции агентам лаборатории Grok: роли, куда класть, шапка KC, запреты | живой runbook |
| `README.md` | Обменник трёх моделей и Владельца; не канон AICM | живой runbook |

## Обменник (метки каталогов, 2026-09-01)

| путь | суть | статус |
|---|---|---|
| `from-grok/README.md` | Каталог Grok; указатели на INDEX/PROVENANCE; новые работы только сюда | живой runbook |
| `from-claude/README.md` | Метка каталога заданий архитектора; файлы кладёт Владелец или Кодекс | живой runbook |
| `from-chatgpt/README.md` | Метка каталога ChatGPT | живой runbook |
| `from-owner/README.md` | Метка каталога Владельца | живой runbook |
| `from-grok/INDEX.md` | Этот обзор поля (полный список файлов) | живой runbook |
| `from-grok/demo/2026-09-01-lenta.md` | Инвентарь сессий Enabler: Bitget DEMO / TV / CoinGlass. Не вход | диагностика |
| `from-grok/2026-09-01-demo-contour.md` | Грант Enabler: Bitget DEMO + TradingView + CoinGlass. Не live-деньги | живой runbook |
## Контур 2026-09-02

| путь | суть | статус |
|---|---|---|
| `from-grok/2026-09-02-htf-filter-elliott-zigzag.md` | Открытые практики HTF: степень/свинги, не close 4h | кандидат |
| `from-grok/2026-09-03-crowd-layer.md` | Толпа/новости: ожидание vs факт. Не вход | живой runbook |
| `from-grok/2026-09-02-five-mechanisms.md` | Цель: 5 механизмов WR≥60% и живой дневной цикл | живой runbook |
| `from-grok/patterns/mehanizmy.md` | Доска: пока 0 из 5 | живой runbook |
| `from-grok/patterns/2026-09-02-c2-replay.md` | C2: n=327 WR 33.95%, хуже P1. 4h-свеча вредна | диагностика |
| `from-grok/patterns/2026-09-02-c3-replay.md` | C3: n=694 WR 39.91% ≈ P1. SMA20 не лифт | диагностика |
| `from-grok/patterns/2026-09-02-c3.md` | AND: P1 + дневной SMA20. Прогон нет | кандидат |
| `from-grok/patterns/2026-09-02-c2.md` | AND: P1 + направление закрытого 4h. Прогон нет | кандидат |
| `from-grok/2026-09-02-wr60-kontekst.md` | Дыры соло-детекторов и AND-комбо к WR≥60%. Не обещание P&L | живой runbook |
| `from-grok/patterns/2026-09-02-p1.md` | Зигзаг A-B-C (EWP). WR 40.6% n=1574 | диагностика |
| `from-grok/patterns/2026-09-02-p2.md` | Треугольник TE. WR 36.5% n=310 | диагностика |
| `from-grok/patterns/2026-09-02-p3.md` | Flat. WR 41.2% n=2220 | диагностика |
| `from-grok/patterns/2026-09-02-p4.md` | Объём CONFIRM, не вход. WR 39.5% n=6553 | диагностика |
| `from-grok/patterns/2026-09-02-p5.md` | Флаг/вымпел не-EWP. WR 30.4% n=612 | диагностика |
| `from-grok/patterns/2026-09-02-c1-replay.md` | C1: n=417 WR 39.09% vs P1 40.6%. Объём не поднял WR | диагностика |
| `from-grok/patterns/2026-09-02-c1.md` | AND: P1 зигзаг + P4 объём. Прогон ещё нет | кандидат |
| `from-grok/patterns/2026-09-02-dnevnik.md` | Дневник дня 1 | диагностика |
| `from-grok/patterns/2026-09-02-replay.md` | Записка прогона K-0 | диагностика |
| `from-grok/demo/2026-09-02-lenta.md` | Демо-лента 02.09, сделок нет | диагностика |
| `razvedka/novinki/2026-09-02-x-api-tape.md` | Срез X 02.09 | кандидат |
| `from-grok/2026-09-01-pattern-loop.md` | Ежедневный контур: 5 правил + replay + эволюция схемы. Не PREF, не канон | живой runbook |
| `from-grok/PROVENANCE.md` | Провенанс задним числом | живой runbook |

## razvedka

| путь | суть | статус |
|---|---|---|
| `razvedka/README.md` | Индекс корпусов разведки | живой runbook |
| `razvedka/2026-08-30-igor-andreev-videos.md` | Каталог публичных/unlisted видео Игоря Андреева (Igor_Kripta) | архив |
| `razvedka/2026-08-30-igor-andreev-public-mechanics.md` | Публичная механика Андреева (не школа, не VIP) | архив |
| `razvedka/2026-08-30-andreev-hedliners-live-supplement.md` | Инкремент Hedliners LIVE `miWQ3VLcLH4` (снова Андреев) | архив |
| `razvedka/2026-08-30-andreev-hedliners-futures.md` | Инкремент: Хедлайнеры фьючерсы `AodqaoVPLOY` (снова Андреев, не новый слой) | архив |
| `razvedka/2026-08-30-andreev-mikheev-podcast.md` | Инкремент: подкаст Михеева `m3rcPEkJNZ4` (ученик S-1 vs кинжал; не S-1) | архив |
| `razvedka/2026-08-30-hedliners-20y-mechanics.md` | Кандидат: Анатолий Радченко, US/новость/сектор (`koTINvlf6fw`). Не клеить | кандидат |
| `razvedka/2026-08-30-hedliners-misha-scalp.md` | Кандидат: Михаил, in-play скальп (`-PLqDWmFgbc`). Не Андреев, не Радченко | кандидат |
| `razvedka/2026-08-30-hedliners-how-markets-move.md` | Короткий ролик Хедлайнеров: ликвидации лесенкой (`wHPlrty6mBs`) | кандидат |
| `razvedka/2026-08-30-hedliners-armen-gevorkyan.md` | Кандидат: Армен Геворкян, объём/тени/фибо (`4iOjwZWb8jQ`). Не клеить | кандидат |
| `razvedka/2026-08-30-hedliners-anton-klevtsov.md` | Кандидат: Антон Клевцов, спред/относительная стоимость (`fuQgXJAgmBU`). Не клеить | кандидат |
| `razvedka/2026-08-30-trader-evolution-triangles.md` | Кандидат: Trader Evolution, треугольники волн (`vymngVM8RkE`). Не Андреев, не EWP | кандидат |
| `razvedka/2026-08-30-zatulyviter-ewp-guide.md` | Кандидат: Eduard Zatulyviter, обзор EWP (`RV-PmmCSr8w`). Третий слой волн, не TE | кандидат |
| `razvedka/2026-08-30-market-context-open.md` | Открытый HTML: выбор актива, календарь, сессии, связки | кандидат |
| `razvedka/2026-08-30-elliott-open-sources.md` | Открытый корпус правил Эллиотта (не книги) | архив |
| `razvedka/2026-08-30-ewp-frost-prechter-digest.md` | Дайджест правил Frost/Prechter с легального MyEWI, не копия книги | архив |
| `razvedka/2026-08-31-douglas-zonalnyy-treyding.md` | Дайджест Дуглас «Зональный трейдинг» (психология исполнения, не зоны S/D) | архив |
| `razvedka/2026-08-31-mark-douglas-trading-in-the-zone.md` | ExecutionPolicy: гейты `MD-EP-01…12`. Не PREF, не сливать с дайджестом R-D | кандидат |
| `razvedka/2026-08-31-ai-questionnaire-ecosystems.md` | ИИ-анкетные экосистемы: слои A/B/C не склеены; `QE-A/B/C-*`, фишки `HQ-01…08` | кандидат |
| `razvedka/2026-08-31-research-center-as-container.md` | Runtime-формы центра как сменный контейнер (`LC-01…16`). OCI=fs+entrypoint. Один контейнер default | кандидат |
| `razvedka/2026-09-01-aicm-world-preferences-lineage.md` | Карта мира AICM S01–S02 CLOSED / S03 NEXT (`WMAP-2026-08-31`, коммит `4984db5f`). Не PREF, не закрытие S03 | источник Владельца |
| `razvedka/2026-09-01-instrumenty-mir-i-avtomatizaciya.md` | Каталог инструментов мира/интерфейса/автоматизации `WI-01…28` (коммит `86d440df`). Не PREF, не QE | кандидат |
| `razvedka/2026-09-01-s03-open-tools.md` | Инкремент Разведчика к WI: идентичность/viewport/хроника `S03-A/B/C/D-*` (коммит `5ee39097`). Scout, не закрытие S03 | кандидат |
| `razvedka/2026-08-30-andreev-vs-elliott.md` | Карта расхождений Андреев vs открытый учебник Эллиотта, v1 | сверка |
| `razvedka/2026-08-30-andreev-vs-elliott-v2.md` | Карта расхождений v2 (против открытого корпуса ChartSchool/Wiki/Waveopedia) | сверка |
| `razvedka/2026-08-30-andreev-vs-elliott-v3.md` | Карта расхождений v3 (против дайджеста Frost/Prechter). v1/v2/v3 не сливать | сверка |

Complementary-слои Андреев / Радченко / Миша / Армен / Клевцов / TE / Zatulyviter / EWP **не склеены**.

## razvedka/novinki

| путь | суть | статус |
|---|---|---|
| `razvedka/novinki/README.md` | Индекс новинок; X MCP read-only `@acapitalmanager` | живой runbook |
| `razvedka/novinki/2026-08-30-srez-otkrytye-lenty.md` | Срез 2026-08-30: агентная инфра + SEC/ETF + слухи AQuA/Clarity; X тогда недоступен | архив |
| `razvedka/novinki/2026-08-30-oss-data-replay.md` | Открытый код / публичные данные / tick-replay. Кандидат, не бот, не live | кандидат |
| `razvedka/novinki/2026-08-30-x-api-tape.md` | Лента X MCP ~24ч, 2026-08-30. Read-only `@acapitalmanager`. Не follow, не live | архив |
| `razvedka/novinki/2026-08-31-x-api-tape.md` | Будни 10:00, 2026-08-31: узкий инкремент X. Read-only `@acapitalmanager` | архив |
| `razvedka/novinki/2026-09-01-x-api-tape.md` | Будни 10:00, 2026-09-01: узкий инкремент X. Read-only `@acapitalmanager` | архив |

## kontury

| путь | суть | статус |
|---|---|---|
| `kontury/README.md` | Индекс спек и отчётов replay | живой runbook |
| `kontury/2026-08-30-k-0.md` | K-0 каркас replay без стратегии (Binance Vision BTCUSDT 1h) | архив |
| `kontury/2026-08-30-k-0-replay.md` | Отчёт прогона K-0 **SUCCESS** | архив |
| `kontury/2026-08-30-k-1.md` | K-1 Nautilus replay-only (не дом исполнения) | архив |
| `kontury/2026-08-30-k-1-replay.md` | Отчёт прогона K-1 **SUCCESS**, H1 **PASS**. K-1b не нужен | архив |
| `kontury/2026-08-30-s-1.md` | S-1 Андреев сетап №1 long-only 1h. If/then не переписывать | архив |
| `kontury/2026-08-30-s-1-replay.md` | Отчёт прогона S-1 **SUCCESS** (метки lab D-1). Не вердикт по Андрееву | архив |
| `kontury/2026-08-30-d-1.md` | Lab D-1: zigzag 10% + фильтры импульса. Не Андреев, не Радченко. Торговли нет | архив |
| `kontury/2026-08-30-d-1-replay.md` | Отчёт разметки D-1 **SUCCESS**. CSV меток не в git | архив |
| `kontury/2026-08-31-ep-1.md` | EP-1 Douglas ExecutionPolicy overlay на узкий S-1. HQ-03: принять overlay. Не вход, не зоны, не гибрид | кандидат |
| `kontury/2026-09-01-ep-1-replay.md` | Диагностика EP-1 **SUCCESS** (коммит `3e19a592`): G01–G07 на 6 филлах; series **INSUFFICIENT_SAMPLE** n=6. Не market replay | диагностика |

## sverki

| путь | суть | статус |
|---|---|---|
| `sverki/README.md` | Индекс сопоставлений слоёв | живой runbook |
| `sverki/2026-08-30-andreev-vs-radchenko.md` | Новость/цена, сессия, волны, риск. Два слоя, не гибрид | сверка |
| `sverki/2026-08-31-douglas-vs-s1-d1-ewp.md` | Дуглас (исполнение) vs узкий S-1 / D-1 / EWP. Не гибрид «волны+зона» | сверка |

## shtab

| путь | суть | статус |
|---|---|---|
| `shtab/ramka.md` | Рабочая рамка лаборатории: что не делается, L0–L2 CLOSED | живой runbook |
| `shtab/celi.md` | Цели и очередь лаборатории (живой указатель) | живой runbook |
| `shtab/plan-cikl-2.md` | План цикла 2: сбор + один инкремент контура | живой runbook |
| `shtab/2026-08-30-codex-intake.md` | Intake пакета Кодекса v2: lab intake, не исполнение приказа Grok | архив |
| `shtab/2026-08-31-lab-as-container.md` | Контракт сменного исследовательского центра (`LAB-C-*`). Один контейнер default | кандидат |
| `shtab/2026-08-31-lab-deploy.md` | Живой runbook поставки одного контейнера (`LAB-D-*`, LAB-D-12) | живой runbook |

## kanon

Получено от Владельца. Семантический канон L0–L2. **Не исследование Grok.** Реализационных правил нет. L0–L2 закрыты.

| путь | суть | статус |
|---|---|---|
| `kanon/README.md` | Индекс единой карты предпочтений (285 PREF numbered) | источник Владельца |
| `kanon/karta.md` | Единая карта: стек закрытий, каталог PREF, дыры, счётчики | источник Владельца |
| `kanon/open.md` | Named OPEN после s18: terminal `OPEN-19-01…12`; без ответов | источник Владельца |
| `kanon/rejected.md` | Named REJECTED из карточек + приложение безымянных | источник Владельца |
| `kanon/sessions/README.md` | Индекс карточек drop1/drop2/s06–s12 | источник Владельца |
| `kanon/sessions/vision.md` | Конституция AICM, Trading Foundation, Capability Registry (2026-08-18) | источник Владельца |
| `kanon/sessions/s01.md` | Сессия 01: knowledge/hypothesis TF-PREF-001…011 | источник Владельца |
| `kanon/sessions/s02.md` | Сессия 02: object model + bootstrap TF-PREF-012…016 | источник Владельца |
| `kanon/sessions/s03.md` | Сессия 03: v0.2 object-model + TF-PREF-017…030 | источник Владельца |
| `kanon/sessions/s04.md` | Сессия 04: SituationContext TF-PREF-031…034; L0-PREF-001…009 | источник Владельца |
| `kanon/sessions/s05.md` | Сессия 05: L0-PREF-010…019; закрыт L0-B1 Purpose Kernel / cold start | источник Владельца |
| `kanon/sessions/s06.md` | Сессия 06: L0-B2 IN_PROGRESS_PARTIALLY_CLOSED; 025…032 proposed | источник Владельца |
| `kanon/sessions/s07.md` | Сессия 07: L0-B2 closed (025…032 confirmed) | источник Владельца |
| `kanon/sessions/s08.md` | Сессия 08: L0-B3 closed | источник Владельца |
| `kanon/sessions/s09.md` | Сессия 09: L0-B4; Level 0 FORMALLY CLOSED | источник Владельца |
| `kanon/sessions/s10.md` | Сессия 10: L1-B1 closed | источник Владельца |
| `kanon/sessions/s11.md` | Сессия 11: L1-B2 closed | источник Владельца |
| `kanon/sessions/s12.md` | Сессия 12: L1-B3 closed (не L1-B2) | источник Владельца |
| `kanon/sessions/s13.md` | Сессия 13: L1-B4 closed | источник Владельца |
| `kanon/sessions/s14.md` | Сессия 14: L1-B5-01; parent L1-B5 ещё in progress | источник Владельца |
| `kanon/sessions/s15.md` | Сессия 15: L1-B5-02; Level 1 FORMALLY CLOSED | источник Владельца |
| `kanon/sessions/s16.md` | Сессия 16: L2-B1 closed | источник Владельца |
| `kanon/sessions/s17.md` | Сессия 17: L2-B2 и L2-B3 closed | источник Владельца |
| `kanon/sessions/s18.md` | Сессия 18: L2-B4; Level 2 FORMALLY_CLOSED; L3-B1 ACTIVE; L3 PREF = 0 | источник Владельца |
