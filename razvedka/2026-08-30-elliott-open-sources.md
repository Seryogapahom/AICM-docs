# Легальный корпус правил Эллиотта (открытые источники)
ACCESS: 2026-08-30 (Europe/Zurich)
СТАТУС: Knowledge Candidate. Не Foundation. Не Consilium. Не канон AICM.
НАЗНАЧЕНИЕ: сверка с публичной механикой Андреева (`2026-08-30-igor-andreev-public-mechanics.md`). Сверку этот файл не делает.
МЕТОД: только открытые HTML. Пиратские PDF (libgen, pdfcoffee, scribd-дампы, «слив курса») не качались и не являются источником закона.
Правило пишется только если страница его явно формулирует.

Сырьё черновиков:
- `local/intel/_draft-elliott-open.md`
- `local/intel/_draft-elliott-primary-legal.md`
- `local/intel/_draft-elliott-closed.md`

---

## 0. Что закрыто — не тащим

| Имя | Витрина | Почему не тащим |
|---|---|---|
| Frost & Prechter, *Elliott Wave Principle* (EWI: first published 1978) | https://www.elliottwave.com/books/elliott-wave-principle/ ($29) | коммерческий учебник; правил из книги нет в корпусе |
| Glenn Neely, *Mastering Elliott Wave* / NEoWave (1990) | https://windsorpublishing.com/product/mastering-elliott-wave/ ($49.95); https://www.neowave.com/product-book.asp | платная книга; NEoWave-правил нет |
| Bill Williams, *Trading Chaos* 2e (Wiley, Feb 2004, ISBN 978-0-471-46308-5) | https://www.wiley.com/en-us/trading-chaos-maximize-profits-with-proven-technical-techniques-2nd-edition-p-9780471463085 | не книга Эллиотта; Андреев советует; механики из книги нет |
| Школа Игоря Андреева / Igor_Kripta | https://school.igorkripta.ru (лендинг OPENED; «ПРОДАЖИ ЗАКРЫТЫ») | уроки/VIP/программа недель не снимались; сливы не искались |
| EWI subscriptions / Pro / Flagship / Socionomics membership | https://www.elliottwave.com/subscriptions/ | платные сервисы; live counts не извлекаем |
| R.N. Elliott 1938 *The Wave Principle* и 1946 *Nature’s Law* как полный текст | см. §2 | **статус PD неясен**; серый скан ≠ public domain; полный текст не тащим |

**Не использовать как источник закона:** scribd.com dumps; pdfcoffee; любые «полный PDF бесплатно». IA restricted lending (`majorworksofrn00elli`) — не PD.

---

## 1. Открыто / энциклопедия

socionomics.net — HTTP 403, правил нет. elliottwave.net — лендинг GRMF, не корпус. Отдельного systematic review правил на PMC/PubMed нет.

### 1.1 Wikipedia (en) — Elliott wave principle
- URL: https://en.wikipedia.org/wiki/Elliott_wave_principle
- LICENSE: CC BY-SA 4.0
- RULES:
  1. Рынок чередует motive/impulse по тренду и corrective против тренда.
  2. Impulse всегда 5 волн младшей степени: 1, 3, 5 — импульсы; 2 и 4 — откаты.
  3. Коррекция делится на 3 волны младшей степени. Медвежий рынок: 5 вниз, 3 вверх.
  4. Волна 2 никогда не откатывает более 100% волны 1.
  5. Волна 3 не может быть самой короткой из 1, 3 и 5.
  6. Волна 4 никогда не заходит на ценовую территорию волны 1.
  7. Guideline чередования: 2 и 4 часто разной формы; треугольник обычно в 4, очень редко во 2.
  8. Коррекции: зигзаг, плоскость, треугольник; могут складываться в сложные.
  9. Фибо в личностях волн: 2 обычно ≤61.8% от 1; 3 часто 1.618:1 к 1; 4 типично <38.2% от 3; C часто ≥A и часто 1.618×A.
  10. Фрактал степеней Grand supercycle → Subminuette.
- NOT_ON_PAGE: 5-3-5 / 3-3-5 / 3-3-3-3-3 по счёту; expanded/running flat; leading/ending diagonal; равенство 1=5; канал.

