---
title: LLM Wiki - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
tags: [知识管理, LLM, Wiki, Karpathy]
type: source-summary
---
# LLM Wiki — 来源摘要

## 核心思想

LLM Wiki 是一种利用 LLM 构建个人知识库的模式。与传统 RAG（每次查询重新检索原始文档）不同，LLM **增量构建并维护一个持久化的 Wiki**——结构化、互联的 Markdown 文件集合。知识编译一次后持续更新，而非每次查询时重新推导。

**关键区别：Wiki 是持续积累的知识制品。** 交叉引用已存在，矛盾已被标记，综合已反映所有已读内容。

## 三层架构

| 层 | 说明 |
|---|---|
| **Raw Sources** | 原始文档，不可变，LLM 只读 |
| **Wiki** | LLM 生成和维护的 Markdown 文件（摘要、实体页、概念页等） |
| **Schema** | 配置文件（如 AGENTS.md），定义结构、约定和工作流程 |

## 三大操作

1. **Ingest（摄入）**：添加来源后，LLM 读取、提炼、整合到 Wiki，更新相关页面和索引
2. **Query（查询）**：基于 Wiki 回答问题，优秀回答可归档为新页面
3. **Lint（检查）**：定期健康检查——矛盾、过时信息、孤立页面、缺失交叉引用

## 适用场景

- 个人目标/健康/心理跟踪
- 深度研究（论文、报告）
- 读书笔记（人物、主题、情节）
- 团队内部 Wiki（Slack、会议记录、项目文档）
- 竞品分析、尽职调查、旅行计划等

## 推荐工具

- [[Obsidian]] — 作为 IDE 浏览和编辑 Wiki
- Obsidian Web Clipper — 将网页转为 Markdown
- [[Dataview]] — Obsidian 插件，查询页面 frontmatter
- [[Marp]] — Markdown 幻灯片格式
- [[qmd]] — 本地 Markdown 搜索引擎（BM25 + 向量搜索 + LLM 重排序）
- Git — 版本控制和协作

## 历史渊源

该理念与 [[Memex]]（Vannevar Bush, 1945）一脉相承——个人化、精心维护的知识库，文档之间的关联与文档本身同样重要。LLM 解决了 Memex 未能解决的问题：谁来维护。

## 核心洞察

> 维护知识库最繁琐的不是阅读或思考，而是记录。LLM 不会感到厌倦，不会忘记更新交叉引用，一次就能处理 15 个文件。维护成本接近零，所以 Wiki 能持续运转。

人的职责：筛选资料、指导分析、提出好问题。LLM 的职责：其余一切。

## 相关链接

- [[LLM Wiki 模式]]
- [[RAG]]
- [[Memex]]
- [[Andrej Karpathy]]
- [[Obsidian]]
- [[qmd]]
- [[Marp]]
- [[Dataview]]
