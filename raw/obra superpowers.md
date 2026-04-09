---
title: "obra/superpowers: An agentic skills framework & software development methodology that works."
source: "https://github.com/obra/superpowers"
author:
published:
created: 2026-04-09
description: "An agentic skills framework & software development methodology that works. - obra/superpowers"
tags:
  - "clippings"
---
## Superpowers 超级大国

Superpowers is a complete software development workflow for your coding agents, built on top of a set of composable "skills" and some initial instructions that make sure your agent uses them.  
Superpowers 是一个完整的软件开发工作流程，适用于您的编码代理，它建立在一组可组合的“技能”和一些初始指令之上，以确保您的代理使用它们。

## How it works 工作原理

It starts from the moment you fire up your coding agent. As soon as it sees that you're building something, it *doesn't* just jump into trying to write code. Instead, it steps back and asks you what you're really trying to do.  
从你启动编码代理的那一刻起，一切就开始了。它一旦发现你在构建某个东西，并 *不会* 立刻开始编写代码。相反，它会先退后一步，询问你真正想要做什么。

Once it's teased a spec out of the conversation, it shows it to you in chunks short enough to actually read and digest.  
一旦从对话中提取出某个规格，它就会将其分成足够短小的片段显示给你，以便你能够真正阅读和理解。

