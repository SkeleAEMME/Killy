#English Version

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
- 📨 Forward messages to **Discord.**  
- 🏷️ Detect chat type (private / group).  
- 📛 Show sender and group name.  
- ⚙️ Clean and modular architecture.  

### Discord → Other Platforms
- 📤 Send messages from **Discord to Telegram.**  
- 📤 Send messages from **Discord to WhatsApp**:
  - 📞 **Private chats (numbers)**  
    - Phone numbers must be written **with prefix**, fully concatenated, e.g., `{Number}`  
    - Format: `/whatsappnumber {Number} {Message}`
  - 👥 **Group chats**  
    - The **exact group name** must be used.  
    - Case-sensitive (uppercase and lowercase must match).  
    - Format: `/whatsappgroup {GroupName} {Message}`  

⚠️ For **WhatsApp private numbers**, a **manual whitelist** is required.  
This whitelist can be managed **only by the bot owner**, for personal security and legal reasons.

### Other Discord Features
- 🔔 Send alerts or notifications inside Discord.  
- ⚡ Custom commands and interactions.  
- 🛠️ Admin/moderation utilities.  
- 🎯 Role or channel management (optional, depends on setup).  

---

## 📜 Commands

### Discord (message export)
- `/telegramma {ID} {Message}` → send message to Telegram channel or private chat.  
- `/whatsappnumber {Number} {Message}` → send message to WhatsApp private number (with prefix).  
- `/whatsappgroup {GroupName} {Message}` → send message to WhatsApp group (exact name, case-sensitive).  

### Telegram (message export)
- `/channel_info` → get info of the channel or private chat.  
- `/discordia` → send message to Discord. [to be implemented]  

### WhatsApp (message export)
- `/discordia` → send message to Discord. [to be implemented]  

---

## 🧠 How It Works

1. The **Discord bot is the core application.**  
2. Telegram and WhatsApp act as **message sources and targets.**  
3. Each incoming message is processed to extract:
   - sender name  
   - chat type (private or group)  
   - group name (if applicable)  
4. Messages can be:
   - imported **from Telegram and WhatsApp into Discord**  
   - sent **from Discord to Telegram and WhatsApp**  
5. Everything is centralized and managed inside Discord.  

---

## 📸 Screenshots

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/yu6Zg7T.png)

### Telegram
![Telegram Preview](https://i.imgur.com/nlOfEnN.png)

---

## 🔒 Notes

- Intended for personal automation and message aggregation.  
- The **source code will never be published.**  
- This **README is public** and exists only to explain how the system works.  

---

## 👤 Author

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Created by **SkeleAEMME**  
README.md by **ChatGPT** bc i'm lazy asf

#Italian Version

# 🤖 KillyBot

Un **bot per Discord costruito con Node.js** che importa e inoltra messaggi da  
**Telegram e WhatsApp** direttamente su Discord.

Il bot funge da **cassettone centrale di messaggi all’interno di Discord**, permettendoti di ricevere messaggi da più piattaforme social in un unico posto.

---

## 🔗 Tecnologie

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

- 📥 Importa messaggi da **Telegram** (chat private e gruppi).  
- 📥 Importa messaggi da **WhatsApp** (chat private e gruppi).  
- 📨 Inoltra messaggi su **Discord**.  
- 🏷️ Rileva il tipo di chat (privata / gruppo).  
- 📛 Mostra il nome del mittente e il nome del gruppo.  
- ⚙️ Architettura pulita e modulare.  

### Discord → Altre Piattaforme
- 📤 Invia messaggi da **Discord a Telegram**.  
- 📤 Invia messaggi da **Discord a WhatsApp**:  
  - 📞 **Chat private (numeri)**.  
    - I numeri telefonici devono essere scritti **con prefisso**, tutti attaccati, es.: `{Number}`.  
    - Formato: `/whatsappnumber {Number} {Message}`.  
  - 👥 **Chat di gruppo**.  
    - Deve essere usato **il nome esatto del gruppo WhatsApp**.  
    - Sensibile alle maiuscole/minuscole.  
    - Formato: `/whatsappgroup {GroupName} {Message}`.  

⚠️ Per i **numeri WhatsApp privati**, è richiesta una **whitelist manuale**.  
Questa whitelist può essere gestita **solo dal proprietario del bot**, per motivi di sicurezza personale e legali.

### Altre funzionalità di Discord
- 🔔 Invio di avvisi o notifiche all’interno di Discord.  
- ⚡ Comandi slash personalizzati e interazioni.  
- 🛠️ Utility per amministrazione/moderazione.  
- 🎯 Gestione di ruoli o canali (opzionale, dipende dalla configurazione).

---

## 📜 Comandi

### Discord (invio messaggi)
- `/telegramma {ID} {Message}` → invia un messaggio a un canale o chat privata Telegram.  
- `/whatsappnumber {Number} {Message}` → invia un messaggio a un numero WhatsApp privato (con prefisso).  
- `/whatsappgroup {GroupName} {Message}` → invia un messaggio a un gruppo WhatsApp (nome esatto, case-sensitive).  

### Telegram (invio messaggi)
- `/channel_info` → ottiene informazioni sul canale o sulla chat privata corrente.  
- `/discordia` → invia un messaggio a Discord *(in sviluppo)*.  

### WhatsApp (invio messaggi)
- `/discordia` → invia un messaggio a Discord *(in sviluppo)*.  

---

## 🧠 Come funziona

1. Il **bot Discord è l’applicazione principale**.  
2. Telegram e WhatsApp agiscono come **sorgenti/bersagli di messaggi**.  
3. Ogni messaggio in arrivo viene processato per estrarre:  
   - nome del mittente;  
   - tipo di chat (privata o gruppo);  
   - nome del gruppo (se applicabile).  
4. I messaggi possono essere:  
   - importati **da Telegram e WhatsApp verso Discord**;  
   - inviati **da Discord verso Telegram e WhatsApp**.  
5. Tutto viene centralizzato e gestito dentro Discord.  

---

## 📸 Screenshot

### WhatsApp
![WhatsApp Preview](https://i.imgur.com/TGAAt5Z.jpeg)

### Telegram
![Telegram Preview](https://imgur.com/a/M3tW2k4)

---

## 🔒 Note

- Pensato per automazione personale e aggregazione di messaggi.  
- Il **codice sorgente non sarà mai pubblico**.  
- Questo **README è pubblico** e serve solo a spiegare come funziona il sistema.  

---

## 👤 Autore

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Creato da **SkeleAEMME**.  
README.md scritto da **ChatGPT** bc i’m lazy asf.
