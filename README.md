# Root Mapping

**Root Mapping** is a product strategy framework that makes decision logic visible as a living source of truth. Paste a URL, describe your product, or dump your research or roadmap — and Claude generates an interactive visual map of the outcomes your product must produce, who they serve, and why they matter.

Works for products, practices, roles, and career clarity.

![Root Map example](https://img.shields.io/badge/Claude_Project-Ready-blue) ![License](https://img.shields.io/badge/License-CC_BY_4.0-green)

## What It Does

You give Claude any of these starting points:
- A product marketing page URL
- A feature list with no strategy behind it
- Research insights or interview notes
- A business mandate looking for customer grounding
- A LinkedIn profile or consulting website (for role/practice maps)

Claude generates an **interactive HTML Root Map** — a zoomable, clickable, editable visualization showing:
- **Outcome hierarchy** — what must be true for customers, organized by enabling relationships
- **Needs** — the customer problems each outcome addresses, with strength indicators
- **Business outcomes** — why the company cares
- **Solutions** — current implementations with effectiveness ratings
- **Confidence indicators** — how sure we are about each belief
- **Essential Value Scope (EVS)** — the irreducible core vs. nice-to-have
- **Key differentiators (★)** — where you win, not just where you must compete
- **Competitive landscape** — how each outcome stacks up against alternatives
- **Detail panels** — click any node for reasoning, sources, team beliefs, competitor tables, and editable notes

### Built for Working Sessions

Every generated Root Map is a living, editable artifact. Open it in any browser and start facilitating — no specialized knowledge required.

- **Inline editing** — click any node to edit outcomes, needs, business outcomes, and solutions in the detail panel
- **Clickable indicators** — change confidence, need strength, and effectiveness by clicking dots
- **EVS toggle** — flip EVS on/off with automatic parent cascade
- **Star (★) differentiators** — mark where you distinctively win, separate from EVS (must-have)
- **Outcome & business indicators** — proposed metrics for how you'd measure each outcome
- **Add/remove nodes** — hover any node for a + button; add branches, features, or sub-features
- **Drag to reposition** — rearrange nodes on the canvas
- **Undo/redo** — full history with ⌘Z / ⌘⇧Z
- **Auto-save** — edits persist in browser storage; restore prompt on reload
- **Save snapshot** — download a self-contained HTML file with all edits baked in and a changelog comment
- **Change log** — tracks every edit with before/after and timestamps
- **Animated connectors** — subtle flow pulses on connector lines showing outcome relationships
- **Dark mode** — automatic via `prefers-color-scheme`
- **Keyboard & accessibility** — Tab through nodes, Enter to open, Escape to close; respects reduced motion preferences

## Quick Start

### Use as a Claude Project
1. Go to [claude.ai](https://claude.ai) → **Projects** → **New Project**
2. Upload these files from this repo to Project Knowledge:

| File | What it does |
|------|-------------|
| `SKILL.md` | Framework instructions — teaches Claude how to think about outcomes, needs, EVS, competitive context, and how to populate the visual template |
| `root-map-template-v4.html` | Visual template v4 — CSS, layout engine, rendering, detail panels, interactive add/remove for business outcomes and solutions, star (★) badges, outcome/business indicators, sub-feature support. Claude replaces only the data section. |
| `airpods-pro3-root-map.html` | Canonical example — a complete Root Map of AirPods Pro 3 showing all features |
| `spotify-root-map.html` | Canonical example — Spotify product map with star differentiators, EVS/non-EVS, competitive landscape, and v4 features |

### Then start a conversation
Try any of these:

> "Root map this: https://www.apple.com/vision-pro/"

> "I'm building a project management tool for freelancers. Here are my planned features: [list]. Root map this."

> "Here are 12 user interview insights from our discovery sprint. Turn these into a root map."

> "Map my consulting practice. Here's my website: [URL]"

Claude will generate an interactive HTML file you can download, open in any browser, edit live, and share with your team.

## The Framework in 60 Seconds

**Nobody cares about your product.** They care what it enables them to do.

An **outcome** is the thing that will be true in customers' lives if the product succeeds. *"Now they can ____."*

Outcomes must be **solution-agnostic** — if the implementation changed completely, the outcome statement should still be true. "Always know where things stand" not "Track progress with real-time dashboard."

The map organizes outcomes into a hierarchy of enabling relationships:
- **Root outcome** = the overall differentiated value proposition
- **Category outcomes** = major branches of value (2–6 is the sweet spot)
- **Feature outcomes** = specific problems solved within each branch

Everything else attaches to outcomes:
- **Needs** sit above (the problem)
- **Business outcomes** and **solutions** sit below (why the business cares, and how we currently deliver)

**EVS (Essential Value Scope)** = the irreducible core. Remove this outcome and customers won't want it.

**Star (★)** = where you distinctively win. Orthogonal to EVS — a node can be both, either, or neither.

## Examples

### Product Map: AirPods Pro 3
6 categories, 18 features, full detail panels with competitive landscape, team beliefs, and sources. Demonstrates EVS vs. non-EVS, star differentiators, confidence indicators, and competitive position tags with icons.

### Personal/Role Map: Peter Lewis
Maps an individual's professional practice as outcomes to ensure. Shows how the same framework adapts for people — "your role is the outcome you're most directly responsible to ensure."

### Product Map: Spotify
4 categories (discovery, access, library, social), 10 features, with star differentiators on algorithmic discovery and Spotify Connect. Demonstrates EVS vs. non-EVS branches, confidence variation, and v4 template features including indicators and interactive add/remove.

### Meta Map: Root Mapping
Root Map of the Root Mapping framework itself. Useful as both an example and a way to understand the framework's own value proposition.

## Based On

Root Mapping (formerly Outcome Laddering) was created by [Peter Lewis](https://peterlewis.design).

- [Original article: "Nobody cares about your product."](https://medium.com/@thispeterlewis/value-mapping-6203c997c463)
- [Companion: "Responsibility Without Territory"](https://medium.com/capitalonedesign/responsibility-without-territory-65501c807f80)
- [Video: IxDA talk on Root Mapping](https://www.youtube.com/watch?v=whw4XOn9cXc)

## License

CC BY-SA 4.0 — use it, adapt it, share it. Attribution required. Share-alike for derivatives.

## Contributing

Found a bug in the template? Have a great example map to share? Open an issue or PR. Framework feedback goes to [@thispeterlewis](https://medium.com/@thispeterlewis).
