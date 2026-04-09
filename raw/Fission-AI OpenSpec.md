---
title: "Fission-AI/OpenSpec: Spec-driven development (SDD) for AI coding assistants."
source: "https://github.com/Fission-AI/OpenSpec"
author:
published:
created: 2026-04-09
description: "Spec-driven development (SDD) for AI coding assistants. - Fission-AI/OpenSpec"
tags:
  - "clippings"
---
[![[raw/assets/269e4940edab1612fe45f58bb3e355f5_MD5.png]]](https://github.com/Fission-AI/OpenSpec)

**The most loved spec framework.  
最受欢迎的规范框架。** Our philosophy: 我们的理念：

```
→ fluid not rigid
→ iterative not waterfall
→ easy not complex
→ built for brownfield not just greenfield
→ scalable from personal projects to enterprises
```

> [!tip] Tip
> **New workflow now available!** We've rebuilt OpenSpec with a new artifact-guided workflow.  
> **全新工作流程现已上线！** 我们已使用全新的工件引导式工作流程重建了 OpenSpec。
> 
> Run `/opsx:propose "your idea"` to get started. → [Learn more here](https://github.com/Fission-AI/OpenSpec/blob/main/docs/opsx.md)  
> 运行 `/opsx:propose "your idea"` 即可开始。→ [点击此处了解更多信息](https://github.com/Fission-AI/OpenSpec/blob/main/docs/opsx.md)

Follow [@0xTab on X](https://x.com/0xTab) for updates · Join the [OpenSpec Discord](https://discord.gg/YctCnvvshC) for help and questions.  
关注 [@0xTab on X](https://x.com/0xTab) 获取最新消息 · 加入 [OpenSpec Discord](https://discord.gg/YctCnvvshC) 获取帮助和解答疑问。

### Teams 团队

Using OpenSpec in a team? [Email here](mailto:teams@openspec.dev) for access to our Slack channel.  
团队中正在使用 OpenSpec？ [请发送邮件至此处](mailto:teams@openspec.dev) 获取我们 Slack 频道的访问权限。

## See it in action 观看实际演示

```
You: /opsx:propose add-dark-mode
AI:  Created openspec/changes/add-dark-mode/
     ✓ proposal.md — why we're doing this, what's changing
     ✓ specs/       — requirements and scenarios
     ✓ design.md    — technical approach
     ✓ tasks.md     — implementation checklist
     Ready for implementation!

You: /opsx:apply
AI:  Implementing tasks...
     ✓ 1.1 Add theme context provider
     ✓ 1.2 Create toggle component
     ✓ 2.1 Add CSS variables
     ✓ 2.2 Wire up localStorage
     All tasks complete!

You: /opsx:archive
AI:  Archived to openspec/changes/archive/2025-01-23-add-dark-mode/
     Specs updated. Ready for the next feature.
```

**OpenSpec Dashboard OpenSpec 仪表盘**

[![[raw/assets/a34230fbcfcc1c895d284594975db7ba_MD5.png]]](https://github.com/Fission-AI/OpenSpec/blob/main/assets/openspec_dashboard.png)

## Quick Start 快速入门

**Requires Node.js 20.19.0 or higher.  
需要 Node.js 20.19.0 或更高版本。**

Install OpenSpec globally:  
全局安装 OpenSpec：

```
npm install -g @fission-ai/openspec@latest
```

Then navigate to your project directory and initialize:  
然后导航到您的项目目录并进行初始化：

```
cd your-project
openspec init
```

Now tell your AI: `/opsx:propose <what-you-want-to-build>`  
现在告诉你的 AI： `/opsx:propose <what-you-want-to-build>`

If you want the expanded workflow (`/opsx:new`, `/opsx:continue`, `/opsx:ff`, `/opsx:verify`, `/opsx:sync`, `/opsx:bulk-archive`, `/opsx:onboard`), select it with `openspec config profile` and apply with `openspec update`.  
如果您想要扩展工作流程（ `/opsx:new` 、 `/opsx:continue` 、 `/opsx:ff` 、 `/opsx:verify` 、 `/opsx:sync` 、 `/opsx:bulk-archive` 、 `/opsx:onboard` ），请使用 `openspec config profile` 选择它，并使用 `openspec update` 应用它。

> [!note] Note
> Not sure if your tool is supported? [View the full list](https://github.com/Fission-AI/OpenSpec/blob/main/docs/supported-tools.md) – we support 20+ tools and growing.  
> 不确定您的工具是否受支持？ [查看完整列表](https://github.com/Fission-AI/OpenSpec/blob/main/docs/supported-tools.md) ——我们支持 20 多种工具，并且还在不断增加。
> 
> Also works with pnpm, yarn, bun, and nix. [See installation options](https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md).  
> 也适用于 pnpm、yarn、bun 和 nix。 [请参阅安装选项](https://github.com/Fission-AI/OpenSpec/blob/main/docs/installation.md) 。

## Docs 文档

→ **[Getting Started](https://github.com/Fission-AI/OpenSpec/blob/main/docs/getting-started.md)**: first steps  
→ **[入门指南](https://github.com/Fission-AI/OpenSpec/blob/main/docs/getting-started.md)** ：第一步  
→ **[Workflows](https://github.com/Fission-AI/OpenSpec/blob/main/docs/workflows.md)**: combos and patterns  
→ **[工作流程](https://github.com/Fission-AI/OpenSpec/blob/main/docs/workflows.md)** ：组合和模式  
→ **[Commands](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)**: slash commands & skills  
→ **[命令](https://github.com/Fission-AI/OpenSpec/blob/main/docs/commands.md)** ：斜杠命令和技能  
→ **[CLI](https://github.com/Fission-AI/OpenSpec/blob/main/docs/cli.md)**: terminal reference  
→ **[CLI](https://github.com/Fission-AI/OpenSpec/blob/main/docs/cli.md)** ：终端参考  
→ **[Supported Tools](https://github.com/Fission-AI/OpenSpec/blob/main/docs/supported-tools.md)**: tool integrations & install paths  
→ **[支持的工具](https://github.com/Fission-AI/OpenSpec/blob/main/docs/supported-tools.md)** ：工具集成和安装路径  
→ **[Concepts](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)**: how it all fits  
→ **[概念](https://github.com/Fission-AI/OpenSpec/blob/main/docs/concepts.md)** ：一切如何衔接  
→ **[Multi-Language](https://github.com/Fission-AI/OpenSpec/blob/main/docs/multi-language.md)**: multi-language support  
→ **[多语言](https://github.com/Fission-AI/OpenSpec/blob/main/docs/multi-language.md)** ：多语言支持  
→ **[Customization](https://github.com/Fission-AI/OpenSpec/blob/main/docs/customization.md)**: make it yours  
→ **[个性化定制](https://github.com/Fission-AI/OpenSpec/blob/main/docs/customization.md)** ：打造专属于你

## Why OpenSpec? 为什么选择 OpenSpec？

AI coding assistants are powerful but unpredictable when requirements live only in chat history. OpenSpec adds a lightweight spec layer so you agree on what to build before any code is written.  
AI 编码助手功能强大，但如果需求仅存在于聊天记录中，则其表现难以预测。OpenSpec 添加了一个轻量级的规范层，让您在编写任何代码之前就对要构建的内容达成一致。

- **Agree before you build** — human and AI align on specs before code gets written  
	**在构建之前达成一致** ——在编写代码之前，人类和人工智能需要就规范达成一致。
- **Stay organized** — each change gets its own folder with proposal, specs, design, and tasks  
	**保持条理清晰** ——每次变更都单独建一个文件夹，里面包含提案、规格、设计和任务。
- **Work fluidly** — update any artifact anytime, no rigid phase gates  
	**工作方式灵活** ——随时更新任何工件，没有严格的阶段性限制。
- **Use your tools** — works with 20+ AI assistants via slash commands  
	**使用你的工具** ——可通过斜杠命令与 20 多个 AI 助手配合使用

### How we compare 我们如何比较

**vs. [Spec Kit](https://github.com/github/spec-kit)** (GitHub) — Thorough but heavyweight. Rigid phase gates, lots of Markdown, Python setup. OpenSpec is lighter and lets you iterate freely.  
**对比 [Spec Kit](https://github.com/github/spec-kit)** （GitHub）——功能全面但体积庞大。它有严格的阶段门控、大量的 Markdown 代码以及 Python 配置。OpenSpec 更轻量级，允许你自由迭代。

**vs. [Kiro](https://kiro.dev/)** (AWS) — Powerful but you're locked into their IDE and limited to Claude models. OpenSpec works with the tools you already use.  
**与 [Kiro](https://kiro.dev/)** （AWS）相比——功能强大，但你只能使用他们的 IDE，而且仅限于 Claude 模型。OpenSpec 可以与你已使用的工具兼容。

**vs. nothing** — AI coding without specs means vague prompts and unpredictable results. OpenSpec brings predictability without the ceremony.  
与没有规范的 **情况相比** ——没有规范的 AI 编码意味着模糊的提示和不可预测的结果。OpenSpec 无需繁琐的流程即可带来可预测性。

## Updating OpenSpec 更新 OpenSpec

**Upgrade the package 升级套餐**

```
npm install -g @fission-ai/openspec@latest
```

**Refresh agent instructions  
刷新代理指令**

Run this inside each project to regenerate AI guidance and ensure the latest slash commands are active:  
在每个项目中运行此命令，以重新生成 AI 指导并确保最新的斜杠命令处于活动状态：

```
openspec update
```

## Usage Notes 使用说明

**Model selection**: OpenSpec works best with high-reasoning models. We recommend Opus 4.5 and GPT 5.2 for both planning and implementation.  
**模型选择** ：OpenSpec 与高推理能力的模型配合使用效果最佳。我们推荐使用 Opus 4.5 和 GPT 5.2 进行规划和实施。

**Context hygiene**: OpenSpec benefits from a clean context window. Clear your context before starting implementation and maintain good context hygiene throughout your session.  
**上下文卫生** ：OpenSpec 受益于干净的上下文窗口。在开始实现之前清除上下文，并在整个会话期间保持良好的上下文卫生。

## Contributing 贡献

**Small fixes** — Bug fixes, typo corrections, and minor improvements can be submitted directly as PRs.  
**小修复** ——错误修复、拼写错误更正和小改进可以直接作为 PR 提交。

**Larger changes** — For new features, significant refactors, or architectural changes, please submit an OpenSpec change proposal first so we can align on intent and goals before implementation begins.  
**较大的变更** ——对于新功能、重大重构或架构变更，请先提交 OpenSpec 变更提案，以便我们在实施开始之前就意图和目标达成一致。

When writing proposals, keep the OpenSpec philosophy in mind: we serve a wide variety of users across different coding agents, models, and use cases. Changes should work well for everyone.  
撰写提案时，请牢记 OpenSpec 的理念：我们服务于各种不同的编码代理、模型和用例的各类用户。所有变更都应惠及所有人。

**AI-generated code is welcome** — as long as it's been tested and verified. PRs containing AI-generated code should mention the coding agent and model used (e.g., "Generated with Claude Code using claude-opus-4-5-20251101").  
**我们欢迎人工智能生成的代码** ——只要它经过测试和验证。包含人工智能生成代码的 PR 应注明所使用的编码代理和模型（例如，“使用 claude-opus-4-5-20251101 通过 Claude Code 生成”）。

### Development 发展

- Install dependencies: `pnpm install`  
	安装依赖项： `pnpm install`
- Build: `pnpm run build`  
	构建： `pnpm run build`
- Test: `pnpm test`  
	测试： `pnpm test`
- Develop CLI locally: `pnpm run dev` or `pnpm run dev:cli`  
	本地开发 CLI： `pnpm run dev` 或 `pnpm run dev:cli`
- Conventional commits (one-line): `type(scope): subject`  
	常规提交（单行）： `type(scope): subject`

## Other 其他

**Telemetry 遥测**

OpenSpec collects anonymous usage stats.

We collect only command names and version to understand usage patterns. No arguments, paths, content, or PII. Automatically disabled in CI.

**Opt-out:** `export OPENSPEC_TELEMETRY=0` or `export DO_NOT_TRACK=1`