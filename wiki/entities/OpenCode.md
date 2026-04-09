---
title: OpenCode
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/anomalyco opencode.md]]"
  - "[[code-yeongyu oh-my-openagent]]"
  - "[[raw/mtymek opencode-obsidian.md]]"
tags:
  - AI编程
  - CLI
  - 开源
  - TUI
type: entity
---

# OpenCode

开源的 AI 编程 CLI 工具，被 [[oh-my-openagent]] 作者认为是市面上最好的代码 Agent。

## 基本信息

- **定位**: AI 编程 CLI 工具（类似 [[Claude Code]]）
- **开源**: 100% 开源
- **界面**: 聚焦 [[TUI]]（终端用户界面）
- **架构**: 客户端/服务器架构
- **提供商**: Provider-agnostic（不绑定特定 LLM）
- **插件系统**: 支持插件（如 oh-my-openagent）

## 核心特性

- [[TUI]] 界面，追求终端体验极致
- 不绑定特定提供商，支持多种模型
- 内置 [[LSP]] 支持
- 插件系统
- Hook 流水线
- 技能系统（Skills）
- [[MCP]] 服务器集成
- 客户端/服务器架构（可本地运行 + 远程控制）

## 与 oh-my-openagent 的关系

- oh-my-openagent 是 OpenCode 的插件/增强框架
- 作者测试所有代码 Agent 后认为 OpenCode 赖了
- OmO 把 OpenCode 喻为 Debian/Arch，OmO 是 Ubuntu/Omarchy

## 内置 Agent

用 `Tab` 键快速切换：

| Agent | 模式 | 权限 | 用途 |
|-------|------|------|------|
| **build** | 默认 | 完整权限 | 开发工作 |
| **plan** | 只读 | 无写权限 | 代码分析、探索未知代码库、规划改动 |
| **general** | 子 Agent | — | 复杂搜索和多步任务（`@general` 调用） |

### plan Agent 特性

- 默认拒绝修改文件
- 运行 bash 命令前会询问
- 适合探索不熟悉的代码库

## 安装方式

```bash
# 直接安装
curl -fsSL https://opencode.ai/install | bash

# 包管理器
npm i -g opencode-ai@latest
brew install anomalyco/tap/opencode  # macOS/Linux（推荐）
scoop install opencode              # Windows
```

桌面应用（BETA）可从 [发布页](https://github.com/anomalyco/opencode/releases) 下载。

## 社区生态

- Discord 社区活跃
- 被 Google、Microsoft、Indent 等公司专业开发人员使用
- [飞书社区](https://applink.feishu.cn/client/chat/chatter/add_by_link?link_token=738j8655-cd59-4633-a30a-1124e0096789)
- [X.com](https://x.com/opencode)

## Obsidian 插件

[opencode-obsidian](https://github.com/mtymek/opencode-obsidian) 是第三方插件，将 OpenCode 嵌入 Obsidian 侧边栏：

- 使用 OpenCode Web 视图，无需自定义聊天 UI
- 支持 [[上下文注入]]（实验性）：自动注入打开的笔记和选中文本
- 通过 [[BRAT]] 安装

参见 [[opencode-obsidian - 摘要]]

## Anthropic 事件

Anthropic 曾屏蔽 OpenCode，导致 [[oh-my-openagent]] 作者将 Hephaestus 命名为"正牌工匠（The Legitimate Craftsman）"作为讽刺。

## 相关链接

- [[oh-my-openagent]] — OpenCode 的插件/增强框架
- [[Claude Code]] — Anthropic 官方 AI 编程 CLI
- [[AmpCode]] — AI 编程工具
- [[AI 编程工具对比]] — 工具对比分析
- [[OpenCode README - 摘要]] — 官方 README 摘要
- [[opencode-obsidian - 摘要]] — Obsidian 插件
- [[OpenClaw]] — OpenCode 是编程 CLI，OpenClaw 是通用个人助手，可互补
- [[LSP]] — 语言服务器协议
- [[TUI]] — 终端用户界面