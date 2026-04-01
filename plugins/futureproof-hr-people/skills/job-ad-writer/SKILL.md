---
name: job-ad-writer
description: "Crafts high-converting job advertisements using FutureProof context, employer brand intelligence, and evidence-based copywriting frameworks."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="job-ad-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including employer brand voice, previous role archetypes, compensation philosophy, ICA candidate profiles, and any winning patterns from prior job ads.

## Step 2: Get Input

Ask the user:
- **Role details**: Job title, department, reporting line, and level (individual contributor, lead, manager, director, executive)
- **Ideal Candidate Audience (ICA)**: Who is the ideal person for this role — what are they doing today, what motivates a move, and what would make them stop scrolling?
- **Key responsibilities**: Top 5–7 core deliverables or outcomes (not a 20-item task list)
- **Must-have vs nice-to-have requirements**: Hard skills, credentials, years of experience — separated strictly into non-negotiable and preferred
- **Compensation & benefits**: Salary range (or band), equity, bonus structure, and top 3–5 benefits that differentiate the offer
- **Work model**: On-site, hybrid, or remote — including location constraints, timezone expectations, and travel requirements
- **Employer brand notes**: Any specific tone, voice guidelines, EVP (Employer Value Proposition) pillars, or cultural narratives to weave in
- **Distribution channels**: Where will this ad be posted? (LinkedIn, Indeed, specialist boards, careers page) — format requirements vary by channel

If FutureProof context contains prior ICA profiles, employer brand assets, or role templates, surface them and ask the user to confirm or adjust rather than re-collecting from scratch.

## Step 3: Do the Work

Build the job ad through a six-dimension framework:

### 3.1 ICA Candidate Analysis

Define the ICA candidate persona:
- **Current state**: Where do they work now, what is their title, what frustrations do they experience?
- **Trigger events**: What makes them open to a new role (stagnation, layoff risk, misalignment, ambition)?
- **Decision criteria**: What do they evaluate first — compensation, mission, growth trajectory, manager quality, flexibility?
- **Language mapping**: What terminology does this ICA use to describe their own skills and aspirations? Mirror it exactly.

### 3.2 Headline & Hook Engineering

Craft the opening 2–3 sentences using the **AIDA-R framework** (Attention, Interest, Desire, Action, Relevance):
- **Attention**: Lead with the transformation or opportunity — not the company name or generic "We're hiring"
- **Interest**: Surface the single most compelling differentiator of the role (impact, autonomy, scale, mission)
- **Relevance**: Speak directly to the ICA's current pain or aspiration within the first 50 words

### 3.3 Role Narrative Construction

Structure the role description as a **90-day impact arc**, not a static task list:
- **First 30 days**: What will the candidate learn, who will they meet, what quick wins are achievable?
- **First 90 days**: What meaningful outcome will they own or contribute to?
- **First year**: What trajectory does success unlock — scope expansion, team growth, strategic influence?

This transforms a job ad from a requirements document into a career narrative.

### 3.4 Requirements Calibration

Apply the **Must / Should / Could / Won't (MoSCoW)** prioritisation to requirements:
- **Must have**: True non-negotiables — typically 3–5 items maximum. Every item must pass the test: "Would we reject an otherwise exceptional candidate who lacked this?"
- **Should have**: Strong preferences that meaningfully improve performance
- **Could have**: Differentiators that signal exceptional fit
- **Won't require**: Explicitly call out common assumptions the ICA might self-screen on (e.g., "You don't need a degree in X" or "We don't require industry-specific experience")

Anti-inflation audit: Flag any requirement that is likely to disproportionately deter underrepresented candidates without being a genuine performance predictor.

### 3.5 Employer Value Proposition Integration

Weave EVP pillars throughout — not as a bolted-on "Why join us" section but embedded in the language:
- **Proof over claims**: Replace "fast-paced environment" with specific evidence ("Shipped 14 product releases last quarter")
- **Specificity over superlatives**: Replace "competitive salary" with the actual range
- **Social proof**: Reference team achievements, Glassdoor ratings, awards, retention metrics, or growth data where available

### 3.6 Inclusion & Bias Audit

