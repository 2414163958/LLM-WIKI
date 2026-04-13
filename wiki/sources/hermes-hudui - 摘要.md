---
title: hermes-hudui - 摘要
created: 2026-04-13
updated: 2026-04-13
sources:
  - [[raw/joeynyc hermes-hudui.md]]
tags: [hermes, hud, web-ui, monitoring]
type: source-summary
---

# hermes-hudui - 摘要

来源：[joeynyc/hermes-hudui](https://github.com/joeynyc/hermes-hudui)

## 项目定位

**Hermes HUD UI** 是一个基于浏览器的意识监测器，用于监测具有持久记忆的 AI 代理 [[Hermes]]。

与 [[TUI]] 版本 [[hermes-hud]] 相比，它提供相同的仪表盘和数据，但运行在浏览器中。

## 核心功能

13 个标签页涵盖 Agent 的所有自我认知：

1. **Identity** — 身份
2. **Memory** — 记忆
3. **Skills** — 技能
4. **Sessions** — 会话
5. **Cron Jobs** — 定时任务
6. **Projects** — 项目
7. **Health** — 健康状况
8. **Costs** — 成本（按模型追踪 token 消耗）
9. **Patterns** — 模式
10. **Corrections** — 纠正
11. **Live Chat** — 实时聊天

## 技术特点

- **实时更新**：通过 WebSocket 推送，无需手动刷新
- **主题系统**：4 种主题可通过 `t` 键切换
  - Neural Awakening（青色）
  - Blade Runner（琥珀色）
  - fsociety（绿色）
  - Anime（紫色）
- **可选 CRT 扫描线效果**
- **键盘快捷键**：
  - `1`–`9`, `0` — 切换标签
  - `t` — 主题选择器
  - `Ctrl+K` — 命令面板

## 快速入门

```bash
git clone https://github.com/joeynyc/hermes-hudui.git
cd hermes-hudui
./install.sh
hermes-hudui
```

打开 http://localhost:3001/

**要求**：
- Python 3.11+
- Node.js 18+
- 正在运行的 Hermes Agent（数据位于 `~/.hermes/`）

## 与 TUI 的关系

- 两者独立读取同一 `~/.hermes/` 数据目录
- 可单独使用或同时使用
- Web UI 是 TUI 的浏览器伴侣，功能完全独立
- Web UI 独有功能：专用 Memory/Skills/Sessions 标签、每模型成本追踪、命令面板、实时聊天、主题切换器

如需同时使用 TUI：`pip install hermes-hudui[tui]`

## 平台支持

macOS · Linux · WSL

## 相关链接

- [[Hermes]] — Hermes AI Agent
- [[hermes-hud]] — TUI 版本
- [[hermes-hudui]] — Web UI 项目
- [[TUI]] — 终端用户界面概念
- [[HUD UI]] — 平视显示器界面概念
