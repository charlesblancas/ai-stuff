---
name: work
description: Entry point for substantial work that routes tasks through work-understand, work-specify, work-plan, work-implement, and work-verify. Use when a task benefits from a gated, auditable workflow rather than immediate execution.
---

# Work

Run the lightweight workflow and route to the right gate. Keep one local `work.md` record. Never stage, commit, or push the work record or make commits on the user's behalf.

## State file

- Create or update `work.md` at the workspace root.
- Keep the current phase, decisions, open questions, confirmed understanding, spec, plan, changed files, and verification results there.
- Add `work.md` to `.git/info/exclude` when the workspace is a Git repository. Do not edit tracked ignore files for this purpose.
- Keep the file readable and current; do not create parallel planning documents.

## Routing

Choose the earliest incomplete gate. Do not skip a gate merely to start changing files sooner.

| State | Use |
| --- | --- |
| Outcome, scope, constraints, or acceptance criteria are unclear | `work-understand` |
| Understanding is confirmed but no testable contract exists | `work-specify` |
| Spec exists but no execution sequence exists | `work-plan` |
| Plan exists and work remains | `work-implement` |
| Planned work is complete and needs evidence | `work-verify` |

Each gate owns its details and exit criteria. Read and follow that gate's skill before acting. If new evidence changes the requirement, plan, or implementation, return to the earliest affected gate and update `work.md`.

## Working rules

- Do not guess through material ambiguity; use `work-understand`.
- After shared understanding is confirmed, continue through `work-specify`, `work-plan`, `work-implement`, and `work-verify` without waiting for approval.
- Do not expand scope without asking.
- Prefer evidence over claims; use `work-verify` before declaring completion.
