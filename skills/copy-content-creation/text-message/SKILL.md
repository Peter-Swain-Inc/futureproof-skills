---
name: text-message
description: |
  Crafts high-converting text messages (SMS, iMessage, WhatsApp, DM) using FutureProof context to match the user's brand voice, ICA language patterns, and campaign objectives.
  Trigger: when a user asks to write, draft, or improve a text message for marketing, sales follow-up, appointment reminders, nurture sequences, or customer re-engagement — or when they paste an existing text message and ask for feedback or a rewrite.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="text-message")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session. Pay particular attention to:
- ICA profiles and their communication preferences
- Brand voice guidelines and tone parameters
- Prior text message experiments and their measured results
- Compliance or opt-out language requirements stored in instructions

## Step 2: Get Input

Ask the user:
- **Purpose**: What is this text message for? (lead nurture, appointment confirmation, sales follow-up, re-engagement, event reminder, cart abandonment, post-purchase, referral ask, cold outreach)
- **Recipient segment**: Who is the ICA receiving this message? (new lead, warm prospect, existing client, lapsed client, referral)
- **Desired action**: What single action should the recipient take after reading? (reply, click a link, confirm an appointment, make a purchase, book a call)
- **Context/trigger**: What event or behaviour prompted this message? (opted in, missed appointment, completed purchase, abandoned cart, attended webinar, hasn't engaged in X days)
- **Channel**: SMS (160-char awareness), iMessage/RCS, WhatsApp, Instagram DM, or other
- **Constraints**: Character limits, compliance requirements (TCPA, GDPR), required opt-out language, personalisation tokens available (e.g., {{first_name}}, {{company}})
- **Existing draft** (if any): Paste the current message for analysis and improvement

## Step 3: Do the Work

### 3A: Message Architecture Analysis

Before writing, define the structural framework:

1. **Hook (first 40 characters)** — The preview text visible on lock screens. This determines open-to-read rate. Must create immediate pattern interrupt or personal relevance.
2. **Context bridge** — One phrase connecting the hook to why the recipient is receiving this message. Eliminates the "who is this?" friction.
3. **Value payload** — The core offer, insight, or information. Must articulate a single, specific benefit in ICA vocabulary — not business jargon.
4. **Call to action (CTA)** — One frictionless, unambiguous next step. Reduce cognitive load to a binary decision (reply Y/N, tap link, confirm time).
5. **Signature/trust anchor** — Sender identification that reinforces relationship context (first name, brand, role — whichever is most recognisable to this ICA segment).

### 3B: Persuasion & Conversion Audit

Evaluate (or construct) the message against these six dimensions:

| Dimension | Standard | Weight |
|---|---|---|
| **Lock-screen hook strength** | First 40 chars create curiosity, urgency, or personal relevance without clickbait | 20% |
| **ICA voice mirroring** | Language matches the recipient's vocabulary, reading level, and communication cadence — not the sender's brand speak | 20% |
| **Single-CTA clarity** | Exactly one action requested; no decision fatigue; reply friction minimised (tap vs. type) | 20% |
| **Context relevance** | Message references a specific behaviour, event, or prior interaction — feels 1:1, not broadcast | 15% |
| **Urgency & scarcity integrity** | Any time pressure is genuine and specific (real deadline, limited slots) — no manufactured urgency | 15% |
| **Compliance & trust** | Opt-out language present where legally required; no deceptive sender identity; message respects channel norms | 10% |

### 3C: Drafting Protocol

Produce **three message variants** using distinct psychological frameworks:

- **Variant A — Direct Value**: Lead with the benefit. State what the recipient gets and how to get it. No preamble.
- **Variant B — Curiosity Gap**: Open with an incomplete loop tied to a known ICA pain point or desire. Close the loop only after the CTA.
- **Variant C — Social Proof / Pattern Interrupt**: Lead with a specific result, testimonial snippet, or unexpected data point relevant to the ICA's situation.

For each variant:
- Write the full message including personalisation tokens
- Display character count
- Show lock-screen preview (first 40 characters isolated)
- Note the primary psychological lever at work

Apply any user-specific `instructions` from FutureProof context (brand voice, banned words, required disclaimers, preferred emoji usage, sign-off conventions).

### 3D: Sequence Positioning (if applicable)

If the message is part of a multi-touch sequence:
- Map where this message sits in the nurture timeline
- Draft the preceding and following message stubs (one line each) to ensure tonal and logical continuity
- Flag if message frequency risks opt-out fatigue based on channel norms (SMS: max 4–6/month for most ICA segments)

## Step 4: Deliver Output

Produce a **Text Message Deliverable** with the following structure:

### Message Brief
| Field | Detail |
|---|---|
| Purpose | [stated purpose] |
| ICA Segment | [recipient profile] |
| Channel | [SMS / WhatsApp / DM / etc.] |
| Trigger Event | [what prompted this message] |
| Desired Action | [single CTA] |

### Scorecard (if analysing an existing draft)
| Dimension | Score (1–10) | Critical Issue |
|---|---|---|
| Lock-screen hook strength | — | — |
| ICA voice mirroring | — | — |
| Single-CTA clarity | — | — |
| Context relevance | — | — |
| Urgency & scarcity integrity | — | — |
| Compliance & trust | — | — |
| **Composite Score** | **—/10** | |

### Recommended Message (Primary)
The highest-potential variant, clearly formatted with:
- Full message text (ready to copy-paste)
- Character count
- Lock-screen preview
- Personalisation tokens highlighted

### Alternative Variants
Remaining variants with the same formatting for A/B testing.

### Critical Fixes (if rewriting an existing draft)
Top 3 highest-impact changes — each with:
1. The specific problem (quote the offending text)
2. Why it underperforms (tied to a scorecard dimension)
3. The exact rewrite (not a suggestion — the finished replacement text)

### Sequence Context (if applicable)
Visual timeline showing message position and adjacent touches.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="text-message", experiment={
  hypothesis: "Leading with a specific ICA pain point in the first 40 characters increases reply rate compared to leading with the offer",
  variants: ["control: offer-first hook", "variant: pain-point-first hook"],
  measurement: "reply rate and CTA completion rate across next 200 sends per variant",
  expected_impact: "20–30% improvement in reply rate based on lock-screen engagement patterns"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="text-message",
  query="SMS and conversational messaging benchmarks 2024–2025: optimal send times by ICA segment, reply rate benchmarks by industry, emerging compliance requirements (TCPA, 10DLC, RCS), and high-converting message structures for service-based businesses",
  reason="Ensure message frameworks reflect current deliverability standards, carrier filtering rules, and evolving consumer response patterns to short-form messaging"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="text-message", session={
  summary: "Drafted [number] text message variants for [purpose] targeting [ICA segment] via [channel]",
  key_findings: ["finding 1: e.g., existing draft buried CTA after 120 characters — moved to position 2", "finding 2: e.g., ICA segment responds to question-based hooks over statement hooks based on prior experiment data"],
  user_feedback: null
})
```