# Before Work Skill

[中文](#中文) | [English](#english)

## 中文

`before-work` 是一个 Codex Skill，用于在执行或改动任务前识别会实质影响结果的关键歧义，同时避免为小问题频繁请示。

### 工作流程

1. 对执行、文件修改、配置变更、安装、发布等会改变状态的任务自动触发。
2. 判断未明确事项是否会导致输出、架构、范围、风险、成本或验收结果出现实质差异。
3. 只有存在实质差异时才每轮提出一个苏格拉底式问题，并在澄清期间仅进行安全的只读检查。
4. 对命名、大小写、格式、放置位置等非关键细节，默认遵循行业规范和项目既有约定，自主决策并直接执行。
5. 若进行了关键澄清，则复述目标与约束并等待确认；没有关键歧义时不做多余请示。
6. 执行、验证并汇报结果；任务完成时进行简短收尾检查。

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

`before-work` is a Codex Skill that identifies consequential ambiguity before execution or modification while avoiding unnecessary questions about minor details.

### Workflow

1. Trigger automatically for state-changing tasks such as execution, file edits, configuration changes, installation, and publishing.
2. Decide whether an unresolved matter could materially change the output, architecture, scope, risk, cost, or acceptance result.
3. Ask one Socratic question per turn only when such a material difference exists, allowing only safe, read-only inspection during clarification.
4. For minor details such as naming, capitalization, formatting, or placement, follow established standards and repository conventions, decide autonomously, and proceed.
5. If consequential clarification occurred, restate the goal and constraints and wait for confirmation; otherwise avoid redundant approval requests.
6. Execute, verify, and report the result; perform a brief completion check when the task is finished.

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
