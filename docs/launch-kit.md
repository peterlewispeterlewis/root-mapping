# Root Mapping — Launch Kit

## 1. Video Talking Points (2–3 min overview)

**Hook (15 sec)**
- "Nobody cares about your product. They care what it enables them to do. And most product teams can't articulate that clearly."
- "I built a tool that fixes this in 5 minutes — using Claude."

**The Problem (30 sec)**
- Product teams argue about features, not outcomes
- Strategy docs go stale in weeks — nobody refers back to them
- PMs, designers, and engineers each have a different mental model of what matters
- Existing frameworks (JTBD, OKRs, Lean Canvas) don't give you a living visual artifact you can point at and debate

**The Demo (60–90 sec)**
- Show a Claude Project conversation — paste a URL (e.g., apple.com/airpods-pro)
- Claude asks a few clarifying questions, then generates an interactive HTML map
- Open the map in a browser — zoom, click nodes, show the detail panel
- Point out: outcomes (blue), needs (coral above), business outcomes (amber below with icons), solutions (green below)
- Click a node — show the confidence reasoning, competitive landscape table, team belief, editable notes
- Point out EVS (solid borders) vs. non-EVS (dashed), star differentiators (★)
- "Every node is a debatable belief about your product. The map makes those beliefs visible so your team can challenge them."

**How To Get It (15 sec)**
- "It's a free Claude Skill. One file, one click install."
- Show: Customize → Skills → + → select root-mapping.skill → done
- "It also works as a Claude Project if you prefer that. Both options on GitHub."
- "Link in the description."

**Close (15 sec)**
- "This works for products, consulting practices, role clarity, career planning — anything where you need to articulate what value you're producing."
- "It's based on a framework I've been developing for years called Root Mapping. The articles and talk are linked in the repo."

**Production notes:**
- Screen-record the Claude conversation and the resulting map side by side
- Use the AirPods Pro 3 map as the demo — it's visually rich and everyone knows the product
- Keep it under 3 minutes. People will stop watching at 3.
- Thumbnail: screenshot of the map zoomed to show a few nodes with the detail panel open


## 2. Testing Plan

### What to test before launch

**Functional (do these yourself, ~30 min)**
- [ ] Skill install: download .skill file → Customize → Skills → + → install. Does it appear in skills list?
- [ ] Fresh conversation (not in a project): say "root map this: [product URL]" → does the skill trigger and generate a valid map?
- [ ] Project install: upload 3 files to a new Claude Project → start conversation → does it generate a valid map?
- [ ] Open the generated HTML in Chrome, Safari, Firefox, Edge — does it render correctly?
- [ ] Open on mobile (just to check — it's desktop-optimized but shouldn't break)
- [ ] Click every node type: root, EVS category, non-EVS category, star node, feature → detail panels work?
- [ ] Zoom in/out (scroll + buttons), pan, reset view (⟲ button)
- [ ] Dark mode: does the map respect system dark mode?
- [ ] Try a role/personal map prompt: "Map my consulting practice based on this LinkedIn: [URL]"
- [ ] Try a vague prompt: "I'm building a task manager" — does Claude ask good questions and generate placeholders?

**Quality (do these with 2–3 trusted people, ~1 hr each)**
- [ ] Give someone the .skill file and a one-line instruction ("install this, then say 'root map this: [URL]'"). Can they get a map without asking you questions?
- [ ] Give someone a generated map. Can they understand it without explanation? What confuses them?
- [ ] Ask someone to bring their own product/practice and try mapping it. Where does Claude struggle?

**Edge cases (quick checks)**
- [ ] Very simple product (1–2 features) — does the map still look reasonable?
- [ ] Very complex product (enterprise SaaS with 20+ features) — does Claude scope it sensibly or does it explode?
- [ ] Non-English product page — does Claude handle it?
- [ ] No URL, just a vague description — does Claude guide the conversation well?

### What NOT to test (save your energy)
- Pixel-perfect rendering across obscure browsers
- Performance with 50+ nodes (outside intended use)
- Mobile-first layout (this is a desktop strategy tool)
- Automated testing infrastructure (premature for launch)

### Success criteria for launch
- 3/3 trusted testers can install the skill and generate a map with no guidance beyond "install this, say root map [URL]"
- Generated maps are legible and structurally correct for 3+ different product types
- No broken rendering in Chrome + Safari (80%+ of users)
- Skill triggers reliably on "root map this" and similar phrases


## 3. Launch Strategy

### Phase 1: Soft launch (Week 1)
**Goal:** Get 20–30 real users, surface critical issues, collect 3–5 testimonial quotes.

**Actions:**
- Publish GitHub repo (public)
- Post on LinkedIn (see copy below) — tag 5–10 people who'd find it useful
- Share in 2–3 Slack/Discord communities where you're already known (design, product, strategy communities)
- Send a personal DM to 5–10 people: "I made a thing — would love your feedback"
- Ask testers to share their generated maps (screenshots or files) — these become social proof

### Phase 2: Content launch (Week 2–3)
**Goal:** Drive organic discovery. Target: 100+ GitHub stars, 50+ real users.

**Actions:**
- Publish a short LinkedIn article: "I taught Claude my product strategy framework — here's what happened" (story format, include screenshots, link to repo)
- Record and post the 2–3 min overview video (LinkedIn native + YouTube)
- Submit to relevant newsletters / aggregators:
  - Product Hunt (as a "free tool" not a SaaS launch — low-key positioning)
  - Lenny's Newsletter community / Slack
  - Reforge community
  - Mind the Product Slack
  - Designer News / Hacker News (if the framing is right — lead with the framework, not the tool)
  - JTBD / strategy-focused communities
