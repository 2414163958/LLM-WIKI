---
title: Obsidian Flavored Markdown
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/kepano obsidian-skills.md]]"
tags:
  - Markdown
  - Obsidian
  - 格式
type: concept
---

# Obsidian Flavored Markdown

Obsidian 扩展的 Markdown 语法，在标准 Markdown 基础上增加了维基链接、嵌入、标注、属性等特性。

## 核心语法

| 特性 | 语法 |
|------|------|
| **维基链接** | `[[页面名]]` 或 `[[页面名\|显示文本]]` |
| **嵌入** | `![[页面名]]` 或 `![[图片.png]]` |
| **标注/Callout** | `> [!note] 标题\n> 内容` |
| **属性/Properties** | YAML frontmatter |
| **标签** | `#标签` |

## 文档

[Obsidian Flavored Markdown 官方文档](https://help.obsidian.md/obsidian-flavored-markdown)

## 在 Agent Skills 中的应用

[[obsidian-skills]] 提供的 `obsidian-markdown` skill 让 Agent 能够：
- 正确使用维基链接语法
- 创建嵌入和标注
- 管理 YAML 属性
- 生成符合 Obsidian 风格的 Markdown

## 相关链接

- [[Obsidian]]
- [[内部链接]]
- [[obsidian-skills - 摘要]]