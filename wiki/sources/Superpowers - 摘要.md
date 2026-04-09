---
title: Superpowers - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/obra superpowers.md]]"
tags:
  - Agent
  - 技能系统
  - 工作流
  - TDD
type: source-summary
---

# Superpowers - 摘要

为编码代理设计的技能框架和软件开发工作流系统，由 [[Jesse Vincent]] 和 [[Prime Radiant]] 团队开发。

## 核心理念

代理在编写代码前**先退后一步**，询问用户真正想要什么，通过苏格拉底式提问提取需求规格，而非直接跳入编码。

## 基本工作流程

1. **brainstorming** — 编码前激活，通过提问完善想法，探索方案，分段展示设计供验证
2. **using-git-worktrees** — 设计批准后激活，创建隔离工作区
3. **writing-plans** — 将工作分解为 2-5 分钟的小任务，包含精确路径和验证步骤
4. **subagent-driven-development** — 为每个任务派遣子代理，两阶段审查
5. **test-driven-development** — 强制执行 RED-GREEN-REFACTOR 循环
6. **requesting-code-review** — 任务间隙审查，按严重程度报告问题
7. **finishing-a-development-branch** — 验证测试，提供合并/PR 选项

## 技能库

### 测试

- **test-driven-development** — RED-GREEN-REFACTOR 循环

### 调试

- **systematic-debugging** — 四阶段根本原因分析
- **verification-before-completion** — 确保问题真正解决

### 协作

- **brainstorming** — 苏格拉底式设计改进
- **writing-plans** — 详细实施计划
- **executing-plans** — 带检查点的批量执行
- **dispatching-parallel-agents** — 并发子代理工作流
- **requesting-code-review** — 审查前检查清单
- **receiving-code-review** — 回复反馈
- **using-git-worktrees** — 并行开发分支
- **finishing-a-development-branch** — 合并/PR 决策流程
- **subagent-driven-development** — 快速迭代，两阶段审查

### 元

- **writing-skills** — 遵循最佳实践创建新技能
- **using-superpowers** — 技能系统简介

## 设计哲学

- **Test-Driven Development** — 始终先编写测试
- **Systematic over ad-hoc** — 流程优于猜测
- **Complexity reduction** — 简洁为首要目标
- **Evidence over claims** — 宣布成功前先验证

## 支持平台

| 平台 | 安装方式 |
|------|----------|
| Claude Code | 官方插件市场 |
| Cursor | 插件市场 |
| OpenCode | 手动安装 |
| Codex | 手动安装 |
| GitHub Copilot CLI | 插件市场 |
| Gemini CLI | 扩展安装 |

## 与其他系统的关联

- 与 [[Agent Skills]] 互补：Superpowers 是完整工作流，Agent Skills 是通用技能标准
- 与 [[oh-my-openagent]] 类似：都强调子代理驱动和并行执行
- 与 [[OpenSpec]] 互补：都强调先规划后编码
- 与 [[规范驱动开发]] 理念相通：结构化变更、灵活迭代

## 社区

- Discord: https://discord.gg/35wsABTejz
- Issues: https://github.com/obra/superpowers/issues

## 相关链接

- [[Agent Skills]]
- [[Jesse Vincent]]
- [[Prime Radiant]]
- [[oh-my-openagent]]
- [[OpenSpec]]
- [[规范驱动开发]]
- [[多智能体协作]]