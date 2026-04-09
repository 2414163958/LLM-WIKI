---
title: "mtymek/opencode-obsidian: Embed OpenCode AI assistant directly in Obsidian's sidebar."
source: "https://github.com/mtymek/opencode-obsidian"
author:
published:
created: 2026-04-09
description: "Embed OpenCode AI assistant directly in Obsidian's sidebar. - mtymek/opencode-obsidian"
tags:
  - "clippings"
---
## OpenCode plugin for ObsidianObsidian 的 OpenCode 插件

Give your notes AI capability by embedding Opencode [OpenCode](https://opencode.ai/) AI assistant directly in Obsidian:  
通过将 [OpenCode](https://opencode.ai/) AI 助手直接嵌入 Obsidian，为您的笔记赋予 AI 功能：

[![[raw/assets/00ccf710f3820a8882eb2cdeef43553e_MD5.png]]](https://github.com/mtymek/opencode-obsidian/blob/main/assets/opencode_in_obsidian.png)

**Use cases:使用案例：**

- Summarize and distill long-form content  
	总结和提炼长篇内容
- Draft, edit, and refine your writing  
	撰写、编辑和完善你的文章
- Query and explore your knowledge base  
	查询和探索您的知识库
- Generate outlines and structured notes  
	生成提纲和结构化笔记

This plugin uses OpenCode's web view that can be embedded directly into Obsidian window. Usually similar plugins would use the ACP protocol, but I want to see how how much is possible without having to implement (and manage) a custom chat UI - I want the full power of OpenCode in my Obsidian.  
此插件使用 OpenCode 的 Web 视图，可直接嵌入到 Obsidian 窗口中。通常类似的插件会使用 ACP 协议，但我希望了解在无需实现（和管理）自定义聊天 UI 的情况下，OpenCode 能实现多少功能——我希望在 Obsidian 中充分利用 OpenCode 的强大功能。

*Note: plugin author is not afiliated with OpenCode or Obsidian - this is a 3rd party software.  
注意：插件作者与 OpenCode 或 Obsidian 无关——这是一个第三方软件。*

## Requirements 要求

- Desktop only (uses Node.js child processes)  
	仅限桌面端（使用 Node.js 子进程）
- [OpenCode CLI](https://opencode.ai/) installed  
	已安装 [OpenCode CLI](https://opencode.ai/)
- [Bun](https://bun.sh/) installed  
	[面包](https://bun.sh/) 安装

## Installation 安装

The easiest way to install this plugin during beta is via [BRAT](https://github.com/TfTHacker/obsidian42-brat) (Beta Reviewer's Auto-update Tool):  
在测试版期间安装此插件最简单的方法是通过 [BRAT](https://github.com/TfTHacker/obsidian42-brat) （Beta Reviewer's Auto-update Tool）：

1. Install the BRAT plugin from Obsidian Community Plugins  
	从 Obsidian Community Plugins 安装 BRAT 插件
2. Open BRAT settings and click "Add Beta plugin"  
	打开 BRAT 设置，然后点击“添加 Beta 插件”。
3. Enter: `mtymek/opencode-obsidian`  
	输入： `mtymek/opencode-obsidian`
4. Click "Add Plugin" - BRAT will install the latest release automatically  
	点击“添加插件”——BRAT 将自动安装最新版本。
5. Enable the OpenCode plugin in Obsidian Settings > Community Plugins  
	在 Obsidian 设置 > 社区插件中启用 OpenCode 插件

BRAT will automatically check for updates and notify you when new versions are available.  
BRAT 会自动检查更新，并在有新版本可用时通知您。

### For Developers 面向开发者

If you want to contribute or develop the plugin:  
如果您想为插件做出贡献或进行开发：

1. Clone to `.obsidian/plugins/obsidian-opencode` subdirectory under your vault's root:  
	克隆到您的保险库根目录下的 `.obsidian/plugins/obsidian-opencode` 子目录中：
	```
	git clone https://github.com/mtymek/opencode-obsidian.git .obsidian/plugins/obsidian-opencode
	```
2. Install dependencies and build:  
	安装依赖项并构建：
	```
	bun install && bun run build
	```
3. Enable in Obsidian Settings > Community Plugins  
	在 Obsidian 设置 > 社区插件中启用
4. Add AGENTS.md to your workspace root to guide the AI assistant  
	将 AGENTS.md 文件添加到工作区根目录，以指导 AI 助手。

## Usage 用法

- Click the terminal icon in the ribbon, or  
	单击功能区中的终端图标，或
- `Cmd/Ctrl+Shift+O` to toggle the panel  
	按 `Cmd/Ctrl+Shift+O` 切换面板
- Server starts automatically when you open the panel  
	打开面板时，服务器会自动启动。

## Settings 设置

### Custom Command Mode 自定义命令模式

Enable "Use custom command" when you need more control over how OpenCode starts—for example, to add extra CLI flags, use a custom wrapper script, or run OpenCode through a container or virtual environment.  
当您需要对 OpenCode 的启动方式进行更多控制时，请启用“使用自定义命令”——例如，添加额外的 CLI 标志、使用自定义包装脚本或通过容器或虚拟环境运行 OpenCode。

When using custom command:  
使用自定义命令时：

- **Hostname and port must match** the values set in the Port and Hostname fields above  
	**主机名和端口必须与上方“端口”和“主机名”字段中设置的值匹配。**
- You **must include `--cors app://obsidian.md`** to allow Obsidian to embed the OpenCode interface  
	您 **必须包含 `--cors app://obsidian.md`** 以允许 Obsidian 嵌入 OpenCode 接口。

Example:例子：

```
opencode serve --port 14096 --hostname 127.0.0.1 --cors app://obsidian.md
```

Other settings (port, hostname, auto-start, view location, context injection) are available through the settings UI and are self-explanatory.  
其他设置（端口、主机名、自动启动、查看位置、上下文注入）可通过设置界面进行设置，其含义不言自明。

### Context injection (experimental)上下文注入（实验性）

This plugin can automatically inject context to the running OC instance: list of open notes and currently selected text.  
该插件可以自动向正在运行的 OC 实例注入上下文：打开的笔记列表和当前选定的文本。

Currently, this is work-in-progress feature with some limitations - it won't work when creating new session from OC interface.  
目前，此功能尚处于开发阶段，存在一些限制——从 OC 界面创建新会话时将无法使用。

## Windows Troubleshooting Windows 故障排除

If you see "Executable not found at 'opencode'" despite opencode being installed:  
如果即使 opencode 已安装，仍然出现“在 'opencode' 找不到可执行文件”的错误：

1. Find your opencode.cmd path:  
	找到 opencode.cmd 的路径：
	```
	where opencode.cmd
	```
2. Configure the full path in plugin settings:  
	在插件设置中配置完整路径：
	```
	C:\Users\{username}\AppData\Roaming\npm\opencode.cmd
	```

This is due to Electron/Obsidian not fully inheriting PATH on Windows.  
这是由于 Electron/Obsidian 在 Windows 上无法完全继承 PATH 环境变量所致。