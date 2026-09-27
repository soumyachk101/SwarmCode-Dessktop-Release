# Changelog

All notable changes to Swarm Code Desktop (Windows & Linux) are documented in this file, newest first. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions match the release tags without the leading `v`.

---

## [Unreleased]

### Planned
- **Windows on ARM (ARM64)**: Native binary builds optimized for Snapdragon X Elite and ARM64 Windows laptops.
- **Linux Flatpak Distribution**: Official Flathub package with sandboxed portal permissions.
- **Portable Windows Edition**: Zero-install standalone archive (`.zip`) for restricted enterprise environments.

---

## [1.0.0] - 2026-09-27

### Summary
Swarm Code Desktop 1.0.0 is the inaugural official cross-platform desktop release bringing the complete Swarm Code multi-agent AI coding environment to Windows and Linux. Built with modern web architecture (Electron 44, React 19, TypeScript, Effect-TS, Tailwind CSS v4) and backed by a native Node.js 22+ engine with a Rust resource monitor sidecar, Swarm Code Desktop delivers 100% workflow parity with the native macOS experience—on your own subscriptions, with zero markup, zero telemetry, and zero cloud sync.

### macOS Dev / Preview Build (Apple Silicon)
- **Standalone DMG Installer**: Built for developer verification and testing (`Swarm-Code-1.0.0-arm64.dmg`), packaged as `SwarmCode Dev.app` with Apple Silicon (arm64) runtime.
- **In-App Update Stream**: Configured with `latest-mac.yml` and differential update package (`Swarm-Code-1.0.0-arm64.zip`) pointing to `soumyachk101/SwarmCode-Dessktop-Release`.

### Official Windows Support
- **Standalone 64-bit Installer**: Distributed as a streamlined NSIS installer (`Swarm-Code-1.0.0-x64.exe`) supporting Windows 10 and Windows 11 (64-bit x64).
- **Native Windowing & Frame**: Native Windows title bar styling with Windows 11 rounded corners, Snap Layouts support, and responsive window controls.
- **Hardware Acceleration**: High-performance Direct3D 11/12 and ANGLE GPU hardware acceleration for smooth 120 fps token streaming and fluid interface rendering.
- **Git for Windows Discovery**: Automatic discovery and integration with Git for Windows installations (`C:\Program Files\Git\cmd\git.exe`, `LocalAppData\Programs\Git\bin\git.exe`), including configured credentials and SSH keys.
- **Windows Credential Manager Integration**: Encrypted local storage for provider API keys (DeepSeek, Meta, OpenAI-compatible) and credentials using Windows Credential Manager via native `@napi-rs/keyring`.
- **PowerShell & CMD Terminal Integration**: Integrated terminal per thread automatically launches PowerShell 7+, Windows PowerShell, or CMD with full ANSI color and PTY support.
- **WSL Runtime Support**: Built-in compatibility layer detecting Windows Subsystem for Linux (WSL 2) distributions and projects.

### Official Linux Support
- **Universal AppImage**: Standalone universal x86_64 AppImage (`Swarm-Code-1.0.0-x86_64.AppImage`) runnable across Ubuntu, Debian, Fedora, Arch Linux, openSUSE, and Pop!_OS without installation.
- **Debian / Ubuntu Package**: Native `.deb` package (`Swarm-Code-1.0.0-amd64.deb`) with proper desktop entry (`swarm-code.desktop`), MIME type registrations, and icons installed to `/usr/share/icons/hicolor`.
- **Arch Linux / AUR Packaging**: PKGBUILD scripts provided under `packaging/aur/` for Arch User Repository package building (`swarm-code-bin`).
- **FreeDesktop Notifications**: Native Linux desktop notifications conforming to the FreeDesktop Notification specification via D-Bus, complete with application icon and action click handlers.
- **D-Bus Secret Service Integration**: Encrypted credential storage using the FreeDesktop Secret Service API (`org.freedesktop.secrets`), seamlessly integrating with GNOME Keyring and KDE KWallet via `@napi-rs/keyring`.
- **System Tray Integration**: Dedicated system tray icon with status menu, quick thread launch, and background running capabilities.
- **GNOME Shell Extension Support**: Optional GNOME extension (`apps/desktop/gnome-extension`) for window capture, workspace management, and system overlay integration.

### Core Multi-Agent Features (Workflow Parity)
- **Hydra Parallel Agent Teams**: One chat coordinates a team of helper agents ("heads"). The Lead Agent writes briefs, dispatches parallel heads into isolated Git worktrees, tracks live progress badges, and lands finished code as a clean three-way merge.
- **Flexible Lead/Head Pairs**: Pair high-reasoning lead models (e.g. Claude 3.7 Sonnet / Opus, GPT-5 / Codex) with rapid execution heads (Gemini 2.5 Flash, OpenCode, DeepSeek) with fused effort sliders.
- **Git Worktree Isolation**: Run multiple parallel coding agents on the same repository without file collision or branch contention.
- **Turn Checkpoints & Diff Reviewer**: Every turn records a local checkpoint. Review additions and deletions with an interactive multi-hunk diff viewer featuring side-by-side and unified views, with 1-click turn reverts.
- **Integrated Terminal per Thread**: Fully-featured terminal emulator embedded beneath every thread with shell persistence and keyboard focus switching.
- **Follow-up Message Queue**: Type prompts while the agent is executing; follow-ups line up smoothly and dispatch automatically upon turn completion.
- **Questions & Approvals Tab**: Interactive approval cards and tool confirmation dialogs keep execution safe without blocking background threads.

### Supported AI Providers
- **CLI-Based Subscriptions (Zero Markup)**: Claude Code (`claude auth login`), Codex CLI (`codex login`), Google Antigravity, GitHub Copilot CLI, Command Code, Pi, and OpenCode.
- **Direct API Providers**: DeepSeek (with remaining balance indicator), Meta (Muse Spark), and Z.ai.
- **Custom Endpoints**: Fully compatible with any OpenAI-compatible or local inference server (Ollama, vLLM, LM Studio).

### Desktop Updates & Release Infrastructure
- **Automated Update Stream**: Integrated `electron-updater` querying GitHub Releases via `latest.yml` (Windows) and `latest-linux.yml` (Linux) with differential blockmap downloads.
- **Cryptographic Verification**: Every release asset published with SHA-256 checksums (`SHA256SUMS-windows.txt` and `SHA256SUMS-linux.txt`).
- **Privacy & Telemetry**: Zero analytics, zero cloud middlemen, zero tracking. All conversation databases (SQLite), worktrees, and keys remain strictly local to your machine.
