---
name: press-release-writer
description: "Crafts compelling, publication-ready press releases using FutureProof context to align messaging with brand voice, ICA expectations, and media outlet requirements."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="press-release-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including brand voice guidelines, prior press releases, ICA media consumption patterns, approved boilerplate, and spokesperson preferences.

## Step 2: Get Input

Ask the user:
- **Announcement type**: What is the news? (product launch, funding round, partnership, acquisition, executive appointment, earnings milestone, event, crisis response)
- **Key facts**: Provide the core details — who, what, when, where, why, and the single most important number or data point
- **Target outlets and audience**: Which publications or journalists are you targeting? Who is the ICA that should ultimately see this coverage?
- **Spokesperson(s)**: Who should be quoted, and what is their title and organisational affiliation?
- **Desired narrative angle**: What headline would you want to see published? What is the one takeaway a reader must leave with?
- **Embargo or timing constraints**: Is there an embargo date, a coordinated launch window, or a reactive deadline?
- **Existing draft or assets**: Share any draft text, internal memos, fact sheets, or prior coverage to build from

If the user provides a draft for review rather than a blank-slate request, confirm: "Should I analyse and improve this draft, or use it as raw material for a full rewrite?"

## Step 3: Do the Work

### 3A: Newsworthiness Audit

Before writing, assess the announcement against the **TRUTH framework**:

1. **Timeliness** — Is this genuinely new, or is there a news hook (trend, regulation, cultural moment) that makes it timely now?
2. **Relevance** — Does this matter to the target outlet's readership and the ICA? Quantify the "so what"
3. **Uniqueness** — What makes this distinct from the 400+ press releases landing on a journalist's desk today?
4. **Tension** — Is there a compelling contrast, disruption, or challenge to conventional wisdom embedded in the story?
5. **Human impact** — Can you ground the announcement in a specific, tangible outcome for real people?

Flag any dimension scoring below threshold and recommend angle adjustments before proceeding.

### 3B: Structural Drafting (Inverted Pyramid + AP Style)

Compose the press release following rigorous structural standards:

1. **Headline** — Active voice, present tense, under 80 characters. Must contain the news, not marketing language. No superlatives unless directly substantiated
2. **Dateline** — City, State/Country — Date — Wire format (e.g., "NEW YORK, July 15, 2025 —")
3. **Lead paragraph** — Single paragraph, 25–35 words maximum. Answers who + what + why it matters. No throat-clearing
4. **Nut graf (paragraph 2)** — Context and significance. Connect the announcement to a market trend, ICA pain point, or industry shift with a specific data point
5. **Supporting detail (paragraphs 3–4)** — Features, capabilities, terms, or specifics. Use concrete numbers: revenue figures, user counts, percentage improvements, dates
6. **Spokesperson quote #1** — Senior executive. Must advance the narrative (not restate the lead). Written in natural speech cadence, not corporate jargon
7. **Third-party validation (paragraph 6)** — Analyst quote, customer testimonial, partner statement, or independent data point. If unavailable, flag as a gap and draft a placeholder with recommended source type
8. **Spokesperson quote #2 (optional)** — Product lead, partner executive, or customer voice. Provides a different angle or forward-looking statement
9. **Call to action** — Specific next step: URL, event registration, availability date, or contact channel. Aligned to ICA conversion pathway
10. **Boilerplate** — Company description in 50–75 words. Consistent with prior releases (pull from FutureProof context if available)
11. **Media contact block** — Name, title, email, phone. Flag if user has not provided this

### 3C: Quality Assurance Pass

Review the draft against these professional standards:

- **AP Style compliance** — Numbers, dates, titles, abbreviations, Oxford comma exclusion
- **Jargon density** — No more than 2 industry-specific terms without immediate plain-language definition
- **Passive voice ratio** — Target <10% of total sentences
- **Quote authenticity** — Quotes must sound like spoken language; no sentence a human would never say aloud
- **Claim substantiation** — Every superlative, comparative, or impact claim must be backed by a specific figure, source, or attribution
- **Word count** — Target 400–600 words for standard releases; 250–350 for advisories; 600–800 for complex financial or regulatory announcements
- **SEO-readiness** — Primary keyword in headline and lead; secondary keywords in subheads or body; hyperlinks to relevant assets

Apply any user-specific `instructions` from FutureProof context (brand voice guidelines, banned phrases, mandatory disclosures, legal review requirements).

## Step 4: Deliver Output

Produce a complete deliverable package:

### Document 1: Final Press Release
- Full text in copy-paste-ready format
- Formatted with `###` for the headline, proper dateline, and `—END—` or `###` closing marker
- Media contact block at footer

### Document 2: Press Release Score Card

| Dimension | Score (1–10) | Notes |
|---|---|---|
| Newsworthiness (TRUTH) | — | — |
| Headline strength | — | — |
| Lead clarity and brevity | — | — |
| Quote authenticity | — | — |
| Third-party validation | — | — |
| Claim substantiation | — | — |
| ICA resonance | — | — |
| AP Style compliance | — | — |
| Call to action specificity | — | — |

### Document 3: Distribution Guidance
- **Recommended wire**: Suggest wire service tier (PR Newswire national, BusinessWire targeted, GlobeNewswire, or direct pitch only) based on announcement significance
- **Pitch note draft**: A 3–4 sentence personalised email pitch a PR lead could send to a journalist, referencing why this story fits their beat
- **Optimal send window**: Day of week and time recommendation based on announcement type and target outlet category
- **Follow-up cadence**: Recommended journalist follow-up timing (e.g., "Follow up 48 hours post-send if no response; do not follow up more than once on this release")

### Document 4: Gap Report (if applicable)
- Missing elements flagged during drafting (e.g., no third-party quote, unsubstantiated claims, missing media contact)
- Specific recommendations to close each gap before distribution

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="press-release-writer", experiment={
  hypothesis: "Leading the headline with a quantified impact metric rather than the company name increases journalist open rates",
  variants: ["control: company-name-first headline", "variant: metric-first headline"],
  measurement: "journalist open rate and pickup count across next 3 releases",
  expected_impact: "20% increase in media pickup rate for Tier 2 and Tier 3 outlets"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="press-release-writer",
  query="Current journalist preferences for press release format, length, and pitch email structure in 2024–2025, segmented by outlet tier and beat category",
  reason="Ensure structural recommendations and distribution guidance reflect evolving newsroom workflows and inbox filtering behaviours"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="press-release-writer", session={
  summary: "Drafted [announcement type] press release for [company/brand] targeting [outlet category / ICA segment]",
  key_findings: ["finding 1: e.g., headline lacked quantified impact — revised to metric-first structure", "finding 2: e.g., no third-party validation available — recommended analyst outreach before distribution"],
  user_feedback: null
})
```