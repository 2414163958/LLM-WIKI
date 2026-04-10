---
title: Windows 运维
created: 2026-04-10
updated: 2026-04-10
sources:
tags: [Windows, 运维, PowerShell, 命令行]
type: concept
---

# Windows 运维

Windows 环境下的系统管理和运维操作，利用现代工具实现类 Unix 的体验。

## 核心工具

### PowerShell

现代 Windows 的命令行环境，支持对象管道和脚本自动化。

```powershell
# 查看系统信息
Get-ComputerInfo

# 文件操作
Get-ChildItem ~
Set-Location path
New-Item -ItemType File -Name "file.txt"
```

### OpenSSH

Windows 10/11 内置 OpenSSH 客户端，支持完整的 SSH 功能：

- `ssh` — 远程登录
- `scp` — 文件传输
- `ssh-keygen` — 密钥生成
- `ssh-agent` — 密钥代理

## 典型场景

### SSH 连接与管理

- [[SSH 免密登录]] — Windows 环境下的配置指南
- 多服务器配置管理（~/.ssh/config）
- 密钥权限管理（icacls）

### 开发环境

- WSL 集成
- Windows Terminal 配置
- 包管理器（winget、scoop、chocolatey）

## Windows vs Linux 差异

| 操作 | Linux | Windows |
|------|-------|---------|
| 查看文件 | `cat file` | `Get-Content file` 或 `type file` |
| 列出目录 | `ls` | `dir` 或 `ls` (PS) |
| 复制 | `cp` | `Copy-Item` 或 `cp` (PS) |
| 权限设置 | `chmod` | `icacls` |
| 公钥上传 | `ssh-copy-id` | 使用 `scp` 手动配置 |

## 相关链接

- [[SSH 免密登录]] — Windows 下的详细配置流程
