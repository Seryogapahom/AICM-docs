# Канонист — индекс карточек drop1 (vision + addenda 01–05)

Это **не** герметика ~190MB live/Hermes-сессий. Это карточки предпочтений по unpacked Foundation Vision package 2026-08-20 with Trading Foundation sessions 01–05.

Источник ROOT (zip sha256 verified `227b7204505f422b837f44a241d6bda97db73eea7a853446cdc35bf3f2718786`):

`aicm_foundation_vision_package_2026-08-20_with_trading_foundation_sessions-01-02-03-04-05-addenda`

Корневой MANIFEST пакета: status `DISCUSSION_DRAFT`, canonical `false`, timezone Europe/Zurich, contract/implementation/runtime_authority `none`. `lineage/` — только provenance predecessor zips, не отдельные сессии.

Картограф **не** вызывался. Дубли и преемники только помечены внутри карточек.

Все карточки: UTF-8 markdown, русский; English technical terms сохранены как в источнике. Markdown originals достаточны (docx пропущены). L0–L2 source files не переписывались.

| файл | дата | статус | package_id | numbered PREF verbatim/gist/mention | что добавила единица | дубли / преемники |
|---|---|---|---|---|---|---|
| `vision.md` | 2026-08-18 | DISCUSSION_DRAFT | `AICM-FOUNDATION-VISION-PACKAGE-2026-08-18` | 0/0/0 numbered; vision-statements 27/1/0 | Конституция AICM, роль Trading Foundation, Capability Registry, Mac Studio primary, one ACCEPT → Terminal Closed | исходник; numbered PREF нет |
| `s01.md` | 2026-08-18 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | `AICM-TRADING-FOUNDATION-INTERNAL-MODEL-ADDENDUM-2026-08-18-SESSION-01` | 11/0/0 | Knowledge/hypothesis: TF-PREF-001…011 (source≠knowledge, competing scenarios, waiting, auto feedback) | первое появление 001–011 |
| `s02.md` | 2026-08-18 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | `AICM-TRADING-FOUNDATION-KNOWLEDGE-OBJECT-MODEL-ADDENDUM-2026-08-18-SESSION-02` | 6/0/6 | Object model + bootstrap: TF-PREF-012…016; AICM-ARCH-DISC-PREF-001 | mention/дубль 002,006–009,011 vs s01; 012–016 получат v0.2 в s03 |
| `s03.md` | 2026-08-19 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | `AICM-TRADING-FOUNDATION-KNOWLEDGE-OBJECT-MODEL-ADDENDUM-2026-08-19-SESSION-03` | 19/0/0 | v0.2 object-model/bootstrap + TF-PREF-017…030 (planes, SourceAssertion, identity, maturity≠authority, training-derived, bounded dependency) | преемник 012–016 vs s02; relation `additive_only_with_versioned_preference_successors_no_in_place_rewrite` |
| `s04.md` | 2026-08-19 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | `AICM-TRADING-FOUNDATION-SITUATION-CONTEXT-AND-AUTONOMOUS-EVOLUTION-ADDENDUM-2026-08-19-SESSION-04` | 13/0/2 | SituationContextSnapshot TF-PREF-031…034; Layer Zero AICM-L0-PREF-001…009 | mention 001 и 030; Purpose Kernel ещё OPEN |
| `s05.md` | 2026-08-20 | DISCUSSION_CAPTURE_AND_PREFERENCE_DRAFT | `AICM-TRADING-FOUNDATION-PURPOSE-KERNEL-AND-AUTONOMY-ADDENDUM-2026-08-20-SESSION-05` | 10/0/15 | AICM-L0-PREF-010…019; закрыт Block 1 Purpose Kernel and cold start | mention L0-001…009, TF-031…034, TF-001, TF-030; не rewrite 001–034 / L0-001–009 |

Счётчики — уникальные numbered PREF ID на карточку, одна fidelity на ID. Vision считается отдельно (нет PREF ID).

---

# Drop2 — addenda 13–18

Это **не** архив s06–s12: в этой пачке их нет, тела L0-020–043 / L1-001–019 / L2 до s13 **не выдуманы**. Drop1 таблица выше не переписывалась.

