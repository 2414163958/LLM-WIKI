---
title: obsidian-git - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/Vinzent03 obsidian-git.md]]"
tags:
  - Obsidian
  - Git
  - 版本控制
  - 插件
type: source-summary
---

# obsidian-git - 摘要

[[Vinzent03]] 开发的 Obsidian 社区插件，将 Git 版本控制集成到 Vault 中。

## 核心功能

| 功能 | 说明 |
|------|------|
| 自动提交同步 | 按计划自动 commit、pull、push |
| 启动自动拉取 | Obsidian 启动时自动拉取远程更新 |
| 源码控制视图 | 暂存/取消暂存、提交、diff 文件 |
| 历史视图 | 浏览提交日志和已更改文件 |
| 差异视图 | 查看文件版本差异 |
| 编辑器标记 | 指示添加、修改、删除的行（仅桌面端） |
| 子模块支持 | 管理多个仓库（仅桌面端） |
| GitHub 集成 | 在浏览器中打开文件和历史 |

## 移动端支持（实验性）

> ⚠️ 移动端极不稳定，作者不建议在移动端使用。

**限制：**
- 无 SSH 认证
- 仓库大小受限（内存限制）
- 无 rebase 合并策略
- 无子模块支持

**替代方案：** [[GitSync]]（Android/iOS）

## 技术实现

移动端使用 [isomorphic-git](https://isomorphic-git.org/)（JavaScript 重新实现的 Git），存在性能和稳定性问题。

## 桌面端注意事项

- Linux：不支持 Snap，不推荐 Flatpak
- 认证：部分 Git 服务需要额外配置 HTTPS/SSH 认证

## 相关链接

- [[Obsidian]]
- [[Vinzent03]]
- [[GitSync]]
- [官方文档](https://publish.obsidian.md/git-doc)