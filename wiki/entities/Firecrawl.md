---
title: Firecrawl
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/firecrawl firecrawl.md]]"
tags: [api, web-scraping, mcp, agent-tools, open-source]
type: entity
---

# Firecrawl

**Firecrawl** 是为 AI Agent 提供网络数据的 API 服务。开源（AGPL-3.0），提供托管服务。

## 定位

"利用干净的网络数据赋能 AI 代理" —— 为 LLM 应用提供 Search、Scrape、Crawl、Agent 等能力，输出 Markdown/JSON/截图等格式。

## 核心能力

| 功能 | 说明 |
|------|------|
| Search | 搜索网络 + 返回完整页面内容 |
| Scrape | URL → Markdown/HTML/JSON/截图 |
| Interact | 抓取后执行页面操作（点击、滚动、输入） |
| Agent | 自主数据采集（描述需求即可） |
| Crawl | 整站爬取 |
| Map | 发现网站所有 URL |
| Batch Scrape | 批量异步抓取 |

## 性能指标

- 覆盖 96% 网页（含 JS 重型页面）
- P95 延迟 3.4 秒
- 自动处理代理轮换、速率限制、JS 屏蔽

## Agent 集成

### Skill

一键为 Agent 配置网络数据能力：

```bash
npx -y firecrawl-cli@latest init --all --browser
```

支持 [[Claude Code]]、[[OpenCode]]、Antigravity 等。

### MCP

提供 [[MCP]] Server，任何兼容 MCP 的客户端可直接接入：

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

## SDK 支持

- **Python**: `pip install firecrawl-py`
- **Node.js**: `npm install @mendable/firecrawl-js`
- **Java**: `com.github.firecrawl:firecrawl-java-sdk:2.0`
- **Elixir**: `{:firecrawl, "~> 1.0"}`
- **社区**: Go、Rust

## 与相关工具对比

| 特性 | Firecrawl | [[Context7]] |
|------|-----------|--------------|
| 数据类型 | 网页内容 | 库文档 |
| 集成方式 | MCP / Skill | MCP |
| 主要用途 | 网络数据采集 | API 文档检索 |
| 自主能力 | Agent 自主采集 | 按需查询 |

## 官方资源

- 官网：https://firecrawl.dev
- 文档：https://docs.firecrawl.dev
- API 参考：https://docs.firecrawl.dev/api-reference
- Playground：https://firecrawl.dev/playground
- GitHub：https://github.com/firecrawl/firecrawl

## 相关链接

- [[Firecrawl - 摘要]] — 技术文档
- [[MCP]] — Model Context Protocol
- [[Agent Skills]] — Agent 技能系统
- [[Context7]] — 文档检索平台（互补工具）
- [[Claude Code]] — 支持的 Agent 客户端
- [[OpenCode]] — 支持的 Agent 客户端