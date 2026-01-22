# English Version

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

- 📥 Import messages from **Telegram** (DMs and Groups).
- 📥 Import messages from **WhatsApp** (DMs and Groups).
- 📨 Forward messages to **Discord**.
- 🏷️ Detect chat type (private / group).
- 📛 Show sender name and group name.
- 🖼️ Full image support (**Discord ↔ WhatsApp ↔ Telegram**).
- 🔁 Bidirectional message flow.
- ⚙️ Clean and modular architecture.

---

## 📜 Commands

### Discord → Telegram / WhatsApp

- `/telegramma {ID} {Message}`  
  📤 Send a message to a Telegram channel or private chat.

- `/whatsappnumber {Number} {Message} {Image}`  
  📤 Send a message (and optional image) to a WhatsApp private number.  
  `{Number}` must include the prefix, for example `39XXXXXXXXXX`  
  (`39` is the Italian phone prefix).

- `/whatsappgroup {GroupName} {Message} {Image}`  
  📤 Send a message (and optional image) to a WhatsApp group.  
  The group name must be **exact and case-sensitive**.

⚠️ For **WhatsApp private numbers**, a **manual whitelist** is required.  
This whitelist can be managed **only by the bot owner**, for security and legal reasons.

---

## 🖼️ Image Handling

All images are processed **in-memory only**.

### Discord → WhatsApp
- Image is fetched from the **Discord CDN URL**.
- Loaded directly into **RAM**.
- Sent to WhatsApp as media.
- ❌ No file is saved on disk.

### Discord → Telegram
- Image is fetched from the **Discord CDN URL**.
- Loaded directly into **RAM**.
- Sent to Telegram as media.
- ❌ No file is saved on disk.

### WhatsApp → Discord
- Media is downloaded **into RAM only**.
- Converted into a Discord attachment.
- Sender and group information are preserved.
- ❌ No media is stored permanently.

### Telegram → Discord
- Media is downloaded **into RAM only**.
- Converted into a Discord attachment.
- Sender and chat information are preserved.
- ❌ No media is stored permanently.

---

## 🧠 How It Works

1. 🧩 Discord is the **core application**.
2. 📡 Telegram and WhatsApp act as **message sources and targets**.
3. 🧪 Each message is parsed to extract:
   - sender name  
   - chat type (private or group)  
   - group name (if applicable)
4. 🔁 Messages and images flow **in both directions**.
5. 🗂️ Everything is centralized inside Discord.

---

## 📸 Screenshots

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/yu6Zg7T.png)

### Telegram
![Telegram Preview](https://i.imgur.com/nlOfEnN.png)

---

## 🔒 Notes

- 🧠 Intended for personal automation and message aggregation.
- 🔐 The source code will never be published.
- 📄 This README exists only to explain how the system works.

---

## 👤 Author

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Created by **SkeleAEMME**  
README.md by **ChatGPT** bc i'm lazy asf

---

# Versione Italiana

# 🤖 KillyBot

Un **bot per Discord sviluppato in Node.js** che importa e inoltra messaggi da  
**Telegram e WhatsApp** direttamente su Discord.

Il bot funziona come una **casella di posta centralizzata**, permettendo di gestire più piattaforme da Discord.

---

## 🔗 Tecnologie utilizzate

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

## ✨ Funzionalità

- 📥 Importazione messaggi da **Telegram** (privati e gruppi).
- 📥 Importazione messaggi da **WhatsApp** (privati e gruppi).
- 📨 Inoltro messaggi su **Discord**.
- 🏷️ Rilevamento automatico del tipo di chat.
- 📛 Visualizzazione mittente e nome gruppo.
- 🖼️ Supporto completo immagini (**Discord ↔ WhatsApp ↔ Telegram**).
- 🔁 Comunicazione bidirezionale.
- ⚙️ Architettura pulita e modulare.

---

## 📜 Comandi

### Discord → Telegram / WhatsApp

- `/telegramma {ID} {Message}`  
  📤 Invia un messaggio a una chat o canale Telegram.

- `/whatsappnumber {Number} {Message} {Immagine}`  
  📤 Invia un messaggio (con immagine opzionale) a un numero WhatsApp.  
  `{Number}` deve includere il prefisso, ad esempio `39XXXXXXXXXX`  
  (`39` è il prefisso telefonico italiano).

- `/whatsappgroup {GroupName} {Message} {Immagine}`  
  📤 Invia un messaggio (con immagine opzionale) a un gruppo WhatsApp.  
  Il nome deve essere **identico e case-sensitive**.

⚠️ I numeri WhatsApp privati richiedono una **whitelist manuale**, gestita solo dal proprietario del bot.

---

## 🖼️ Gestione delle immagini

Tutte le immagini vengono gestite **esclusivamente in RAM**.

### Discord → WhatsApp
- L’immagine viene presa dall’**URL Discord**.
- Caricata direttamente in **RAM**.
- Inviata a WhatsApp come media.
- ❌ Nessun file viene salvato su disco.

### Discord → Telegram
- L’immagine viene presa dall’**URL Discord**.
- Caricata direttamente in **RAM**.
- Inviata a Telegram come media.
- ❌ Nessun file viene salvato su disco.

### WhatsApp → Discord
- I media vengono scaricati **solo in RAM**.
- Convertiti in allegati Discord.
- Mittente e gruppo vengono mantenuti.
- ❌ Nessun file viene memorizzato.

### Telegram → Discord
- I media vengono scaricati **solo in RAM**.
- Convertiti in allegati Discord.
- Mittente e chat vengono mantenuti.
- ❌ Nessun file viene memorizzato.

---

## 🧠 Come funziona

1. 🧩 Discord è il centro del sistema.
2. 📡 Telegram e WhatsApp sono sorgenti e destinazioni.
3. 🧪 Ogni messaggio viene analizzato per estrarre:
   - mittente  
   - tipo di chat  
   - nome del gruppo
4. 🔁 Messaggi e immagini viaggiano in entrambe le direzioni.
5. 🗂️ Tutto viene gestito da Discord.

---

## 📸 Screenshot

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/yu6Zg7T.png)

### Telegram
![Telegram Preview](https://i.imgur.com/nlOfEnN.png)

---

## 🔒 Note

- 🧠 Pensato per automazione personale.
- 🔐 Il codice sorgente non sarà pubblico.
- 📄 Questo README è solo descrittivo.

---

## 👤 Autore

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Creato da **SkeleAEMME**  
README.md scritto da **ChatGPT** bc sono pigro
