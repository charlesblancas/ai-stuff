# AI Stuff

Small Codex skills for repeatable work.

## Design approach

These skills are written for readability and auditability. Each one has a narrow purpose, explicit trigger, short workflow, and clear exit condition. Instructions stay only when they change an action, prevent a likely mistake, or make verification possible. Related complexity is split into separate skills instead of hidden in a large framework.

The result should be easy for a human to inspect: what triggers it, what it does, what it avoids, and how it knows it is done.

## Skills

- [`concise-skill-writer`](skills/concise-skill-writer/SKILL.md) — Writes or tightens skills so they remain short, direct, and human-auditable.
- [`handoff`](skills/handoff/SKILL.md) — Creates a compact, redacted handoff document for a fresh agent.

### Work workflow

`work` is the entry point for a gated workflow. It keeps the current state in one local `work.md` record and routes to the earliest incomplete step.

- [`work`](skills/work/SKILL.md) — Routes substantial work through the workflow.
- [`work-understand`](skills/work-understand/SKILL.md) — Builds shared understanding through evidence and rounds of independent questions.
- [`work-specify`](skills/work-specify/SKILL.md) — Turns confirmed intent into an approved, testable specification.
- [`work-plan`](skills/work-plan/SKILL.md) — Creates an approved, file-aware implementation plan.
- [`work-implement`](skills/work-implement/SKILL.md) — Executes the approved plan while controlling scope and recording deviations.
- [`work-verify`](skills/work-verify/SKILL.md) — Produces evidence that the work meets its specification.
