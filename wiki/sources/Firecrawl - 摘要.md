---
title: Firecrawl - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/firecrawl firecrawl.md]]"
tags: [web-scraping, api, mcp, agent-tools]
type: source-summary
---

# Firecrawl - 摘要

## 概述

Firecrawl 是为 AI Agent 提供网络数据的 API 服务。覆盖 96% 网页（含 JS 重型页面），P95 延迟 3.4 秒，输出 Markdown/JSON/截图等 LLM 友好格式。开源（AGPL-3.0），提供托管服务。

## 核心端点

### Search（搜索）

搜索网络并返回完整页面内容：

```python
from firecrawl import Firecrawl
app = Firecrawl(api_key="fc-YOUR_API_KEY")
result = app.search("firecrawl web scraping", limit=5)
```

**输出格式**：
```json
[
  {
    "url": "https://firecrawl.dev",
    "title": "Firecrawl",
    "markdown": "Turn websites into..."
  }
]
```

### Scrape（抓取）

将 URL 转换为 Markdown/HTML/JSON/截图：

```python
result = app.scrape('firecrawl.dev', formats=["markdown"])
print(result.markdown)
```

### Interact（交互）

抓取页面后执行操作（点击、滚动、输入、等待）：

```python
result = app.scrape("https://amazon.com")
scrape_id = result.metadata.scrape_id

app.interact(scrape_id, prompt="Search for 'mechanical keyboard'")
app.interact(scrape_id, prompt="Click the first result")
```

### Agent（自主采集）

描述需求，Agent 自动搜索、导航、提取：

```python
result = app.agent(prompt="Find the pricing plans for Notion")
print(result.data)
```

**结构化输出**（使用 Pydantic Schema）：

```python
from pydantic import BaseModel, Field
from typing import List, Optional

class Founder(BaseModel):
    name: str = Field(description="Full name of the founder")
    role: Optional[str] = Field(None, description="Role or position")

class FoundersSchema(BaseModel):
    founders: List[Founder] = Field(description="List of founders")

result = app.agent(
    prompt="Find the founders of Firecrawl",
    schema=FoundersSchema
)
```

**模型选择**：

| Model | Cost | Best For |
|-------|------|----------|
| `spark-1-mini`（默认） | 便宜 60% | 大多数任务 |
| `spark-1-pro` | 标准 | 复杂研究、关键提取 |

### Crawl（整站爬取）

抓取网站所有页面：

```python
docs = app.crawl("https://docs.firecrawl.dev", limit=50)
for doc in docs.data:
    print(doc.metadata.source_url, doc.markdown[:100])
```

### Map（URL 发现）

发现网站所有链接：

```python
result = app.map("https://firecrawl.dev", search="pricing")
# 返回与 "pricing" 相关度排序的 URL 列表
```

### Batch Scrape（批量抓取）

异步抓取数千个 URL：

```python
job = app.batch_scrape([
    "https://firecrawl.dev",
    "https://docs.firecrawl.dev",
    "https://firecrawl.dev/pricing"
], formats=["markdown"])
```

## Agent 集成

### Skill（一键配置）

```bash
npx -y firecrawl-cli@latest init --all --browser
```

支持 Claude Code、OpenCode、Antigravity 等。

### MCP Server

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

## SDK

### Python

```bash
pip install firecrawl-py
```

```python
from firecrawl import Firecrawl
app = Firecrawl(api_key="fc-YOUR_API_KEY")

# 单页抓取
doc = app.scrape("https://firecrawl.dev", formats=["markdown"])

# Agent 自主采集
result = app.agent(prompt="Find the founders of Stripe")

# 整站爬取
docs = app.crawl("https://docs.firecrawl.dev", limit=50)

# 网络搜索
results = app.search("best web scraping tools 2024", limit=10)
```

### Node.js

```bash
npm install @mendable/firecrawl-js
```

```javascript
import Firecrawl from '@mendable/firecrawl-js';
const app = new Firecrawl({ apiKey: 'fc-YOUR_API_KEY' });

const doc = await app.scrape('https://firecrawl.dev', { formats: ['markdown'] });
const result = await app.agent({ prompt: 'Find the founders of Stripe' });
const docs = await app.crawl('https://docs.firecrawl.dev', { limit: 50 });
const results = await app.search('best web scraping tools 2024', { limit: 10 });
```

### Java

```groovy
repositories {
    mavenCentral()
    maven { url 'https://jitpack.io' }
}

dependencies {
    implementation 'com.github.firecrawl:firecrawl-java-sdk:2.0'
}
```

```java
FirecrawlClient client = new FirecrawlClient(System.getenv("FIRECRAWL_API_KEY"), null, null);
FirecrawlDocument doc = client.scrapeURL("https://firecrawl.dev", scrapeParams);
AgentStatusResponse result = client.getAgentStatus(start.getId());
```

### Elixir

```elixir
def deps do
  [{:firecrawl, "~> 1.0"}]
end

{:ok, response} = Firecrawl.scrape_and_extract_from_url(
  url: "https://firecrawl.dev",
  formats: ["markdown"]
)
```

### 社区 SDK

- [Go SDK](https://github.com/mendableai/firecrawl-go)
- [Rust SDK](https://docs.firecrawl.dev/sdks/rust)

## 关键特性

- **可靠性**：96% 网页覆盖率，处理 JS 重型页面
- **速度**：P95 延迟 3.4 秒
- **零配置**：自动处理代理轮换、速率限制、JS 屏蔽
- **媒体解析**：PDF、DOCX 等文件解析
- **实时预览**：Interact 操作提供 Live View URL

## 相关链接

- [[Firecrawl]] — 实体详情
- [[MCP]] — MCP 协议概念
- [[Agent Skills]] — Agent 技能系统
- [[Context7]] — 类似的 LLM 数据服务平台