---
name: work-specify
description: Convert a confirmed shared understanding into an approved, testable specification. Use after work-understand and before implementation planning.
---

# Work: Specify

Turn confirmed intent into a short, testable contract. Use the local `work.md` record and never stage, commit, or push it.

## Write the spec

Capture:

- Goal and intended users.
- Non-goals and scope boundaries.
- Required behavior, including important failure and edge cases.
- Interfaces or user-visible changes: APIs, screens, commands, data, and compatibility.
- Constraints and decisions already made.
- Acceptance criteria expressed as observable outcomes.

Use precise statements. Mark any remaining choice as an open question instead of silently deciding it. Do not prescribe an implementation unless it is itself a requirement.

## Review and exit

Check that every acceptance criterion can be verified and every requirement is traceable to the confirmed understanding. Update `work.md` with the spec, decisions, and open questions.

Show the spec to the user. Do not plan implementation until the user approves it or explicitly delegates the remaining decisions.
