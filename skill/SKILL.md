---
name: codex-second-brain-memory
description: Build and maintain a file-based second brain for a Codex project by organizing project rules, user preferences, decisions, workflows, source notes, candidate memories, and conflicts into separate Markdown files with a short entry index.
metadata:
  short-description: Build a project memory system for Codex
---

# Codex Second Brain

Use this skill when the user wants to turn a Codex project into a durable,
file-based second brain instead of repeating long prompts across sessions.

## Core Contract

Do not create a parallel memory system before checking the project. First inspect
the current project for existing guidance and memory structures such as:

- `AGENTS.md`
- `README.md`
- `skills/`
- `project-knowledge/`
- `codex-brain/`
- any other project rule, memory, or knowledge directory

Reuse existing structures when they already serve the same purpose. Create or
complete `codex-brain/` only when the project has no suitable memory area.

## Read Order

Load only the references needed for the task:

- `references/memory-layers.md`: read when creating or auditing the memory file structure.
- `references/memory-promotion.md`: read when turning conversation material into durable memory, preferences, decisions, or workflows.
- `references/reading-workflow.md`: read when the user asks to read, study, digest, or internalize an article, link, note, transcript, or book excerpt.
- `references/safety-boundaries.md`: read before writing memories that may include private, sensitive, unconfirmed, or externally sourced information.
- `references/usage-prompts.md`: read when the user wants copyable setup, daily-use, or publishing prompts.

## Default Memory Directory

If a project needs a new memory area, use:

```text
codex-brain/
  INDEX.md
  00-current-context.md
  01-project-rules.md
  02-user-preferences.md
  03-decisions.md
  04-workflows.md
  05-sources-and-notes.md
  06-memory-candidates.md
  07-conflicts-and-updates.md
  sources/
  sources/books/
```

Keep `INDEX.md` short. It is an entry index, not the memory body.

## Workflow

1. Inspect the project structure and existing guidance.
2. Decide whether to reuse existing memory files or create `codex-brain/`.
3. Classify information into the right layer instead of dumping it into one file.
4. Write confirmed information to the correct durable file.
5. Put uncertain information in `06-memory-candidates.md`.
6. Put new-vs-old disagreements in `07-conflicts-and-updates.md`.
7. Update `INDEX.md` with reading order and the current top context.
8. Report created files, modified files, confirmed memories, candidates, and open questions.

## Output Contract

At the end of a memory-building or memory-updating task, report:

- files created
- files modified
- confirmed memories written
- candidate memories awaiting user confirmation
- conflicts or questions that need resolution

Do not claim durable memory was created unless files were actually written.