- Cross-post to X/Twitter with a thread format: "Nobody cares about your product → here's a framework → here's a free Claude tool → [link]"

### Phase 3: Sustained growth (Month 2+)
**Goal:** Organic word-of-mouth. Let the tool sell itself.

**Actions:**
- Collect and showcase example maps from real users (with permission)
- Write 1–2 "how I root mapped [well-known product]" case study posts (Tesla, Notion, Figma, etc.)
- Consider a "Root Map challenge" — invite people to map their product and share results
- Update the repo with community-contributed examples
- Respond to every GitHub issue and discussion — early community building matters disproportionately

### Where to promote (ranked by expected ROI)

| Channel | Why | Format |
|---------|-----|--------|
| **Claude Skills / Browse Plugins** | Native distribution. Users discover and install in one click. Zero friction. Investigate whether submissions are open or curated. | .skill file + description |
| **LinkedIn** | Your audience is here. Product/design/strategy professionals. | Post + article + video |
| **GitHub** | Discovery hub. Stars = social proof. README is your landing page. | Repo + good README + .skill in Releases |
| **X/Twitter** | Reach beyond your network. Thread format works well for frameworks. | Thread + screenshots |
| **Product communities** (Lenny's, Reforge, MTP) | High-intent product people who immediately get the value. | Community post, not promo |
| **YouTube** | Long-tail discovery. "Product strategy framework" is a searchable topic. | 2–3 min video |
| **Product Hunt** | Spike of attention. Good for GitHub stars. Time it for a weekday. | Launch page |
| **Hacker News** | High risk, high reward. Lead with "Show HN" and the framework thinking, not the Claude integration. | Show HN post |
| **Medium** | You already have an audience here from the original articles. | Update or new article linking to repo |


## 4. Marketing Copy

### GitHub repo description (one-liner)
> Product strategy framework for Claude. Install as a Skill or Project → paste a URL or describe your product → get an interactive visual map of outcomes, needs, competitive context, and what to build first. Free, CC BY 4.0.

### GitHub topics/tags
`product-strategy` `product-management` `claude` `claude-skill` `ai-tools` `product-design` `jtbd` `outcome-mapping` `strategy-framework` `design-strategy`

### LinkedIn post (launch)

Nobody cares about your product.

They care what it enables them to do. And most product teams can't clearly articulate that — which is why they spend months arguing about features instead of aligning on outcomes.

I've been developing a framework called Root Mapping (formerly Outcome Laddering) for years. The core idea: map the outcomes your product must produce — for customers and the business — as a visual hierarchy of enabling relationships. Make the decision logic visible so the team can debate it instead of guessing.

I finally turned it into something anyone can use in under a minute.

It's a free Claude Skill. Install one file, and every conversation with Claude can generate interactive visual strategy maps with:
→ Outcome hierarchy (what must be true for customers)
→ Needs and severity (the problems you're solving)
→ Business outcomes (why the company cares)
→ Solutions with effectiveness ratings
→ Competitive landscape per outcome
→ Confidence indicators (how sure are we about each belief?)
→ EVS — the irreducible core vs. nice-to-have
→ Clickable detail panels with reasoning, sources, and editable notes

It works for products, consulting practices, role clarity, and career planning.

Everything's on GitHub: [LINK]

The framework articles and talk that started this:
→ "Nobody cares about your product.": [LINK]
→ "Responsibility Without Territory": [LINK]
→ IxDA talk: [LINK]

CC BY 4.0 — use it, adapt it, share it.

### LinkedIn article title options (pick one)
- "I Taught Claude My Product Strategy Framework — Here's What Happened"
- "How to Map Any Product's Decision Logic in 5 Minutes with Claude"
- "Nobody Cares About Your Product: A Free Strategy Tool for Claude"

### X/Twitter thread (condensed)

**1/** Nobody cares about your product. They care what it enables them to do.

Most product teams can't articulate that clearly. So they argue about features instead of outcomes.

I built a free tool that fixes this. 🧵

**2/** Root Mapping: paste a product URL into Claude, get an interactive visual map of:
- What must be true for customers (outcomes)
- Why the business cares (biz outcomes)
- What's essential vs. nice-to-have (EVS)
- Where you win (★ differentiators)
- How confident you are about each belief

**3/** [Screenshot of AirPods Pro 3 map — zoomed to show 2–3 categories with detail panel open]

Every node is a debatable belief about your product. The map makes those beliefs visible so your team can challenge them.

**4/** It works for products, consulting practices, role clarity, career planning — anything where you need to articulate what value you're producing.

Free Claude Skill on GitHub — one file, one click install: [LINK]

CC BY 4.0.

**5/** Based on Root Mapping (formerly Outcome Laddering) — a framework I've been developing for years.

The original articles:
→ "Nobody cares about your product.": [LINK]
→ "Responsibility Without Territory": [LINK]

### Product Hunt tagline options
- "Turn any product URL into a visual strategy map — using Claude"
- "Make your product's decision logic visible and debatable"
- "Free Claude Project kit for product strategy visualization"

### Short description (for directories, newsletters, etc.)
> Root Mapping is a free Claude Skill that turns product descriptions, URLs, or research into interactive visual strategy maps. Install one file and every Claude conversation can generate outcome hierarchies with confidence indicators, competitive context, and essential-vs-nice-to-have scoping. Based on Peter Lewis's Root Mapping framework (formerly Outcome Laddering). CC BY 4.0.
