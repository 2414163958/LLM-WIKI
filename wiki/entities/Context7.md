---
title: Context7
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[upstash context7]]"
tags:
  - AI工具
  - LLM
  - 文档检索
  - MCP
  - 开源
type: entity
---

# Context7

由 [[Upstash]] 开发的 LLM 文档检索平台，为 AI 代码编辑器提供最新的库文档和代码示例。

## 核心价值

解决 LLM 训练数据过时的问题：
- 过时的代码示例（基于一年前的训练数据）
- 虚构不存在的 API
- 旧版本的通用答案

## 技术架构

### 两种模式

| 模式 | 实现 | 特点 |
|------|------|------|
| CLI + Skills | `ctx7` 命令行工具 + 技能文件 | 无需 MCP，轻量 |
| MCP | Model Context Protocol 服务器 | 原生集成，深度调用 |

### 核心工具

**CLI**：
- `ctx7 library` — 搜索库
- `ctx7 docs` — 检索文档

**MCP**：
- `resolve-library-id` — 解析库 ID
- `query-docs` — 查询文档

## 安装使用

### 快速开始

```bash
npx ctx7 setup
```

支持：`--cursor`、`--claude`、`--opencode`

### 手动配置

MCP 服务器：`https://mcp.context7.com/mcp`

API 密钥：[context7.com/dashboard](https://context7.com/dashboard) 免费获取

## 支持的代理/编辑器

- [[Cursor]]
- [[Claude Code]]
- [[OpenCode]]
- 30+ MCP 客户端

## 开源信息

- GitHub: [upstash/context7](https://github.com/upstash/context7)
- License: MIT
- 注意：API 后端、解析引擎、爬虫引擎为私有

## 与其他概念的关联

- 基于 [[MCP]] 协议提供工具集成
- 与 [[Agent Skills]] 理念互补：Skills 教 Agent "如何做"，Context7 提供最新的"参考资料"
- 可用于增强 [[LLM Wiki 模式]] 中的 Agent 能力

## 相关链接

- [[Context7 - 摘要]]
- [[Upstash]]
- [[MCP]]
- [[Agent Skills]]
- [官网](https://context7.com/)
- [GitHub](https://github.com/upstash/context7)