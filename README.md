# VCMC - Voice Chat for Minecraft Bedrock

**VCMC** is the ultimate tool for integrating advanced proximity voice communication into your Minecraft games, whether in local worlds or dedicated servers.

<p align="center">
  <img src="assets/logojpg.png" alt="VCMC Icon" width="128">
</p>

---

## 🚀 Getting Started

The application is divided into two main sections: **Servers** and **Worlds**. 

**Important:** You must install the official VCMC Addon to play. You can now download the Addon directly from inside the VCMC App! (Or download it manually from our [GitHub Releases](https://github.com/narucreations1-hub/VCMC-ADDON/releases)).

![Tabs Overview](assets/image.png)

---

## 🌍 Mode: Worlds (Local P2P)

Ideal for playing with friends in local worlds. **Note: In this mode, custom commands do not exist.** The connection is established purely through a direct link.

### For the Host (World Creator):
1. Go to the **Worlds** tab and select the **My World** option.
   ![My World Section](assets/myworld.jpeg)
2. **In Minecraft:** Apply the **World** version of the VCMC Behavior Pack to your game.
   > ⚠️ **CRITICAL REQUIREMENT:**
   > In your Minecraft General Settings, you MUST turn **ON** "Enable WebSockets" and turn **OFF** "Require Encrypted WebSockets". Otherwise, Minecraft will kick you from your own world.
3. Once inside the app room and your Minecraft world, you will see a **Link** at the top of the app (or in the floating bubble).
   ![Command Link](assets/link.jpeg)
4. Click the link to copy it, and paste it into your Minecraft world's chat.

### For Guests (Joining a friend):
1. In the **Worlds** tab, tap the **Add Friend** (+) button located at the bottom right.
   ![Add Button](assets/add.jpeg)
2. Type the Host's exact gamertag. Once added, click on their name in the list.
3. You will enter the room where you can see all participants. 
4. **You're all set!** Just join your friend's world in Minecraft. You don't need to paste any commands or change your WebSocket settings.

---

## 🖥️ Mode: Servers (Aternos, BDS, etc.)

Configuration for 24/7 communities and dedicated servers. 
*⚠️ You MUST use the **Server** version of the Behavior Pack for this to work.*

### Server Setup (Admin):
1. Install the Addon (Resource Pack & Server Behavior Pack) into your server files.
2. **Non-Aternos Hosts (BDS, Paid Hosts):** You MUST give the Addon internet permissions. Go to your server files: `config/default/permissions.json` and add `"@minecraft/server-net"` to the `"allowed_modules"` list. *(Aternos users can skip this step).*
3. In the app, go to the **Servers** tab, press the (+) button, and enter the **IP** and **Port** of your server.
4. Enter the server room in the app, copy the `/vcmc:join...` link, and paste it into the Minecraft server chat. **You only need to do this ONCE forever.**

### Commands (Server Mode Only):
* `/vcmc:join` - Links the app room to the server (Admin only).
* `/reconnect` - If the app disconnects or you stop hearing people, type this in the game chat to fix it instantly. *(Note: Recording and other old commands have been temporarily removed to improve performance).*

---

## 💬 Floating Bubble Guide

The floating bubble in Android tells you your connection status at a glance:
* 🟢 **Green:** Everything is perfect. Connected and Mic is active.
* 🔴 **Red:** You are Muted.
* ⚪ **Transparent:** Normal background state.
* 🔌 **Plug Icon:** **Disconnected from Minecraft!** Paste the link again (World mode) or type `/reconnect` (Server mode).

---

## 🛠️ Requirements Table

| Feature | Local World (Host) | Local World (Guest) | Servers (IP/Port) |
| :--- | :--- | :--- | :--- |
| **Addon Version** | **WORLD** Pack | No Addon Needed | **SERVER** Pack |
| **Profile WebSocket**| ✅ Must be ON | ❌ Not Required | ❌ Not Required |
| **Encrypted Websocket**| ❌ Must be OFF | ❌ Not Required | ❌ Not Required |

---

## 🤝 Community & Support

* **Documentation:** Read our easy-to-follow guide [here](https://antoic.netlify.app/docs/vcmc.html).
* **Video Tutorial:** Watch the setup guide here: [Watch Tutorial](https://youtu.be/LydcPINpo8A?si=boGhZgMJ8d9eD0jy)
* **YouTube Channel:** Subscribe for more updates: [@NARUBOY](https://www.youtube.com/@NARUBOY)
* **Discord:** Join our community for updates and support: [Join Discord](https://discord.gg/HA5gKcpsaq)
* **Play Store:** Download the app to support the project: [Download VCMC](https://play.google.com/store/apps/details?id=com.naru.vcmc)
* **Donate:** Support development via PayPal: [paypal.me/NaruBoing](https://paypal.me/NaruBoing)

---

## 👤 Creator

<p align="center">
  <img src="./naru.png" alt="Creator" width="100" style="border-radius: 50%;">
  <br>
  Developed by <b>Naru</b>
</p>
