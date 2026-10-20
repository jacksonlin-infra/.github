## Jacksonlin Infra

Open-source infrastructure for building with AI: small, focused tools for coding agents, model pipelines and everyday developer workflows.

面向 AI 的开源基础设施：为编码 Agent、模型调用链路和日常研发流程打造的小而专的工具。

### Projects

| Project | What it does |
|---|---|
| [Twinline](https://github.com/jacksonlin-infra/twinline) | Bilingual mode for Claude Code: write in your language, let Claude work in English, read both side by side. |
| [TunBridge](https://github.com/jacksonlin-infra/tunbridge) | System-wide TUN for the HTTP(S)/SOCKS5 proxy you already have: Git, SSH, package managers, AI CLIs and containers all use it, with no per-app settings. Windows, Linux and macOS. |

### TunBridge

[TunBridge](https://github.com/jacksonlin-infra/tunbridge) puts a system-wide TUN in front of the HTTP(S) or SOCKS5 proxy you already run, so every application on the machine uses it without per-app settings. If the proxy, the engine or the UI fails, traffic stays blocked instead of silently going direct. The privileged part is a small system service that the desktop app can reach only through a fixed set of typed commands. No telemetry. GPL-3.0-or-later.

Windows 11 · Ubuntu 24.04/26.04 · Omarchy · macOS 12+ — [Download](https://github.com/jacksonlin-infra/tunbridge/releases/latest) · [Documentation](https://github.com/jacksonlin-infra/tunbridge#readme) · [简体中文](https://github.com/jacksonlin-infra/tunbridge/blob/main/README.zh-CN.md)

TunBridge 在你已有的 HTTP(S)/SOCKS5 代理前加一层系统级 TUN，让 Git、SSH、包管理器、AI CLI、容器和各类原生应用都走这个代理，无需逐个设置。代理、引擎或界面出故障时，流量保持阻断，不会悄悄直连；特权部分是一个很小的系统服务，桌面端只能通过固定的几种强类型命令与它通信。无遥测，GPL-3.0-or-later 开源。支持 Windows 11、Ubuntu、Omarchy 和 macOS 12+。

More tools are on the way.

### How we build

- **Private by default.** No telemetry; your data goes only where you configure it.
- **Few dependencies.** Zero runtime dependencies wherever possible.
- **Fail open.** A tool should never break the workflow it supports.
- **Bilingual docs.** English and 简体中文.

### Get involved

Issues and pull requests are welcome in each repository. Report security issues privately through the repository's Security tab.
