---
title: OpenClaw 飞书插件 - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/‍‬⁢‍‍‍﻿‬⁣‍⁢‬‌﻿‍‬⁡⁢‬⁢⁢⁡‍⁡​⁢​⁤‌⁢⁤﻿‌‍﻿​‌⁡⁣⁣​⁡⁣‍⁢‬​‌⁢‍OpenClaw 飞书官方插件使用指南（公开版） - 飞书云文档.md]]"
tags: [OpenClaw, 飞书, 插件, 配置]
type: source-summary
---

# OpenClaw 飞书插件 - 摘要

OpenClaw 飞书官方插件的安装和配置指南。

## 安装

```bash
npx -y @larksuite/openclaw-lark install
```

Windows 用户如遇扫码问题，建议使用 [Cmder](https://cmder.app/) 终端。

## 用户授权

在飞书对话中发送 `/feishu auth` 快速完成批量授权，授权后 OpenClaw 可通过用户身份完成：
- 消息操作
- 文档操作
- 多维表格操作
- 日历操作

## 学习新技能

安装插件后，建议在飞书对话中发送：
```
学习一下我安装的新飞书插件，列出有哪些能力
```

让 OpenClaw 学习并正确使用新技能。

## 升级插件版本

```bash
npx -y @larksuite/openclaw-lark@2026.4.1 install --version 2026.4.1 --tools-version 1.0.37
```

## 多机器人配置

支持多个飞书机器人对应不同 Agent：

1. 创建新的飞书机器人：[立即创建](https://open.feishu.cn/page/openclaw?form=multiAgent)
2. 告诉 AI 新 Agent 的用途和关联账号
3. 发送配置指南让 OpenClaw 自动完成配置

详细操作：[多机器人配置指南](https://bytedance.larkoffice.com/docx/WNNXdhKxmo8KDJxMM9dc0GD5nFf)

## 相关链接

- [[OpenClaw]] — 项目实体
- [[OpenClaw - 摘要]] — 主项目摘要
- [[技能注入]] — 技能系统机制
- [[ClawHub]] — 技能注册中心