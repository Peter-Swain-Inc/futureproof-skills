---
name: offer-diagnostic
description: |
  Diagnoses the structural health, positioning clarity, and conversion readiness of an offer using a systematic audit framework.
  Trigger: when a user shares an offer (landing page, sales page, course outline, service package, proposal, or pricing structure) and asks for a diagnostic, audit, teardown, or wants to understand why it isn't converting.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="offer-diagnostic")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior ICA definitions, positioning work, competitive intel, or conversion data the user has accumulated.

## Step 2: Get Input

Ask the user to provide:

1. **The offer itself** — landing page URL, sales page copy, pitch deck, service package description, pricing table, or proposal document
2. **The ICA this offer targets** — who specifically is this for? (If ICA is already defined in FutureProof context, confirm or refine)
3. **The primary conversion mechanism** — how does the prospect say yes? (application, checkout, booking call, reply, sign contract)
4. **Current performance data** (if available) — traffic, conversion rate, close rate, average deal value, refund rate, objection frequency
5. **The user's hypothesis** — what do they believe is broken, or where do they feel the friction lives?

If the user cannot provide performance data, proceed with qualitative diagnostic and flag data gaps as a finding.

## Step 3: Conduct the Offer Diagnostic

Apply a **seven-dimension diagnostic framework** to systematically evaluate the offer. Each dimension maps to a specific failure mode that suppresses conversion.

### Dimension 1: ICA Specificity & Problem Articulation

- Does the offer name a specific person with a specific problem, or does it speak to a vague audience?
- Is the problem articulated in the ICA's own language (first-person phrasing, vernacular, emotional register)?
- Is the severity of the problem established — what is the cost of inaction?
- **Failure mode**: Offer speaks to everyone, resonates with no one.

### Dimension 2: Mechanism Clarity

- Does the offer explain *how* it solves the problem — the unique mechanism, method, or framework?
- Is the mechanism named, proprietary, or differentiated from commodity alternatives?
- Can the prospect understand *why this approach works* without needing a sales call to fill in gaps?
- **Failure mode**: Prospect sees no reason to choose this over alternatives or inaction.

### Dimension 3: Transformation Architecture

- Is there a clearly defined **before state** (current pain) and **after state** (desired outcome)?
- Are outcomes expressed in concrete, measurable, or viscerally felt terms — not abstract benefits?
- Is the transformation scoped to a believable timeframe?
- **Failure mode**: Prospect cannot visualise the result or does not believe it applies to them.

### Dimension 4: Offer Structure & Value Stack

- Is the offer structured as a coherent solution (not a feature list or menu of deliverables)?
- Does each component of the value stack map to a specific ICA obstacle or objection?
- Is there a logical hierarchy — core deliverable, accelerators, risk-removers?
- Is scope clearly bounded to prevent scope anxiety ("what am I actually getting?")?
- **Failure mode**: Prospect is overwhelmed, confused, or underwhelmed by the composition.

### Dimension 5: Pricing & Risk Architecture

- Does the price anchor against the cost of the problem or the value of the outcome (not cost of delivery)?
- Is there a risk-reversal mechanism (guarantee, pilot, milestone-based payment, proof-of-concept)?
- Are pricing tiers (if present) structured to guide the prospect toward the optimal option, not paralyse them?
- Is the price-to-perceived-value ratio at minimum 1:3 (prospect perceives 3× the value of the price)?
- **Failure mode**: Prospect stalls on price because value framing is insufficient or risk feels asymmetric.

### Dimension 6: Proof & Credibility Density

- Are claims substantiated by case studies, results, testimonials, data, or credentials?
- Is proof *specific* (named outcomes, timeframes, ICA-similar clients) rather than generic?
- Is proof distributed throughout the offer — not clustered in a single testimonials section?
- Does the proof address the prospect's implicit question: "Will this work for *someone like me*?"
- **Failure mode**: Prospect believes the offer works — just not for them.

### Dimension 7: Conversion Path & Friction Audit

- Is the call to action singular, specific, and low-ambiguity?
- Is the next step proportional to the commitment level (micro-commitment for high-ticket, direct checkout for low-ticket)?
- Are there unnecessary friction points — excessive form fields, unclear next steps, competing CTAs, missing urgency?
- Does the page or document maintain a single persuasive through-line, or does it leak attention?
- **Failure mode**: Interested prospects drop off due to procedural friction or decision fatigue.

