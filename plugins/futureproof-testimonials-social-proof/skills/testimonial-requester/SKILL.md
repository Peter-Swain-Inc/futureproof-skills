---
name: testimonial-requester
description: "Crafts strategic testimonial request sequences that maximise response rates and extract high-impact social proof from clients and customers."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="testimonial-requester")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly ICA segments, offer details, known transformation outcomes, and any previously successful testimonial language.

## Step 2: Get Input

Ask the user:
- **Who are you requesting testimonials from?** (specific client segment, cohort, programme completers, recent purchasers — map to ICA if context available)
- **What is the core transformation or result these clients experienced?** (before state → after state)
- **What format do you need?** (written testimonial, video prompt script, case study interview questions, LinkedIn recommendation request, review platform submission)
- **Where will the testimonials be deployed?** (sales page, pitch deck, proposal, email sequence, social media, case study library)
- **What is the relationship temperature?** (warm/active client, past client re-engagement, post-onboarding, post-delivery)
- **Any previous testimonial requests that underperformed or went unanswered?**

## Step 3: Map the Testimonial Strategy

Before drafting, build a **Testimonial Extraction Framework** tailored to the user's situation:

### 3a. Segment & Prioritise Recipients

Rank testimonial candidates across three dimensions:

| Dimension | Weight | Criteria |
|-----------|--------|----------|
| **Result magnitude** | 40% | Measurable outcome achieved (revenue, time saved, transformation depth) |
| **ICA representativeness** | 35% | How closely the client mirrors the target ICA — prospects must see themselves in the testimonial |
| **Relationship equity** | 25% | Likelihood of response based on recency, satisfaction signals, and engagement history |

Produce a **prioritised outreach list** of up to 10 recipients, segmented into Tier 1 (high-value, request immediately), Tier 2 (strong candidates, batch outreach), and Tier 3 (opportunistic, lower priority).

### 3b. Select the Optimal Request Mechanism

Match each tier to the highest-conversion request method:

1. **Direct personal ask** (video call or voice memo) — Tier 1, relationship equity > 8/10
2. **Personalised email with guided prompts** — Tier 1–2, scalable but high-touch
3. **Structured questionnaire** (5–7 targeted questions) — Tier 2–3, lowers friction for less engaged clients
4. **Reciprocity-anchored request** (paired with value delivery — resource, introduction, insight) — re-engagement of lapsed clients
5. **Automated post-milestone trigger** (systemised request at peak satisfaction moment) — ongoing collection infrastructure

### 3c. Define the Proof Architecture

Identify which **proof type** each testimonial should target based on deployment context:

- **Outcome proof** — specific, quantified results ("increased revenue by 42% in 90 days")
- **Process proof** — credibility of the methodology ("the framework was rigorous and immediately actionable")
- **Identity proof** — ICA resonance ("as a solo founder with no marketing team, this was built for me")
- **Objection-neutralising proof** — pre-empts the top 3 ICA objections ("I was sceptical about the price, but ROI was evident within 2 weeks")
- **Authority proof** — credential transfer ("recommended by [notable company/title]")

## Step 4: Craft the Testimonial Request Sequence

Produce the following deliverables:

### Deliverable 1: Primary Request Message

A personalised outreach message (email, DM, or voice memo script) that includes:

1. **Gratitude anchor** — specific reference to the shared experience (not generic "thanks for being a client")
2. **Result reflection** — mirror back the transformation the client achieved, using their own language where possible
3. **The ask** — framed as helping others like them make the decision, not as a favour to the business
4. **Guided prompts** — 3–5 specific questions designed to extract the proof type identified in Step 3c
5. **Friction reducer** — explicit permission to keep it brief (2–3 sentences), offer to draft based on their bullet points, or provide a fill-in-the-blank template
6. **Logistics clarity** — where to reply, estimated time commitment (under 5 minutes), and how it will be used (with approval)

