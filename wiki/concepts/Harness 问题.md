---
title: Harness 问题
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[code-yeongyu oh-my-openagent]]"
tags:
  - Agent
  - 工具链
  - 编辑
  - 错误率
type: concept
---

# Harness 问题

由 Can Bölük 在《The Harness Problem》一文中提出的问题，指出绝大多数 Agent 故障其实不是大模型变笨，而是编辑工具太烂。

## 问题本质

目前所有文件编辑工具都无法为模型提供稳定、可验证的行定位标识。它们全都依赖模型强行复写原文，一旦模型写错（很常见），用户就会怪罪大模型太蠢。

## 表现

- 缩进空格错乱
- 改错行
- 上下文理解错误导致修改失败

## 解决方案：Hashline

[[oh-my-openagent]] 受 oh-my-pi 启发，实现 **Hashline** 技术：

```
11#VK| function hello() {
22#XJ|   return "world";
33#MB| }
```

- 每行末尾绑定内容哈希值
- Agent 修改时必须引用目标行哈希
- 文件变化时哈希验证失败，直接驳回修改
- 0% 错误修改

## 效果

在 Grok Code Fast 1 上，仅更换 Hashline 编辑工具，修改成功率从 **6.7% 飙升至 68.3%**。

## 其他解决方案

### Everything Claude Code

[[Everything Claude Code]] 通过验证循环和 AgentShield 减少 Harness 问题的影响：
- 检查点机制：失败可回滚
- 持续评估：每步验证修改正确性
- 安全审计：检测危险配置

### 模型选型

使用更强的模型（如 Claude Opus）可降低 Harness 问题发生率。

## 来源

- [The Harness Problem](https://blog.can.ac/2026/02/12/the-harness-problem/) by Can Bölük
- [oh-my-pi](https://github.com/can1357/oh-my-pi) 启发

## 相关链接

- [[oh-my-openagent]]
- [[oh-my-openagent - 摘要]]
- [[Everything Claude Code]] — 验证循环缓解方案
- [[验证循环]] — ECC 的评估机制
- [[AgentShield]] — ECC 的安全审计