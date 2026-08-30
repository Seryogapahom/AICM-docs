# Карта предпочтений (переработка сессий)

Статус: единая карта собрана. Не Foundation. Не runtime. Не канон Гермеса.
Дата: 2026-08-30
Источник: архивы сессий Владельца (zip в git не кладём)
Provenance: sha256 zip + package_id в карточках `sessions/`

Зачем: одна читаемая карта предпочтений из 18 сессий — почва для лаборатории и сверка для Кодекса. Разжёвываем ясность, не добавляем ограничений и не ставим человека в контур. Владелец — External Enabler.

Это **не** канон Гермеса и не Cloud canon v2. Источник закона: session cards `sessions/vision.md` + `sessions/s01.md`…`s18.md`. `DISCUSSION_DRAFT` / session addenda. `canonical: false`. `contract/implementation/runtime_authority: none`.

Zip, docx и ~190 МБ сырых архивов сюда не класть.

## Четыре файла карты

| файл | роль |
|---|---|
| [`karta.md`](karta.md) | единая карта предпочтений: как читать; стек закрытий; vision/конституция; каталог PREF (один ID — одно тело); индекс closures; дыры; счётчики |
| [`open.md`](open.md) | named OPEN после s18: terminal `OPEN-19-01`…`12`; inherited realization (отдельно); closed OPEN index; **без ответов** на OPEN-19 |
| [`rejected.md`](rejected.md) | named REJECTED IDs из карточек + приложение безымянных |
| [`README.md`](README.md) | этот индекс |

Рабочий указатель карточек Канониста: [`sessions/README.md`](sessions/README.md), `sessions/vision.md`, `sessions/s01.md`…`s18.md`. `_report*.md` — ориентация, не закон, в git не кладём.

## Стек закрытий (карточки, не HQ lineage)

| session | что закрыла | next |
|---|---|---|
| s05 | L0-B1 Purpose Kernel / cold start | L0-B2 |
| s06 | L0-B2 **IN_PROGRESS_PARTIALLY_CLOSED** (не closed); 025–032 proposed | s07 |
| s07 | **L0-B2 closed** (025–032 confirmed) | L0-B3 |
| s08 | L0-B3 | L0-B4 |
| s09 | L0-B4; **Level 0 FORMALLY CLOSED** | L1-B1 |
| s10 | L1-B1 | L1-B2 |
| s11 | **L1-B2 closed** | L1-B3 |
| s12 | **L1-B3 closed (NOT L1-B2)** | L1-B4 |
| s13 | L1-B4 | L1-B5 |
| s14 | L1-B5-01; parent L1-B5 ещё in progress | L1-B5-02 |
| s15 | L1-B5-02; parent L1-B5; **Level 1 FORMALLY CLOSED** | L2-B1 |
| s16 | **L2-B1** | L2-B2 |
| s17 | **L2-B2 and L2-B3** | L2-B4 |
| s18 | **L2-B4**; **Level 2 FORMALLY_CLOSED**; **L3-B1 ACTIVE_NOT_CLOSED**; confirmed L3 PREF = 0 | Session 19 / L3-B1 |

Карточка побеждает lineage. Cloud canon v2 — только architect context, не источник новых claims.

## Счётчики (verify against cards)

- unique numbered PREF в `karta.md`: **285**
  - TF-PREF-001…034 = 34
  - AICM-ARCH-DISC-PREF-001 = 1
  - AICM-L0-PREF-001…043 = 43
  - AICM-DOC-PREF-001…005 = 5
  - AICM-ROADMAP-L0-APPROVAL-001 = 1
  - AICM-L1-PREF-001…055 = 55
  - AICM-L2-PREF-001…146 = 146
- gist numbered PREF: **0**
- confirmed L3 PREF: **0** (не назначались)
- live named OPEN: **12** terminal (`OPEN-19-01`…`12`); inherited realization still named remaining по s18: **0**
- named REJECTED: **126** (`REJECTED-05`…`REJECTED-14`; s15–s18 named = 0)

## Дыры / proposed vs confirmed

- `AICM-L0-PREF-025`…`032` proposed в s06, **CONFIRMED в s07** (acting = s07) — не дыра.
- L3-B1 working principles s18 — provisional, **не PREF**.
- Missing numbered PREF bodies в ожидаемых диапазонах: **0**.
- Extra PREF ID вне диапазонов: **0**.

## Автономия

Система автономна. Owner/Operator = External Enabler only (login, payment, file / объективно внешнее право, ресурс, legal acceptance, identity/KYC, contractual или physical act). После внешнего предиката — automatic resume, без second approval. Человека нет в контуре управления.

## Как Codex должен verify

1. Сверять `karta.md` / `open.md` / `rejected.md` **против session cards**, не против Cloud canon v2 и не против HQ lineage.
2. Unique PREF: numbered IDs в verbatim-заголовках `### ID` карточек (не mention-group) vs каталог в `karta.md`.
3. Closures не считать PREF.
4. Mentions не удваивать тело.
5. `TF-PREF-012…016` acting = s03 v0.2.
6. Не требовать L3 PREF: s18 `confirmed_l3_preference_ids = 0`.
7. Named OPEN live = только `OPEN-19-*` по s18; OPEN-12/13 last named remaining = s15, later cards dropped from named remaining without named close.
8. Не reopen L0–L2. Не invent ID. Не отвечать OPEN-19.

Индекс карточек Канониста: [`sessions/README.md`](sessions/README.md).
