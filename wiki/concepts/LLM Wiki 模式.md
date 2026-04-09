---
title: LLM Wiki 模式
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
tags: [知识管理, LLM, Wiki, 模式]
type: concept
---

# LLM Wiki 模式

一种利用 LLM 构建和维护个人知识库的方法论，由 [[Andrej Karpathy]] 提出。

## 核心原理

LLM 不是在查询时从原始文档中检索（如 [[RAG]]），而是**增量构建一个持久化的结构化 Wiki**。知识编译一次后持续更新，每次添加来源或提问都会让知识库更丰富。

## 与 RAG 的区别

| 维度 | RAG | LLM Wiki |
|------|-----|----------|
| 知识处理 | 查询时实时检索 | 摄入时预编译 |
| 积累性 | 无积累，每次从头 | 持续积累，不断丰富 |
| 交叉引用 | 无 | 自动维护 |
| 矛盾检测 | 无 | 自动标记 |

## 三层架构

1. **Raw Sources**（原始来源）：不可变的源文档
2. **Wiki**（知识库）：LLM 生成和维护的 Markdown 文件
3. **Schema**（模式）：配置文件，定义工作规范

## 三大操作

- **Ingest**：摄入新来源，提炼并整合到 Wiki
- **Query**：基于 Wiki 回答问题，优秀回答归档为新页面
- **Lint**：定期健康检查

## 设计哲学

- Obsidian 是 IDE，LLM 是程序员，Wiki 是代码库
- 人负责筛选资料和提问，LLM 负责所有维护工作
- 维护成本接近零，因此 Wiki 能持续运转
- 理念源自 [[Memex]]（Vannevar Bush, 1945）
- Schema 层与 [[Agent Skills]] 的理念相通：都是通过结构化指令文件塑造 Agent 行为

## 相关链接

- [[RAG]]
- [[Memex]]
- [[Agent Skills]]
- [[Andrej Karpathy]]
- [[Anthropic]]
- [[LLM Wiki - 摘要]]
- [[Obsidian]]
- [[oh-my-openagent]]（类似理念：结构化指令 + 自动化维护）
