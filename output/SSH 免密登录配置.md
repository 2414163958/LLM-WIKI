---
title: SSH 免密登录配置
created: 2026-04-10
updated: 2026-04-10
type: note
tags: [SSH, 服务器配置, 运维, Windows]
---

## 一、生成 SSH 密钥对

打开 PowerShell，执行：

```powershell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

**提示说明：**
- 按回车使用默认路径（`C:\Users\24141\.ssh\id_rsa`）
- 可设置密码保护私钥（可选，直接回车跳过）

生成后得到两个文件：
- `id_rsa` - 私钥（保密，不要分享）
- `id_rsa.pub` - 公钥（上传到服务器）

---

## 二、将公钥上传到服务器

### 方法 1：自动上传（Linux/macOS 推荐）

```bash
ssh-copy-id root@服务器 IP
```

> ⚠️ **注意**：Windows 默认不包含 `ssh-copy-id` 命令。如果在 PowerShell 中执行提示"无法识别该命令"，请使用方法 2 手动上传。

### 方法 2：手动上传（Windows 推荐）

```powershell
# 1. 查看公钥内容
type C:\Users\24141\.ssh\id_rsa.pub

# 2. 复制全部内容

# 3. 登录服务器（需要密码）
ssh root@服务器 IP

# 4. 在服务器上执行
mkdir -p ~/.ssh
echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQC4UOnnMLNnVFovVKWyN8RMJRQLvYI4R/sLDrKsn9K3e+l/nIq709GnhSfhiXBilIUXNNLseYAoVBn/YyGO+VBpZfsf856JciptJyB6PsyRGDvtA1MeNJpZAAxrxBDeaMKdY6VeGN0OQkc8RqlRGtuheDUDpz4UsT96DotGvuF23aFm5P3ZFIcftmw2GU975sdiFOXofKWC6QA19bEErNcGBW1dnvxE9ypPCeGq7TZRWvwhDfdsbZ8Yi3BhWB4cHQFP3hMzkEkQOTv3BMa3RT60IvORWOZ3vxKTVMM3glEps5+S/b0uKDD7WCBLTX2YvpkPlnw18sXElRUijOEb/irW+CWfMZMKtPRwIRwdEr3Rx3ZC/ToeHnIqHWcN4ADmlETt27gsnezDLxbySz5hDQ/g1rIl31JcjZmsuQLLK5mgeJAW3AwWMWGOc6+NeUbzhqAe/rxOnXwLRTwxsnRvNrlxTswKTAgSKjtOxWo8KOnm6zTO3MalcJR1m2gckv2KK38=" >> ~/.ssh/authorized_keys
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
exit
```

#### 方法 2b：使用 scp 自动上传（Windows 替代方案）

如果你不想手动复制粘贴，可以使用 `scp` 命令：

```powershell
# 将公钥上传到服务器并自动配置
scp C:\Users\24141\.ssh\id_rsa.pub root@服务器 IP:/tmp/
ssh root@服务器 IP "mkdir -p ~/.ssh && cat /tmp/id_rsa.pub >> ~/.ssh/authorized_keys && chmod 700 ~/.ssh && chmod 600 ~/.ssh/authorized_keys && rm /tmp/id_rsa.pub"
```

---

## 三、测试免密登录

```powershell
ssh root@服务器 IP
```

如果直接登录成功，无需输入密码，说明配置完成。

---

## 四、配置多个服务器快捷连接

编辑配置文件：`C:\Users\24141\.ssh\config`

```
# 开发服务器
Host dev-server
    HostName 192.168.1.100
    User root
    IdentityFile C:\Users\24141\.ssh\id_rsa

# 生产服务器
Host prod-server
    HostName 10.0.0.100
    User admin
    Port 2222
    IdentityFile C:\Users\24141\.ssh\id_rsa_prod
```

配置后，只需输入：
```powershell
ssh dev-server     # 连接开发服务器
ssh prod-server    # 连接生产服务器
```

---

## 五、常见问题

### 1. 权限问题（Windows）

```powershell
# 修复私钥权限
icacls C:\Users\24141\.ssh\id_rsa /inheritance:r
icacls C:\Users\24141\.ssh\id_rsa /grant:r "$($env:USERNAME):(R)"
```

### 2. 服务器拒绝密钥

检查服务器端权限：
```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```

### 3. 清除旧密钥（服务器重装后）

```powershell
ssh-keygen -R 服务器 IP
```

---