### 1.2 Wikipedia (ru) — Волновая теория Эллиотта
- URL: https://ru.wikipedia.org/wiki/Волновая_теория_Эллиотта
- LICENSE: CC BY-SA 4.0
- RULES:
  1. Восемь волн: пять по тренду, три против.
  2. 13 типовых моделей; фрактал по форме, не обязательно по времени/амплитуде.
  3. Соотношения — числа Фибоначчи (конкретные 38.2/50/61.8 страница не называет).
  4. В пятиволновке 1-3-5 движущие, 2-4 коррекционные.
  5. Три свойства: 2 никогда не пересекает старт 1; 3 никогда не самая короткая; 4 никогда не заходит на территорию 1.
  6. Движущие — пятиволновые, коррекционные — трёхволновые (с вариантами).
  7. Цикл = 8: 5 цифрами + 3 буквами; A-B-C корректирует всю 1–5.
  8. Движущие: 1-3-5-A-C; коррекционные: 2-4-B.
- NOT_ON_PAGE: 38.2/50/61.8, 1.618, имена зигзаг/плоскость/треугольник, чередование, 1=5.

### 1.3 Wikipedia — Fibonacci retracement
- URL: https://en.wikipedia.org/wiki/Fibonacci_retracement
- LICENSE: CC BY-SA 4.0
- RULES:
  1. Два экстремума, вертикаль делится фибо-отношениями.
  2. Обычные уровни: 23.6%, 38.2%, 50%, 61.8%.
  3. Горизонтали = support/resistance.
  4. 61.8% = золотое сечение.
  5. Retracement используется в т.ч. в Elliott wave principle (без перечня правил Эллиотта).
  6. Значимость «не подтверждена данными» (Merrill).
- NOT_ON_PAGE: импульс 5 / коррекция 3; hard rules 2/3/4.

### 1.4 StockCharts ChartSchool — Introduction
- URL: https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/introduction-to-elliott-wave-theory
- LICENSE: © StockCharts.com, Inc. All Rights Reserved.
- RULES:
  1. Одни паттерны на lesser и higher degree (фрактал).
  2. Motive всегда по тренду на степень старше; делится на 1–5.
  3. 1, 3, 5 — actionary; 2 и 4 — corrective.
  4. Три правила motive: 2 всегда <100% от 1; 4 всегда <100% от 3; 3 всегда за конец 1 и никогда не самая короткая.
  5. Actionary по 5, corrective по 3 → 5-3-5-3-5.
  6. Коррекция в общем A-B-C как 5-3-5; не все коррекции ровно трёхволновые.
  7. Цикл = 8 (5+3). После цикла ожидается снова 5.
  8. В нисходящем тренде: 5 вниз, 3 вверх.
  9. Это не техника входа/выхода.
- NOT_ON_PAGE: Фибо 38.2/50/61.8; overlap 4 vs 1 (есть <100% отката 4 от 3, не «4 не заходит в 1»); имена ZZ/flat/triangle; 1=5.

### 1.5 StockCharts ChartSchool — Identifying patterns
- URL: https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/identifying-elliott-wave-patterns
- LICENSE: © StockCharts.com, Inc.
- RULES:
  1. Motive: Impulse и Diagonal.
  2. Impulse = 5-3-5-3-5. Три нерушимых: 2 не >100% от 1; 3 никогда не shortest из 1/3/5; 4 никогда не overlap с 1. Нарушение → не impulse.
  3. Sub-wave 3 импульса всегда impulse. Полный retrace 1 отменяет счёт 2.
  4. Extension: обычно одна из 1/3/5; чаще 3.
  5. Truncated fifth: 5 не выходит за конец 3.
  6. Ending diagonal (в 5 или C): 3-3-3-3-3, 2 и 4 могут overlap. Leading diagonal (в 1 или A зигзага): 5-3-5-3-5, но 2 и 4 overlap.
  7. Zigzag A-B-C 5-3-5; sharp; в импульсе обычно во 2.
  8. Flat A-B-C 3-3-5; в 4 часто, во 2 редко. Expanded / running — варианты B и C.
  9. Triangle 3-3-3-3-3 A-B-C-D-E; всегда перед финальным ходом (4 импульса или B зигзага).
  10. Combinations W-X-Y или W-X-Y-X-Z.
