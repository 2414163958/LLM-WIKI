---
title: OpenSpec
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/Fission-AI OpenSpec.md]]"
tags: [ai-coding, spec-driven-development, framework]
type: entity
---

# OpenSpec

最受欢迎的规范驱动开发（SDD）框架，专为 AI 编码助手设计。由 [[Fission-AI]] 开发维护。

## 核心功能

### 变更管理

每次变更创建独立目录：
```
openspec/changes/<change-name>/
├── proposal.md  — 变更动机和范围
├── specs/       — 需求规格和场景
├── design.md    — 技术设计
└── tasks.md     — 实现清单
```

### Slash 命令

| 命令 | 功能 |
|------|------|
| `/opsx:propose` | 创建变更提案 |
| `/opsx:apply` | 执行任务清单 |
| `/opsx:archive` | 归档完成变更 |

扩展命令：`/opsx:new`、`/opsx:continue`、`/opsx:ff`、`/opsx:verify`、`/opsx:sync`、`/opsx:bulk-archive`、`/opsx:onboard`

## 安装

```bash
npm install -g @fission-ai/openspec@latest
cd your-project
openspec init
```

**要求**：Node.js 20.19.0+

## 技术特点

- **支持 20+ AI 助手**：Claude Code、Cursor、OpenCode 等
- **模型推荐**：Opus 4.5、GPT 5.2（高推理能力）
- **遥测**：收集匿名使用统计（命令名称和版本），可通过环境变量禁用

## 竞品对比

| 工具 | 优势 | 劣势 |
|------|------|------|
| OpenSpec | 轻量、灵活、工具中立 | - |
| Spec Kit (GitHub) | 全面 | 重量、阶段门控严格 |
| Kiro (AWS) | 功能强大 | 绑定 IDE、仅 Claude 模型 |

## 相关链接

- [[规范驱动开发]] — 核心概念
- [[Fission-AI]] — 开发组织
- [[Agent Skills]] — 互补的知识包系统
- [[AI 编程工具对比]] — 工具对比分析
- GitHub: https://github.com/Fission-AI/OpenSpec