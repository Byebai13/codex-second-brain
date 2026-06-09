# Reading And Internalization Workflow

Use this workflow when the user asks to read, study, digest, make notes, create a
reading card, or internalize a source into the second brain.

## Trigger Phrases

Examples:

- "read this deeply"
- "make notes from this"
- "internalize this into my second brain"
- "turn this article into a source card"
- "study this book excerpt"
- "summarize this and save reusable points"

If the user only drops a link or title without asking to internalize it, ask
whether they want a quick answer or a durable source card.

## Source Card Location

For articles, links, transcripts, notes, or short excerpts:

```text
codex-brain/sources/YYYY-MM-DD-source-title.md
```

For whole books or large dossiers:

```text
codex-brain/sources/books/YYYY-MM-DD-book-title/
  INDEX.md
  00-overview.md
  chapters/
```

## Source Card Structure

Use:

```md
# Source Title

- Source:
- Type:
- Date:
- Why this was read:

## One-Sentence Takeaway

## What The Source Actually Says

## Structure Map

## Key Claims And Evidence

## Assumptions And Boundaries

## Use For This Project

## Candidate Memories

## Possible Core Viewpoints

## Do Not Internalize
```

## Internalization Rules

Separate these layers:

- what the source says
- Codex's structured understanding
- what matters for the current project
- what may become candidate memory
- what may become a core viewpoint after confirmation
- what should not be adopted

Do not turn source claims directly into user preferences, project rules, core
viewpoints, or decisions.

First write source notes. Then, if useful, add candidate memories. Promote only
after user confirmation or clear project evidence. If a source repeatedly shapes
the user's judgment, the confirmed result may move to `08-core-viewpoints.md`.
