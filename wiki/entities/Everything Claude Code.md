---
title: Everything Claude Code
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/affaan-m everything-claude-code.md]]"
tags: [Claude Code, 配置集合, 开源, 插件]
type: entity
---

# Everything Claude Code

Anthropic 黑客马拉松获胜者开发的 Claude Code 完整配置集合。

## 基本信息

| 属性 | 值 |
|------|-----|
| GitHub | affaan-m/everything-claude-code |
| Stars | 140K+ |
| Forks | 21K+ |
| 贡献者 | 170+ |
| 语言 | 12+ 语言系统 |
| 许可 | MIT |
| 简称 | ECC |

## 核心组件

| 类型 | 数量 | 说明 |
|------|------|------|
| 代理 | 47 | 专用子智能体（planner、reviewer、architect 等） |
| 技能 | 181 | 工作流定义与领域知识库 |
| 命令 | 79 | 传统斜杠命令兼容层 |
| 规则 | 5 语言 | TypeScript、Python、Go、Swift、PHP |
| 钩子 | 多个 | 会话生命周期、上下文管理 |

## 核心创新

### 持续学习系统

从会话自动提取模式 → Instincts → Skills

详见 [[持续学习]]

### 内存持久化

跨会话自动保存/加载上下文

详见 [[内存持久化]]

### 多智能体编排

`multi-*` 命令系列（需 ccg-workflow 运行时）

详见 [[多智能体协作]]

### AgentShield 安全审计

1282 项测试、98% 覆盖率

详见 [[AgentShield]]

## 跨平台支持

- Claude Code（主要目标）
- OpenCode
- Cursor
- Codex
- Antigravity
- Gemini

## 安装方式

```
/plugin marketplace add affaan-m/everything-claude-code
/plugin install ecc@ecc
./install.sh --profile full
```

## 作者背景

作者 @affaan-m 使用 Claude Code 构建 zenith.chat，赢得 Anthropic x Forum Ventures 黑客马拉松（2025 年 9 月）。

详见 [[affaan-m]]

## 与其他框架的对比

| 维度 | ECC | oh-my-openagent |
|------|-----|-----------------|
| 目标平台 | Claude Code 为主 | OpenCode 为主 |
| 持续学习 | ✓ Instincts → Skills | ✗ |
| 多智能体 | ✓ multi-* 命令 | ✓ 自律军团 |
| 安全审计 | ✓ AgentShield | ✗ |
| 上下文管理 | disabledMcpServers | 按需 MCP（销毁） |

两者都解决 MCP 全局加载问题，方案不同。

## 相关链接

- [[Everything Claude Code - 摘要]] — 详细摘要
- [[AgentShield]] — 安全审计工具
- [[affaan-m]] — 作者
- [[持续学习]] — 核心创新
- [[上下文管理]] — Token 优化
- [[内存持久化]] — 跨会话状态
- [[验证循环]] — 评估机制
- [[安全审计]] — 配置检查
- [[Claude Code]] — 主要目标平台
- [[Agent Skills]] — 技能系统理念
- [[oh-my-openagent]] — 类似框架
- [[MCP]] — MCP 配置管理