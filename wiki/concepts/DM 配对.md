---
title: DM 配对
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/openclaw openclaw.md]]"
tags:
  - 安全
  - 配对机制
  - 私信控制
type: concept
---

# DM 配对

## 概念

**DM 配对** 是 OpenClaw 的安全机制，控制谁可以通过私信与助手交互。默认拒绝未知发送者，要求配对代码批准，防止未授权访问。

## 配对流程

```
未知发送者 → 收到配对代码 → 管理员批准 → 加入允许列表 → 可交互
```

批准命令：`openclaw pairing approve <channel> <code>`

## 配对策略

| 策略 | 行为 | 适用场景 |
|------|------|----------|
| `pairing`（默认） | 未知发送者收到配对代码，不处理消息 | 单用户私有助手 |
| `open` | 公开 DM，需要显式选择加入 | 公共服务、演示 |

## 配置方式

```json
{
  "channels": {
    "discord": {
      "dmPolicy": "pairing",
      "allowFrom": ["user-id-1", "user-id-2"]
    },
    "slack": {
      "dmPolicy": "pairing",
      "allowFrom": ["U123456"]
    }
  }
}
```

公开 DM 配置：
```json
{
  "channels": {
    "discord": {
      "dmPolicy": "open",
      "allowFrom": ["*"]
    }
  }
}
```

## 安全检查

运行 `openclaw doctor` 检查：

- 有风险的 DM 策略配置
- 缺失的权限控制
- 不安全的公开访问设置

## 沙箱隔离

对于群组/通道，可启用 Docker 沙箱：

```json
{
  "agents": {
    "defaults": {
      "sandbox": {
        "mode": "non-main"
      }
    }
  }
}
```

非主会话在沙箱中运行，bash 执行受限。

## 与其他安全机制的关系

| 机制 | 层级 | 作用 |
|------|------|------|
| DM 配对 | 通道层 | 控制谁可以发送消息 |
| 沙箱隔离 | 会话层 | 控制工具执行权限 |
| TCC 权限 | 设备层 | 控制 macOS 系统权限 |

三层协同形成完整安全模型。

## 相关链接

- [[OpenClaw]] — 所属项目
- [[Gateway]] — 安全边界
- [[安全审计]] — AI Agent 安全检查
- [[OpenClaw - 摘要]] — 来源摘要

## 外部链接

- 安全文档：https://docs.openclaw.ai/gateway/security
- Doctor 命令：https://docs.openclaw.ai/gateway/doctor