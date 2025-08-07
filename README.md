REPO Broken - WIll fix it soon

# Marstek LilyGO + Home Assistant Configuration

Welcome!  
This repository contains my personal configuration for integrating a **Marstek Plug-in Battery** with **Home Assistant** using **ESPHome** and the **LilyGO T-Display RS485 (T-CAN485)**.

You'll find:

- 🧠 My **Home Assistant Dashboard YAML**
- 🔌 My **ESPHome Modbus configuration** for LilyGO
- 📊 Helpful links and resources for Modbus integration
- 📷 UI Screenshots from both Home Assistant and the LilyGO Web UI

> I hope this setup helps others working on similar energy monitoring projects!

---

## 🔧 What’s Inside

- ESPHome config for LilyGO T-Display RS485 (`t-can485`)
- Dashboard YAML for Home Assistant (Lovelace) with Mushroom and ESPHome Integration
- Optimized Modbus settings for Marstek batteries
- Inspiration and references for deeper Modbus integration

## 📦 Requirements

- ✅ Home Assistant (2023.6+ recommended)
- ✅ [ESPHome](https://esphome.io) (configured via USB or OTA)
- ✅ [HACS](https://hacs.xyz) – Home Assistant Community Store
- ✅ [Mushroom UI Cards](https://github.com/piitaya/lovelace-mushroom)
- ✅ LilyGO T-Display RS485 (`T-CAN485`)
- ✅ Marstek Battery with RS485 Modbus support
---

## 📸 Screenshots

### Home Assistant Dashboard
<img width="1634" height="763" alt="Screenshot 2025-08-05 193034" src="https://github.com/user-attachments/assets/8601715d-cf4d-4362-a433-e1585aa6486f" />
<img width="1625" height="744" alt="Screenshot 2025-08-05 193042" src="https://github.com/user-attachments/assets/cf8b575d-1923-488f-932c-92e6b2b52167" />

### LilyGO Web UI
<img width="1510" height="4504" alt="192 168 178 160_" src="https://github.com/user-attachments/assets/52b085ab-14dc-4d53-a86e-b2c9cca3bac4" />


---

## 🔗 Credits & Resources

Big thanks to everyone whose work helped this integration succeed:

- 📘 **Modbus Register Documentation**  
  [Duravolt Plug-in Battery Modbus.pdf](https://duravolt.nl/wp-content/uploads/Duravolt-Plug-in-Battery-Modbus.pdf)

- 💡 **@Superduper1969** – MarstekVenus-LilygoRS485  
  [GitHub Repository](https://github.com/Superduper1969/MarstekVenus-LilygoRS485/tree/main)

- 💬 **Tweakers Community Discussions**  
  - [Topic 1](https://gathering.tweakers.net/forum/list_messages/2282240)  
  - [Topic 2](https://gathering.tweakers.net/forum/list_messages/2262054)

- 🧰 **scruysberghs** – ha-marstek-venus  
  [GitHub Repository](https://github.com/scruysberghs/ha-marstek-venus)

- 📑 **Google Spreadsheet – Modbus Register Overview**  
  [Public Sheet](https://docs.google.com/spreadsheets/u/0/d/e/2PACX-1vSyu0LKoSrQQzvrosMH-sOcSKT7pgHSXEwAcIJe0cy3NCrmwiLH6VDGjh0_2HOKhL0nZmnI3Mk5Fb_d/pubhtml?gid=319238506&single=true&pli=1)

---

## 🙏 Final Note

If this repository helped you, feel free to star ⭐ it or contribute back.  
Let’s build smarter energy systems together!
