# <picture><source media="(prefers-color-scheme: dark)" srcset="docs/references/badges/openchamber-logo-dark.svg"><img src="docs/references/badges/openchamber-logo-light.svg" width="32" height="32" align="absmiddle" /></picture> OpenChamber
[![GitHub stars](https://img.shields.io/github/stars/openchamber/openchamber?style=flat&labelColor=100F0F&color=66800B)](https://github.com/openchamber/openchamber/stargazers)
[![GitHub release](https://img.shields.io/github/v/release/openchamber/openchamber?style=flat&labelColor=100F0F&color=205EA6)](https://github.com/openchamber/openchamber/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-join.svg?style=flat&labelColor=100F0F&color=8B7EC8&logo=discord&logoColor=FFFCF0)](https://discord.gg/ZYRSdnwwKA)
[![Support the project](https://img.shields.io/badge/Support-Project-black?style=flat&labelColor=100F0F&color=EC8B49&logo=patreon&logoColor=FFFCF0)](https://www.patreon.com/openchamber)
<a href="https://www.blacksmith.sh/"><picture><source media="(prefers-color-scheme: dark)" srcset="docs/references/badges/blacksmith-dark.svg"><img src="docs/references/badges/blacksmith-light.svg" height="28" alt="CI powered by Blacksmith" /></picture></a>
## 运行智能体任务，全程保持掌控，随时随地交付
**OpenChamber 是一套开源工作空间，可在桌面端、网页、VS Code 和移动端运行与审阅 AI 编码任务。**

启动智能体任务，查看代码变更，完成评审直至发布。切换设备或暂时离开时，你的项目与任务会话状态会持续保留。

![OpenChamber Chat](docs/references/chat_example.png)
<details>
<summary>更多截图</summary>
![VS Code 扩展](packages/vscode/extension.jpg)
<p>
<img src="docs/references/pwa_chat_example.png" width="45%" alt="OpenChamber PWA 对话界面">
<img src="docs/references/pwa_diff_example.png" width="45%" alt="OpenChamber PWA 差异评审界面">
</p>
</details>

## OpenChamber 可以实现这些能力
### 可自主持续推进的任务目标
通过**会话目标（Session Goals）**为一次任务设定终点。OpenChamber 在每一轮执行后校验结果，驱动智能体持续工作，直到达成目标、遇到阻塞或到达你设定的执行上限。即使关闭应用，任务也可继续后台运行。

### 多任务运行对比与结果合并
使用**多实例运行（Multi-run）**，将同一个任务同时交给最多五个大模型，每个模型独立会话、可独立配置工作目录。查看各模型实际产出的代码成果，挑选最优结果；或使用**融合（Fusion）**功能，提取各版本亮点合并生成全新会话。

### 变更分步引导讲解
**变更导览（Changes Walkthrough）**可把庞大的代码差异转换成 AI 引导式的改动讲解。它会把相关改动分组整理为步骤，按逻辑顺序展示，解释各代码片段之间的关联。

### 运行中应用实时检视
通过**预览（Preview）**，将你的应用和对话界面并排打开。点击页面元素，即可把截图、样式、元素坐标、浏览器报错一并发送给智能体，不再需要费力描述“这里这个控件”。桌面客户端内置浏览器，对任意网页都支持该能力。

### GitHub 全链路上下文：从 Issue 到 PR
可基于 GitHub Issue 或 Pull Request 直接创建会话，自动挂载完整上下文。把 CI 失败信息、评审意见回传给智能体；并且能直接在 OpenChamber 内更新或合并 PR。

### 跨设备接续工作
桌面端、网页/PWA、VS Code、iOS、Android 可访问同一套项目与任务会话。随时查看进度、答疑、评审代码变更，重新接入正在运行的终端会话。

### 私有远程访问
设备之间通过一次性二维码配对，依托**私有中继（Private Relay）**建立连接，**无需端口映射，也不用暴露公网服务**。连接采用端到端加密，可随时撤销。同时也支持直连、局域网/VPN、Cloudflare/Ngrok 隧道、SSH 连接。

### 跨项目任务总览
查看所有会话状态：运行中、等待、已完成、失败；同时展示审批状态、定时任务、模型服务商配额、Token 消耗与费用。可将会话归入文件夹，配套保存笔记、待办清单和项目可复用操作。

### 定时执行任务
单次、每日、每周或通过 cron 表达式定时执行指令。定时任务同样支持会话目标机制，不会单次回答后就停止，会持续向目标推进。

## 在你常用的环境中使用
| 运行端 | 能力说明 |
| --- | --- |
| **桌面端** | macOS、Windows、Linux 完整工作空间；支持多窗口、迷你对话、远程主机、SSH、原生系统通知 |
| **网页 / PWA** | 浏览器内打开工作空间，可安装为独立应用；后台通知同步状态 |
| **VS Code** | 在编辑器侧边常驻会话，选中代码直接发给智能体，结果在编辑器打开，对比多实例并行运行的差异 |
| **iOS / Android** | 离开电脑也能管控、审阅任务；接收完成提醒；支持触屏终端操作 |
| **命令行 / 服务端** | 在工作站或服务器上运行 OpenChamber，配置定时任务、管理远程访问，登出后服务持续可用 |

## 快速上手
### macOS / Windows / Linux 桌面端
从 [GitHub Releases](https://github.com/openchamber/openchamber/releases/latest) 下载最新安装包。桌面端内置配套 OpenCode CLI，无需单独安装 OpenCode。

Linux 提供 x86_64 和 ARM64 架构 AppImage。下载后赋予可执行权限，放在可写目录才能使用应用内更新：
```bash
chmod +x OpenChamber-*.AppImage
./OpenChamber-*.AppImage
