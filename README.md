# DRILL PROTOCOL by SVGN Systems

**Real-time survival simulation that bleeds into real life.**

Terminal/HUD aesthetic. AI Vision photo validation. ARG scenarios that make you get up, move, and prove you're ready. The world's first survival training app that treats your real home as the game world.

**Live site:** [svgnsystems.com](https://svgnsystems.com)

---

## For Partners & Contributors

If you're new here, read the docs in this order:

| # | Document | What it answers |
|---|----------|-----------------|
| 1 | [docs/00_START_HERE.md](docs/00_START_HERE.md) | What is this project? What are we building? How does everything fit together? |
| 2 | [docs/01_CONTENT_BIBLE.md](docs/01_CONTENT_BIBLE.md) | Every screen, every line of text, every emotion the user feels. The complete user experience from first click to daily return. |
| 3 | [docs/02_BUILD_ORDER.md](docs/02_BUILD_ORDER.md) | What to build, in what order, with what tech. Concrete tasks for developers. |
| 4 | [docs/03_GLOBAL_VISION.md](docs/03_GLOBAL_VISION.md) | Where this goes long-term. Global strategy, revenue targets, 15 scenario types, B2B, localization. |

---

## Quick Start (Development)

```bash
npm install
npm run dev
```

Runs on `localhost:3000`. Deploys to GitHub Pages via `.github/workflows/deploy.yml`.

**Stack:** Vite + TypeScript + Tailwind CSS + Alpine.js (landing page), vanilla TS (app)

---

## Project Structure

```
SOVEREIGN-OS/
├── index.html              # Landing page (live at svgnsystems.com)
├── docs/
│   ├── 00_START_HERE.md    # Project overview for new contributors
│   ├── 01_CONTENT_BIBLE.md # Complete UX content (every screen, every word)
│   ├── 02_BUILD_ORDER.md   # Development tasks and priorities
│   └── 03_GLOBAL_VISION.md # Long-term strategy and roadmap
├── src/                    # App source (to be built)
│   ├── components/         # Terminal UI components
│   ├── screens/            # Quick Scan, Drills, Drill Hub
│   ├── services/           # Camera, AI Vision, Share, Storage
│   └── data/               # Scenario content (JSON)
├── public/                 # Static assets, legal pages
└── marketing/              # Brand docs, ad templates
```
