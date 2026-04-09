---
title: colleague-skill - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[titanwings colleague-skill]]"
tags:
  - agent-skill
  - knowledge-distillation
  - persona
  - digital-immortality
type: source-summary
---

# colleague-skill - 摘要

## 核心定位

将离职同事的知识和人格转化为可复用的 **AI Skill**，实现"赛博永生"——用他的技术规范写代码，用他的语气回答问题。

## 技术架构

### 双层结构

| 部分 | 职责 |
|------|------|
| **Work Skill** | 系统知识、技术规范、工作流程、经验知识库 |
| **Persona** | 五层性格结构：硬规则 → 身份 → 表达风格 → 决策模式 → 人际行为 |

运行逻辑：`接到任务 → Persona 判断态度 → Work Skill 执行 → 用他的语气输出`

### Persona 五层结构

1. **硬规则**：不可违反的核心约束
2. **身份**：职业角色、公司背景
3. **表达风格**：用词习惯、口头禅
4. **决策模式**：如何权衡、何时甩锅
5. **人际行为**：与他人的互动方式

## 数据来源

| 来源 | 消息记录 | 文档/Wiki | 多维表格 |
|------|---------|----------|---------|
| 飞书 | ✅ API | ✅ | ✅ |
| 钉钉 | ⚠️ 浏览器 | ✅ | ✅ |
| Slack | ✅ API | — | — |
| 微信 | ✅ SQLite | — | — |
| PDF/图片/邮件/Markdown | ✅ 手动 | — | — |

## 功能特性

- **进化机制**：追加文件 → 增量 merge；对话纠正 → Correction 层立即生效
- **版本管理**：每次更新自动存档，支持回滚
- **管理命令**：`/list-colleagues`、`/{slug}`、`/{slug}-work`、`/{slug}-persona`、`/colleague-rollback`、`/delete-colleague`

## 支持的标签

- **个性**：认真负责、甩锅高手、完美主义、拖延症、PUA 高手、阴阳怪气等
- **企业文化**：字节范、阿里味、腾讯味、华为味、第一性原理、OKR 狂热者等
- **职级**：字节 2-1~3-3+、阿里 P5~P11、腾讯 T1~T4、百度 T5~T9 等

## 安装与使用

```bash
# Claude Code（项目级）
mkdir -p .claude/skills
git clone https://github.com/titanwings/colleague-skill .claude/skills/create-colleague

# Claude Code（全局）
git clone https://github.com/titanwings/colleague-skill ~/.claude/skills/create-colleague

# OpenClaw
git clone https://github.com/titanwings/colleague-skill ~/.openclaw/workspace/skills/create-colleague
```

使用命令：`/create-colleague` 按提示输入信息

## 相关链接

- [[Agent Skills]] — 本项目遵循的开放标准
- [[知识蒸馏]] — 从原始材料提取结构化知识
- [[Persona]] — 人格建模
- [[数字永生]] — 核心理念