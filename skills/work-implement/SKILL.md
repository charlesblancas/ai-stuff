---
name: work-implement
description: Execute an approved work plan while controlling scope and preserving an auditable record. Use only after work-specify and work-plan are approved.
---

# Work: Implement

Execute the approved plan, one deliberate step at a time. Use the local `work.md` record and never stage, commit, or push it.

## Before changing files

Confirm the approved spec and plan still match the workspace. Check the relevant baseline and preserve unrelated user changes. If the task, constraints, or repository state materially changed, return to the appropriate earlier gate.

## Execute

For each plan step:

1. Make the smallest change that satisfies the step.
2. Follow established project patterns and keep unrelated cleanup out of scope.
3. Run the step's relevant check when practical.
4. Record changed files, results, and any deviation in `work.md`.

Stop and ask before making an unapproved product decision, changing the plan materially, or accepting a failing check. Do not claim completion from inspection alone.

## Exit

When the planned changes are complete, update `work.md` with the implementation status, deviations, and remaining verification. Hand off to `work-verify` with the approved acceptance criteria and the checks already run.
