# <picture><source media="(prefers-color-scheme: dark)" srcset="docs/references/badges/openchamber-logo-dark.svg"><img src="docs/references/badges/openchamber-logo-light.svg" width="32" height="32" align="absmiddle" /></picture> OpenChamber

[![GitHub stars](https://img.shields.io/github/stars/openchamber/openchamber?style=flat&labelColor=100F0F&color=66800B)](https://github.com/openchamber/openchamber/stargazers)
[![GitHub release](https://img.shields.io/github/v/release/openchamber/openchamber?style=flat&labelColor=100F0F&color=205EA6)](https://github.com/openchamber/openchamber/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-join.svg?style=flat&labelColor=100F0F&color=8B7EC8&logo=discord&logoColor=FFFCF0)](https://discord.gg/ZYRSdnwwKA)
[![Support the project](https://img.shields.io/badge/Support-Project-black?style=flat&labelColor=100F0F&color=EC8B49&logo=patreon&logoColor=FFFCF0)](https://www.patreon.com/openchamber)

<a href="https://www.blacksmith.sh/"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/references/badges/blacksmith-dark.svg"><img src="docs/references/badges/blacksmith-light.svg" height="28" alt="CI powered by Blacksmith" /></picture></a>

## 运行智能体任务。保持全面掌控。随时随地交付。

**OpenChamber 是一个开源工作区，用于在桌面端、Web 端、VS Code 以及移动端运行和审查 AI 编程任务。**

启动智能体任务，查看变更内容，并推进至审查与发布阶段。无论你切换设备还是暂时离开，项目与会话均可随时继续访问。

![OpenChamber Chat](docs/references/chat_example.png)

<details>
<summary>更多截图</summary>

![VS Code Extension](packages/vscode/extension.jpg)

<p>
<img src="docs/references/pwa_chat_example.png" width="45%" alt="OpenChamber PWA chat">
<img src="docs/references/pwa_diff_example.png" width="45%" alt="OpenChamber PWA diff review">
</p>

</details>

## OpenChamber 能做什么

### 自主推进的会话目标

通过**会话目标（Session Goals）**为会话设定终点。OpenChamber 会在每一轮交互后检查结果，让智能体持续工作，直至达成目标、遇到阻碍或达到你设定的上限。即使关闭应用，任务依然可以继续运行。

### 对比与合并多次运行

使用**多重运行（Multi-run）**将同一任务分配给最多 5 个模型，每个模型都在独立的会话中运行，并可选择独立的 worktree。直观对比每个模型的实际构建成果，挑选最佳结果，或使用**融合（Fusion）**功能将各方案的最优部分合并为新会话。

### 引导式变更导览

**变更导览（Changes Walkthrough）**可将庞大的代码差异（diff）转化为由 AI 引导的渐进式导览。它将相关的修改归类为不同步骤，按合乎逻辑的顺序排列，并解释各模块如何协同工作。

### 检查运行中的应用

通过**预览（Preview）**在对话旁打开你的应用。点击任意元素即可向智能体发送其屏幕截图、样式、坐标位置以及浏览器报错信息。无需再费力解释“这里这个东西”。桌面端应用还可以在其内置浏览器中对任意网页执行相同操作。

### 贯穿 Issue 到 Pull Request 的 GitHub 上下文

直接从 GitHub Issue 或 Pull Request 发起会话并附带相关上下文。将失败的检查项或评审评论反馈给智能体，然后直接在 OpenChamber 中更新或合并 Pull Request。

### 跨设备无缝衔接

在桌面端、Web/PWA、VS Code、iOS 或 Android 上打开相同的项目和会话。随时查看进度、回答智能体提问、审查代码变更，并重新连接至正在运行的终端。

### 私密远程访问

通过一次性二维码与设备配对，并通过**私有中继（Private Relay）**建立连接，无需开放端口或暴露公网服务器。连接全程端到端加密，且随时可撤销。同时支持直连、局域网（LAN）/VPN 访问、Cloudflare/Ngrok 隧道以及 SSH。

### 跨项目追踪任务

清晰查看哪些会话正在运行、等待、已完成或失败，并跟踪审批流、定时任务、模型提供商配额、Token 用量和费用。将会话整理至不同文件夹，随时取用笔记、待办事项和可复用的项目操作。

### 定时周期性任务

按单次、每天、每周或基于 Cron 定时执行提示词。定时任务支持结合会话目标使用，使其持续朝着既定结果推进，而不是在单次响应后就停止。

## 在你工作的地方尽情使用

| 使用形态 | 作用定位 |
| --- | --- |
| **桌面端** | 适用于 macOS、Windows 和 Linux 的完整工作区，支持多窗口、迷你聊天（Mini Chat）、远程主机、SSH 和系统原生通知 |
| **Web / PWA** | 在浏览器中打开工作区，可作为应用安装，并通过后台通知保持最新状态同步 |
| **VS Code** | 在代码旁保留会话，向智能体发送代码选区，在编辑器中打开结果，并对比并行运行的表现 |
| **iOS / Android** | 离开工位时审查和把控任务进度，接收完成提醒，并通过触控操作终端 |
| **CLI / 服务端** | 在工作站或服务器上运行 OpenChamber，调度任务，管理远程访问，并在登录后保持服务可用 |

## 快速上手

### 适用于 macOS、Windows 和 Linux 的桌面端

从 [GitHub Releases](https://github.com/openchamber/openchamber/releases/latest) 下载最新版本。桌面端内置了相匹配的 OpenCode CLI，因此无需单独安装 OpenCode。

Linux 版本提供 x86_64 和 ARM64 架构的 AppImage。请赋予下载的 AppImage 可执行权限，并存放在可写路径下以便支持应用内更新：

```bash
chmod +x OpenChamber-*.AppImage
./OpenChamber-*.AppImage


Linux AppImage 依赖 FUSE（`libfuse.so.2`）。如无 FUSE 环境，请使用 `APPIMAGE_EXTRACT_AND_RUN=1` 运行。

### VS Code

从 [Visual Studio Marketplace 安装 OpenChamber](https://marketplace.visualstudio.com/items?itemName=fedaykindev.openchamber)，或在扩展商店中搜索“OpenChamber”。

### Web 和 PWA 适用的 CLI

需要 Node.js 24.14+。CLI/Web 和 VS Code 依赖你本地安装的 [OpenCode CLI](https://opencode.ai)。

```bash
curl -fsSL https://raw.githubusercontent.com/openchamber/openchamber/main/scripts/install.sh | bash
openchamber --ui-password be-creative-here
```

常用命令操作：

```bash
openchamber status
openchamber connect-url --qr
openchamber tunnel start --provider cloudflare --mode quick --qr
openchamber startup enable
openchamber logs
openchamber stop
openchamber update
```

OpenChamber 默认监听 localhost。仅在受信任的网络中才建议使用 `--lan`，并务必通过 `--ui-password` 保护浏览器访问权限。

## 使用指南

深入探索 OpenChamber 指南文档：

- [快速入门](packages/docs/content/docs/quickstart.mdx)
- [安装指南](packages/docs/content/docs/install.mdx)
- [连接设备](packages/docs/content/docs/connect-devices.mdx)
- [私有中继（Private Relay）](packages/docs/content/docs/private-relay.mdx)
- [多重运行（Multi-run）](packages/docs/content/docs/multi-run.mdx)
- [会话目标（Session Goals）](packages/docs/content/docs/session-goals.mdx)
- [变更导览（Changes Walkthrough）](packages/docs/content/docs/walkthrough.mdx)
- [预览与开发服务器](packages/docs/content/docs/preview.mdx)
- [GitHub 工作流](packages/docs/content/docs/github.mdx)
- [移动端](packages/docs/content/docs/mobile.mdx)
- [安全性](packages/docs/content/docs/security.mdx)
- [疑难解答](packages/docs/content/docs/troubleshooting.mdx)

有关自建部署（Self-hosting）细节，请参阅[反向代理指南](docs/REVERSE_PROXY.md)。自定义主题编写请参阅[自定义主题指南](docs/CUSTOM_THEMES.md)。

## 为什么选择 OpenCode？

OpenChamber 使用 [OpenCode](https://opencode.ai) 来运行编程智能体。我们选择它是因为其开源特性、稳定的 API 以及出色的可扩展性。

OpenChamber 则负责其余的工作流体验：决定尝试什么方案、确保智能体方向正确、审查最终结果、从其他设备远程接入并交付代码变更。

OpenChamber 是一个独立项目，不隶属于 OpenCode 官方团队。

## 参与贡献

欢迎通过 PR 提交 Bug 修复和小型改进。新特性和行为变更请先在 [Ideas 讨论区](https://github.com/openchamber/openchamber/discussions/categories/ideas) 发起，以便在编写代码前在产品层面达成一致。提交 PR 前请阅读 [CONTRIBUTING.md](./CONTRIBUTING.md)，其中包含环境配置、评审准则以及如何处理大型未规划 PR 的说明。文档编写指导见 [`packages/docs`](packages/docs/README.md)。

Bug 报告请前往 [Issues](https://github.com/openchamber/openchamber/issues/new/choose)。疑问请前往 [Q&A 讨论区](https://github.com/openchamber/openchamber/discussions/categories/q-a)。

## 鸣谢

特别鸣谢：

- [OpenCode](https://opencode.ai) 提供了 OpenChamber 所依托的 API 和开源架构
- [Pierre](https://pierrejs-docs.vercel.app/) 提供了差异对比查看器（diff viewer）与语法高亮
- [T3 Code](https://github.com/pingdotgg/t3code) 团队为 [libghostty-vt](https://github.com/ghostty-org/ghostty) 构建的浏览器适配层（我们的终端正基于此构建）
- [Yulia Ivashko](https://github.com/yulia-ivashko) 制作了每次成功推送时播放的烟花庆祝动画
- 感谢每一位贡献代码、反馈 Bug 或分享想法的朋友

## 开源协议

MIT
```
