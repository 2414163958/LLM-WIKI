---
title: "kepano/obsidian-skills: Agent skills for Obsidian. Teach your agent to use Markdown, Bases, JSON Canvas, and use the CLI."
source: "https://github.com/kepano/obsidian-skills"
author:
published:
created: 2026-04-09
description: "Agent skills for Obsidian. Teach your agent to use Markdown, Bases, JSON Canvas, and use the CLI. - kepano/obsidian-skills"
tags:
  - "clippings"
---
Agent Skills for use with Obsidian.  
适用于 Obsidian 的特工技能。

These skills follow the [Agent Skills specification](https://agentskills.io/specification) so they can be used by any skills-compatible agent, including Claude Code and Codex CLI.  
这些技能遵循 [Agent Skills 规范](https://agentskills.io/specification) ，因此任何兼容技能的代理都可以使用它们，包括 Claude Code 和 Codex CLI。

## Installation 安装

### Marketplace 市场

```
/plugin marketplace add kepano/obsidian-skills
/plugin install obsidian@obsidian-skills
```

### npx skills npx 技能

```
npx skills add git@github.com:kepano/obsidian-skills.git
```

### Manually 手动

#### Claude Code 克劳德·科德

Add the contents of this repo to a `/.claude` folder in the root of your Obsidian vault (or whichever folder you're using with Claude Code). See more in the [official Claude Skills documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview).  
将此仓库的内容添加到 Obsidian Vault 根目录下的 `/.claude` 文件夹中（或者您使用 Claude Code 的任何文件夹）。更多信息请参阅 [Claude Skills 官方文档](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) 。

#### Codex CLI

Copy the `skills/` directory into your Codex skills path (typically `~/.codex/skills`). See the [Agent Skills specification](https://agentskills.io/specification) for the standard skill format.  
将 `skills/` 目录复制到您的 Codex 技能路径（通常为 `~/.codex/skills` ）。有关标准技能格式，请参阅 [Agent 技能规范](https://agentskills.io/specification) 。

#### OpenCode

Clone the entire repo into the OpenCode skills directory (`~/.opencode/skills/`):  
将整个代码库克隆到 OpenCode 技能目录（ `~/.opencode/skills/` ）：

```
git clone https://github.com/kepano/obsidian-skills.git ~/.opencode/skills/obsidian-skills
```

Do not copy only the inner `skills/` folder — clone the full repo so the directory structure is `~/.opencode/skills/obsidian-skills/skills/<skill-name>/SKILL.md`.  
不要只复制内部的 `skills/` 文件夹——克隆整个仓库，以便目录结构为 `~/.opencode/skills/obsidian-skills/skills/<skill-name>/SKILL.md` 。

OpenCode auto-discovers all `SKILL.md` files under `~/.opencode/skills/`. No changes to `opencode.json` or any config file are needed. Skills become available after restarting OpenCode.  
OpenCode 会自动发现 `~/.opencode/skills/` 目录下的所有 `SKILL.md` 文件。无需修改 `opencode.json` 或任何配置文件。重启 OpenCode 后，技能即可生效。

## Skills 技能

| Skill 技能 | Description 描述 |
| --- | --- |
| [obsidian-markdown](https://github.com/kepano/obsidian-skills/blob/main/skills/obsidian-markdown) | Create and edit [Obsidian Flavored Markdown](https://help.obsidian.md/obsidian-flavored-markdown) (`.md`) with wikilinks, embeds, callouts, properties, and other Obsidian-specific syntax   使用维基链接、嵌入、标注、属性和其他 Obsidian 特有的语法创建和编辑 [Obsidian 风格的 Markdown](https://help.obsidian.md/obsidian-flavored-markdown) ( `.md` ) 文件 |
| [obsidian-bases 黑曜石底座](https://github.com/kepano/obsidian-skills/blob/main/skills/obsidian-bases) | Create and edit [Obsidian Bases](https://help.obsidian.md/bases/syntax) (`.base`) with views, filters, formulas, and summaries   创建和编辑 [Obsidian 数据库](https://help.obsidian.md/bases/syntax) ( `.base` )，包括视图、筛选器、公式和摘要 |
| [json-canvas](https://github.com/kepano/obsidian-skills/blob/main/skills/json-canvas) | Create and edit [JSON Canvas](https://jsoncanvas.org/) files (`.canvas`) with nodes, edges, groups, and connections   创建和编辑包含节点、边、组和连接的 [JSON Canvas](https://jsoncanvas.org/) 文件（ `.canvas` ）。 |
| [obsidian-cli](https://github.com/kepano/obsidian-skills/blob/main/skills/obsidian-cli) | Interact with Obsidian vaults via the [Obsidian CLI](https://help.obsidian.md/cli) including plugin and theme development   通过 [Obsidian CLI](https://help.obsidian.md/cli) 与 Obsidian Vault 进行交互，包括插件和主题开发 |
| [defuddle 去污](https://github.com/kepano/obsidian-skills/blob/main/skills/defuddle) | Extract clean markdown from web pages using [Defuddle](https://github.com/kepano/defuddle-cli), removing clutter to save tokens   使用 [Defuddle](https://github.com/kepano/defuddle-cli) 从网页中提取干净的 Markdown 代码，去除冗余信息以节省令牌。 |