Корни пакетов (zip в git не кладём):
- `AICM-TRADING-FOUNDATION-SESSION-13-ADDENDUM-2026-08-22`
- `AICM-TRADING-FOUNDATION-SESSION-14-ADDENDUM-2026-08-22`
- `AICM-TRADING-FOUNDATION-SESSION-15-ADDENDUM-2026-08-23`
- `AICM-TRADING-FOUNDATION-SESSION-16-ADDENDUM-2026-08-23`
- `AICM-TRADING-FOUNDATION-SESSION-17-ADDENDUM-2026-08-23`
- `AICM-TRADING-FOUNDATION-SESSION-18-ADDENDUM-2026-08-24`

Картограф **не** вызывался. GitHub / zip / Hermes / live не трогались. L0–L2 source не переписывались.

| файл | дата | статус | package_id | numbered PREF verbatim/gist/mention-group | что закрыла единица | OPEN remaining (named) |
|---|---|---|---|---|---|---|
| `s13.md` | 2026-08-22 | `L1_B4_CONSILIUM_AND_KNOWLEDGE_EVOLUTION_AUTHORITY_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-13-ADDENDUM-2026-08-22` | 11/0/1 (`AICM-L1-PREF-020`…`030`; closure `AICM-L1-B4-CLOSURE-001` отдельно) | **L1-B4** semantic | `OPEN-12-01`…`06`, `OPEN-13-01`…`10` |
| `s14.md` | 2026-08-22 | `L1_B5_01_BEST_BOUNDED_SLICE_SELECTION_AND_SCOPE_CONTRACT_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-14-ADDENDUM-2026-08-22` | 9/0/1 (`AICM-L1-PREF-031`…`039`; closure `AICM-L1-B5-01-CLOSURE-001` отдельно) | **L1-B5-01** semantic; parent L1-B5 ещё IN PROGRESS | `OPEN-12-01`…`06`, `OPEN-13-01`…`09`, `OPEN-14-01`…`10` (`OPEN-13-10` закрыт slice) |
| `s15.md` | 2026-08-23 | `LEVEL_1_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-15-ADDENDUM-2026-08-23` | 16/0/1 (`AICM-L1-PREF-040`…`055`) | **L1-B5-02**, parent **L1-B5**, **Level 1** FORMALLY CLOSED | `OPEN-12-01`…`06`, `OPEN-13-01`…`09` (`OPEN-14-01`…`10` закрыты) |
| `s16.md` | 2026-08-23 | `L2_B1_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-16-ADDENDUM-2026-08-23` | 33/0/1 (`AICM-L2-PREF-001`…`033`) | **L2-B1** semantic; Level 2 ещё OPEN | `OPEN-17-01`…`12` (`OPEN-16-01`…`11` закрыты) |
| `s17.md` | 2026-08-23 | `L2_B2_AND_L2_B3_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-17-ADDENDUM-2026-08-23` | 69/0/1 (`AICM-L2-PREF-034`…`102`) | **L2-B2**, **L2-B3**; Level 2 ещё OPEN | `OPEN-18-01`…`12` (`OPEN-17-01`…`12` закрыты) |
| `s18.md` | 2026-08-24 | `READY` | `AICM-TRADING-FOUNDATION-SESSION-18-ADDENDUM-2026-08-24` | 44/0/1 (`AICM-L2-PREF-103`…`146`) | **L2-B4**; **Level 2** FORMALLY_CLOSED; L3-B1 ACTIVE_NOT_CLOSED; confirmed L3 PREF = 0 | `OPEN-19-01`…`12` (`OPEN-18-01`…`12` закрыты) |

Unique NEW numbered PREF IDs drop2: **182** (`L1-020`…`055` = 36; `L2-001`…`146` = 146). Inherited TF/L0/L1-prior/DOC — mention-group, не reopen. Именованные REJECTED: s13 `REJECTED-13-01`…`19`; s14 `REJECTED-14-01`…`15`; s15/s16/s17/s18 именованных REJECTED ID нет.

---

# s06–s12 (drop3–drop6)

Drop1 и Drop2 таблицы выше **не переписывались**. Картограф не вызывался. GitHub / zip / Hermes / live не трогались.

