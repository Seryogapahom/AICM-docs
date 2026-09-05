# Knowledge Candidate — Trevs Agents / trevortaylor29 (provenance)

**Status:** не канон, не live, не identity AICM. Клон целиком не делался. Git лаборатории не писался.

## Идентификация

- User: https://github.com/trevortaylor29 (14 public repos)
- Brand site (landing, not verified purchases): https://trevsagents.com/
- Key repos:
  - https://github.com/trevortaylor29/Fundamental — Streamlit fund/ETF score; SHA root listing ref `2a0d61941a17a7f02842d7a96d58c874fa94dd8a`; score.py sha `dd200fe95c6cd7e0053004197eff652ccb447b38`
  - https://github.com/trevortaylor29/whataptisthis — Apartment Decoder MVP; ref `2081babac3275a5d54a8b4b045cb6802b09a7635`
  - https://github.com/trevortaylor29/trevasgents — Next.js landing
  - https://github.com/trevortaylor29/bofbot — TypeScript product surface
  - homework/old: IntroToVS, readandwritefiles, OOP, quiz1, Inheritance, lambdalist, djangoPROJECT, mydictionaries, ch10HOMEWORK, webscraping

## LICENSE status (URL + 1 line)

- Fundamental LICENSE https://github.com/trevortaylor29/Fundamental/blob/2a0d61941a17a7f02842d7a96d58c874fa94dd8a/LICENSE — **size=1**, empty/blank; GitHub SPDX effectively NOASSERTION. Not a usable grant.
- whataptisthis — **нет LICENSE**; package.json `"private": true`, no license field.
- trevasgents — **нет LICENSE** (404 Contents API).
- bofbot — **нет LICENSE** (404).
- Правило: публичный репо ≠ разрешённое копирование кода; только идеи/паттерны до явного grant.

## Fundamental score pitfalls (подтверждено в fundintel/score.py)

URL: https://github.com/trevortaylor29/Fundamental/blob/2a0d61941a17a7f02842d7a96d58c874fa94dd8a/fundintel/score.py

1. `_logistic01`: при nan или width<=0 возвращает **0.5** — неизвестность выглядит как середина шкалы.
2. `_downside_vol(window=63)`: параметр `window` **не используется** — downside std по всей истории отрицательных returns.
3. Broad-market anchor bonus: SPY/VOO/IVV/SPLG/VTI/^GSPC (+ name terms) получают +0.10/+0.05/+0.02 к total01 до clip — авторский bias.
4. Pillar weights и spread-expand зависят от risk/horizon — авторские; score 0–100 формула, **не** вероятность сделки.
5. Consistency win_rate по excess vs ^GSPC/SPY + upside kickers в high risk.

## whataptisthis pipeline

URL README: https://github.com/trevortaylor29/whataptisthis/blob/2081babac3275a5d54a8b4b045cb6802b09a7635/README.md

Spec: apartment-decoder-mvp-spec.md

Pipeline: clues (vision OpenRouter) → Serper web search → reasoning rank candidates → confidence + limiting_factors; POST /api/analyze; mock mode MOCK_OPENROUTER=1. Для AICM: схема research pipeline (evidence+confidence+limits), не продукт недвижимости.

## ACE / BOLT / SAGE в public

- Имена 14 public repos: **нет** ACE, BOLT, SAGE.
- code search `ACE`, `BOLT OR SAGE OR sportsbook OR paper trading` user:trevortaylor29 → **total_count 0** (API incomplete_results=true, items empty).
- Вывод: публичной реализации торговой арены / этих агентов **не подтверждено**; могут быть private/не опубликованы. Не брать маркетинг как evidence.

## Связь со штабом

Sibling extract уже в AICM-docs: from-grok/2026-09-05-trevsagents-extract.md commit ce25581 (TA-01…). Этот файл — короткий provenance для razvedka/novinki; архивирует штаб.

## Метод

GitHub MCP search_users/search_repositories/search_code/get_file_contents only. Full clone нет.


---

## Штамп штаба (2026-09-05)

Архив пакета Разведчика (`intel/` → `razvedka/novinki/`). Предложения копирования: [`from-grok/2026-09-05-trevsagents-extract.md`](../../from-grok/2026-09-05-trevsagents-extract.md) (TA-01…, `ce25581`). Не identity AICM. Исходники без LICENSE не переносить.
