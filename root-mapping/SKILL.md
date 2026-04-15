---
name: root-mapping
description: Product strategy framework for clarifying what to build and why. Use when helping with product definition, feature prioritization, roadmap alignment, team alignment on strategy, translating insights into product decisions, identifying essential vs. nice-to-have features, diagnosing why a product effort feels unfocused, competitive analysis, value proposition design, jobs to be done mapping, product-market fit analysis, strategic differentiation, or building a compelling product story. Also useful for personal and role maps — mapping a consulting practice, personal brand strategy, role clarity, career focus, or defining responsibilities as outcomes to ensure. Trigger on phrases like "what should we build", "why does this feature exist", "how do we prioritize", "what's our differentiation", "map my practice", or "clarify my role." Based on Peter Lewis's Root Mapping framework (formerly Outcome Laddering).
license: CC BY 4.0 — Attribution required. Based on Root Mapping by Peter Lewis (https://medium.com/@thispeterlewis/value-mapping-6203c997c463)
---

# Nobody Cares About Your Product

Root Mapping helps teams make better product decisions by making decision logic visible. It creates a shared, evolving snapshot of the outcomes a product must produce — for customers and the business — visualized as a hierarchy of enabling relationships.

## Attribution

Based on the Root Mapping framework (formerly Outcome Laddering / Value Mapping) by Peter Lewis.
- Original article: ["Nobody cares about your product."](https://medium.com/@thispeterlewis/value-mapping-6203c997c463)
- Companion article on role definition: https://medium.com/capitalonedesign/responsibility-without-territory-65501c807f80
- Video presentation: https://www.youtube.com/watch?v=whw4XOn9cXc

## Core Principle

**Nobody cares about your product.** They care what it enables them to do. A product is a mediator of a value exchange: customers get outcomes that improve their lives; the business gets outcomes that improve its competitive position. The solution (product/feature) is just the current best way to make those outcomes happen.

An outcome is **the thing that will be true** in customers' lives if the product succeeds. "Now they can ____."

This reframing isn't just conceptual — it changes team dynamics. When people define their stake as activities, outputs, or territory ("I own visual design on iOS"), they defend turf. When they define it as outcomes ("I'm responsible for ensuring every detail is beautiful, consistent, and intuitive"), they lower their guard. The conversation shifts from "do I like it?" and "is this mine?" to "is this effective at producing the outcome we agreed to?" Fear — of losing ownership, of being replaced, of someone stepping into "your" area — is what kills most team alignment. Outcome orientation is the antidote. (See Peter Lewis's companion article, "Responsibility Without Territory.")

## How Root Mapping Works

### Experience Outcomes Are the Backbone

The map's primary nodes are **experience outcomes** — always the same color (blue) regardless of scope. Everything else attaches to them:

- **Experience outcomes** = the connected nodes. Root, category, feature — all blue, all outcomes.
- **Inferred needs** = the customer problem each outcome addresses. Attached above the outcome.
- **Business outcomes** = what's now true for the business if this customer outcome is achieved. Attached below relevant outcomes. Business outcomes are **results**, not solutions or features: talent maturity, customer retention, direct revenue, new market access, reduced support costs, brand authority, data asset growth, regulatory compliance. NOT "AI-powered dashboard" (that's a solution), NOT "users can track metrics" (that's a customer outcome), NOT "improve engagement" (too vague — what business result does engagement produce?).
- **Solutions** = how we currently propose to produce each outcome. Attached below. Only attach solutions where a concrete one exists.
- **Metadata** = confidence, evidence, competitive position, tech requirements, effectiveness ratings.

**The root outcome** (top) is always the **overall differentiated value proposition.**

### Hierarchy (Levels of Zoom)

1. Inferred need + Root outcome + Business outcomes (product level)
2. Feature category outcomes (major branches)
3. Feature-level outcomes (specific problems solved)
4. Sub-feature outcomes (deeper detail if needed)

The hierarchy supports **n levels** depending on product complexity. A large digital platform might have many layers of parent/child branches. The current template renders three tiers (root, category, feature); deeper hierarchies can be modeled by nesting categories or expanding the template's `RY` array.

Arrows connect **node groups to node groups**, flowing upward. Each outcome enables the one above it. Everything else (needs, biz outcomes, solutions) attaches directly to its outcome node as subordinate cards in a group — NOT connected by arrows.

**Conceptual altitude matters.** Every node must be at the tier that matches its strategic scope:
- A broad value proposition branch → category tier (row 2)
- A specific capability addressing a discrete need → feature tier (row 3)
- A sub-component or control → sub-feature tier (row 4, if used)

### Indicators on Nodes

Three distinct indicators, each answering a different question:

1. **Outcome confidence** (dot, top-right of blue outcome card): "Is this the right problem to solve? Is this the right value to offer?" High/medium/low.
2. **Need severity** (3-dot row, top of need card above description text): "How painful is this for customers?" Severe/moderate/minor.
3. **Solution effectiveness** (dot, top-right of green solution card): "How well does this solution produce the outcome?" Strong/adequate/unproven.

### Essential Value Scope (EVS)

EVS = the irreducible core. If you address fewer outcomes, customers won't want it and you can't compete.

- EVS outcomes get solid borders and solid connecting lines
- Non-EVS outcomes get dashed borders and dashed lines
- Test: remove an outcome — does the root still work? If yes, it's non-EVS.

### Key Differentiator (★ Star)

Star marks outcomes where you **win**, distinct from EVS which marks outcomes you **must have**. They're orthogonal — a node can be both EVS and starred, either one alone, or neither.

- EVS = "without this, you can't compete" (table stakes to be viable)
- Star = "this is where you're distinctively better than alternatives" (reason to choose you)

A table-stakes outcome that most competitors actually fail to deliver can be both EVS and starred. A non-EVS outcome that's a genuine differentiator (e.g., thought leadership, culture) gets starred but not EVS.

Star nodes display a gold `★` badge next to the outcome label and show "★ key differentiator" in the detail panel tag line. Add `star: true` to the node data object.

### Competitive Context

Tag each outcome with its competitive position:
- **Differentiated** — we do this significantly better
- **Table stakes** — everyone does this; we must too
- **Battleground** — active competition, unclear winner
- **Uncontested** — nobody else does this
- **Behind** — competitors do this better

## Scope & Complexity Guidance

Not every product needs the same level of detail. Use these guidelines to keep maps useful rather than exhausting.

**Category count (branches off root):** 2–6 is the sweet spot. The Waze example in Peter's article has 2 main branches ("fight traffic" and "do it together") — simple and clear. A complex platform might have 5–6. More than 7–8 categories usually means either some categories should merge, or you're mapping at too fine a grain and need to zoom out. If a product genuinely has 8+ distinct outcome areas, consider splitting into multiple maps (e.g., one per major product surface or user segment).

**Features per category:** 2–5 features per category keeps each branch readable. A single feature under a category suggests the category might not be a real branch — it might be a feature that's been over-promoted to category altitude. More than 6 features in one branch suggests some should cluster into sub-categories or that the category is too broad.

**When to add depth (sub-features):** Only when a feature outcome itself breaks down into meaningfully distinct sub-problems. If you're listing UI controls or implementation details, you've gone too deep — those belong in a design spec, not a strategy map.

**When to split into multiple maps:** When the product serves fundamentally different user types with different root outcomes (e.g., a marketplace's buyer map vs. seller map), or when a platform is large enough that a single map would exceed ~25–30 total nodes and become unreadable.

**Start lean, expand as needed.** Peter's article emphasizes starting with what you have — a half-baked map that exposes gaps is more useful than a comprehensive map you never finish. You can always add branches and depth in later iterations.

## Personal & Role Maps

Root Mapping works for more than products. Peter describes in his article how he mapped his own role's areas of responsibility as outcomes to ensure, and used the same approach to facilitate career planning for a teammate. A companion article, "Responsibility Without Territory," lays out the deeper principle: **your role is the outcome you're most directly responsible to ensure.**

### Why outcomes instead of activities

Traditional role definitions anchor on territory — activities you perform, skills you "own," platforms you control ("I'm the iOS UI Designer," "I own the notification feature"). This breeds the fear that ruins teams: Will someone step into my area? Will I get pigeonholed? Will my contributions be recognized? Define too broadly and nobody knows who to depend on; define too narrowly and people feel confined.

Outcome-oriented roles dissolve this. Three ideas make the shift:

**The outcome(s)** — not the outputs you make, not the activities you perform, not the methods you use, but the thing that should be true if you're successful. The intended result for the people you serve and the organization.

**…you're most directly responsible** — overlap is expected (teams are unique combinations of humans, not embodied task lists), but there should be something each person has distinctive experience, knowledge, and judgment to be primarily accountable for. Others can contribute, but everyone knows who the expert is to defer to when there's disagreement.

**…to ensure** — ownership isn't about keeping something to yourself; it's about making an outcome a reality *by any effective and honest means*. Sometimes you do it yourself. Sometimes you teach others. Sometimes you delegate, hire, or build a system. The main thing is that it happens — that's the job.

This reframing has three practical effects:
1. **Better partnership.** It sends a clear message that you're not there to "do design" or "do research" but to achieve specific outcomes that your cross-functional partners also care about. It translates what specialists care about into something everyone cares about.
2. **Lower defensiveness.** If what you ultimately care about is an outcome, not a method, you're more open to feedback. The question becomes "is this solution effective?" rather than "do I like what you did in my area?"
3. **Room for creativity and growth.** If you're responsible for an outcome by any effective means, you're empowered to explore better approaches and grow by expanding your means — training others, delegating, hiring — rather than accumulating more territory.

### How a role maps to Root Map structure

When the "product" is a person, practice, or role, adapt the vocabulary:

- **Root outcome** = the overall value this person/practice delivers. For a product design leader, this might be "Ensure a healthy design team that reliably delivers an effective product experience." For a consultant: "Delegate with confidence, not terror." The root is what's true in the world if you're succeeding.
- **Category outcomes** = major areas of responsibility. A design leader might have: Communication (everyone has the info to make effective decisions), Product strategy (every feature decision grounded in well-defined human needs), Hiring & staffing (right mix of skills, reasonable workload), Team health & maturity (culture of respect, collaboration, growth paths). Each is an outcome to ensure, not a task list.
- **Feature outcomes** = more specific outcomes within each area. Under "Team health" a feature-level outcome might be "Every teammate has a clear and credible growth path."
- **Customers** = clients, stakeholders, the organization, the people you serve
- **Business outcomes** = career outcomes, practice growth, organizational impact, revenue
- **Solutions** = services offered, methods used, programs led, deliverables produced. These are means, not ends — they should be the most effective current approach, and they can change.
- **EVS** = the irreducible core. Without these outcomes, clients wouldn't hire you / the role wouldn't justify itself.
- **Star** = what makes you the distinctive choice over alternatives
- **Competitive context** = how your approach compares to other practitioners, firms, or internal alternatives (e.g., "could an agency do this cheaper?")

### When to use personal/role maps

This variant is useful for:
- **Consultants and freelancers** defining their practice — what outcomes do clients hire you to ensure?
- **Professionals clarifying their role** for performance reviews, goal-setting, or new-role onboarding — what should be true if you're successful this year?
- **Leaders defining team roles** — especially when skills overlap and territorial tensions emerge. Map each person's role as outcomes to ensure, and the overlaps become collaborations rather than conflicts.
- **Career transitions** — articulating "why does my work matter and what should I focus on next?"

The same indicators apply: confidence ("am I sure this is the right outcome to own?"), severity ("how much do my stakeholders need this?"), and effectiveness ("how well does my current approach deliver this outcome?").

**Note on role-mapping depth:** A role map often goes one level deeper than a product map at the same scope. Where a product map might have root → category → feature, a role map might add sub-features for specific responsibilities within each area. This is fine — the framework supports n levels. But apply the same discipline: if you're listing daily tasks, you've gone too deep.

## Workflow: From Conversation to Visualization

### Step 1: Accept Whatever the User Brings

Users arrive with different ingredients at different levels of clarity:
- A feature list with no outcomes → you need to identify the outcomes those features produce
- A business mandate → you need to find the customer outcomes that make it viable
- A product vision → you need to break it into addressable outcome branches
- Research insights → you need to translate them into testable product beliefs
- A solution looking for a problem → you need to articulate what outcome it produces
- A LinkedIn profile, website, or bio → you need to extract the value proposition and map it

**Name what they've provided and what's missing.** Example: "You've given me features and a business goal. What's missing is the customer outcomes — what will be true for users if this succeeds."

### Step 2: Build the Map Through Conversation

Use the navigation questions to fill in the hierarchy:

- **Moving UP**: "What broader need does this point to — so that they can ____?"
- **Moving DOWN**: "What smaller problems must be solved to produce this outcome?"
- **Bridging to business**: "If this customer outcome is achieved, what does the business gain?"
- **Bridging to solutions**: "What's your current best shot at making this outcome happen?"
- **Testing EVS**: "If we removed this outcome, would customers still care? Can we compete without it?"

**Take your best guess when the user can't articulate something.** Mark it with a confidence level. An imperfect articulation that's visible and debatable beats a blank space. Tolerate incompleteness — gaps tell the team where their thinking needs work.

### Step 3: Generate the Visual Root Map

**CRITICAL: Before writing ANY data, read the template file first.** Search for a file named `root-map-template*.html` in the available project files or skill directory and read it with the `view` tool. Do NOT generate a Root Map from memory — the template contains the exact data schema, markers, and rendering engine. Every Root Map must start from the template. Skipping this step produces broken output.

After gathering enough context (even if incomplete), **automatically generate an interactive HTML Root Map** showing:

- Outcome nodes grouped with their attached needs, biz outcomes, and solutions in container cards
- Arrows connecting node groups upward through the hierarchy
- Confidence, severity, and effectiveness indicators on nodes (severity as row above need text)
- Differentiation tags
- Dashed lines/borders for non-EVS
- Clickable detail panels with confidence rationale, sources, competitor landscape, team beliefs, and a notes field
- Selected node highlighted with white background and grey border to match detail panel
- Fit-to-viewport initial zoom with zoom-to-cursor scroll behavior

**Always include placeholders for missing ingredients.** If the user hasn't provided something you assess as important for a complete product strategy, include it as a low-confidence placeholder node with a note like "Needs articulation" or "What business outcome does this produce?" or "What's the user need driving this?" Placeholders are especially important for:

- Missing root outcome (if user only has features)
- Missing needs (if outcomes are stated but problems aren't clear)
- Missing business outcomes (if user focuses only on customer value)
- Missing solutions for EVS outcomes (design opportunities)
- Missing branches you infer should exist based on the market/product type

### Step 4: Iterate Through Conversation

The conversation with Claude IS the iteration engine. The user reviews the map and comes back with changes:

- "Change 'Control what I hear' to 'Master my sound environment'"
- "The hearing health confidence should be medium"
- "Add a new feature outcome under Daily"
- "We decided the fitness branch is EVS after all"
- "Add a business outcome to the fitness category: 'Recurring subscription revenue from health-conscious segment'"
- "Remove the business outcome from the awareness branch — that was speculative"
- "Add a solution to the noise cancellation outcome: 'H2 chip + adaptive mesh filtering'"
- "Remove the solution from hearing protection — we're pivoting away from that approach"
- "Here's research that changes our belief about X"

Claude regenerates the HTML incorporating these changes. Each version is a snapshot of the team's evolving beliefs.

**The detail panel includes an editable notes field** where the user can add context, links, evidence, or questions during review. These notes persist for the session and can be fed back into the conversation for the next iteration.

### Step 5: Offer Expansion Opportunities (Optional — Ask First)

**NEVER generate expansion nodes unless the user explicitly requests them.** Expansion nodes are speculative and should not appear on a first-pass map. The first map should be the current-state decision logic only.

Once the core map is stable, you may **ask the user** if they'd like expansion suggestions. Only generate expansion nodes if the user says yes.

**How to ask:** "The core map looks solid. Want me to suggest high-value areas of differentiated expansion or enhancement — places where the product could grow its moat or create new categories?"

If the user agrees, analyze the map for:
- Gaps between existing branches where adjacent value could be captured
- Data or capability assets that could be monetized as new product lines
- Shifts from reactive to proactive (measurement → prediction)
- Missing positive framing (what drives success, not just what causes failure)
- Leaky handoffs where customers leave the platform to do the next step
- Emerging customer types or use cases not yet addressed

**Expansion node rules:**

1. **Correct altitude.** An expansion node must sit at the tier matching its strategic scope:
   - A new outcome branch (comparable to existing categories) → category tier, as a peer
   - A new feature within an existing branch → feature tier, rightmost in its parent's children
   - NEVER create a separate "expansion tier" — expansions live alongside existing nodes

2. **Purple treatment.** Expansion nodes use `isExp: true` and get the purple dashed visual treatment (dashed purple borders, OPPORTUNITY badge, leverage indicator instead of confidence dot). This makes them immediately distinguishable from validated current-state nodes.

3. **Leverage instead of confidence.** Expansion nodes use `leverage: 'high'|'medium'` instead of outcome confidence. High leverage = extends moat or creates new category. Medium leverage = deepens existing differentiation.

4. **Position rightmost.** Expansion categories go to the right of their most related existing category in `catOrd`. Expansion features get the highest `idx` in their parent's child array.

5. **Use `e-` prefix** for expansion node IDs.

### Step 6: Share and Gather Feedback

The HTML file can be shared (download, screen share, etc.). Team members review and provide feedback. The user brings that feedback back to Claude:

- "The PM says 'it's not quite that, more like ____'"
- "Engineering flagged that solution X needs capability Y"
- "Research contradicts our belief about Z"

Claude incorporates and regenerates. This is the loop: **conversation → visualization → review → conversation.**

## Common Mistakes

These are errors that have come up repeatedly during Root Map generation. Check against this list before finalizing any map.

1. **Wrong altitude.** A feature-level outcome placed at category tier (or vice versa). Before assigning a tier, run this checklist:
   - Does this outcome represent a **whole branch** of distinct value (multiple sub-problems)? → **Category**
   - Does it solve **one discrete problem** within a broader branch? → **Feature**
   - Does it break down into 3+ meaningfully distinct sub-outcomes? → Probably a **category**
   - Does it have only 0–1 sub-outcomes? → Probably a **feature** (or it's a category that needs more features beneath it)
   - Could it be a **sub-feature** (a control, setting, or implementation detail)? → Too deep for a strategy map — belongs in a design spec, not here
   - When in doubt: start it as a feature. Promote to category only if you discover it needs multiple children.

2. **Outcomes that are really features in disguise.** "AI-powered recommendations" is a solution, not an outcome. "Discover what's relevant without searching" is the outcome. Always ask: if the solution changed completely, what would still need to be true?

3. **Business outcomes that are really solutions, needs, or user outcomes.** Business outcomes must be things that are **now true for the business** — not features, not customer benefits, not strategies. Test: could a CFO or board member point to this as a business result? "Reduced churn by 15%" yes. "AI-powered analytics dashboard" no (solution). "Users love the product" no (too vague — what business result does that love produce?). "Entered enterprise segment" yes. Good examples: retention, revenue, margin improvement, talent attraction, market expansion, regulatory compliance, data asset growth, brand authority.

4. **Missing or wrong parent references.** Every `F[]` item needs a `parent` field matching a category `id` in `O[]`, and that feature's `id` must appear in the parent's array in `catCh`. If these are out of sync, features will be orphaned or misplaced.

5. **catOrd / catCh mismatch.** Every category `id` in `catOrd` must exist as a key in `catCh`, and every key in `catCh` must appear in `catOrd`. Missing entries cause layout failures.

6. **Overly abstract outcome language.** "Enhanced audio experience" tells you nothing testable. "Block unwanted noise completely" is something you can verify. Push for concrete, direct language — especially at the feature tier where specificity matters most.

7. **Need cards without severity.** Every need should have `needSev: 3|2|1`. Missing severity defaults to no indicator, which looks like a rendering bug.

8. **Solutions on everything.** Not every outcome needs a solution card. Only attach solutions where a concrete implementation exists or is proposed. Empty or vague solutions ("TBD") add noise — use placeholder outcomes instead.

9. **Forgetting the root's need.** The root outcome addresses a need too — the overarching problem the product exists to solve. This is often the most important need statement on the entire map.

### Pre-Output Checklist

Before saving a Root Map file, review the data section against these checks:

**Hierarchy integrity (does it flow upward?):**
- For EACH outcome, verify it directly enables its parent. Ask: "If this child outcome becomes true, does it make the parent outcome MORE true?" If you can't articulate the enabling relationship, the hierarchy is broken — the node is either under the wrong parent, at the wrong altitude, or not a real outcome.
- Read the full chain from any leaf node to root. It should tell a coherent story: "Because [feature outcome] → [category outcome] → [root outcome]." If the chain feels like a stretch at any link, fix the link.
- Watch for "sibling masquerading as child" — two outcomes that are peers (both enable the same parent) but one has been incorrectly nested under the other.

**Outcome language quality:**
- Read each `label` field aloud. Is it concrete enough to verify? Could you test whether it's true? If not, rewrite it.
- Check for corporate-speak: "enhanced," "optimized," "leveraged," "comprehensive" — these are almost always vague. Replace with what the customer actually experiences.
- Check for solution-as-outcome: if the label describes a technology or feature name rather than what it enables, you've written a solution, not an outcome.

**Confidence variation:**
- If every outcome is `conf: 'high'`, you haven't thought hard enough. A map with uniform confidence is a map where nobody questioned anything. Vary confidence honestly — low confidence on a node is more useful than false certainty.
- At minimum: root and well-evidenced categories can be high. New/unproven features should be medium or low. Gen-1 capabilities and beta features should almost always be medium or low.

**Data integrity (the template validates these automatically, but catch them before rendering):**
- Every `id` in `catOrd` has a matching key in `catCh` (and vice versa)
- Every feature's `parent` matches a real category in `catCh`, and the feature's `id` is listed in that category's child array
- Every need has a `needSev` value (1, 2, or 3)
- Root is the first item in `O[]` with `root: true`

## Writing Strong Outcomes

Outcome statements should be:

- **Brief, catchy, and provocative** — these are headlines. Think "now you can ____." A good label sticks in someone's head after seeing the map once.
- **Benefit-focused, never solution-oriented** — describe what's now true for the customer, not what was built. If the label mentions a technology, algorithm, chip, or feature name, it's a solution disguised as an outcome.
- **Concrete and testable** — you could verify whether this is true. "Block unwanted noise completely" is testable. "Enhanced audio experience" is not.
- **Direct and confident** — "Control what I hear" not "Help users manage their audio environment"

The `sub` field then unpacks the headline in plain benefit language — still solution-agnostic. If the label is the movie poster tagline, `sub` is the one-sentence synopsis.

Bad label: "AI-powered noise management" (solution, not outcome)
Bad label: "Enhanced noise management capabilities" (vague corporate)
Bad label: "Noise cancellation feature" (feature name)
Good label: "Control what I hear"
Good sub: "Block, filter, or enhance any sound in your environment on demand"

Bad label: "Hearing health feature suite" (feature name + corporate)
Good label: "Protect and improve my hearing"
Good sub: "Proactively guard against damage and track hearing over time"

For role/personal maps, the same principle applies — shift from activity/territory to outcome:

Bad: "I own visual design on iOS — color, typography, design systems"
Good: "Every detail of the product experience is beautiful, internally-consistent, platform-appropriate, and intuitive"
Bad: "I'm the UX researcher"
Good: "The team has valid, insightful, and actionable evidence to guide user-focused design decisions"
Bad: "I manage the design team"
Good: "A healthy design team reliably delivers an effective product experience"

Notice how the good versions describe what's *true in the world* if the person succeeds — not what they do all day. This is the same cognitive move the framework asks of product teams: stop describing what you build, start describing what becomes true.

### Prefer existing language when it's already strong

When building a Root Map from existing materials — a website, marketing copy, LinkedIn profile, article, or pitch deck — **look for outcome statements the subject has already written well.** A well-crafted tagline, value prop, or signature phrase that already captures the outcome with personality and precision should be used as-is, not rewritten for consistency.

Rewriting strong existing language is a downgrade. The goal is the most compelling, memorable articulation — not the most "framework-consistent" one. Synthesis is for filling gaps, not replacing things that already work.

**How to evaluate:** If the subject's own words are concrete, testable, and memorable, use them. If they're vague or internal-facing ("leverage our platform capabilities"), rewrite. When in doubt, prefer their voice — especially for root outcomes and key differentiator nodes where personality and memorability matter most.

Examples:
- Website says "Delegate with confidence, not terror" → use it (concrete, memorable, has personality)
- Website says "We provide comprehensive delegation solutions" → rewrite (vague corporate)
- LinkedIn says "Shape the future, don't litigate the past" → use it as a label (signature phrase, teaches the concept in one sentence)
- Resume says "Led feedback improvement initiatives" → rewrite (internal-facing, forgettable)

This also applies to marketing messages, testimonial language, and signature frameworks that already function as clear outcome statements or value propositions.

## Generating the Root Map HTML

**Use the locked visual template** — search for `root-map-template*.html` in the project files or skill directory. This template contains the exact CSS, layout engine, rendering logic, detail panel, and interaction from the validated v4 design.

**DO NOT MODIFY anything outside the DATA section.** This means:
- Do NOT touch any CSS (the `<style>` block)
- Do NOT touch the toolbar HTML (the `#bar` div)
- Do NOT touch the layout engine, rendering functions, arrow drawing, detail panel, or zoom code (everything after `===END DATA===`)
- Do NOT add `<script>` tags, `<link>` tags, or any other HTML outside the DATA section (exception: the `<title>` and toolbar `<h1>` for the product name)
- ONLY replace content between the `===DATA===` and `===END DATA===` markers

If you find yourself wanting to change the rendering — stop. The template handles it. You only supply data.

### How to populate the template

1. Read the template file to get the full HTML structure
2. Replace `PRODUCT_NAME` in the title and toolbar with the actual product name
3. Replace the DATA section (between `===DATA===` markers) with product-specific arrays:
   - `catCh` — maps category IDs to their child feature IDs
   - `catOrd` — left-to-right category display order (EVS by shipping sequence → non-EVS → expansion)
   - `O[]` — root + category outcome objects
   - `F[]` — feature outcome objects with `parent` and `idx` fields
4. If expansion nodes were requested, include them inline:
   - Category-level expansions: add to `O[]` with `isExp:true`, add their ID to `catOrd` and `catCh`
   - Feature-level expansions: add to `F[]` with `isExp:true`, add their ID to their parent's array in `catCh`
   - Update the toolbar subtitle to "Inferred decision logic + expansion opportunities"
   - Add the Opportunity legend item to the toolbar
5. The layout engine automatically computes zone widths, positions, centers root above all categories, fits to viewport, and draws arrow paths
6. Save as a new HTML file in outputs

### Data object schema

Every outcome node (root, category, or feature) uses this shape:

```javascript
{
  id: 'c-xxx',                      // unique id (c- for categories, f- for features, e- for expansions)
  parent: 'c-xxx',                   // features only: parent category id
  idx: 0,                            // features only: position index within parent
  root: true,                        // root only: marks as root node
  evs: true|false,                   // essential value scope
  star: true,                        // optional — key differentiator (where you WIN, not just must-have)
  diff: 'diff'|'ts'|'bg'|'unc'|'beh', // competitive position
  conf: 'high'|'medium'|'low',      // outcome confidence
  label: 'Outcome statement',        // brief, catchy, provocative, benefit-focused (see "Writing Strong Outcomes")
  sub: 'Supporting detail',            // ALWAYS solution-agnostic. Explains the catchy headline in plain language.
                                       // Good: "Never miss a word, even in noisy environments"
                                       // Bad: "Uses H2 chip with adaptive filtering" (that's a solution)
                                       // Bad: "Our noise cancellation feature" (that's a feature name)
  need: 'Customer problem',          // every outcome should have this
  needSev: 3|2|1,                    // 3=severe, 2=moderate, 1=minor
  biz: ['Business outcome'],         // optional array — things NOW TRUE FOR THE BUSINESS (see Common Mistakes #3)
  bizIndicators: ['Metric or signal'], // optional array — how you'd measure business outcomes (e.g., "NPS > 50", "churn < 5%")
  sol: [{name, tech, eff}],          // optional array — only when concrete solution exists
  indicators: ['Metric or signal'],  // optional array — how you'd know this outcome is being achieved
                                     // e.g., "Task completion rate > 90%", "Zero noise complaints in user testing"
                                     // These are proposed, not commitments — they help teams discuss what "true" means
  detail: {confReason, sources, belief, competitors, notes}  // for detail panel
  // EXPANSION ONLY:
  isExp: true,                       // marks as expansion opportunity node
  leverage: 'high'|'medium',         // strategic leverage (replaces confidence in display)
}
```

### Placeholder nodes

For missing ingredients, create nodes with:
- `conf: 'low'`
- `label: '? [Best guess or description of what goes here]'`
- `need: '? What problem does this solve for users?'` (if need is missing)
- No `sol` array (if no solution exists yet)
- `detail.notes: 'PLACEHOLDER — needs team input to articulate this outcome'`

### Visual rules

The template CSS and layout engine are the source of truth for all visual rendering. Do not duplicate CSS values in the data layer. For a readable reference of the template's visual rules (colors, sizes, borders, spacing), see `references/visual-spec-v4.md`.

Key **conceptual rules** to keep in mind when populating data (these affect data structure, not CSS):
- All outcome cards are blue. Root, category, feature — same color, different scope.
- Arrows connect node groups to node groups ONLY, flowing upward. No arrows between non-outcome elements.
- Need cards always sit above their parent outcome within the container group.
- Business and solution cards sit below their parent outcome within the container group.
- Non-EVS nodes: `evs: false` → template renders dashed borders, dashed lines, reduced opacity.
- EVS nodes: `evs: true` → template renders solid borders, solid lines, full opacity.
- Expansion nodes: `isExp: true` → template renders purple treatment, OPPORTUNITY badge, leverage dot.
- Category order in `catOrd`: EVS by shipping sequence (foundational → dependent), then non-EVS, then expansion rightmost.
- Root auto-centers above the midpoint of all categories. No manual positioning needed.

## Quick Diagnostic

When a product effort feels stuck, ask:

1. Can you state the top-level customer outcome in one sentence?
2. Does the whole team agree?
3. Which outcomes are essential vs. nice-to-have?
4. Is there a clear business outcome that makes this worth doing?
5. Are features justified by outcomes, or just by being "good ideas"?

If any answer is unclear, that's where to focus.

## References

### Template & specs
- `root-map-template*.html` — **Locked visual template (v4 spec).** Read this first before generating any Root Map. Contains exact CSS, layout engine, rendering, and detail panel. Only replace the DATA section. Search project files or skill directory for this file.
- `visual-spec*.md` — Readable reference for the template's visual rules (colors, spacing, typography, indicators). The template is the source of truth; this file is for quick lookup.

### Canonical examples
Search the available project files or skill directory for example Root Maps. Key examples to look for:
- `airpods-pro3-root-map*.html` — **Primary data reference.** Complex product with EVS/non-EVS categories, expansion opportunities, full detail panels, star differentiators, Phosphor icons on business outcomes. Best example of field usage and data structure completeness.
- `peter-lewis-root-map*.html` — **Personal/role map example.** Maps an individual's professional practice as outcomes to ensure. Shows how the framework adapts for people, not products.
- `root-mapping-meta-root-map*.html` — **Meta example.** Root Map of the Root Mapping framework itself. Demonstrates self-referential use and how to map a framework/methodology.
- `spotify-root-map*.html` — **Product map example.** Well-known consumer product with star differentiators, EVS/non-EVS categories, competitive landscape, and v4 template features (indicators, interactive add/remove).

### Source materials
- Peter Lewis, "Nobody cares about your product." — original framework article (https://medium.com/@thispeterlewis/value-mapping-6203c997c463)
- Peter Lewis, "Responsibility Without Territory" — companion article on outcome-oriented role definition, foundational for Personal & Role Maps (https://medium.com/capitalonedesign/responsibility-without-territory-65501c807f80)