- NOT_ON_PAGE: Фибо 38.2/50/61.8 и 1.618; equality 1=5.

### 1.6 StockCharts ChartSchool — Guidelines
- URL: https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/guidelines-for-applying-elliott-wave-theory
- LICENSE: © StockCharts.com. Guideline ≠ rule.
- RULES:
  1. Equality: если 3 extended, 5 ≈ 1 по цене.
  2. Alternation в импульсе: 2 и 4 чередуются (sharp vs sideways).
  3. Alternation в коррекции: A и B чередуются.
  4. Depth: коррекция часто до территории предыдущей Wave 4 младшей степени.
  5. Channeling импульса: параллели по трём точкам.
  6. Scale: arithmetic и semi-log.
  7. Личности: 2 сильно ест 1; 3 самая сильная; 4 sideways; 5 слабее 3 (если не extended).
  8. A из 5 = зигзаг; A из 3 = flat или triangle.
- NOT_ON_PAGE: Fibonacci; hard overlap 4/1.

### 1.7 Investopedia — glossary
- URL: https://www.investopedia.com/terms/e/elliottwavetheory.asp
- LICENSE: коммерческий сайт; Updated May 23, 2026; correction July 27, 2023.
- RULES:
  1. Motive/impulse и corrective; фрактал.
  2. Impulse: 5 подволн по старшему тренду.
  3. Wave 2 can’t retrace more than the beginning of Wave 1.
  4. Wave 3 can not be the shortest of 1, 3, and 5 (correction 2023-07-27).
  5. Wave 4 does not overlap Wave 1 (correction 2023-07-27).
  6. Wave 5 needs to end with momentum divergence. Нарушение → не impulse.
  7. Страница называет corrective «diagonal waves»: 3 или комбинация троек; «corrective wave consists of 5 sub-waves».
  8. Фибо 38% и 62%; коррекция может быть 38% предшествующего импульса.
- NOT_ON_PAGE: ZZ/flat/triangle 5-3-5/3-3-5/3-3-3-3-3; 1=5; 1.618; чередование.
- ОСОБО: формулировка «corrective = diagonal / 5 sub-waves» — слова этой страницы, расходится с ортодоксом Wiki/ChartSchool/Waveopedia.

### 1.8 Investopedia — article 111401
- URL: https://www.investopedia.com/articles/technical/111401.asp
- RULES:
  1. Пять волн в одном направлении, затем три в противоположном.
  2. Impulse по старшему тренду всегда из пяти; corrective против.
  3. Вложенность-матрёшка.
  4. Базовая 5–3 постоянна; длительность волн может меняться.
  5. 1–5 = impulse, A-B-C = correction.
  6. A и C impulsive по 5, B corrective по 3.
  7. Девять степеней Grand super cycle … Sub-minuette.
  8. FAQ: коррекции 38%, 50% и 62%.
- NOT_ON_PAGE: три hard rules 2/3/4; ZZ/flat/triangle; 1=5.

### 1.9 Investopedia — Fibonacci retracement
- URL: https://www.investopedia.com/terms/f/fibonacciretracement.asp
- Updated December 23, 2025.
- RULES:
  1. Retracement-зоны из ряда Фибоначчи.
  2. 23.6%, 38.2%, 50%, 61.8%, 78.6%; чаще 38.2/50/61.8.
  3. Два якоря swing high/low.
  4. Extensions: 100%, 161.8%, 261.8%.
  5. Связь с Эллиоттом явно: retracements для Wave 2 и 4; extensions для Wave 3 и Wave C.
- NOT_ON_PAGE: корпус hard rules Эллиотта.

### 1.10 EWI free HTML — Introduction
- URL: https://www.elliottwave.com/free/introduction-to-the-wave-principle/
- LICENSE: © 2026 Elliott Wave International. Бесплатный HTML, не paywall-курс.
- RULES:
  1. Impulsive = 5 подволн по тренду следующей большей величины.
  2. Corrective = 3 подволны против того тренда.
  3. 1–5 = больший импульс → трёхволновая (2) → снова импульс.
  4. Ищут завершённые 5- и 3-структуры. ≥2 валидных счёта; preferred = максимум guidelines.
  5. Фибо только после валидной интерпретации. Коррекции: 38%, 50%, 62%.
  6. 13 паттернов, повторяющихся по форме.
  7. Прогресс = пять волн; (2)(4) обязательные перерывы.
