<p align="center">
  <img src="https://github.com/zShift1/FallenWare-Releases/raw/main/logo.png" alt="FallenWare" width="120">
</p>

<h1 align="center">FallenWare</h1>

<p align="center">
  <b>The glass-dark Fast Flags studio for Roblox on Windows.</b><br>
  Edit. Inject. Play.
</p>

<p align="center">
  <a href="https://github.com/zShift1/FallenWare-Releases/releases"><img src="https://img.shields.io/badge/Download-v4.0.2-5865F2?style=for-the-badge&logo=windows&logoColor=white" alt="Download"></a>
  <a href="https://discord.gg/Dxg8Ayj4RY"><img src="https://img.shields.io/badge/Discord-join-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"></a>
  <img src="https://img.shields.io/badge/Windows-10%2F11-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/.NET-8-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET 8">
</p>

---

## 📥 Download

Grab the latest installer from the [Releases page](https://github.com/zShift1/FallenWare-Releases/releases).

| File | Size | Link |
| --- | --- | --- |
| `setup.exe` | ~76 MB | [Download v4.0.2](https://github.com/zShift1/FallenWare-Releases/releases/download/v4.0.2/setup.exe) |

> This repository ships **installers only**. The source code is private.

---

## 🚀 Installation

1. Download `setup.exe` from the [Releases page](https://github.com/zShift1/FallenWare-Releases/releases).
2. Run it — requires **Administrator** privileges (the installer prompts automatically).
3. Done. FallenWare installs to `C:\Program Files\FallenWare\` and creates a desktop shortcut.

### Requirements

- **Windows 10 or 11 (x64)**
- No .NET install needed — the installer is fully self-contained.

---

## ✨ Features

- **Live flag editing** — apply Fast Flags without restarting Roblox
- **Single-click injection** — inject changes straight into the running client
- **Presets** — one-click flag sets (`V1` → `V35`), custom profiles, and `.swcfg` configs
- **Customization** — custom title, colors, glass buttons, and a background photo
- **Mods** — custom cursor and font packs
- **Auto offsets** — fetch & live-dump offsets after every Roblox update
- **Silent operation** — no console window, runs entirely in the tray-backed UI

---

## 🧠 How it works

```
FallenWare.exe ── JSON-RPC over named pipe ──▶ FallenWare.Core.exe ──▶ RobloxPlayerBeta
                                                     │
                                                     └── reads/writes Roblox memory
```

The UI never touches the game. A privileged C# sidecar (`FallenWare.Core.exe`) handles all injection — clean separation, faster iteration.

---

## 📦 Data & Configuration

Everything is stored in `%APPDATA%\FallenWare\`:

| File | Purpose |
| --- | --- |
| `flags.json` | Your active Fast Flags |
| `presets.json` | Saved presets |
| `app_settings.json` | App settings (theme, colors, RPC) |
| `configs/` | `.swcfg` profiles |
| `offsets/` | Roblox offsets |

Uninstalling does **not** delete your data — it's preserved for the next install.

---

## ❓ FAQ

**Is my data safe?**  
Yes — flags, presets and configs live in `%APPDATA%\FallenWare\` and survive reinstallations.

**Do I need to install .NET?**  
No. The installer is self-contained (x64, .NET 8 included).

**Why no source code?**  
This repo hosts official builds only. The source is maintained in a private repository.

**Does it work on Roblox updates?**  
Yes — offsets are fetched and re-dumped so injection keeps working after game updates.

---

## 📜 Changelog

### v4.0.2
- Silent C# core — no console window ever again
- New animated collapsible sidebar UI
- Rebranded app, core, data path and pipe under the **FallenWare** name
- Migrated data folder to `%APPDATA%\FallenWare`
- Discord RPC integration

---

<p align="center">
  <sub>Built with ♥ by <a href="https://github.com/zShift1">zShift1</a></sub>
</p>