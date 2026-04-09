---
title: Gateway
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/openclaw openclaw.md]]"
tags:
  - 网关
  - 控制平面
  - WebSocket
  - 架构
type: concept
---

# Gateway

## 概念

**Gateway** 是 OpenClaw 的单一 WebSocket 控制平面，作为系统的核心枢纽，管理会话、通道、工具和事件。所有客户端和设备节点通过 Gateway WebSocket 连接和交互。

## 核心功能

- **会话管理**：main 会话用于直接聊天，群组隔离，激活模式
- **通道连接**：WhatsApp、Telegram、Slack 等 20+ 消息平台
- **工具执行**：浏览器控制、Canvas、节点操作、定时任务
- **事件处理**：webhooks、Gmail Pub/Sub 触发器

## 技术架构

```
消息平台 → Gateway（WebSocket 控制平面）→ 
         ws://127.0.0.1:18789
         ├─ Pi agent（RPC）
         ├─ CLI（openclaw …）
         ├─ WebChat UI
         ├─ macOS app
         └─ iOS / Android nodes
```

## 客户端类型

| 客户端 | 功能 |
|--------|------|
| CLI | 网关控制、代理对话、消息发送 |
| WebChat | 网页聊天界面，从 Gateway 直接服务 |
| macOS app | 菜单栏控制、语音唤醒、远程网关管理 |
| iOS/Android nodes | 设备配对、本地操作执行 |

## 远程访问

- **Tailscale Serve**：tailnet-only HTTPS，使用 Tailscale 身份认证
- **Tailscale Funnel**：公共 HTTPS，需要密码认证
- **SSH 隧道**：token/password 认证的远程连接

Gateway 可在小型 Linux 实例运行，客户端通过网络连接。

## 安全边界

- **绑定地址**：Serve/Funnel 启用时必须保持 `loopback`
- **认证模式**：password 或 Tailscale 身份
- **权限隔离**：主机执行 vs 设备本地执行分离

## 与其他架构对比

| 架构 | 控制平面 | Gateway 的位置 |
|------|----------|----------------|
| [[MCP]] | 服务器-客户端 | MCP 是工具协议，Gateway 是控制平面 |
| [[oh-my-openagent]] | 多模型协调 | OmO 强调协作，Gateway 强调单一用户 |

## 相关链接

- [[OpenClaw]] — 所属项目
- [[设备节点]] — 通过 Gateway 配对
- [[DM 配对]] — Gateway 安全机制
- [[OpenClaw - 摘要]] — 来源摘要
- [[MCP]] — 协议对比

## 外部链接

- Gateway 文档：https://docs.openclaw.ai/gateway
- 架构概述：https://docs.openclaw.ai/concepts/architecture