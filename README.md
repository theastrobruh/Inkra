# Inkra

> A free, browser-based studio to arrange trading card proxies into print-ready, real-scale (1:1) grid layouts — no installation required.

<p align="center">
  <a href="https://theastrobruh.github.io/Inkra/">
    <img src="https://img.shields.io/badge/%E2%96%B6%20Open%20Inkra-Try%20it%20now-4f46e5?style=for-the-badge&logoColor=white" alt="Open Inkra — try it now" height="44">
  </a>
</p>

**Live app: [theastrobruh.github.io/Inkra](https://theastrobruh.github.io/Inkra/)**

![GitHub Actions](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-222?logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Features

- **Search cards online** — Magic: The Gathering, Pokémon TCG, Yu-Gi-Oh! and Disney Lorcana.
- **Upload local images** — PNG, JPG and WEBP, including multiple files at once.
- **Paste an image URL** — useful when a card is not listed in the supported databases.
- **True 1:1 scale output** — cards print at exact physical dimensions.
- **Download a real-size PDF** — each page matches the selected paper size, ready for USB, sharing or printing. The PDF embeds the images, so it does not depend on the original websites.
- **Game presets** — Cardfight!! Vanguard, Yu-Gi-Oh!, Pokémon / Magic / Lorcana, Tarot, Mini Euro and custom sizes.
- **Multiple paper formats** — A4, Letter, Legal, A3 — Portrait & Landscape.
- **Crop marks** — optional cutting guides for every card.
- **i18n** — English, Español, Deutsch.
- **Print / Save PDF from the browser** — a separate browser-print flow is still available.
- **Duplicate & Delete** per-card controls in the preview.
- **Runs in the browser** — card search requests go directly from your browser to the public card APIs; nothing is uploaded to an Inkra server.

---

## Usage

### Online

**[Open Inkra →](https://theastrobruh.github.io/Inkra/)** then:

1. Choose **Search online** or **Upload**.
2. Add the cards you want to the sheet.
3. Configure paper, orientation, card size, spacing and crop marks.
4. Click **Download PDF** for a real-size file, or **Print** for the browser print dialog.

### Local

Open `inkra.html` in any modern browser. The PDF engine is included in `vendor/`, so PDF export works without a build step.

> Card search requires an internet connection because it uses public card databases.

---

## Printing tips

| Setting | Recommended value |
|---|---|
| Scale | **100% / Actual Size** |
| Margins | **None** |
| Background graphics | **Enabled** |
| Paper size | Match the selector in the tool |

For the most predictable result when sharing or moving files on a USB drive, use **Download PDF**: the PDF is generated at the exact paper and card dimensions and contains the card images.

---

## Card data sources

| Game | Source |
|---|---|
| Magic: The Gathering | [Scryfall API](https://scryfall.com/docs/api) |
| Pokémon TCG | [Pokémon TCG API](https://docs.pokemontcg.io/) |
| Yu-Gi-Oh! | [YGOPRODeck API](https://ygoprodeck.com/api-guide/) |
| Disney Lorcana | [Lorcana API](https://lorcana-api.com/) |

Card search availability and rate limits are controlled by each service. Vanguard cards can still be uploaded manually or added through an image URL.

Card names, images and game data belong to their respective owners. Inkra only provides a layout tool for personal proxy printing.

---

## Project structure

```
├── inkra.html              # The entire app (HTML + CSS + JS, self-contained)
├── index.html              # GitHub Pages entry point (redirects to inkra.html)
├── oricas_generator.html   # Legacy URL redirect (previous app name)
├── vendor/
│   └── jspdf.umd.min.js    # Local PDF engine
├── README.md
├── .gitattributes
├── .gitignore
└── .github/
    └── workflows/
        └── deploy.yml      # GitHub Actions — auto-deploy to GitHub Pages
```

---

## Development

There is no build step. Edit `inkra.html` and push — GitHub Actions deploys the repository root to GitHub Pages.

---

## License

MIT © 2026 — Free to use and modify.
