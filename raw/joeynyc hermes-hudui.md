---
title: "joeynyc/hermes-hudui: Web UI consciousness monitor for Hermes — the AI agent with persistent memory"
source: "https://github.com/joeynyc/hermes-hudui"
author:
published:
created: 2026-04-13
description: "Web UI consciousness monitor for Hermes — the AI agent with persistent memory - joeynyc/hermes-hudui"
tags:
  - "clippings"
---
## ☤ Hermes HUD — Web UI

A browser-based consciousness monitor for [Hermes](https://github.com/nousresearch/hermes-agent), the AI agent with persistent memory.  
一款基于浏览器的意识监测器，用于监测具有持久记忆的人工智能代理 [Hermes](https://github.com/nousresearch/hermes-agent) 。

Same data, same soul, same dashboard that made the [TUI version](https://github.com/joeynyc/hermes-hud) popular — now in your browser.  
同样的数据、同样的理念、同样的仪表盘，这些都让 [TUI 版本](https://github.com/joeynyc/hermes-hud) 广受欢迎——现在，您可以在浏览器中使用它们了。

[![[raw/assets/c07c0259dbf14519e18761f4f7a99661_MD5.png]]](https://github.com/joeynyc/hermes-hudui/blob/main/assets/dashboard-costs.png)

[![[raw/assets/d82ea12b29b1a02c7de6368bade7ddc5_MD5.png]]](https://github.com/joeynyc/hermes-hudui/blob/main/assets/profiles.png)

## Quick Start 快速入门

```
git clone https://github.com/joeynyc/hermes-hudui.git
cd hermes-hudui
./install.sh
hermes-hudui
```

Open [http://localhost:3001](http://localhost:3001/)  
打开 [http://localhost:3001](http://localhost:3001/)

**Requirements:** Python 3.11+, Node.js 18+, a running Hermes agent with data in `~/.hermes/`  
**要求：** Python 3.11+、Node.js 18+，以及一个正在运行且数据位于 `~/.hermes/` 目录下的 Hermes 代理。

On future runs:关于未来的运行：

```
source venv/bin/activate && hermes-hudui
```

## What's Inside 里面有什么

13 tabs covering everything your agent knows about itself — identity, memory, skills, sessions, cron jobs, projects, health, costs, patterns, corrections, and live chat.  
13 个标签页涵盖了您的代理所了解的一切——身份、记忆、技能、会话、定时任务、项目、健康状况、成本、模式、纠正和实时聊天。

Updates in real-time via WebSocket. No manual refresh needed.  
通过 WebSocket 实时更新，无需手动刷新。

## Themes 主题

Four themes switchable with `t`: **Neural Awakening** (cyan), **Blade Runner** (amber), **fsociety** (green), **Anime** (purple). Optional CRT scanlines.  
四种主题可通过 `t` 切换： **神经觉醒** （青色）、 **银翼杀手** （琥珀色）、 **fsociety** （绿色）、 **动漫** （紫色）。可选 CRT 扫描线效果。

## Keyboard Shortcuts 键盘快捷键

| Key 钥匙 | Action 行动 |
| --- | --- |
| `1` – `9`, `0`   `1` `0` `9` | Switch tabs 切换标签 |
| `t` | Theme picker 主题选择器 |
| `Ctrl+K` | Command palette 命令面板 |

## Relationship to the TUI 与 TUI 的关系

This is the browser companion to [hermes-hud](https://github.com/joeynyc/hermes-hud). Both read from the same `~/.hermes/` data directory independently — use either one, or both at the same time.  
这是 [hermes-hud](https://github.com/joeynyc/hermes-hud) 的浏览器配套程序。两者都独立地从同一个 `~/.hermes/` 数据目录读取数据——可以单独使用其中一个，也可以同时使用两个。

The Web UI is fully standalone and adds features the TUI doesn't have: dedicated Memory, Skills, and Sessions tabs; per-model token cost tracking; command palette; live chat; theme switcher.  
Web UI 是完全独立的，并添加了 TUI 没有的功能：专用的内存、技能和会话选项卡；每个模型的令牌成本跟踪；命令面板；实时聊天；主题切换器。

If you also have the TUI installed, you can enable it with `pip install hermes-hudui[tui]`.  
如果您也安装了 TUI，则可以使用 `pip install hermes-hudui[tui]` 启用它。

## Platform Support 平台支持

macOS · Linux · WSL

## License 执照

MIT — see [LICENSE](https://github.com/joeynyc/hermes-hudui/blob/main/LICENSE).  
MIT — 请参阅 [LICENSE](https://github.com/joeynyc/hermes-hudui/blob/main/LICENSE) 。

---

[![[raw/assets/b25a58fb0867326b32bb0f695f3f935a_MD5.svg]]](https://www.star-history.com/?repos=joeynyc%2Fhermes-hudui&type=date&logscale=&legend=top-left)