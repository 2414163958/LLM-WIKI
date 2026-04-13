---
title: Hermes
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
tags: [ai-agent, memory, persistent]
type: entity
---

# Hermes

**Hermes** 是一个具有持久记忆的 AI 代理（AI Agent with persistent memory）。

由 [Nous Research](https://github.com/nousresearch/hermes-agent) 开发。

## 核心特性

- **持久记忆**：跨会话保持上下文和状态
- **自我认知**：Agent 了解自己的身份、记忆、技能、会话等信息
- **数据目录**：所有数据存储在 `~/.hermes/` 目录

## 监控工具

Hermes 配备了两款监控仪表盘：

1. [[hermes-hud]] — 终端用户界面（TUI）版本
2. [[hermes-hudui]] — 浏览器界面（Web UI）版本

两者独立读取同一数据目录，可同时使用。

## 监控维度

Hermes 的自我认知包括 13 个维度：身份、记忆、技能、会话、定时任务、项目、健康状况、成本、模式、纠正、实时聊天等。

详见 [[hermes-hudui - 摘要]]。

## 相关链接

- [[hermes-hud]] — TUI 监控工具
- [[hermes-hudui]] — Web UI 监控工具
- [[HUD UI]] — 平视显示器界面概念
- [[内存持久化]] — 跨会话保存上下文的技术