After you've signed off on the design, your agent puts together an implementation plan that's clear enough for an enthusiastic junior engineer with poor taste, no judgement, no project context, and an aversion to testing to follow. It emphasizes true red/green TDD, YAGNI (You Aren't Gonna Need It), and DRY.  
设计方案经您签字确认后，您的代理人会制定一份实施计划，这份计划清晰易懂，即使是对测试缺乏热情、判断力欠佳、不了解项目背景且厌恶测试的初级工程师也能轻松上手。计划强调真正的红绿测试驱动开发（TDD）、YAGNI（你不需要它）原则以及 DRY（Don't Repeat Yourself，不要重复自己）原则。

Next up, once you say "go", it launches a *subagent-driven-development* process, having agents work through each engineering task, inspecting and reviewing their work, and continuing forward. It's not uncommon for Claude to be able to work autonomously for a couple hours at a time without deviating from the plan you put together.  
接下来，一旦你发出“开始”指令，它就会启动一个 *由子代理驱动的开发* 流程，让各个代理逐一完成工程任务，检查并审查他们的工作，然后继续推进。克劳德能够自主工作几个小时而不偏离你制定的计划，这并不罕见。

There's a bunch more to it, but that's the core of the system. And because the skills trigger automatically, you don't need to do anything special. Your coding agent just has Superpowers.  
还有很多其他功能，但这只是系统的核心。而且由于技能会自动触发，你无需进行任何特殊操作。你的编程代理就拥有了超能力。

## Sponsorship 赞助

If Superpowers has helped you do stuff that makes money and you are so inclined, I'd greatly appreciate it if you'd consider [sponsoring my opensource work](https://github.com/sponsors/obra).  
如果 Superpowers 帮助你做了能赚钱的事情，并且你也愿意，我非常希望你能考虑 [赞助我的开源工作](https://github.com/sponsors/obra) 。

Thanks!谢谢！

- Jesse 杰西

## Installation 安装

**Note:** Installation differs by platform. Claude Code or Cursor have built-in plugin marketplaces. Codex and OpenCode require manual setup.  
**注意：** 不同平台的安装方式有所不同。Claude Code 或 Cursor 内置插件市场。Codex 和 OpenCode 则需要手动安装。

### Claude Code Official MarketplaceClaude Code 官方市场

Superpowers is available via the [official Claude plugin marketplace](https://claude.com/plugins/superpowers)  
Superpowers 插件可通过 [Claude 官方插件市场](https://claude.com/plugins/superpowers) 获取。

Install the plugin from Claude marketplace:  
从 Claude 应用市场安装插件：

```
/plugin install superpowers@claude-plugins-official
```

### Claude Code (via Plugin Marketplace)Claude Code（通过插件市场）

In Claude Code, register the marketplace first:  
在 Claude Code 中，首先要注册市场：

```
/plugin marketplace add obra/superpowers-marketplace
```

Then install the plugin from this marketplace:  
然后从这个应用市场安装插件：

```
/plugin install superpowers@superpowers-marketplace
```

### Cursor (via Plugin Marketplace)光标（通过插件市场）

In Cursor Agent chat, install from marketplace:  
在 Cursor Agent 聊天软件中，请从应用商店安装：

```
/add-plugin superpowers
```

or search for "superpowers" in the plugin marketplace.  
或者在插件市场搜索“超能力”。

### Codex 法典

Tell Codex:告诉法典：

```
Fetch and follow instructions from https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.codex/INSTALL.md
```

**Detailed docs:** [docs/README.codex.md](https://github.com/obra/superpowers/blob/main/docs/README.codex.md)  
**详细文档：** [docs/README.codex.md](https://github.com/obra/superpowers/blob/main/docs/README.codex.md)

### OpenCode

Tell OpenCode:告诉 OpenCode：

```
Fetch and follow instructions from https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.opencode/INSTALL.md
```

**Detailed docs:** [docs/README.opencode.md](https://github.com/obra/superpowers/blob/main/docs/README.opencode.md)  
**详细文档：** [docs/README.opencode.md](https://github.com/obra/superpowers/blob/main/docs/README.opencode.md)

### GitHub Copilot CLI

```
copilot plugin marketplace add obra/superpowers-marketplace
copilot plugin install superpowers@superpowers-marketplace
```

### Gemini CLI 双子座15

```
gemini extensions install https://github.com/obra/superpowers
```

To update:更新：

```
gemini extensions update superpowers
```

### Verify Installation 验证安装

Start a new session in your chosen platform and ask for something that should trigger a skill (for example, "help me plan this feature" or "let's debug this issue"). The agent should automatically invoke the relevant superpowers skill.  
在您选择的平台上开始一个新的会话，并提出一些能够触发技能的问题（例如，“帮我规划一下这个功能”或“我们来调试一下这个问题”）。智能体应该会自动调用相关的超能力技能。

## The Basic Workflow 基本工作流程

1. **brainstorming** - Activates before writing code. Refines rough ideas through questions, explores alternatives, presents design in sections for validation. Saves design document.  
	**头脑风暴** ——在编写代码之前启动。通过提问完善初步想法，探索各种方案，分段展示设计以供验证。保存设计文档。
2. **using-git-worktrees** - Activates after design approval. Creates isolated workspace on new branch, runs project setup, verifies clean test baseline.  
	**using-git-worktrees** - 设计方案获批后激活。在新分支上创建隔离的工作区，运行项目设置，验证测试基线是否干净。
3. **writing-plans** - Activates with approved design. Breaks work into bite-sized tasks (2-5 minutes each). Every task has exact file paths, complete code, verification steps.  
	**编写计划** - 根据已批准的设计方案启动。将工作分解成易于处理的小任务（每个任务耗时 2-5 分钟）。每个任务都包含精确的文件路径、完整的代码和验证步骤。
4. **subagent-driven-development** or **executing-plans** - Activates with plan. Dispatches fresh subagent per task with two-stage review (spec compliance, then code quality), or executes in batches with human checkpoints.  
	**子代理驱动的开发** 或 **执行计划** - 根据计划激活。为每个任务派遣新的子代理，并进行两阶段审查（先检查规范符合性，再检查代码质量），或者分批执行，并设置人工检查点。
5. **test-driven-development** - Activates during implementation. Enforces RED-GREEN-REFACTOR: write failing test, watch it fail, write minimal code, watch it pass, commit. Deletes code written before tests.  
	**测试驱动开发** ——在实现阶段激活。强制执行红绿重构流程：编写失败的测试，观察其失败，编写最小代码，观察其通过，然后提交。删除测试之前编写的代码。
6. **requesting-code-review** - Activates between tasks. Reviews against plan, reports issues by severity. Critical issues block progress.  
	**请求代码审查** - 在任务间隙激活。根据计划进行审查，并按严重程度报告问题。严重问题会阻碍进度。
7. **finishing-a-development-branch** - Activates when tasks complete. Verifies tests, presents options (merge/PR/keep/discard), cleans up worktree.  
	**完成开发分支** - 当任务完成后激活。验证测试，提供选项（合并/PR/保留/丢弃），清理工作树。

**The agent checks for relevant skills before any task.** Mandatory workflows, not suggestions.  
**代理会在执行任何任务前检查相关技能。** 工作流程为强制性流程，而非建议。

## What's Inside 里面有什么

### Skills Library 技能库

**Testing 测试**

- **test-driven-development** - RED-GREEN-REFACTOR cycle (includes testing anti-patterns reference)  
	**测试驱动开发** - 红-绿-重构循环（包括测试反模式参考）

**Debugging 调试**

- **systematic-debugging** - 4-phase root cause process (includes root-cause-tracing, defense-in-depth, condition-based-waiting techniques)  
	**系统调试** - 四阶段根本原因分析流程（包括根本原因追踪、纵深防御、基于条件的等待技术）
- **verification-before-completion** - Ensure it's actually fixed  
	**完成前验证** - 确保问题已真正解决

**Collaboration 合作**

- **brainstorming** - Socratic design refinement  
	**头脑风暴** ——苏格拉底式设计改进
- **writing-plans** - Detailed implementation plans  
	**写作计划** - 详细实施计划
- **executing-plans** - Batch execution with checkpoints  
	**执行计划** - 带检查点的批量执行
- **dispatching-parallel-agents** - Concurrent subagent workflows  
	**并行代理调度** - 并发子代理工作流
- **requesting-code-review** - Pre-review checklist  
	**请求代码审查** - 审查前检查清单
- **receiving-code-review** - Responding to feedback  
	**接收代码审查** - 回复反馈
- **using-git-worktrees** - Parallel development branches  
	**使用 Git 工作树** - 并行开发分支
- **finishing-a-development-branch** - Merge/PR decision workflow  
	**完成开发分支** - 合并/PR 决策工作流程
- **subagent-driven-development** - Fast iteration with two-stage review (spec compliance, then code quality)  
	**基于子代理的开发** ——快速迭代，两阶段审查（先审查规范符合性，再审查代码质量）

**Meta 元**

- **writing-skills** - Create new skills following best practices (includes testing methodology)  
	**写作技能** - 遵循最佳实践创建新技能（包括测试方法）
- **using-superpowers** - Introduction to the skills system  
	**运用超能力** ——技能系统简介

## Philosophy 哲学

- **Test-Driven Development** - Write tests first, always  
	**测试驱动开发** ——始终先编写测试。
- **Systematic over ad-hoc** - Process over guessing  
	**系统化优于临时性** ——流程优于猜测
- **Complexity reduction** - Simplicity as primary goal  
	**降低复杂性** ——以简洁为首要目标
- **Evidence over claims** - Verify before declaring success  
	**证据重于空谈** ——在宣布成功之前务必核实。

Read more: [Superpowers for Claude Code](https://blog.fsck.com/2025/10/09/superpowers/)  
阅读更多： [克劳德·科德的超能力](https://blog.fsck.com/2025/10/09/superpowers/)

## Contributing 贡献

Skills live directly in this repository. To contribute:  
技能直接存储在此代码库中。如需贡献：

1. Fork the repository fork 该仓库
2. Create a branch for your skill  
	为你的技能创建一个分支
3. Follow the `writing-skills` skill for creating and testing new skills  
	遵循 `writing-skills` 技巧，创造和测试新技能
4. Submit a PR 提交 PR

See `skills/writing-skills/SKILL.md` for the complete guide.  
请参阅 `skills/writing-skills/SKILL.md` 以获取完整指南。

## Updating 正在更新

Skills update automatically when you update the plugin:  
插件更新时，技能会自动更新：

```
/plugin update superpowers
```

## License 执照

MIT License - see LICENSE file for details  
MIT 许可证 - 详情请参阅 LICENSE 文件。

## Community 社区

Superpowers is built by [Jesse Vincent](https://blog.fsck.com/) and the rest of the folks at [Prime Radiant](https://primeradiant.com/).  
Superpowers 由 [Jesse Vincent](https://blog.fsck.com/) 和 [Prime Radiant](https://primeradiant.com/) 的其他成员共同打造。

- **Discord**: [Join us](https://discord.gg/35wsABTejz) for community support, questions, and sharing what you're building with Superpowers  
	**Discord** ： [加入我们，](https://discord.gg/35wsABTejz) 获取社区支持、提出问题，并分享您使用 Superpowers 构建的内容。
- **Issues**: [https://github.com/obra/superpowers/issues](https://github.com/obra/superpowers/issues)  
	**问题反馈** ： [https://github.com/obra/superpowers/issues](https://github.com/obra/superpowers/issues)
- **Release announcements**: [Sign up](https://primeradiant.com/superpowers/) to get notified about new versions  
	**发布公告** ： [注册](https://primeradiant.com/superpowers/) 即可获取新版本通知