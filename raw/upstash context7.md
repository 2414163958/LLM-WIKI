---
title: "upstash/context7: Context7 Platform -- Up-to-date code documentation for LLMs and AI code editors"
source: https://github.com/upstash/context7
author:
published:
created: 2026-04-09
description: Context7 Platform -- Up-to-date code documentation for LLMs and AI code editors - upstash/context7
tags:
  - clippings
---
[![[raw/assets/5d87a550d3b323b14db4a0274e7c97d7_MD5.png]]](https://github.com/upstash/context7/blob/master/public/cover.png?raw=true)

## Context7 Platform - Up-to-date Code Docs For Any PromptContext7 平台 - 针对任何提示提供最新代码文档

## ❌ Without Context7 ❌ 无上下文7

LLMs rely on outdated or generic information about the libraries you use. You get:  
法学硕士课程依赖于关于你所用库的过时或通用信息。你会得到：

- ❌ Code examples are outdated and based on year-old training data  
	❌ 代码示例已过时，且基于一年前的训练数据。
- ❌ Hallucinated APIs that don't even exist  
	❌ 根本不存在的虚构 API
- ❌ Generic answers for old package versions  
	❌ 旧版本软件包的通用答案

## ✅ With Context7 ✅ 借助 Context7

Context7 pulls up-to-date, version-specific documentation and code examples straight from the source — and places them directly into your prompt.  
Context7 直接从源代码中提取最新的、特定版本的文档和代码示例，并将它们直接放入您的提示符中。

```
Create a Next.js middleware that checks for a valid JWT in cookies
and redirects unauthenticated users to \`/login\`. use context7
```
```
Configure a Cloudflare Worker script to cache
JSON API responses for five minutes. use context7
```
```
Show me the Supabase auth API for email/password sign-up.
```

Context7 fetches up-to-date code examples and documentation right into your LLM's context. No tab-switching, no hallucinated APIs that don't exist, no outdated code generation.  
Context7 会将最新的代码示例和文档直接导入到您的 LLM 上下文中。无需切换标签页，无需使用不存在的虚假 API，也无需生成过时的代码。

Works in two modes:  
有两种工作模式：

- **CLI + Skills** — installs a skill that guides your agent to fetch docs using `ctx7` CLI commands (no MCP required)  
	**CLI + 技能** — 安装一项技能，指导您的代理使用 `ctx7` CLI 命令获取文档（无需 MCP）
- **MCP** — registers a Context7 MCP server so your agent can call documentation tools natively  
	**MCP** — 注册一个 Context7 MCP 服务器，以便您的代理可以原生调用文档工具。

## Installation 安装

> [!note] Note
> **API Key Recommended**: Get a free API key at [context7.com/dashboard](https://context7.com/dashboard) for higher rate limits.  
> **推荐使用 API 密钥** ：在 [context7.com/dashboard](https://context7.com/dashboard) 获取免费 API 密钥，以获得更高的速率限制。

Set up Context7 for your coding agents with a single command:  
使用一条命令即可为您的编码代理设置 Context7：

```
npx ctx7 setup
```

Authenticates via OAuth, generates an API key, and installs the appropriate skill. You can choose between CLI + Skills or MCP mode. Use `--cursor`, `--claude`, or `--opencode` to target a specific agent.  
通过 OAuth 进行身份验证，生成 API 密钥，并安装相应的技能。您可以选择 CLI + 技能模式或 MCP 模式。使用 `--cursor` 、 `--claude` 或 `--opencode` 参数可以指定特定代理。

To configure manually, use the Context7 server URL `https://mcp.context7.com/mcp` with your MCP client and pass your API key via the `CONTEXT7_API_KEY` header. See the link below for client-specific setup instructions.  
要手动配置，请使用 Context7 服务器 URL `https://mcp.context7.com/mcp` 连接 MCP 客户端，并通过 `CONTEXT7_API_KEY` 标头传递您的 API 密钥。有关特定客户端的设置说明，请参阅以下链接。

**[Manual Installation / Other Clients →  
手动安装/其他客户端 →](https://context7.com/docs/resources/all-clients)**

## Important Tips 重要提示

### Use Library Id 使用图书馆 ID

If you already know exactly which library you want to use, add its Context7 ID to your prompt. That way, Context7 can skip the library-matching step and directly retrieve docs.  
如果您已经确切知道要使用哪个库，请将其 Context7 ID 添加到提示符中。这样，Context7 就可以跳过库匹配步骤，直接检索文档。

```
Implement basic authentication with Supabase. use library /supabase/supabase for API and docs.
```

The slash syntax tells Context7 exactly which library to load docs for.  
斜杠语法可以准确地告诉 Context7 要加载哪个库的文档。

### Specify a Version 指定版本

To get documentation for a specific library version, just mention the version in your prompt:  
要获取特定库版本的文档，只需在提示符中指定版本号即可：

```
How do I set up Next.js 14 middleware? use context7
```

Context7 will automatically match the appropriate version.  
Context7 将自动匹配合适的版本。

### Add a Rule 添加规则

If you installed via `ctx7 setup`, a skill is configured automatically that triggers Context7 for library-related questions. To set up a rule manually instead, add one to your coding agent:  
如果您是通过 `ctx7 setup` 安装的，则会自动配置一个技能，该技能会在遇到与图书馆相关的问题时触发 Context7。要手动设置规则，请将其添加到您的编码代理中：

- **Cursor**: `Cursor Settings > Rules`  
	**光标** ： `Cursor Settings > Rules`
- **Claude Code**: `CLAUDE.md`  
	**克劳德代码** ： `CLAUDE.md`
- Or the equivalent in your coding agent  
	或者在你的编码代理中实现等效功能

**Example rule:示例规则：**

```
Always use Context7 when I need library/API documentation, code generation, setup or configuration steps without me having to explicitly ask.
```

## Available Tools 可用工具

### CLI Commands 命令行界面命令

- `ctx7 library <name> <query>`: Searches the Context7 index by library name and returns matching libraries with their IDs.  
	`ctx7 library <name> <query>`: 按库名称搜索 Context7 索引，并返回匹配的库及其 ID。
- `ctx7 docs <libraryId> <query>`: Retrieves documentation for a library using a Context7-compatible library ID (e.g., `/mongodb/docs`, `/vercel/next.js`).  
	ctx7 docs `/vercel/next.js` `ctx7 docs <libraryId> <query>`: 使用 Context7 兼容的库 ID（例如 `/mongodb/docs` ）检索库的文档。

### MCP Tools MCP 工具

- `resolve-library-id`: Resolves a general library name into a Context7-compatible library ID.  
	`resolve-library-id` ：将通用库名称解析为与 Context7 兼容的库 ID。
	- `query` (required): The user's question or task (used to rank results by relevance)  
		`query` （必填）：用户的问题或任务（用于按相关性对结果进行排名）
		- `libraryName` (required): The name of the library to search for  
		`libraryName` （必填）：要查找的库的名称
- `query-docs`: Retrieves documentation for a library using a Context7-compatible library ID.  
	`query-docs` ：使用与 Context7 兼容的库 ID 检索库的文档。
	- `libraryId` (required): Exact Context7-compatible library ID (e.g., `/mongodb/docs`, `/vercel/next.js`)  
		`libraryId` （必填）：与 Context7 兼容的确切库 ID（例如， `/mongodb/docs` ， `/vercel/next.js` ）
		- `query` (required): The question or task to get relevant documentation for  
		`query` （必填）：要获取相关文档的问题或任务

## More Documentation 更多文档

- [CLI Reference](https://context7.com/docs/clients/cli) - Full CLI documentation
- [MCP Clients](https://context7.com/docs/resources/all-clients) - Manual MCP installation for 30+ clients
- [Adding Libraries](https://context7.com/docs/adding-libraries) - Submit your library to Context7
- [Troubleshooting](https://context7.com/docs/resources/troubleshooting) - Common issues and solutions
- [API Reference](https://context7.com/docs/api-guide) - REST API documentation
- [Developer Guide](https://context7.com/docs/resources/developer) - Run Context7 MCP locally

## Disclaimer

1- Context7 projects are community-contributed and while we strive to maintain high quality, we cannot guarantee the accuracy, completeness, or security of all library documentation. Projects listed in Context7 are developed and maintained by their respective owners, not by Context7. If you encounter any suspicious, inappropriate, or potentially harmful content, please use the "Report" button on the project page to notify us immediately. We take all reports seriously and will review flagged content promptly to maintain the integrity and safety of our platform. By using Context7, you acknowledge that you do so at your own discretion and risk.

2- This repository hosts the MCP server’s source code. The supporting components — API backend, parsing engine, and crawling engine — are private and not part of this repository.

## 🤝 Connect with Us

Stay updated and join our community:

- 📢 Follow us on [X](https://x.com/context7ai) for the latest news and updates
- 🌐 Visit our [Website](https://context7.com/)
- 💬 Join our [Discord Community](https://upstash.com/discord)

## 📺 Context7 In Media

- [Better Stack: "Free Tool Makes Cursor 10x Smarter"](https://youtu.be/52FC3qObp9E)
- [Cole Medin: "This is Hands Down the BEST MCP Server for AI Coding Assistants"](https://www.youtube.com/watch?v=G7gK8H6u7Rs)
- [Income Stream Surfers: "Context7 + SequentialThinking MCPs: Is This AGI?"](https://www.youtube.com/watch?v=-ggvzyLpK6o)
- [Julian Goldie SEO: "Context7: New MCP AI Agent Update"](https://www.youtube.com/watch?v=CTZm6fBYisc)
- [JeredBlu: "Context 7 MCP: Get Documentation Instantly + VS Code Setup"](https://www.youtube.com/watch?v=-ls0D-rtET4)
- [Income Stream Surfers: "Context7: The New MCP Server That Will CHANGE AI Coding"](https://www.youtube.com/watch?v=PS-2Azb-C3M)
- [AICodeKing: "Context7 + Cline & RooCode: This MCP Server Makes CLINE 100X MORE EFFECTIVE!"](https://www.youtube.com/watch?v=qZfENAPMnyo)
- [Sean Kochel: "5 MCP Servers For Vibe Coding Glory (Just Plug-In & Go)"](https://www.youtube.com/watch?v=LqTQi8qexJM)

## ⭐ Star History

[![[raw/assets/809830a731c50685fdce07f9f815af18_MD5.svg]]](https://www.star-history.com/#upstash/context7&Date)

## 📄 License

MIT