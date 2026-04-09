---
title: AgentShield
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/affaan-m everything-claude-code.md]]"
tags: [安全, 审计, 漏洞扫描, Claude Code]
type: entity
---

# AgentShield

AI Agent 配置安全审计工具，于 Claude Code 黑客松（2026 年 2 月）开发完成。

## 基本信息

| 属性 | 值 |
|------|-----|
| 开发者 | @affaan-m |
| 测试 | 1282 项 |
| 覆盖率 | 98% |
| 静态分析规则 | 102 条 |
| npm | ecc-agentshield |
| GitHub | affaan-m/agentshield |

## 扫描范围

| 文件类型 | 检测内容 |
|----------|----------|
| CLAUDE.md | 项目配置漏洞 |
| settings.json | 全局配置漏洞 |
| MCP 配置 | 服务风险评估 |
| 钩子定义 | 注入分析 |
| 智能体定义 | 配置审查 |
| 技能模块 | 模式检查 |

## 检测类别

| 类别 | 内容 | 数量 |
|------|------|------|
| 密钥检测 | API key、token、password | 14 种模式 |
| 权限审计 | 过宽权限、危险操作 | 多条 |
| 钩子注入分析 | shell 注入、路径穿越 | 多条 |
| MCP 服务风险评估 | 危险工具、数据泄露 | 多条 |
| 智能体配置审查 | model/tools 权限 | 多条 |

## Opus 对抗推理

`--opus` 参数启动 3 个 Claude Opus 4.6 智能体：

| 角色 | 任务 |
|------|------|
| 攻击者（红队） | 寻找利用链 |
| 防御者（蓝队） | 评估防护机制 |
| 审计者 | 综合生成优先级风险报告 |

对抗推理而非单纯模式匹配。

## 输出格式

- **终端**：彩色等级（A-F）
- **JSON**：CI 流水线集成
- **Markdown**：文档格式
- **HTML**：可视化报告
- **退出码**：严重问题返回 2（可做构建门禁）

## 使用方式

```bash
npx ecc-agentshield scan           # 快速扫描
npx ecc-agentshield scan --fix     # 自动修复
npx ecc-agentshield scan --opus    # 深度对抗分析
npx ecc-agentshield init           # 从零生成安全配置
```

在 Claude Code 中：`/security-scan`

在 CI 中：GitHub Action 集成

## 相关链接

- [[Everything Claude Code]] — 包含 AgentShield
- [[安全审计]] — 概念页面
- [[验证循环]] — 安全评估器
- [[affaan-m]] — 开发者