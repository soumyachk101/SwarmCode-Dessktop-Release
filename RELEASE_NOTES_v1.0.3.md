# Swarm Code Desktop v1.0.3 — Windows & Linux Update

**Swarm Code Desktop v1.0.3** fixes multiple MCP dialog UI rendering issues on Windows and Linux, restoring proper form layout and interaction feedback after a shared UI component refactor. All fixes are synced with the latest macOS codebase.

---

### 🐛 Bug Fixes

#### Custom MCP Server Dialog
- **Section Labels Restored**: All field labels (Server name, Transport, Command, Arguments, Server URL, Environment variables/Headers) now render with correct text styling (`text-xs font-medium text-foreground`). Labels were rendering unstyled after a UI refactor removed the default className.
- **Transport Radio Cards — Selection Feedback Fixed**: Selecting Stdio or HTTP transport now visibly highlights the chosen card with a primary-colored border and tinted background. The `data-checked:` Tailwind classes were previously applied to an inner `<div>` wrapper instead of the `<Radio>` element itself, making the selected state invisible.
- **Monospace Inputs — Font Restored**: Command, arguments (textarea), and URL input fields now display text in a proper monospace font. The previous `font="mono"` React prop was non-standard and silently ignored; replaced with the correct `font-mono` CSS class.
- **Variable Trash Button — Hover Color Fixed**: The delete (trash) button on each environment variable row now correctly shows destructive red coloring on hover. The color classes were applied to a parent `<div>` instead of the Button element, causing CSS specificity issues.
- **Accessibility — `aria-labelledby` Restored**: The Transport RadioGroup now correctly references its section label via `aria-labelledby` for screen reader compatibility.

---

### 📦 Release Assets

| OS / Target | Format | File |
| :--- | :--- | :--- |
| **Windows 10/11** | NSIS 64-bit Setup | [`Swarm-Code-1.0.3-x64.exe`](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.3/Swarm-Code-1.0.3-x64.exe) |
| **Linux (Universal)** | Universal AppImage | [`Swarm-Code-1.0.3-x86_64.AppImage`](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.3/Swarm-Code-1.0.3-x86_64.AppImage) |
| **Ubuntu / Debian** | Debian Package | [`Swarm-Code-1.0.3-amd64.deb`](https://github.com/soumyachk101/SwarmCode-Dessktop-Release/releases/download/v1.0.3/Swarm-Code-1.0.3-amd64.deb) |

> **macOS users**: Continue receiving updates via the [Swarm-Code-Release](https://github.com/soumyachk101/Swarm-Code-Release) repository (currently on v1.8.11).

---

### 🔧 Technical Details

| Component | File | Change Type |
| :--- | :--- | :--- |
| Custom MCP Server Dialog | `CustomMCPServerDialog.tsx` | UI bug fix (6 issues) |
| SectionLabel sub-component | `CustomMCPServerDialog.tsx` | Restored default styling + added `id` prop |
| Radio card layout | `CustomMCPServerDialog.tsx` | Fixed `data-checked:` target element |
| Input styling | `CustomMCPServerDialog.tsx` | `font="mono"` → `className="font-mono"` |
| Button specificity | `CustomMCPServerDialog.tsx` | Destructive classes moved to Button element |

---

Built with Electron 44, React 19, TypeScript, Tailwind CSS v4. MIT Licensed.
