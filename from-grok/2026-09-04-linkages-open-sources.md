# Knowledge Candidate: механизмы связности активов (A→B / сектор / картина)

| Поле | Значение |
|------|----------|
| ID слой | **LINK-*** (Knowledge Candidate only) |
| Дата доступа | **2026-09-04** |
| Автор слоя | лаборатория Grok (разведка) |
| PREF | **нет** — не PREF |
| Entry / live-trade | **нет** |
| EWP / Elliott | **не клеить** |
| Macro NFP if/then | **не клеить** |
| GitHub write / dump в наш git | **не делалось** |
| Назначение | механизмы, линзы трейдера, открытые docs, OSS для *копирования механизма* |

---

## Что это

Как новость или дроп в **A** передаётся в **B**, в сектор и в «целую картину»: корреляция / бета / коинтеграция; факторные нагрузки; граф поставщиков/пиров; в крипте — BTC dominance, beta альтов, ETF flow, basis/funding. Здесь — **открытые** первичные docs/papers/tools и GitHub, откуда можно **украсть механизм** (не код в наш репозиторий). Не entry. Не live.

Метки на карточках: **copyable** = механизм можно перенять; **adaptable** = идея/API открыты, адаптация нужна; **не брать** = закрыто / SaaS-only / лицензия блокирует.

---

## 1. Открытые корреляции / beta / коинтеграция

**LINK-01** · https://www.statsmodels.org/stable/generated/statsmodels.tsa.stattools.coint.html  
Engle–Granger (`statsmodels.tsa.stattools.coint`): тест «нет коинтеграции» для пары I(1); для AICM — первичный открытый тест связности спреда A–B, не путать с корреляцией. · **copyable**

**LINK-02** · https://www.statsmodels.org/dev/generated/statsmodels.tsa.vector_ar.vecm.coint_johansen.html  
Johansen (`coint_johansen` / VECM): ранг коинтеграции для **нескольких** рядов; для AICM — когда «картина» >2 активов (секторный basket). · **copyable**

**LINK-03** · https://bashtage.github.io/linearmodels/ (repo: https://github.com/bashtage/linearmodels · NCSA)  
Panel/asset-pricing регрессии (CAPM, Fama–MacBeth и т.п.): rolling/time-series beta к рынку как линза «A дроп → нагрузка на B». · **copyable**

**LINK-04** · https://arch.readthedocs.io/ (bashtage/arch)  
GARCH/EGARCH волатильности и ковариационных режимов: для AICM — когда связность «ломается» в стрессе (corr spike ≠ стационарный спред). · **adaptable**

**LINK-05** · https://www.quantconnect.com/docs/v2/research-environment/applying-research/pca-and-pairs-trading  
QuantConnect LEAN Research: PCA → кандидаты пар → Engle–Granger на спреде; открытый tutorial-механизм pair screen без dump кода в наш git. · **adaptable**

**LINK-06** · https://www.quantconnect.com/docs/v2/writing-algorithms/algorithm-framework/alpha/supported-models  
LEAN Alpha: PearsonCorrelation / BasePairsTrading models — как платформа смотрит на ratio mean-reversion (линза трейдера, не сигнал entry). · **adaptable**

---

## 2. Факторные модели

**LINK-07** · https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html  
Ken French Data Library: FF3/FF5/MOM + test portfolios, free CSV; канон для «сектор/стиль» связности через SMB/HML/RMW/CMA. · **copyable** (данные; цитировать источник)

**LINK-08** · https://www.aqr.com/Insights/Datasets · https://www.aqr.com/Insights/Datasets/About-the-AQR-Data-Library  
AQR Data Library: BAB, QMJ, Value&Momentum Everywhere, TSMOM — открытые факторные ряды к papers; расширяет FF-линзу без Barra. · **copyable** (данные; academic citation)

**LINK-09** · https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html  
sklearn PCA: ортогональные факторы доходности → «общий шок» vs идиосинкразия; Barra-style **approximation**, не коммерческий Barra. · **copyable**

