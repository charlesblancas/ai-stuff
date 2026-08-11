---
name: handoff
description: Create a compact, redacted handoff document for a fresh Codex agent to continue the current task. Use when the user asks for a handoff, session summary for another agent, context compaction, or continuation notes, especially when an argument describes the next session's focus.
---

# Handoff

Produce a standalone Markdown handoff file in the operating system's temporary directory, never in the current workspace. Capture only the context needed to continue the work and point to existing artifacts instead of copying their contents.

## Workflow

1. Inspect the current conversation and identify the active objective, decisions, constraints, blockers, and concrete next actions.
2. If the user supplied an argument, treat it as the focus of the next session and tailor the handoff around it.
3. If needed, inspect referenced artifacts. Do not duplicate content already recorded in specs, plans, ADRs, issues, commits, diffs, or other artifacts; cite each by absolute path or URL.
4. Redact API keys, passwords, tokens, authentication material, private URLs containing secrets, and unnecessary personally identifying information. Replace redacted values with `[REDACTED]`.
5. Write the handoff as Markdown to the OS temporary directory obtained from the relevant environment variable (`TEMP`/`TMP` on Windows, `TMPDIR` on Unix-like systems). Use a descriptive filename such as `codex-handoff-YYYYMMDD-HHmmss.md`.
6. Include a `Suggested skills` section listing skills the next agent should invoke, with a brief reason for each. Include only skills relevant to the stated next-session focus.
7. Verify the file exists and report its absolute path.

## Required document structure

Use this compact structure, omitting empty sections:

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
