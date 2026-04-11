# Slide Maker v2

**Multi-brand Instagram carousel and post generator — single HTML file deployed to Vercel.**

---

## What it does

Slide Maker generates ready-to-post Instagram carousels and single posts for three content brands from a single interface. You pick a brand, choose a palette and style, enter a topic, and get polished slides back — no design tool needed.

## Features

- **3 brands supported:** ElleMentys, GuiaOlim, SoftStack
- **7 color palettes per brand** (21 total)
- **5 style variants** per palette
- **Mascot system** with per-brand character integration
- **NotebookLM prompt output** for repurposing content into podcast scripts
- **Web search integration** for topic research before generation
- **Parallel Claude Haiku calls** for speed

## Stack

| Layer | Tech |
|---|---|
| Frontend | Vanilla HTML / CSS / JS (single file) |
| AI | Claude Haiku API (parallel calls) |
| Hosting | Vercel |

## Status

✅ **Shipped** — 420 combination tests passed across all brand × palette × style variants.

## Why I built it

I run three content brands and was spending hours in Canva designing carousels manually. Slide Maker reduced that to under 2 minutes per post. The single-file architecture keeps deployment simple — one push to Vercel, done.

## Architecture

See [ARCHITECTURE.md](./ARCHITECTURE.md) for the high-level data flow.
