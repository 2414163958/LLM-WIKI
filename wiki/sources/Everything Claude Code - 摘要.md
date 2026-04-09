---
title: Everything Claude Code - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/affaan-m everything-claude-code.md]]"
tags: [Claude Code, 配置, 技能系统, 多智能体, 安全]
type: source-summary
---

# Everything Claude Code - 摘要

## 核心定位

Anthropic 黑客马拉松获胜者开发的 **Claude Code 完整配置集合**：140K+ stars，47 个代理、181 个技能、79 个命令。不止配置文件，而是一整套系统——技能体系、本能行为、记忆优化、持续学习、安全扫描。

## 技术架构

### 组件结构

| 目录 | 内容 | 数量 |
|------|------|------|
| agents/ | 专用子智能体 | 36 |
| skills/ | 工作流定义与领域知识库 | 181 |
| commands/ | 传统斜杠命令兼容层 | 79 |
| rules/ | 必须遵守的规范（按语言分类） | 5 语言 |
| hooks/ | 基于触发器的自动化逻辑 | 多个 |
| contexts/ | 动态注入的系统提示上下文 | 3 模式 |
| mcp-configs/ | MCP 服务端配置 | 多服务 |

### 核心创新

#### 持续学习系统（v2）

从会话中自动提取模式到可复用技能：

- **Instincts**：单次会话学到的直觉（带置信度评分）
- **Skills**：相关直觉聚类后的可复用工作流
- **命令**：`/instinct-status`、`/instinct-import`、`/instinct-export`、`/evolve`

#### 内存持久化

跨会话自动保存/加载上下文的钩子系统：

- 会话启动时加载上下文
- 会话结束时保存状态
- 上下文精简前状态保存

#### 多智能体编排

`multi-*` 命令系列（需 ccg-workflow 运行时）：

- `/multi-plan` — 多智能体任务拆解
- `/multi-execute` — 多智能体工作流编排
- `/multi-backend` — 后端多服务编排
- `/multi-frontend` — 前端多服务编排
- `/multi-workflow` — 通用多服务工作流

#### 安全审计（AgentShield）

1282 项测试、98% 覆盖率、102 条静态分析规则：

- 密钥检测（14 种模式）
- 权限审计
- 钩子注入分析
- MCP 服务风险评估
- 智能体配置审查
- `--opus` 模式：3 个 Opus 4.6 智能体红队/蓝队对抗推理

## 上下文管理警告

**关键警告**：启用太多 MCP 会将 200k 上下文窗口压缩到 70k。

经验法则：
- 配置 20-30 个 MCP
- 每个项目保持启用少于 10 个
- 活动工具少于 80 个

使用 `disabledMcpServers` 禁用未使用的服务。

## 跨平台支持

- **Windows/macOS/Linux** 全面支持
- **IDE 集成**：Cursor、OpenCode、Antigravity
- **包管理器检测**：npm、pnpm、yarn、bun 自动识别
- **钩子运行时**：Node.js 重写，最佳兼容性

## 安装方式

### 插件安装（推荐）

```
/plugin marketplace add affaan-m/everything-claude-code
/plugin install ecc@ecc
```

### 规则安装（必需）

```
./install.sh --profile full       # macOS/Linux
.\install.ps1 --profile full      # Windows
```

## 技能创建器

两种从仓库生成 Claude Code 技能的方法：

| 方式 | 功能 | 适用场景 |
|------|------|----------|
| `/skill-create` | 本地分析 git 历史 | 无需外部服务 |
| GitHub 应用 | 10k+ 提交、自动 PR、团队共享 | 高级功能 |

## 作者背景

- 黑客马拉松获胜者（Anthropic x Forum Ventures，2025 年 9 月）
- 使用 Claude Code 构建 zenith.chat
- 配置经多个生产应用实战测试

## 相关链接

- [[Everything Claude Code]] — 项目实体页面
- [[AgentShield]] — 安全审计工具
- [[持续学习]] — 从会话提取模式
- [[上下文管理]] — Token 优化策略
- [[内存持久化]] — 跨会话状态保存
- [[验证循环]] — 评估机制
- [[Claude Code]] — 目标平台
- [[Agent Skills]] — 技能系统理念
- [[oh-my-openagent]] — 类似的多智能体框架
- [[多智能体协作]] — 编排模式