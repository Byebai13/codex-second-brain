# Codex Second Brain

Codex Second Brain is a Codex skill package for turning a project into a
file-based second brain. It gives Codex a durable memory system it can inspect,
update, and reuse across sessions without relying on one ever-growing prompt.

The skill separates memory into layers: project rules, user preferences,
confirmed decisions, reusable workflows, source notes, candidate memories, and
conflict updates. It also defines how conversations, articles, notes, and book
excerpts can be promoted gradually into durable project knowledge.

This repository is arranged for public sharing:

```text
skill/
  SKILL.md
  agents/openai.yaml
  references/
docs/
  xhs-introduction.md
```

Use `skill/` as the actual Codex skill directory. The skill invocation name is
`codex-second-brain-memory`. The root README is for GitHub. The
`docs/xhs-introduction.md` file is a social-post draft, not the canonical GitHub
introduction.

## What It Does

- Builds or reuses a project memory directory such as `codex-brain/`.
- Keeps the entry index short so Codex knows what to read first.
- Separates project rules, user preferences, confirmed decisions, reusable workflows, source notes, candidate memories, and conflicts.
- Promotes useful conversation material gradually: conversation -> candidate memory -> stable preference or viewpoint -> decision -> workflow.
- Turns articles, links, notes, and book excerpts into reusable reading cards instead of one-off summaries.
- Protects private data by refusing to store secrets, cookies, tokens, full chat logs, or unconfirmed model guesses as durable facts.

## Why This Exists

Long-running Codex projects usually accumulate context that should not live in a
single prompt: rules, preferences, decisions, reading notes, successful
workflows, and unresolved conflicts. If all of that context stays in chat,
future sessions either forget it or require the user to repeat it manually.

This skill makes that context explicit and reviewable. It gives every memory
state a place, and it requires uncertain information to pass through candidate
memory before becoming a durable preference, rule, decision, or workflow.

## Quick Start

After installing the skill, run this in the target project:

```text
Use $codex-second-brain-memory to build a file-based second brain for this project. First inspect the existing structure, reuse any existing project rules or memory files, avoid overwriting files, and then tell me what you created or changed and what still needs my confirmation.
```

For Chinese users:

```text
请使用 codex-second-brain-memory，在当前项目里为我构建一套文件化第二大脑。先检查现有项目结构，不要覆盖已有文件；把项目规则、用户偏好、已确认决策、可复用工作流、资料卡片、候选记忆和冲突更新分别放到正确文件里。完成后告诉我新增或修改了哪些文件，以及哪些候选记忆需要我确认。
```

## Installation Shape

If your skill installer supports a repository subdirectory, point it at:

```text
skill/
```

If your installer expects the skill at repository root, copy the contents of
`skill/` into the target skill folder.

## Repository Contents

- `skill/SKILL.md`: short trigger and workflow contract for Codex.
- `skill/agents/openai.yaml`: UI metadata for the skill.
- `skill/references/memory-layers.md`: file responsibilities and default memory layout.
- `skill/references/memory-promotion.md`: conversation-to-memory promotion rules.
- `skill/references/reading-workflow.md`: article, note, and book internalization workflow.
- `skill/references/safety-boundaries.md`: privacy and confirmation boundaries.
- `skill/references/usage-prompts.md`: copyable setup and daily-use prompts.
- `docs/xhs-introduction.md`: Chinese social-post draft for RedSkill/Xiaohongshu publishing.

## License

MIT. See [LICENSE](LICENSE).
