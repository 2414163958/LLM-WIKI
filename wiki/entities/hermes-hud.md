---
title: hermes-hud
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
tags: [hermes, tui, monitoring, dashboard]
type: entity
---

# hermes-hud

**hermes-hud** 是 [[Hermes]] AI 代理的终端（TUI）意识监测器。

作者：[joeynyc](https://github.com/joeynyc)

仓库：[joeynyc/hermes-hud](https://github.com/joeynyc/hermes-hud)

## 核心功能

在终端中显示 Hermes Agent 的自我认知状态仪表盘。

## 与 hermes-hudui 的关系

[[hermes-hudui]] 是浏览器版本，功能更丰富。

hermes-hudui 独有而 hermes-hud 没有的功能：

- 专用 Memory、Skills、Sessions 标签页
- 每模型 token 成本追踪
- 命令面板
- 实时聊天
- 主题切换器

两者可同時使用，独立读取 `~/.hermes/` 数据。

## 相关链接

- [[Hermes]] — 被监控的 AI Agent
- [[hermes-hudui]] — Web UI 版本
- [[TUI]] — 终端用户界面
- [[HUD UI]] — 平视显示器概念
