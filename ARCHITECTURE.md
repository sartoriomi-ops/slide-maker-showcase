<div align="center">

# 📐 Architecture: Slide Maker v2

</div>

---

## High-level flow

```
User input (topic + brand + palette + style)
       │
       ▼
┌─────────────────┐
│ Brand Config    │  ← selects palette, mascot, fonts, style rules
│ Layer           │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Web Search      │  ← optional topic research via Anthropic search API
│ Module          │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Prompt Builder  │  ← assembles system + user prompt per slide
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Claude API      │  ← parallel calls (one per slide)
│                 │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Render Engine   │  ← HTML/CSS slide generation in-browser
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ Export Module   │  ← download as images + optional NotebookLM prompt
└─────────────────┘
```

---

## Key design decisions

**Single-file architecture.** The entire app lives in one HTML file (3080 lines). This eliminates build steps, keeps Vercel deploys instant, and makes the codebase easy to debug. For a tool used by one person across three brands, simplicity wins over modularity.

**Parallel API calls.** Each carousel slide is generated independently via its own API call. This cuts total generation time from sequential (N x latency) to roughly 1x latency for the full set.

**Brand config as data.** Each brand's palettes, fonts, mascot references, and style rules are stored as plain objects. Adding a new brand means adding one config block. No code changes to the generation pipeline.

**Decoration kits.** Six visual kits control the background textures, corner elements, doodles, and overlays per slide. Each brand maps to specific kits. ElleMentys and GuiaOlim have custom kits. SoftStack uses the shared kits.

**Dual-model routing.** Content generation (carousels, single posts) uses a capable model with web search enabled. Fast tasks (captions, hashtags, NotebookLM prompts) use a lighter model with parallel execution for speed.

**Client-side processing.** The tool runs entirely in the browser. No backend server required.

---

## Combination matrix

3 brands x 7 palettes x 5 styles = **105 unique visual combinations**, tested across 4 slide counts + single post modes = **476 total test cases**.

---

<div align="center">

*Back to [README](./README.md)*

</div>
