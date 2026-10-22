## Jacksonlin Infra

Open-source infrastructure for building with AI: small, focused tools for coding agents, model pipelines and everyday developer workflows.

面向 AI 的开源基础设施：为编码 Agent、模型调用链路和日常研发流程打造的小而专的工具。

### Projects

| Project | What it does |
|---|---|
| [Twinline](https://github.com/jacksonlin-infra/twinline) | Bilingual mode for Claude Code: write in your language, let Claude work in English, read both side by side. |
| [TunBridge](https://github.com/jacksonlin-infra/tunbridge) | System-wide TUN for the HTTP(S)/SOCKS5 proxy you already have: Git, SSH, package managers, AI CLIs and containers all use it, with no per-app settings. Windows, Linux and macOS. |
| [omarchy-doubao](https://github.com/jacksonlin-infra/omarchy-doubao) | Voice input on Omarchy powered by Doubao (Volcengine) speech recognition: hold F9, speak, release, and punctuated text lands at the cursor. |

### Twinline

[Twinline](https://github.com/jacksonlin-infra/twinline) is a Claude Code plugin for people who think in one language and want Claude to work in English. What you type is translated into English before it is sent, so the model and the transcript only ever see English. Your original stays on screen with the English underneath, and each reply gets a translation into your language once it has settled. It works in the terminal and in the Desktop app's Code tab, handles any language (with tuned rules for Traditional Chinese and Japanese), and translates through your Claude Code sign-in by default, with optional OpenAI, DeepL or Ollama backends. MIT.

Requires Claude Code 2.1.292 or later — [Install](https://github.com/jacksonlin-infra/twinline#install) · [Guide](https://github.com/jacksonlin-infra/twinline/blob/main/docs/GUIDE.md) · [简体中文](https://github.com/jacksonlin-infra/twinline/blob/main/README.zh-CN.md)

Twinline 是 Claude Code 的“双语模式”插件：用你熟悉的语言输入，发送前自动译成英文，模型和对话记录里只有英文；界面上保留你的原文并在下方显示英文，每条回复稳定后再附上用你的语言写的译文。支持终端和桌面版的 Code 标签页，可使用任意语言（对繁体中文、日文有专门的文字与措辞规则），默认通过你的 Claude Code 登录完成翻译，也可选用 OpenAI、DeepL 或 Ollama。MIT 开源。需要 Claude Code 2.1.292 或更高版本。

### TunBridge

[TunBridge](https://github.com/jacksonlin-infra/tunbridge) puts a system-wide TUN in front of the HTTP(S) or SOCKS5 proxy you already run, so every application on the machine uses it without per-app settings. If the proxy, the engine or the UI fails, traffic stays blocked instead of silently going direct. The privileged part is a small system service that the desktop app can reach only through a fixed set of typed commands. No telemetry. GPL-3.0-or-later.

Windows 11 · Ubuntu 24.04/26.04 · Omarchy · macOS 12+ — [Download](https://github.com/jacksonlin-infra/tunbridge/releases/latest) · [Documentation](https://github.com/jacksonlin-infra/tunbridge#readme) · [简体中文](https://github.com/jacksonlin-infra/tunbridge/blob/main/README.zh-CN.md)

TunBridge 在你已有的 HTTP(S)/SOCKS5 代理前加一层系统级 TUN，让 Git、SSH、包管理器、AI CLI、容器和各类原生应用都走这个代理，无需逐个设置。代理、引擎或界面出故障时，流量保持阻断，不会悄悄直连；特权部分是一个很小的系统服务，桌面端只能通过固定的几种强类型命令与它通信。无遥测，GPL-3.0-or-later 开源。支持 Windows 11、Ubuntu、Omarchy 和 macOS 12+。

### omarchy-doubao

[omarchy-doubao](https://github.com/jacksonlin-infra/omarchy-doubao) brings Doubao speech recognition to Omarchy, where the Doubao IME has no Linux build. It plugs Volcengine's Doubao streaming ASR into Voxtype, Omarchy's built-in dictation tool, through a small local bridge, so nothing runs on your GPU or CPU. Hold F9 in any window (browser, terminal, Claude Code or Codex prompt), speak, and release: text with punctuation, normalized numbers and filler words removed is typed at the cursor. One script installs and verifies everything, and the repository includes an AGENTS.md so you can hand the link to a coding agent and let it set things up. Supports both new-console API keys and legacy App ID + Access Token. MIT.

Omarchy (Arch + Hyprland) · Volcengine account — [Install](https://github.com/jacksonlin-infra/omarchy-doubao#手动安装) · [Agent guide](https://github.com/jacksonlin-infra/omarchy-doubao/blob/main/AGENTS.md)

omarchy-doubao 让 Omarchy 用上豆包语音识别（豆包输入法没有 Linux 版）。它通过一个本地小服务，把火山引擎的豆包流式语音识别接到 Omarchy 自带的听写工具 Voxtype 上，本机不跑任何模型。在任意窗口（浏览器、终端、Claude Code / Codex 输入框）按住 F9 说话，松开后带标点、数字规整、去掉口水词的文字直接打到光标处。一条脚本完成安装和自检；仓库附带 AGENTS.md，把链接发给编码 Agent 就能让它代为部署。同时支持新版控制台 API Key 和旧版 App ID + Access Token。MIT 开源。

More tools are on the way.

### How we build

- **Private by default.** No telemetry; your data goes only where you configure it.
- **Few dependencies.** Zero runtime dependencies wherever possible.
- **Fail open.** A tool should never break the workflow it supports.
- **Bilingual docs.** English and 简体中文.

### Get involved

Issues and pull requests are welcome in each repository. Report security issues privately through the repository's Security tab.
