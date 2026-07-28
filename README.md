# VCMC for PC 2.0

<div align="center">

<img src="https://antoic.com/icons/vcmc.png" width="110" alt="VCMC logo">

**A proximity voice chat tool for Minecraft Bedrock and Java/Geyser**

[Download latest release](../../releases/latest) · [Documentation](https://antoic.com/docs/vcmc.html) · [Changelog](https://antoic.com/changelog/vcmc/) · [Discord](https://discord.gg/HA5gKcpsaq)

[![Version](https://img.shields.io/badge/VCMC-2.0-5865F2)](https://antoic.com/changelog/vcmc/2.0.0.html)
[![Windows](https://img.shields.io/badge/Windows-Installer-0078D7?logo=windows&logoColor=white)](../../releases/latest)
[![Microsoft Store](https://img.shields.io/badge/Microsoft-Store-107C10?logo=microsoft&logoColor=white)](https://apps.microsoft.com/detail/9N74NFWF305Q)

</div>

## What This Repository Contains

This repository distributes the desktop version of VCMC:

- Windows installer
- Microsoft Store package
- Linux AppImage when included in a release

VCMC is also available for [Android](https://play.google.com/store/apps/details?id=com.naru.vcmc), [iOS](https://apps.apple.com/mx/app/vcmc-voice-chat-for-mc/id6784284005), and [the web](https://antoic.com/play/vcmc/).

## What VCMC Does

VCMC connects voice to Minecraft player positions. Nearby players sound louder, distant players sound quieter, and the app automatically changes connections as players move, change dimensions, enter groups, or leave the game.

It works with:

| Minecraft mode | Required component |
|---|---|
| Bedrock world | VCMC app + Addon World + Resource Pack |
| Dedicated Bedrock server | VCMC app + Addon Server + Resource Pack |
| Java or Java/Geyser server | VCMC app + VCMC Java plugin |

## Install on Windows

Choose one:

1. Download the installer from [GitHub Releases](../../releases/latest).
2. Install VCMC from the [Microsoft Store](https://apps.microsoft.com/detail/9N74NFWF305Q).

The Microsoft Store version receives automatic updates. GitHub releases are useful when the Store is unavailable.

Windows may request microphone and network permissions on first launch. Both are required for voice chat.

## Quick Start

### Bedrock World

1. Install the VCMC app.
2. Add `VCMC - WORLD` and the Resource Pack to the host's world.
3. Enable WebSockets and disable **Encrypted WebSockets only** in Minecraft.
4. Everyone enters the host's room in VCMC.
5. The host copies the generated `/wsserver` command into Minecraft.
6. Each guest copies and pastes their own `/vcmc:verify "<code>"`.

Only the host installs the Addon. Guests still verify individually before VCMC places them in the world's secure voice subroom.

### Dedicated Bedrock Server

1. The administrator installs Addon Server and the Resource Pack.
2. Add the server in VCMC.
3. Join Minecraft.
4. Copy `/vcmc:verify "<code>"` from the app and paste it in chat.

The Addon creates and restores the server room automatically.

### Java or Java/Geyser Server

1. The administrator installs the VCMC plugin.
2. Add the server in VCMC.
3. Join Minecraft.
4. Copy `/vcmc:verify "<code>"` from the app and paste it in chat.

Java and Bedrock players can share the same voice room when the server uses Geyser.

## VCMC 2.0 Features

- Distance and spatial voice
- Secure World subrooms
- Voice groups with optional passwords
- Administrative and hidden groups
- Built-in, environmental, and custom effects
- Megaphone routing
- Master and per-player volume
- App and Minecraft settings synchronization
- Input and output device selection
- Push to talk on Windows
- Persistent recordings with microphone, remote voices, and effects
- Custom-dimension support
- Improved P2P, SFU, connection, and reconnection behavior
- Compatibility with older Addons, plugins, and app versions through the legacy protocol

## World Verification in VCMC 2.0

The old World flow connected every guest directly after the host pasted a link. VCMC 2.0 protects each world with a separate subroom:

- The host links the world once with `/wsserver`.
- Every guest receives a personal `/vcmc:verify` command.
- The verification button updates if the code changes.
- It disappears after the player is verified.
- Returning verified players reconnect automatically.

## Removed Commands

`/vcmc:join`, `/vcmc:room`, and `/vcmc:reconnect` are no longer used. Room discovery and reconnection happen automatically.

## Minecraft Components

- [Bedrock Addon](https://github.com/narucreations1-hub/Voice-Chat-Minecraft-Bedrock-VCMC-Addon)
- [Java/Geyser plugin](https://github.com/narucreations1-hub/Voice-Chat-Minecraft-Geyser-Plugin)
- [Plugin on CurseForge](https://www.curseforge.com/minecraft/bukkit-plugins/vcmc-voice-chat-for-mc-pluggin)

## Troubleshooting

### Minecraft does not show as connected

- Confirm that the app is inside the correct room.
- In World mode, the host must link Minecraft before guests verify.
- Confirm that the Gamertag in VCMC exactly matches the Minecraft name.
- Reopen the room if the app reports that the VCMC service is unavailable.

### Other players can hear me, but I cannot hear them

- Check the selected output device and Windows volume mixer.
- Confirm that the master and per-player volumes are above zero.
- Disable call or communication-device processing from other applications.

### A verification command is still visible

Paste the newest command shown by VCMC. After the server confirms the player, the command disappears automatically.

For more help, use the [official documentation](https://antoic.com/docs/vcmc.html) or contact the [VCMC Discord](https://discord.gg/HA5gKcpsaq).

## Release Notes

- [VCMC 2.0 changelog](https://antoic.com/changelog/vcmc/2.0.0.html)
- [Complete version history](https://antoic.com/changelog/vcmc/)

VCMC is a free, independent project created by Naru. It is not affiliated with Mojang Studios. Minecraft is a trademark of Mojang AB.
