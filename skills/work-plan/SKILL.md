---
name: work-plan
description: Create an approved implementation plan from a tested specification. Use after work-specify and before changing the product or code.
---

# Work: Plan

Translate the approved spec into an executable sequence. Use the local `work.md` record and never stage, commit, or push it.

## Inspect before planning

Read the relevant code paths, project conventions, tests, dependencies, and current baseline. Do not invent file names or patterns when the repository can answer.

## Write the plan

For each step, state:

- The purpose and dependency order.
- Exact files, components, or systems affected.
- The intended change and any migration or compatibility concern.
- The acceptance criterion it satisfies.
- The verification to run when the step is complete.

Keep steps small enough to review and adjust. Include setup, data migration, rollback, documentation, or deployment work only when the spec requires it. Call out risks, alternatives rejected, and decisions that need approval.

## Review and exit

Check that the plan covers every acceptance criterion without scope creep. Update `work.md` with the plan, affected areas, risks, and verification sequence.

Present the plan for approval. Do not implement until approved.
