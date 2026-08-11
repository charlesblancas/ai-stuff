---
name: concise-skill-writer
description: Write or revise Codex skills to be short, clear, readable, and auditable by humans. Use when creating a new skill, tightening an existing SKILL.md, removing filler, or improving a skill's instructions without adding unnecessary process or documentation.
---

# Concise Skill Writer

Write the shortest skill that reliably guides its task.

## Rules

- Make the frontmatter description specific about purpose and triggers.
- Use imperative verbs: “Read,” “Check,” “Write,” “Verify.”
- Keep instructions that change behavior or prevent mistakes. Remove everything else.
- Remove greetings, motivation, generic advice, repetition, and commentary about the skill.
- Prefer one clear workflow. Use bullets for rules and numbered steps for sequence.
- Name tools, paths, formats, and validation commands only when necessary.
- Move genuinely needed long variants, schemas, or examples to references.
- Do not add README files, installation guides, changelogs, or other filler.
- Preserve user requirements and safety constraints.

## Writing workflow

1. State purpose and triggers in frontmatter.
2. Define the minimum reliable workflow.
3. Add only non-obvious rules, decisions, and validation.
4. Delete any sentence that does not guide an action or decision.
5. Check that a human can quickly locate and audit each section.
6. Validate the skill structure.

## Quality test

The skill must answer: “When do I use it?”, “What do I do?”, and “How do I know it worked?” If a sentence can be removed without reducing correctness, safety, or usability, remove it.
