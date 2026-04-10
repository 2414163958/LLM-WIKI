---
title: SSH 免密登录配置 - 摘要
created: 2026-04-10
updated: 2026-04-10
source: [[raw/SSH 免密登录配置.md]]
tags: [SSH, 服务器配置, 运维, Windows, PowerShell]
type: source-summary
---

# SSH 免密登录配置 - 摘要

## 来源信息

- **原始文档**：[[raw/SSH 免密登录配置.md]]
- **类型**：操作指南/教程
- **创建日期**：2026-04-10

## 主要内容

本文档是 Windows 环境下 SSH 免密登录的完整配置指南，涵盖密钥生成、公钥上传、多服务器配置和常见问题解决。

### 核心流程

1. **生成密钥对**：使用 `ssh-keygen` 生成 RSA 4096 位密钥
2. **上传公钥**：Windows 使用 `scp` + SSH 命令自动配置，Linux/macOS 使用 `ssh-copy-id`
3. **配置多服务器**：编辑 `~/.ssh/config` 创建别名快捷连接
4. **权限修复**：服务器端设置正确的 `.ssh` 目录权限，Windows 端使用 `icacls` 修复私钥权限

### Windows 特有方案

- **公钥上传**：通过 `scp` 上传 + SSH 命令自动追加到 `authorized_keys`
- **权限修复**：使用 `icacls` 限制私钥文件访问权限
- **多服务器管理**：通过 SSH config 文件简化连接

### 关键命令

```powershell
# 生成密钥
ssh-keygen -t rsa -b 4096 -C "email@example.com"

# Windows 上传方案
scp ~/.ssh/id_rsa.pub root@server:/tmp/
ssh root@server "cat /tmp/id_rsa.pub >> ~/.ssh/authorized_keys"

# 修复 Windows 私钥权限
icacls ~/.ssh/id_rsa /inheritance:r
icacls ~/.ssh/id_rsa /grant:r "$($env:USERNAME):(R)"
```

## 提取的概念

- [[SSH 免密登录]] — 公钥认证机制的原理和配置
- [[服务器配置]] — Linux 服务器运维基础知识
- [[Windows 运维]] — Windows 环境下的运维操作

## 标签

#SSH #服务器配置 #运维 #Windows #PowerShell
