---
title: "anthropics/skills: Public repository for Agent Skills"
source: "https://github.com/anthropics/skills"
author:
published:
created: 2026-04-09
description: "Public repository for Agent Skills. Contribute to anthropics/skills development by creating an account on GitHub."
tags:
  - "clippings"
---
> **Note:** This repository contains Anthropic's implementation of skills for Claude. For information about the Agent Skills standard, see [agentskills.io](http://agentskills.io/).  
> **注：** 此仓库包含 Anthropic 为 Claude 实现的技能。有关 Agent Skills 标准的信息，请访问 [agentskills.io](http://agentskills.io/) 。

## Skills 技能

Skills are folders of instructions, scripts, and resources that Claude loads dynamically to improve performance on specialized tasks. Skills teach Claude how to complete specific tasks in a repeatable way, whether that's creating documents with your company's brand guidelines, analyzing data using your organization's specific workflows, or automating personal tasks.  
技能文件夹包含指令、脚本和资源，Claude 会动态加载这些文件夹来提升特定任务的执行效率。技能教会 Claude 如何以可重复的方式完成特定任务，例如按照公司品牌指南创建文档、使用组织特定的工作流程分析数据，或自动化个人任务。

For more information, check out:  
更多信息，请查看：

- [What are skills?什么是技能？](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude  
	克劳德运用技能](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [How to create custom skills  
	如何创建自定义技能](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Equipping agents for the real world with Agent Skills  
	为特工配备现实世界所需的技能](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

## About This Repository 关于本仓库

This repository contains skills that demonstrate what's possible with Claude's skills system. These skills range from creative applications (art, music, design) to technical tasks (testing web apps, MCP server generation) to enterprise workflows (communications, branding, etc.).  
该仓库包含的技能展示了克劳德的技能系统所能实现的功能。这些技能涵盖了从创意应用（艺术、音乐、设计）到技术任务（测试 Web 应用程序、MCP 服务器生成）再到企业工作流程（沟通、品牌推广等）的各个方面。

Each skill is self-contained in its own folder with a `SKILL.md` file containing the instructions and metadata that Claude uses. Browse through these skills to get inspiration for your own skills or to understand different patterns and approaches.  
每项技能都独立存在于各自的文件夹中，每个文件夹内都包含一个 `SKILL.md` 文件，其中包含 Claude 使用的指令和元数据。浏览这些技能，可以从中汲取灵感，开发自己的技能，或者了解不同的模式和方法。

Many skills in this repo are open source (Apache 2.0). We've also included the document creation & editing skills that power [Claude's document capabilities](https://www.anthropic.com/news/create-files) under the hood in the [`skills/docx`](https://github.com/anthropics/skills/blob/main/skills/docx), [`skills/pdf`](https://github.com/anthropics/skills/blob/main/skills/pdf), [`skills/pptx`](https://github.com/anthropics/skills/blob/main/skills/pptx), and [`skills/xlsx`](https://github.com/anthropics/skills/blob/main/skills/xlsx) subfolders. These are source-available, not open source, but we wanted to share these with developers as a reference for more complex skills that are actively used in a production AI application.  
本仓库中的许多技能都是开源的（Apache 2.0）。此外，我们还在 [`skills/docx`](https://github.com/anthropics/skills/blob/main/skills/docx) 、 [`skills/pdf`](https://github.com/anthropics/skills/blob/main/skills/pdf) 、 [`skills/pptx`](https://github.com/anthropics/skills/blob/main/skills/pptx) 和 [`skills/xlsx`](https://github.com/anthropics/skills/blob/main/skills/xlsx) 子文件夹中包含了 [Claude 底层文档](https://www.anthropic.com/news/create-files) 创建和编辑功能所需的技能。这些技能虽然不是开源的，但其源代码是公开的。我们希望与开发者分享这些技能，作为他们在实际 AI 应用中使用的更复杂技能的参考。

## Disclaimer 免责声明

**These skills are provided for demonstration and educational purposes only.** While some of these capabilities may be available in Claude, the implementations and behaviors you receive from Claude may differ from what is shown in these skills. These skills are meant to illustrate patterns and possibilities. Always test skills thoroughly in your own environment before relying on them for critical tasks.  
**这些技能仅用于演示和教学目的。** 虽然 Claude 可能具备其中一些功能，但您在 Claude 中实际体验到的功能和行为可能与这些技能演示有所不同。这些技能旨在展示一些模式和可能性。在将这些技能用于关键任务之前，请务必在您自己的环境中进行充分测试。

## Skill Sets 技能组合

- [./skills](https://github.com/anthropics/skills/blob/main/skills): Skill examples for Creative & Design, Development & Technical, Enterprise & Communication, and Document Skills  
	[./skills](https://github.com/anthropics/skills/blob/main/skills) ：创意与设计、开发与技术、企业与沟通以及文档技能的示例
- [./spec](https://github.com/anthropics/skills/blob/main/spec): The Agent Skills specification  
	[./spec](https://github.com/anthropics/skills/blob/main/spec) ：特工技能规范
- [./template](https://github.com/anthropics/skills/blob/main/template): Skill template  
	[./template](https://github.com/anthropics/skills/blob/main/template) ：技能模板

## Try in Claude Code, Claude.ai, and the API请在 Claude Code、Claude.ai 和 API 中尝试

## Claude Code 克劳德·科德

You can register this repository as a Claude Code Plugin marketplace by running the following command in Claude Code:  
您可以通过在 Claude Code 中运行以下命令，将此存储库注册为 Claude Code 插件市场：

```
/plugin marketplace add anthropics/skills
```

Then, to install a specific set of skills:  
然后，要培养一套特定的技能：

1. Select `Browse and install plugins`  
	选择 `Browse and install plugins`
2. Select `anthropic-agent-skills`  
	选择 `anthropic-agent-skills`
3. Select `document-skills` or `example-skills`  
	选择 `document-skills` 或 `example-skills`
4. Select `Install now`  
	选择 `Install now`

Alternatively, directly install either Plugin via:  
或者，您也可以直接通过以下方式安装插件：

```
/plugin install document-skills@anthropic-agent-skills
/plugin install example-skills@anthropic-agent-skills
```

After installing the plugin, you can use the skill by just mentioning it. For instance, if you install the `document-skills` plugin from the marketplace, you can ask Claude Code to do something like: "Use the PDF skill to extract the form fields from `path/to/some-file.pdf` "  
安装插件后，您只需提及该技能即可使用。例如，如果您从应用商店安装了 `document-skills` 插件，您可以让 Claude Code 执行类似这样的操作：“使用 PDF 技能从 `path/to/some-file.pdf` 中提取表单字段”。

## Claude.ai

These example skills are all already available to paid plans in Claude.ai.  
这些示例技能在 Claude.ai 的付费计划中均已可用。

To use any skill from this repository or upload custom skills, follow the instructions in [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b).  
要使用此存储库中的任何技能或上传自定义技能，请按照 [Claude 中的“使用技能”](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b) 说明进行操作。

## Claude API 克劳德 API

You can use Anthropic's pre-built skills, and upload custom skills, via the Claude API. See the [Skills API Quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill) for more.  
您可以通过 Claude API 使用 Anthropic 的预置技能，并上传自定义技能。更多信息请参阅 [技能 API 快速入门指南](https://docs.claude.com/en/api/skills-guide#creating-a-skill) 。

## Creating a Basic Skill 培养基本技能

Skills are simple to create - just a folder with a `SKILL.md` file containing YAML frontmatter and instructions. You can use the **template-skill** in this repository as a starting point:  
创建技能很简单——只需创建一个文件夹，其中包含一个 `SKILL.md` 文件，该文件包含 YAML 前置元数据和说明。您可以使用此存储库中的 **模板技能** 作为起点：

```
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that Claude will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

The frontmatter requires only two fields:  
前置元数据只需要两个字段：

- `name` - A unique identifier for your skill (lowercase, hyphens for spaces)  
	`name` - 您的技能的唯一标识符（小写，空格用连字符表示）
- `description` - A complete description of what the skill does and when to use it  
	`description` ——对该技能的功能及其使用时机的完整描述。

The markdown content below contains the instructions, examples, and guidelines that Claude will follow. For more details, see [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills).  
以下 Markdown 内容包含 Claude 将遵循的说明、示例和指南。更多详情，请参阅 [“如何创建自定义技能”](https://support.claude.com/en/articles/12512198-creating-custom-skills) 。

## Partner Skills 合作伙伴技能

Skills are a great way to teach Claude how to get better at using specific pieces of software. As we see awesome example skills from partners, we may highlight some of them here:  
技能培训是帮助克劳德更好地使用特定软件的绝佳途径。我们看到合作伙伴们展现了非常棒的技能，因此我们在此重点介绍其中一些：

- **Notion** - [Notion Skills for Claude](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0)  
	**Notion** - [Claude 的 Notion 技能](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0)