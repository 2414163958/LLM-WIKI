---
title: Hermes
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
  - [[raw/NousResearch hermes-agent.md]]
tags: [ai-agent, memory, persistent, self-learning]
type: entity
---

# Hermes

**Hermes** 是由 Nous Research 开发的自学习型 AI 智能体。它是唯一一款内置学习循环的智能体，能从经验中积累技能并在使用过程中自我改进。

## 核心特性

- **闭环学习系统**：智能体管理的记忆，定期提示；复杂任务后自主创建技能；技能自我提升；FTS5 会话搜索 + LLM 摘要实现跨会话回忆
- **持久记忆**：跨会话保持上下文和状态
- **自我认知**：Agent 了解自己的身份、记忆、技能、会话等信息
- **多平台支持**：Telegram、Discord、Slack、WhatsApp、Signal、Email；支持本地、Docker、SSH、Daytona、Singularity、Modal 六种终端后端
- **模型灵活性**：支持 Nous Portal、OpenRouter（200+ 模型）、z.ai/GLM、Kimi/Moonshot、MiniMax、OpenAI 等，可随时切换
- **数据目录**：所有数据存储在 `~/.hermes/` 目录

## 监控工具

Hermes 配备了两款监控仪表盘：

1. [[hermes-hud]] — 终端用户界面（TUI）版本
2. [[hermes-hudui]] — 浏览器界面（Web UI）版本

两者独立读取同一数据目录，可同时使用。

## 监控维度

Hermes 的自我认知包括 13 个维度：身份、记忆、技能、会话、定时任务、项目、健康状况、成本、模式、纠正、实时聊天等。

详见 [[hermes-hudui - 摘要]]。

## 快速安装

```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

支持 Linux、macOS、WSL2、Android (Termux)。Windows 需安装 WSL2。

## 核心命令

| 命令 | 说明 |
|------|------|
| `hermes` | 启动交互式 CLI |
| `hermes model` | 选择 LLM 提供商和模型 |
| `hermes tools` | 配置启用的工具 |
| `hermes gateway` | 启动消息网关 |
| `hermes setup` | 运行完整设置向导 |
| `hermes claw migrate` | 从 [[OpenClaw]] 迁移 |

详见 [[NousResearch hermes-agent - 摘要]]。

## 相关链接

- [[hermes-hud]] — TUI 监控工具
- [[hermes-hudui]] — Web UI 监控工具
- [[HUD UI]] — 平视显示器界面概念
- [[内存持久化]] — 跨会话保存上下文的技术
- [[NousResearch hermes-agent - 摘要]] — Hermes Agent 来源摘要
- [[OpenClaw]] — 可从 OpenClaw 迁移
