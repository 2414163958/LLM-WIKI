---
title: "NousResearch/hermes-agent: The agent that grows with you"
source: "https://github.com/NousResearch/hermes-agent"
author:
published:
created: 2026-04-13
description: "The agent that grows with you. Contribute to NousResearch/hermes-agent development by creating an account on GitHub."
tags:
  - "clippings"
---
[![[raw/assets/799a7f85a6cd2ee30f64fd9d7763519e_MD5.png]]](https://github.com/NousResearch/hermes-agent/blob/main/assets/banner.png)

## Hermes Agent ☤ 赫尔墨斯代理人☤

**The self-improving AI agent built by [Nous Research](https://nousresearch.com/).** It's the only agent with a built-in learning loop — it creates skills from experience, improves them during use, nudges itself to persist knowledge, searches its own past conversations, and builds a deepening model of who you are across sessions. Run it on a $5 VPS, a GPU cluster, or serverless infrastructure that costs nearly nothing when idle. It's not tied to your laptop — talk to it from Telegram while it works on a cloud VM.  
**[Nous Research](https://nousresearch.com/) 开发的这款自学习型 AI 智能体，** 是唯一一款内置学习循环的智能体——它能从经验中积累技能，在使用过程中不断改进，持续学习并巩固知识，还能搜索过往对话记录，并在不同会话中逐步构建更深入的自我认知模型。它可以运行在 5 美元的 VPS、GPU 集群或几乎零成本的无服务器基础设施上。它不依赖于你的笔记本电脑——即使它在云端虚拟机上运行，你也可以通过 Telegram 与它互动。

Use any model you want — [Nous Portal](https://portal.nousresearch.com/), [OpenRouter](https://openrouter.ai/) (200+ models), [z.ai/GLM](https://z.ai/), [Kimi/Moonshot](https://platform.moonshot.ai/), [MiniMax](https://www.minimax.io/), OpenAI, or your own endpoint. Switch with `hermes model` — no code changes, no lock-in.  
您可以随意选择模型——Nous [Portal](https://portal.nousresearch.com/) 、 [OpenRouter](https://openrouter.ai/) （200 多种模型）、 [z.ai/GLM](https://z.ai/) 、 [Kimi/Moonshot](https://platform.moonshot.ai/) 、 [MiniMax](https://www.minimax.io/) 、OpenAI，或者您自己的端点。使用 `hermes model` 即可轻松切换——无需修改代码，也无需担心被锁定。

| **A real terminal interface   真正的终端接口** | Full TUI with multiline editing, slash-command autocomplete, conversation history, interrupt-and-redirect, and streaming tool output.   完整的 TUI，支持多行编辑、斜杠命令自动完成、对话历史记录、中断和重定向以及流媒体工具输出。 |
| --- | --- |
| **Lives where you do 住在你那里** | Telegram, Discord, Slack, WhatsApp, Signal, and CLI — all from a single gateway process. Voice memo transcription, cross-platform conversation continuity.   Telegram、Discord、Slack、WhatsApp、Signal 和 CLI——全部通过单一网关进程实现。语音备忘录转录，跨平台对话无缝衔接。 |
| **A closed learning loop 闭环学习** | Agent-curated memory with periodic nudges. Autonomous skill creation after complex tasks. Skills self-improve during use. FTS5 session search with LLM summarization for cross-session recall. [Honcho](https://github.com/plastic-labs/honcho) dialectic user modeling. Compatible with the [agentskills.io](https://agentskills.io/) open standard.   智能体管理的记忆，并定期进行提示。复杂任务完成后自主创建技能。技能在使用过程中自我提升。FTS5 会话搜索 [，](https://github.com/plastic-labs/honcho) 结合 LLM 摘要实现跨会话回忆。Honcho 辩证用户建模。兼容 [agentskills.io](https://agentskills.io/) 开放标准。 |
| **Scheduled automations 定时自动化** | Built-in cron scheduler with delivery to any platform. Daily reports, nightly backups, weekly audits — all in natural language, running unattended.   内置定时任务调度器，支持向任何平台推送。每日报告、夜间备份、每周审计——所有操作均以自然语言进行，无需人工干预即可运行。 |
| **Delegates and parallelizes   委托和并行化** | Spawn isolated subagents for parallel workstreams. Write Python scripts that call tools via RPC, collapsing multi-step pipelines into zero-context-cost turns.   为并行工作流生成独立的子代理。编写 Python 脚本，通过 RPC 调用工具，将多步骤管道简化为零上下文成本的回合。 |
| **Runs anywhere, not just your laptop   可在任何地方运行，不仅限于笔记本电脑** | Six terminal backends — local, Docker, SSH, Daytona, Singularity, and Modal. Daytona and Modal offer serverless persistence — your agent's environment hibernates when idle and wakes on demand, costing nearly nothing between sessions. Run it on a $5 VPS or a GPU cluster.   六种终端后端——本地、Docker、SSH、Daytona、Singularity 和 Modal。Daytona 和 Modal 提供无服务器持久化——代理环境在空闲时进入休眠状态，并在需要时唤醒，会话间几乎不产生任何开销。可在 5 美元的 VPS 或 GPU 集群上运行。 |
| **Research-ready 研究就绪** | Batch trajectory generation, Atropos RL environments, trajectory compression for training the next generation of tool-calling models.   批量轨迹生成、Atropos RL 环境、轨迹压缩，用于训练下一代工具调用模型。 |

---

## Quick Install 快速安装

```
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

Works on Linux, macOS, WSL2, and Android via Termux. The installer handles the platform-specific setup for you.  
可在 Linux、macOS、WSL2 和 Android（通过 Termux）上运行。安装程序会自动处理平台特定的设置。

> **Android / Termux:** The tested manual path is documented in the [Termux guide](https://hermes-agent.nousresearch.com/docs/getting-started/termux). On Termux, Hermes installs a curated `.[termux]` extra because the full `.[all]` extra currently pulls Android-incompatible voice dependencies.  
> **Android / Termux：** 经测试的手动安装路径已记录在 [Termux 指南](https://hermes-agent.nousresearch.com/docs/getting-started/termux) 中。在 Termux 上，Hermes 安装的是一个经过筛选的 `.[termux]` 扩展包，因为完整的 `.[all]` 扩展包目前会引入与 Android 不兼容的语音依赖项。
> 
> **Windows:** Native Windows is not supported. Please install [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) and run the command above.  
> **Windows：** 不支持原生 Windows 系统。请安装 [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) 并运行上述命令。

After installation:安装后：

```
source ~/.bashrc    # reload shell (or: source ~/.zshrc)
hermes              # start chatting!
```

---

## Getting Started 入门

```
hermes              # Interactive CLI — start a conversation
hermes model        # Choose your LLM provider and model
hermes tools        # Configure which tools are enabled
hermes config set   # Set individual config values
hermes gateway      # Start the messaging gateway (Telegram, Discord, etc.)
hermes setup        # Run the full setup wizard (configures everything at once)
hermes claw migrate # Migrate from OpenClaw (if coming from OpenClaw)
hermes update       # Update to the latest version
hermes doctor       # Diagnose any issues
```

📖 **[Full documentation →](https://hermes-agent.nousresearch.com/docs/)**  
📖 **[完整文档→](https://hermes-agent.nousresearch.com/docs/)**

## CLI vs Messaging Quick ReferenceCLI 与消息传递快速参考

Hermes has two entry points: start the terminal UI with `hermes`, or run the gateway and talk to it from Telegram, Discord, Slack, WhatsApp, Signal, or Email. Once you're in a conversation, many slash commands are shared across both interfaces.  
Hermes 提供两种入口：使用 `hermes` 命令启动终端界面，或者运行网关并通过 Telegram、Discord、Slack、WhatsApp、Signal 或电子邮件与其通信。一旦进入对话，许多斜杠命令在两种界面中都是通用的。

| Action 行动 | CLI | Messaging platforms 即时通讯平台 |
| --- | --- | --- |
| Start chatting 开始聊天 | `hermes` 爱马仕 | Run `hermes gateway setup` + `hermes gateway start`, then send the bot a message   运行 `hermes gateway setup` 和 `hermes gateway start` 命令，然后向机器人发送消息。 |
| Start fresh conversation   开启新的对话 | `/new` or `/reset`   `/new` 或 `/reset` | `/new` or `/reset`   `/new` 或 `/reset` |
| Change model 改变模式 | `/model [provider:model]` | `/model [provider:model]` |
| Set a personality 塑造个性 | `/personality [name]` /个性\[姓名\] | `/personality [name]` /个性\[姓名\] |
| Retry or undo the last turn   重试或撤销上一回合 | `/retry`, `/undo`   `/retry` ， `/undo` | `/retry`, `/undo`   `/retry` ， `/undo` |
| Compress context / check usage   压缩上下文/检查使用情况 | `/compress`, `/usage`, `/insights [--days N]`   `/compress` 、 `/usage` 、 `/insights [--days N]` | `/compress`, `/usage`, `/insights [days]`   `/compress` 、 `/usage` 、 `/insights [days]` |
| Browse skills 浏览技能 | `/skills` or `/<skill-name>`   `/skills` 或 `/<skill-name>` | `/skills` or `/<skill-name>`   `/skills` 或 `/<skill-name>` |
| Interrupt current work 中断当前工作 | `Ctrl+C` or send a new message   `Ctrl+C` 或发送新消息 | `/stop` or send a new message   `/stop` 或发送新消息 |
| Platform-specific status   平台特定状态 | `/platforms` | `/status`, `/sethome`   `/status` ， `/sethome` |

For the full command lists, see the [CLI guide](https://hermes-agent.nousresearch.com/docs/user-guide/cli) and the [Messaging Gateway guide](https://hermes-agent.nousresearch.com/docs/user-guide/messaging).  
有关完整的命令列表，请参阅 [CLI 指南](https://hermes-agent.nousresearch.com/docs/user-guide/cli) 和 [消息网关指南](https://hermes-agent.nousresearch.com/docs/user-guide/messaging) 。

---

## Documentation 文档

All documentation lives at **[hermes-agent.nousresearch.com/docs](https://hermes-agent.nousresearch.com/docs/)**:  
所有文档都位于 **[hermes-agent.nousresearch.com/docs](https://hermes-agent.nousresearch.com/docs/)** ：

| Section 部分 | What's Covered 涵盖范围 |
| --- | --- |
| [Quickstart 快速入门](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart) | Install → setup → first conversation in 2 minutes   安装 → 设置 → 2 分钟内即可进行首次对话 |
| [CLI Usage CLI 用法](https://hermes-agent.nousresearch.com/docs/user-guide/cli) | Commands, keybindings, personalities, sessions   命令、快捷键、个性化设置、会话 |
| [Configuration 配置](https://hermes-agent.nousresearch.com/docs/user-guide/configuration) | Config file, providers, models, all options   配置文件、提供程序、模型、所有选项 |
| [Messaging Gateway 消息网关](https://hermes-agent.nousresearch.com/docs/user-guide/messaging) | Telegram, Discord, Slack, WhatsApp, Signal, Home Assistant   Telegram、Discord、Slack、WhatsApp、Signal、Home Assistant |
| [Security 安全](https://hermes-agent.nousresearch.com/docs/user-guide/security) | Command approval, DM pairing, container isolation   命令批准、DM 配对、容器隔离 |
| [Tools & Toolsets 工具和工具集](https://hermes-agent.nousresearch.com/docs/user-guide/features/tools) | 40+ tools, toolset system, terminal backends   40多种工具、工具集系统、终端后端 |
| [Skills System 技能系统](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) | Procedural memory, Skills Hub, creating skills   程序性记忆、技能中心、技能创造 |
| [Memory 记忆](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory) | Persistent memory, user profiles, best practices   持久内存、用户配置文件、最佳实践 |
| [MCP Integration MCP 集成](https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp) | Connect any MCP server for extended capabilities   连接任何 MCP 服务器以扩展功能 |
| [Cron Scheduling 定时任务](https://hermes-agent.nousresearch.com/docs/user-guide/features/cron) | Scheduled tasks with platform delivery   平台交付的计划任务 |
| [Context Files 上下文文件](https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files) | Project context that shapes every conversation   项目背景影响着每一次对话 |
| [Architecture 建筑学](https://hermes-agent.nousresearch.com/docs/developer-guide/architecture) | Project structure, agent loop, key classes   项目结构、代理循环、关键类 |
| [Contributing 贡献](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) | Development setup, PR process, code style   开发环境、PR 流程、代码风格 |
| [CLI Reference CLI 参考](https://hermes-agent.nousresearch.com/docs/reference/cli-commands) | All commands and flags   所有命令和标志 |
| [Environment Variables 环境变量](https://hermes-agent.nousresearch.com/docs/reference/environment-variables) | Complete env var reference   完整的环境变量引用 |

---

## Migrating from OpenClaw 从 OpenClaw 迁移

If you're coming from OpenClaw, Hermes can automatically import your settings, memories, skills, and API keys.  
如果您之前使用过 OpenClaw，Hermes 可以自动导入您的设置、记忆、技能和 API 密钥。

**During first-time setup:** The setup wizard (`hermes setup`) automatically detects `~/.openclaw` and offers to migrate before configuration begins.  
**首次设置时：** 设置向导（ `hermes setup` ）会自动检测 `~/.openclaw` 并提示在配置开始前进行迁移。

**Anytime after install:安装后任何时间：**

```
hermes claw migrate              # Interactive migration (full preset)
hermes claw migrate --dry-run    # Preview what would be migrated
hermes claw migrate --preset user-data   # Migrate without secrets
hermes claw migrate --overwrite  # Overwrite existing conflicts
```

What gets imported:导入的内容：

- **SOUL.md** — persona file  
	**SOUL.md** — 角色文件
- **Memories** — MEMORY.md and USER.md entries  
	**内存** — MEMORY.md 和 USER.md 条目
- **Skills** — user-created skills → `~/.hermes/skills/openclaw-imports/`  
	**技能** — 用户创建的技能 → `~/.hermes/skills/openclaw-imports/`
- **Command allowlist** — approval patterns  
	**命令允许列表** — 审批模式
- **Messaging settings** — platform configs, allowed users, working directory  
	**消息传递设置** — 平台配置、允许的用户、工作目录
- **API keys** — allowlisted secrets (Telegram, OpenRouter, OpenAI, Anthropic, ElevenLabs)  
	**API 密钥** — 已列入允许列表的密钥（Telegram、OpenRouter、OpenAI、Anthropic、ElevenLabs）
- **TTS assets** — workspace audio files  
	**TTS 资源** ——工作区音频文件
- **Workspace instructions** — AGENTS.md (with `--workspace-target`)  
	**工作区指令** — AGENTS.md（使用 `--workspace-target` ）

See `hermes claw migrate --help` for all options, or use the `openclaw-migration` skill for an interactive agent-guided migration with dry-run previews.  
有关所有选项，请参阅 `hermes claw migrate --help` ，或使用 `openclaw-migration` 技能进行交互式代理引导迁移，并可进行试运行预览。

---

## Contributing 贡献

We welcome contributions! See the [Contributing Guide](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) for development setup, code style, and PR process.  
我们欢迎大家贡献代码！请参阅 [贡献指南](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) ，了解开发环境设置、代码风格和 PR 流程。

Quick start for contributors:  
贡献者快速入门指南：

```
git clone https://github.com/NousResearch/hermes-agent.git
cd hermes-agent
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv venv --python 3.11
source venv/bin/activate
uv pip install -e ".[all,dev]"
python -m pytest tests/ -q
```

> **RL Training (optional):** To work on the RL/Tinker-Atropos integration:  
> **强化学习训练（可选）：** 用于强化学习/Tinker-Atropos 集成：
> 
> ```
> git submodule update --init tinker-atropos
> uv pip install -e "./tinker-atropos"
> ```

---

## Community 社区

- 💬 [Discord](https://discord.gg/NousResearch)
- 📚 [Skills Hub](https://agentskills.io/)  
	📚 [技能中心](https://agentskills.io/)
- 🐛 [Issues](https://github.com/NousResearch/hermes-agent/issues) 🐛 [问题](https://github.com/NousResearch/hermes-agent/issues)
- 💡 [Discussions](https://github.com/NousResearch/hermes-agent/discussions)  
	💡 [讨论](https://github.com/NousResearch/hermes-agent/discussions)
- 🔌 [HermesClaw](https://github.com/AaronWong1999/hermesclaw) — Community WeChat bridge: Run Hermes Agent and OpenClaw on the same WeChat account.  
	🔌 [HermesClaw](https://github.com/AaronWong1999/hermesclaw) — 社区微信桥：在同一个微信账号上运行 Hermes Agent 和 OpenClaw。

---

## License 执照

MIT — see [LICENSE](https://github.com/NousResearch/hermes-agent/blob/main/LICENSE).  
MIT — 请参阅 [LICENSE](https://github.com/NousResearch/hermes-agent/blob/main/LICENSE) 。

Built by [Nous Research](https://nousresearch.com/).  
由 [Nous Research](https://nousresearch.com/) 开发。