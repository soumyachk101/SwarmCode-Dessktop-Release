# Swarm Code Desktop v1.0.1 — macOS Preview & Auto-Update Release

Official release of **Swarm Code Desktop v1.0.1**, delivering stability fixes for macOS preview builds, updating auto-update feed distribution to `soumyachk101/SwarmCode-Dessktop-Release`, and aligning application packaging with full React 19 / Electron interface parity.

---

### 🚀 Highlights & Fixes

- **Branding & Packaging Alignment**: Bundles macOS preview application as `SwarmCode Dev.app` with Apple Silicon (arm64) runtime to prevent naming collisions with native AppKit installations while delivering 100% React 19 / Electron interface parity.
- **In-App Auto-Update Feed**: Enhanced `electron-updater` differential update distribution via `latest-mac.yml` (`Swarm-Code-1.0.1-arm64.zip`) pointing directly to `soumyachk101/SwarmCode-Dessktop-Release`.
- **DMG Installer Refresh**: Updated macOS DMG background artwork with authentic `SwarmCode Dev` typography and verified drag-to-Applications directory mapping.
- **Cross-Platform Parity**: Full parity across Windows (`.exe`), Linux (`.AppImage`, `.deb`), and macOS with Hydra parallel agent teams, real-time diff checkpoints, embedded terminals, and zero markup.

---

### 📦 Release Assets & Downloads

| File | OS / Target | Format | Checksum (SHA-256) |
| :--- | :--- | :--- | :--- |
| **`SwarmCode-Dev-1.0.1-arm64.dmg`** | macOS (Dev / Testing) | 64-bit Apple Silicon DMG | `1f0b194c4668dab5454f90eafcc32407c62a957b6fa070e63743ccb828d0b747` |
| **`Swarm-Code-1.0.1-arm64.dmg`** | macOS (Installer) | 64-bit Apple Silicon DMG | `1f0b194c4668dab5454f90eafcc32407c62a957b6fa070e63743ccb828d0b747` |
| **`Swarm-Code-1.0.1-arm64.zip`** | macOS (Auto-Update) | 64-bit Update Archive | `7e71ff2c487256c8919889287b1485cbf1f967decbb170787ca5de55e90100df` |
| **`latest-mac.yml`** | macOS | Auto-update feed manifest | macOS update stream manifest |
| **`SHA256SUMS-mac.txt`** | macOS | SHA-256 verification hash | [Download SHA256](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.1/SHA256SUMS-mac.txt) |

---

### 🔐 Verification

To verify the integrity of your downloaded installer, run:

```bash
shasum -a 256 SwarmCode-Dev-1.0.1-arm64.dmg
```
