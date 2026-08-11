---
name: work-understand
description: Build shared understanding of a task through evidence and dependency-aware rounds of questions. Use when the outcome, scope, constraints, decisions, or acceptance criteria are materially unclear.
---

# Work: Understand

Reach shared understanding before specifying or acting. Keep the evolving record in local `work.md`; never stage, commit, or push it.

## Prepare

Read the request and inspect the workspace, tools, documents, and relevant history. Find discoverable facts yourself; do not ask the user for information the environment can provide.

List the decisions needed for a sound outcome: goal, users, scope, behavior, constraints, tradeoffs, acceptance criteria, risks, and ownership. Note which decisions depend on others.

## Ask in rounds

Ask all questions that can be answered now in one short numbered round. Do not ask questions whose answer depends on another still-open decision; ask those in the next round after their prerequisite is settled.

Keep questions natural and direct. Give a recommendation when evidence supports one or when a tradeoff needs framing; explain the consequence when the choice affects scope, cost, risk, or implementation. Wait for the user's answers before the next round.

## Continue and exit

After each answer, update the decision list, settle assumptions, and derive the next independent questions. Record questions, answers, facts, decisions, assumptions, and unresolved items in `work.md`. Add `work.md` to `.git/info/exclude` when applicable.

Finish only when no material decision is silently assumed. Summarize the shared understanding, accepted assumptions, and acceptance criteria. Do not proceed to `work-specify` until the user confirms that summary.
