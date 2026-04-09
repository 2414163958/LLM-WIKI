---
title: OpenClaw - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - [[raw/openclaw openclaw.md]]
  - "[[raw/‍‬⁢‍‍‍﻿‬⁣‍⁢‬‌﻿‍‬⁡⁢‬⁢⁢⁡‍⁡​⁢​⁤‌⁢⁤﻿‌‍﻿​‌⁡⁣⁣​⁡⁣‍⁢‬​‌⁢‍OpenClaw 飞书官方插件使用指南（公开版） - 飞书云文档.md]]"
tags: [AI助手, 个人助理, 多渠道, Gateway, 开源项目]
type: source-summary
---

# OpenClaw - 摘要

## 核心定位

**OpenClaw** 是一款运行在用户自己设备上的个人 AI 助手。区别于云端服务，强调本地优先、速度快、始终在线的单人体验。网关只是控制平面，产品本身是助手。

## 关键架构

### Gateway 控制平面

- **单一 WebSocket 控制平面** (`ws://127.0.0.1:18789`)
- 管理会话、通道、工具和事件
- 客户端包括：CLI、WebChat、macOS 应用、iOS/Android 节点
- 支持 Tailscale Serve/Funnel 远程访问

### 多渠道支持

支持 20+ 消息平台：WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、iMessage（BlueBubbles）、IRC、Microsoft Teams、Matrix、飞书、LINE、Mattermost、Nextcloud Talk、Nostr、Synology Chat、Tlon、Twitch、Zalo、微信、WebChat。

**飞书官方插件**：
- 安装：`npx -y @larksuite/openclaw-lark install`
- 授权：飞书对话中 `/feishu auth` 批量授权
- 功能：消息、文档、多维表格、日历操作
- 多机器人：支持不同飞书机器人关联不同 Agent
- 详细指南：[[OpenClaw 飞书插件 - 摘要]]

### 设备节点

- **iOS 节点**：Canvas、语音唤醒、通话模式、相机、屏幕录制、Bonjour 设备配对
- **Android 节点**：连接选项卡、聊天会话、语音、Canvas、相机/屏幕录制、设备命令（通知/位置/短信/照片/联系人/日历）
- **macOS 节点模式**：system.run/notify + canvas/camera 权限控制

### 技能系统

- **工作区注入**：`~/.openclaw/workspace` 中的 `AGENTS.md`、`SOUL.md`、`TOOLS.md`
- **技能路径**：`~/.openclaw/workspace/skills/<skill>/SKILL.md`
- **ClawHub**：极简技能注册中心，代理可自动搜索和添加技能

## 安全模型

### DM 配对机制

- 默认 `dmPolicy="pairing"`：未知发送者收到配对代码，不处理消息
- 批准：`openclaw pairing approve <channel> <code>`
- 公开 DM 需要显式选择加入：`dmPolicy="open"` + `"*"` 在允许列表

### 沙箱隔离

- **默认**：工具在主机上运行，主会话完全访问
- **组/通道安全**：`agents.defaults.sandbox.mode: "non-main"` 为非主会话启用 Docker 沙箱
- **沙箱默认值**：允许 bash/process/read/write/edit/sessions_*；拒绝 browser/canvas/nodes/cron/discord/gateway

## 技术栈

- **运行时**：Node 24（推荐）或 Node 22.16+
- **安装**：`npm install -g openclaw@latest`
- **入门**：`openclaw onboard --install-daemon`
- **开发**：pnpm 构建，tsx 运行 TypeScript

## 特色功能

- **语音唤醒 + 通话模式**：macOS/iOS 唤醒词，Android 连续语音（ElevenLabs + 系统 TTS）
- **Live Canvas**：代理驱动的可视化工作空间（A2UI）
- **浏览器控制**：专用 Chrome/Chromium，CDP 控制
- **多代理路由**：入站通道/账户路由到隔离代理（工作区 + 会话）
- **会话工具**：sessions_list、sessions_history、sessions_send 实现代理间协调

## 与现有知识关联

| 关联页面 | 关系 |
|---------|------|
| [[Agent Skills]] | OpenClaw 的技能系统与 Agent Skills 概念相似，但强调工作区注入 |
| [[OpenCode]] | OpenCode 是 AI 编程 CLI，OpenClaw 是通用个人助手；可互补 |
| [[Claude Code]] | Claude Code 是 Anthropic 官方工具，OpenClaw 是第三方开源项目 |
| [[oh-my-openagent]] | OmO 是多模型协作框架，OpenClaw 是单用户本地助手 |
| [[MCP]] | OpenClaw 支持多渠道集成，与 MCP 工具协议有交集 |
| [[上下文注入]] | OpenClaw 的 AGENTS.md/SOUL.md 注入机制是上下文注入实例 |

## 配置要点

```json
{
  "agent": {
    "model": "<provider>/<model-id>"
  },
  "gateway": {
    "tailscale": {
      "mode": "serve" | "funnel"
    }
  },
  "agents": {
    "defaults": {
      "sandbox": {
        "mode": "non-main"
      }
    }
  }
}
```

## 开发通道

- **stable**：tagged releases，npm dist-tag `latest`
- **beta**：prerelease tags，npm dist-tag `beta`
- **dev**：main 分支头部，npm dist-tag `dev`
- 切换：`openclaw update --channel stable|beta|dev`

## 相关链接

- [[OpenClaw]] — 项目实体页面
- [[OpenClaw 飞书插件 - 摘要]] — 飞书插件配置指南
- [[Gateway]] — 网关控制平面概念
- [[技能注入]] — 工作区 AGENTS.md/SOUL.md 模式
- [[设备节点]] — 分布式执行架构
- [[DM 配对]] — 安全配对机制
- [[ClawHub]] — 技能注册中心