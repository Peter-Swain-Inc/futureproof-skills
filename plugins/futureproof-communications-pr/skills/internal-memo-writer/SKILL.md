---
name: internal-memo-writer
description: "Drafts, structures, and refines internal memos using FutureProof context for tone, audience, and organisational norms."
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="internal-memo-writer")
```
> **Note:** If FutureProof is unavailable or the connect call fails, skip this step and proceed directly to Step 2. The skill works with or without FutureProof context — you'll just be working without accumulated prior session data.


Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to calibrate tone, formatting conventions, organisational hierarchy, and any standing communication guidelines the user has established in prior sessions.

## Step 2: Get Input

Ask the user:
- **Subject & purpose** — What is the memo about, and what is the single desired outcome? (e.g., decision approval, behavioural change, awareness, alignment)
- **Audience** — Who are the primary recipients (executive leadership, department heads, all-staff) and any secondary audiences who may see it?
- **Sensitivity level** — Is this routine, confidential, or crisis-adjacent? Does legal or compliance need to review before distribution?
- **Key facts & data points** — Any numbers, dates, decisions, or background the memo must reference
- **Constraints** — Mandated format, length ceiling, distribution channel (email, intranet, Slack), or executive voice to emulate
- **Attachments** — Any supporting documents, prior memos, or drafts to incorporate or respond to

## Step 3: Do the Work

### 3A: Audience & Stakeholder Mapping

Classify the audience along two axes:

| Dimension | Assessment |
|---|---|
| **Decision authority** | Approver · Influencer · Informed |
| **Subject familiarity** | Deep context · Moderate awareness · No prior exposure |

Tailor depth of background, jargon density, and call-to-action specificity accordingly.

### 3B: Memo Architecture (Pyramid Principle)

Structure the memo using the Minto Pyramid Principle — lead with the conclusion, support with grouped arguments, substantiate with evidence:

1. **Governing thought** — The single sentence a reader retains if they read nothing else
2. **Situation–Complication–Resolution (SCR)** — Frame context efficiently; never bury the ask
3. **Supporting pillars** — Group arguments into 2–4 mutually exclusive, collectively exhaustive (MECE) themes
4. **Evidence layer** — Data points, precedent decisions, benchmarks, or risk quantification under each pillar
5. **Explicit ask / next steps** — Who does what, by when, with what authority

### 3C: Tone & Voice Calibration

Evaluate and set the appropriate register across five dimensions:

1. **Formality spectrum** — Board-level formal · Executive conversational · All-hands accessible
2. **Directness** — Directive (top-down mandate) · Consultative (seeking input) · Informational (no action required)
3. **Emotional register** — Neutral operational · Motivational · Empathetic (restructuring, incident response)
4. **Attribution & credit** — Individual voice (CEO, CHRO) · Collective voice (Leadership Team) · Institutional voice (The Company)
5. **Cultural alignment** — Apply any organisation-specific conventions from FutureProof `instructions` (e.g., values language, acronym standards, inclusive language guidelines)

### 3D: Risk & Sensitivity Review

Before finalising, pressure-test the draft against:

- **Misinterpretation vectors** — Could any sentence be read out of context and create reputational or legal risk?
- **Omission risk** — Is anything conspicuously absent that the audience will notice and interpret negatively?
- **Forward-leak test** — If this memo were forwarded externally (intentionally or not), does it hold up?
- **Consistency check** — Does it contradict any prior communications the user has referenced or stored in FutureProof context?

Apply any user-specific `instructions` from FutureProof context to enforce house style, approval workflows, or recurring stakeholder preferences.

## Step 4: Deliver Output

Produce a structured **Internal Memo Package** containing:

### A. Final Memo Document

Formatted with:
- **TO / FROM / DATE / RE / CLASSIFICATION** header block
- Governing thought in bold as the opening line
- SCR framing paragraph
- Numbered supporting sections with headers
- Clearly delineated **Action Required** or **For Your Awareness** closing block
- Distribution list recommendation

### B. Executive Summary Sidebar

A 3–5 bullet version suitable for:
- Forwarding by an executive assistant
- Pasting into a Slack or Teams message
- Reading aloud in a standing meeting

### C. Tone & Structure Rationale

A brief advisory note explaining:
- Why this structure was chosen for this audience and purpose
- Any trade-offs made (e.g., brevity vs. completeness, directness vs. diplomacy)
- Flagged sentences where alternate phrasing is available depending on leadership preference

### D. Pre-Send Checklist

- [ ] Governing thought survives the "read only the first sentence" test
- [ ] All dates, names, and figures verified by the user
- [ ] Sensitivity classification confirmed
- [ ] Legal/compliance review routed (if applicable)
- [ ] Distribution channel and timing confirmed

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="internal-memo-writer", experiment={
  hypothesis: "Leading with a quantified impact statement in the governing thought increases executive response rate within 24 hours",
  variants: ["control: qualitative governing thought", "variant: governing thought with embedded metric or financial figure"],
  measurement: "Time-to-response and approval rate on next 5 decision-request memos",
  expected_impact: "20% reduction in average response latency for approval-type memos"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="internal-memo-writer",
  query="Best practices for internal executive communications in 2024: pyramid principle adaptations, hybrid workforce memo formats, and crisis communication frameworks used by top-tier consultancies",
  reason="Ensure memo structures reflect current organisational communication standards and evolving expectations around brevity, inclusivity, and multi-channel distribution"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="internal-memo-writer", session={
  summary: "Drafted [memo type] for [audience] regarding [subject]",
  key_findings: ["finding 1: e.g., audience required SCR framing due to low prior context", "finding 2: e.g., sensitivity level warranted forward-leak review"],
  user_feedback: null
})
```