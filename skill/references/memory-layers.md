# Memory Layers

Use separate files for separate memory states. The goal is not to store more
text; the goal is to make memory readable, correctable, and reusable.

## Default Files

### `INDEX.md`

Short entry index.

Include:

- how this memory directory is used
- file responsibilities
- task-type reading order
- the current top 3-5 context items

Do not store full rules, full notes, or long histories here.

### `00-current-context.md`

Current project context.

Use for:

- active project status
- current task focus
- unresolved next steps
- short warnings Codex should know at the start of work

Move old material out when it becomes a decision, workflow, preference, or source
card.

### `01-project-rules.md`

Project truth and operating rules.

Use for:

- what the project is
- source-of-truth files
- directory boundaries
- what must not be edited
- validation rules
- irreversible actions that require user confirmation

### `02-user-preferences.md`

Stable user preferences.

Use only for recurring behavior preferences, not one-off tastes or guesses.

### `03-decisions.md`

Confirmed decisions.

Suggested shape:

```md
## YYYY-MM-DD: Decision Title

- Decision:
- Background:
- Impact:
- Invalidates when:
```

### `04-workflows.md`

Reusable workflows.

Only promote workflows that are likely to be reused and have multiple steps.

Suggested shape:

```md
## Workflow Name

- Trigger:
- Inputs:
- Steps:
- Output:
- Validation:
- Do not:
```

### `05-sources-and-notes.md`

Index for source cards, articles, books, transcripts, and external materials.

Do not store full source text here. Link to source cards under `sources/`.

### `06-memory-candidates.md`

Candidate memory inbox.

Use when the information might matter later but is not confirmed enough for a
durable rule, preference, decision, or workflow.

Suggested table:

```md
| Date | Candidate | Type | Source | Confidence | Suggested Action |
|---|---|---|---|---|---|
```

### `07-conflicts-and-updates.md`

Conflict and update log.

Use when new information disagrees with older memory.

Suggested shape:

```md
## YYYY-MM-DD: Conflict Title

- Old statement:
- New statement:
- Conflict:
- Confirmation needed:
- Temporary handling:
```