**LINK-10** · https://riskfolio-lib.readthedocs.io/ · https://github.com/dcajasn/Riskfolio-Lib  
Riskfolio-Lib: risk factors, PCA risk, risk parity — портфельная обёртка факторной связности. · **copyable** (BSD-3-Clause)

**LINK-11** · https://pyportfolioopt.readthedocs.io/ · https://github.com/PyPortfolio/PyPortfolioOpt  
PyPortfolioOpt: covariance estimators / risk models как вход в «как A тянет корзину». · **copyable** (MIT)

---

## 3. Company graphs: supply-chain / peers

**LINK-12** · https://www.gleif.org/en/lei-data/access-and-use-lei-data/ · https://www.gleif.org/en/lei-data/lei-mapping/download-oc-to-lei-relationship-files  
GLEIF LEI (+ open OC↔LEI mapping CSV): открытая **identity** юрлица / parent–subsidiary; якорь графа, не FactSet. · **copyable**

**LINK-13** · https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html  
OECD ICIO: межстрановые input–output потоки (сектор×страна) — механизм «шок в upstream → downstream сектор». · **copyable** (официальные таблицы)

**LINK-14** · https://www.bea.gov/data/industries/input-output-accounts-data  
US BEA Input–Output Accounts: Make/Use/Requirements — US supply-chain матрица для отраслевого A→сектор. · **copyable**

**LINK-15** · https://comtradeplus.un.org/ (UN Comtrade)  
Продуктовая торговля; с ICIO — product-level GVC vulnerability (как в OECD papers). · **adaptable** (лимиты API/лицензии использования данных)

**LINK-16** · https://www.wikidata.org/ · свойство LEI (P1278), OpenCorporates ID (P1320)  
Wikidata: открытый entity graph для peers/affiliates; Diffbot — **не брать** как identity. · **adaptable**

**LINK-17** · https://networkx.org/documentation/stable/ · https://github.com/networkx/networkx (BSD-3-Clause в LICENSE.txt)  
NetworkX: DiGraph поставщик→клиент, centrality, contagion-прототипы на IO/EDGAR edges. · **copyable**

**Примечание identity:** FactSet / Bloomberg peer & supply-chain — **не брать** как канон identity (закрыто). OpenCorporates полезен, но bulk/API часто коммерческий — GLEIF mapping files предпочтительнее как открытый слой.

---

## 4. Crypto linkages: BTC dominance / alts beta / ETF flow

**LINK-18** · https://www.tradingview.com/symbols/BTC.D/  
BTC.D (Bitcoin Dominance): доля BTC в crypto mcap — линза ротации BTC↔alts («дроп dominance → альты» как гипотеза, не causation). · **adaptable** (публичная страница; не API-ключ)

**LINK-19** · https://farside.co.uk/btc/ · (ETH: https://farside.co.uk/eth/)  
Farside Investors: дневные таблицы spot BTC/ETH ETF flows по эмитентам — read-only публичный источник flow→price linkage. · **adaptable**

**LINK-20** · https://sosovalue.com/assets/etf/us-btc-spot  
SoSoValue: дашборд US spot BTC ETF (AUM, per-fund flows) — визуальная линза институционального потока. · **adaptable** (read-only; не live bot)

**LINK-21** · https://www.coinglass.com/etf/bitcoin · https://www.coinglass.com/FundingRate/BTC · https://www.coinglass.com/open-interest/BTC  
CoinGlass public: ETF + funding + OI — cross-exchange basis/funding как связность leverage↔spot; **без ключей**, только публичные страницы. · **adaptable**

**LINK-22** · https://researchonline.lse.ac.uk/id/eprint/137306/1/Bitcoin_ETFs_and_structural_decoupling_in_the_cryptocurrency_market_evidence_from_altcoin_correlation_dynamics.pdf  
LSE/open PDF (Li et al., 2026): post-ETF decoupling — падение corr BTC–alts; механизм «independent inflows» в BTC. · **copyable** (идея/эмпирика; не код)

**Не брать здесь:** Glassnode SaaS API keys; live Bitget/X bot; вызов X.

