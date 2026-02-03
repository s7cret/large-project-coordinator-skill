# Large Project Coordinator — Documentation

## Purpose
A skill for orchestrating large software projects (bots, GitHub-based development, new OpenClaw skills) with multi‑agent role assignment, token‑minimization prompts, structured planning, and coordinator status reporting.

## When to use
- Multi‑stage projects that require clear planning and coordination
- GitHub‑centric workflows (issues/PRs as source of truth)
- Projects needing structured artifacts (plans/notes/reports)
- Work that benefits from multi‑model role separation
- Any task needing a strict flow: **discussion → plan → detailed implementation**

## Core workflow
1) Intake & constraints
2) Role/model selection (with user approval)
3) High‑level plan
4) Detailed implementation steps
5) Execution coordination (issues/PRs, artifacts)
6) Status reporting by coordinator
7) Quality gates (tests + Docker if possible)

## Flowchart
```mermaid
flowchart TD
  A[Start / Skill invoked] --> B[Intake & constraints]
  B --> C[Check available models]
  C --> D[Propose roles + fallbacks]
  D --> E{User confirms roles?}
  E -- No --> D
  E -- Yes --> F[High‑level plan]
  F --> G[Detailed implementation steps]
  G --> H[Execute / Coordinate]
  H --> I[Quality gates + tests]
  I --> J[Docker deployment (if possible)]
  J --> K[Coordinator status report]
  K --> L[End / Next phase]
```

## Coordinator status format
```
Статус: <1–3 строки>
Сделано:
- ...
Осталось:
- ...
Блокеры/риски:
- ...
Следующий шаг:
- ...

Опционально (если есть данные):
Статистика агентов:
- активных/задействованных: ...
- токены (≈): ...
```

## Example project (condensed)
**Project:** Telegram bot + OpenClaw integration
**Goal:** Add `/vault` commands + GitHub CI + Docker

**Phase 1 — Discussion**
- Inputs: features, constraints, timeline
- Output: confirmed scope + repo structure

**Phase 2 — Plan (short)**
- Implement command handlers
- Add tests + CI
- Dockerize + docs

**Phase 3 — Detailed steps**
- Add handler module + tests
- Add GitHub Actions workflow
- Create Dockerfile + compose
- Publish status report

## Example agent report
```
Done:
- Added /vault handler
In progress:
- Tests for auth flow
Blockers:
- None
Next:
- Add CI workflow
Links:
- PR #12
```

## Example coordinator status
```
Статус: Функционал /vault готов, тесты в процессе.
Сделано:
- /vault handler + базовые проверки
Осталось:
- CI, Docker, docs
Блокеры/риски:
- нет
Следующий шаг:
- добавить workflow и docker‑compose
```

## References
- `roles.md` — role map, model selection, fallback, user confirmation
- `workflow.md` — discussion → plan → detailed instructions
- `artifacts.md` — repo structure and artifact rules
- `quality.md` — tests, gates, Docker checklist
- `reports.md` — agent report templates
- `prompts.md` — minimal‑token prompts
