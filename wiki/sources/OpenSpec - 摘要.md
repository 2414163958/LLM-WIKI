---
title: OpenSpec - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/Fission-AI OpenSpec.md]]"
tags: [spec-driven-development, ai-coding, workflow]
type: source-summary
---

# OpenSpec - 摘要

## 核心定位

OpenSpec 是一个**规范驱动开发（Spec-driven Development, SDD）框架**，专为 AI 编码助手设计。核心理念是"先规范后代码"——在编写任何代码之前，先让人类和 AI 对需求达成一致。

## 核心理念

```
→ fluid not rigid        （灵活而非僵化）
→ iterative not waterfall（迭代而非瀑布）
→ easy not complex       （简单而非复杂）
→ built for brownfield not just greenfield（兼容遗留项目）
→ scalable from personal projects to enterprises（可扩展）
```

## 工作流程

### 基本流程（opsx）

```
/opsx:propose → 创建变更提案（proposal.md、specs/、design.md、tasks.md）
/opsx:apply   → 执行任务清单
/opsx:archive → 归档完成的变更
```

### 扩展流程

- `/opsx:new` - 新建变更
- `/opsx:continue` - 继续进行中变更
- `/opsx:ff` - 快速前进
- `/opsx:verify` - 验证
- `/opsx:sync` - 同步
- `/opsx:bulk-archive` - 批量归档
- `/opsx:onboard` - 入门引导

## 目录结构

每次变更创建独立文件夹：
```
openspec/changes/<change-name>/
├── proposal.md  — 为什么做，改什么
├── specs/       — 需求和场景
├── design.md    — 技术方案
└── tasks.md     — 实现清单
```

## 与其他工具对比

| 工具 | 特点 | 限制 |
|------|------|------|
| **OpenSpec** | 轻量、灵活、支持 20+ AI 助手 | - |
| [Spec Kit](https://github.com/github/spec-kit) (GitHub) | 全面 | 重量、阶段门控严格、需要 Python |
| [Kiro](https://kiro.dev/) (AWS) | 功能强大 | 绑定 IDE、仅限 Claude 模型 |
| **无规范** | - | 提示模糊、结果不可预测 |

## 使用建议

- **模型选择**：推荐高推理能力模型（Opus 4.5、GPT 5.2）
- **上下文卫生**：开始实现前清除上下文，保持干净的上下文窗口
- **Node.js 要求**：20.19.0 或更高版本

## 与 Agent Skills 的关系

OpenSpec 提供变更管理的**结构化工作流**，[[Agent Skills]] 提供可复用的**知识包**。两者可互补：
- Skills 可用于自动化 OpenSpec 工作流中的验证步骤
- OpenSpec 的 specs/ 可作为 Skills 的结构化输入

## 相关链接

- [[规范驱动开发]] — 核心概念
- [[OpenSpec]] — 实体页面
- [[Fission-AI]] — 开发组织
- [[Agent Skills]] — 可互补的知识包系统
- [[AI 编程工具对比]] — 工具对比分析