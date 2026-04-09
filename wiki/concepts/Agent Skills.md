---
title: Agent Skills
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/anthropics skills.md]]"
tags:
  - AI
  - Agent
  - 技能系统
  - Claude
type: concept
---

# Agent Skills

由 [[Anthropic]] 提出的 Agent 技能系统，让 AI Agent 动态加载指令、脚本和资源来提升特定任务表现。

## 核心思想

技能是**可复用的知识包**——教会 Agent 以可重复的方式完成特定任务，无需每次重新说明。与 [[LLM Wiki 模式]] 中 Schema 层的理念相通：通过结构化的指令文件塑造 Agent 的行为。

## 技能结构

一个技能 = 一个文件夹 + 一个 `SKILL.md` 文件：

```yaml
---
name: my-skill-name
description: 该技能的功能和使用时机
---

# 技能指令内容
```

frontmatter 只需 `name`（唯一标识）和 `description`（功能描述）两个字段。

## 使用平台

| 平台 | 使用方式 |
|------|----------|
| Claude Code | 插件市场安装，或通过 `/plugin install` 命令 |
| Claude.ai | 付费计划内置，也可上传自定义技能 |
| Claude API | 通过 Skills API 使用和上传 |

## 技能分类

- **创意与设计**：艺术、音乐、设计
- **开发与技术**：Web 应用测试、MCP 服务器生成
- **企业与沟通**：品牌、沟通模板
- **文档技能**：docx、pdf、pptx、xlsx 的创建和编辑

## 开放标准

Agent Skills 有一个开放标准规范，定义于 agentskills.io，允许跨平台复用技能。

## 实现案例

### oh-my-openagent

[[oh-my-openagent]] 实现了完整的技能系统：
- 面向特定领域的调优系统指令
- 按需加载的独立 MCP 服务器（任务完成即销毁）
- 对 Agent 能力边界的强制约束
- 默认内置：playwright、git-master、frontend-ui-ux

### colleague-skill

[[colleague-skill]] 是 Agent Skills 的创新应用——将离职同事的知识和人格转化为可复用的 Skill：
- **Work Skill**：技术规范、工作流程、经验知识库
- **Persona**：五层性格结构（硬规则 → 身份 → 表达风格 → 决策模式 → 人际行为）
- **数据来源**：飞书、钉钉、Slack、微信、邮件、PDF 等
- **进化机制**：增量 merge、对话纠正、版本管理
- **应用场景**：知识传承、数字永生

### Everything Claude Code

[[Everything Claude Code]] (ECC) 实现了大规模技能生态系统：
- **181 个技能**：覆盖前端、后端、安全、测试等领域
- **持续学习**：从会话自动提取 Instincts → Skills
- **技能创建器**：从 Git 历史生成 SKILL.md 文件
- **跨平台**：Claude Code、OpenCode、Cursor、Gemini

### obsidian-skills

[[obsidian-skills]] 是 [[Steph Ango]] 创建的 Obsidian 专用技能集：
- `obsidian-markdown` — [[Obsidian Flavored Markdown]]
- `obsidian-bases` — [[Obsidian Bases]]
- `json-canvas` — [[JSON Canvas]]
- `obsidian-cli` — [[Obsidian CLI]]
- `defuddle` — [[Defuddle]] 网页提取

### Superpowers

[[Superpowers]] 是完整的软件开发工作流实现，由 [[Jesse Vincent]] 和 [[Prime Radiant]] 开发：
- 强制工作流（非建议性）
- 子代理驱动开发
- TDD、YAGNI、DRY 原则
- 两阶段审查（规范符合性 → 代码质量）
- 技能库：brainstorming、writing-plans、test-driven-development、systematic-debugging 等
- 支持平台：Claude Code、OpenCode、Cursor、Codex、Gemini CLI

与 Agent Skills 的关系：Superpowers 是完整工作流实现，Agent Skills 是通用技能标准规范。

## 与其他概念的关联

- 与 [[LLM Wiki 模式]] 的 Schema 层理念相通：都是通过结构化指令文件指导 Agent 行为
- 与 [[Memex]] 的关联路径不同：Skills 是"行为知识"，Wiki 是"领域知识"
- 与 [[oh-my-openagent]] 的技能系统理念相通，但 OmO 增加了按需 MCP 和边界约束
- 与 [[Context7]] 互补：Skills 定义 Agent "如何做"，Context7 提供最新的"参考资料"
- 与 [[Firecrawl]] 互补：Skills 定义 Agent "如何做"，Firecrawl 提供"网络数据来源"
- 与 [[持续学习]] 互补：持续学习自动生成 Skills
- 与 [[OpenSpec]] 互补：Skills 定义"如何做"，OpenSpec 定义变更的"做什么、为什么、怎么改"
- 与 [[OpenClaw]] 相似：OpenClaw 的技能注入是 Agent Skills 的具体实现，强调工作区 AGENTS.md/SOUL.md/TOOLS.md 注入

## 相关链接

- [[Anthropic]]
- [[Agent Skills - 摘要]]
- [[LLM Wiki 模式]]
- [[oh-my-openagent]]
- [[oh-my-openagent - 摘要]]
- [[colleague-skill]] — 创新应用：将同事知识转化为 Skill
- [[colleague-skill - 摘要]]
- [[Everything Claude Code]] — 181 个技能的生态系统
- [[obsidian-skills - 摘要]] — Obsidian 专用技能集
- [[知识蒸馏]]
- [[Persona]]
- [[数字永生]]
- [[Context7]] — 为 Agent 提供最新的库文档和代码示例
- [[Firecrawl]] — 为 Agent 提供网络数据采集能力
- [[持续学习]] — 从会话自动生成 Skills
- [[Superpowers]] — 完整工作流实现，Agent Skills 的深度实践
- [[Jesse Vincent]] — Superpowers 作者
- [[Prime Radiant]] — Superpowers 开发团队
- [[OpenClaw]] — 技能注入是 Agent Skills 的具体实现
- [[技能注入]] — OpenClaw 的工作区注入机制
- [[ClawHub]] — OpenClaw 的技能注册中心
