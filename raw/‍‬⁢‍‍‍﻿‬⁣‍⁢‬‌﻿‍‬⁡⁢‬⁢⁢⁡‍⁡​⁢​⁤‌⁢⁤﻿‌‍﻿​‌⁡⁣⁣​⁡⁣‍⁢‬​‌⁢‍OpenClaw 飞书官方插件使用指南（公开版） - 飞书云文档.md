---
title: "‍‬⁢‍‍‍﻿‬⁣‍⁢‬‌﻿‍‬⁡⁢‬⁢⁢⁡‍⁡​⁢​⁤‌⁢⁤﻿‌‍﻿​‌⁡⁣⁣​⁡⁣‍⁢‬​‌⁢‍OpenClaw 飞书官方插件使用指南（公开版） - 飞书云文档"
source: "https://bytedance.larkoffice.com/docx/MFK7dDFLFoVlOGxWCv5cTXKmnMh"
author:
published:
created: 2026-04-08
description:
tags:
  - "clippings"
---
## 安装飞书插件

```shell
npx -y @larksuite/openclaw-lark install
```

>[!warning] 如果 Windows 设备中无法扫码成功，可能是因为终端的分辨率问题导致，建议更换终端使用 [Cmder](https://cmder.app/)。


- 若希望快速完成用户授权，便于后续 OpenClaw 通过你的身份完成消息、文档、多维表格、日历等任务，可以在飞书对话中发送 `/feishu auth` 来完成批量授权。
    
- 为了让 OpenClaw 能学会这些新技能并正确使用，建议在飞书对话中发送 `学习一下我安装的新飞书插件，列出有哪些能力`。

## 升级飞书插件版本

```Shell
npx -y @larksuite/openclaw-lark@2026.4.1 install --version 2026.4.1 --tools-version 1.0.37
```

## 如何在飞书插件中配置 OpenClaw 关联多个飞书机器人，对应不同 Agent

详细操作参考：[如何在飞书插件中配置 OpenClaw 关联多个飞书机器人，对应不同Agent](https://bytedance.larkoffice.com/docx/WNNXdhKxmo8KDJxMM9dc0GD5nFf)

**快捷方法**：

1. 创建新的飞书机器人，用于关联到新的账号上

	一键创建一个OpenClaw 机器人：[立即创建](https://open.feishu.cn/page/openclaw?form=multiAgent)

2. 告诉 AI 你想创建一个怎样的新 Agent，以及这个 Agent 关联的飞书账号是什么，并将操作指南发给 OpenClaw 请他自己完成对应配置：[如何在飞书插件中配置 OpenClaw 关联多个飞书机器人，对应不同Agent](https://bytedance.larkoffice.com/docx/WNNXdhKxmo8KDJxMM9dc0GD5nFf)


