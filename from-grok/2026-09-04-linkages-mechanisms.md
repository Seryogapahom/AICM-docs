# Knowledge Candidate — механизмы связей (инкремент к контракту)

ACCESS: 2026-09-04. Не Foundation. Не вход. Не live.
Слой: инкремент `from-grok/2026-09-04-linkages-layer.md` (LNK-1…6). Не замена. Не клеить с EWP / макро if/then / толпой.

## Уточнённые if/then (research IDs)

| id | if/then | источник идеи | тест |
|---|---|---|---|
| LNK-RCORR | rolling Pearson(r_A,r_B; W) > τ_high (или < τ_low) → флаг жёсткой / анти-связки | Investopedia Correlation; OHLCV | BTC+ETH или SPY+QQQ; W∈{20,60,90}d |
| LNK-RBETA | rolling β(A\|Leader) резко растёт → A = high-beta follower | CAPM/OLS | ALT\|BTC или stock\|SPY; 60–120d |
| LNK-CointZ | Engle–Granger/ADF residual стационарен AND \|z\|>k → mean-reversion *кандидат* (не вход) | QuantStart CADF | пара ETF/peers; не BTC alone |
| LNK-FACT | residual после Mkt(+Sector/FF) аномален → идиосинкразия, не общий фактор | Kenneth French Data Library | stock + Mkt-RF; crypto: BTC/ETH proxy |
| LNK-XASSET | VIX↑ AND DXY↑ AND yields↑ → режим risk-off (контекст сжатия corr) | FRED / публичные proxys | BTC/ETH/SPY + VIX + DXY (≥3 ряда) |
| LNK-CRYPTO-ROT | BTC.D↓ AND TOTAL↑ AND ETH/BTC↑ (± ETF net inflow) → ротация в альты (журнал) | TradingView BTC.D/TOTAL; публичные ETF dashboards | BTC.D + TOTAL + ETHBTC |
| LNK-GRAPH-LAG | шок у A AND ребро A→B (peer/supplier) → event-study lag/CAR на B | SEC 10-K customers; WIOD; JoF production-network | ≥2 тикера + дата события |

Соответствие контракту: LNK-1 ≈ RCORR/RBETA; LNK-2 ≈ FACT; LNK-3 ≈ XASSET; LNK-4 ≈ CRYPTO-ROT; LNK-5 ≈ GRAPH-LAG; LNK-6 = дисперсия residual vs sector (рядом с FACT). Первый замороженный прогон по-прежнему **LNK-1a** (`linkages/2026-09-04-lnk1a.md`).

## GitHub shortlist (лицензии уточнены)

| Репо | License (срез) | Зачем | Риск |
|---|---|---|---|
| OpenBB-finance/OpenBB (~72k) | **AGPL-3.0** | мультиактивные ряды | viral AGPL — не тащить в закрытый прод без юриста |
| microsoft/qlib (~48k) | MIT | факторный пайплайн | тяжёлый стек |
| polakowo/vectorbt (~9k) | Commons Clause (ограничение Sell) | corr/β offline | не «свободный продукт» |
| JerBouma/FinanceDatabase (~8k) | MIT | taxonomy peers | не цены |
| dcajasn/Riskfolio-Lib (~4.5k) | BSD-3 | cov/corr / risk contrib | оптимизация ≠ прогноз |
| stefan-jansen/zipline-reloaded (~1.9k) | Apache-2.0 | event-study multi-asset | не бот |
| stefan-jansen/alphalens-reloaded (~0.6k) | Apache-2.0 | IC/quantile по LNK-фичам | нужен panel |
| lukstei/trading-backtest (~0.3k) | MIT | cointegration + Kalman hedge | Java; research |
| KidQuant/Pairs-Trading-With-Python | license unknown | учебный spread | не бот |
| AI4Finance FinRL | MIT | только если state = multi-asset | соблазн live — не core слоя |

Код в AICM-docs не дампить. mlfinlab — commercial history / NOASSERTION: не shortlist «copy freely».

## ML-фичи (имена)

`roll_corr_w60`, `roll_beta_to_btc_w90`, `spread_z_coint`, `adf_p_spread`, `resid_mkt_factor`, `corr_regime_stress`, `dxy_ret_1d`, `vix_chg_1d`, `btc_dominance_chg_7d`, `eth_btc_ret_7d`, `etf_btc_netflow_5d` (если public), `supplier_shock_lag_ret_1_3_5d`, `conditional_comove_score`.

## URL

1. Investopedia Correlation — https://www.investopedia.com/terms/c/correlation.asp
2. QuantStart Cointegration — https://www.quantstart.com/articles/Cointegrated-Time-Series-Analysis-for-Mean-Reversion-Trading-with-R/
3. QuantStart SPY–IWM pairs — https://www.quantstart.com/articles/Backtesting-An-Intraday-Mean-Reversion-Pairs-Strategy-Between-SPY-And-IWM/
4. BTC.D explained — https://crypto.news/what-is-bitcoin-dominance-btc-d-chart-explained/
5. JoF production-network spillovers — https://doi.org/10.1111/jofi.13181
6. Kenneth French Data Library — http://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html

## Честно

Нельзя: причинность из голой corr; вечную пару; altseason по календарю. Можно мерить: условный co-move; рост β; стационарность спреда in-sample + OOS; lag после шока по ребру; risk-off как контекст. n<20 → `INSUFFICIENT_SAMPLE`.
