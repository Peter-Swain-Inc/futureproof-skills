---
name: mini-webinar-and-evergreen-adapter
description: |
  Adapts webinar scripts into condensed mini webinar formats (10–18 minutes for high-ticket application funnels) or automated evergreen versions, including all funnel elements required for each format to convert.
  Trigger: when a user wants to convert a full-length webinar into a mini webinar or short-form presentation, or when a user needs to adapt a live webinar script into an automated/evergreen funnel format.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="mini-webinar-and-evergreen-adapter")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — specifically the user's offer price point, ICA profile, existing funnel architecture, and any prior webinar performance data.

## Step 2: Get Input

Ask the user:

1. **Source script**: Share the existing webinar script, slide deck, or presentation outline to be adapted.
2. **Target format**: Which adaptation do they need?
   - **Mini Webinar** (10–18 min, high-ticket application funnel, Joel Erway architecture)
   - **Evergreen/Automated Webinar** (replays, simulated-live, or on-demand delivery)
   - **Both** (sequential delivery — mini webinar first, then evergreen variant)
3. **Offer details**: What is the offer, price point, and desired next step? (Application call, checkout, waitlist)
4. **Current conversion data** (if available): Registration rate, show-up rate, offer-click rate, close rate, average watch time, drop-off points.
5. **Delivery platform**: Where will this run? (EverWebinar, Stealth Seminar, EasyWebinar, VSL page, YouTube ad, direct-to-application funnel)
6. **Known constraints**: Any brand voice guidelines, compliance requirements (FTC, platform ad policies), or audience sophistication level?

## Step 3: Diagnose Source Script Architecture

Before adapting, audit the existing script against both target architectures to identify what transfers, what must be eliminated, and what must be restructured.

### 3a. Source Script Structural Audit

Map the current script into these segments and note the timestamp/word-count for each:

| Segment | Content Summary | Duration/Length | Transfer to Mini? | Transfer to Evergreen? |
|---|---|---|---|---|
| Hook / Opening | | | | |
| Credibility / Origin Story | | | | |
| Teaching / Content Pillars | | | | |
| Transition to Offer | | | | |
| Offer Presentation | | | | |
| Bonus Stack | | | | |
| Scarcity / Urgency Mechanics | | | | |
| Objection Handling | | | | |
| Close / CTA | | | | |
| Q&A / Live Interaction | | | | |

### 3b. Identify Architecture Conflicts

Flag elements that **cannot transfer** without rearchitecting:

