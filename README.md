<div align="center">

<img src="assets/icon.png" alt="Swarm Code Desktop" width="130" height="130">

# Swarm Code Desktop

### Your coding agents. Native on Windows & Linux.

<p>
  <a href="https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/latest"><img src="https://img.shields.io/badge/Release-v1.0.0-blue?logo=github" alt="Latest Release"></a>
  <a href="https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x64.exe"><img src="https://img.shields.io/badge/Windows-10%20%7C%2011%20(x64)-0078D6?logo=windows&logoColor=white" alt="Windows"></a>
  <a href="https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x86_64.AppImage"><img src="https://img.shields.io/badge/Linux-AppImage%20%7C%20.deb-FCC624?logo=linux&logoColor=black" alt="Linux"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-success" alt="MIT License"></a>
</p>

<p align="center">
  <i>One unified desktop workspace for Claude, Codex, Antigravity, Copilot, Cursor, OpenCode, Grok, and DeepSeek.<br>Run on your own subscriptions. Zero markup. Zero cloud sync. Zero telemetry.</i>
</p>

</div>

---

## ⚡ Quick Downloads

Official desktop binary releases for Windows and Linux (64-bit):

| Platform | Format | Architecture | Download Link | File Size |
| :--- | :--- | :--- | :--- | :--- |
| **Windows** | Installer (`.exe`) | 64-bit (x64) | [**Download for Windows (Installer)**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x64.exe) | ~129 MB |
| **Linux (Universal)** | Standalone AppImage | 64-bit (x86_64) | [**Download Linux AppImage**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x86_64.AppImage) | ~150 MB |
| **Linux (Debian / Ubuntu)** | Native Package (`.deb`) | 64-bit (amd64) | [**Download Debian / Ubuntu .deb**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-amd64.deb) | ~118 MB |

> **Verification Checksums**: [Windows SHA-256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/SHA256SUMS-windows.txt) · [Linux SHA-256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/SHA256SUMS-linux.txt)

---

## 🚀 Installation Guide

### Windows (10 & 11)
1. Download [**`Swarm-Code-1.0.0-x64.exe`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x64.exe).
2. Double-click the installer and follow the setup wizard.
3. Swarm Code will install to your user profile and launch automatically.
4. *Optional*: Ensure Git for Windows is installed and accessible in your `PATH` for full Git worktree and checkpoint functionality.

### Linux — Universal AppImage
The AppImage runs on any modern 64-bit Linux distribution (Ubuntu, Debian, Fedora, Arch, openSUSE, etc.) without installation:

```bash
# 1. Download AppImage
curl -LO https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-x86_64.AppImage

# 2. Make it executable
chmod +x Swarm-Code-1.0.0-x86_64.AppImage

# 3. Launch Swarm Code
./Swarm-Code-1.0.0-x86_64.AppImage
```

### Linux — Debian / Ubuntu (.deb)
```bash
# 1. Download .deb package
curl -LO https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/Swarm-Code-1.0.0-amd64.deb

# 2. Install package
sudo dpkg -i Swarm-Code-1.0.0-amd64.deb || sudo apt-get install -f -y

# 3. Launch from your application launcher or terminal
swarm-code
```

### Linux — Arch Linux / AUR
PKGBUILD build scripts are included in the source under `packaging/aur/t3code-bin/PKGBUILD` for Arch Linux makepkg installation.

---

## 💎 Key Features

- **Hydra Multi-Agent Orchestration**: Coordinate parallel agent teams. The Lead Agent plans and briefs helper heads (Hank, Walter, Ada), dispatches them in parallel worktrees, and merges their changes back with three-way git conflict resolution.
- **Git Worktree Isolation**: Never let multiple AI agents collide. Every task or Hydra head gets its own dedicated worktree branch.
- **Turn Checkpoints & Interactive Diffs**: Every turn is snapshotted. Inspect exact line-by-line diffs with syntax highlighting, side-by-side comparison, and 1-click revert.
- **Embedded Terminal per Thread**: Built-in xterm emulator beneath every conversation thread running your native shell (PowerShell on Windows, bash/zsh on Linux).
- **Zero Cloud Middleman**: Connects directly to CLI agents or native API keys. No Swarm Code cloud servers, no proxy latency, no markup.
- **Secure OS Credential Storage**: Uses Windows Credential Manager on Windows and FreeDesktop Secret Service / GNOME Keyring / KWallet on Linux via native `@napi-rs/keyring`.
- **Follow-up Message Queue**: Keep typing while an agent works. Prompts queue above the composer and run sequentially.
- **26+ Themes**: Dark, Light, Catppuccin, Tokyo Night, Dracula, Claude, Codex, Matrix, and more.

---

## 🧠 Supported AI Providers

Swarm Code uses the subscriptions and credentials you already have:

| Provider | Integration Type | Login / Setup Command |
| :--- | :--- | :--- |
| **Claude Code** | CLI Process | `claude auth login` |
| **Codex (OpenAI)** | CLI Process | `codex login` |
| **Google Antigravity** | CLI Process | Detected via installed `antigravity` environment |
| **GitHub Copilot CLI** | CLI Process | `copilot auth` |
| **Command Code** | CLI Process | `cmd login` |
| **Pi / OpenCode** | CLI Process | `pi /login` or `opencode auth` |
| **DeepSeek** | Direct API | Set API Key in **Settings › Providers** (Keychain encrypted) |
| **Meta (Muse Spark)** | Direct API | Set API Key in **Settings › Providers** (Keychain encrypted) |
| **OpenAI Compatible** | Direct API / Local | Connect Ollama, vLLM, LM Studio, or custom gateways |

---

## 🛠️ System Architecture

Swarm Code Desktop is built with high-performance modern web technologies and systems engineering:

- **Desktop Shell**: [Electron 44](https://www.electronjs.org/) with secure context isolation, ASLR, and hardware-accelerated rendering.
- **Frontend**: [React 19](https://react.dev/), [TanStack Router](https://tanstack.com/router), [Tailwind CSS v4](https://tailwindcss.com/), and [Lucide Icons](https://lucide.dev/).
- **Backend Concurrency**: [Effect-TS](https://effect.website/) running on [Node.js 22+](https://nodejs.org/) for resilient streaming, fiber-based process management, and cancellation.
- **Local Storage**: Embedded [SQLite](https://www.sqlite.org/) database for sub-millisecond thread switching and offline conversation persistence.
- **Native Hardware Telemetry**: Rust sidecar utilizing `sysinfo` for live CPU/RAM load metrics.
- **Platform Integrations**:
  - Windows: Windows Credential Manager, Direct3D/ANGLE GPU pipeline, PowerShell execution.
  - Linux: D-Bus client (`dbus-next`), FreeDesktop Notifications, GNOME extension bridge, Secret Service API.

---

## 🔄 Automated Updates

Swarm Code Desktop features automatic background updates powered by `electron-updater`:
- Windows checks `latest.yml` on GitHub Releases and applies incremental delta blockmaps.
- Linux checks `latest-linux.yml` for new AppImage or deb package availability.
- Updates are completely optional and never interrupt ongoing tasks.

---

## 📄 License & Attribution

- **License**: Released under the [MIT License](LICENSE).
- **Author**: Created and maintained by [Soumya Chakraborty](https://github.com/soumyachk101).
- **Main Repository**: [github.com/soumyachk101/Swarm-Code](https://github.com/soumyachk101/Swarm-Code)
- **Official Website**: [swarmcode.vercel.app](https://swarmcode.vercel.app)
