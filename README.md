# Spartacus Protection & Consulting — Redesign Demos

Modern, responsive redesign of [spartacusprocon.com](https://www.spartacusprocon.com/) as a
**standalone static site**. Three visual directions to demo, each a self-contained single page
built with plain HTML + CSS + a little vanilla JS — **no build step, no frameworks, no dependencies**.

## What's here

```
spartacus/
├─ index.html                     # Demo chooser — start here
├─ design-a-dark-metallic/        # A · Tactical premium dark + steel
│  └─ index.html
├─ design-b-modern-blue/          # B · Modernized Spartacus blue
│  └─ index.html
├─ design-c-light-pro/            # C · Light editorial (navy + gold, serif)
│  └─ index.html
├─ assets/                        # Shared brand images (logo, skyline, team photos)
│  ├─ logo.avif  skyline.avif  dino.avif  amy.avif
└─ README.md
```

All three share the same sections and copy (Hero → Our Story → Team → Services → Testimonials →
Contact/Footer), sticky nav with a mobile hamburger menu, fluid responsive layout, and on-scroll
reveals. Only the look & feel differs.

| | Direction | Fonts | Palette |
|---|---|---|---|
| **A** | Tactical premium | Oswald + Barlow | Charcoal / steel-silver |
| **B** | Confident, on-brand | Bricolage Grotesque + DM Sans | Spartacus blue / navy |
| **C** | Light editorial | Fraunces + Public Sans | Warm white / navy / gold |

## Preview locally

Open `index.html` in any browser, **or** (recommended, so the Google Fonts and relative asset
paths behave exactly like production) run a tiny local server from this folder:

```bash
# Python 3
python -m http.server 8080
# then visit http://localhost:8080
```

Resize the window (or use the browser device toolbar) to see the responsive behavior — the nav
collapses to a hamburger and grids stack to a single column on small screens.

## Hosting / Wix notes

This is portable static HTML, so you can host it anywhere (Netlify, Cloudflare Pages, GitHub Pages,
S3, etc.). To use the chosen direction on **Wix**:

- **Cleanest result:** rebuild the chosen design natively in the Wix Editor, using its page here as
  the exact visual spec (colors, fonts, spacing, copy are all defined in the one HTML file).
- **Embed option:** add a Wix **Embed → Embed HTML / Custom Element** block and point it at a hosted
  copy of the chosen `index.html`, or paste the markup. (Embedded HTML runs in an iframe, so it's
  best for sections rather than replacing the whole site chrome.)
- The Google Fonts are loaded via `<link>` and work as-is when hosted.

## Notes & follow-ups

- **Images** are `.avif` (small, modern, broadly supported). If you need to support older browsers,
  we can add `<picture>` + `.jpg` fallbacks.
- **Copy** is taken from the current site and lightly tightened for scannability — no new claims.
  Easy to adjust per section.
- **Services** shows the two current offerings (Risk Assessment, Security Consultation); the card
  grid is built to drop in more without layout changes.
- Social links (`#`) and legal pages are placeholders — point them at the real URLs when ready.
