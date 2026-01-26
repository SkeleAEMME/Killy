# English Version

# 🤖 KillyBot

A **Discord bot built with Node.js** that imports messages from **Telegram and WhatsApp** into Discord **and allows sending messages from Discord to Telegram and WhatsApp**.  
The bot acts as a **central inbox inside Discord**, allowing you to manage multiple platforms from one place.

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
- 📛 Show sender name and group name  
- 🖼️ Full image support (**Discord ↔ WhatsApp ↔ Telegram**)  
- 🔁 Bidirectional message flow  
- ⚙️ Clean and modular architecture  
- 💾 **Autocomplete support for all Discord commands** (`/whatsappgroup`, `/whatsappnumber`, `/telegramma`) based on saved chat/group info  
- 📇 **WhatsApp contact management**:
  - `/crea-contatto {Name} {Number}` → save a new contact  
  - `/elimina-contatto {Number}` → remove a contact  
  - `/info-contatto {Number}` → get info: Name, WhatsApp ID, profile picture, Business account, registration date & time (GMT+1 Rome)  
- 🔁 **Telegram → Discord** via `/discordia` command (documentation is directly in the command itself; images not yet supported)  
- 🔁 **WhatsApp → Discord** `/discordia` coming by the end of the week  
- 🔒 Only the bot owner or users with database access can view **sensitive data (WhatsApp phone numbers only)**  

---

## 📜 Commands

### Discord → Telegram / WhatsApp

- `/telegramma {ID} {Message}`  
  📤 Send a message to a Telegram channel or private chat  
  💾 Autocomplete suggests previously used groups or private chats for authorized users

- `/whatsappnumber {Number} {Message} {Image}`  
  📤 Send a message (and optional image) to a WhatsApp private number  
  `{Number}` must include the prefix, e.g., `39XXXXXXXXXX`  
  💾 Autocomplete suggests previously used private chat IDs for authorized users

- `/whatsappgroup {GroupName} {Message} {Image}`  
  📤 Send a message (and optional image) to a WhatsApp group  
  The group name must be **exact and case-sensitive**  
  💾 Autocomplete suggests previously used group names for authorized users

- `/crea-contatto {Name} {Number}`  
  📇 Register a new WhatsApp contact

- `/elimina-contatto {Number}`  
  ❌ Delete a WhatsApp contact

- `/info-contatto {Number}`  
  ℹ️ Show contact info:
  - Name  
  - WhatsApp ID  
  - Profile picture URL  
  - Business account or not  
  - Registration date/time in **DD/MM/YYYY HH:MM GMT+1 Rome**

- Telegram `/discordia`  
  🔁 Send messages from Telegram to Discord. See command help for usage.  
  ⚠️ Images are **not yet supported**.  

- WhatsApp `/discordia`  
  🔜 Coming by the end of the week

⚠️ For **WhatsApp private numbers**, a **manual whitelist** is required and managed only by the bot owner

---

## 🖼️ Image Handling

All images are processed **in-memory only**

### Discord → WhatsApp
- Image is fetched from the **Discord CDN URL**  
- Loaded directly into **RAM**  
- Sent to WhatsApp as media  
- ❌ No file is saved on disk

### Discord → Telegram
- Image is fetched from the **Discord CDN URL**  
- Loaded directly into **RAM**  
- Sent to Telegram as media  
- ❌ No file is saved on disk

### WhatsApp → Discord
- Media is downloaded **into RAM only**  
- Converted into a Discord attachment  
- Sender and group information are preserved  
- ❌ No media is stored permanently

### Telegram → Discord
- Media is downloaded **into RAM only**  
- Converted into a Discord attachment  
- Sender and chat information are preserved  
- ❌ No media is stored permanently

---

## 🧠 How It Works

1. 🧩 Discord is the **core application**  
2. 📡 Telegram and WhatsApp act as **message sources and targets**  
3. 🧪 Each message is parsed to extract:
   - sender name  
   - chat type (private or group)  
   - group name (if applicable)  
4. 💾 Only **chat/group info and contacts** are saved for autocomplete (no messages):
   - WhatsApp: group names, group IDs, private chat IDs (contain phone numbers)  
   - Telegram: group names, private chat names, group IDs, private chat IDs  
