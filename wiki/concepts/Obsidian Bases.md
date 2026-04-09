---
title: Obsidian Bases
created: 2026-04-09
updated: 2026-04-09
sources: "[[raw/kepano obsidian-skills.md]]"
tags:
  - Obsidian
  - 数据库
  - 查询
type: concept
---

# Obsidian Bases

Obsidian 的数据库功能（`.base` 文件），支持视图、筛选、公式和摘要，类似 Notion Database。

## 功能

- **视图**：表格、列表、看板等多种展示形式
- **筛选**：基于属性过滤页面
- **公式**：计算字段值
- **摘要**：聚合统计

## 文档

[Obsidian Bases 官方文档](https://help.obsidian.md/bases/syntax)

## 在 Agent Skills 中的应用

[[obsidian-skills]] 提供的 `obsidian-bases` skill 让 Agent 能够：
- 创建 `.base` 文件
- 定义视图和筛选条件
- 编写公式和摘要
- 构建动态数据库视图

## 与 Dataview 的关系

[[Dataview]] 是社区插件，提供类似的查询功能；Obsidian Bases 是官方原生实现。

## 相关链接

- [[Obsidian]]
- [[Dataview]]
- [[obsidian-skills - 摘要]]