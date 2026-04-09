---
title: RAG
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
tags: [AI, 知识管理, 检索]
type: concept
---

# RAG（检索增强生成）

Retrieval-Augmented Generation 的缩写。一种让 LLM 基于外部文档回答问题的技术模式。

## 工作原理

1. 用户上传一组文档
2. 查询时，系统检索相关文档片段
3. LLM 基于检索到的片段生成答案

## 局限性

在 [[LLM Wiki 模式]] 的语境下，RAG 存在以下问题：

- **无积累**：每次查询都从头重新发现知识，不建立持久知识结构
- **无交叉引用**：无法自动识别文档间的关联和矛盾
- **综合能力弱**：需要综合多个文档的复杂问题时，每次都要重新拼凑
- **维护负担**：无法自动维护知识的一致性和时效性

## 代表系统

NotebookLM、ChatGPT 文件上传、大多数 RAG 系统都遵循此模式。

## 相关链接

- [[LLM Wiki 模式]]
- [[LLM Wiki - 摘要]]
- [[qmd]]
