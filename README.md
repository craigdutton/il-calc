# Insertion Loss Calculator — Standalone Mobile (PWA)

A responsive, offline-capable web app for **fibre optic insertion loss testing**.  
Designed for use directly in the field on mobile or tablet — no internet connection required after the first load.

---

## 🚀 Features

- 📱 **Mobile-first design** – large touch-friendly inputs and buttons  
- ⚡ **Instant PASS/FAIL results** for each wavelength and direction (A ➜ B / B ➜ A)  
- 💾 **Local storage** – save, load, delete, and export test results  
- 📊 **Auto calculations** based on:
  - Fibre type (OS1/OS2, OM1–OM5)
  - Length, connectors, and splices
- 📤 **Export options**
  - Download all tests as a `.csv`
  - Export to Google Sheets via your own Apps Script Web App URL
- 🧮 **Auto-incrementing Cable ID** when saving “Next Core”
- 🔋 **Offline mode** – works fully without connectivity
- 🧭 **PWA-enabled** – install it as an app on your home screen

---

## 🧱 Project Structure

```
.
├── index.html
├── insertion-loss-calculator-mobile.html
├── manifest.webmanifest
├── sw.js
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── .nojekyll
```

> Both `index.html` and `insertion-loss-calculator-mobile.html` are identical for compatibility.  
> `manifest.webmanifest` and `sw.js` enable offline caching and PWA installation.

---

## 📦 Installation (Local or Field Deployment)

### Option 1 — Run locally
1. Download or clone this repository.
2. Open `index.html` in your browser (works offline).

### Option 2 — Deploy on GitHub Pages
Already live here:  
👉 [**https://craigdutton.github.io/il-calc/**](https://craigdutton.github.io/il-calc/)

> Once opened, choose “Add to Home Screen” on mobile Safari or Chrome to install it as a standalone app.

---

## ⚙️ Updating the App

Whenever you make changes:

1. Open **`sw.js`** and bump the cache name, for example:
   ```js
   const CACHE_NAME = "il-mobile-v11";
   ```
2. Commit and push your changes.
3. Reload the site using a query string to force an update:  
   `https://craigdutton.github.io/il-calc/?v=11`

---

## 🧩 Optional: Google Sheets Integration

To export data online:
1. Create a Google Apps Script Web App that writes to your Sheet.
2. Paste its URL into the **“Google Sheets Web App URL”** field in the calculator.
3. Tests will export automatically when you press **Export All** or **Export** next to a test.

---

## 📲 PWA Installation

**iOS (Safari)**  
1. Open [https://craigdutton.github.io/il-calc/](https://craigdutton.github.io/il-calc/)  
2. Tap **Share → Add to Home Screen**  
3. Launch it like a native app (full-screen, offline ready)

**Android (Chrome)**  
1. Visit the same URL  
2. Tap the **Install App** prompt (or ⋮ → “Install app”)  
3. Launch from your home screen

---

## 🧰 Built With
- HTML5 + Vanilla JavaScript
- LocalStorage for offline data persistence
- Service Worker for caching and offline access
- Tailwind CSS utility styles (via CDN)
- GitHub Pages for hosting

---

## 🧑‍💻 Author
**Craig Dutton**  
Field Tools for Fibre Testing · Built for reliability and simplicity

---

## 🪄 License
This project is released under the [MIT License](LICENSE).  
Use, modify, and deploy freely.
