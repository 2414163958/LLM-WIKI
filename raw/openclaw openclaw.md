---
title: "openclaw/openclaw: Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞"
source: "https://github.com/openclaw/openclaw"
author:
published:
created: 2026-04-09
description: "Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞  - openclaw/openclaw: Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞"
tags:
  - "clippings"
---
## 🦞 OpenClaw — Personal AI Assistant🦞 OpenClaw — 个人人工智能助手

![[raw/assets/b6cc9a20aeafc1c24baeaad3a68635e7_MD5.svg]]

**EXFOLIATE! EXFOLIATE!去角质！去角质！**

**OpenClaw** is a *personal AI assistant* you run on your own devices. It answers you on the channels you already use (WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, iMessage, BlueBubbles, IRC, Microsoft Teams, Matrix, Feishu, LINE, Mattermost, Nextcloud Talk, Nostr, Synology Chat, Tlon, Twitch, Zalo, Zalo Personal, WeChat, WebChat). It can speak and listen on macOS/iOS/Android, and can render a live Canvas you control. The Gateway is just the control plane — the product is the assistant.  
**OpenClaw** 是一款运行在您自己的设备上的 *个人 AI 助手* 。它可以通过您常用的渠道（WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、iMessage、BlueBubbles、IRC、Microsoft Teams、Matrix、飞书、LINE、Mattermost、Nextcloud Talk、Nostr、Synology Chat、Tlon、Twitch、Zalo、Zalo Personal、微信、WebChat）回复您的问题。它支持 macOS/iOS/Android 系统，并可渲染由您控制的实时 Canvas 界面。网关只是控制平台，产品本身才是真正的助手。

If you want a personal, single-user assistant that feels local, fast, and always-on, this is it.  
如果你想要一个感觉像本地助手、速度快、始终在线的单人个人助理，那就是它了。

