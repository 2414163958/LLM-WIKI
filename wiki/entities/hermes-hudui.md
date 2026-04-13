---
title: hermes-hudui
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
tags: [hermes, web-ui, monitoring, dashboard]
type: entity
---

# hermes-hudui

**hermes-hudui** 是 [[Hermes]] AI 代理的浏览器意识监测器。

作者：[joeynyc](https://github.com/joeynyc)

仓库：[joeynyc/hermes-hudui](https://github.com/joeynyc/hermes-hudui)

## 核心功能

提供 13 个标签页的仪表盘，实时显示 Hermes Agent 的自我认知状态：

- Identity、Memory、Skills、Sessions、Cron Jobs、Projects、Health、Costs、Patterns、Corrections、Live Chat

## 技术特点

- **WebSocket 实时更新** — 无需手动刷新
- **4 种主题** — Neural Awakening（青色）、Blade Runner（琥珀色）、fsociety（绿色）、Anime（紫色）
- **键盘快捷键** — 快速切换标签、主题、命令面板
- **可选 CRT 扫描线效果**

## 与 hermes-hud 的关系

[[hermes-hud]] 是 TUI 版本，hermes-hudui 是浏览器版本。

两者差异：

| 特性 | hermes-hud (TUI) | hermes-hudui (Web) |
|------|------------------|-------------------|
| 界面 | 终端 | 浏览器 |
| Memory 标签 | ❌ | ✅ |
| Skills 标签 | ❌ | ✅ |
| Sessions 标签 | ❌ | ✅ |
| 每模型成本追踪 | ❌ | ✅ |
| 命令面板 | ❌ | ✅ |
| 实时聊天 | ❌ | ✅ |
| 主题切换器 | ❌ | ✅ |

两者可同時使用，独立读取 `~/.hermes/` 数据。

## 安装

```bash
git clone https://github.com/joeynyc/hermes-hudui.git
cd hermes-hudui
./install.sh
hermes-hudui
```

可选 TUI 支持：`pip install hermes-hudui[tui]`

## 相关链接

- [[Hermes]] — 被监控的 AI Agent
- [[hermes-hud]] — TUI 版本
- [[HUD UI]] — 平视显示器概念
- [[TUI]] — 终端用户界面
