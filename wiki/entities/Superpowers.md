---
title: Superpowers
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/obra superpowers.md]]"
tags:
  - Agent
  - 技能系统
  - 工作流
  - 开源
type: entity
---

# Superpowers

为编码代理设计的技能框架和软件开发工作流系统，让代理"拥有超能力"。

## 概述

由 [[Jesse Vincent]] 和 [[Prime Radiant]] 团队开发的开源项目，提供完整的软件开发工作流。代理不会直接跳入编码，而是先退后一步，通过苏格拉底式提问提取需求规格。

## 核心特性

- **强制工作流** — 技能自动触发，非建议性
- **子代理驱动** — 可自主工作数小时不偏离计划
- **TDD 优先** — 强制 RED-GREEN-REFACTOR 循环
- **两阶段审查** — 先检查规范符合性，再检查代码质量

## 安装方式

### Claude Code

```bash
/plugin install superpowers@claude-plugins-official
```

### Cursor

```
/add-plugin superpowers
```

### OpenCode

```bash
# 获取并按说明安装
# https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.opencode/INSTALL.md
```

### Codex

```bash
# 获取并按说明安装
# https://raw.githubusercontent.com/obra/superpowers/refs/heads/main/.codex/INSTALL.md
```

## 与其他工具的关系

| 工具 | 关系 |
|------|------|
| [[Agent Skills]] | 互补：Superpowers 是完整工作流实现，Agent Skills 是通用标准 |
| [[oh-my-openagent]] | 类似：都强调子代理驱动和并行执行 |
| [[OpenSpec]] | 互补：都强调先规划后编码 |
| [[Claude Code]] | 原生支持，官方插件市场可用 |
| [[OpenCode]] | 支持手动安装 |
| [[Cursor]] | 插件市场支持 |

## 项目信息

- 仓库：https://github.com/obra/superpowers
- 许可证：MIT
- 社区：Discord、GitHub Issues

## 相关链接

- [[Agent Skills]]
- [[Jesse Vincent]]
- [[Prime Radiant]]
- [[Claude Code]]
- [[OpenCode]]
- [[Cursor]]
- [[oh-my-openagent]]
- [[OpenSpec]]
- [[规范驱动开发]]
- [[多智能体协作]]