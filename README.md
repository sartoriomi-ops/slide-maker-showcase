<div align="center">

# 🎨 Slide Maker v2

**Multi-brand Instagram carousel and post generator. Single HTML file deployed to Vercel.**

![Status](https://img.shields.io/badge/Status-Shipped-brightgreen?style=for-the-badge)
![Tests](https://img.shields.io/badge/Combo%20Tests-420%20Passed-blue?style=for-the-badge)

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
| **Multi-brand support** | 3 brands supported: ElleMentys, GuiaOlim, SoftStack |
| **Visual variety** | 7 color palettes per brand (21 total), 5 style variants per palette |
| **Mascot system** | Per-brand character integration on slides |
| **NotebookLM output** | Repurpose content into podcast scripts |
| **Web search** | Optional topic research before generation |
| **Parallel API calls** | One call per slide for speed |

---

## 🏗️ Stack

| Layer | Tech |
|---|---|
| Frontend | Vanilla HTML / CSS / JS (single file) |
| AI | Claude API (parallel calls) |
| Hosting | Vercel |

---

## 🧪 Test coverage

3 brands x 7 palettes x 5 styles = **105 unique visual combinations**, tested across 4 slide counts = **420 total test cases passed**.

---

## 💡 Why I built it

Designing carousels manually in Canva took too long when running multiple content brands. Slide Maker reduced that to under 2 minutes per post. The single-file architecture keeps deployment simple: one push to Vercel, done.

---

## 📐 Architecture

See [ARCHITECTURE.md](./ARCHITECTURE.md) for the high-level data flow.

---

<div align="center">

[![Portfolio](https://img.shields.io/badge/Portfolio-michellesartorio.com-58A6FF?style=flat-square&logo=googlechrome&logoColor=white)](https://michellesartorio.com)

</div>
