---
title: oh-my-openagent - 摘要
created: 2026-04-09
updated: 2026-04-09
sources:
  - "[[raw/code-yeongyu oh-my-openagent.md]]"
tags:
  - AI编程
  - 多智能体
  - OpenCode
  - 框架
type: source-summary
---

# oh-my-openagent - 摘要

oh-my-openagent（OmO）是一个为 OpenCode 打造的多模型协作 AI 编程框架，支持 Claude、GPT、Kimi、Gemini 等模型并行工作。

## 核心特性

### ultrawork（一键触发）

- 输入 `ultrawork` 或 `ulw`，自动调度多智能体协作
- 任务完成前绝不停止（Ralph Loop 自引用闭环）
- Todo 强制执行：系统强制 Agent 完成任务，防止摸鱼

### 自律军团（Discipline Agents）

- **Sisyphus**（主指挥官）：制定计划、分配任务、激进并行策略（支持 claude-opus-4-6 / kimi-k2.5 / glm-5）
- **Hephaestus**（自主深度工作者）：独立执行任务，无需保姆式指导（gpt-5.4）
- **Prometheus**（战略规划师）：访谈模式，动代码前先做详尽规划（claude-opus-4-6 / kimi-k2.5 / glm-5）

### 智能体调度机制

智能体选择**类别（Category）**而非具体模型，系统自动映射：

| 类别 | 作用领域 |
|------|----------|
| `visual-engineering` | 前端、UI/UX、设计 |
| `deep` | 深度自主调研与执行 |
| `quick` | 单文件修改、修错字 |
| `ultrabrain` | 复杂硬核逻辑、架构决策 |

### 核心技术创新

1. **Hashline**（基于哈希的编辑工具）：解决 [[Harness 问题]]
   - 每行代码末尾绑定内容哈希值（如 `11#VK|`）
   - 修改时必须引用目标行哈希，验证失败则驳回
   - Grok Code Fast 1 上修改成功率从 6.7% 飙升至 68.3%

2. **IntentGate**（意图门）：行动前先分析真实意图，避免字面误导

3. **LSP + AST-Grep + Tmux + MCP 深度集成**：
   - LSP：工作区级重命名、构建前诊断、IDE 级精度
   - AST-Grep：25 种语言的语法树模式匹配和重写
   - Tmux：完整交互式终端，支持 REPL、调试器、TUI 工具
   - MCP：内置 Exa（网络搜索）、Context7（官方文档）、Grep.app（GitHub 搜索）

4. **技能系统（Skills）**：与 [[Agent Skills]] 理念相通
   - 面向特定领域的调优指令
   - 按需加载的独立 MCP 服务器（任务完成即销毁）
   - 对 Agent 能力边界的强制约束
   - 默认内置：playwright（浏览器自动化）、git-master（原子提交）、frontend-ui-ux

5. **深度上下文初始化（/init-deep）**：
   - 自动生成树状 `AGENTS.md` 文件系统
   - Agent 自动加载对应层级的 Context

### Prometheus 规划师

- `/start-work` 触发访谈模式
- 像真实主管采访用户，深挖需求、指出模糊地带
- 动代码前产出严密论证的计划

## 兼容性

- 完全兼容 Claude Code 的 Hooks、命令、技能、MCP、插件
- 所有配置直接生效，包括插件系统

## 推荐订阅

以下订阅之一即可顺畅工作（与项目无关联）：
- ChatGPT 订阅（$20）
- Kimi Code 订阅（$0.99）
- GLM Coding 套餐（$10）

## 用户评价摘录

- "因为它，我取消了 Cursor 的订阅" — Arthur Guiot
- "用 Oh My Opencode 一天解决了 8000 个 eslint 警告" — Jacob Ferrari
- "45k 行 Tauri 应用一晚上转换成 SaaS Web 应用" — James Hargis

## 作者理念

作者花费 $24,000 测试所有代码 Agent，认为 OpenCode 赢了。OmO 是踩坑总结的结晶（Distillation）：
- 把 OpenCode 喻为 Debian/Arch，OmO 是开箱即用的 Ubuntu/Omarchy
- 持续跟踪竞品特性，把最强的全偷过来更新
- 99% 代码由 OpenCode 生成，但 README 作者亲自审核重写

## 背景设定

详见 [overview 文档](https://github.com/code-yeongyu/oh-my-openagent/blob/dev/docs/guide/overview.md)

## 相关链接

- [[oh-my-openagent]]
- [[OpenCode]]
- [[Harness 问题]]
- [[多智能体协作]]
- [[Agent Skills]]
- [[Claude Code]]
- [[AmpCode]]