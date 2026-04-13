---
title: NousResearch/hermes-agent - 摘要
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/NousResearch hermes-agent.md]]
tags: [AI 智能体，自学习，自动化]
type: source-summary
---

# NousResearch/hermes-agent - 摘要

**Hermes Agent** 是由 Nous Research 开发的自学习型 AI 智能体。它是唯一一款内置学习循环的智能体，能从经验中积累技能并在使用过程中自我改进。

## 核心特性

### 1. 闭环学习系统
- 智能体管理的记忆，定期进行提示
- 复杂任务完成后自主创建技能
- 技能在使用过程中自我提升
- FTS5 会话搜索 + LLM 摘要实现跨会话回忆
- Honcho 辩证用户建模
- 兼容 [agentskills.io](https://agentskills.io/) 开放标准

### 2. 多平台支持
- **消息平台**: Telegram, Discord, Slack, WhatsApp, Signal, Email
- **终端后端**: 本地、Docker、SSH、Daytona、Singularity、Modal
- **无服务器部署**: Daytona 和 Modal 提供持久化，空闲时休眠，按需唤醒

### 3. 模型灵活性
支持多种 LLM 提供商，可随时切换：
- Nous Portal
- OpenRouter (200+ 模型)
- z.ai/GLM
- Kimi/Moonshot
- MiniMax
- OpenAI
- 自定义端点

### 4. 主要功能
- 完整的 TUI 界面（多行编辑、斜杠命令自动完成、对话历史）
- 内置定时任务调度器（cron）
- 子代理系统（并行工作流）
- 语音备忘录转录
- 40+ 工具支持
- MCP 集成

### 5. 研究功能
- 批量轨迹生成
- Atropos RL 环境
- 轨迹压缩（用于训练下一代工具调用模型）

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
| `hermes claw migrate` | 从 OpenClaw 迁移 |

## 从 OpenClaw 迁移

Hermes 可自动导入 OpenClaw 的设置、记忆、技能和 API 密钥：

```bash
hermes claw migrate              # 交互式迁移
hermes claw migrate --dry-run    # 预览迁移内容
hermes claw migrate --preset user-data   # 不含密钥的迁移
```

## 相关链接

- 官网文档：https://hermes-agent.nousresearch.com/docs/
- GitHub: https://github.com/NousResearch/hermes-agent
- Nous Research: https://nousresearch.com/
- Skills Hub: https://agentskills.io/
- Discord 社区：https://discord.gg/NousResearch
