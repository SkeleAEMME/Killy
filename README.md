# 🤖 KillyBot

A **Discord bot built with Node.js** that imports and forwards messages from  
**Telegram and WhatsApp** directly into Discord.

The bot acts as a **central inbox inside Discord**, allowing you to receive messages from multiple social platforms in one place.

---

## 🔗 Built With

<p align="left">
  <a href="https://nodejs.org/" target="_blank">
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white"/>
  </a>

  <a href="https://discord.js.org/" target="_blank">
    <img src="https://img.shields.io/badge/discord.js-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>
  </a>

  <a href="https://telegraf.js.org/" target="_blank">
    <img src="https://img.shields.io/badge/Telegraf.js-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>

  <a href="https://wwebjs.dev/" target="_blank">
    <img src="https://img.shields.io/badge/whatsapp--web.js-25D366?style=for-the-badge&logo=whatsapp&logoColor=white"/>
  </a>
</p>

---

## ✨ Features

- 📥 Import messages from **Telegram** (DMs and Groups)  
- 📥 Import messages from **WhatsApp** (DMs and Groups)  
- 📨 Forward messages to **Discord**  
- 🧠 Ignore old/unread messages on startup  
- 🏷️ Detect chat type (private / group)  
- 📛 Show sender and group name  
- ⚙️ Clean and modular architecture  

### Other Discord Features
- 🔔 Send alerts or notifications inside Discord  
- ⚡ Custom commands and interactions  
- 🛠️ Admin/moderation utilities  
- 🎯 Role or channel management (optional, depends on setup)  

---

## 🧠 How It Works

1. The **Discord bot is the core application**  
2. Telegram and WhatsApp act only as **message sources**  
3. Each incoming message is processed to extract:
   - sender name
   - chat type (private or group)
   - group name (if applicable)
4. The message is forwarded into Discord, keeping everything centralized

---

## 📸 Screenshots

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/TGAAt5Z.jpeg)

### Telegram
![Telegram Preview](https://i.imgur.com/hIJfjjD.jpeg)

---

## 🔒 Notes

- Tokens and credentials must never be committed  
- Session folders should be excluded via `.gitignore`  
- Intended for personal automation and message aggregation

---

## 👤 Author

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Created by **SkeleAEMME**
README.md by **ChatGPT** bc i'm lazy asf
