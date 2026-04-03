---
name: offer-naming-positioner
description: |
  Creates differentiated, market-specific offer names using Hormozi's MAGIC naming formula (Make a Magnetic reason why, Announce your avatar, Give them a goal, Indicate a time container, Complete with a container word) so the offer stands out as a 'category of one' and resists commoditisation or price comparison.
  Trigger: when a user asks for help naming an offer, product, program, or service — or when they say their current offer sounds generic, is being compared on price, or needs repositioning to stand out in their market.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="offer-naming-positioner")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any previously defined ICA profiles, existing offer architecture, brand voice guidelines, and prior naming experiments.

## Step 2: Get Input

Ask the user to provide:

1. **The offer itself** — What does it deliver? What transformation does the buyer experience? (If undefined, flag that offer design should precede naming and recommend the relevant skill.)
2. **The ICA** — Who is this for? Industry, role, demographic, psychographic profile, and the language they use to describe their own problem.
3. **Current name (if any)** — What is the offer called today, and why does it feel insufficient? (e.g., sounds generic, gets compared on price, doesn't communicate uniqueness)
4. **Competitive landscape** — Name 2–5 competing or substitute offers the ICA encounters. What are they called? How are they positioned?
5. **Desired perception** — What should the ICA feel or believe the moment they hear the offer name? (e.g., exclusivity, speed, certainty, specificity)
6. **Constraints** — Any brand guidelines, tone preferences, words to avoid, or domain/trademark considerations?

If FutureProof context already contains ICA profiles or offer details, surface them and ask the user to confirm or update rather than re-entering from scratch.

## Step 3: Audit the Current Positioning Landscape

Before generating names, perform a **Commoditisation Risk Audit**:

1. **Generic Language Test** — Could the current name (or description) be used by any competitor without modification? If yes, it fails.
2. **Price Anchor Test** — Does the name invite comparison to lower-priced alternatives? (e.g., "Consulting Package" → immediately compared to Fiverr freelancers)
3. **ICA Specificity Test** — Does the name signal *exactly* who it is for, causing non-ICA prospects to self-deselect?
4. **Mechanism Visibility Test** — Does the name hint at a proprietary method, framework, or process that cannot be replicated?
5. **Outcome Clarity Test** — Can the ICA infer the result they will achieve from the name alone?

Score each dimension **1–5** and identify the weakest areas. These become the primary constraints the MAGIC formula must resolve.

## Step 4: Apply Hormozi's MAGIC Naming Formula

Systematically work through each element of the MAGIC framework, generating multiple candidates per element before combining:

### M — Make a Magnetic Reason Why
Generate 3–5 **"reason why" modifiers** that create urgency, scarcity, or intrigue. These answer: *Why this? Why now?*
- Examples of patterns: challenge-based, seasonal, outcome-driven, contrarian, event-based

### A — Announce Your Avatar
Generate 3–5 **avatar-specific identifiers** drawn directly from the ICA's self-description. The name must make the ICA say: *"That's for me."*
- Use the ICA's own language, not industry jargon they wouldn't use
- Consider role titles, aspirational identities, or community labels

### G — Give Them a Goal
Generate 3–5 **outcome or goal descriptors** that name the specific, tangible result the ICA wants. Prioritise:
- Measurable outcomes over vague aspirations
- Language the ICA uses when describing their desired future state
- Goals that competitors do NOT name explicitly

### I — Indicate a Time Container
Generate 3–5 **temporal frames** that create urgency and set expectations:
- Sprint durations (7-day, 30-day, 90-day)
- Event-based containers (intensive, accelerator, sprint)
- Seasonal or cohort-based timing

### C — Complete with a Container Word
Generate 3–5 **container words** that frame the delivery vehicle and signal value:
- High-value containers: Academy, Institute, Accelerator, Blueprint, System, Protocol, Lab, Vault
- Avoid overused containers in the ICA's specific market (reference competitive landscape from Step 2)
- Match the container word to the price point and perceived sophistication

## Step 5: Assemble and Evaluate Candidate Names

### Name Generation
Combine elements from Step 4 to produce **8–12 candidate offer names**, organised into three tiers:

| Tier | Description | Count |
|------|-------------|-------|
| **Bold** | Maximum differentiation, high memorability, potentially polarising | 3–4 names |
| **Balanced** | Clear, professional, strong ICA resonance, broadly safe | 3–4 names |
| **Conservative** | Understated, credible, suitable for enterprise or regulated markets | 2–4 names |

### Evaluation Matrix
Score each candidate name against five criteria (1–10 each):

1. **ICA Magnetism** — Does the ICA immediately self-identify? Would they screenshot this and send it to a peer?
2. **Competitive Differentiation** — Is this name impossible to confuse with the competing offers listed in Step 2?
3. **Outcome Transparency** — Can the ICA infer the transformation from the name alone?
4. **Memorability & Shareability** — Is it easy to say, spell, and repeat in conversation?
5. **Price Insulation** — Does the name resist downward price comparison? Does it signal premium?

### Deliver the Top 3 Recommendations
For each of the top 3 scoring names, provide:

- **The full offer name**
- **MAGIC element breakdown** — label which word/phrase maps to M, A, G, I, C
- **Positioning statement** — one sentence: *"[Offer Name] is the only [container] that helps [avatar] achieve [goal] in [timeframe] by [mechanism]."*
- **Tagline variant** — a 5–10 word hook for landing pages or ad copy
- **Risk assessment** — any trademark, cultural, or market-perception risks

## Step 6: Deliver the Offer Naming & Positioning Dossier

Produce the **Offer Naming & Positioning Dossier** containing:

1. **Executive Summary** — The recommended name, the strategic rationale, and how it resolves the commoditisation risks identified in Step 3.
2. **Commoditisation Risk Audit** — Scorecard from Step 3 showing before-state weaknesses.
3. **MAGIC Element Library** — The full bank of candidates per element (M, A, G, I, C) for future remixing.
4. **Top 3 Named Offers** — Full evaluation per Step 5, with scores and positioning statements.
5. **Competitive Positioning Map** — A simple 2×2 or list showing how the recommended name sits relative to competitor offers on the axes of *specificity* and *perceived value*.
6. **Implementation Guidance** — Where and how to deploy the name: sales pages, ad headlines, email subject lines, verbal pitch, and social media bios. Include specific copy-paste examples for each channel.

Format: structured markdown document. If FutureProof context indicates the user works with a team, note that this dossier is suitable for sharing with copywriters, marketing leads, or brand stakeholders.

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="offer-naming-positioner", experiment={
  hypothesis: "Replacing the current generic offer name with the MAGIC-formula name increases landing page click-through rate by signalling ICA-specific relevance",
  variants: ["control: current offer name in headline and CTA", "variant: top-recommended MAGIC name in headline and CTA"],
  measurement: "Landing page CTR, sales page conversion rate, and qualitative ICA feedback over 14-day window",
  expected_impact: "20–35% improvement in click-through rate; reduction in price-objection frequency during sales conversations"
})
```

```
FutureProof:save_experiment(skill="offer-naming-positioner", experiment={
  hypothesis: "Using the avatar-specific identifier (A element) in ad copy pre-qualifies traffic and reduces unqualified lead volume",
  variants: ["control: broad audience language in ad headline", "variant: ICA-specific avatar term from MAGIC name in ad headline"],
  measurement: "Lead qualification rate and cost-per-qualified-lead over 30 days",
  expected_impact: "15% reduction in cost-per-qualified-lead through improved self-selection"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="offer-naming-positioner",
  query="Current high-performing offer name structures and container words in [user's industry/niche] — including overused terms losing differentiation power and emerging naming conventions that signal premium positioning, 2024–2025",
  reason="Ensure recommended names avoid saturated naming patterns in the user's specific market and leverage emerging conventions that signal category leadership"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="offer-naming-positioner", session={
  summary: "Generated MAGIC-formula offer names for [offer type] targeting [ICA segment] in [market/niche]",
  key_findings: ["Primary commoditisation risk: [weakest audit dimension]", "Top recommended name: [name] — scored [X]/50 on evaluation matrix", "Key differentiator leveraged: [specific MAGIC element that drove the most separation from competitors]"],
  artifacts: ["Offer Naming & Positioning Dossier", "MAGIC Element Library", "Competitive Positioning Map"],
  user_feedback: null
})
```