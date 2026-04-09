---
title: oh-my-openagent
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/code-yeongyu oh-my-openagent.md]]"
tags:
  - AI编程
  - 框架
  - OpenCode
  - 多智能体
type: entity
---

# oh-my-openagent

为 [[OpenCode]] 打造的多模型协作 AI 编程框架（原名 oh-my-opencode），支持 Claude、GPT、Kimi、Gemini 等模型并行工作。

## 基本信息

- **GitHub**: https://github.com/code-yeongyu/oh-my-openagent
- **原名**: oh-my-opencode
- **简称**: OmO
- **作者**: yeon_gyu_kim（韩国开发者）
- **开源**: 是

## 核心功能

### ultrawork

一键触发多智能体协作命令（`ultrawork` 或 `ulw`），任务完成前绝不停止。

### 自律军团（Discipline Agents）

- **Sisyphus**: 主指挥官（claude-opus-4-6 / kimi-k2.5 / glm-5）
- **Hephaestus**: 自主深度工作者（gpt-5.4）
- **Prometheus**: 战略规划师（claude-opus-4-6 / kimi-k2.5 / glm-5）

详见 [[多智能体协作]]

## 核心技术

- **Hashline**: 解决 [[Harness 问题]] 的哈希定位编辑工具
- **IntentGate**: 意图门，行动前先分析真实意图
- **技能系统**: 与 [[Agent Skills]] 理念相通的按需加载技能

## 兼容性

完全兼容 [[Claude Code]] 的 Hooks、命令、技能、MCP、插件。

## 定位

作者把 OpenCode 喻为 Debian/Arch，OmO 是开箱即用的 Ubuntu/Omarchy。

## 与 ECC 的对比

[[Everything Claude Code]] (ECC) 与 oh-my-openagent 都解决 MCP 全局加载问题：

| 维度 | oh-my-openagent | ECC |
|------|-----------------|-----|
| 目标平台 | OpenCode 为主 | Claude Code 为主 |
| MCP 管理 | 按需加载，任务完成销毁 | disabledMcpServers 禁用 |
| 多智能体 | 自律军团（Sisyphus/Hephaestus/Prometheus） | multi-* 命令系列 |
| 持续学习 | ✗ | ✓ Instincts → Skills |
| 安全审计 | ✗ | ✓ AgentShield |
| 内存持久化 | ✗ | ✓ 钩子驱动 |

## 相关链接

- [[oh-my-openagent - 摘要]]
- [[OpenCode]]
- [[Claude Code]]
- [[AmpCode]]
- [[Harness 问题]]
- [[多智能体协作]]
- [[Agent Skills]]
- [[AI 编程工具对比]]
- [[Everything Claude Code]] — 类似框架（Claude Code 生态）
- [[上下文管理]] — ECC 的 MCP 管理方案
- [[OpenClaw]] — OmO 是多模型协作框架，OpenClaw 是单用户本地助手