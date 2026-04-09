---
title: qmd
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
tags: [工具, 搜索, 本地]
type: entity
---

# qmd

一款本地 Markdown 文件搜索引擎，由 Tobi（Shopify CEO）开发。

## 特性

- 混合搜索：BM25 + 向量搜索
- LLM 重排序
- 全部在设备端运行（无需云端）
- 提供 CLI 和 MCP Server 两种接口

## 在 LLM Wiki 模式中的角色

在 [[LLM Wiki 模式]] 中，qmd 用于在 Wiki 规模增长后替代简单的 [[index.md]] 文件，提供更强大的搜索能力。LLM 可以通过 CLI 或 MCP Server 直接调用 qmd 进行搜索。

## 相关链接

- [[LLM Wiki 模式]]
- [[LLM Wiki - 摘要]]
- [[RAG]]
