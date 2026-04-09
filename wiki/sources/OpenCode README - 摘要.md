---
title: OpenCode README - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/anomalyco opencode.md]]"
tags:
  - AI编程
  - CLI
  - 开源
type: source-summary
---

# OpenCode README - 摘要

开源 AI 编程 CLI 工具 OpenCode 的官方 README 摘要。

## 核心定位

- **100% 开源**：完全开源，代码可审计
- **Provider-agnostic**：不绑定特定 LLM 提供商，支持 OpenCode Zen、Claude、OpenAI、Google 甚至本地模型
- **聚焦 TUI**：终端界面优先，由 Neovim 爱好者和 [terminal.shop](https://terminal.shop/) 创建者打造
- **客户端/服务器架构**：可本地运行，远程控制，TUI 只是众多潜在客户端之一

## 安装方式

### 命令行安装

```bash
# 直接安装
curl -fsSL https://opencode.ai/install | bash

# 包管理器
npm i -g opencode-ai@latest
scoop install opencode             # Windows
brew install anomalyco/tap/opencode # macOS/Linux（推荐）
brew install opencode              # macOS/Linux（官方 brew formula）
sudo pacman -S opencode            # Arch Linux
paru -S opencode-bin               # Arch Linux (AUR)
mise use -g opencode               # 任意系统
nix run nixpkgs#opencode           # Nix
```

### 桌面应用（BETA）

从 [发布页](https://github.com/anomalyco/opencode/releases) 或 [opencode.ai/download](https://opencode.ai/download) 下载：

- macOS (Apple Silicon/Intel)
- Windows
- Linux (.deb/.rpm/AppImage)

```bash
# macOS Homebrew Cask
brew install --cask opencode-desktop
# Windows Scoop
scoop bucket add extras; scoop install extras/opencode-desktop
```

### 安装目录优先级

1. `$OPENCODE_INSTALL_DIR` - 自定义安装目录
2. `$XDG_BIN_DIR` - XDG 基础目录规范路径
3. `$HOME/bin` - 用户二进制目录
4. `$HOME/.opencode/bin` - 默认备用路径

## 内置 Agent

用 `Tab` 键快速切换：

| Agent | 模式 | 权限 | 用途 |
|-------|------|------|------|
| **build** | 默认 | 完整权限 | 开发工作 |
| **plan** | 只读 | 无写权限 | 代码分析、探索未知代码库、规划改动 |
| **general** | 子 Agent | — | 复杂搜索和多步任务（内部使用，可 `@general` 调用） |

### plan Agent 特性

- 默认拒绝修改文件
- 运行 bash 命令前会询问
- 适合探索不熟悉的代码库

## 与 Claude Code 的差异

| 特性 | OpenCode | Claude Code |
|------|----------|-------------|
| 开源 | 100% 开源 | 闭源 |
| 提供商绑定 | 不绑定，支持多种模型 | 仅 Claude |
| LSP 支持 | 内置 | ? |
| 界面 | 聚焦 TUI | ? |
| 架构 | 客户端/服务器 | ? |

## 技术亮点

1. **内置 LSP 支持**：无需外部配置，开箱即用的语言服务器协议集成
2. **TUI 优先**：终端用户界面，追求终端体验的极致
3. **客户端/服务器架构**：本地运行 + 远程控制，TUI 只是众多客户端之一
4. **模型灵活性**：模型迭代缩小差异、降低成本，provider-agnostic 策略

## 社区

- [飞书](https://applink.feishu.cn/client/chat/chatter/add_by_link?link_token=738j8655-cd59-4633-a30a-1124e0096789)
- [X.com](https://x.com/opencode)

## 相关链接

- [[OpenCode]] — 实体页面
- [[Claude Code]] — 对比参考
- [[AI 编程工具对比]] — 工具对比
- [[LSP]] — 语言服务器协议
- [[TUI]] — 终端用户界面