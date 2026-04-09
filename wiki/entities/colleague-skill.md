---
title: colleague-skill
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[titanwings colleague-skill]]"
tags:
  - agent-skill
  - tool
  - open-source
type: entity
---

# colleague-skill

## 基本信息

| 属性 | 值 |
|------|-----|
| 项目 | titanwings/colleague-skill |
| 作者 | [@titanwings](https://github.com/titanwings) |
| 支持 | Shanghai AI Lab · AI Safety Center |
| 标准 | [AgentSkills](https://agentskills.io/) |
| 许可 | 开源 |

## 核心功能

将离职同事的知识和人格转化为可复用的 **AI Skill**：
- 用他的技术规范写代码
- 用他的语气回答问题
- 知道他什么时候会甩锅

## 技术架构

双层结构：
- **Work Skill**：系统知识、技术规范、工作流程
- **Persona**：五层性格结构（硬规则 → 身份 → 表达风格 → 决策模式 → 人际行为）

## 支持平台

- Claude Code（项目级或全局安装）
- OpenClaw

## 数据来源

- 自动采集：飞书（API）、钉钉（浏览器）、Slack（API）
- 手动导入：微信聊天记录、PDF、图片、邮件、Markdown、直接粘贴

## 相关链接

- [[Agent Skills]] — 遵循的开放标准
- [[知识蒸馏]] — 核心技术
- [[Persona]] — 人格建模方法
- [[数字永生]] — 核心理念
- [[colleague-skill - 摘要]] — 详细摘要