- NOT_ON_PAGE: явный список hard rules 2/3/4; ZZ/flat/triangle; 1=5; 1.618.

### 1.11–1.20 EWI Waveopedia (открытый HTML, © 2026 EWI)

| карточка | URL | ядро правил на странице |
|---|---|---|
| Impulse | https://www.elliottwave.com/waveopedia/impulse/ | 5 волн 5-3-5-3-5 без overlap; 4 не входит в территорию 1 (cash; на фьючерсах overlap редок); подволна 3 всегда impulse |
| Motive Waves | https://www.elliottwave.com/waveopedia/motive-waves/ | motive=5; 2 всегда <100% от 1; 4 всегда <100% от 3; 3 всегда за конец 1; 3 никогда не shortest; impulse и diagonal |
| Corrective Waves | https://www.elliottwave.com/waveopedia/corrective-waves/ | тройки против тренда; Corrections are never fives; ZZ 5-3-5 / Flat 3-3-5 / Triangle 3-3-3-3-3; sharp vs sideways |
| Zigzags | https://www.elliottwave.com/waveopedia/zigzags/ | sharp A-B-C 5-3-5; в импульсах 2-я часто zigzag, 4-я редко; double/triple W-X-Y |
| Flats | https://www.elliottwave.com/waveopedia/flats/ | sideways 3-3-5; 4 часто, 2 редко; regular / expanded (Elliott: «irregular») / running |
| Triangles | https://www.elliottwave.com/waveopedia/triangles/ | 3-3-3-3-3 A-B-C-D-E; всегда перед финальной actionary (4 импульса, B в ABC); «треугольник во 2» почти всегда часть double three |
| Fibonacci Relationships | https://www.elliottwave.com/waveopedia/fibonacci-relationships/ | .618 / .382 / 1.618; коррекции 38% (common), также 50% и 62%; фибо только при валидном счёте |
| Equality | https://www.elliottwave.com/waveopedia/equality/ | если 3 самая длинная, 5 и 1 стремятся быть равны; иначе множитель .618 |
| Extension | https://www.elliottwave.com/waveopedia/extension/ | обычно extension в одной и только одной из 1/3/5; чаще 3; 9 сходных волн ≡ 5 |
| Alternation | https://www.elliottwave.com/waveopedia/alternation/ | если 2 sharp, 4 sideways и наоборот; guideline, не закон; diagonal не чередует 2 и 4 |

Полные 5–10 пунктов по каждой карточке — в `_draft-elliott-open.md`.

### 1.21 PMC — не обзор правил
- URL: https://pmc.ncbi.nlm.nih.gov/articles/PMC7836128/
- LICENSE: CC BY-NC-ND 4.0. COVID-приложение + Fibonacci Pinball авторов, не канон Frost/Prechter.
- Не systematic review. Hard rules 2/3/4 не сформулированы.

### 1.22 Scientific Reports — NFT эмпирика
- URL: https://www.nature.com/articles/s41598-024-55011-x
- 23 Feb 2024, OA. Результат: autocycles в NFT не поддержали Elliott Wave behavior.
- Не учебник правил.

---

## 2. Первоисточник 1938 / 1946 — где легально

**Вердикт PD: статус неясен.** Не выдавать серый скан за public domain. Elliott ум. 15.01.1948 — это не PD-вердикт.

| работа | легальный путь 2026-08-30 | полный бесплатный PD-текст |
|---|---|---|
| 1938 *The Wave Principle* (ii+50 лл., LCCN 42043983, LC HG6041 .E4 1938) | купить Alanpuri facsimile **$50**: https://www.alanpuritrading.com/product/wave-principle-1938-r-n-elliott/ ; 3-set **$110**; LOC offsite «Request item»; EWI *Masterworks* (~$29 в сниппете, HTML timeout) | **нет / не доказано** |
| 1946 *Nature’s Law* (64 стр., 63 Wall St.) | Alanpuri facsimile **$50**: https://www.alanpuritrading.com/product/natures-law-secret-universe-1946-r-n-elliott/ ; Snowball 124p **$15.62** (не факсимиле, не 64 стр.) | **нет / не доказано** |

