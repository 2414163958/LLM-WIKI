---
title: AI 编程工具对比
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/code-yeongyu oh-my-openagent.md]]"
tags:
  - AI编程
  - 对比
  - 工具
type: comparison
---

# AI 编程工具对比

主流 AI 编程工具的特性对比与定位分析。

## 工具概览

| 工具 | 类型 | 开源 | 提供商 | 定位 |
|------|------|------|--------|------|
| [[OpenCode]] | CLI/TUI | 100% | Provider-agnostic | 基础框架（类比 Debian/Arch） |
| [[oh-my-openagent]] | CLI 插件 | 是 | 多模型 | 开箱即用增强（类比 Ubuntu/Omarchy） |
| [[Claude Code]] | CLI | 否 | Anthropic | Anthropic 官方 AI 编程工具 |
| [[AmpCode]] | CLI | 否 | ? | AI 编程工具 |
| [[Cursor]] | IDE | 否 | 多模型 | VS Code 基础的 AI IDE |
| [[OpenClaw]] | CLI | 是 | 多模型 | 通用个人助手（非编程专用） |

## 核心对比

### 多模型支持

| 工具 | 多模型 | 模型选择 |
|------|--------|----------|
| OpenCode | ✓ | OpenCode Zen、Claude、OpenAI、Google、本地模型 |
| oh-my-openagent | ✓✓ | Claude、GPT、Kimi、Gemini 并行协作 |
| Claude Code | ✗ | 仅 Claude |
| AmpCode | ? | 未知 |
| Cursor | ✓ | 多种模型 |

### 技术架构

| 工具 | LSP 支持 | TUI | 客户端/服务器 | 内置 Agent |
|------|----------|-----|---------------|------------|
| OpenCode | ✓ 内置 | ✓ 聚焦 | ✓ | build/plan/general |
| oh-my-openagent | ✓ | ✓ | ? | ? |
| Claude Code | ? | ? | ? | ? |
| Cursor | ✓（VS Code） | ✗ | ✗ | ✗ |

### 技能系统

| 工具 | 技能系统 | 按需 MCP |
|------|----------|----------|
| OpenCode | ✓ | ? |
| oh-my-openagent | ✓✓ | ✓（任务完成即销毁） |
| Claude Code | ✓ | ✗（全局 MCP） |
| AmpCode | ? | ? |
| Cursor | ? | ? |

### 编辑工具

| 工具 | 哈希定位 | Harness 问题 |
|------|----------|--------------|
| OpenCode | ? | 存在 |
| oh-my-openagent | ✓（Hashline） | ✓ 解决 |
| Claude Code | ✗ | 存在 |
| AmpCode | ? | ? |
| Cursor | ? | 存在 |

### 多智能体协作

| 工具 | 多智能体 | 并行执行 |
|------|----------|----------|
| OpenCode | ✓ | ? |
| oh-my-openagent | ✓✓ | ✓（5+ 并行） |
| Claude Code | ✗ | ✗ |
| AmpCode | ? | ? |
| Cursor | ? | ? |

### 兼容性

| 工具 | 兼容 Claude Code 配置 |
|------|----------------------|
| OpenCode | ? |
| oh-my-openagent | ✓ 完全兼容 |
| Claude Code | — |
| AmpCode | ? |
| Cursor | ? |

## oh-my-openagent 的优势

### 相比 Claude Code

- 多模型协作（不依赖单一 Claude）
- 解决 Harness 问题（Hashline）
- 按需 MCP（不撑爆 Context）
- 更激进的并行策略
- 完全兼容 Claude Code 配置

**作者观点**："仅仅使用 Kimi K2.5 + GPT-5.4 就足以碾压原版的 Claude Code。完全不需要配置。"

### 相比 Cursor

- 开源免费
- CLI 更轻量
- 多智能体协作
- 用户评价："因为它，我取消了 Cursor 的订阅"

### 相比 OpenCode

- OmO 是 OpenCode 的插件/增强
- OpenCode 是底层框架（类比 Debian/Arch）
- OmO 是开箱即用版（类比 Ubuntu/Omarchy）
- OmO 做了所有脏活累活（配置、调优）

## 用户场景对比

| 场景 | 推荐工具 |
|------|----------|
| 快速上手、开箱即用 | oh-my-openagent |
| 深度定制、底层控制 | OpenCode |
| Anthropic 生态、Claude 优先 | Claude Code |
| IDE 集成、VS Code 用户 | Cursor |
| 通用助手、多渠道消息 | OpenClaw |

## 成本对比

| 工具 | 成本 |
|------|------|
| OpenCode | 免费（需 API Token） |
| oh-my-openagent | 免费（推荐 ChatGPT/Kimi/GLM 订阅） |
| Claude Code | Claude API/订阅 |
| AmpCode | 未知 |
| Cursor | 付费订阅 |

## 技能框架与工作流工具

[[Superpowers]] 是完整的工作流框架，可与上述所有工具配合使用：

| 工具 | 类型 | 定位 |
|------|------|------|
| [[Superpowers]] | 技能框架 + 工作流 | TDD、子代理驱动、强制工作流 |
| [[OpenSpec]] | 工作流框架 | 规范驱动开发，"先规范后代码" |
| [Spec Kit](https://github.com/github/spec-kit) | 工作流框架 | 重量、阶段门控严格 |
| [Kiro](https://kiro.dev/) | IDE + 工作流 | 绑定 IDE、仅 Claude 模型 |

Superpowers 的平台支持：

| 平台 | Superpowers 支持 |
|------|-----------------|
| [[Claude Code]] | ✓ 官方插件市场 |
| [[Cursor]] | ✓ 插件市场 |
| [[OpenCode]] | ✓ 手动安装 |
| Codex | ✓ 手动安装 |
| Gemini CLI | ✓ 扩展安装 |

## 相关链接

- [[Superpowers]] — 技能框架 + TDD 工作流
- [[Jesse Vincent]] — Superpowers 作者
- [[Prime Radiant]] — Superpowers 开发团队
- [[YAGNI]] — You Aren't Gonna Need It
- [[DRY]] — Don't Repeat Yourself