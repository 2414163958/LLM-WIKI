---
title: SSH 免密登录
created: 2026-04-10
updated: 2026-04-10
sources:
  - [[output/SSH 免密登录配置.md]]
tags: [SSH, 服务器配置, 运维, 安全, Windows]
type: concept
---

# SSH 免密登录

SSH 免密登录是通过公钥认证机制实现的无需密码的安全远程登录方式。

## 核心原理

1. **密钥对**：生成一对非对称加密密钥（公钥 + 私钥）
2. **公钥上传**：将公钥添加到服务器的 `~/.ssh/authorized_keys`
3. **私钥认证**：本地使用私钥完成身份验证，无需密码

## Windows 环境配置流程

### 1. 生成密钥对

```powershell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- 默认路径：`C:\Users\{用户名}\.ssh\id_rsa`
- 私钥：`id_rsa`（保密）
- 公钥：`id_rsa.pub`（上传到服务器）

### 2. 上传公钥

**Windows 推荐（scp 方案）：**

```powershell
# 上传公钥
scp C:\Users\24141\.ssh\id_rsa.pub root@服务器IP:/tmp/

# 配置服务器
ssh root@服务器IP "mkdir -p ~/.ssh && cat /tmp/id_rsa.pub >> ~/.ssh/authorized_keys && chmod 700 ~/.ssh && chmod 600 ~/.ssh/authorized_keys && rm /tmp/id_rsa.pub"
```

**Linux/macOS（ssh-copy-id）：**

```bash
ssh-copy-id root@服务器IP
```

### 3. 配置多服务器快捷连接

编辑 `C:\Users\{用户名}\.ssh\config`：

```
Host dev-server
    HostName 192.168.1.100
    User root
    IdentityFile C:\Users\24141\.ssh\id_rsa

Host prod-server
    HostName 10.0.0.100
    User admin
    Port 2222
    IdentityFile C:\Users\24141\.ssh\id_rsa_prod
```

连接时只需：
```powershell
ssh dev-server
ssh prod-server
```

## 关键权限设置

**服务器端：**
```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```

**Windows 端（修复私钥权限）：**
```powershell
icacls C:\Users\24141\.ssh\id_rsa /inheritance:r
icacls C:\Users\24141\.ssh\id_rsa /grant:r "$($env:USERNAME):(R)"
```

## 常见问题

| 问题 | 解决 |
|------|------|
| 服务器重装后连接失败 | `ssh-keygen -R 服务器IP` 清除旧密钥 |
| 权限被拒绝 | 检查服务器端 `.ssh` 目录权限 |
| Windows 提示权限过宽 | 使用 `icacls` 修复私钥文件权限 |

## 相关链接

- [[服务器配置]] — 服务器运维综合指南
- [[Windows 运维]] — Windows 环境下的运维操作