---

## 5. GitHub repos (механизм украсть; лицензия проверена 2026-09-04)

| # | Repo | URL | License | Что украсть | Вердикт |
|---|------|-----|---------|-------------|---------|
| R1 | **statsmodels** | https://github.com/statsmodels/statsmodels | **BSD-3-Clause** | `coint`, Johansen/VECM — ядро pair/basket linkage | **брать механизм** |
| R2 | **empyrical** | https://github.com/quantopian/empyrical | **Apache-2.0** | beta/alpha/rolling risk metrics к бенчмарку | **брать** (archived-friendly; API стабилен) |
| R3 | **alphalens** | https://github.com/quantopian/alphalens | **Apache-2.0** | factor tear-sheet: IC, quantile returns — линза фактора, не entry | **брать** |
| R4 | **qlib** | https://github.com/microsoft/qlib | **MIT** | research workflow: факторы, alpha pipeline, dataset handlers | **брать механизм** |
| R5 | **PyPortfolioOpt** | https://github.com/PyPortfolio/PyPortfolioOpt | **MIT** | covariance / risk models как вход связности корзины | **брать** |
| R6 | **Riskfolio-Lib** | https://github.com/dcajasn/Riskfolio-Lib | **BSD-3-Clause** | PCA risk factors, risk contribution | **брать** |
| R7 | **machine-learning-for-trading** | https://github.com/stefan-jansen/machine-learning-for-trading | **MIT** | notebooks: FF factors, pairs/coint patterns — учебный каркас | **брать как шаблон**, не dump в наш git |
| R8 | **networkx** | https://github.com/networkx/networkx | **BSD-3-Clause** (текст LICENSE.txt) | graph ops для supply-chain / peer contagion | **брать** |

### Проверено и **не брать** / с оговоркой

| Repo | URL | License | Почему |
|------|-----|---------|--------|
| mlfinlab | https://github.com/hudson-and-thames/mlfinlab | **proprietary / Other** (LICENSE.txt agreement) | ограниченная коммерческая лицензия — **не брать** |
| vectorbt | https://github.com/polakowo/vectorbt | **Apache-2.0 + Commons Clause** | нельзя «Sell» продукт на базе — **не брать** для продакшн-обёрток; только личное чтение идеи |
| yfinance / ta / freqtrade / ccxt | (data/bot) | разное | data-only или торговый бот — **не linkage model**; ccxt ≠ модель связности |
| edgar-crawler | https://github.com/lefterisloukas/edgar-crawler | **GPL-3.0** | полезен для текста 10-K, но copyleft — **осторожно** (не в proprietary dump); механизм парсинга адаптировать отдельно |
| Glassnode scrapers без лицензии | — | часто нет LICENSE | **не брать** |

---

## Не брать (явно)

- Live API keys, school-only paywalls как «канон».
- Клей с EWP/Elliott или с macro NFP if/then слоем.
- Корреляция = причинность.
- Dump FRED/факторных CSV в наш git.
- FactSet/Bloomberg/Diffbot как identity.
- Live-trade / Bitget bot / вызов X.

---

## Gaps / provenance

| Gap | Деталь |
|-----|--------|
| Barra OSS | Полноценного open Barra нет; PCA + FF/AQR — приближение. |
| Firm-level supply graph | OECD/BEA — сектор; firm edges из EDGAR NLP — шумные, лицензии crawler'ов разные. |
| ETF flow machine-readable | Farside/SoSoValue — HTML/таблицы; стабильного OSS scraper с чистой лицензией не зафиксировали. |
| Alts beta papers | Много blog-grade; LINK-22 — один проверяемый academic PDF. |
| vectorbt / mlfinlab | Исключены по лицензии несмотря на техническую релевантность. |
| Provenance | Access date **2026-09-04**; лицензии — raw LICENSE / GitHub API; docs — WebFetch/WebSearch; лежит в from-grok/. |

**Счётчик:** LINK-01 … LINK-22 = **22** карточки; GitHub в §5 = **8** (плюс таблица исключений).

