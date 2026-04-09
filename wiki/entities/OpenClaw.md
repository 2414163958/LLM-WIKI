---
title: OpenClaw
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/‍‬⁢‍‍‍﻿‬⁣‍⁢‬‌﻿‍‬⁡⁢‬⁢⁢⁡‍⁡​⁢​⁤‌⁢⁤﻿‌‍﻿​‌⁡⁣⁣​⁡⁣‍⁢‬​‌⁢‍OpenClaw 飞书官方插件使用指南（公开版） - 飞书云文档.md]]"
  - "[[raw/openclaw openclaw.md]]"
tags:
  - AI助手
  - 个人助理
  - 开源项目
  - 本地优先
type: entity
---

# OpenClaw

## 简介

**OpenClaw** 是一款运行在用户自己设备上的个人 AI 助手。开源项目，强调本地优先、速度快、始终在线的单人体验。支持 20+ 消息平台，可在 macOS、Linux、Windows（WSL2）运行。

## 核心特点

- **本地优先**：Gateway 运行在用户设备，数据不出本地
- **多渠道支持**：WhatsApp、Telegram、Slack、Discord、微信等 20+ 平台
- **语音交互**：macOS/iOS 语音唤醒，Android 连续语音模式
- **可视化工作空间**：Live Canvas（A2UI 驱动）
- **设备节点**：iOS/Android/macOS 作为执行节点，分布式操作

## 技术架构

```
消息平台 → Gateway（WebSocket 控制平面）→ 代理/客户端/节点
         ws://127.0.0.1:18789
```

- **Gateway**：单一 WebSocket 控制平面，管理会话、通道、工具、事件
- **代理运行时**：Pi agent RPC 模式，工具流式传输
- **设备节点**：通过 WebSocket 配对，执行设备本地操作

## 技能系统

- **工作区注入**：`AGENTS.md`、`SOUL.md`、`TOOLS.md` 注入代理上下文
- **技能路径**：`~/.openclaw/workspace/skills/<skill>/SKILL.md`
- **ClawHub**：技能注册中心，代理可自动搜索和添加技能

### 飞书官方插件

```bash
npx -y @larksuite/openclaw-lark install
```

授权后支持：消息、文档、多维表格、日历操作。可通过 `/feishu auth` 批量授权，并让 AI 学习新技能。

支持多机器人配置：不同飞书机器人可关联不同 Agent。

详细指南：[[OpenClaw 飞书插件 - 摘要]]

## 安全模型

- **DM 配对**：默认拒绝未知发送者，需要配对代码批准
- **沙箱隔离**：非主会话在 Docker 沙箱中运行
- **权限控制**：macOS TCC 权限通过 Gateway 协议管理

## 快速开始

```bash
npm install -g openclaw@latest
openclaw onboard --install-daemon
openclaw gateway --port 18789 --verbose
```

## 与其他工具对比

| 工具 | 定位 | OpenClaw 的位置 |
|------|------|-----------------|
| [[OpenCode]] | AI 编程 CLI | 编程助手，OpenClaw 是通用助手 |
| [[Claude Code]] | Anthropic 官方工具 | 商业产品，OpenClaw 是开源替代 |
| [[oh-my-openagent]] | 多模型协作框架 | 团队协作，OpenClaw 是单用户本地 |
| [[Agent Skills]] | Anthropic 技能系统 | 概念相似，OpenClaw 强调工作区注入 |

## 相关链接

- [[OpenClaw - 摘要]] — 来源摘要
- [[OpenClaw 飞书插件 - 摘要]] — 飞书插件配置指南
- [[Gateway]] — 网关控制平面
- [[技能注入]] — 工作区注入模式
- [[设备节点]] — 分布式执行架构
- [[DM 配对]] — 安全配对机制
- [[ClawHub]] — 技能注册中心
- [[Agent Skills]] — 概念关联
- [[上下文注入]] — 技术关联

## 外部链接

- 官网：https://openclaw.ai/
- 文档：https://docs.openclaw.ai/
- GitHub：https://github.com/openclaw/openclaw
- Discord：https://discord.gg/clawd