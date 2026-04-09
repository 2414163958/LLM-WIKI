---
title: "firecrawl/firecrawl: 🔥 The Web Data API for AI - Power AI agents with clean web data"
source: "https://github.com/firecrawl/firecrawl"
author:
published:
created: 2026-04-09
description: "🔥 The Web Data API for AI - Power AI agents with clean web data - firecrawl/firecrawl"
tags:
  - "clippings"
---
## 🔥 Firecrawl 🔥 火行者

**Power AI agents with clean web data.** The API to search, scrape, and interact with the web at scale. Open source and available as a [hosted service](https://firecrawl.dev/?ref=github).  
**利用干净的网络数据赋能 AI 代理。** 提供用于大规模搜索、抓取和交互网络的 API。开源，并可作为 [托管服务](https://firecrawl.dev/?ref=github) 使用。

*Pst. Hey, you, join our stargazers:)  
嘘！嘿，你，加入我们的观星队伍吧:)*

---

## Why Firecrawl? 为什么选择 Firecrawl？

- **Industry-leading reliability**: Covers 96% of the web, including JS-heavy pages — no proxy headaches, just clean data ([see benchmarks](https://www.firecrawl.dev/blog/the-worlds-best-web-data-api-v25))  
	**业界领先的可靠性** ：覆盖 96% 的网络，包括大量使用 JS 的页面——无需代理，只有干净的数据（ [参见基准测试](https://www.firecrawl.dev/blog/the-worlds-best-web-data-api-v25) ）
- **Blazingly fast**: P95 latency of 3.4s across millions of pages, built for real-time agents and dynamic apps  
	**速度极快** ：P95 延迟仅为 3.4 秒，可处理数百万页，专为实时代理和动态应用程序而打造。
- **LLM-ready output**: Clean markdown, structured JSON, screenshots, and more — spend fewer tokens, build better AI apps  
	**支持 LLM 的输出** ：简洁的 Markdown、结构化的 JSON、屏幕截图等等——花费更少的代币，构建更优质的 AI 应用
- **We handle the hard stuff**: Rotating proxies, orchestration, rate limits, JS-blocked content, and more — zero configuration  
	**我们负责处理所有棘手的问题** ：代理轮换、编排、速率限制、JS 屏蔽内容等等——无需任何配置。
- **Agent ready**: Connect Firecrawl to any AI agent or MCP client with a single command  
	**代理就绪** ：只需一条命令即可将 Firecrawl 连接到任何 AI 代理或 MCP 客户端
- **Media parsing**: Parse and extract content from web-hosted PDFs, DOCX, and more  
	**媒体解析** ：解析并提取网络托管的 PDF、DOCX 等文件中的内容
- **Actions**: Click, scroll, write, wait, and press before extracting content  
	**操作** ：点击、滚动、输入、等待、按下按钮，然后提取内容
- **Open source**: Developed transparently and collaboratively — [join our community](https://github.com/firecrawl/firecrawl)  
	**开源** ：以透明协作的方式开发—— [加入我们的社区](https://github.com/firecrawl/firecrawl)

---

## Feature Overview 功能概述

**Core Endpoints 核心端点**

| Feature 特征 | Description 描述 |
| --- | --- |
| [**Search 搜索**](#search) | Search the web and get full page content from results   搜索网络并从搜索结果中获取完整页面内容。 |
| [**Scrape 刮**](#scrape) | Convert any URL to markdown, HTML, screenshots, or structured JSON   将任何 URL 转换为 Markdown、HTML、屏幕截图或结构化 JSON |
| [**Interact 相互影响**](#interact) | Scrape a page, then interact with it using AI prompts or code   抓取网页内容，然后使用 AI 提示或代码与其交互。 |

**More 更多的**

| Feature 特征 | Description 描述 |
| --- | --- |
| [**Agent 代理人**](#agent) | Automated data gathering, just describe what you need   自动数据采集，只需描述您的需求即可 |
| [**Crawl 爬行**](#crawl) | Scrape all URLs of a website with a single request   通过一次请求抓取网站的所有 URL |
| [**Map 地图**](#map) | Discover all URLs on a website instantly   立即发现网站上的所有网址 |
| [**Batch Scrape 批量抓取**](#batch-scrape) | Scrape thousands of URLs asynchronously   异步抓取数千个 URL |

---

## Quick Start 快速入门

Sign up at [firecrawl.dev](https://firecrawl.dev/) to get your API key. Try the [playground](https://firecrawl.dev/playground) to test it out.  
请访问 [firecrawl.dev](https://firecrawl.dev/) 注册以获取 API 密钥。然后尝试使用 [Playground](https://firecrawl.dev/playground) 进行测试。

### Search 搜索

Search the web and get full content from results.  
搜索网络并从搜索结果中获取完整内容。

```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

search_result = app.search("firecrawl web scraping", limit=5)
```
**Node.js / cURL / CLI**

**Node.js**

```
import Firecrawl from '@mendable/firecrawl-js';

const app = new Firecrawl({apiKey: "fc-YOUR_API_KEY"});

app.search("firecrawl web scraping", { limit: 5 })
```

**cURL**

```
curl -X POST 'https://api.firecrawl.dev/v2/search' \
-H 'Authorization: Bearer fc-YOUR_API_KEY' \
-H 'Content-Type: application/json' \
-d '{
  "query": "firecrawl web scraping",
  "limit": 5
}'
```

**CLI**

```
firecrawl search "firecrawl web scraping" --limit 5
```

Output:输出：

```
[
  {
    "url": "https://firecrawl.dev",
    "title": "Firecrawl",
    "markdown": "Turn websites into..."
  },
  {
    "url": "https://docs.firecrawl.dev",
    "title": "Firecrawl Docs",
    "markdown": "# Getting Started..."
  }
]
```

### Scrape 刮

Get LLM-ready data from any website — markdown, JSON, screenshots, and more.  
从任何网站获取 LLM 就绪数据——markdown、JSON、屏幕截图等。

```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

result = app.scrape('firecrawl.dev')
```
**Node.js / cURL / CLI**

**Node.js**

```
import Firecrawl from '@mendable/firecrawl-js';

const app = new Firecrawl({ apiKey: "fc-YOUR_API_KEY" });

app.scrape('firecrawl.dev')
```

**cURL**

```
curl -X POST 'https://api.firecrawl.dev/v2/scrape' \
-H 'Authorization: Bearer fc-YOUR_API_KEY' \
-H 'Content-Type: application/json' \
-d '{
  "url": "firecrawl.dev"
}'
```

**CLI**

```
firecrawl scrape https://firecrawl.dev
firecrawl https://firecrawl.dev --only-main-content
```

Output:输出：

```
# Firecrawl

Firecrawl is a powerful web scraping tool that makes it easy
to extract clean data from any website.

## Features
- Scrape: Markdown from any page
- Search: Search + scrape the web
- Map: Discover all site URLs
- Agent: Extract with AI prompts
```

### Interact 相互影响

Scrape a page, then interact with it using AI prompts or code.  
抓取网页内容，然后使用人工智能提示或代码与其进行交互。

```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

result = app.scrape("https://amazon.com")
scrape_id = result.metadata.scrape_id

app.interact(scrape_id, prompt="Search for 'mechanical keyboard'")
app.interact(scrape_id, prompt="Click the first result")
```
**Node.js / cURL / CLI**

**Node.js**

```
import Firecrawl from '@mendable/firecrawl-js';

const app = new Firecrawl({apiKey: "fc-YOUR_API_KEY"});

const result = await app.scrape("https://amazon.com");

await app.interact(result.metadata.scrapeId, {
  prompt: "Search for 'mechanical keyboard'"
});
await app.interact(result.metadata.scrapeId, {
  prompt: "Click the first result"
});
```

**cURL**

```
# 1. Scrape the page
curl -X POST 'https://api.firecrawl.dev/v2/scrape' \
-H 'Authorization: Bearer fc-YOUR_API_KEY' \
-H 'Content-Type: application/json' \
-d '{"url": "https://amazon.com"}'

# 2. Interact with the page (use scrapeId from step 1)
curl -X POST 'https://api.firecrawl.dev/v2/scrape/SCRAPE_ID/interact' \
-H 'Authorization: Bearer fc-YOUR_API_KEY' \
-H 'Content-Type: application/json' \
-d '{"prompt": "Search for mechanical keyboard"}'
```

**CLI**

```
firecrawl scrape https://amazon.com
firecrawl interact exec --prompt "Search for 'mechanical keyboard'"
firecrawl interact exec --prompt "Click the first result"
```

Output:输出：

```
{
  "success": true,
  "output": "Keyboard available at $100",
  "liveViewUrl": "https://liveview.firecrawl.dev/..."
}
```

---

## Power Your Agent 赋能你的经纪人

Connect Firecrawl to any AI agent or MCP client in minutes.  
几分钟内即可将 Firecrawl 连接到任何 AI 代理或 MCP 客户端。

### Skill 技能

Give your agent easy access to real-time web data with one command.  
只需一条命令，即可让您的代理轻松访问实时网络数据。

```
npx -y firecrawl-cli@latest init --all --browser
```

Restart your agent after installing. Works with [Claude Code](https://claude.ai/code), [Antigravity](https://antigravity.google/), [OpenCode](https://opencode.ai/), and more.  
安装后请重启代理。支持 [Claude Code](https://claude.ai/code) 、 [Antigravity](https://antigravity.google/) 、 [OpenCode](https://opencode.ai/) 等多种框架。

### MCP

Connect any MCP-compatible client to the web in seconds.  
只需几秒钟，即可将任何兼容 MCP 的客户端连接到互联网。

```
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

### Agent Onboarding 代理入职

Are you an AI agent? Fetch this skill to sign up your user, get an API key, and start building with Firecrawl.  
您是人工智能代理吗？获取此技能以注册您的用户、获取 API 密钥并开始使用 Firecrawl 进行构建。

```
curl -s https://firecrawl.dev/agent-onboarding/SKILL.md
```

See the [Skill + CLI documentation](https://docs.firecrawl.dev/sdks/cli) for all available commands. For MCP, see [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server).  
请参阅 [Skill + CLI 文档](https://docs.firecrawl.dev/sdks/cli) 以了解所有可用命令。对于 MCP，请参阅 [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) 。

---

## More Endpoints 更多端点

### Agent 代理人

**The easiest way to get data from the web.** Describe what you need, and our AI agent searches, navigates, and extracts it. No URLs required.  
**从网络获取数据的最简便方法。** 只需描述您的需求，我们的人工智能代理即可搜索、浏览并提取所需内容。无需提供网址。

Agent is the evolution of our `/extract` endpoint: faster, more reliable, and doesn't require you to know the URLs upfront.  
Agent 是我们 `/extract` 端点的升级版：速度更快、更可靠，而且无需您事先知道 URL。

```
curl -X POST 'https://api.firecrawl.dev/v2/agent' \
  -H 'Authorization: Bearer fc-YOUR_API_KEY' \
  -H 'Content-Type: application/json' \
  -d '{
    "prompt": "Find the pricing plans for Notion"
  }'
```

Response:回复：

```
{
  "success": true,
  "data": {
    "result": "Notion offers the following pricing plans:\n\n1. Free - $0/month...\n2. Plus - $10/seat/month...\n3. Business - $18/seat/month...",
    "sources": ["https://www.notion.so/pricing"]
  }
}
```

#### Agent with Structured Output具有结构化输出的代理

Use a schema to get structured data:  
使用模式获取结构化数据：

```
from firecrawl import Firecrawl
from pydantic import BaseModel, Field
from typing import List, Optional

app = Firecrawl(api_key="fc-YOUR_API_KEY")

class Founder(BaseModel):
    name: str = Field(description="Full name of the founder")
    role: Optional[str] = Field(None, description="Role or position")

class FoundersSchema(BaseModel):
    founders: List[Founder] = Field(description="List of founders")

result = app.agent(
    prompt="Find the founders of Firecrawl",
    schema=FoundersSchema
)

print(result.data)
```
```
{
  "founders": [
    {"name": "Eric Ciarla", "role": "Co-founder"},
    {"name": "Nicolas Camara", "role": "Co-founder"},
    {"name": "Caleb Peffer", "role": "Co-founder"}
  ]
}
```

#### Agent with URLs (Optional)代理（带 URL，可选）

Focus the agent on specific pages:  
将代理引导至特定页面：

```
result = app.agent(
    urls=["https://docs.firecrawl.dev", "https://firecrawl.dev/pricing"],
    prompt="Compare the features and pricing information"
)
```

#### Model Selection 模型选择

Choose between two models based on your needs:  
根据您的需求，从以下两种型号中选择：

| Model | Cost 成本 | Best For 最适合 |
| --- | --- | --- |
| `spark-1-mini` (default)   `spark-1-mini` （默认） | 60% cheaper 便宜 60%。 | Most tasks 大多数任务 |
| `spark-1-pro` | Standard 标准 | Complex research, critical extraction   复杂研究，关键提取 |

```
result = app.agent(
    prompt="Compare enterprise features across Firecrawl, Apify, and ScrapingBee",
    model="spark-1-pro"
)
```

**When to use Pro:何时使用专业版：**

- Comparing data across multiple websites  
	比较多个网站的数据
- Extracting from sites with complex navigation or auth  
	从具有复杂导航或身份验证的网站中提取信息
- Research tasks where the agent needs to explore multiple paths  
	研究任务中，智能体需要探索多条路径
- Critical data where accuracy is paramount  
	准确性至关重要的关键数据

Learn more about Spark models in our [Agent documentation](https://docs.firecrawl.dev/features/agent).  
在我们的 [代理文档](https://docs.firecrawl.dev/features/agent) 中了解更多关于 Spark 模型的信息。

### Crawl 爬行

Crawl an entire website and get content from all pages.  
抓取整个网站并获取所有页面的内容。

```
curl -X POST 'https://api.firecrawl.dev/v2/crawl' \
  -H 'Authorization: Bearer fc-YOUR_API_KEY' \
  -H 'Content-Type: application/json' \
  -d '{
    "url": "https://docs.firecrawl.dev",
    "limit": 100,
    "scrapeOptions": {
      "formats": ["markdown"]
    }
  }'
```

Returns a job ID:  
返回一个作业 ID：

```
{
  "success": true,
  "id": "123-456-789",
  "url": "https://api.firecrawl.dev/v2/crawl/123-456-789"
}
```

#### Check Crawl Status 检查爬取状态

```
curl -X GET 'https://api.firecrawl.dev/v2/crawl/123-456-789' \
  -H 'Authorization: Bearer fc-YOUR_API_KEY'
```
```
{
  "status": "completed",
  "total": 50,
  "completed": 50,
  "creditsUsed": 50,
  "data": [
    {
      "markdown": "# Page Title\n\nContent...",
      "metadata": {"title": "Page Title", "sourceURL": "https://..."}
    }
  ]
}
```

**Note:** The [SDKs](#sdks) handle polling automatically for a better developer experience.  
**注意：** [SDK](#sdks) 会自动处理轮询，以提供更好的开发者体验。

### Map 地图

Discover all URLs on a website instantly.  
立即发现网站上的所有网址。

```
curl -X POST 'https://api.firecrawl.dev/v2/map' \
  -H 'Authorization: Bearer fc-YOUR_API_KEY' \
  -H 'Content-Type: application/json' \
  -d '{"url": "https://firecrawl.dev"}'
```

Response:回复：

```
{
  "success": true,
  "links": [
    {"url": "https://firecrawl.dev", "title": "Firecrawl", "description": "Turn websites into LLM-ready data"},
    {"url": "https://firecrawl.dev/pricing", "title": "Pricing", "description": "Firecrawl pricing plans"},
    {"url": "https://firecrawl.dev/blog", "title": "Blog", "description": "Firecrawl blog"}
  ]
}
```

#### Map with Search 带搜索功能的地图

Find specific URLs within a site:  
查找网站内的特定 URL：

```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

result = app.map("https://firecrawl.dev", search="pricing")
# Returns URLs ordered by relevance to "pricing"
```

### Batch Scrape 批量抓取

Scrape multiple URLs at once:  
一次抓取多个 URL：

```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

job = app.batch_scrape([
    "https://firecrawl.dev",
    "https://docs.firecrawl.dev",
    "https://firecrawl.dev/pricing"
], formats=["markdown"])

for doc in job.data:
    print(doc.metadata.source_url)
```

---

## SDKs SDK

Our SDKs provide a convenient way to interact with all Firecrawl features and automatically handle polling for async operations like crawling and batch scraping.  
我们的 SDK 提供了一种便捷的方式来与所有 Firecrawl 功能进行交互，并自动处理异步操作（如爬取和批量抓取）的轮询。

### Python

Install the SDK:安装 SDK：

```
pip install firecrawl-py
```
```
from firecrawl import Firecrawl

app = Firecrawl(api_key="fc-YOUR_API_KEY")

# Scrape a single URL
doc = app.scrape("https://firecrawl.dev", formats=["markdown"])
print(doc.markdown)

# Use the Agent for autonomous data gathering
result = app.agent(prompt="Find the founders of Stripe")
print(result.data)

# Crawl a website (automatically waits for completion)
docs = app.crawl("https://docs.firecrawl.dev", limit=50)
for doc in docs.data:
    print(doc.metadata.source_url, doc.markdown[:100])

# Search the web
results = app.search("best web scraping tools 2024", limit=10)
print(results)
```

### Node.js

Install the SDK:安装 SDK：

```
npm install @mendable/firecrawl-js
```
```
import Firecrawl from '@mendable/firecrawl-js';

const app = new Firecrawl({ apiKey: 'fc-YOUR_API_KEY' });

// Scrape a single URL
const doc = await app.scrape('https://firecrawl.dev', { formats: ['markdown'] });
console.log(doc.markdown);

// Use the Agent for autonomous data gathering
const result = await app.agent({ prompt: 'Find the founders of Stripe' });
console.log(result.data);

// Crawl a website (automatically waits for completion)
const docs = await app.crawl('https://docs.firecrawl.dev', { limit: 50 });
docs.data.forEach(doc => {
    console.log(doc.metadata.sourceURL, doc.markdown.substring(0, 100));
});

// Search the web
const results = await app.search('best web scraping tools 2024', { limit: 10 });
results.data.web.forEach(result => {
    console.log(\`${result.title}: ${result.url}\`);
});
```

### Java

Add the dependency ([Gradle/Maven](https://docs.firecrawl.dev/sdks/java#installation)):  
添加依赖项（ [Gradle/Maven](https://docs.firecrawl.dev/sdks/java#installation) ）：

```
repositories {
    mavenCentral()
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'com.github.firecrawl:firecrawl-java-sdk:2.0'
}
```
```
import dev.firecrawl.client.FirecrawlClient;
import dev.firecrawl.model.*;

FirecrawlClient client = new FirecrawlClient(
    System.getenv("FIRECRAWL_API_KEY"), null, null
);

// Scrape a single URL
ScrapeParams scrapeParams = new ScrapeParams();
scrapeParams.setFormats(new String[]{"markdown"});
FirecrawlDocument doc = client.scrapeURL("https://firecrawl.dev", scrapeParams);
System.out.println(doc.getMarkdown());

// Use the Agent for autonomous data gathering
AgentParams agentParams = new AgentParams("Find the founders of Stripe");
AgentResponse start = client.createAgent(agentParams);
AgentStatusResponse result = client.getAgentStatus(start.getId());
System.out.println(result.getData());

// Crawl a website (polls until completion)
CrawlParams crawlParams = new CrawlParams();
crawlParams.setLimit(50);
CrawlStatusResponse job = client.crawlURL("https://docs.firecrawl.dev", crawlParams, null, 10);
for (FirecrawlDocument page : job.getData()) {
    System.out.println(page.getMetadata().get("sourceURL"));
}

// Search the web
SearchParams searchParams = new SearchParams("best web scraping tools 2024");
searchParams.setLimit(10);
SearchResponse results = client.search(searchParams);
for (SearchResult r : results.getResults()) {
    System.out.println(r.getTitle() + ": " + r.getUrl());
}
```

### Elixir 灵药

Add the dependency:添加依赖项：

```
def deps do
  [
    {:firecrawl, "~> 1.0"}
  ]
end
```
```
# Scrape a URL
{:ok, response} = Firecrawl.scrape_and_extract_from_url(
  url: "https://firecrawl.dev",
  formats: ["markdown"]
)

# Crawl a website
{:ok, response} = Firecrawl.crawl_urls(
  url: "https://docs.firecrawl.dev",
  limit: 50
)

# Search the web
{:ok, response} = Firecrawl.search_and_scrape(
  query: "best web scraping tools 2024",
  limit: 10
)

# Map URLs
{:ok, response} = Firecrawl.map_urls(url: "https://example.com")
```

### Community SDKs 社区 SDK

- [Go SDK](https://github.com/mendableai/firecrawl-go)
- [Rust SDK](https://docs.firecrawl.dev/sdks/rust)

---

## Integrations 集成

**Agents & AI Tools 代理和人工智能工具**

- [Firecrawl Skill 火行技能](https://docs.firecrawl.dev/sdks/cli)
- [Firecrawl MCP 火爬 MCP](https://github.com/mendableai/firecrawl-mcp-server)

**Platforms 平台**

- [Lovable 可爱的](https://docs.lovable.dev/integrations/firecrawl)
- [Zapier](https://zapier.com/apps/firecrawl/integrations)
- [n8n](https://n8n.io/integrations/firecrawl/)

[View all integrations →  
查看所有集成 →](https://www.firecrawl.dev/integrations)

**Missing your favorite tool?** [Open an issue](https://github.com/mendableai/firecrawl/issues) and let us know!  
**找不到您最喜欢的工具？** [请提交问题报告](https://github.com/mendableai/firecrawl/issues) 告诉我们！

---

## Resources 资源

- [Documentation 文档](https://docs.firecrawl.dev/)
- [API Reference API 参考](https://docs.firecrawl.dev/api-reference/introduction)
- [Playground 操场](https://firecrawl.dev/playground)
- [Changelog 更新日志](https://firecrawl.dev/changelog)

---

## Open Source vs Cloud 开源与云

Firecrawl is open source under the AGPL-3.0 license. The cloud version at [firecrawl.dev](https://firecrawl.dev/) includes additional features:  
[Firecrawl](https://firecrawl.dev/) 采用 AGPL-3.0 许可协议开源。firecrawl.dev 上的云版本包含以下附加功能：

[![[raw/assets/02ebcdfe6471f69ad91cf1f5bff19a5a_MD5.png]]](https://raw.githubusercontent.com/firecrawl/firecrawl/main/img/open-source-cloud.png)

To run locally, see the [Contributing Guide](https://github.com/firecrawl/firecrawl/blob/main/CONTRIBUTING.md). To self-host, see [Self-Hosting Guide](https://docs.firecrawl.dev/contributing/self-host).  
要在本地运行，请参阅 [贡献指南](https://github.com/firecrawl/firecrawl/blob/main/CONTRIBUTING.md) 。要自行托管，请参阅 [自行托管指南](https://docs.firecrawl.dev/contributing/self-host) 。

---

## Contributing 贡献

We love contributions! Please read our [Contributing Guide](https://github.com/firecrawl/firecrawl/blob/main/CONTRIBUTING.md) before submitting a pull request.  
我们欢迎大家贡献代码！请在提交 pull request 前阅读我们的 [贡献指南](https://github.com/firecrawl/firecrawl/blob/main/CONTRIBUTING.md) 。

### Contributors 贡献者

[![[raw/assets/180020e9a48bdd9bc1815f12b9774080_MD5.svg]]](https://github.com/firecrawl/firecrawl/graphs/contributors)

---

## License 执照

This project is primarily licensed under the GNU Affero General Public License v3.0 (AGPL-3.0). The SDKs and some UI components are licensed under the MIT License. See the LICENSE files in specific directories for details.  
本项目主要采用 GNU Affero 通用公共许可证 v3.0 (AGPL-3.0) 授权。SDK 和部分 UI 组件采用 MIT 许可证授权。详情请参阅特定目录中的 LICENSE 文件。

---

**It is the sole responsibility of end users to respect websites' policies when scraping.** Users are advised to adhere to applicable privacy policies and terms of use. By default, Firecrawl respects robots.txt directives. By using Firecrawl, you agree to comply with these conditions.  
**用户在使用网页抓取工具时，有责任遵守网站的政策。** 建议用户遵守适用的隐私政策和使用条款。Firecrawl 默认遵循 robots.txt 指令。使用 Firecrawl 即表示您同意遵守这些条款。

[↑ Back to Top ↑  
↑ 返回顶部 ↑](#readme-top)