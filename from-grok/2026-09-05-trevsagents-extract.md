# Trevs Agents / trevortaylor29 — независимое извлечение (TA-01…)

Статус: Knowledge Candidate / pattern reference. **Не канон. Не live. Не identity AICM.**  
Провенанс: штаб Grok, GitHub API + Contents API, **2026-09-05**. ChatGPT share — только intake.

## Идентификация

| Узел | Факт API |
|---|---|
| GitHub | [`trevortaylor29`](https://github.com/trevortaylor29) — name «Trevor», 14 public repos, created 2018-08-10 |
| Сайт бренда | https://trevsagents.com/ (landing; покупки не тестировались) |
| Лендинг-репо | [`trevasgents`](https://github.com/trevortaylor29/trevasgents) — Next.js landing, **нет backend**, покупки → Gumroad; README ещё упоминает `tonkasdungeon.com` |
| Instagram/YouTube | @trevsagents (маркетинг; PnL **не** независимый evidence) |

**ACE / BOLT / SAGE** (спортивные ставки / крипто / акции на скриншоте): по дереву публичных репо `Fundamental`, `trevasgents`, `bofbot`, `whataptisthis` — **реализации торговой арены / paper-агентов не найдено**. Могут быть закрытыми или не опубликованы.

## Репозитории (срез)

Все 14 public; звёзды **0** у ключевых. Лицензии:

| repo | SPDX / факт | pushed |
|---|---|---|
| **Fundamental** | `NOASSERTION`; файл `LICENSE` **size=1** (пустая строка) | 2025-09-06 |
| **trevasgents** | нет | 2026-07-02 |
| **bofbot** | нет | 2026-05-14 |
| **whataptisthis** | нет | 2026-05-02 |
| остальные (учебные OOP/quiz/…) | нет | 2022 |

**Публичный репозиторий ≠ разрешённое копирование кода.** Перед любым переносом исходников — явный grant от автора или другой лицензии. Пока: **только идеи / формулы / UX-паттерны**, не vendor drop.

## Fundamental (приоритет №1 для изучения)

Streamlit research tool: сравнение ETF/funds; `yfinance`; score 0–100.

Ключевые модули: `fundintel/data.py`, `fundintel/score.py`, `fundintel/compare.py`, `universe.py`, `news.py`.

### Подтверждено в коде

1. **`_logistic01`**: при `nan` или `width<=0` возвращает **`0.5`** — «неизвестно» выглядит как середина шкалы (`fundintel/score.py`).
2. **`_downside_vol(window=63)`**: параметр `window` **не используется** — downside std по всей истории отрицательных returns (баг/несогласованность с docstring окна).
3. Столпы: perf / risk / quality / consistency vs S&P; веса зависят от risk preference и horizon.
4. **Broad-market anchor bonus**: SPY/VOO/IVV/SPLG/VTI/^GSPC (+ name terms) получают `+0.10/+0.05/+0.02` к total01 до clip — **авторский bias**, не нейтральный рейтинг.
5. Score — формула, **не** вероятность прибыльной сделки.

## whataptisthis (Apartment Decoder)

MVP: признаки из медиа → веб-поиск (Serper) → ранжирование кандидатов (OpenRouter vision + reasoning) → confidence + limits. Есть mock mode.  
**Для AICM:** схема research pipeline (evidence + confidence + ограничения), не недвижимость.

## bofbot

Публичный репо без SPDX; продукт/сайт отдельно (https://bofbot.com/).  
**Для AICM:** идея локального production-модуля контента — низкий приоритет для торгового ядра; лицензия неясна.

## trevasgents

Маркетинговый сайт. Цены/тарифы в README **устарели относительно живого сайта** — не брать как источник условий. Следы бренда Tonka’s Dungeon.

## TA — что копировать (идеи), куда, чего не брать

| ID | Что | Evidence | Copy? | Куда (лаба) | Риск / NOT |
|---|---|---|---|---|---|
| **TA-01** | Прозрачный multi-pillar score + объяснение вкладов | `score.py` pillars | **Да (идея)** | research UI / сравнение механизмов | Не как WR/вероятность |
| **TA-02** | Явная полнота данных вместо нейтрали 0.5 | `_logistic01` → 0.5 | **Да (исправить урок)** | любые score-карты | Fake mid = ложная уверенность |
| **TA-03** | Consistency vs benchmark (excess + win windows) | S_cons vs ^GSPC/SPY | **Частично** | сверка стратегий с baseline | Окна и веса — авторские |
| **TA-04** | Research pipeline: clues → sources → candidates → confidence | whataptisthis README/spec | **Да (процесс)** | разведка возможностей / macro/news | Не копировать продукт |
| **TA-05** | Специализация агента + история действий в UI | маркетинг UI (скрин) | **Идея UX** | demo dashboard | Не спорт-арена капитала |
| **TA-06** | Локальный content/batch tool как сменный контейнер | bofbot (поверхность) | **Низкий приоритет** | неторговые ветки позже | Лицензия / не ядро |

### Явно НЕ брать

1. Исходники без лицензии / пустой LICENSE как «MIT-like».
2. ACE/BOLT/SAGE / sportsbook / paper→live как доказанный edge.
3. Instagram/YouTube PnL и заявления Inner Circle ($ / участники).
4. Broad-market bonus и авторские веса «как есть» без своей калибровки.
5. Лендинг/Gumroad/Fuel credits как архитектуру Hermes.
6. Путать hashtag OpenClaw/Hermes в роликах с авторством этих систем.

## Цикл / следующие шаги

- Повторный взгляд: только если появится **публичный** репо с trading agents / paper ledger (watch `trevortaylor29`).
- Приоритет теста в лабе: **прогнать идеи TA-01/02 на своих метриках** (не vendor app) после канонов; не ставить Bitget от этого пакета.
- Разведчику: KC-карта URL + LICENSE status (без полного клона).

## Изоляция

Pattern reference only. Не запускать чужие бинарники с production keys. Не покупать Inner Circle ради кода.
