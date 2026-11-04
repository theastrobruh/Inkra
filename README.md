# 🃏 Oricas Generator

> A free, browser-based tool to arrange trading card proxies (oricas) into print-ready, real-scale (1:1) grid layouts — no installation required.

![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-222?logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![No dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen)

---

## ✨ Features

- 📐 **True 1:1 scale output** — cards print at exact physical dimensions
- 🃏 **Game presets** — Cardfight!! Vanguard, Yu-Gi-Oh!, Pokémon / Magic / Lorcana, Tarot, Mini Euro and more
- 📄 **Multiple paper formats** — A4, Letter, Legal, A3 · Portrait & Landscape
- ✂️ **Crop marks** — optional cutting guides for every card
- 🌐 **i18n** — English, Español, Deutsch
- 🖨️ **Print / Save PDF** — directly from the browser, no plugins needed
- 🗂️ **Duplicate & Delete** per-card controls in-preview
- 📦 **100% client-side** — works offline, nothing uploaded to any server

---

## 🚀 Usage

### Online
Open the live site → upload your orica images → configure paper & card size → **Print / Save PDF**.

### Local
Just open `oricas_generator.html` in any modern browser. No server needed.

---

## 🖨️ Printing Tips

| Setting | Recommended value |
|---|---|
| Scale | **100% / Actual Size** |
| Margins | **None** |
| Background graphics | **Enabled** |
| Paper size | Match the selector in the tool |

---

## 🗂️ Project Structure

```
├── oricas_generator.html   # The entire app (HTML + CSS + JS, self-contained)
├── index.html              # GitHub Pages entry point (redirects to the app)
├── README.md
├── .gitattributes
├── .gitignore
└── .github/
    └── workflows/
        └── deploy.yml      # GitHub Actions — auto-deploy to GitHub Pages
```

---

## 🛠️ Development

Since this is a self-contained HTML file, there's no build step.  
Edit `oricas_generator.html` and push — GitHub Actions will deploy automatically.

---

## 📄 License

MIT © 2026 — Free to use and modify.
