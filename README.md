# 🛰️ SPACEAPP — General README (v3.0 → v5.x)

*Real-time satellite lookup and tracking platform evolving from lightweight lookup (v3.0) to a scalable, cloud-powered tracking system (v5.x).*

---

## 📦 Version Status

* 🧓 **v3.0** — *Retired (2025)*
* 🗂️ **v4.0 / v4.2** — *Legacy (service extended to May)*
* 🚀 **v5.x Series (Current)**

  * v5.0 — Stable foundation
  * v5.0-beta-x — Experimental builds
  * v5.5.x — Latest stable releases

---

## 🌌 Overview

SPACEAPP is designed for **fast satellite lookup, learning, and real-time tracking**, evolving across versions:

### 🔹 Core Features (All Versions)

* Curated satellite list (~800 objects across 5 categories):

  * Special, Starlink, Science, Weather, GPS
* One-click satellite lookup
* Manual search via NORAD ID
* Live satellite data (position, speed, orbit, etc.)
* Two API modes (Efficient vs Non-efficient)

---

### 🚀 v5.5 Enhancements (Major Upgrade)

* **🔍 Name-Based Lookup** — Search satellites instantly by name
* **☁️ Supabase Pre-Indexed Database** — Faster, smarter, scalable search (10× larger dataset)
* **🌍 `near:` Advanced Sky Search** — Query satellites from any location on Earth
* **📡 Satellite Path Prediction** — Visualize orbital paths + history
* **⚡ Smart API Reduction** — ~25% fewer API calls (adaptive logic)
* **📢 Check Info System** — In-app messages for updates, surveys, announcements
* **💻 x64 Installer** — Clean install experience (no more raw EXE ZIP)

---

## ⚙️ Setup

1. Go to https://www.n2yo.com/ and sign up
2. Copy your **API Key** (called *Developer / License Key* usually at the end of the [page](https://www.n2yo.com/login/edit/))
3. Open SPACEAPP → Signup → paste API key
4. Login and start using the app

✔ Multiple accounts supported
✔ Easy API key switching via login/logout

---

## ⚡ Quick Start

1. Open the app
2. Choose a category (e.g., Science)
3. Click a satellite → view live data
4. Or search by:

   * Name (v5.x)
   * NORAD ID
5. Hover (?) icons for explanations

---

## 🌍 Location Behavior (v5.x)

* Location is estimated via IP
* Cached during session
* Restart app to refresh location
* VPN may affect accuracy

---

## 🗄️ Satellite Database

### ☁️ Cloud Database (v5.x)

* Pre-indexed via Supabase
* Auto-updated
* Handles aliases + edge cases

### 💾 Local Database

* Used for offline + core features
* Periodic updates recommended

⚠️ Do not interrupt updates — may corrupt data

---

## 📊 What Data You’ll See

* Name & NORAD ID
* Live Position
* Orbit / TLE
* Orbital Path (v5.x)
* Speed
* Estimated time in space

---

## 🔁 API Modes (Polling System)

Choose based on performance vs API usage:

### ⚡ Efficient Mode

* Slower updates
* Lower API usage

### 🚀 Non-Efficient Mode

* Faster updates
* Higher API usage

---

### 🧠 v5.5 Smart Optimization

* Starlink (LEO): normal updates
* Non-Starlink (MEO/GEO): updates every other cycle

➡️ ~25% API reduction on average

---

## 💡 Tips for Best Results

* Use curated categories first
* Double-check NORAD IDs
* Use Efficient mode for long sessions
* Keep database updated
* Watch for in-app announcements (v5.x)

---

## 🛠️ Troubleshooting

**No data / errors**

* Check internet
* Switch API mode
* Update database

**App freeze during update**

* Wait → restart if needed
* Reinstall if corrupted

**Search returns nothing**

* Check spelling / NORAD ID
* Satellite may be inactive or renamed

---

## 🔒 Privacy

SPACEAPP uses public satellite data APIs.
**No personal data is collected beyond required functionality.**

---

## 📬 Support

Contact: *[tanbinhvo.hcm@gmail.com](mailto:tanbinhvo.hcm@gmail.com)*

---

## 👤 Credits

Vo Tan Binh (Henry Vo) — Sole developer of SPACEAPP

---

## © License

© Vo Tan Binh / SPACEAPP. All rights reserved.
Unauthorized redistribution or reuse is prohibited unless permitted by the author.

---

## 🛰️ Open Source v3.0

The original public release, SPACEAPP Open Source v3.0, is available separately under the MIT License.

Repository:
https://github.com/Henrycoding-design/SpaceappwebOpenSrc

---

## 🧾 Notes

Most features are self-explained in the interface.
This README highlights key behaviors and safe-use guidelines.

🚀 *Enjoy exploring the sky with SPACEAPP — from v3 roots to v5 scalability.*
