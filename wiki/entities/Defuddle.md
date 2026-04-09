---
title: Defuddle
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/kepano obsidian-skills]]"
tags:
  - 工具
  - 网页抓取
  - Markdown
type: entity
---

# Defuddle

从网页提取干净 Markdown 的工具，去除广告、导航等冗余内容，节省 LLM Token。

## 功能

- 从任意网页提取正文内容
- 输出干净的结构化 Markdown
- 减少噪音，优化 LLM 输入

## 仓库

[kepano/defuddle-cli](https://github.com/kepano/defuddle-cli)

## 在 Agent Skills 中的应用

[[obsidian-skills]] 提供的 `defuddle` skill 让 Agent 能够：
- 抓取网页内容
- 自动清洗和格式化
- 生成适合 LLM 处理的 Markdown

## 相关链接

- [[Steph Ango]] — 作者
- [[obsidian-skills - 摘要]]
- [[Firecrawl]] — 类似功能，提供 API 和 MCP 集成