---
title: Context7 - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[upstash context7]]"
tags:
  - AI
  - LLM
  - 文档检索
  - MCP
  - 开发工具
type: source-summary
---

# Context7 — 来源摘要

## 核心问题

LLM 的训练数据过时，导致代码生成时出现：
- 基于旧版本训练数据的过时代码示例
- 虚构不存在的 API
- 旧版本软件包的通用答案

## 解决方案

Context7 直接从源代码提取最新的、特定版本的文档和代码示例，注入到 LLM 上下文中。

## 安装配置

### 一键安装

```bash
npx ctx7 setup
```

自动完成：OAuth 认证 → 生成 API 密钥 → 安装技能

可选参数：`--cursor`、`--claude`、`--opencode` 指定特定代理

### 手动配置（MCP）

服务器 URL：`https://mcp.context7.com/mcp`

认证方式：通过 `CONTEXT7_API_KEY` 标头传递 API 密钥

### API 密钥

免费获取：[context7.com/dashboard](https://context7.com/dashboard)

推荐使用 API 密钥以获得更高的速率限制

## 使用方式

### 工作模式

| 模式 | 说明 | 适用场景 |
|------|------|----------|
| CLI + Skills | 安装技能指导 Agent 使用 `ctx7` 命令 | 无需 MCP |
| MCP | 注册 MCP 服务器，Agent 原生调用工具 | 深度集成 |

### 提示词示例

```
Create a Next.js middleware that checks for a valid JWT
in cookies and redirects unauthenticated users to `/login`.
use context7
```

```
Show me the Supabase auth API for email/password sign-up.
```

### 高级技巧

**指定 Library ID**（跳过匹配步骤）：
```
Implement basic authentication with Supabase.
use library /supabase/supabase for API and docs.
```

**指定版本**：
```
How do I set up Next.js 14 middleware? use context7
```

## 可用工具

### CLI 命令

| 命令 | 功能 |
|------|------|
| `ctx7 library <name> <query>` | 按名称搜索库，返回匹配库及其 ID |
| `ctx7 docs <libraryId> <query>` | 使用库 ID 检索文档 |

### MCP 工具

| 工具 | 功能 | 参数 |
|------|------|------|
| `resolve-library-id` | 解析库名称为 Context7 ID | `libraryName`, `query` |
| `query-docs` | 检索库文档 | `libraryId`, `query` |

## 支持的工具/代理

- **Cursor**：`Cursor Settings > Rules`
- **Claude Code**：`CLAUDE.md`
- **OpenCode**：`--opencode` 参数
- 其他：[30+ MCP 客户端](https://context7.com/docs/resources/all-clients)

## 添加规则示例

```
Always use Context7 when I need library/API documentation,
code generation, setup or configuration steps without me
having to explicitly ask.
```

## 支持的库（示例）

- Next.js
- Supabase
- Cloudflare Workers
- MongoDB
- 更多社区贡献库

## 相关链接

- [[Context7]]
- [[Upstash]]
- [[MCP]]
- [CLI Reference](https://context7.com/docs/clients/cli)
- [MCP Clients](https://context7.com/docs/resources/all-clients)
- [API Reference](https://context7.com/docs/api-guide)