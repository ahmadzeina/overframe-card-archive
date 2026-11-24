# AHMAD ZEINA — Overframe Card Archive

An interactive 3D card rack and digital archive showcasing Yu-Gi-Oh! Overframe cards, their original counterparts, and full-bleed artwork wallpapers.

## Features

- **3D Perspective Card Rack:** Smooth inertial scrolling, drag gestures, wheel navigation, arrow controls, and an interactive timeline scrubber across 12 Overframe releases.
- **Dynamic Frame Accenting:** Automatically adapts UI accents, borders, and typography to each card's frame type (Normal, Effect, Ritual, Fusion, Spell).
- **Detail & Comparison Sheet:** Opens with a `clip-path` transition revealing full card stats, OCG release dates, effect text, custom wallpaper backdrop, and a delayed reveal of the original/retrained card.
- **Duelist Profile ("About Me"):** Dedicated slide-over profile sheet with custom wallpaper and responsive grid layout.

## Project Structure

```text
├── index.html               # Single-file HTML, CSS, and interactive 3D rack logic
├── overframe-cards/         # Overframe card artworks (.webp, .png, .jpg)
├── overframe-originals/     # Original & classic reference card artworks
└── overframe-wallpapers/    # Full-screen detail & profile backdrop wallpapers
```

## Local Setup

Because the archive loads local relative assets (`./overframe-cards/`, `./overframe-originals/`, `./overframe-wallpapers/`), serve the root directory with any static local server:

```bash
# Using Python
python -m http.server 8000

# Or using Node.js (npx)
npx serve .
```

Then open `http://localhost:8000` in your browser.

## Deployment

This project is a zero-build static site and deploys directly to **Vercel** or **GitHub Pages** from the `main` branch with the root directory set to `./`.

> **Note on Case-Sensitive Hosting:** Linux-based hosts (including Vercel) treat file paths as case-sensitive. Ensure all image filenames match the exact casing referenced in `SEED` inside `index.html` (for example, `ra.jpg` vs. `RA.jpg`).

## Credits & Disclaimer

- **Curated & Built by:** [Ahmad Zeina](https://github.com/ahmadzeina) ([LinkedIn](https://www.linkedin.com/in/ahmadzeina821))
- **Artwork Copyright:** ©スタジオ・ダイス／集英社・テレビ東京・KONAMI. All rights reserved. This is a non-commercial fan archive.