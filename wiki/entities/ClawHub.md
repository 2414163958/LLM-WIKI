---
title: ClawHub
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/openclaw openclaw.md]]"
tags:
  - 技能注册
  - OpenClaw
  - 技能市场
type: entity
---

# ClawHub

## 简介

**ClawHub** 是 OpenClaw 的极简技能注册中心。启用后，代理可自动搜索技能并根据需要添加新技能。

## 功能

- **自动搜索**：代理根据任务需求自动查找相关技能
- **动态添加**：运行时添加新技能，无需手动安装
- **技能注册**：技能发布和发现的中央位置

## 与 Agent Skills 的关系

| 特点 | ClawHub | Agent Skills |
|------|---------|--------------|
| 来源 | OpenClaw 项目 | Anthropic 提出 |
| 注册机制 | 中央注册中心 | 本地技能目录 |
| 发现方式 | 代理自动搜索 | 手动配置/注入 |
| 注入方式 | 工作区 SKILL.md | AGENTS.md 等 |

ClawHub 可视为 [[Agent Skills]] 的一个具体实现，但强调中央注册和自动发现。

## 使用方式

ClawHub 默认启用，代理会在需要时自动搜索和添加技能。技能存储在 `~/.openclaw/workspace/skills/<skill>/SKILL.md`。

## 相关链接

- [[OpenClaw]] — 所属项目
- [[Agent Skills]] — 概念关联
- [[技能注入]] — 技术机制
- [[OpenClaw - 摘要]] — 来源摘要

## 外部链接

- ClawHub：https://clawhub.com/