<div align="center">

# 🎨 Slide Maker v2

**Multi-brand Instagram carousel and post generator. Single HTML file deployed to Vercel.**

![Status](https://img.shields.io/badge/Status-Shipped-brightgreen?style=for-the-badge)
![Tests](https://img.shields.io/badge/Combo%20Tests-476%20Passed-blue?style=for-the-badge)
![Lines](https://img.shields.io/badge/Codebase-3080%20Lines-lightgrey?style=for-the-badge)

![Claude API](https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=claude&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000?style=flat-square&logo=vercel&logoColor=white)
![HTML/CSS/JS](https://img.shields.io/badge/HTML%2FCSS%2FJS-E34F26?style=flat-square&logo=html5&logoColor=white)

</div>

---

## 💡 What it does

Slide Maker generates ready-to-post Instagram carousels and single posts for three content brands from a single interface. Pick a brand, choose a palette and style, enter a topic, and get polished slides back. No design tool needed.

---

## ✨ Features

| Feature | Details |
|---|---|
| **Multi-brand** | 3 brands: ElleMentys, GuiaOlim, SoftStack |
| **Visual variety** | 7 palettes per brand (21 total) + custom hex palette, 5 style variants (A-E), 6 decoration kits |
| **Slide types** | Cover, Content, Recap, CTA |
| **Carousel mode** | 3 to 12 slides per carousel |
| **Single post mode** | 4 styles: bold, split, minimal, stat |
| **Mascot system** | None, small, or large per-brand character integration |
| **Caption panel** | Auto-generates Instagram caption + 30 hashtags + Twitter/X thread after carousel generation |
| **NotebookLM output** | Generates podcast scripts and video content prompts from carousel content |
| **Web search** | Topic research via Anthropic web search API before slide generation |
| **Export formats** | 1:1, 4:5, 9:16 (Stories), LinkedIn 1.91:1 |
| **Auto-save** | localStorage draft restore on next session |
| **Parallel API calls** | One Claude Haiku call per slide for speed |

---

## 🏗️ Stack

| Layer | Tech |
|---|---|
| Frontend | Vanilla HTML / CSS / JS (single file) |
| AI | Claude API (parallel Haiku calls + Sonnet for content) |
| Search | Anthropic web search API |
| Hosting | Vercel |

---

## 🧪 Test coverage

3 brands x 7 palettes x 5 styles = **105 unique visual combinations**, tested across 4 slide counts + single post modes = **476 total test cases passed**.

Zero undefined, zero NaN, zero JS throws.

---

## 💡 Why I built it

Designing carousels manually took hours per post across three content brands. Slide Maker reduced that to under 2 minutes. The single-file architecture keeps deployment simple: one push to Vercel, done.

---

## 🚀 Coming in v3

Slide Maker is being upgraded to a full visual content studio. Planned features:

| Area | What's changing |
|---|---|
| **Search engine** | Multi-angle web research (stats, pain points, news, expert takes) replaces single search |
| **Content framework** | AIDA structure built into the prompt engine so each slide serves a different purpose |
| **Layout styles** | Expanding from 5 to 8 distinct styles per brand |
| **Visual editor** | Drag-drop image placement, inline text editing, resize/rotate controls |
| **Sticker library** | 100+ brand-themed SVG stickers and doodles |
| **New modes** | URL-to-carousel, paste-text-to-carousel, PDF and video export |
| **UI overhaul** | Redesigned interface with panel layout and filmstrip navigation |

> v3 is in active planning. Build sessions start soon.

---

## 📐 Architecture

See [ARCHITECTURE.md](./ARCHITECTURE.md) for the high-level data flow and key design decisions.

---

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-michellesartorio.com-58A6FF?style=flat-square&logo=googlechrome&logoColor=white)](https://michellesartorio.com)

</div>
