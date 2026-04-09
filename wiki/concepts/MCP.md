---
title: MCP
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[upstash context7]]"
tags:
  - AI
  - Agent
  - 协议
  - 工具集成
type: concept
---

# MCP (Model Context Protocol)

Model Context Protocol，AI Agent 工具集成协议，让 LLM 能够通过标准化接口调用外部工具和服务。

## 核心思想

为 LLM 提供统一的工具调用接口：
- **标准化**：统一不同工具的调用方式
- **原生集成**：Agent 无需额外配置即可调用
- **解耦**：工具实现与 Agent 逻辑分离

## 工作原理

```
LLM/Agent ←→ MCP Server ←→ 工具/服务
```

1. Agent 需要外部信息或能力
2. 调用 MCP 服务器提供的工具
3. MCP 服务器执行操作并返回结果
4. Agent 基于结果继续推理

## 典型应用

| 场景 | 示例 |
|------|------|
| 文档检索 | [[Context7]] 提供最新的库文档 |
| 网络数据 | [[Firecrawl]] 提供搜索、抓取、交互能力 |
| 数据库操作 | 查询、插入、更新数据库 |
| API 调用 | 调用外部服务的 API |
| 文件操作 | 读写文件系统 |

## Context7 的 MCP 实现

[[Context7]] 提供两个 MCP 工具：

| 工具 | 功能 |
|------|------|
| `resolve-library-id` | 解析库名称为 Context7 ID |
| `query-docs` | 检索库文档 |

配置方式：
- 服务器 URL：`https://mcp.context7.com/mcp`
- 认证：通过 `CONTEXT7_API_KEY` 标头

## Firecrawl 的 MCP 实现

[[Firecrawl]] 提供网络数据 MCP Server：

```json
{
  "mcpServers": {
    "firecrawl-mcp": {
      "command": "npx",
      "args": ["-y", "firecrawl-mcp"],
      "env": {
        "FIRECRAWL_API_KEY": "fc-YOUR_API_KEY"
      }
    }
  }
}
```

提供的能力：
- Search：搜索网络 + 返回完整页面内容
- Scrape：URL → Markdown/JSON/截图
- Crawl：整站爬取
- Map：发现网站所有 URL

## 与其他概念的关联

- 与 [[Agent Skills]] 互补：Skills 定义"如何做"，MCP 提供"用什么工具"
- 与 [[LSP]] 类似：都是标准化协议，LSP 用于语言服务，MCP 用于工具集成
- 是 [[LLM Wiki 模式]] 中增强 Agent 能力的基础设施
- [[Context7]] 是 MCP 协议的典型应用案例（文档检索）
- [[Firecrawl]] 是 MCP 协议的典型应用案例（网络数据）
- [[OpenCode]] 内置 MCP 服务器集成能力

## 相关链接

- [[Context7]]
- [[Context7 - 摘要]]
- [[Firecrawl]]
- [[Firecrawl - 摘要]]
- [[Agent Skills]]
- [[Upstash]]
- [[LSP]]
- [[OpenCode]]