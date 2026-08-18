# Before Work Skill

[中文](#中文) | [English](#english)

## 中文

`before-work` 是一个 Codex Skill，用于在执行或改动任务前澄清目标，避免在关键要求尚不明确时直接开始操作。

### 工作流程

1. 对执行、文件修改、配置变更、安装、发布等会改变状态的任务自动触发。
2. 每轮只提出一个苏格拉底式问题，逐步澄清目标、范围、约束和验收标准。
3. 澄清期间仅允许安全的只读检查。
4. 在理解充分后复述目标与关键约束，并等待用户明确确认。
5. 获得确认后执行、验证并汇报结果；任务完成时进行简短收尾检查。

纯问答、解释、诊断和代码审查默认不触发。用户可以对当前任务明确要求跳过或终止提问。

### 安装

将本仓库克隆到 Codex 的 Skills 目录：

```powershell
git clone https://github.com/yajnignez/before-work-skill.git "$env:USERPROFILE\.codex\skills\before-work"
```

如果设置了 `CODEX_HOME`，请改为克隆到 `$env:CODEX_HOME\skills\before-work`。重新启动 Codex 任务后，Skill 会被自动发现。

### 文件

- `SKILL.md`：触发条件与完整工作流程。
- `agents/openai.yaml`：Codex 界面元数据。

## English

`before-work` is a Codex Skill that clarifies execution and modification requests before action begins, preventing work from starting while consequential requirements remain unresolved.

### Workflow

1. Trigger automatically for state-changing tasks such as execution, file edits, configuration changes, installation, and publishing.
2. Ask one Socratic question per turn to clarify the goal, scope, constraints, and acceptance criteria.
3. Allow only safe, read-only inspection during clarification.
4. Once the task is understood, restate the goal and key constraints, then wait for explicit user confirmation.
5. After confirmation, execute, verify, and report the result; perform a brief completion check when the task is finished.

Pure questions, explanations, diagnostics, and code reviews do not trigger the Skill by default. The user may explicitly skip or terminate questioning for the current task.

### Installation

Clone this repository into the Codex Skills directory:

```powershell
git clone https://github.com/yajnignez/before-work-skill.git "$env:USERPROFILE\.codex\skills\before-work"
```

If `CODEX_HOME` is set, clone it to `$env:CODEX_HOME\skills\before-work` instead. Restart the Codex task so the Skill can be discovered.

### Files

- `SKILL.md`: Trigger conditions and the complete workflow.
- `agents/openai.yaml`: Codex UI metadata.
