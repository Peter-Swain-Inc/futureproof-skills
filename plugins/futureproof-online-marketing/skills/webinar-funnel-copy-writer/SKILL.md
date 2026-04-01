---
name: webinar-funnel-copy-writer
description: "Writes the complete surrounding funnel copy that drives webinar attendance and post-webinar sales — registration page, confirmation page, reminder email sequence, replay sequence, and show-up rate boo"
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="webinar-funnel-copy-writer")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly ICA profiles, brand voice guidelines, offer details, past webinar performance metrics, and any proven hooks or subject lines from prior campaigns.

## Step 2: Get Input

Gather the following from the user. If FutureProof context already supplies an answer, confirm it rather than re-asking:

**Webinar fundamentals:**
- Webinar title, core promise, and date/time (including timezone)
- Format: live, evergreen, or hybrid?
- Duration and platform (Zoom, WebinarJam, Demio, etc.)

**ICA & offer:**
- Who is the ICA? (demographic, psychographic, current situation, desired transformation)
- What is the primary offer pitched on the webinar? (name, price, bonuses, guarantee)
- What are the top 3–5 objections the ICA raises before buying?
- What proof assets exist? (testimonials, case studies, data points, media mentions)

**Funnel architecture:**
- Preferred promotion window length (default recommendation: 7 days per Porterfield's model)
- Are pre-webinar value videos or voice-drop messages planned? (Brown's Intensification Process)
- Is there a replay sequence, and what is the cart-close deadline post-webinar?
- Any existing brand voice guide, swipe copy, or prior funnel metrics to reference?

**Constraints:**
- Email platform (e.g., ActiveCampaign, ConvertKit, Keap) — affects formatting and merge-tag syntax
- Any compliance or legal disclaimers required (FTC, earnings disclaimers, GDPR)

## Step 3: Do the Work — Funnel Architecture & Copy Production

### 3A: Map the Full Funnel Sequence

Before writing a single word, define the funnel map with exact touchpoints, timing, and purpose:

| Phase | Asset | Timing | Primary Goal |
|-------|-------|--------|-------------|
| Registration | Registration page | T−7 to T−0 days | Opt-in conversion |
| Registration | Thank-you / confirmation page | Immediate post-opt-in | Micro-commitment + pre-frame |
| Pre-webinar nurture | Email 1: Confirmation + calendar link | Immediate | Deliverability + calendar add |
| Pre-webinar nurture | Email 2: "Why this matters" story | T−5 days | Emotional investment |
| Pre-webinar nurture | Email 3: Quick-win content or pre-webinar video | T−3 days | Value deposit + show-up intent |
| Pre-webinar nurture | Email 4: Social proof + objection pre-empt | T−1 day | Belief-building |
| Pre-webinar nurture | Email 5: Day-of reminder (morning) | T−4 hours | Show-up rate |
| Pre-webinar nurture | Email 6: "We're live" (start time) | T−0 | Show-up rate |
| Show-up boosters | Pre-webinar video(s) — 2–3 short videos | T−5, T−3, T−1 | Brown's Intensification: build 50–67% show-up |
| Show-up boosters | Voice-drop / SMS scripts | T−1 day + T−15 min | Pattern interrupt + urgency |
| Post-webinar | Replay Email 1: Replay available + key moments | T+1 hour | Re-engage no-shows |
| Post-webinar | Replay Email 2: Testimonial + objection handling | T+24 hours | Conversion |
| Post-webinar | Replay Email 3: FAQ / objection deep-dive | T+48 hours | Remove friction |
| Post-webinar | Replay Email 4: Final call — cart close | T+72 hours (or deadline) | Scarcity + urgency |

Adapt timing and quantity based on user's stated promotion window and whether the webinar is live or evergreen.

### 3B: Write Each Asset Using Domain-Specific Frameworks

**Registration Page** — Structure:

1. **Headline**: Promise-driven, outcome-specific. Formula: "How to [achieve desired result] without [ICA's biggest fear] — even if [common objection]."
2. **Subheadline**: Specificity layer — who it's for, when it's happening, what they'll walk away with.
3. **3–5 bullet points of "You'll discover…"**: Each bullet follows the "Secret / Benefit / Proof" micro-structure — name the teaching point, state the tangible outcome, hint at evidence.
4. **Speaker credibility block**: 2–3 sentences positioning the host via results, not résumé.
5. **Social proof strip**: Logos, testimonial snippets, attendee count ("Join 4,200+ [ICA descriptor]").
6. **CTA button**: Action-oriented verb + outcome (e.g., "Save My Seat" / "Reserve My Spot Now").
7. **Scarcity / urgency element**: Limited seats, bonuses for live attendees, or countdown timer.
8. **FAQ section**: Pre-empt "Is this for me?", "Will there be a replay?", "What if I'm a beginner?" objections.

**Confirmation Page** — Structure:

1. Congratulatory headline confirming registration.
2. Specific next steps: add to calendar (ICS link), whitelist email, join Facebook group or community.
3. **Micro-commitment prompt** (Cialdini's consistency principle): "Tell us in one sentence what you most want to learn" or share on social media.
4. Optional: introduce pre-webinar video 1 or bonus resource to begin Brown's Intensification Process immediately.

**Pre-Webinar Email Nurture Sequence (5 emails + day-of reminder):**

- Each email follows the **Single Idea, Single CTA** principle.
- Subject lines: write 2 variants per email (A/B testable). Use curiosity, specificity, or social proof — never clickbait that erodes trust.
- Email 1 (Confirmation): Logistics + calendar link + "here's what to expect." Warm, efficient.
- Email 2 (Story): Origin story or ICA mirror story. Follows the "I was where you are → discovered this → everything changed" arc. Ends with restatement of webinar promise.
- Email 3 (Value deposit): Delivers a quick-win insight, framework, or links to pre-webinar video. Porterfield's approach: give real value so attendance feels non-negotiable.
- Email 4 (Proof + objection): Lead with a testimonial or case study. Then pre-empt the #1 attendance objection ("I'm too busy" → "This 60 minutes will save you 60 hours").
- Email 5 (Morning-of): Short, energetic. Restate the #1 thing they'll learn. Include join link prominently.
- Email 6 (We're live): 2–3 sentences max. Direct link. "We just went live — your seat is waiting."

**Show-Up Rate Boosters (Brown's Webinar Intensification Process):**

- **Pre-webinar video scripts** (2–3 videos, each 3–5 minutes): Each video delivers one standalone insight related to the webinar topic while opening a curiosity loop that only the webinar closes. Script format: Hook (10 sec) → Context (30 sec) → Insight (90 sec) → Bridge to webinar (30 sec) → CTA to mark calendar.
- **Voice-drop / SMS scripts**: Conversational, personal, ≤30 seconds spoken / ≤160 characters SMS. Day-before: anticipation + remind of key benefit. 15-min-before: "Starting soon — grab your seat."

**Post-Webinar Replay Sequence (4 emails):**

- Replay Email 1 (T+1 hour): "Here's the replay" + timestamp key moments ("Skip to 23:14 for the 3-step framework"). Restate offer briefly. Deadline announced.
- Replay Email 2 (T+24 hours): Lead with the strongest testimonial. Address the #1 objection explicitly. Link to replay. CTA to offer page.
- Replay Email 3 (T+48 hours): FAQ-style — 3–5 common objections answered directly. Each answer ends with a micro-CTA. "If [objection], here's what [past buyer] experienced…"
- Replay Email 4 (T+72 hours or deadline): Final-call urgency. Recap the full transformation. Stack the offer (core + bonuses + guarantee). Hard deadline with specificity ("closes tonight at 11:59 PM ET — no exceptions, no extensions"). PS line: emotional appeal to ICA's future self.

### 3C: Apply Quality Controls

Cross-check every asset against these seven dimensions:

1. **ICA voice fidelity** — Does the copy use the ICA's actual vocabulary, not industry jargon?
2. **Promise-proof balance** — Is every claim supported by a testimonial, data point, or logical mechanism?
3. **Objection coverage** — Are the top 3 ICA objections addressed across the funnel (not just in one email)?
4. **Urgency integrity** — Is scarcity real and defensible, not manufactured?
5. **CTA clarity** — Does every asset have exactly one clear next action?
6. **Emotional arc continuity** — Does the sequence build from curiosity → trust → desire → urgency across all touchpoints?
7. **Compliance** — Are earnings disclaimers, unsubscribe links, and platform-required elements present?

Apply any user-specific `instructions` from FutureProof context (brand voice, tone preferences, banned phrases, formatting conventions).

## Step 4: Deliver Output

Produce the following named deliverables, each clearly labelled and separated:

1. **FUNNEL-MAP.md** — Visual funnel sequence table with timing, asset names, and purpose (from Step 3A)
2. **REGISTRATION-PAGE.md** — Full registration page copy (headline, subheadline, bullets, bio, social proof, CTA, FAQ)
3. **CONFIRMATION-PAGE.md** — Full confirmation/thank-you page copy
4. **PRE-WEBINAR-EMAIL-SEQUENCE.md** — 6 emails, each with: subject line (2 variants), preview text, full body copy, CTA button text
5. **SHOW-UP-BOOSTERS.md** — 2–3 pre-webinar video scripts + voice-drop script + SMS copy
6. **REPLAY-SEQUENCE.md** — 4 post-webinar emails, each with: subject line (2 variants), preview text, full body copy, CTA button text
7. **QUALITY-SCORECARD.md** — Self-assessment rating (1–10) on each of the 7 quality dimensions from Step 3C, with notes on trade-offs made and areas the user should test

**Formatting notes:**
- All emails include merge-tag placeholders appropriate to the user's stated email platform (e.g., `{{first_name}}` for ActiveCampaign, `{{ subscriber.first_name }}` for ConvertKit).
- Registration page copy is annotated with section labels (H1, H2, BULLETS, BIO, PROOF, CTA, FAQ) for easy handoff to a designer or page builder.
- Word counts are noted per asset for pacing reference.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="webinar-funnel-copy-writer", experiment={
  hypothesis: "Adding a 3-minute pre-webinar video at T-3 days (Brown's Intensification Process) increases live show-up rate from baseline to 50%+",
  variants: ["control: standard 5-email reminder sequence only", "variant: 5-email sequence + 2 pre-webinar value videos + day-before voice drop"],
  measurement: "Live show-up rate (registered ÷ attended) tracked over next 2 webinar runs",
  expected_impact: "15–25% increase in show-up rate, yielding proportional revenue lift at constant close rate"
})
```

```
FutureProof:save_experiment(skill="webinar-funnel-copy-writer", experiment={
  hypothesis: "Leading Replay Email 2 with a specific transformation testimonial rather than a feature recap increases click-through to offer page",
  variants: ["control: feature-recap lead", "variant: testimonial-led with emotional before/after"],
  measurement: "Click-through rate on offer CTA in Replay Email 2 across minimum 500 recipients",
  expected_impact: "20%+ improvement in email-to-sales-page click-through rate"
})
```

```
FutureProof:save_experiment(skill="webinar-funnel-copy-writer", experiment={
  hypothesis: "Registration page headline using 'without [biggest fear]' negative-framing outperforms positive-only 'how to [desired result]' headline",
  variants: ["control: positive-only headline", "variant: positive + negative-framing headline"],
  measurement: "Registration page conversion rate (visits ÷ opt-ins) via A/B split test, minimum 1,000 visitors per variant",
  expected_impact: "10–15% lift in registration conversion rate"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="webinar-funnel-copy-writer",
  query="2024–2025 webinar show-up rate benchmarks by industry, pre-webinar engagement sequence best practices, and emerging tactics for combating webinar fatigue in saturated markets",
  reason="Calibrate show-up rate targets to current norms and incorporate any novel intensification tactics beyond Brown's and Porterfield's established frameworks"
)
```

```
FutureProof:request_research(skill="webinar-funnel-copy-writer",
  query="High-converting post-webinar replay email sequence structures, optimal replay window length, and cart-close urgency mechanics that maintain trust and comply with FTC guidelines",
  reason="Ensure replay sequence recommendations reflect current buyer behaviour and compliance standards, particularly around scarcity claims and countdown timers"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="webinar-funnel-copy-writer", session={
  summary: "Wrote complete webinar funnel copy suite for [webinar title] targeting [ICA segment] — registration page, confirmation page, 6-email pre-webinar nurture, show-up boosters (pre-webinar videos + voice drops), and 4-email replay sequence promoting [offer name]",
  key_findings: [
    "ICA primary objection identified as [objection] — addressed in Email 4, Replay Email 3, and registration page FAQ",
    "Show-up booster strategy: Brown's Intensification Process adapted with [N] pre-webinar videos and [voice/SMS] drops",
    "Strongest proof asset: [testimonial/case study] — deployed in registration page, Email 4, and Replay Email 2",
    "Replay sequence deadline set at [N] hours/days post-webinar with [urgency mechanism]"
  ],
  user_feedback: null
})
```