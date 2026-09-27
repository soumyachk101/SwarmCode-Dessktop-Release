# Swarm Code Desktop v1.0.0 — Official Windows & Linux Release

Official release of **Swarm Code Desktop v1.0.0**, introducing standalone 64-bit Windows installers and universal Linux binaries with complete multi-agent workflow parity.

---

### 🚀 Highlights

- **Native Windows Support**: Complete Windows 10 & 11 (64-bit x64) experience packaged via NSIS (`Swarm-Code-1.0.0-x64.exe`) with hardware acceleration and Windows Credential Manager integration.
- **Universal Linux Packaging**: Available as standalone universal x86_64 AppImage (`Swarm-Code-1.0.0-x86_64.AppImage`) and Debian/Ubuntu `.deb` (`Swarm-Code-1.0.0-amd64.deb`) with D-Bus FreeDesktop notifications and system tray support.
- **Hydra Multi-Agent Orchestration**: Coordinate parallel agent teams (Hank, Walter, Ada) across isolated Git worktrees with automatic three-way merge resolution.
- **Turn Checkpoints & Diffs**: Real-time checkpointing with syntax-highlighted multi-hunk diff review and 1-click turn revert.
- **Embedded Terminal per Thread**: Full PTY terminal integration running native shells (PowerShell on Windows, bash/zsh on Linux).
- **12+ AI Providers (Zero Markup)**: Connect Claude Code, Codex, Antigravity, Copilot, Cursor, OpenCode, Grok, DeepSeek, Meta, and OpenAI-compatible local models directly on your own subscriptions.
- **Automated Update Feeds**: Seamless in-app update checks powered by `electron-updater` via `latest.yml`, `latest-linux.yml`, and `latest-mac.yml`.

---

### 📦 Release Assets & Downloads

| File | OS / Target | Format | Checksum |
| :--- | :--- | :--- | :--- |
| **`Swarm-Code-1.0.0-arm64.dmg`** | macOS (Dev / Preview) | 64-bit Apple Silicon DMG | `2954520be85068959435bec...` |
| **`Swarm-Code-1.0.0-arm64.zip`** | macOS (Auto-Update) | 64-bit Update Archive | `df94f8769aa2daf880bac33...` |
| **`Swarm-Code-1.0.0-x64.exe`** | Windows 10/11 | 64-bit NSIS Installer | `0e29ea07e90d6a4d7aa174d...` |
| **`Swarm-Code-1.0.0-x86_64.AppImage`** | Linux (Universal) | 64-bit AppImage | `30d727a31855546e6ec59dc...` |
| **`Swarm-Code-1.0.0-amd64.deb`** | Ubuntu / Debian | 64-bit Debian Package | `cfdf6724f7490e9cd91ba23...` |
| **`latest-mac.yml`** | macOS | Auto-update feed manifest | macOS update stream |
| **`latest.yml`** | Windows | Auto-update feed manifest | Windows differential updater |
| **`latest-linux.yml`** | Linux | Auto-update feed manifest | Linux update stream |
| **`SHA256SUMS-mac.txt`** | macOS | SHA-256 verification hash | [Download SHA256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/SHA256SUMS-mac.txt) |
| **`SHA256SUMS-windows.txt`** | Windows | SHA-256 verification hash | [Download SHA256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/SHA256SUMS-windows.txt) |
| **`SHA256SUMS-linux.txt`** | Linux | SHA-256 verification hash | [Download SHA256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.0/SHA256SUMS-linux.txt) |

---

### 🔐 Verification

To verify the integrity of your downloaded installer, run the corresponding command:

**macOS (Terminal):**
```bash
shasum -a 256 Swarm-Code-1.0.0-arm64.dmg
```

**Windows (PowerShell):**
```powershell
Get-FileHash -Algorithm SHA256 Swarm-Code-1.0.0-x64.exe
```

**Linux (Bash):**
```bash
sha256sum Swarm-Code-1.0.0-x86_64.AppImage
sha256sum Swarm-Code-1.0.0-amd64.deb
```
