---
name: handoff
description: Create a compact, redacted handoff document for a fresh Codex agent to continue the current task. Use when the user asks for a handoff, session summary for another agent, context compaction, or continuation notes, especially when an argument describes the next session's focus.
---

# Handoff

Write a standalone Markdown handoff in the OS temporary directory, never the workspace. Capture only what a fresh agent needs to continue.

## Workflow

1. Identify the objective, status, decisions, constraints, blockers, and next actions.
2. Treat any user argument as the next session's focus.
3. Reference existing specs, plans, ADRs, issues, commits, diffs, and other artifacts by absolute path or URL; do not duplicate them.
4. Redact keys, passwords, tokens, authentication material, secret-bearing URLs, and unnecessary personal information as `[REDACTED]`.
5. Write to `TEMP`/`TMP` on Windows or `TMPDIR` on Unix-like systems, using a name such as `codex-handoff-YYYYMMDD-HHmmss.md`. Include only relevant suggested skills, verify the file, and report its absolute path.

## Required document structure

Use this structure; omit empty sections:

```markdown
# Handoff

## Next-session focus
...

## Objective and current status
...

## Key context and decisions
...

## Artifacts and references
- `/absolute/path/to/artifact` — why it matters

## Blockers, risks, and open questions
...

## Next actions
1. ...

## Suggested skills
- `skill-name` — reason to invoke it

## Handoff notes
...
```
