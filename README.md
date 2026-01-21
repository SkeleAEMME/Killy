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
- 🏷️ Detect chat type (private / group)  
- 📛 Show sender and group name  
- ⚙️ Clean and modular architecture  

### Discord → Other Platforms
- 📤 Send messages from **Discord to Telegram**  
- 📤 Send messages from **Discord to WhatsApp**:
  - 📞 **Private chats (numbers)**  
    - Phone numbers must be written **with prefix**, fully concatenated, e.g., `{Number}`  
    - Format: `/whatsappnumber {Number} {Message}`
  - 👥 **Group chats**  
    - The **exact group name** must be used  
    - Case-sensitive (uppercase and lowercase must match)  
    - Format: `/whatsappgroup {GroupName} {Message}`  

⚠️ For **WhatsApp private numbers**, a **manual whitelist** is required.  
This whitelist can be managed **only by the bot owner**, for personal security and legal reasons.

### Other Discord Features
- 🔔 Send alerts or notifications inside Discord  
- ⚡ Custom commands and interactions  
- 🛠️ Admin/moderation utilities  
- 🎯 Role or channel management (optional, depends on setup)  

---

## 📜 Commands

### Discord (message export)
- `/telegramma {ID} {Message}` → send message to Telegram channel or private chat  
- `/whatsappnumber {Number} {Message}` → send message to WhatsApp private number (with prefix)  
- `/whatsappgroup {GroupName} {Message}` → send message to WhatsApp group (exact name, case-sensitive)  

### Telegram (message export)
- `/channel_info` → get info of the channel or private chat  
- `/discordia` → send message to Discord [to be implemented]  

### WhatsApp (message export)
- `/discordia` → send message to Discord [to be implemented]  

---

## 🧠 How It Works

1. The **Discord bot is the core application**  
2. Telegram and WhatsApp act as **message sources and targets**  
3. Each incoming message is processed to extract:
   - sender name  
   - chat type (private or group)  
   - group name (if applicable)  
4. Messages can be:
   - imported **from Telegram and WhatsApp into Discord**  
   - sent **from Discord to Telegram and WhatsApp**  
5. Everything is centralized and managed inside Discord  

---

## 📸 Screenshots

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/yu6Zg7T.png)

### Telegram
![Telegram Preview](https://i.imgur.com/nlOfEnN.png)

---

## 🔒 Notes

- Intended for personal automation and message aggregation  
- The **source code will never be public**  
- This **README is public** and exists only to explain how the system works  

---

## 👤 Author

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Created by **SkeleAEMME**  
README.md by **ChatGPT** bc i'm lazy asf
