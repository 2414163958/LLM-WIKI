---
title: obsidian-git
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/Vinzent03 obsidian-git.md]]"
tags:
  - Obsidian
  - Git
  - 插件
  - 版本控制
type: entity
---

# obsidian-git

Obsidian 社区插件，将 Git 版本控制集成到 Vault 中。

## 开发者

[[Vinzent03]]（自 2021 年 3 月起维护，原开发者 denolehov）

## 主要功能

- **自动同步**：按计划自动 commit、pull、push
- **源码控制视图**：类似 VS Code 的 Git 管理界面
- **历史视图**：浏览提交历史
- **差异视图**：对比文件版本
- **编辑器标记**：行级变更指示（仅桌面端）

## 平台支持

| 平台 | 状态 |
|------|------|
| 桌面端（Windows/macOS/Linux） | ✅ 完整支持 |
| 移动端（iOS/Android） | ⚠️ 实验性，不稳定 |

## 移动端替代

移动端推荐使用 [[GitSync]]，支持 iOS 和 Android。

## 技术细节

- 移动端基于 isomorphic-git（JavaScript 实现）
- 桌面端使用系统 Git

## 相关链接

- [[Obsidian]]
- [[Vinzent03]]
- [[GitSync]]
- [[obsidian-git - 摘要]]
- [GitHub 仓库](https://github.com/Vinzent03/obsidian-git)
- [官方文档](https://publish.obsidian.md/git-doc)