Internet Archive: отдельного item на оригинал 1938/1946 нет. Есть компиляция Prechter *The major works of R. N. Elliott* (NCL, metadata 1990): https://archive.org/details/majorworksofrn00elli — `access-restricted-item: true`, `printdisabled`/`inlibrary`, «No suitable files to display here», lending AVAILABLE при логине. Это **не** 1938 pamphlet и **не** PD.

Open Library 1938: https://openlibrary.org/books/OL6445643M/The_wave_principle — «currently unavailable». Google Books: No preview. HathiTrust: карточка не открылась.

CCE Gutenberg-транскрипты renewal ~1965–66 и ~1973–74: заглавий R.N. Elliott / этих двух книг не видно. **Это не юридическое «не renewili» и не PD.**

webtrading.org ($47 microfilm reprint) — серый коммерческий репринт, не первоисточник и не PD.

---

## 3. Ортодокс, который можно тащить в сверку (из открытых страниц)

Собран с Wikipedia en + ChartSchool Identifying + Waveopedia. Не из Frost/Prechter/Neely/Williams/школы.

1. Impulse = 5 (5-3-5-3-5). Hard: 2 не >100% от 1; 3 не shortest; 4 не overlap с 1.
2. Corrections are never fives. ZZ 5-3-5; flat 3-3-5; triangle 3-3-3-3-3.
3. Чередование 2/4 — guideline, не hard rule.
4. Фибо коррекции 38/50/62; 3 часто 1.618; equality 1≈5 если 3 extended.
5. Треугольник обычно в 4, не во 2.
6. Extension обычно в одной из 1/3/5, чаще 3.

Расхождения внутри открытого слоя (не закрывать как закон):
- ChartSchool intro: «4 <100% от 3», не overlap 4 vs 1.
- Investopedia glossary: momentum divergence на 5; путает corrective с diagonal.
- ru.Wikipedia не называет 38.2/50/61.8.

---

## 4. Отчёт штабу — список URL

**Открытые (правила сняты):**
- https://en.wikipedia.org/wiki/Elliott_wave_principle
- https://ru.wikipedia.org/wiki/Волновая_теория_Эллиотта
- https://en.wikipedia.org/wiki/Fibonacci_retracement
- https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/introduction-to-elliott-wave-theory
- https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/identifying-elliott-wave-patterns
- https://chartschool.stockcharts.com/table-of-contents/market-analysis/elliott-wave-analysis-articles/guidelines-for-applying-elliott-wave-theory
- https://www.investopedia.com/terms/e/elliottwavetheory.asp
- https://www.investopedia.com/articles/technical/111401.asp
- https://www.investopedia.com/terms/f/fibonacciretracement.asp
- https://www.elliottwave.com/free/introduction-to-the-wave-principle/
- https://www.elliottwave.com/waveopedia/impulse/
- https://www.elliottwave.com/waveopedia/motive-waves/
- https://www.elliottwave.com/waveopedia/corrective-waves/
- https://www.elliottwave.com/waveopedia/zigzags/
- https://www.elliottwave.com/waveopedia/flats/
- https://www.elliottwave.com/waveopedia/triangles/
- https://www.elliottwave.com/waveopedia/fibonacci-relationships/
- https://www.elliottwave.com/waveopedia/equality/
- https://www.elliottwave.com/waveopedia/extension/
- https://www.elliottwave.com/waveopedia/alternation/
- https://pmc.ncbi.nlm.nih.gov/articles/PMC7836128/ (не корпус правил)
- https://www.nature.com/articles/s41598-024-55011-x (эмпирика против, не учебник)

**Первоисточник (купить / borrow, текст не тащим):**
- https://www.alanpuritrading.com/product/wave-principle-1938-r-n-elliott/
- https://www.alanpuritrading.com/product/natures-law-secret-universe-1946-r-n-elliott/
- https://archive.org/details/majorworksofrn00elli (restricted, компиляция NCL)
- https://lccn.loc.gov/42043983

**Закрыто, только имена:**
- https://www.elliottwave.com/books/elliott-wave-principle/
- https://windsorpublishing.com/product/mastering-elliott-wave/
- https://www.wiley.com/en-us/trading-chaos-maximize-profits-with-proven-technical-techniques-2nd-edition-p-9780471463085
- https://school.igorkripta.ru
