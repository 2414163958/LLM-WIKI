---
title: HUD UI
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
tags: [ui, dashboard, monitoring]
type: concept
---

# HUD UI

**HUD**（Heads-Up Display，平视显示器）是一种界面设计模式，源自航空领域的仪表盘设计。

在软件中，HUD 指实时显示关键状态信息的仪表盘界面。

## 特点

- **实时性** — 数据实时更新（如通过 WebSocket 推送）
- **信息密度高** — 在单一视图中展示多维度状态
- **非侵入式** — 不干扰主要操作，作为辅助监控层
- **可视化** — 使用图表、颜色、进度条等视觉元素

## 应用场景

- **游戏** — 显示生命值、弹药、地图等
- **AI Agent 监控** — 如 [[Hermes]] 的 [[hermes-hudui]] 和 [[hermes-hud]]
- **系统监控** — CPU、内存、网络等实时状态
- **运维仪表盘** — 服务健康度、日志、告警

## 实现形式

| 形式 | 示例 |
|------|------|
| TUI（终端） | [[hermes-hud]] |
| Web UI（浏览器） | [[hermes-hudui]] |
| 桌面应用 | 各类系统监控工具 |
| 移动端 | 监控 App |

## 相关链接

- [[hermes-hudui]] — Hermes 的 Web UI 监控器
- [[hermes-hud]] — Hermes 的 TUI 监控器
- [[TUI]] — 终端用户界面
- [[Hermes]] — 具有持久记忆的 AI Agent
