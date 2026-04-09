---
title: obsidian-skills - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - [[raw/kepano obsidian-skills.md]]
tags: [Agent Skills, Obsidian, 工具]
type: source-summary
---

# obsidian-skills - 摘要

[[Steph Ango]] (kepano) 创建的 Obsidian 专用 Agent Skills 集合，遵循 [Agent Skills 规范](https://agentskills.io/specification)，支持 Claude Code、Codex CLI、OpenCode 等兼容平台。

## 包含技能

| 技能 | 功能 |
|------|------|
| **obsidian-markdown** | 创建/编辑 [[Obsidian Flavored Markdown]]（维基链接、嵌入、标注、属性等） |
| **obsidian-bases** | 创建/编辑 [[Obsidian Bases]]（视图、筛选、公式、摘要） |
| **json-canvas** | 创建/编辑 [[JSON Canvas]] 文件（节点、边、分组、连接） |
| **obsidian-cli** | 通过 [[Obsidian CLI]] 与 Vault 交互，包括插件和主题开发 |
| **defuddle** | 使用 [[Defuddle]] 从网页提取干净 Markdown，去除冗余以节省 Token |

## 安装方式

- **Marketplace**：`/plugin install obsidian@obsidian-skills`
- **npx skills**：`npx skills add git@github.com:kepano/obsidian-skills.git`
- **OpenCode**：克隆到 `~/.opencode/skills/obsidian-skills/`

## 相关链接

- [[Steph Ango]] — 作者
- [[Obsidian]]
- [[Agent Skills]]
- [[JSON Canvas]]
- [[Defuddle]]
- [[Obsidian Flavored Markdown]]
- [[Obsidian Bases]]
- [[Obsidian CLI]]