Корни пакетов (zip в git не кладём):
- `AICM-TRADING-FOUNDATION-GOAL-FORMATION-PORTFOLIO-ADDENDUM-2026-08-21-SESSION-06`
- `AICM-TRADING-FOUNDATION-SESSION-07-ADDENDUM-2026-08-21`
- `AICM-TRADING-FOUNDATION-SESSION-08-ADDENDUM-2026-08-21`
- `AICM-TRADING-FOUNDATION-SESSION-09-ADDENDUM-2026-08-22`
- `AICM-TRADING-FOUNDATION-SESSION-10-ADDENDUM-2026-08-22`
- `AICM-TRADING-FOUNDATION-SESSION-11-ADDENDUM-2026-08-22`
- `AICM-TRADING-FOUNDATION-SESSION-12-ADDENDUM-2026-08-22`

Lineage **по источнику**, не подгонка HQ: s06 не закрывает L0-B2; s12 закрывает L1-B3, не L1-B2.

| файл | дата | статус | package_id | numbered PREF verbatim/gist/mention-group | что закрыла единица | OPEN remaining (named) |
|---|---|---|---|---|---|---|
| `s06.md` | 2026-08-21 | `DISCUSSION_CAPTURE_AND_PARTIAL_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-GOAL-FORMATION-PORTFOLIO-ADDENDUM-2026-08-21-SESSION-06` | 10/0/1 (`L0-020`…`024`, `DOC-001`…`004`, `ROADMAP-L0-APPROVAL-001`). `025`…`032` proposed, не confirmed | L0-B2 **IN_PROGRESS_PARTIALLY_CLOSED**, не закрыт | `OPEN-06-01`…`12` |
| `s07.md` | 2026-08-21 | `L0_B2_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-07-ADDENDUM-2026-08-21` | 8/0/1 (`L0-025`…`032`); closure `L0-B2-CLOSURE-001` отдельно | **L0-B2** semantic | `OPEN-06-02`…`12` (`OPEN-06-01` закрыт) |
| `s08.md` | 2026-08-21 | `L0_B3_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-08-ADDENDUM-2026-08-21` | 6/0/1 (`L0-033`…`038`); closure `L0-B3-CLOSURE-001` отдельно | **L0-B3** semantic | `OPEN-06-03`…`04`, `06`…`12`, `OPEN-08-01`, `OPEN-08-02` (`OPEN-06-02`, `OPEN-06-05` закрыты) |
| `s09.md` | 2026-08-22 | `LEVEL_0_CONSTITUTIONAL_ARCHITECTURE_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-09-ADDENDUM-2026-08-22` | 5/0/1 (`L0-039`…`043`); closures B4 / CONTRADICTION-AUDIT / L0-CLOSURE отдельно | **L0-B4**; **Level 0** FORMALLY CLOSED | `OPEN-06-03`…`04`, `07`…`12`, `OPEN-08-01` (partial), `OPEN-08-02`, `OPEN-09-01` (`OPEN-06-06` закрыт). next L1-B1 `NEXT / PARTIALLY CLOSED` |
| `s10.md` | 2026-08-22 | `L1_B1_RUNTIME_READ_BUNDLE_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-10-ADDENDUM-2026-08-22` | 4/0/1 (`L1-001`…`004`); closure `L1-B1-CLOSURE-001` отдельно | **L1-B1** semantic | `OPEN-10-01`…`06` (`OPEN-05-13`, `OPEN-06-07` закрыты) |
| `s11.md` | 2026-08-22 | `L1_B2_HYPOTHESIS_MODEL_AND_DURABLE_WAITING_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-11-ADDENDUM-2026-08-22` | 7/0/1 (`L1-005`…`011`); closure `L1-B2-CLOSURE-001` отдельно | **L1-B2** semantic | `OPEN-10-06`, `OPEN-11-01`…`08` |
| `s12.md` | 2026-08-22 | `L1_B3_UPTAKE_ACTUAL_USE_DECISION_OUTCOME_LINEAGE_SEMANTIC_CLOSURE` | `AICM-TRADING-FOUNDATION-SESSION-12-ADDENDUM-2026-08-22` | 9/0/1 (`L1-012`…`019`, `DOC-005`); closure `L1-B3-CLOSURE-001` отдельно | **L1-B3** semantic (**не** L1-B2 — L1-B2 inherited) | `OPEN-11-04`, `OPEN-12-01`…`08` (`OPEN-10-06`, `OPEN-11-08` закрыты; `OPEN-11-07` core `NO_ACTION`) |

Unique NEW numbered PREF IDs s06–s12: **49** (`L0-020`…`043` = 24; `L1-001`…`019` = 19; `DOC-001`…`005` = 5; `ROADMAP-L0-APPROVAL-001` = 1). gist = 0.