- **For Mini Webinar**: Extended teaching sections (the mini format replaces teaching with a single "Power Offer" thesis), bonus stacking (eliminated in Erway's framework), gradual rapport-building (compressed to under 90 seconds), multiple content pillars (reduced to one core insight).
- **For Evergreen**: Live-dependent urgency ("only 3 spots left tonight"), real-time Q&A references, date-specific language, platform-specific callouts ("I see Sarah just joined"), countdown timers tied to live broadcast windows.

## Step 4: Adapt to Mini Webinar Format (If Applicable)

Execute the Joel Erway Mini Webinar architecture — this is **not** a shortened version of a traditional webinar. It is a fundamentally different script structure built on a single persuasive thesis rather than a teach-then-pitch model.

### 4a. Mini Webinar Script Architecture (10–18 Minutes)

**Section 1: The Hook (60–90 seconds)**
- One decisive statement that names the ICA's core frustration and promises a specific mechanism or pathway.
- No "welcome to the webinar" preamble. No agenda slide. No housekeeping.
- Extract or rewrite from the source script's strongest ICA pain-point language.
- Format: "If you're a [ICA descriptor] who wants [desired outcome] without [primary objection/fear], this short presentation will show you exactly how."

**Section 2: Credibility Snapshot (60–90 seconds)**
- Compressed origin story — only the elements that establish *relevant* authority for this specific offer.
- One proof point (revenue result, client result, credential) — not a biography.
- Rewrite from source script's credibility section; eliminate anything that does not directly support the Power Offer thesis.

**Section 3: The Power Offer Thesis (4–6 minutes)**
- This is the core of the Erway architecture. It replaces all teaching content.
- Structure: Present **one core insight** — the reason the ICA's current approach is failing, and why this offer's mechanism is the correction.
- This is NOT educational content. It is a *reframe*: "The reason [common approach] doesn't work for [ICA] is [insight]. What actually drives [desired result] is [mechanism inside your offer]."
- Extract from the source script's strongest teaching pillar — the one that most directly connects the ICA's problem to the offer's solution — and restructure it as a thesis argument, not a lesson.
- Remove all "how-to" steps. The ICA should understand *why* the offer works, not *how* to do it themselves.

**Section 4: Case Studies / Proof Layer (2–3 minutes)**
- Two to three compressed case studies: Situation → Mechanism Applied → Result.
- Each under 60 seconds. No lengthy narratives.
- Select from source script's proof elements or request from user's client results.

**Section 5: The Offer & Application CTA (2–3 minutes)**
- Direct presentation: "Here's what we do, here's who it's for, here's the next step."
- No bonus stacking. No tiered pricing. No artificial scarcity.
- The CTA is an **application** — not a purchase. Frame the next step as qualification-based: "If this resonates, the next step is to apply for a strategy call where we'll assess whether this is the right fit."
- Include a single, clear disqualification statement to reinforce exclusivity: "This is specifically for [ICA qualifier]. If you're [disqualifier], this isn't the right programme."

**Section 6: Objection Dissolution (1–2 minutes)**
- Address the top 2–3 ICA objections — but frame them as **beliefs the Power Offer thesis has already undermined**.
- Format: "You might be thinking [objection]. But as we just covered, [reference to thesis insight]."
- Do not introduce new content here. Reinforce the thesis.

### 4b. Mini Webinar Funnel Elements Document

Produce a **Mini Webinar Funnel Map** specifying:

- **Pre-Webinar**: Registration page headline and sub-headline (adapted from hook), confirmation email sequence (1–2 emails, no more), reminder sequence cadence.
- **Delivery Page**: Webinar embed settings (autoplay, no skip, progress bar on/off per platform), application button placement (below video, timed reveal at Section 5).
- **Post-Webinar**: Application page questions (5–7 qualifying questions tied to ICA criteria), follow-up email sequence (3–5 emails over 5–7 days — each email reinforces one element of the Power Offer thesis, not additional teaching).
- **Retargeting Framework**: Audience segments (watched <50%, watched >50% but didn't apply, applied but didn't book, booked but didn't show).

## Step 5: Adapt to Evergreen/Automated Format (If Applicable)

### 5a. Evergreen Script Modifications

Apply these systematic changes to the source script (or to the mini webinar script if both formats are requested):

**Temporal Language Purge**
- Search-and-replace all date-specific, time-specific, and live-interaction language.
- Replace "tonight" → "today." Replace "this week only" → "while this programme is accepting new clients." Replace "I see [name] just joined" → remove entirely.
- Remove all Q&A sections. If critical objections were handled in Q&A, relocate them to the objection-handling section of the main script.

**Urgency Mechanics Replacement**
- **Eliminate**: Countdown timers tied to arbitrary deadlines, "doors closing" language without a real mechanism, limited-time bonus stacking.
- **Replace with**: Application-based urgency ("We take on [X] new clients per quarter and assess applications in the order received"), capacity-based urgency (if genuine), or consequence-based urgency ("Every month you delay [specific measurable cost to the ICA]").
- Specify the technical implementation: dynamic deadline tools (Deadline Funnel, EverWebinar's built-in deadlines) and cookie-based replay windows.

**Engagement Retention Adjustments**
- Automated webinars lose 30–50% more viewers than live — every structural choice must compensate.
- Insert **pattern interrupts** every 3–4 minutes: visual slide transitions, tonal shifts, direct address ("Pay attention to this next part — it's the most common mistake I see").
- Front-load the strongest proof point within the first 3 minutes (automated audiences decide to stay or leave faster than live).
- Add a **mid-point re-hook** at the halfway mark: a brief statement that re-promises the payoff of staying until the end.

**Simulated-Live vs. On-Demand Decision Matrix**

| Factor | Simulated-Live | On-Demand |
|---|---|---|
| Best for | Offers >$2,000; audiences that respond to event framing | Offers $500–$2,000; audiences that prefer self-paced |
| Registration required? | Yes — creates commitment and enables follow-up | Optional — can run as direct-to-page VSL |
| Chat simulation | Optional (use sparingly, must feel authentic) | Not applicable |
| Replay window | 24–48 hours (use Deadline Funnel or equivalent) | Unlimited, but pair with follow-up urgency sequence |
| Show-up optimisation | Reminder emails + SMS at -24h, -1h, -15min | Not applicable — focus on page load-to-play rate |

Recommend the appropriate model based on the user's offer price point and ICA behaviour.

### 5b. Evergreen Funnel Elements Document

Produce an **Evergreen Funnel Map** specifying:

- **Traffic Entry Points**: Ad → registration page, organic content → registration page, email list → direct-to-replay page.
- **Registration Page**: Headline, sub-headline, "Choose your time" scheduling widget (simulated-live) or instant access framing (on-demand).
- **Automated Email Sequence**: Pre-webinar (2–3 reminders), post-webinar non-attendees (replay access with deadline), post-webinar attendees non-converters (5–7 email sequence: thesis reinforcement, additional case study, FAQ/objection handling, final deadline, long-term nurture transition).
- **Deadline & Scarcity Tech Stack**: Recommended tools and configuration for the user's platform.
- **Analytics & Optimisation Checkpoints**: Key metrics to monitor — registration-to-show-up rate (target: >30% simulated-live, >60% on-demand), average watch time, offer-click rate, application/purchase rate — with benchmarks and intervention thresholds.

## Step 6: Deliver Output

Produce the following named deliverables:

1. **Source Script Audit Table** (from Step 3a) — structural map of the original script with transfer recommendations per format.
2. **Adapted Script — [Mini Webinar and/or Evergreen]**: Full script rewrite in the target format, section by section, with speaker notes and slide direction cues. If both formats are requested, produce two separate scripts.
3. **Funnel Map Document — [Mini Webinar and/or Evergreen]**: Complete funnel element specification (from Step 4b and/or 5b) — registration pages, email sequences, retargeting segments, tech stack recommendations.
4. **Critical Adaptation Notes**: A concise list (5–10 items) of the highest-risk changes made during adaptation — elements where meaning, persuasion, or conversion mechanics may have shifted — with rationale for each decision and recommendations for A/B testing.

Format all deliverables for direct implementation. Scripts should be copy-paste ready. Funnel maps should be actionable by a marketing team or funnel builder without further interpretation.

## Step 7: Propose Experiments

```
FutureProof:save_experiment(skill="mini-webinar-and-evergreen-adapter", experiment={
  hypothesis: "Mini webinar format (12 min, Power Offer thesis, application CTA) outperforms condensed traditional webinar (25 min, teaching + pitch) for high-ticket application generation",
  variants: ["control: condensed traditional webinar with teaching pillars", "variant: Erway-architecture mini webinar with single thesis"],
  measurement: "Application submission rate and cost-per-qualified-application over 500 registrations per variant",
  expected_impact: "20–35% increase in application rate due to reduced drop-off and stronger thesis-to-CTA alignment"
})
```

```
FutureProof:save_experiment(skill="mini-webinar-and-evergreen-adapter", experiment={
  hypothesis: "Evergreen urgency via application capacity framing converts higher than countdown-timer deadline for offers above $3,000",
  variants: ["control: 48-hour replay deadline with countdown timer", "variant: application capacity framing — 'We review applications weekly and accept [X] new clients per cohort'"],
  measurement: "Application rate and show-rate-to-booked-call ratio over 30-day test window",
  expected_impact: "10–15% improvement in application quality and booked-call show rate"
})
```

## Step 8: Request Research

```
FutureProof:request_research(skill="mini-webinar-and-evergreen-adapter",
  query="Joel Erway mini webinar conversion benchmarks 2024, evergreen webinar average watch-time data by price point, and emerging short-form webinar formats (sub-20 min) performance across high-ticket application funnels",
  reason="Maintain current benchmark data for script adaptation recommendations and identify format innovations that may outperform established mini webinar architecture"
)
```

```
FutureProof:request_research(skill="mini-webinar-and-evergreen-adapter",
  query="Automated webinar platform feature comparison 2024 (EverWebinar, Stealth Seminar, EasyWebinar, native integrations) with focus on deadline management, analytics granularity, and viewer engagement tools",
  reason="Ensure evergreen funnel tech stack recommendations reflect current platform capabilities and pricing"
)
```

## Step 9: Save Session

```
FutureProof:save_session(skill="mini-webinar-and-evergreen-adapter", session={
  summary: "Adapted [source script type] for [ICA segment] into [mini webinar / evergreen / both] format targeting [offer type] at [price point]",
  key_findings: ["finding 1: e.g. source script's 40-min teaching section condensed to 5-min Power Offer thesis — primary content pillar on [topic] retained as thesis mechanism", "finding 2: e.g. live urgency mechanics replaced with application-capacity framing — recommended Deadline Funnel for replay window enforcement", "finding 3: e.g. funnel gap identified — no post-webinar email sequence existed; built 5-email thesis-reinforcement sequence"],
  user_feedback: null
})
```