Run the draft through a structured bias review:
- **Gendered language scan**: Flag and neutralise terms with demonstrated gender-coded skew (e.g., "rockstar," "ninja," "nurturing") per Gaucher et al. (2011) research
- **Requirement inflation check**: Identify requirements that serve as proxies for tenure, pedigree, or access rather than capability
- **Accessibility & clarity**: Ensure reading level is appropriate (aim for Grade 9–11), jargon is contextualised, and the application process is transparent
- **Inclusive signals**: Verify that the ad contains at least one explicit inclusion statement and that benefits listed are relevant to diverse life circumstances

Apply any user-specific `instructions` from FutureProof context — including brand voice rules, DEI commitments, legal disclaimers, and formatting standards.

## Step 4: Deliver Output

Produce the following structured deliverables:

### Deliverable 1: Job Ad — Full Copy

A publication-ready job advertisement formatted for the primary distribution channel, including:
- **Headline** (optimised for search and scroll-stop)
- **Opening hook** (2–3 sentences)
- **About the role** (90-day impact arc narrative)
- **What you'll do** (5–7 outcome-oriented responsibilities)
- **What you bring** (MoSCoW-structured requirements, clearly separated)
- **What we offer** (EVP-integrated compensation and benefits)
- **About the company** (2–3 sentences — mission, scale, stage)
- **How to apply** (specific, frictionless next step)

### Deliverable 2: Channel-Adapted Variants

If multiple distribution channels were specified, provide adapted versions:
- **LinkedIn**: Optimised for 150-character preview, hashtag strategy, and mobile readability
- **Indeed / Job boards**: Keyword-dense, structured for ATS parsing, bullet-heavy
- **Careers page**: Longer-form, brand-rich, multimedia-friendly structure
- **Social media teaser**: 280-character hook version for X/Twitter, or short-form for Instagram/TikTok recruitment campaigns

### Deliverable 3: ICA Candidate Persona Card

A one-page reference document for hiring managers and recruiters:
- ICA demographic and psychographic profile
- Top 3 attraction levers for this persona
- Top 3 objections this persona will have (and how the ad pre-empts them)
- Recommended sourcing channels ranked by ICA density

### Deliverable 4: Bias & Quality Scorecard

| Dimension | Score (1–10) | Notes |
|---|---|---|
| ICA resonance | | Does the language mirror the ICA's vocabulary? |
| Headline stopping power | | Would the ICA pause their scroll? |
| Role clarity | | Can the candidate picture day-to-day reality? |
| Requirement calibration | | Are requirements tight, fair, and justified? |
| EVP specificity | | Are claims backed by evidence, not platitudes? |
| Inclusion & bias | | Language neutrality, barrier reduction, accessibility |
| Call to action clarity | | Is the next step obvious and low-friction? |

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="job-ad-writer", experiment={
  hypothesis: "Leading with the 90-day impact narrative instead of a traditional responsibility list increases qualified application rate",
  variants: ["control: standard responsibilities-first structure", "variant: 90-day impact arc opening"],
  measurement: "Qualified applicant volume and applicant-to-screen conversion rate over 30-day posting window",
  expected_impact: "20% increase in qualified applications and 10% reduction in unqualified applications"
})
```

```
FutureProof:save_experiment(skill="job-ad-writer", experiment={
  hypothesis: "Explicitly listing salary range in the headline increases click-through rate from job board search results",
  variants: ["control: title only in headline", "variant: title + salary band in headline"],
  measurement: "Click-through rate and apply rate from job board impressions over 30-day posting window",
  expected_impact: "25% increase in click-through rate with no decrease in applicant quality"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="job-ad-writer",
  query="Latest data on job ad conversion rates by structure, length, and language patterns across LinkedIn, Indeed, and direct careers pages — 2024-2025 benchmarks by industry and role level",
  reason="Ensure job ad frameworks reflect current candidate behaviour, platform algorithm preferences, and high-converting structural patterns"
)
```

```
FutureProof:request_research(skill="job-ad-writer",
  query="Updated research on gendered and exclusionary language in job postings and its measurable impact on applicant diversity — post-2022 studies",
  reason="Keep the inclusion and bias audit methodology current with the latest applied linguistics and behavioural research"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="job-ad-writer", session={
  summary: "Crafted job ad for [role title] targeting [ICA persona] at [company/team], optimised for [primary channel]",
  key_findings: ["ICA attraction lever identified as [lever]", "Requirement list reduced from [X] to [Y] must-haves after calibration", "Bias audit flagged [N] language adjustments"],
  deliverables: ["Full job ad copy", "Channel-adapted variants", "ICA candidate persona card", "Bias & quality scorecard"],
  user_feedback: null
})
```