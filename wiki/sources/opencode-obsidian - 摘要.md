---
title: opencode-obsidian - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/mtymek opencode-obsidian.md]]"
tags: [插件, Obsidian, OpenCode]
type: source-summary
---

# opencode-obsidian - 摘要

将 [[OpenCode]] AI 助手直接嵌入 Obsidian 侧边栏的第三方插件。

## 核心价值

- 在 Obsidian 内直接使用 OpenCode，无需切换应用
- 使用 OpenCode 原生 Web 视图，而非实现自定义聊天 UI
- 支持笔记总结、内容编辑、知识库查询、提纲生成等场景

## 技术实现

- 使用 OpenCode 的 Web 视图嵌入 Obsidian 窗口
- 通过 Node.js 子进程运行 OpenCode CLI
- 需要配置 `--cors app://obsidian.md` 允许 Obsidian 嵌入

## 依赖要求

- **仅限桌面端**：使用 Node.js 子进程
- [[OpenCode]] CLI 已安装
- Bun 运行时

## 安装方式

通过 [[BRAT]] 插件安装：
1. 安装 BRAT 插件
2. 添加 Beta 插件：`mtymek/opencode-obsidian`
3. 启用 OpenCode 插件

## 主要功能

### 自定义命令模式

支持自定义 OpenCode 启动方式，例如：
- 添加额外 CLI 标志
- 使用包装脚本
- 通过容器或虚拟环境运行

### 上下文注入（实验性）

自动向 OpenCode 实例注入上下文：
- 打开的笔记列表
- 当前选中的文本

限制：从 OC 界面创建新会话时无法使用。

## Windows 故障排除

Electron/Obsidian 在 Windows 上无法完全继承 PATH 环境变量，需手动配置 opencode.cmd 完整路径：
```
C:\Users\{username}\AppData\Roaming\npm\opencode.cmd
```

## 相关链接

- [[OpenCode]]
- [[Obsidian]]
- [[BRAT]]
- [[上下文注入]]