5. 🔁 Messages and images flow **in both directions**  
6. 🗂️ Everything is centralized inside Discord  
7. 🔒 Sensitive data saved for autocomplete: **WhatsApp phone numbers only**

---

## 📸 Screenshots

### Discord → Telegram
![Discord → Telegram](https://i.imgur.com/hJqd7BW.png)

### Discord → Telegram Group
![Discord → Telegram Group](https://i.imgur.com/U6MFJqO.png)

### Discord → WhatsApp
![Discord → WhatsApp](https://i.imgur.com/GIKCUBt.png)

### Discord → WhatsApp Group
![Discord → WhatsApp Group](https://i.imgur.com/7PItUjE.png)

### Telegram → Discord
![Telegram → Discord](https://i.imgur.com/ZE2i8Nd.png)

### /crea-contatto, /info-contatto, /elimina-contatto
![Contacts](https://i.imgur.com/75kAVDe.png)

---

## 🔒 Notes

- 🧠 Intended for personal automation and message aggregation  
- 🔐 The source code will never be published  
- 📄 Only the bot owner or authorized users can view **sensitive data (WhatsApp phone numbers only)**

---

## 👤 Author

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Created by **SkeleAEMME**  
README.md by **ChatGPT (GPT-5 mini)**

---

# Versione Italiana

# 🤖 KillyBot

Un **bot per Discord sviluppato in Node.js** che importa messaggi da **Telegram e WhatsApp** su Discord **e permette di inviare messaggi da Discord verso Telegram e WhatsApp**.  
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

- 📥 Importazione messaggi da **Telegram** (privati e gruppi)  
- 📥 Importazione messaggi da **WhatsApp** (privati e gruppi)  
- 📨 Inoltro messaggi su **Discord**  
- 🏷️ Rilevamento automatico del tipo di chat  
- 📛 Visualizzazione mittente e nome gruppo  
- 🖼️ Supporto completo immagini (**Discord ↔ WhatsApp ↔ Telegram**)  
- 🔁 Comunicazione bidirezionale  
- ⚙️ Architettura pulita e modulare  
- 💾 **Autocomplete su tutti i comandi Discord** (`/whatsappgroup`, `/whatsappnumber`, `/telegramma`) basato solo su:
  - WhatsApp: nomi dei gruppi, ID dei gruppi, ID chat private (contengono numeri)  
  - Telegram: nomi dei gruppi, nomi chat private, ID dei gruppi, ID chat private  
- 📇 **Gestione contatti WhatsApp**:
  - `/crea-contatto {Nome} {Numero}` → registra un nuovo contatto  
  - `/elimina-contatto {Numero}` → elimina un contatto  
  - `/info-contatto {Numero}` → mostra info contatto: Nome, ID WhatsApp, foto profilo, account Business, data/ora registrazione in **DD/MM/YYYY HH:MM GMT+1 Roma**  
- 🔁 **Telegram → Discord** tramite comando `/discordia` (spiegazione direttamente nel comando; immagini non ancora supportate)  
- 🔁 **WhatsApp → Discord** `/discordia` in arrivo entro fine settimana  
- 🔒 Solo l’owner del bot o utenti autorizzati possono visualizzare **dati sensibili (numeri WhatsApp solamente)**

---

## 📜 Comandi

- `/telegramma {ID} {Messaggio}`  
  📤 Invia un messaggio a una chat o canale Telegram  
  💾 Autocomplete suggerisce gruppi o chat private precedentemente utilizzati per utenti autorizzati

- `/whatsappnumber {Numero} {Messaggio} {Immagine}`  
  📤 Invia un messaggio (con immagine opzionale) su WhatsApp ad un numero  
  `{Numero}` deve includere il prefisso, es. `39XXXXXXXXXX`  
  💾 Autocomplete suggerisce chat private precedentemente utilizzate per utenti autorizzati

- `/whatsappgroup {NomeGruppo} {Messaggio} {Immagine}`  
  📤 Invia un messaggio (con immagine opzionale) su un gruppo WhatsApp  
  Il nome deve essere **identico e case-sensitive**  
  💾 Autocomplete suggerisce gruppi precedentemente utilizzati per utenti autorizzati

- `/crea-contatto {Nome} {Numero}`  
  📇 Registra un nuovo contatto WhatsApp

- `/elimina-contatto {Numero}`  
  ❌ Elimina un contatto WhatsApp

- `/info-contatto {Numero}`  
  ℹ️ Mostra info contatto:
  - Nome  
  - ID WhatsApp  
  - Foto profilo  
  - Account Business o meno  
  - Data/ora registrazione in **DD/MM/YYYY HH:MM GMT+1 Roma**

- Telegram `/discordia`  
  🔁 Invia messaggi da Telegram a Discord. Vedere aiuto comando per dettagli.  
  ⚠️ Le immagini **non sono ancora supportate**

- WhatsApp `/discordia`  
  🔜 Arriverà entro fine settimana

⚠️ I numeri privati WhatsApp richiedono una **whitelist manuale**, gestita solo dall’owner del bot

---

## 🖼️ Gestione delle immagini

Tutte le immagini vengono gestite **esclusivamente in RAM**

### Discord → WhatsApp
- Immagine presa dall’**URL Discord**  
- Caricata direttamente in **RAM**  
- Inviata a WhatsApp come media  
- ❌ Nessun file salvato su disco

### Discord → Telegram
- Immagine presa dall’**URL Discord**  
- Caricata direttamente in **RAM**  
- Inviata a Telegram come media  
- ❌ Nessun file salvato su disco

### WhatsApp → Discord
- Media scaricato **solo in RAM**  
- Convertito in allegato Discord  
- Mittente e gruppo preservati  
- ❌ Nessun file salvato permanentemente

### Telegram → Discord
- Media scaricato **solo in RAM**  
- Convertito in allegato Discord  
- Mittente e chat preservati  
- ❌ Nessun file salvato permanentemente

---

## 🧠 Come funziona

1. 🧩 Discord è il **centro del sistema**  
2. 📡 Telegram e WhatsApp agiscono come **sorgenti e destinazioni**  
3. 🧪 Ogni messaggio viene analizzato per estrarre:
   - mittente  
   - tipo di chat (privata o gruppo)  
   - nome del gruppo (se applicabile)  
4. 💾 Solo **info chat/gruppo e contatti** salvate per autocomplete (nessun messaggio):
   - WhatsApp: nomi dei gruppi, ID dei gruppi, ID chat private (contengono numeri)  
   - Telegram: nomi dei gruppi, nomi chat private, ID dei gruppi, ID chat private  
5. 🔁 Messaggi e immagini viaggiano **in entrambe le direzioni**  
6. 🗂️ Tutto è centralizzato in Discord  
7. 🔒 Dati sensibili salvati per autocomplete: **solamente numeri di telefono**

---

## 📸 Screenshot

### Discord → Telegram
![Discord → Telegram](https://i.imgur.com/hJqd7BW.png)

### Discord → Telegram Group
![Discord → Telegram Group](https://i.imgur.com/U6MFJqO.png)

### Discord → WhatsApp
![Discord → WhatsApp](https://i.imgur.com/GIKCUBt.png)

### Discord → WhatsApp Group
![Discord → WhatsApp Group](https://i.imgur.com/7PItUjE.png)

### Telegram → Discord
![Telegram → Discord](https://i.imgur.com/ZE2i8Nd.png)

### /crea-contatto, /info-contatto, /elimina-contatto
![Contacts](https://i.imgur.com/75kAVDe.png)

---

## 🔒 Note

- 🧠 Pensato per automazione personale e aggregazione messaggi  
- 🔐 Il codice sorgente non sarà pubblico  
- 📄 Solo l’owner del bot o utenti autorizzati possono visualizzare **dati sensibili (solamente numeri di Telefono)**

---

## 👤 Autore

<p align="left">
  <a href="https://t.me/Dr1ft7" target="_blank">
    <img src="https://img.shields.io/badge/Telegram-@Dr1ft7-26A5E4?style=for-the-badge&logo=telegram&logoColor=white"/>
  </a>
</p>

Creato da **SkeleAEMME**  
README.md by **ChatGPT (GPT-5 mini)**
