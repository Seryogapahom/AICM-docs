# Knowledge Candidate — независимая разведка androoAGI/starnet

**Date access:** 2026-09-04 Europe/Zurich.  
**Source:** GitHub API androoAGI/starnet (not ChatGPT text). Full clone NOT done. Lab git NOT written.

**Repo:** https://github.com/androoAGI/starnet  
**HEAD listing ref:** `ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6`

## Версия релиза

- **v0.10.13** — latest GitHub Release published 2026-09-03; tag `v0.10.13`; assets Win/macOS on androoAGI/starnet + mirror starnet-releases. URL: https://github.com/androoAGI/starnet/releases/tag/v0.10.13
- **package.json** version `0.10.13`, license MIT. URL: https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/package.json

## LICENSE

- https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/LICENSE — MIT License, Copyright (c) 2026 Andrew Sims

## Docs DECISIONS / MISTAKES / BRAIN (есть)

- [docs/BRAIN.md](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/docs/BRAIN.md) — orientation: local-first desktop harness + pixel station; npm start → sidecar/index.js; truthful telemetry.
- [docs/DECISIONS.md](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/docs/DECISIONS.md) — locked decision log; Full Power = host computer; object=capability
- [docs/MISTAKES.md](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/docs/MISTAKES.md) — recurring failures: fake done, stale plans, untruthful telemetry, parallel-agent breakage

## Sidecar (URL + 1 строка)

- [sidecar/loop.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/loop.js) — runAgentLoop() main agentic loop
- [sidecar/autonomy-ledger.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/autonomy-ledger.js) — autonomy ledger (near recommendation-ledger.js)
- [sidecar/permissions.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/permissions.js) — permissions grants for agents/tools
- [sidecar/budget.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/budget.js) — budget spend/caps (also budgetcaps.js, spend.js)
- [sidecar/memcore.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/memcore.js) — Memory Core pure reductions/stats over memory.* event log
- [sidecar/nightshift.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/sidecar/nightshift.js) — Night Shift (nightshift-driver.js); unattended/away path
- note: sidecar/index.js composition root; loops/*.md are QA crew directives not runtime loop

## recommend.js

- [frontend/app/recommend.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/frontend/app/recommend.js) — THE RECOMMENDATION SPINE: pure, node-testable, zero DOM/fetch
- mirror [website/app/app/recommend.js](https://github.com/androoAGI/starnet/blob/ebf7c4f2a06add0a743e0aeb63cc26ddf3f973c6/website/app/app/recommend.js) same SHA `5dfed253…`

## Метод / границы

GitHub MCP only, no full clone, no AICM-docs push, not AICM identity, not Hermes, ChatGPT not source.


---

## Штамп штаба (2026-09-04)

Архив из пакета Разведчика (`intel/` → `razvedka/novinki/`). Предложения копирования / NOT-to-copy: [`from-grok/2026-09-04-starnet-extract.md`](../../from-grok/2026-09-04-starnet-extract.md) (SN-01…10, commit chain `8ac38ca`→`c2c7e4b`). Не identity AICM. Full Power не брать.
