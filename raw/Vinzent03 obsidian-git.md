---
title: "Vinzent03/obsidian-git: Integrate Git version control with automatic commit-and-sync and other advanced features in Obsidian.md"
source: "https://github.com/Vinzent03/obsidian-git"
author:
published:
created: 2026-04-09
description: "Integrate Git version control with automatic commit-and-sync and other advanced features in Obsidian.md - Vinzent03/obsidian-git"
tags:
  - "clippings"
---
## Obsidian Git Plugin Obsidian Git 插件

A powerful community plugin for [Obsidian.md](https://github.com/Vinzent03/obsidian-git/blob/master/Obsidian.md) that brings Git integration right into your vault. Automatically commit, pull, push, and see your changes — all within Obsidian.  
一款功能强大的 [Obsidian.md](https://github.com/Vinzent03/obsidian-git/blob/master/Obsidian.md) 社区插件，可将 Git 集成到您的代码库中。自动提交、拉取、推送并查看更改——所有操作均可在 Obsidian 内完成。

## 📚 Documentation 📚 文档

All setup instructions (including mobile), common issues, tips, and advanced configuration can be found in the 📖 [full documentation](https://publish.obsidian.md/git-doc).  
所有设置说明（包括移动设备）、常见问题、技巧和高级配置都可以在 📖 [完整文档](https://publish.obsidian.md/git-doc) 中找到。

> Mobile users: The plugin is **highly unstable ⚠️!** Please check the dedicated [Mobile](#-mobile-support-%EF%B8%8F--experimental) section below.  
> 移动端用户请注意：该插件 **极不稳定！** 请查看下方专门的 [移动端](#-mobile-support-%EF%B8%8F--experimental) 部分。

## Key Features 主要特点

- 🔁 **Automatic commit-and-sync** (commit, pull, and push) on a schedule.  
	🔁 按计划 **自动提交和同步** （提交、拉取和推送）。
- 📥 **Auto-pull on Obsidian startup**  
	📥 **Obsidian 启动时自动拉取**
- 📂 **Submodule support** for managing multiple repositories (desktop only and opt-in)  
	📂 **支持子模块** 管理多个存储库（仅限桌面端，需选择启用）
- 🔧 **Source Control View** to stage/unstage, commit and diff files - Open it with the `Open source control view` command.  
	🔧 **源代码控制视图，** 用于暂存/取消暂存、提交和比较文件 - 使用 `Open source control view` 命令打开它。
- 📜 **History View** for browsing commit logs and changed files - Open it with the `Open history view` command.  
	📜 **历史记录视图** ，用于浏览提交日志和已更改的文件 - 使用 `Open history view` 视图”命令打开它。
- 🔍 **Diff View** for viewing changes in a file - Open it with the `Open diff view` command.  
	🔍 **差异视图** ，用于查看文件中的更改 - 使用 `Open diff view` 命令打开它。
- 📝 **Signs in the editor** to indicate added, modified, and deleted lines/hunks (desktop only).  
	📝 **编辑器中的符号，** 用于指示添加、修改和删除的行/块（仅限桌面版）。
- GitHub integration to open files and history in your browser  
	GitHub 集成，可在浏览器中打开文件和历史记录

> For detailed file history, consider pairing this plugin with the Version History Diff plugin.  
> 如需查看详细的文件历史记录，请考虑将此插件与版本历史差异插件结合使用。

## UI Previews 用户界面预览

### 🔧 Source Control View 🔧 源代码控制视图

Manage your file changes directly inside Obsidian like stage/unstage individual files and commit them.  
直接在 Obsidian 中管理文件更改，例如暂存/取消暂存单个文件并提交它们。

[![[raw/assets/54263e1e6221a8700d5b5a77f690bf82_MD5.png]]](https://raw.githubusercontent.com/Vinzent03/obsidian-git/master/images/source-view.png)

### 📜 History View 📜 历史记录

Show the commit history of your repository. The commit message, author, date, and changed files can be shown. Author and date are disabled by default as shown in the screenshot, but can be enabled in the settings.  
显示仓库的提交历史记录。可以显示提交消息、作者、日期和已更改的文件。作者和日期默认处于禁用状态（如屏幕截图所示），但可以在设置中启用。

[![[raw/assets/9c80f10276fb4bd17dd9b975945f19fb_MD5.png]]](https://raw.githubusercontent.com/Vinzent03/obsidian-git/master/images/history-view.png)

### 🔍 Diff View 🔍 不同视图

Compare versions with a clear and concise diff viewer. Open it from the source control view or via the `Open diff view` command.  
使用清晰简洁的差异查看器比较版本。可以从源代码控制视图打开，也可以通过 `Open diff view` 器”命令打开。

[![[raw/assets/7c43e6d6084d131f6b5abc84dbd587a1_MD5.png]]](https://raw.githubusercontent.com/Vinzent03/obsidian-git/master/images/diff-view.png)

### 📝 Signs in the Editor

View line-by-line changes directly in the editor with added, modified, and deleted line/hunk indicators. You can stage and reset changes right from the signs. There also commands to navigate between hunks and stage/reset hunks under the cursor. Needs to be enabled in the plugin settings.

[![[raw/assets/abf0484286aace0820f75e9ce80d0795_MD5.png]]](https://raw.githubusercontent.com/Vinzent03/obsidian-git/master/images/signs.png)

## Available Commands

> Not exhaustive - these are just some of the most common commands. For a full list, see the Command Palette in Obsidian.

- 🔄 Changes
	- `List changed files`: Lists all changes in a modal
		- `Open diff view`: Open diff view for the current file
		- `Stage current file`
		- `Unstage current file`
		- `Discard all changes`: Discard all changes in the repository
- ✅ Commit
	- `Commit`: If files are staged only commits those, otherwise commits only files that have been staged
		- `Commit with specific message`: Same as above, but with a custom message
		- `Commit all changes`: Commits all changes without pushing
		- `Commit all changes with specific message`: Same as above, but with a custom message
- 🔀 Commit-and-sync
	- `Commit-and-sync`: With default settings, this will commit all changes, pull, and push
		- `Commit-and-sync with specific message`: Same as above, but with a custom message
		- `Commit-and-sync and close`: Same as `Commit-and-sync`, but if running on desktop, will close the Obsidian window. Will not exit Obsidian app on mobile.
- 🌐 Remote
	- `Push`, `Pull`
		- `Edit remotes`: Add new remotes or edit existing remotes
		- `Remove remote`
		- `Clone an existing remote repo`: Opens dialog that will prompt for URL and authentication to clone a remote repo
		- `Open file on GitHub`: Open the file view of the current file on GitHub in a browser window. Note: only works on desktop
		- `Open file history on GitHub`: Open the file history of the current file on GitHub in a browser window. Note: only works on desktop
- 🏠 Manage local repository
	- `Initialize a new repo`
		- `Create new branch`
		- `Delete branch`
		- `CAUTION: Delete repository`
- 🧪 Miscellaneous
	- `Open source control view`: Opens side pane displaying [Source control view](#sidebar-view)
		- `Open history view`: Opens side pane displaying [History view](#history-view)
		- `Edit .gitignore`
		- `Add file to .gitignore`: Add current file to `.gitignore`

## 💻 Desktop Notes

### 🔐 Authentication

Some Git services may require further setup for HTTPS/SSH authentication. Refer to the [Authentication Guide](https://publish.obsidian.md/git-doc/Authentication)

### Obsidian on Linux

- ⚠️ Snap is not supported due to its sandboxing restrictions.
- ⚠️ Flatpak is not recommended, because it doesn't have access to all system files. They are actively fixing many issues, but there are still issues. Especially with more advanced setups.
- ✅ Please use AppImage or a full access installation of your system's package manager instead ([Linux installation guide](https://publish.obsidian.md/git-doc/Installation#Linux))

## 📱 Mobile Support (⚠️ Experimental)

The Git implementation on mobile is **very unstable**! I would not recommend using this plugin on mobile, but try other syncing services.

One such alternative is [GitSync](https://github.com/ViscousPot/GitSync), which is available on both Android and iOS. It is not associated with this plugin, but it may be a better option for mobile users. A tutorial for setting it up can be found [here](https://viscouspotenti.al/posts/gitsync-all-devices-tutorial).

> 🧪 The Git plugin works on mobile thanks to [isomorphic-git](https://isomorphic-git.org/), a JavaScript-based re-implementation of Git - but it comes with serious limitations and issues. It is not possible for an Obsidian plugin to use a native Git installation on Android or iOS.

### ❌ Mobile Feature Limitations

- No **SSH authentication** ([isomorphic-git issue](https://github.com/isomorphic-git/isomorphic-git/issues/231))
- Limited repo size, because of memory restrictions
- No rebase merge strategy
- No submodules support

### ⚠️ Performance Caveats

> [!caution] Caution
> Depending on your device and available free RAM, Obsidian may
> 
> - crash on clone/pull
> - create buffer overflow errors
> - run indefinitely.
> 
> It's caused by the underlying git implementation on mobile, which is not efficient. I don't know how to fix this. If that's the case for you, I have to admit this plugin won't work for you. So commenting on any issue or creating a new one won't help. I am sorry.

### Tips for Mobile Use:

If you have a large repo/vault I recommend to stage individual files and only commit staged files.

## 🙋 Contact & Credits

- The Line Authoring feature was developed by [GollyTicker](https://github.com/GollyTicker), so any questions may be best answered by her.
- This plugin was initial developed by [denolehov](https://github.com/denolehov). Since March 2021, it's me [Vinzent03](https://github.com/Vinzent03) who is developing this plugin. That's why the GitHub repository got moved to my account in July 2024.
- If you have any kind of feedback or questions, feel free to reach out via GitHub issues.