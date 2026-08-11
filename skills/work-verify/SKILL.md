---
name: work-verify
description: Produce evidence that implemented work meets its approved specification. Use after work-implement, before reporting completion or handing work off.
---

# Work: Verify

Verify outcomes against the approved spec, not intent alone. Use the local `work.md` record and never stage, commit, or push it.

## Build the checks

Map every acceptance criterion to evidence: automated tests, builds, linting, type checks, manual flows, visual inspection, migration checks, or performance and security checks. Reuse the repository's standard commands when available.

## Run and assess

Run the relevant checks. Record the command or method, result, and any limitation. Investigate failures before declaring success; fix and rerun when implementation is in scope. If a criterion cannot be verified, say why and record the risk.

## Exit

Update `work.md` with a concise verification table or list: criterion, evidence, status, and remaining risks. Report only verified outcomes, outstanding failures, and follow-up work. Return to `work-implement`, `work-plan`, or `work-specify` if the evidence exposes a defect, plan gap, or requirement gap.
