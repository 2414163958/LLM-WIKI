---
title: Agent Skills - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[anthropics skills]]"
tags:
  - AI
  - Agent
  - Claude
  - 技能系统
type: source-summary
---

# Agent Skills — 来源摘要

## 核心内容

[[Anthropic]] 为 Claude 提供的技能系统。技能是包含指令、脚本和资源的文件夹，Claude 动态加载以提升特定任务表现。

## 技能结构

- 每个技能一个文件夹，核心是 `SKILL.md` 文件
- frontmatter 需要 `name`（唯一标识）和 `description`（功能描述）
- Markdown 正文包含指令、示例和指南

## 技能覆盖范围

- 创意与设计（艺术、音乐、设计）
- 开发与技术（Web 测试、MCP 服务器生成）
- 企业与沟通（品牌、沟通）
- 文档处理（docx、pdf、pptx、xlsx）— source-available，非开源

## 使用方式

- **Claude Code**：`/plugin marketplace add anthropics/skills`，然后安装插件
- **Claude.ai**：付费计划内置，也可上传自定义技能
- **Claude API**：通过 Skills API 使用

## 开放生态

- 多数技能 Apache 2.0 开源
- [agentskills.io](http://agentskills.io/) 定义了 Agent Skills 开放标准
- 合作伙伴示例：Notion Skills for Claude

## 相关链接

- [[Agent Skills]]
- [[Anthropic]]
- [[LLM Wiki 模式]]
