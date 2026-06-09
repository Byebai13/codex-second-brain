# Memory Promotion

Memory should move gradually. Do not turn one conversation into a permanent rule
without checking its status.

## Promotion Chain

```text
conversation detail
  -> candidate memory
  -> stable preference or core viewpoint
  -> confirmed decision or project rule
  -> reusable workflow
```

Not every item moves through every stage. Some items should stay as source notes
or be ignored.

## Conversation To Candidate

Use `06-memory-candidates.md` when:

- the user says something that may recur
- the user expresses a preference but has not confirmed it as durable
- a repeated behavior pattern appears
- a useful project fact appears but needs verification
- an external source might influence future work

Do not promote model guesses directly.

## Candidate To Preference

Promote to `02-user-preferences.md` only when:

- the user explicitly confirms it
- the preference is stable across tasks
- it changes how Codex should answer or act later

Examples:

- preferred answer style
- default project behavior
- stable writing or research preferences
- recurring collaboration rules

## Candidate To Core Viewpoint

Promote to `08-core-viewpoints.md` when:

- the user confirms a durable belief, principle, or judgment frame
- the statement affects how future evidence should be interpreted
- it is broader than a preference but not yet a specific decision
- it shapes the assistant's role, tone, boundaries, or default reasoning

Examples:

- personal operating principles
- project philosophy
- repeated evaluation criteria
- stable role definitions for Codex
- important beliefs derived from multiple sources or conversations

Do not use `08-core-viewpoints.md` as a place for attractive but unconfirmed
ideas from books or articles.

## Preference Or Core Viewpoint To Decision

Promote to `03-decisions.md` when:

- the user chooses a path
- the choice closes an alternative
- future work should follow the choice
- the decision has a boundary or invalidation condition

Decisions need context. Include why it was decided and when it should be revisited.

## Decision To Workflow

Promote to `04-workflows.md` when:

- the same operation will repeat
- it has three or more concrete steps
- it has a clear trigger
- it has a validation signal

Do not create workflows for one-off tasks.

## End-Of-Task Memory Sweep

Before closing a substantial task, check:

- Did the user confirm a durable preference?
- Did a candidate become a stable viewpoint or principle?
- Was a decision made?
- Did a reusable workflow succeed?
- Did a source change future judgment?
- Did new information conflict with old memory?
- Is there an unresolved next step?

Then update the relevant file and report the changes.
