---
title: Obsidian
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
  - "[[raw/How I use Obsidian.md]]"
  - "[[mtymek opencode-obsidian]]"
  - "[[raw/Vinzent03 obsidian-git.md]]"
tags:
  - 工具
  - 知识管理
  - Markdown
type: entity
---

# Obsidian

一款基于本地 Markdown 文件的知识管理和笔记应用。

## 在 LLM Wiki 模式中的角色

在 [[LLM Wiki 模式]] 中，Obsidian 扮演 **IDE** 的角色：

- LLM 是"程序员"，Wiki 是"代码库"，Obsidian 是查看和浏览的 IDE
- 支持双向链接、图谱视图（Graph View）
- 实时浏览 LLM 的编辑结果

## 相关插件和工具

- **Obsidian Web Clipper**：浏览器扩展，将网页文章转为 Markdown，便于收集来源
- [[Dataview]]：对页面 frontmatter 运行查询，生成动态表格和列表
- [[Marp]]：Markdown 幻灯片格式，直接从 Wiki 内容生成演示文稿
- **[[Obsidian Bases]]**：官方数据库功能（类似 Notion Database）
- **opencode-obsidian**：将 [[OpenCode]] AI 助手嵌入侧边栏（参见 [[opencode-obsidian - 摘要]]）
- **[[obsidian-git]]**：Git 版本控制集成，自动提交同步（参见 [[obsidian-git - 摘要]]）

## Agent Skills

[[obsidian-skills]] 是 [[Steph Ango]] 创建的 Obsidian 专用 Agent Skills 集合，包含：
- `obsidian-markdown` — 创建/编辑 [[Obsidian Flavored Markdown]]
- `obsidian-bases` — 创建/编辑 [[Obsidian Bases]]
- `json-canvas` — 创建/编辑 [[JSON Canvas]]
- `obsidian-cli` — 通过 [[Obsidian CLI]] 操作 Vault
- `defuddle` — 使用 [[Defuddle]] 提取干净 Markdown

## 图片本地化

在 Obsidian 中设置固定附件文件夹路径（如 `raw/assets/`），配合快捷键可将网页图片下载到本地，便于 LLM 直接查看和引用。

## 相关链接

- [[LLM Wiki 模式]]
- [[Dataview]]
- [[Marp]]
- [[Obsidian Bases]]
- [[Obsidian Flavored Markdown]]
- [[JSON Canvas]]
- [[Defuddle]]
- [[obsidian-skills - 摘要]]
- [[LLM Wiki - 摘要]]
- [[opencode-obsidian - 摘要]]
- [[obsidian-git - 摘要]]
- [[obsidian-git]]
- [[Steph Ango]]
