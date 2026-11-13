# Hand-off

[简体中文](#简体中文) | [English](#english)

## 简体中文

**Hand-off** 是一项长会话交接与收尾 Skill，帮助跨天或多阶段任务记录可核验的当前状态，并在任务完成时总结成果、工作流与经验。

### 适用场景

- 任务跨天或包含多个阶段，需要交接或续接。
- 用户要求复盘、总结，或任务完成后需要收尾。
- 需要基于当前对话和可访问材料整理进度、阻塞、决定与下一步。

普通短任务默认不触发；用户明确说会话结束、任务结束或收尾时，也会进入收尾流程。

### 使用

Codex 用 `$hand-off` 显式调用，Trae 用 `/hand-off` 显式调用，其他宿主或语法不可用时用自然语言明确点名 hand-off 技能。Skill 会根据证据判断应执行交接、完成收尾还是续接；不把计划写成已完成，也不补造缺失信息。

默认交接文件位置为当前项目的 `progress/HANDOFF.md`。明确结束指令触发时，项目 `progress/memory.md`、`wiki.md`、`learnings.md` 和进度 checkpoint 在有内容时按类别自动保存；跨项目的全局记忆、经验或工作流只在用户逐项确认后写入。

### 交接模板包含

- 整体目标与成功条件，以及最近子任务目标与成功条件
- 会话名称、交接对象、原因和依据
- 计划进度、验收证据、已完成事项、待办与阻塞
- 决策、约束、风险、待确认事项和下一步
- 文件变更与 Git 状态
- 任务完成时的成果、工作流、经验教训与记忆候选复盘

会话名称概括跨阶段的整体主线；仅在证据表明整体目标已转换时更新主题。无法判断时保留当前名称并注明未确认。

## English

**Hand-off** is a long-session handoff and wrap-up skill. It helps record verifiable project state across multi-stage work and summarize outcomes, workflow, and lessons when a task is complete.

### When to use it

- Work spans multiple days or stages and needs a handoff or continuation.
- The user asks for a retrospective or summary, or a completed task needs a wrap-up.
- Progress, blockers, decisions, and next steps need to be organized from the current conversation and accessible project materials.

Ordinary short tasks do not trigger it by default. An explicit instruction to end or wrap up the session also starts the closeout workflow.

### Usage

In Codex, invoke `$hand-off`; in Trae, invoke `/hand-off`; on other hosts or when no explicit syntax is available, ask in natural language to use the hand-off skill. Based on available evidence, the skill chooses handoff, completion wrap-up, or continuation. It does not present plans as completed work or invent missing information.

The default handoff file is `progress/HANDOFF.md` in the current project. On an explicit end instruction, project `progress/memory.md`, `wiki.md`, `learnings.md`, and a progress checkpoint are saved by category when there is relevant content. Cross-project global memory, lessons, or workflows are written only after the user approves each candidate.

### The handoff template covers

- Overall goal and success criteria, plus the latest subtask and its success criteria
- Session name, recipient, reason, and supporting evidence
- Plan progress, acceptance evidence, completed work, pending work, and blockers
- Decisions, constraints, risks, open questions, and next steps
- File changes and Git status
- Outcomes, workflow, lessons, and memory candidates for completed-task retrospectives

The session name should describe the overall thread across stages. Change the topic only when evidence shows the overall goal has changed. If the overall topic cannot be identified, keep the current name and mark it as unconfirmed.