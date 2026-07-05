# VCMC — Proximity Voice Chat for Minecraft

<div align="center">

<img src="https://antoic.com/icons/vcmc.png" width="110" alt="VCMC Logo">

**The easiest proximity voice chat for Minecraft Bedrock and Java**

[📥 Download App](https://antoic.com/app.html) · [📖 Documentation](https://antoic.com/docs/vcmc.html) · [💬 Discord](https://discord.gg/HA5gKcpsaq)

[![Android](https://img.shields.io/badge/Android-Google_Play-34A853?logo=googleplay&logoColor=white)](https://play.google.com/store/apps/details?id=com.naru.vcmc)
[![Windows](https://img.shields.io/badge/Windows-Microsoft_Store-0078D7?logo=windows&logoColor=white)](https://apps.microsoft.com/detail/9N74NFWF305Q)
[![Linux](https://img.shields.io/badge/Linux-AppImage-E95420?logo=linux&logoColor=white)](https://github.com/NARUxd/Voice-Chat-Minecraft-PC-VCMC/releases)

</div>

---

## This Repository

This repo contains the official **VCMC desktop app** releases for **Windows** (`.exe` installer) and **Linux** (`AppImage`).

👉 **[Download latest release →](../../releases/latest)**

---

## What is VCMC?

VCMC is a **free proximity voice chat app for Minecraft**. Talk to nearby players in real time — the further away they are, the quieter they sound.

Originally built for **Minecraft Bedrock**, VCMC now also supports **Java servers via the Geyser plugin**. No Discord, no external calls, no complex configuration. Just open the app, paste one command in the Minecraft chat, and you're talking.

---

## Why VCMC?

| Feature | VCMC | Others |
|---|:---:|:---:|
| Minecraft Bedrock support | ✅ | ❌ Rare |
| Java + Geyser support | ✅ | ❌ Rare |
| Local worlds | ✅ | ❌ |
| Dedicated server support | ✅ | Sometimes |
| Setup time | ~30 seconds | Hours |
| Floating overlay (control mic in-game) | ✅ | Sometimes |
| In-game mute indicator on screen | ✅ | ✅ (rare) |
| Nametag mute indicator | ✅ | ✅ (rare) |
| **Config synced Minecraft ↔ app** | ✅ | ❌ |
| Android + Windows + Linux | ✅ | Sometimes |
| Free | ✅ | Sometimes |

> The one thing no other proximity chat does yet: your in-game VCMC settings sync straight to the app (and back). Most other differences are things competitors *sometimes* have — the linked config is the real standout.

---

## Downloads

### App (required on every device)

| Platform | Link |
|---|---|
| 📱 Android | [Google Play](https://play.google.com/store/apps/details?id=com.naru.vcmc) |
| 🖥️ Windows | [Microsoft Store](https://apps.microsoft.com/detail/9N74NFWF305Q) · [GitHub (.exe)](https://github.com/NARUxd/Voice-Chat-Minecraft-PC-VCMC/releases) |
| 🐧 Linux | [GitHub (AppImage)](https://github.com/NARUxd/Voice-Chat-Minecraft-PC-VCMC/releases) |
| 🍎 iOS | Coming soon |

### Minecraft Files

| File | Link |
|---|---|
| 🟩 Bedrock Addon (.mcaddon) | [Voice-Chat-Minecraft-Bedrock-VCMC-Addon/releases](https://github.com/narucreations1-hub/Voice-Chat-Minecraft-Bedrock-VCMC-Addon/releases) |
| ☕ Java Plugin (.jar) | [CurseForge](https://www.curseforge.com/minecraft/bukkit-plugins/vcmc-voice-chat-for-mc-pluggin) |

---

## Compatibility

| Mode | Platform | What you need |
|---|---|---|
| **Local World** | Minecraft Bedrock | App + Addon (World pack) |
| **Bedrock Server** | Any Bedrock server | App + Addon (Server pack) |
| **Java Server** | Java server with Geyser | App + VCMC Plugin (.jar) |

---

## App Interface

### First Launch
On first launch VCMC asks for **microphone permission** — required for voice chat to work. After granting it, you reach the main menu.

From the main menu you can:
- **Download the Addon** directly to your device
- Open **World Rooms** — for local Minecraft worlds
- Open **Server Rooms** — for Bedrock or Java servers

### World Rooms
Use this when you are hosting or joining a local Minecraft world.

- **Host:** Tap **MY WORLD** to create a room. The app gives you a command to paste in Minecraft chat.
- **Friends:** Tap **+**, enter the host's Gamertag, and join their room. No command needed on their side.

### Server Rooms
Use this for dedicated Bedrock or Java (Geyser) servers.

You no longer enter an IP or port. The server creates its own VCMC room automatically — each player just adds a room with any name they like, then verifies once inside Minecraft with `/vcmc:verify`. After verifying, your device is remembered and you won't have to repeat it.

### Floating Bubble (Overlay)
Once connected, a small floating bubble stays visible over every app including Minecraft. No need to switch apps to manage your mic.

| Bubble state | Meaning |
|---|---|
| 🟢 Green | Connected — microphone active |
| 🔴 Red | Muted |
| 🔌 Plug icon | Disconnected from Minecraft |

Tap the bubble to toggle mute. Long-press to reposition it anywhere on screen.

### In-Game Indicators *(rare in other apps)*
- A **message appears on your Minecraft screen** every time you mute or unmute
- A **symbol next to your nametag** shows your mic state to nearby players in real time

---

## How to Use

### Mode 1 — Local World (Bedrock)

1. **Host:** Open VCMC → tap **MY WORLD** → a room is created.
2. **Friends:** Open VCMC → tap **+** → enter the host's Gamertag → join the room.
3. **Host:** Install the **World** behavior pack in your Minecraft world. In world settings → General: enable Websockets and disable "Encrypted Websockets only".
4. **Host:** Open the floating bubble → copy the link → paste it in the Minecraft chat.
5. ✅ Everyone hears each other with proximity audio.

> Only the host installs the addon and pastes the command. Friends only join the room in the app.

### Mode 2 — Bedrock Server

1. Upload the **Server** behavior pack + resource pack to your server.
2. For non-Aternos servers, add `@minecraft/server-net` to `config/default/permissions.json`.
3. Players open VCMC → **SERVER** → add a room with any name.
4. Each player copies the `/vcmc:verify` command the app shows and pastes it in Minecraft chat (once per device).
5. ✅ Proximity voice chat is active.

### Mode 3 — Java Server with Geyser

1. Drop the VCMC `.jar` into your server's `plugins/` folder and restart.
2. The plugin creates the server's VCMC room automatically (you'll see it in the console).
3. Players open VCMC → **SERVER** → add a room with any name → paste `/vcmc:verify` in chat.
4. ✅ Works for both Java and Bedrock players on the same server.

---

## Commands Reference

> **Local World mode has no commands** — the host just pastes the bubble link in the chat. The commands below are for **servers**, where each player connects by verifying once with `/vcmc:verify`.

### Bedrock Addon (Server)

| Command | Description |
|---|---|
| `/vcmc:verify <code>` | Verify your account with the code shown in the app (once per player/device) |
| `/vcmc:menu` | Open your personal VCMC menu — settings, groups and per-player volume |
| `/vcmc:admin` | Open the server admin panel (operators only) |
| `/vcmc:mute <selector> <true\|false>` | Force-mute or restore a player. Example: `/vcmc:mute @a[name=Steve] true` |
| `/vcmc:reconnect` | Check your connection and force an immediate re-check |
| `/vcmc:room` | Show the server's internal Room ID (admins / diagnostics) |
| `/vcmc:join <room_id> [token]` | ⚠️ Legacy/advanced — manually override the saved room. Not the normal flow |

### Java Plugin (Geyser)

| Command | Description |
|---|---|
| `/vcmc:verify "<code>"` | Verify your account with the app's code (paste with quotes) |
| `/vcmc:menu` | Personal menu in a chest UI: settings, groups, per-player volume |
| `/vcmc:admin` | Admin panel in a chest UI. Requires OP or `vcmc.admin` |
| `/vcmc:mute <player\|@a> <true\|false>` | Silence or restore a player |
| `/vcmc:groups create/join/leave/list` | Create and manage voice groups |
| `/vcmc:room` | Show the server's internal Room ID |
| `/vcmc:reconnect` | Check if your app appears connected to the server |

---

## Full Documentation

Step-by-step guide with screenshots, troubleshooting and all configuration options:

📖 **[antoic.com/docs/vcmc.html](https://antoic.com/docs/vcmc.html)**

---

## About the Project

VCMC is part of **[Antoic Projects](https://antoic.com)** — apps and tools for Minecraft created by **Naru**.

This is a **solo project**. Updates may take time, but every bug report makes the app better. Thank you for your patience and support 🙏

### Found a bug?
- Report it in the [Discord server](https://discord.gg/HA5gKcpsaq)
- Or open an [Issue](../../issues) in this repository

### Support the project
VCMC is free and always will be. If it has been useful to you:

💙 [paypal.me/NaruBoing](https://www.paypal.com/paypalme/NaruBoing)

---

*Unofficial Minecraft application. Not affiliated with Mojang AB. "Minecraft" is a trademark of Mojang AB. [Mojang Brand Guidelines](http://account.mojang.com/documents/brand_guidelines).*