**Guided prompt questions must follow the STAR-T framework:**
- **S**ituation — "What was happening in your business/life before we worked together?"
- **T**ask — "What were you trying to solve or achieve?"
- **A**ction — "What specifically did we do together that made the difference?"
- **R**esult — "What measurable or tangible outcome did you experience?"
- **T**ransformation — "How would you describe the before vs. after?"

### Deliverable 2: Follow-Up Sequence

A 2-touch follow-up cadence:

- **Follow-up 1** (5–7 days): lighter touch, reframe the ask, offer alternative format (e.g., "happy to jump on a 5-minute call and capture it for you")
- **Follow-up 2** (10–14 days): final nudge with an easy-exit option ("completely understand if timing doesn't work — would it be okay if I drafted something based on our results and sent it for your approval?")

### Deliverable 3: Ghost-Drafted Testimonial Template

For clients who agree but never follow through, provide a **pre-written testimonial draft** based on known results that the client can approve, edit, or personalise. Structure:

> "[Pain/situation before]. [What we did together]. [Specific result achieved]. [Who I'd recommend this to]."

### Deliverable 4: Testimonial Deployment Map

A one-page matrix showing:

| Testimonial | Proof Type | Deployment Location | ICA Segment Served | Objection Neutralised |
|-------------|-----------|--------------------|--------------------|----------------------|
| Client A | Outcome | Sales page hero | [Segment] | Price sensitivity |
| Client B | Identity | Email sequence | [Segment] | "Not for people like me" |

## Step 5: Quality & Compliance Review

Evaluate all drafted materials against:

1. **Authenticity** — does it sound like the client, not the marketer? Flag any language that reads as manufactured
2. **Specificity density** — every testimonial must contain at least one concrete metric, timeframe, or named outcome
3. **Legal & ethical compliance** — include consent language, confirm permission for name/likeness use, note any industry-specific disclosure requirements (FTC, ASA, GDPR)
4. **ICA mirror test** — would the target ICA read this testimonial and think "that person is exactly like me"?
5. **Objection coverage audit** — cross-reference collected proof types against the user's top 3 known ICA objections to identify gaps

Produce a **Coverage Scorecard**:

| Proof Type | Covered? | Gap Action |
|-----------|----------|------------|
| Outcome proof | ✓ / ✗ | [Specific next request to close gap] |
| Process proof | ✓ / ✗ | |
| Identity proof | ✓ / ✗ | |
| Objection-neutralising proof | ✓ / ✗ | |
| Authority proof | ✓ / ✗ | |

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="testimonial-requester", experiment={
  hypothesis: "Sending a ghost-drafted testimonial for client approval yields 2x higher completion rate than open-ended request prompts",
  variants: ["control: guided prompt questions only", "variant: ghost-drafted testimonial sent for approval/editing"],
  measurement: "testimonial completion rate and time-to-response across next 20 requests",
  expected_impact: "60% increase in testimonial collection rate, 50% reduction in average response time"
})
```

```
FutureProof:save_experiment(skill="testimonial-requester", experiment={
  hypothesis: "Requesting testimonials within 48 hours of a measurable client win produces more specific, result-dense proof than requests sent 30+ days post-engagement",
  variants: ["control: standard post-project request", "variant: triggered request within 48 hours of documented result"],
  measurement: "specificity score (metrics per testimonial) and response rate across next 15 requests per variant",
  expected_impact: "35% increase in testimonials containing quantified outcomes"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="testimonial-requester",
  query="Highest-converting testimonial formats and placement strategies 2024–2025, including video vs. written response rates, optimal testimonial length for sales pages, and emerging social proof patterns in B2B and DTC",
  reason="Ensure request formats and deployment recommendations reflect current buyer trust psychology and platform-specific conversion benchmarks"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="testimonial-requester", session={
  summary: "Built testimonial request strategy for [ICA segment] across [number] client recipients, targeting [proof types] for deployment on [locations]",
  key_findings: ["finding 1: coverage gaps identified in [proof type]", "finding 2: highest-priority request sent to [Tier 1 client] using [method]", "finding 3: ghost-draft template created for [number] lapsed respondents"],
  user_feedback: null
})
```