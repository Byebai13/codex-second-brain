# Usage Prompts

Copy and adapt these prompts when the user wants a ready-to-use setup or daily
workflow.

## Initial Setup

```text
Use $codex-second-brain-memory to build a file-based second brain for this project.

First inspect the existing structure. Reuse any existing AGENTS.md, README.md,
skills/, project-knowledge/, codex-brain/, or similar memory files. Do not create
a parallel system if one already exists.

If no suitable memory area exists, create or complete codex-brain/ and separate
project rules, user preferences, confirmed decisions, reusable workflows, source
notes, candidate memories, and conflicts into the right files.

Keep the entry index short. Do not save full chat logs, secrets, cookies, tokens,
or unconfirmed guesses as durable memory.

When finished, tell me what files you created or modified and what needs my
confirmation.
```

## Chinese Initial Setup

```text
请使用 codex-second-brain-memory，在当前项目里为我构建一套文件化第二大脑。

先检查现有项目结构，复用已有的 AGENTS.md、README.md、skills/、project-knowledge/、codex-brain/ 或类似记忆文件，不要重复创建一套平行系统。

如果没有合适的记忆区，请创建或补齐 codex-brain/，并把项目规则、用户偏好、已确认决策、可复用工作流、资料卡片、候选记忆和冲突更新分别放到正确文件里。

入口索引要短。不要保存完整聊天记录、密码、密钥、cookie、token，也不要把未确认的模型推断直接写成长期记忆。

完成后告诉我新增或修改了哪些文件，以及哪些候选记忆需要我确认。
```

## Start Work

```text
Before starting this task, use the second-brain entry index to read only the context needed for this task.
```

## End Work

```text
Please do a second-brain closing sweep: decide whether anything from this task should become a candidate memory, preference, decision, workflow, source note, or conflict update, then update the relevant files and report the changes.
```

## Source Reading

```text
Use $codex-second-brain-memory to read and internalize this source. Create a source card if the content is readable. Separate what the source says, Codex's structured understanding, project use, candidate memories, and points that should not be internalized.
```
