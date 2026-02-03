---
name: large-project-coordinator
description: Orchestrate large software projects (bots, GitHub-based dev, new OpenClaw skills) with multi-agent roles, model selection, token-minimization prompts, and structured planning. Use when a project needs coordinated stages (discussion → plan → detailed implementation), role assignment across models, GitHub artifact structure, status reporting, testing, or Docker deployment.
---

# Large Project Coordinator

## Overview
Guide large dev projects with a strict workflow, minimal-token prompts, multi-model role assignment, GitHub-first artifacts, and coordinator status reports.

## Workflow (required)
1) **Intake & constraints**
   - Clarify goal, scope, success criteria, budget/time limits.
   - Confirm GitHub usage and artifact structure.

2) **Model/role selection (must do)**
   - Analyze available models and propose roles.
   - Confirm with the user before proceeding.
   - Use fallback logic if preferred models are unavailable.
   - See `references/roles.md`.

3) **Project plan**
   - Produce a high-level roadmap with deliverables and risks.
   - Keep it short; expand only on request.
   - See `references/workflow.md`.

4) **Detailed implementation plan**
   - Convert the roadmap into step-by-step instructions.
   - Assign tasks to roles with outputs/acceptance criteria.

5) **Execution coordination (if asked)**
   - Drive tasks via issues/PRs, keep artifacts in repo.
   - Enforce checklists and tests.
   - See `references/quality.md` and `references/reports.md`.

6) **Coordinator status report (always provide on request)**
   - Use the required format from `references/status.md`.

## Token minimization (mandatory)
- Start with the shortest useful response.
- Ask before expanding scope.
- Summarize context periodically.
- Use concise prompts (see `references/prompts.md`).

## Resources
- `references/roles.md` — role map, model selection, fallback logic, user confirmation rules.
- `references/workflow.md` — discussion → plan → detailed instruction sequence.
- `references/artifacts.md` — repo structure and artifact rules.
- `references/status.md` — coordinator status format.
- `references/quality.md` — tests, gates, Docker deployment checklist.
- `references/reports.md` — agent sync/report templates.
- `references/prompts.md` — minimal-token prompt templates.