[Website](https://openclaw.ai/) · [Docs](https://docs.openclaw.ai/) · [Vision](https://github.com/openclaw/openclaw/blob/main/VISION.md) · [DeepWiki](https://deepwiki.com/openclaw/openclaw) · [Getting Started](https://docs.openclaw.ai/start/getting-started) · [Updating](https://docs.openclaw.ai/install/updating) · [Showcase](https://docs.openclaw.ai/start/showcase) · [FAQ](https://docs.openclaw.ai/help/faq) · [Onboarding](https://docs.openclaw.ai/start/wizard) · [Nix](https://github.com/openclaw/nix-openclaw) · [Docker](https://docs.openclaw.ai/install/docker) · [Discord](https://discord.gg/clawd)  
[网站](https://openclaw.ai/) · [文档](https://docs.openclaw.ai/) · [愿景](https://github.com/openclaw/openclaw/blob/main/VISION.md) · [DeepWiki](https://deepwiki.com/openclaw/openclaw) · [入门指南](https://docs.openclaw.ai/start/getting-started) · [更新](https://docs.openclaw.ai/install/updating) · [案例展示](https://docs.openclaw.ai/start/showcase) · [常见问题](https://docs.openclaw.ai/help/faq) · [新手引导](https://docs.openclaw.ai/start/wizard) · [Nix](https://github.com/openclaw/nix-openclaw) · [Docker](https://docs.openclaw.ai/install/docker) · [Discord](https://discord.gg/clawd)

Preferred setup: run `openclaw onboard` in your terminal. OpenClaw Onboard guides you step by step through setting up the gateway, workspace, channels, and skills. It is the recommended CLI setup path and works on **macOS, Linux, and Windows (via WSL2; strongly recommended)**. Works with npm, pnpm, or bun. New install? Start here: [Getting started](https://docs.openclaw.ai/start/getting-started)  
推荐设置：在终端运行 `openclaw onboard` Onboard 会引导您逐步完成网关、工作区、通道和技能的设置。这是推荐的命令行设置路径，可在 **macOS、Linux 和 Windows（通过 WSL2；强烈推荐）** 上运行。支持 npm、pnpm 或 bun。全新安装？请从这里开始： [入门指南](https://docs.openclaw.ai/start/getting-started)

## Sponsors 赞助

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |

**Subscriptions (OAuth):订阅（OAuth）：**

- **[OpenAI](https://openai.com/)** (ChatGPT/Codex)  
	**[OpenAI](https://openai.com/)** （ChatGPT/Codex）

Model note: while many providers and models are supported, prefer a current flagship model from the provider you trust and already use. See [Onboarding](https://docs.openclaw.ai/start/onboarding).  
型号说明：虽然我们支持多种供应商和型号，但建议您选择您信任且已在使用的供应商的最新旗舰型号。请参阅 [“入门指南”](https://docs.openclaw.ai/start/onboarding) 。

## Models (selection + auth)模型（选择+身份验证）

- Models config + CLI: [Models](https://docs.openclaw.ai/concepts/models)  
	模型配置 + CLI： [模型](https://docs.openclaw.ai/concepts/models)
- Auth profile rotation (OAuth vs API keys) + fallbacks: [Model failover](https://docs.openclaw.ai/concepts/model-failover)  
	身份验证配置文件轮换（OAuth 与 API 密钥）+ 备用方案： [模型故障转移](https://docs.openclaw.ai/concepts/model-failover)

Runtime: **Node 24 (recommended) or Node 22.16+**.  
运行时： **Node 24（推荐）或 Node 22.16+** 。

```
npm install -g openclaw@latest
# or: pnpm add -g openclaw@latest

openclaw onboard --install-daemon
```

OpenClaw Onboard installs the Gateway daemon (launchd/systemd user service) so it stays running.  
OpenClaw Onboard 会安装 Gateway 守护进程（launchd/systemd 用户服务），使其保持运行状态。

## Quick start (TL;DR) 快速入门（TL;DR）

Runtime: **Node 24 (recommended) or Node 22.16+**.  
运行时： **Node 24（推荐）或 Node 22.16+** 。

Full beginner guide (auth, pairing, channels): [Getting started](https://docs.openclaw.ai/start/getting-started)  
完整入门指南（认证、配对、通道）： [入门指南](https://docs.openclaw.ai/start/getting-started)

```
openclaw onboard --install-daemon

openclaw gateway --port 18789 --verbose

# Send a message
openclaw message send --to +1234567890 --message "Hello from OpenClaw"

# Talk to the assistant (optionally deliver back to any connected channel: WhatsApp/Telegram/Slack/Discord/Google Chat/Signal/iMessage/BlueBubbles/IRC/Microsoft Teams/Matrix/Feishu/LINE/Mattermost/Nextcloud Talk/Nostr/Synology Chat/Tlon/Twitch/Zalo/Zalo Personal/WeChat/WebChat)
openclaw agent --message "Ship checklist" --thinking high
```

Upgrading? [Updating guide](https://docs.openclaw.ai/install/updating) (and run `openclaw doctor`).  
升级？ [更新指南](https://docs.openclaw.ai/install/updating) （并运行 `openclaw doctor` ）。

## Development channels 发展渠道

- **stable**: tagged releases (`vYYYY.M.D` or `vYYYY.M.D-<patch>`), npm dist-tag `latest`.  
	**stable**: tagged releases ( `vYYYY.MD` or `vYYYY.MD-<patch>` ), npm dist-tag `latest`.
- **beta**: prerelease tags (`vYYYY.M.D-beta.N`), npm dist-tag `beta` (macOS app may be missing).  
	**beta** ：预发布标签（ `vYYYY.MD-beta.N` ），npm dist-tag `beta` （macOS 应用可能缺失）。
- **dev**: moving head of `main`, npm dist-tag `dev` (when published).  
	**dev** ：移动 `main` 的头部，npm dist-tag `dev` （发布时）。

Switch channels (git + npm): `openclaw update --channel stable|beta|dev`. Details: [Development channels](https://docs.openclaw.ai/install/development-channels).  
切换通道（git + npm）： `openclaw update --channel stable|beta|dev` 。详细信息： [开发通道](https://docs.openclaw.ai/install/development-channels) 。

## From source (development)来自源头（开发）

Prefer `pnpm` for builds from source. Bun is optional for running TypeScript directly.  
首选 `pnpm` 进行源代码构建。Bun 可用于直接运行 TypeScript，但并非必需。

```
git clone https://github.com/openclaw/openclaw.git
cd openclaw

pnpm install
pnpm ui:build # auto-installs UI deps on first run
pnpm build

pnpm openclaw onboard --install-daemon

# Dev loop (auto-reload on source/config changes)
pnpm gateway:watch
```

Note: `pnpm openclaw ...` runs TypeScript directly (via `tsx`). `pnpm build` produces `dist/` for running via Node / the packaged `openclaw` binary.  
注意： `pnpm openclaw ...` 直接运行 TypeScript（通过 `tsx` ）。pnpm `pnpm build` 生成 `dist/` 目录，用于通过 Node 运行打包好的 `openclaw` 二进制文件。

## Security defaults (DM access)安全默认设置（DM 访问权限）

OpenClaw connects to real messaging surfaces. Treat inbound DMs as **untrusted input**.  
OpenClaw 连接到真实的即时通讯平台。将收到的私信视为 **不可信输入** 。

Full security guide: [Security](https://docs.openclaw.ai/gateway/security)  
完整安全指南： [安全](https://docs.openclaw.ai/gateway/security)

Default behavior on Telegram/WhatsApp/Signal/iMessage/Microsoft Teams/Discord/Google Chat/Slack:  
Telegram/WhatsApp/Signal/iMessage/Microsoft Teams/Discord/Google Chat/Slack 的默认行为：

- **DM pairing** (`dmPolicy="pairing"` / `channels.discord.dmPolicy="pairing"` / `channels.slack.dmPolicy="pairing"`; legacy: `channels.discord.dm.policy`, `channels.slack.dm.policy`): unknown senders receive a short pairing code and the bot does not process their message.  
	**DM 配对** （ `dmPolicy="pairing"` / `channels.discord.dmPolicy="pairing"` / `channels.slack.dmPolicy="pairing"` ；旧版： `channels.discord.dm.policy` ， `channels.slack.dm.policy` ）：未知发送者会收到一个简短的配对代码，机器人不会处理他们的消息。
- Approve with: `openclaw pairing approve <channel> <code>` (then the sender is added to a local allowlist store).  
	使用以下方式批准： `openclaw pairing approve <channel> <code>` （然后将发件人添加到本地允许列表存储中）。
- Public inbound DMs require an explicit opt-in: set `dmPolicy="open"` and include `"*"` in the channel allowlist (`allowFrom` / `channels.discord.allowFrom` / `channels.slack.allowFrom`; legacy: `channels.discord.dm.allowFrom`, `channels.slack.dm.allowFrom`).  
	公开的入站私信需要明确选择加入：设置 `dmPolicy="open"` 并在频道允许列表中包含 `"*"` （ `allowFrom` / `channels.discord.allowFrom` / `channels.slack.allowFrom` ；旧版： `channels.discord.dm.allowFrom` ， `channels.slack.dm.allowFrom` ）。

Run `openclaw doctor` to surface risky/misconfigured DM policies.  
运行 `openclaw doctor` 以发现有风险/配置错误的 DM 策略。

## Highlights 精彩片段

- **[Local-first Gateway](https://docs.openclaw.ai/gateway)** — single control plane for sessions, channels, tools, and events.  
	**[本地优先网关](https://docs.openclaw.ai/gateway)** ——会话、通道、工具和事件的单一控制平台。
- **[Multi-channel inbox](https://docs.openclaw.ai/channels)** — WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, BlueBubbles (iMessage), iMessage (legacy), IRC, Microsoft Teams, Matrix, Feishu, LINE, Mattermost, Nextcloud Talk, Nostr, Synology Chat, Tlon, Twitch, Zalo, Zalo Personal, WeChat, WebChat, macOS, iOS/Android.  
	**[多渠道收件箱](https://docs.openclaw.ai/channels)** ——WhatsApp、Telegram、Slack、Discord、Google Chat、Signal、BlueBubbles（iMessage）、iMessage（旧版）、IRC、Microsoft Teams、Matrix、飞书、LINE、Mattermost、Nextcloud Talk、Nostr、Synology Chat、Tlon、Twitch、Zalo、Zalo Personal、微信、WebChat、macOS、iOS/Android。
- **[Multi-agent routing](https://docs.openclaw.ai/gateway/configuration)** — route inbound channels/accounts/peers to isolated agents (workspaces + per-agent sessions).  
	**[多代理路由](https://docs.openclaw.ai/gateway/configuration)** — 将入站通道/帐户/对等体路由到隔离的代理（工作区 + 每个代理的会话）。
- **[Voice Wake](https://docs.openclaw.ai/nodes/voicewake) + [Talk Mode](https://docs.openclaw.ai/nodes/talk)** — wake words on macOS/iOS and continuous voice on Android (ElevenLabs + system TTS fallback).  
	**[语音唤醒](https://docs.openclaw.ai/nodes/voicewake) + [通话模式](https://docs.openclaw.ai/nodes/talk)** — macOS/iOS 上的唤醒词和 Android 上的连续语音（ElevenLabs + 系统 TTS 回退）。
- **[Live Canvas](https://docs.openclaw.ai/platforms/mac/canvas)** — agent-driven visual workspace with [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui).  
	**[Live Canvas](https://docs.openclaw.ai/platforms/mac/canvas)** — 基于代理的可视化工作空间，采用 [A2UI 技术](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) 。
- **[First-class tools](https://docs.openclaw.ai/tools)** — browser, canvas, nodes, cron, sessions, and Discord/Slack actions.  
	**[一流的工具](https://docs.openclaw.ai/tools)** ——浏览器、画布、节点、定时任务、会话和 Discord/Slack 操作。
- **[Companion apps](https://docs.openclaw.ai/platforms/macos)** — macOS menu bar app + iOS/Android [nodes](https://docs.openclaw.ai/nodes).  
	**[配套应用](https://docs.openclaw.ai/platforms/macos)** — macOS 菜单栏应用 + iOS/Android [节点](https://docs.openclaw.ai/nodes) 。
- **[Onboarding](https://docs.openclaw.ai/start/wizard) + [skills](https://docs.openclaw.ai/tools/skills)** — onboarding-driven setup with bundled/managed/workspace skills.  
	**[入职培训](https://docs.openclaw.ai/start/wizard) + [技能](https://docs.openclaw.ai/tools/skills)** — 以入职培训为导向的设置，包含捆绑式/管理式/工作区技能。

## Star History 星际历史

[![[raw/assets/5ebfedb380fa149594af769e895caa38_MD5.svg]]](https://www.star-history.com/#openclaw/openclaw&type=date&legend=top-left)

## Everything we built so far我们迄今为止所建造的一切

### Core platform 核心平台

- [Gateway WS control plane](https://docs.openclaw.ai/gateway) with sessions, presence, config, cron, webhooks, [Control UI](https://docs.openclaw.ai/web), and [Canvas host](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui).  
	[Gateway WS 控制平面，](https://docs.openclaw.ai/gateway) 包含会话、状态、配置、定时任务、Webhooks、 [控制 UI](https://docs.openclaw.ai/web) 和 [Canvas 主机](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) 。
- [CLI surface](https://docs.openclaw.ai/tools/agent-send): gateway, agent, send, [onboarding](https://docs.openclaw.ai/start/wizard), and [doctor](https://docs.openclaw.ai/gateway/doctor).  
	[CLI 接口](https://docs.openclaw.ai/tools/agent-send) ：网关、代理、发送、 [入职](https://docs.openclaw.ai/start/wizard) 和 [医生](https://docs.openclaw.ai/gateway/doctor) 。
- [Pi agent runtime](https://docs.openclaw.ai/concepts/agent) in RPC mode with tool streaming and block streaming.  
	[Pi 代理运行时环境](https://docs.openclaw.ai/concepts/agent) 采用 RPC 模式，支持工具流式传输和块流式传输。
- [Session model](https://docs.openclaw.ai/concepts/session): `main` for direct chats, group isolation, activation modes, queue modes, reply-back. Group rules: [Groups](https://docs.openclaw.ai/channels/groups).  
	[会话模型](https://docs.openclaw.ai/concepts/session) ： `main` 用于直接聊天、群组隔离、激活模式、队列模式、回复。群组规则： [群组](https://docs.openclaw.ai/channels/groups) 。
- [Media pipeline](https://docs.openclaw.ai/nodes/images): images/audio/video, transcription hooks, size caps, temp file lifecycle. Audio details: [Audio](https://docs.openclaw.ai/nodes/audio).  
	[媒体管道](https://docs.openclaw.ai/nodes/images) ：图像/音频/视频、转录钩子、大小限制、临时文件生命周期。音频详情： [音频](https://docs.openclaw.ai/nodes/audio) 。

### Channels 频道

- [Channels](https://docs.openclaw.ai/channels): [WhatsApp](https://docs.openclaw.ai/channels/whatsapp) (Baileys), [Telegram](https://docs.openclaw.ai/channels/telegram) (grammY), [Slack](https://docs.openclaw.ai/channels/slack) (Bolt), [Discord](https://docs.openclaw.ai/channels/discord) (discord.js), [Google Chat](https://docs.openclaw.ai/channels/googlechat) (Chat API), [Signal](https://docs.openclaw.ai/channels/signal) (signal-cli), [BlueBubbles](https://docs.openclaw.ai/channels/bluebubbles) (iMessage, recommended), [iMessage](https://docs.openclaw.ai/channels/imessage) (legacy imsg), [IRC](https://docs.openclaw.ai/channels/irc), [Microsoft Teams](https://docs.openclaw.ai/channels/msteams), [Matrix](https://docs.openclaw.ai/channels/matrix), [Feishu](https://docs.openclaw.ai/channels/feishu), [LINE](https://docs.openclaw.ai/channels/line), [Mattermost](https://docs.openclaw.ai/channels/mattermost), [Nextcloud Talk](https://docs.openclaw.ai/channels/nextcloud-talk), [Nostr](https://docs.openclaw.ai/channels/nostr), [Synology Chat](https://docs.openclaw.ai/channels/synology-chat), [Tlon](https://docs.openclaw.ai/channels/tlon), [Twitch](https://docs.openclaw.ai/channels/twitch), [Zalo](https://docs.openclaw.ai/channels/zalo), [Zalo Personal](https://docs.openclaw.ai/channels/zalouser), WeChat (`@tencent-weixin/openclaw-weixin`), [WebChat](https://docs.openclaw.ai/web/webchat).  
	[渠道](https://docs.openclaw.ai/channels) ： [WhatsApp](https://docs.openclaw.ai/channels/whatsapp) (Baileys)、 [Telegram](https://docs.openclaw.ai/channels/telegram) (grammY)、 [Slack](https://docs.openclaw.ai/channels/slack) (Bolt)、 [Discord](https://docs.openclaw.ai/channels/discord) (discord.js)、 [Google Chat](https://docs.openclaw.ai/channels/googlechat) (Chat API)、 [Signal](https://docs.openclaw.ai/channels/signal) (signal-cli)、 [BlueBubbles](https://docs.openclaw.ai/channels/bluebubbles) (iMessage，推荐)、 [iMessage](https://docs.openclaw.ai/channels/imessage) (旧版 imsg)、 [IRC](https://docs.openclaw.ai/channels/irc) 、 [Microsoft Teams](https://docs.openclaw.ai/channels/msteams) 、 [Matrix](https://docs.openclaw.ai/channels/matrix) 、 [飞书](https://docs.openclaw.ai/channels/feishu) 、 [LINE](https://docs.openclaw.ai/channels/line) 、 [Mattermost](https://docs.openclaw.ai/channels/mattermost) 、 [Nextcloud Talk](https://docs.openclaw.ai/channels/nextcloud-talk) 、 [Nostr](https://docs.openclaw.ai/channels/nostr) 、 [Synology Chat](https://docs.openclaw.ai/channels/synology-chat) 、 [Tlon](https://docs.openclaw.ai/channels/tlon) 、 [Twitch](https://docs.openclaw.ai/channels/twitch) 、 [Zalo](https://docs.openclaw.ai/channels/zalo) 、 [Zalo Personal](https://docs.openclaw.ai/channels/zalouser) 、微信 ( `@tencent-weixin/openclaw-weixin` )、 [WebChat](https://docs.openclaw.ai/web/webchat) 。
- [Group routing](https://docs.openclaw.ai/channels/group-messages): mention gating, reply tags, per-channel chunking and routing. Channel rules: [Channels](https://docs.openclaw.ai/channels).  
	[群组路由](https://docs.openclaw.ai/channels/group-messages) ：提及门控、回复标签、按频道分块和路由。频道规则： [频道](https://docs.openclaw.ai/channels) 。

### Apps + nodes 应用 + 节点

- [macOS app](https://docs.openclaw.ai/platforms/macos): menu bar control plane, [Voice Wake](https://docs.openclaw.ai/nodes/voicewake) /PTT, [Talk Mode](https://docs.openclaw.ai/nodes/talk) overlay, [WebChat](https://docs.openclaw.ai/web/webchat), debug tools, [remote gateway](https://docs.openclaw.ai/gateway/remote) control.  
	[macOS 应用](https://docs.openclaw.ai/platforms/macos) ：菜单栏控制平面、 [语音唤醒](https://docs.openclaw.ai/nodes/voicewake) /PTT、 [通话模式](https://docs.openclaw.ai/nodes/talk) 叠加、 [WebChat](https://docs.openclaw.ai/web/webchat) 、调试工具、 [远程网关](https://docs.openclaw.ai/gateway/remote) 控制。
- [iOS node](https://docs.openclaw.ai/platforms/ios): [Canvas](https://docs.openclaw.ai/platforms/mac/canvas), [Voice Wake](https://docs.openclaw.ai/nodes/voicewake), [Talk Mode](https://docs.openclaw.ai/nodes/talk), camera, screen recording, Bonjour + device pairing.  
	[iOS 节点](https://docs.openclaw.ai/platforms/ios) ： [Canvas](https://docs.openclaw.ai/platforms/mac/canvas) 、 [语音唤醒](https://docs.openclaw.ai/nodes/voicewake) 、 [通话模式](https://docs.openclaw.ai/nodes/talk) 、相机、屏幕录制、Bonjour + 设备配对。
- [Android node](https://docs.openclaw.ai/platforms/android): Connect tab (setup code/manual), chat sessions, voice tab, [Canvas](https://docs.openclaw.ai/platforms/mac/canvas), camera/screen recording, and Android device commands (notifications/location/SMS/photos/contacts/calendar/motion/app update).  
	[Android 节点](https://docs.openclaw.ai/platforms/android) ：连接选项卡（设置代码/手册）、聊天会话、语音选项卡、 [Canvas](https://docs.openclaw.ai/platforms/mac/canvas) 、相机/屏幕录制和 Android 设备命令（通知/位置/短信/照片/联系人/日历/运动/应用程序更新）。
- [macOS node mode](https://docs.openclaw.ai/nodes): system.run/notify + canvas/camera exposure.  
	[macOS 节点模式](https://docs.openclaw.ai/nodes) ：system.run/notify + canvas/camera 曝光。

### Tools + automation 工具 + 自动化

- [Browser control](https://docs.openclaw.ai/tools/browser): dedicated openclaw Chrome/Chromium, snapshots, actions, uploads, profiles.  
	[浏览器控制](https://docs.openclaw.ai/tools/browser) ：专用 openclaw Chrome/Chromium，快照，操作，上传，配置文件。
- [Canvas](https://docs.openclaw.ai/platforms/mac/canvas): [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) push/reset, eval, snapshot.  
	[Canvas](https://docs.openclaw.ai/platforms/mac/canvas) ： [A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) 推送/重置、评估、快照。
- [Nodes](https://docs.openclaw.ai/nodes): camera snap/clip, screen record, [location.get](https://docs.openclaw.ai/nodes/location-command), notifications.  
	[节点](https://docs.openclaw.ai/nodes) ：相机快照/剪辑、屏幕录制、 [位置获取](https://docs.openclaw.ai/nodes/location-command) 、通知。
- [Cron + wakeups](https://docs.openclaw.ai/automation/cron-jobs); [webhooks](https://docs.openclaw.ai/automation/webhook); [Gmail Pub/Sub](https://docs.openclaw.ai/automation/gmail-pubsub).  
	[Cron + 唤醒](https://docs.openclaw.ai/automation/cron-jobs) ； [webhooks](https://docs.openclaw.ai/automation/webhook) ； [Gmail 发布/订阅](https://docs.openclaw.ai/automation/gmail-pubsub) 。
- [Skills platform](https://docs.openclaw.ai/tools/skills): bundled, managed, and workspace skills with install gating + UI.  
	[技能平台](https://docs.openclaw.ai/tools/skills) ：捆绑式、管理式和工作区技能，具有安装限制和用户界面。

### Runtime + safety 运行时 + 安全性

- [Channel routing](https://docs.openclaw.ai/channels/channel-routing), [retry policy](https://docs.openclaw.ai/concepts/retry), and [streaming/chunking](https://docs.openclaw.ai/concepts/streaming).  
	[通道路由](https://docs.openclaw.ai/channels/channel-routing) 、 [重试策略](https://docs.openclaw.ai/concepts/retry) 和 [流式传输/分块传输](https://docs.openclaw.ai/concepts/streaming) 。
- [Presence](https://docs.openclaw.ai/concepts/presence), [typing indicators](https://docs.openclaw.ai/concepts/typing-indicators), and [usage tracking](https://docs.openclaw.ai/concepts/usage-tracking).  
	[在线状态](https://docs.openclaw.ai/concepts/presence) 、 [输入指示器](https://docs.openclaw.ai/concepts/typing-indicators) 和 [使用情况跟踪](https://docs.openclaw.ai/concepts/usage-tracking) 。
- [Models](https://docs.openclaw.ai/concepts/models), [model failover](https://docs.openclaw.ai/concepts/model-failover), and [session pruning](https://docs.openclaw.ai/concepts/session-pruning).  
	[模型](https://docs.openclaw.ai/concepts/models) 、 [模型故障转移](https://docs.openclaw.ai/concepts/model-failover) 和 [会话修剪](https://docs.openclaw.ai/concepts/session-pruning) 。
- [Security](https://docs.openclaw.ai/gateway/security) and [troubleshooting](https://docs.openclaw.ai/channels/troubleshooting).  
	[安全](https://docs.openclaw.ai/gateway/security) 和 [故障排除](https://docs.openclaw.ai/channels/troubleshooting) 。

### Ops + packaging 运营 + 包装

- [Control UI](https://docs.openclaw.ai/web) + [WebChat](https://docs.openclaw.ai/web/webchat) served directly from the Gateway.  
	[控制界面](https://docs.openclaw.ai/web) + [WebChat](https://docs.openclaw.ai/web/webchat) 直接由网关提供服务。
- [Tailscale Serve/Funnel](https://docs.openclaw.ai/gateway/tailscale) or [SSH tunnels](https://docs.openclaw.ai/gateway/remote) with token/password auth.  
	使用令牌/密码认证的 [Tailscale Serve/Funnel](https://docs.openclaw.ai/gateway/tailscale) 或 [SSH 隧道](https://docs.openclaw.ai/gateway/remote) 。
- [Nix mode](https://docs.openclaw.ai/install/nix) for declarative config; [Docker](https://docs.openclaw.ai/install/docker) -based installs.  
	[Nix 模式](https://docs.openclaw.ai/install/nix) 支持声明式配置；基于 [Docker 的](https://docs.openclaw.ai/install/docker) 安装。
- [Doctor](https://docs.openclaw.ai/gateway/doctor) migrations, [logging](https://docs.openclaw.ai/logging).  
	[医生](https://docs.openclaw.ai/gateway/doctor) 迁移， [日志记录](https://docs.openclaw.ai/logging) 。

## How it works (short) 工作原理（简述）

```
WhatsApp / Telegram / Slack / Discord / Google Chat / Signal / iMessage / BlueBubbles / IRC / Microsoft Teams / Matrix / Feishu / LINE / Mattermost / Nextcloud Talk / Nostr / Synology Chat / Tlon / Twitch / Zalo / Zalo Personal / WeChat / WebChat
               │
               ▼
┌───────────────────────────────┐
│            Gateway            │
│       (control plane)         │
│     ws://127.0.0.1:18789      │
└──────────────┬────────────────┘
               │
               ├─ Pi agent (RPC)
               ├─ CLI (openclaw …)
               ├─ WebChat UI
               ├─ macOS app
               └─ iOS / Android nodes
```

## Key subsystems 关键子系统

- **[Gateway WebSocket network](https://docs.openclaw.ai/concepts/architecture)** — single WS control plane for clients, tools, and events (plus ops: [Gateway runbook](https://docs.openclaw.ai/gateway)).  
	**[Gateway WebSocket 网络](https://docs.openclaw.ai/concepts/architecture)** — 客户端、工具和事件的单一 WS 控制平面（以及操作： [Gateway 运行手册](https://docs.openclaw.ai/gateway) ）。
- **[Tailscale exposure](https://docs.openclaw.ai/gateway/tailscale)** — Serve/Funnel for the Gateway dashboard + WS (remote access: [Remote](https://docs.openclaw.ai/gateway/remote)).  
	**[Tailscale 曝光](https://docs.openclaw.ai/gateway/tailscale)** — 用于 Gateway 仪表板的 Serve/Funnel + WS（远程访问： [远程](https://docs.openclaw.ai/gateway/remote) ）。
- **[Browser control](https://docs.openclaw.ai/tools/browser)** — openclaw‑managed Chrome/Chromium with CDP control.  
	**[浏览器控制](https://docs.openclaw.ai/tools/browser)** ——使用 CDP 控制的 openclaw 管理的 Chrome/Chromium。
- **[Canvas + A2UI](https://docs.openclaw.ai/platforms/mac/canvas)** — agent‑driven visual workspace (A2UI host: [Canvas/A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui)).  
	**[Canvas + A2UI](https://docs.openclaw.ai/platforms/mac/canvas)** — 代理驱动的可视化工作区（A2UI 主机： [Canvas/A2UI](https://docs.openclaw.ai/platforms/mac/canvas#canvas-a2ui) ）。
- **[Voice Wake](https://docs.openclaw.ai/nodes/voicewake) + [Talk Mode](https://docs.openclaw.ai/nodes/talk)** — wake words on macOS/iOS plus continuous voice on Android.  
	**[语音唤醒](https://docs.openclaw.ai/nodes/voicewake) + [通话模式](https://docs.openclaw.ai/nodes/talk)** — macOS/iOS 上的唤醒词加上 Android 上的连续语音。
- **[Nodes](https://docs.openclaw.ai/nodes)** — Canvas, camera snap/clip, screen record, `location.get`, notifications, plus macOS‑only `system.run` / `system.notify`.  
	**[节点](https://docs.openclaw.ai/nodes)** — Canvas、相机快照/剪辑、屏幕录制、 `location.get` 、通知，以及仅限 macOS 的 `system.run` / `system.notify` 。

## Tailscale access (Gateway dashboard)Tailscale 访问权限（网关控制面板）

OpenClaw can auto-configure Tailscale **Serve** (tailnet-only) or **Funnel** (public) while the Gateway stays bound to loopback. Configure `gateway.tailscale.mode`:  
OpenClaw 可以自动配置 Tailscale **Serve** （仅限尾网）或 **Funnel** （公共网络），同时网关保持绑定到环回接口。配置 `gateway.tailscale.mode` ：

- `off`: no Tailscale automation (default).  
	`off` ：不使用 Tailscale 自动化（默认）。
- `serve`: tailnet-only HTTPS via `tailscale serve` (uses Tailscale identity headers by default).  
	`serve` ：仅使用 tailnet 的 HTTPS，通过 `tailscale serve` （默认使用 Tailscale 身份标头）。
- `funnel`: public HTTPS via `tailscale funnel` (requires shared password auth).  
	`funnel` ：通过 `tailscale funnel` 进行公共 HTTPS 访问（需要共享密码认证）。

Notes:笔记：

- `gateway.bind` must stay `loopback` when Serve/Funnel is enabled (OpenClaw enforces this).  
	启用 Serve/Funnel 时， `gateway.bind` 必须保持 `loopback` （OpenClaw 强制执行此操作）。
- Serve can be forced to require a password by setting `gateway.auth.mode: "password"` or `gateway.auth.allowTailscale: false`.  
	可以通过设置 `gateway.auth.mode: "password"` 或 `gateway.auth.allowTailscale: false` 来强制服务器需要密码。
- Funnel refuses to start unless `gateway.auth.mode: "password"` is set.  
	除非设置 `gateway.auth.mode: "password"` 否则 Funnel 拒绝启动。
- Optional: `gateway.tailscale.resetOnExit` to undo Serve/Funnel on shutdown.  
	可选： `gateway.tailscale.resetOnExit` 以在关闭时撤销 Serve/Funnel。

Details: [Tailscale guide](https://docs.openclaw.ai/gateway/tailscale) · [Web surfaces](https://docs.openclaw.ai/web)  
详情： [Tailscale 指南](https://docs.openclaw.ai/gateway/tailscale) · [Web 表面](https://docs.openclaw.ai/web)

## Remote Gateway (Linux is great)远程网关（Linux 真棒）

It’s perfectly fine to run the Gateway on a small Linux instance. Clients (macOS app, CLI, WebChat) can connect over **Tailscale Serve/Funnel** or **SSH tunnels**, and you can still pair device nodes (macOS/iOS/Android) to execute device‑local actions when needed.  
在小型 Linux 实例上运行网关完全没问题。客户端（macOS 应用、CLI、WebChat）可以通过 **Tailscale Serve/Funnel** 或 **SSH 隧道** 连接，并且您仍然可以根据需要将设备节点（macOS/iOS/Android）配对以执行设备本地操作。

- **Gateway host** runs the exec tool and channel connections by default.  
	**网关主机** 默认运行执行工具并建立通道连接。
- **Device nodes** run device‑local actions (`system.run`, camera, screen recording, notifications) via `node.invoke`. In short: exec runs where the Gateway lives; device actions run where the device lives.  
	**设备节点** 通过 `node.invoke` 运行设备本地操作（ `system.run` 、摄像头、屏幕录制、通知）。简而言之：exec 函数在网关所在位置运行；设备操作在设备所在位置运行。

Details: [Remote access](https://docs.openclaw.ai/gateway/remote) · [Nodes](https://docs.openclaw.ai/nodes) · [Security](https://docs.openclaw.ai/gateway/security)  
详情： [远程访问](https://docs.openclaw.ai/gateway/remote) · [节点](https://docs.openclaw.ai/nodes) · [安全性](https://docs.openclaw.ai/gateway/security)

## macOS permissions via the Gateway protocolmacOS 通过 Gateway 协议的权限

The macOS app can run in **node mode** and advertises its capabilities + permission map over the Gateway WebSocket (`node.list` / `node.describe`). Clients can then execute local actions via `node.invoke`:  
macOS 应用可以以 **节点模式** 运行，并通过网关 WebSocket（ `node.list` / `node.describe` ）发布其功能和权限映射。客户端随后可以通过 `node.invoke` 执行本地操作：

- `system.run` runs a local command and returns stdout/stderr/exit code; set `needsScreenRecording: true` to require screen-recording permission (otherwise you’ll get `PERMISSION_MISSING`).  
	`system.run` 运行本地命令并返回 stdout/stderr/退出代码；设置 `needsScreenRecording: true` 以需要屏幕录制权限（否则您将收到 `PERMISSION_MISSING` ）。
- `system.notify` posts a user notification and fails if notifications are denied.  
	`system.notify` 会向用户发送通知，如果通知被拒绝，则会发送失败。
- `canvas.*`, `camera.*`, `screen.record`, and `location.get` are also routed via `node.invoke` and follow TCC permission status.  
	`canvas.*` 、 `camera.*` 、 `screen.record` 和 `location.get` 也通过 `node.invoke` 进行路由，并遵循 TCC 权限状态。

Elevated bash (host permissions) is separate from macOS TCC:  
提升权限的 bash（主机权限）与 macOS TCC 是分开的：

- Use `/elevated on|off` to toggle per‑session elevated access when enabled + allowlisted.  
	使用 `/elevated on|off` 可在启用 + 添加到允许列表时切换每个会话的提升访问权限。
- Gateway persists the per‑session toggle via `sessions.patch` (WS method) alongside `thinkingLevel`, `verboseLevel`, `model`, `sendPolicy`, and `groupActivation`.  
	Gateway 通过 `sessions.patch` （WS 方法）持久化每个会话的切换，以及 `thinkingLevel` 、 `verboseLevel` 、 `model` 、 `sendPolicy` 和 `groupActivation` 。

Details: [Nodes](https://docs.openclaw.ai/nodes) · [macOS app](https://docs.openclaw.ai/platforms/macos) · [Gateway protocol](https://docs.openclaw.ai/concepts/architecture)  
详情： [节点](https://docs.openclaw.ai/nodes) · [macOS 应用](https://docs.openclaw.ai/platforms/macos) · [网关协议](https://docs.openclaw.ai/concepts/architecture)

## Agent to Agent (sessions\_\* tools)代理到代理（sessions\_\* 工具）

- Use these to coordinate work across sessions without jumping between chat surfaces.  
	使用此功能可以跨会话协调工作，而无需在聊天界面之间切换。
- `sessions_list` — discover active sessions (agents) and their metadata.  
	`sessions_list` — 发现活动会话（代理）及其元数据。
- `sessions_history` — fetch transcript logs for a session.  
	`sessions_history` — 获取会话的记录日志。
- `sessions_send` — message another session; optional reply‑back ping‑pong + announce step (`REPLY_SKIP`, `ANNOUNCE_SKIP`).  
	`sessions_send` — 向另一个会话发送消息；可选的回复-ping-pong + 公告步骤（ `REPLY_SKIP` ， `ANNOUNCE_SKIP` ）。

Details: [Session tools](https://docs.openclaw.ai/concepts/session-tool)  
详情： [会话工具](https://docs.openclaw.ai/concepts/session-tool)

## Skills registry (ClawHub)技能注册中心（ClawHub）

ClawHub is a minimal skill registry. With ClawHub enabled, the agent can search for skills automatically and pull in new ones as needed.  
ClawHub 是一个极简的技能注册系统。启用 ClawHub 后，代理可以自动搜索技能，并根据需要添加新技能。

[ClawHub](https://clawhub.com/)

## Chat commands 聊天命令

Send these in WhatsApp/Telegram/Slack/Google Chat/Microsoft Teams/WebChat (group commands are owner-only):  
请通过 WhatsApp/Telegram/Slack/Google Chat/Microsoft Teams/WebChat 发送这些内容（群组命令仅限群主使用）：

- `/status` — compact session status (model + tokens, cost when available)  
	`/status` — 精简会话状态（模型 + 令牌，以及可用时的费用）
- `/new` or `/reset` — reset the session  
	`/new` 或 `/reset` — 重置会话
- `/compact` — compact session context (summary)  
	`/compact` — 精简会话上下文（摘要）
- `/think <level>` — off|minimal|low|medium|high|xhigh (GPT-5.2 + Codex models only)  
	`/think <level>` — 关闭|最低|低|中|高|超高（仅限 GPT-5.2 和 Codex 型号）
- `/verbose on|off`
- `/usage off|tokens|full` — per-response usage footer  
	`/usage off|tokens|full` — 每个响应的使用情况页脚
- `/restart` — restart the gateway (owner-only in groups)  
	`/restart` — 重启网关（仅限群组所有者）
- `/activation mention|always` — group activation toggle (groups only)  
	`/activation mention|always` — 群组激活切换（仅限群组）

## Apps (optional) 应用（可选）

The Gateway alone delivers a great experience. All apps are optional and add extra features.  
网关本身就能提供出色的体验。所有应用程序均为可选，并添加额外功能。

If you plan to build/run companion apps, follow the platform runbooks below.  
如果您计划构建/运行配套应用程序，请遵循以下平台运行手册。

### macOS (OpenClaw.app) (optional)macOS（OpenClaw.app）（可选）

- Menu bar control for the Gateway and health.  
	用于网关和健康状况的菜单栏控制。
- Voice Wake + push-to-talk overlay.  
	语音唤醒 + 一键通话叠加功能。
- WebChat + debug tools.  
	WebChat + 调试工具。
- Remote gateway control over SSH.  
	通过 SSH 进行远程网关控制。

Note: signed builds required for macOS permissions to stick across rebuilds (see [macOS Permissions](https://docs.openclaw.ai/platforms/mac/permissions)).  
注意：需要使用已签名的构建版本，才能使 macOS 权限在重新构建后仍然有效（请参阅 [macOS 权限](https://docs.openclaw.ai/platforms/mac/permissions) ）。

### iOS node (optional) iOS 节点（可选）

- Pairs as a node over the Gateway WebSocket (device pairing).  
	通过网关 WebSocket 进行节点配对（设备配对）。
- Voice trigger forwarding + Canvas surface.  
	语音触发转发 + Canvas 表面。
- Controlled via `openclaw nodes …`.  
	通过 `openclaw nodes …`

Runbook: [iOS connect](https://docs.openclaw.ai/platforms/ios).  
Runbook： [iOS 连接](https://docs.openclaw.ai/platforms/ios) 。

### Android node (optional) Android 节点（可选）

- Pairs as a WS node via device pairing (`openclaw devices ...`).  
	通过设备配对（ `openclaw devices ...` ）作为 WS 节点配对。
- Exposes Connect/Chat/Voice tabs plus Canvas, Camera, Screen capture, and Android device command families.  
	显示“连接/聊天/语音”选项卡以及“画布”、“相机”、“屏幕截图”和“Android 设备命令”系列。
- Runbook: [Android connect](https://docs.openclaw.ai/platforms/android).  
	Runbook： [Android 连接](https://docs.openclaw.ai/platforms/android) 。

## Agent workspace + skills 代理工作区 + 技能

- Workspace root: `~/.openclaw/workspace` (configurable via `agents.defaults.workspace`).  
	工作区根目录： `~/.openclaw/workspace` （可通过 `agents.defaults.workspace` 配置）。
- Injected prompt files: `AGENTS.md`, `SOUL.md`, `TOOLS.md`.  
	注入的提示文件： `AGENTS.md` 、 `SOUL.md` 、 `TOOLS.md` 。
- Skills: `~/.openclaw/workspace/skills/<skill>/SKILL.md`.技能： `~/.openclaw/workspace/skills/<skill>/SKILL.md` 。

## Configuration 配置

Minimal `~/.openclaw/openclaw.json` (model + defaults):  
最简 `~/.openclaw/openclaw.json` （模型 + 默认值）：

```
{
  agent: {
    model: "<provider>/<model-id>",
  },
}
```

[Full configuration reference (all keys + examples).  
完整配置参考（所有键 + 示例）。](https://docs.openclaw.ai/gateway/configuration)

## Security model (important)安全模型（重要）

- **Default:** tools run on the host for the **main** session, so the agent has full access when it’s just you.  
	**默认设置：** 工具在主机上运行以进行 **主** 会话，因此当只有您一个人时，代理拥有完全访问权限。
- **Group/channel safety:** set `agents.defaults.sandbox.mode: "non-main"` to run **non‑main sessions** (groups/channels) inside per‑session Docker sandboxes; bash then runs in Docker for those sessions.  
	**组/通道安全：** 设置 `agents.defaults.sandbox.mode: "non-main"` 以在每个会话的 Docker 沙箱中运行 **非主会话** （组/通道）；然后 bash 在 Docker 中为这些会话运行。
- **Sandbox defaults:** allowlist `bash`, `process`, `read`, `write`, `edit`, `sessions_list`, `sessions_history`, `sessions_send`, `sessions_spawn`; denylist `browser`, `canvas`, `nodes`, `cron`, `discord`, `gateway`.  
	**沙箱默认值：** 允许列表 `bash` 、 `process` 、 `read` 、 `write` 、 `edit` 、 `sessions_list` 、 `sessions_history` 、 `sessions_send` 、 `sessions_spawn` ；拒绝列表 `browser` 、 `canvas` 、 `nodes` 、 `cron` 、 `discord` 、 `gateway` 。

Details: [Security guide](https://docs.openclaw.ai/gateway/security) · [Docker + sandboxing](https://docs.openclaw.ai/install/docker) · [Sandbox config](https://docs.openclaw.ai/gateway/configuration)  
详情： [安全指南](https://docs.openclaw.ai/gateway/security) · [Docker + 沙箱](https://docs.openclaw.ai/install/docker) · [沙箱配置](https://docs.openclaw.ai/gateway/configuration)

### WhatsApp

- Link the device: `pnpm openclaw channels login` (stores creds in `~/.openclaw/credentials`).  
	连接设备： `pnpm openclaw channels login` （将凭据存储在 `~/.openclaw/credentials` 中）。
- Allowlist who can talk to the assistant via `channels.whatsapp.allowFrom`.  
	允许列表允许谁通过 `channels.whatsapp.allowFrom` 与助理交谈。
- If `channels.whatsapp.groups` is set, it becomes a group allowlist; include `"*"` to allow all.  
	如果设置了 `channels.whatsapp.groups` ，它将成为一个群组允许列表；包含 `"*"` 以允许所有群组。

### Telegram 电报

- Set `TELEGRAM_BOT_TOKEN` or `channels.telegram.botToken` (env wins).  
	设置 `TELEGRAM_BOT_TOKEN` 或 `channels.telegram.botToken` （环境变量优先）。
- Optional: set `channels.telegram.groups` (with `channels.telegram.groups."*".requireMention`); when set, it is a group allowlist (include `"*"` to allow all). Also `channels.telegram.allowFrom` or `channels.telegram.webhookUrl` + `channels.telegram.webhookSecret` as needed.  
	可选：设置 `channels.telegram.groups` （使用 `channels.telegram.groups."*".requireMention` ）；设置后，它将成为一个群组允许列表（包含 `"*"` 以允许所有群组）。根据需要，还可以设置 `channels.telegram.allowFrom` 或 `channels.telegram.webhookUrl` + `channels.telegram.webhookSecret` 。
```
{
  channels: {
    telegram: {
      botToken: "123456:ABCDEF",
    },
  },
}
```

### Slack 松弛

- Set `SLACK_BOT_TOKEN` + `SLACK_APP_TOKEN` (or `channels.slack.botToken` + `channels.slack.appToken`).  
	设置 `SLACK_BOT_TOKEN` + `SLACK_APP_TOKEN` （或 `channels.slack.botToken` + `channels.slack.appToken` ）。

### Discord

- Set `DISCORD_BOT_TOKEN` or `channels.discord.token`.  
	设置 `DISCORD_BOT_TOKEN` 或 `channels.discord.token` 。
- Optional: set `commands.native`, `commands.text`, or `commands.useAccessGroups`, plus `channels.discord.allowFrom`, `channels.discord.guilds`, or `channels.discord.mediaMaxMb` as needed.  
	可选：根据需要设置 `commands.native` 、 `commands.text` 或 `commands.useAccessGroups` ，以及 `channels.discord.allowFrom` 、 `channels.discord.guilds` 或 `channels.discord.mediaMaxMb` 。
```
{
  channels: {
    discord: {
      token: "1234abcd",
    },
  },
}
```

### Signal 信号

- Requires `signal-cli` and a `channels.signal` config section.  
	需要 `signal-cli` 和 `channels.signal` 配置部分。

### BlueBubbles (iMessage) BlueBubbles（iMessage）

- **Recommended** iMessage integration.  
	**推荐的** iMessage 集成方案。
- Configure `channels.bluebubbles.serverUrl` + `channels.bluebubbles.password` and a webhook (`channels.bluebubbles.webhookPath`).  
	配置 `channels.bluebubbles.serverUrl` + `channels.bluebubbles.password` 和 webhook ( `channels.bluebubbles.webhookPath` )。
- The BlueBubbles server runs on macOS; the Gateway can run on macOS or elsewhere.  
	BlueBubbles 服务器运行在 macOS 上；网关可以运行在 macOS 或其他系统上。

### iMessage (legacy) iMessage（旧版）

- Legacy macOS-only integration via `imsg` (Messages must be signed in).  
	仅限 macOS 的传统集成方式是通过 `imsg` （必须登录“信息”应用）。
- If `channels.imessage.groups` is set, it becomes a group allowlist; include `"*"` to allow all.  
	如果设置了 `channels.imessage.groups` ，它将变成一个组允许列表；包含 `"*"` 以允许所有组。

### Microsoft Teams 微软团队

- Configure a Teams app + Bot Framework, then add a `msteams` config section.  
	配置 Teams 应用 + Bot Framework，然后添加 `msteams` 配置部分。
- Allowlist who can talk via `msteams.allowFrom`; group access via `msteams.groupAllowFrom` or `msteams.groupPolicy: "open"`.  
	通过 `msteams.allowFrom` 设置允许发言的用户列表；通过 `msteams.groupAllowFrom` 或 `msteams.groupPolicy: "open"` 。

### WeChat 微信

- Official Tencent plugin via [`@tencent-weixin/openclaw-weixin`](https://www.npmjs.com/package/@tencent-weixin/openclaw-weixin) (iLink Bot API). Private chats only; v2.x requires OpenClaw `>=2026.3.22`.  
	腾讯官方插件，通过 [`@tencent-weixin/openclaw-weixin`](https://www.npmjs.com/package/@tencent-weixin/openclaw-weixin) （iLink Bot API）。仅限私聊；v2.x 需要 OpenClaw `>=2026.3.22` 。
- Install: `openclaw plugins install "@tencent-weixin/openclaw-weixin"`, then `openclaw channels login --channel openclaw-weixin` to scan the QR code.  
	安装： `openclaw plugins install "@tencent-weixin/openclaw-weixin"` ，然后 `openclaw channels login --channel openclaw-weixin` 扫描二维码。
- Requires the WeChat ClawBot plugin (WeChat > Me > Settings > Plugins); gradual rollout by Tencent.  
	需要微信 ClawBot 插件（微信 > 我 > 设置 > 插件）；腾讯正在逐步推出。

### WebChat 网络聊天

- Uses the Gateway WebSocket; no separate WebChat port/config.  
	使用网关 WebSocket；没有单独的 WebChat 端口/配置。

Browser control (optional):  
浏览器控制（可选）：

```
{
  browser: {
    enabled: true,
    color: "#FF4500",
  },
}
```

## Docs 文档

Use these when you’re past the onboarding flow and want the deeper reference.  
当你完成新手引导流程并需要更深入的参考资料时，可以使用这些资料。

- [Start with the docs index for navigation and “what’s where.”  
	首先查看文档索引，了解导航和“内容位置”。](https://docs.openclaw.ai/)
- [Read the architecture overview for the gateway + protocol model.  
	请阅读网关+协议模型的架构概述。](https://docs.openclaw.ai/concepts/architecture)
- [Use the full configuration reference when you need every key and example.  
	需要所有键值和示例时，请使用完整的配置参考文档。](https://docs.openclaw.ai/gateway/configuration)
- [Run the Gateway by the book with the operational runbook.  
	严格按照操作手册运行网关。](https://docs.openclaw.ai/gateway)
- [Learn how the Control UI/Web surfaces work and how to expose them safely.  
	了解控件 UI/Web 界面的工作原理以及如何安全地公开它们。](https://docs.openclaw.ai/web)
- [Understand remote access over SSH tunnels or tailnets.  
	了解通过 SSH 隧道或尾网进行远程访问。](https://docs.openclaw.ai/gateway/remote)
- [Follow OpenClaw Onboard for a guided setup.  
	请按照 OpenClaw Onboard 的引导进行设置。](https://docs.openclaw.ai/start/wizard)
- [Wire external triggers via the webhook surface.  
	通过 webhook 接口连接外部触发器。](https://docs.openclaw.ai/automation/webhook)
- [Set up Gmail Pub/Sub triggers.  
	设置 Gmail 发布/订阅触发器。](https://docs.openclaw.ai/automation/gmail-pubsub)
- [Learn the macOS menu bar companion details.  
	了解 macOS 菜单栏助手的详细信息。](https://docs.openclaw.ai/platforms/mac/menu-bar)
- [Platform guides: Windows (WSL2)](https://docs.openclaw.ai/platforms/windows), [Linux](https://docs.openclaw.ai/platforms/linux), [macOS](https://docs.openclaw.ai/platforms/macos), [iOS](https://docs.openclaw.ai/platforms/ios), [Android](https://docs.openclaw.ai/platforms/android)  
	[平台指南：Windows (WSL2)](https://docs.openclaw.ai/platforms/windows) 、 [Linux](https://docs.openclaw.ai/platforms/linux) 、 [macOS](https://docs.openclaw.ai/platforms/macos) 、 [iOS](https://docs.openclaw.ai/platforms/ios) 、 [Android](https://docs.openclaw.ai/platforms/android)
- [Debug common failures with the troubleshooting guide.  
	使用故障排除指南排查常见故障。](https://docs.openclaw.ai/channels/troubleshooting)
- [Review security guidance before exposing anything.  
	在泄露任何信息之前，请先阅读安全指南。](https://docs.openclaw.ai/gateway/security)

## Advanced docs (discovery + control)高级文档（发现 + 控制）

- [Discovery + transports 发现 + 运输](https://docs.openclaw.ai/gateway/discovery)
- [Bonjour/mDNS 你好/mDNS](https://docs.openclaw.ai/gateway/bonjour)
- [Gateway pairing 网关配对](https://docs.openclaw.ai/gateway/pairing)
- [Remote gateway README 远程网关自述文件](https://docs.openclaw.ai/gateway/remote-gateway-readme)
- [Control UI 控制界面](https://docs.openclaw.ai/web/control-ui)
- [Dashboard 仪表板](https://docs.openclaw.ai/web/dashboard)

## Operations & troubleshooting操作与故障排除

- [Health checks 健康检查](https://docs.openclaw.ai/gateway/health)
- [Gateway lock 网关锁](https://docs.openclaw.ai/gateway/gateway-lock)
- [Background process 背景过程](https://docs.openclaw.ai/gateway/background-process)
- [Browser troubleshooting (Linux)  
	浏览器故障排除（Linux）](https://docs.openclaw.ai/tools/browser-linux-troubleshooting)
- [Logging 日志记录](https://docs.openclaw.ai/logging)

## Deep dives 深度探索

- [Agent loop 代理循环](https://docs.openclaw.ai/concepts/agent-loop)
- [Presence 在场](https://docs.openclaw.ai/concepts/presence)
- [TypeBox schemas TypeBox 架构](https://docs.openclaw.ai/concepts/typebox)
- [RPC adapters RPC 适配器](https://docs.openclaw.ai/reference/rpc)
- [Queue 队列](https://docs.openclaw.ai/concepts/queue)

## Workspace & skills 工作空间和技能

- [Skills config 技能配置](https://docs.openclaw.ai/tools/skills-config)
- [Default AGENTS 默认代理](https://docs.openclaw.ai/reference/AGENTS.default)
- [Templates: AGENTS 模板：代理](https://docs.openclaw.ai/reference/templates/AGENTS)
- [Templates: BOOTSTRAP 模板：BOOTSTRAP](https://docs.openclaw.ai/reference/templates/BOOTSTRAP)
- [Templates: IDENTITY 模板：身份](https://docs.openclaw.ai/reference/templates/IDENTITY)
- [Templates: SOUL 模板：灵魂](https://docs.openclaw.ai/reference/templates/SOUL)
- [Templates: TOOLS 模板：工具](https://docs.openclaw.ai/reference/templates/TOOLS)
- [Templates: USER 模板：用户](https://docs.openclaw.ai/reference/templates/USER)

## Platform internals 平台内部结构

- [macOS dev setup macOS 开发配置](https://docs.openclaw.ai/platforms/mac/dev-setup)
- [macOS menu bar macOS 菜单栏](https://docs.openclaw.ai/platforms/mac/menu-bar)
- [macOS voice wake macOS 语音唤醒](https://docs.openclaw.ai/platforms/mac/voicewake)
- [iOS node iOS 节点](https://docs.openclaw.ai/platforms/ios)
- [Android node Android 节点](https://docs.openclaw.ai/platforms/android)
- [Windows (WSL2)](https://docs.openclaw.ai/platforms/windows)
- [Linux app Linux 应用](https://docs.openclaw.ai/platforms/linux)

## Email hooks (Gmail) 电子邮件钩子（Gmail）

- [docs.openclaw.ai/gmail-pubsub](https://docs.openclaw.ai/automation/gmail-pubsub)

## Molty 莫尔蒂

OpenClaw was built for **Molty**, a space lobster AI assistant. 🦞 by Peter Steinberger and the community.  
OpenClaw 是为 **Molty** （一款太空龙虾 AI 助手）而开发的。🦞 由 Peter Steinberger 和社区共同打造。

- [openclaw.ai](https://openclaw.ai/)
- [soul.md](https://soul.md/)
- [steipete.me](https://steipete.me/)

## Community 社区

See [CONTRIBUTING.md](https://github.com/openclaw/openclaw/blob/main/CONTRIBUTING.md) for guidelines, maintainers, and how to submit PRs. AI/vibe-coded PRs welcome! 🤖  
请参阅 [CONTRIBUTING.md](https://github.com/openclaw/openclaw/blob/main/CONTRIBUTING.md) 文件，了解贡献指南、维护者信息以及如何提交 PR。欢迎提交 AI/vibe 编码的 PR！🤖

Special thanks to [Mario Zechner](https://mariozechner.at/) for his support and for [pi-mono](https://github.com/badlogic/pi-mono). Special thanks to Adam Doppelt for lobster.bot.  
特别感谢 [Mario Zechner](https://mariozechner.at/) 的支持和帮助 [pi-mono](https://github.com/badlogic/pi-mono) 。特别感谢 Adam Doppelt 开发的 lobster.bot。
