# Swarm Code Desktop v1.0.2 — Multi-OS Universal Release

Official release of **Swarm Code Desktop v1.0.2** across **macOS, Windows, and Linux**, fixing a critical projector decoding bug during thread creation and ensuring seamless multi-agent coding across all platforms.

---

### 🚀 Highlights & Fixes

- **Thread Creation & Orchestration Bug Fix**: Resolves `Projector decode failed for thread.created:thread: Expected string | undefined at ["hydraParentThreadId"]` by permitting both `null` and `undefined` in schema decoders across `OrchestrationThread`, `ThreadCreateCommand`, and `ThreadCreatedPayload`.
- **Universal Multi-OS Release**:
  - **macOS (Apple Silicon)**: Standalone `SwarmCode-Dev-1.0.2-arm64.dmg` & `Swarm-Code-1.0.2-arm64.dmg` with in-app differential auto-updater (`Swarm-Code-1.0.2-arm64.zip`).
  - **Windows 10/11 (64-bit)**: Streamlined NSIS installer (`Swarm-Code-1.0.2-x64.exe`) with PowerShell/CMD integration, Credential Manager, and WSL runtime support.
  - **Linux (Universal)**: Standalone AppImage (`Swarm-Code-1.0.2-x86_64.AppImage`) and Debian/Ubuntu `.deb` (`Swarm-Code-1.0.2-amd64.deb`).
- **Complete Workflow Parity**: Full parity across all platforms with Hydra parallel agent teams, real-time diff checkpoints, embedded terminals, and zero cloud markup.

---

### 📦 Release Assets & Downloads

| OS / Target | Format | File |
| :--- | :--- | :--- |
| **macOS (Apple Silicon)** | DMG Installer | [**`SwarmCode-Dev-1.0.2-arm64.dmg`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/SwarmCode-Dev-1.0.2-arm64.dmg) |
| **macOS (Apple Silicon)** | DMG Installer | [**`Swarm-Code-1.0.2-arm64.dmg`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/Swarm-Code-1.0.2-arm64.dmg) |
| **macOS (Auto-Update)** | Update Archive | [**`Swarm-Code-1.0.2-arm64.zip`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/Swarm-Code-1.0.2-arm64.zip) |
| **Windows 10/11** | NSIS 64-bit Setup | [**`Swarm-Code-1.0.2-x64.exe`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/Swarm-Code-1.0.2-x64.exe) |
| **Linux (Universal)** | Universal AppImage | [**`Swarm-Code-1.0.2-x86_64.AppImage`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/Swarm-Code-1.0.2-x86_64.AppImage) |
| **Ubuntu / Debian** | Debian Package | [**`Swarm-Code-1.0.2-amd64.deb`**](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.2/Swarm-Code-1.0.2-amd64.deb) |
