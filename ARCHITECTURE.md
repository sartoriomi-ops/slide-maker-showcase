# Architecture — Slide Maker v2

## High-level flow

```
User input (topic + brand + palette + style)
        │
        ▼
┌─────────────────────┐
│  Brand Config Layer  │  ← selects palette, mascot, fonts, style rules
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Web Search Module   │  ← optional topic research via search API
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Prompt Builder      │  ← assembles system + user prompt per slide
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Claude Haiku API    │  ← parallel calls (one per slide)
│  (parallel calls)    │
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Render Engine       │  ← HTML/CSS slide generation in-browser
└─────────┬───────────┘
          │
          ▼
┌─────────────────────┐
│  Export Module        │  ← download as images + optional NotebookLM prompt
└─────────────────────┘
```

## Key design decisions

**Single-file architecture.** The entire app lives in one HTML file. This eliminates build steps, keeps Vercel deploys instant, and makes the codebase easy to debug. The tradeoff is a large file, but for a tool used by one person across three brands, simplicity wins over modularity.

**Parallel API calls.** Each carousel slide is generated independently via its own Claude Haiku call. This cuts total generation time from sequential (N × latency) to roughly 1 × latency for the full set.

**Brand config as data.** Each brand's palettes, fonts, mascot references, and style rules are stored as plain objects. Adding a new brand means adding one config block — no code changes to the generation pipeline.

**No backend.** API calls go directly from the browser to Claude's API. This is acceptable because the tool is personal-use only and the API key is scoped to a low-cost Haiku model.

## Combination matrix

3 brands × 7 palettes × 5 styles = **105 unique visual combinations**, tested across 4 slide counts = **420 total test cases**.
