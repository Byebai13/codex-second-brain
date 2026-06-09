# Codex Second Brain

Codex Second Brain is a Codex skill package for turning a project into a
file-based second brain. It gives Codex a durable memory system it can inspect,
update, and reuse across sessions without relying on one ever-growing prompt.

The skill separates memory into layers: project rules, user preferences, core
viewpoints, confirmed decisions, reusable workflows, source notes, candidate
memories, and conflict updates. It also defines how conversations, articles,
notes, and book excerpts can be promoted gradually into durable project
knowledge.

This repository is arranged for public sharing:

```text
SKILL.md
agents/openai.yaml
references/
```

The repository root is the actual Codex skill directory. The skill invocation
name is `codex-second-brain`.

## 中文介绍

Codex 不只是编程助手。它可以帮你写文档、整理资料、跑自动化、维护项目上下文，甚至成为一个真正懂你的个人知识管理助手。但前提是：你需要给 Codex 一套可以持续读取、持续更新的记忆系统。

Codex Second Brain 做的就是这件事。它会为你的项目建立一套文件化第二大脑，把记忆分层保存：项目规则、长期偏好、核心观点、已确认决策、可复用工作流、资料卡片、候选记忆和冲突更新，各自都有明确位置。

它不是把聊天记录粗暴塞进一个大文件，而是让 Codex 学会区分、沉淀和升级记忆。一段对话可以先进入候选记忆，经过确认后变成稳定偏好或核心观点；当这些观点反复影响行动时，再上升为决策或工作流。文章、链接和书籍摘录也不会只被总结一次，而是会被整理成资料卡片，再按需要内化进记忆系统。

最终效果是：下次 Codex 进入同一个项目时，不需要靠你重新解释一遍。它会先读入口索引，再按任务读取相关文件，知道哪些内容已经确认、哪些只是候选、哪些外部观点不能直接变成你的原则。

## What It Does

- Builds or reuses a project memory directory such as `codex-brain/`.
- Keeps the entry index short so Codex knows what to read first.
- Separates project rules, user preferences, core viewpoints, confirmed decisions, reusable workflows, source notes, candidate memories, and conflicts.
- Promotes useful conversation material gradually: conversation -> candidate memory -> stable preference or core viewpoint -> decision -> workflow.
- Turns articles, links, notes, and book excerpts into reusable reading cards instead of one-off summaries.
- Protects private data by refusing to store secrets, cookies, tokens, full chat logs, or unconfirmed model guesses as durable facts.

## Why This Exists

Long-running Codex projects usually accumulate context that should not live in a
single prompt: rules, preferences, decisions, reading notes, successful
workflows, and unresolved conflicts. If all of that context stays in chat,
future sessions either forget it or require the user to repeat it manually.

This skill makes that context explicit and reviewable. It gives every memory
state a place, and it requires uncertain information to pass through candidate
memory before becoming a durable preference, core viewpoint, rule, decision, or
workflow.

## Quick Start

After installing the skill, run this in the target project:

```text
Use $codex-second-brain to build a file-based second brain for this project. First inspect the existing structure, reuse any existing project rules or memory files, avoid overwriting files, and then tell me what you created or changed and what still needs my confirmation.
```

For Chinese users:

```text
请使用 codex-second-brain，在当前项目里为我构建一套文件化第二大脑。先检查现有项目结构，不要覆盖已有文件；把项目规则、用户偏好、核心观点、已确认决策、可复用工作流、资料卡片、候选记忆和冲突更新分别放到正确文件里。完成后告诉我新增或修改了哪些文件，以及哪些候选记忆需要我确认。
```

## Installation

Install from the repository root:

```text
https://github.com/Byebai13/codex-second-brain
```

The root contains `SKILL.md`, `agents/`, and `references/`, so installers that
expect a skill at repository root can use this repository directly.

## Repository Contents

- `SKILL.md`: short trigger and workflow contract for Codex.
- `agents/openai.yaml`: UI metadata for the skill.
- `references/memory-layers.md`: file responsibilities and default memory layout.
- `references/memory-promotion.md`: conversation-to-memory promotion rules.
- `references/core-viewpoints.md`: stable viewpoint, principle, and role-memory rules.
- `references/reading-workflow.md`: article, note, and book internalization workflow.
- `references/safety-boundaries.md`: privacy and confirmation boundaries.
- `references/usage-prompts.md`: copyable setup and daily-use prompts.

## License

MIT. See [LICENSE](LICENSE).
