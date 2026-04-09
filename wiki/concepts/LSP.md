---
title: LSP
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/anomalyco opencode.md]]"
  - "[[code-yeongyu oh-my-openagent]]"
tags:
  - 协议
  - 开发工具
  - AI编程
type: concept
---

# LSP

Language Server Protocol（语言服务器协议），微软开发的编辑器与语言服务通信协议。

## 定义

LSP 将编程语言支持（自动补全、跳转定义、查找引用、重构等）从编辑器中分离，作为独立服务运行。

## 核心能力

- **自动补全**：代码补全建议
- **跳转定义**：Go to Definition
- **查找引用**：Find All References
- **重命名**：工作区级符号重命名
- **诊断**：语法错误、类型错误检测
- **悬停提示**：Hover 文档

## 在 AI 编程工具中的应用

### OpenCode

- **内置 LSP 支持**：无需外部配置，开箱即用
- 提供 IDE 级精度的代码理解能力

### oh-my-openagent

- **LSP + AST-Grep + Tmux + MCP 深度集成**
- 工作区级重命名
- 构建前诊断
- IDE 级精度

## 架构优势

```
编辑器/IDE  <--LSP-->  语言服务器
    ↑                      ↑
  多客户端            多语言实现
```

- 编辑器无需为每种语言实现支持
- 语言服务器实现一次，多编辑器复用
- 降低编辑器开发成本

## 相关链接

- [[OpenCode]]
- [[oh-my-openagent]]
- [[AI 编程工具对比]]
- [[MCP]] — Model Context Protocol，类似的工具集成协议