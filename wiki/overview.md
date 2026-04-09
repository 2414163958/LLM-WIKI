---
title: 知识库总览
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/llm-wiki.md]]"
  - "[[anthropics skills]]"
  - "[[code-yeongyu oh-my-openagent]]"
  - "[[titanwings colleague-skill]]"
  - "[[upstash context7]]"
tags:
  - 总览
type: overview
---

# 知识库总览

测试自动提交

这是一个个人知识库，基于 LLM Wiki 模式构建。知识库通过 LLM 增量构建和维护，以结构化、互联的 Markdown 文件形式组织知识。

## 设计理念

与传统的 RAG（检索增强生成）不同，本知识库采用**持久化、递增式**的知识管理方式：

- **不是每次重新检索**：LLM 在摄入来源时就已经提炼、综合、交叉引用了知识
- **知识持续积累**：每次添加新来源或提出新问题，知识库都会变得更丰富
- **矛盾自动标记**：当新信息与旧信息冲突时，会明确标注
- **LLM 负责维护**：所有的整理、索引、交叉引用、一致性维护都由 LLM 完成

## 知识库结构

- **raw/**：原始来源文档（不可变）
- **wiki/**：LLM 生成和维护的知识页面
- **AGENTS.md**：LLM 的工作指南和规范

## 使用方式

1. **摄入（Ingest）**：将来源文档放入 `raw/`，告诉 LLM 处理
2. **查询（Query）**：向 LLM 提问，基于已有知识综合回答
3. **检查（Lint）**：定期让 LLM 检查知识库健康状况

## 当前状态

知识库已包含 6 个来源：
- [[LLM Wiki - 摘要]]：知识管理方法论
- [[Agent Skills - 摘要]]：Agent 技能系统
- [[oh-my-openagent - 摘要]]：多模型协作 AI 编程框架
- [[colleague-skill - 摘要]]：将同事知识转化为 AI Skill
- [[Context7 - 摘要]]：文档检索平台
- [[Everything Claude Code - 摘要]]：Claude Code 完整配置集合

涵盖知识管理、Agent 技能、AI 编程工具、安全审计等领域。

## 核心主题

- **知识管理**：LLM Wiki 模式、RAG、Memex、持续学习、内存持久化
- **Agent 系统**：Agent Skills、多智能体协作、Harness 问题、上下文管理
- **AI 编程工具**：oh-my-openagent、OpenCode、Claude Code、ECC、AmpCode、Cursor
- **安全与验证**：安全审计、AgentShield、验证循环

## 相关链接

- [[index|内容目录]]
- [[log|操作日志]]
- [[LLM Wiki 模式]]
- [[Agent Skills]]
- [[AI 编程工具对比]]
- [[Everything Claude Code]]