Cross-reference all findings against any user-specific `instructions` from FutureProof context (e.g., brand voice constraints, compliance requirements, industry norms).

## Step 4: Deliver the Offer Diagnostic Report

Produce a structured **Offer Diagnostic Report** with the following sections:

### 4.1 — Diagnostic Scorecard

| Dimension | Score (1–10) | Severity | Verdict |
|---|---|---|---|
| ICA Specificity & Problem Articulation | — | Critical / Moderate / Healthy | One-line finding |
| Mechanism Clarity | — | Critical / Moderate / Healthy | One-line finding |
| Transformation Architecture | — | Critical / Moderate / Healthy | One-line finding |
| Offer Structure & Value Stack | — | Critical / Moderate / Healthy | One-line finding |
| Pricing & Risk Architecture | — | Critical / Moderate / Healthy | One-line finding |
| Proof & Credibility Density | — | Critical / Moderate / Healthy | One-line finding |
| Conversion Path & Friction | — | Critical / Moderate / Healthy | One-line finding |
| **Composite Offer Health Score** | **—/70** | | |

### 4.2 — Root Cause Analysis

Identify the **primary conversion bottleneck** — the single dimension most responsible for suppressing results. Explain the causal chain: why this specific weakness leads to the observed (or likely) outcome.

### 4.3 — Critical Fixes (Priority-Ranked)

Deliver the **top 5 highest-impact interventions**, each containing:

1. **What to change** — specific element (headline, pricing section, CTA, value stack item)
2. **Why it matters** — the conversion psychology or structural principle at play
3. **Exact rewrite or restructure** — not a suggestion, but a concrete draft the user can deploy immediately
4. **Expected impact** — qualitative or quantitative estimate of improvement

### 4.4 — Revised Core Section

Select the single weakest section of the offer and produce a **full rewrite** — maintaining the user's brand voice (drawn from FutureProof context where available) while resolving all identified deficiencies in that section.

### 4.5 — Competitive Positioning Note

Based on the mechanism and ICA, flag any positioning collisions with commodity alternatives (e.g., "This offer currently positions identically to a generic [category] — here is how to create separation").

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="offer-diagnostic", experiment={
  hypothesis: "[Specific hypothesis based on the primary conversion bottleneck identified — e.g., 'Replacing the feature-list value stack with an obstacle-mapped solution narrative will increase page-to-application conversion']",
  variants: ["control: current offer structure", "variant: restructured offer with [specific change]"],
  measurement: "[Relevant metric — e.g., landing page conversion rate, sales call booking rate, proposal-to-close ratio, measured over N prospects or N days]",
  expected_impact: "[Quantified estimate — e.g., 20-35% improvement in page-to-call conversion based on improved ICA problem specificity]"
})
```

Propose 1–2 additional experiments if multiple critical fixes were identified, each targeting a different dimension.

## Step 6: Request Research

```
FutureProof:request_research(skill="offer-diagnostic",
  query="[Contextual query based on the user's ICA, industry, and identified gaps — e.g., 'High-converting offer structures and pricing psychology for B2B consulting services targeting mid-market CFOs 2024' or 'Risk-reversal mechanisms with highest impact on SaaS trial-to-paid conversion']",
  reason="[Specific rationale — e.g., 'User's offer lacks differentiated mechanism positioning; need current competitive landscape and emerging offer architectures in their vertical to inform restructure']"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="offer-diagnostic", session={
  summary: "Conducted full offer diagnostic for [offer name/type] targeting [ICA segment]. Composite health score: [X/70]. Primary bottleneck: [dimension]. Delivered [N] critical fixes with rewrites.",
  key_findings: ["[Finding 1 — e.g., 'ICA specificity scored 3/10: headline addresses generic audience, zero first-person pain language']", "[Finding 2 — e.g., 'No mechanism differentiation: offer is structurally identical to 4+ competitors in the space']", "[Finding 3 — e.g., 'Risk architecture absent: no guarantee, no pilot option, full payment upfront on a $12K offer']"],
  recommendations_delivered: ["[Rec 1]", "[Rec 2]", "[Rec 3]"],
  user_feedback: null
})
```