# Root Mapping

**Root Mapping** is a product strategy framework that makes decision logic visible as a living source of truth. Paste a URL, describe your product, or dump your research or roadmap — and Claude generates an interactive visual map of the outcomes your product must produce, who they serve, and why they matter.

Works for products, practices, roles, and career clarity.

![Claude Skill](https://img.shields.io/badge/Claude_Skill-Ready-blue) ![License](https://img.shields.io/badge/License-CC_BY_4.0-green)

## What It Does

You give Claude any of these starting points:
- A product marketing page URL
- A feature list with no strategy behind it
- Research insights or interview notes
- A business mandate looking for customer grounding
- A LinkedIn profile or consulting website (for role/practice maps)

Claude generates an **interactive HTML Root Map** — a zoomable, clickable visualization showing:
- **Outcome hierarchy** — what must be true for customers, organized by enabling relationships
- **Needs** — the customer problems each outcome addresses, with severity indicators
- **Business outcomes** — why the company cares, with contextual icons
- **Solutions** — current implementations with effectiveness ratings
- **Confidence indicators** — how sure we are about each belief
- **Essential Value Scope (EVS)** — the irreducible core vs. nice-to-have
- **Key differentiators (★)** — where you win, not just where you must compete
- **Competitive landscape** — how each outcome stacks up against alternatives
- **Detail panels** — click any node for reasoning, sources, team beliefs, competitor tables, and editable notes

The map is a living conversation artifact. Review it, challenge it, update it — the conversation with Claude is the iteration engine.

## Quick Start

### Option A: Install as a Claude Skill (recommended)

1. Download `root-mapping.zip` from [Releases](../../releases)
2. In Claude → **Customize** → **Skills** → click **+**
3. Upload the zip file — done. The skill activates automatically in any conversation when relevant.

Requires a Claude account (free, Pro, Max, Team, or Enterprise) with [code execution enabled](https://support.claude.com/en/articles/12111783-create-and-edit-files-with-claude).

### Option B: Use as a Claude Project

1. Go to [claude.ai](https://claude.ai) → **Projects** → **New Project**
2. Upload these three files from the `root-mapping/` folder to Project Knowledge:

| File | What it does |
|------|-------------|
| `SKILL.md` | Framework instructions — teaches Claude how to think about outcomes, needs, EVS, competitive context, and how to populate the visual template |
| `templates/root-map-template.html` | Locked visual template — CSS, layout engine, rendering logic, detail panels. Claude replaces only the data section. |
| `examples/airpods-pro3-root-map.html` | Canonical example — a complete Root Map of AirPods Pro 3 showing all features: EVS/non-EVS, star differentiators, confidence levels, competitive tables, Phosphor icons on business outcomes |

### Then start a conversation

Try any of these:

> "Root map this: https://www.apple.com/vision-pro/"

> "I'm building a project management tool for freelancers. Here are my planned features: [list]. Root map this."

> "Here are 12 user interview insights from our discovery sprint. Turn these into a root map."

> "Map my consulting practice. Here's my website: [URL]"

Claude will generate an interactive HTML file you can download, open in any browser, and share with your team.

## What's in This Repo

```
root-mapping/
├── README.md                          ← You are here
├── LICENSE                            ← CC BY 4.0
├── root-mapping/                      ← The skill (also the zip for Releases)
│   ├── SKILL.md                       ← Framework skill file
│   ├── templates/
│   │   └── root-map-template.html     ← Locked visual template (v3 spec)
│   ├── examples/
│   │   └── airpods-pro3-root-map.html ← Product map example
│   └── references/
│       └── visual-spec-v3.md          ← Visual design reference
├── examples/
│   ├── peter-lewis-root-map.html      ← Personal/role map example
│   └── root-mapping-meta-root-map.html ← Meta map of the framework itself
└── docs/
    └── launch-kit.md                  ← Video script, testing plan, launch strategy
```

## Examples

### Product Map: AirPods Pro 3
6 categories, 18 features, full detail panels with competitive landscape, team beliefs, and sources. Demonstrates EVS vs. non-EVS, star differentiators, confidence indicators, and Phosphor icons on business outcomes. *(Included in the skill package.)*

### Personal/Role Map: Peter Lewis
Maps an individual's professional practice as outcomes to ensure. Shows how the same framework adapts for people — "your role is the outcome you're most directly responsible to ensure."

### Meta Map: Root Mapping
Root Map of the Root Mapping framework itself. Useful as both an example and a way to understand the framework's own value proposition.

## The Framework in 60 Seconds

**Nobody cares about your product.** They care what it enables them to do.

An **outcome** is the thing that will be true in customers' lives if the product succeeds. *"Now they can ____."*

The map organizes outcomes into a hierarchy of enabling relationships:
- **Root outcome** = the overall differentiated value proposition
- **Category outcomes** = major branches of value (2–6 is the sweet spot)
- **Feature outcomes** = specific problems solved within each branch

Everything else attaches to outcomes:
- **Needs** sit above (the problem)
- **Business outcomes** and **solutions** sit below (why the business cares, and how we currently deliver)

**EVS (Essential Value Scope)** = the irreducible core. Remove this outcome and customers won't want it.

**Star (★)** = where you distinctively win. Orthogonal to EVS — a node can be both, either, or neither.

## Based On

Root Mapping (formerly Outcome Laddering) was created by [Peter Lewis](https://medium.com/@thispeterlewis).

- [Original article: "Nobody cares about your product."](https://medium.com/@thispeterlewis/value-mapping-6203c997c463)
- [Companion: "Responsibility Without Territory"](https://medium.com/capitalonedesign/responsibility-without-territory-65501c807f80)
- [Video: IxDA talk on Root Mapping](https://www.youtube.com/watch?v=whw4XOn9cXc)

## License

CC BY 4.0 — use it, adapt it, share it. Attribution required.

## Contributing

Found a bug in the template? Have a great example map to share? Open an issue or PR. Framework feedback goes to [@thispeterlewis](https://medium.com/@thispeterlewis).
