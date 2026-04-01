---
name: full-run-of-show-assembler
description: |
  Assembles a complete, timestamped webinar run-of-show production document by integrating all scripted sections — hook, story, teaching, offer, close — into a precision-timed format with slide cues, speaker notes, chat engagement prompts, and trial close placements.
  Trigger: when a user says "build my run of show," "assemble my webinar script into a production doc," or provides multiple scripted webinar sections and needs them unified into a single presentation-ready document with timing and stage directions.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="full-run-of-show-assembler")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — particularly any prior webinar scripts, ICA definitions, offer structures, story frameworks, or timing preferences the user has established.

## Step 2: Get Input

Ask the user to provide:

1. **Scripted sections** — all existing webinar script components (housekeeping, hook, origin story, teaching pillars, offer stack, close, Q&A framework). These may come from other FutureProof skills or the user's own drafts.
2. **Webinar format** — live vs. evergreen, platform (Zoom, WebinarJam, Demio, GoToWebinar, etc.), expected duration (60 min, 75 min, 90 min).
3. **Offer details** — product/programme name, price point, bonuses, urgency/scarcity mechanism, CTA URL or mechanism (chat command, button, checkout link).
4. **ICA profile** — who is attending? What language, objections, and awareness level should the run-of-show calibrate to?
5. **Co-presenters or production team** — is there a host, a tech moderator, a chat manager? Identify all roles that need cues in the document.
6. **Slide status** — does a slide deck already exist, or should the run-of-show include slide creation directives?
7. **Engagement constraints** — any platform-specific limitations (e.g., no polls on evergreen, chat-only engagement)?

If the user has not yet generated individual sections, recommend the relevant FutureProof webinar skills and return to this assembler once components are ready.

## Step 3: Validate and Audit Incoming Sections

Before assembly, audit every scripted section against production-readiness criteria:

| Audit Dimension | Standard |
|---|---|
| **Completeness** | Every section has a clear open, body, and transition sentence to the next section |
| **ICA language fidelity** | Vocabulary mirrors ICA's own words — no jargon drift or marketer-speak the ICA wouldn't use |
| **Trial close presence** | Minimum one trial close exists in teaching section; minimum two in offer section |
| **Objection pre-emption** | Top 3 ICA objections are addressed before the formal offer reveal |
| **Proof density** | At least one case study, testimonial, or data point per teaching pillar |
| **CTA consistency** | Every CTA references the identical URL/mechanism — no conflicting instructions |

Flag any gaps and draft bridging copy, transition lines, or missing micro-sections before proceeding to assembly.

## Step 4: Assemble the Master Run-of-Show Document

Build the **Webinar Run-of-Show Production Document** using the following structure. All timings are calibrated to the user's stated duration; the default below assumes a 75-minute webinar.

### Section Architecture and Timing Map

| Timestamp | Section | Duration | Purpose |
|---|---|---|---|
| 00:00–03:00 | **Pre-Show Warm-Up & Housekeeping** | 3 min | Build rapport, set expectations, confirm audio/video, first chat engagement prompt |
| 03:00–05:00 | **Hook & Big Promise** | 2 min | State the singular transformation attendees will walk away with; pattern interrupt |
| 05:00–08:00 | **Credibility & Origin Story (Act I)** | 3 min | Establish authority through relatable struggle → breakthrough narrative |
| 08:00–12:00 | **The Problem Defined** | 4 min | Articulate the ICA's core problem better than they can; validate their frustration |
| 12:00–14:00 | **Framework Introduction & Roadmap** | 2 min | Preview the 3 teaching pillars; set the "secret" structure; first trial close |
| 14:00–22:00 | **Teaching Pillar #1** | 8 min | Deliver value, include proof element, end with chat engagement prompt |
| 22:00–24:00 | **Transition & Trial Close #1** | 2 min | Bridge to Pillar #2; soft close ("Are you starting to see how this changes things?") |
| 24:00–32:00 | **Teaching Pillar #2** | 8 min | Deliver value, include proof element, end with chat engagement prompt |
| 32:00–34:00 | **Transition & Trial Close #2** | 2 min | Bridge to Pillar #3; escalate commitment language |
| 34:00–42:00 | **Teaching Pillar #3** | 8 min | Deliver value, include proof element, end with chat engagement prompt |
| 42:00–44:00 | **The Gap & Invitation** | 2 min | "You now know the what — here's how to get the how"; pivot to offer |
| 44:00–54:00 | **Offer Stack Reveal** | 10 min | Systematic value build: core → bonuses → guarantee → price reveal → urgency mechanism |
| 54:00–56:00 | **Hard Close & CTA** | 2 min | Direct, unambiguous call to action with exact steps |
| 56:00–60:00 | **FAQ / Objection Handling** | 4 min | Address top 3–5 objections as "common questions"; re-state CTA after each answer |
| 60:00–65:00 | **Social Proof Stack** | 5 min | Testimonials, results, screenshots; re-state CTA |
| 65:00–72:00 | **Live Q&A** | 7 min | Answer attendee questions; weave CTA naturally into answers |
| 72:00–75:00 | **Final Close & Urgency Reminder** | 3 min | Countdown, scarcity recap, emotional future-pace, final CTA |

### For Each Row, Produce the Following Detail

```
═══════════════════════════════════════════════════════
[TIMESTAMP] — SECTION NAME
═══════════════════════════════════════════════════════

▸ SLIDE CUE:
  Slide #[X] — [Slide title / visual description / on-screen text]

▸ SPEAKER SCRIPT:
  [Full verbatim script for this section, including transitions]

▸ SPEAKER NOTES:
  - Tone/pacing directive (e.g., "Slow down here — this is the emotional anchor")
  - Emphasis words (bolded in script)
  - Physical/vocal cues ("Pause 3 seconds after this line")

▸ CHAT ENGAGEMENT PROMPT:
  [Exact prompt to type or speak, e.g., "Type 'YES' in the chat if you've ever felt stuck here"]
  — Expected response volume: [High / Medium / Low]
  — Chat moderator action: [e.g., "Pin top response," "Reply to first 5 with 🔥"]

▸ TRIAL CLOSE (if applicable):
  [Exact trial close language]
  — Type: [Soft agreement / Commitment escalation / Direct buy signal]

▸ TECH/PRODUCTION CUES:
  - [e.g., "Tech moderator: drop poll at 14:30"]
  - [e.g., "Switch to screen share at slide transition"]
  - [e.g., "Evergreen: trigger countdown timer overlay"]

▸ TRANSITION LINE:
  [Exact sentence that bridges to the next section]

═══════════════════════════════════════════════════════
```

### Supplementary Production Elements

Append the following to the master document:

1. **Pre-Webinar Checklist** — tech setup, link testing, slide load confirmation, backup plan for platform failure, moderator briefing agenda (15 min prior)
2. **Chat Moderator Playbook** — scripted responses for common attendee questions during the live event, escalation protocol for technical issues, CTA link drops (exact timestamps when the moderator posts the link)
3. **Engagement Scorecard** — a tracking template for chat response rates per prompt, poll completion rates, CTA click timestamps, and attendee drop-off benchmarks by section
4. **Post-Webinar Sequence Trigger Map** — which email/SMS sequences fire based on attendee behaviour (attended + bought, attended + didn't buy, registered + didn't attend), with recommended send times

## Step 5: Deliver Output

Produce the following named deliverables:

1. **[Webinar Name] — Master Run-of-Show v1.0** — the complete timestamped production document as detailed in Step 4, formatted for easy printing or teleprompter import
2. **[Webinar Name] — Slide Outline** — a sequential list of all slides with title, key visual/text, and the timestamp at which each appears (suitable for handing to a slide designer)
3. **[Webinar Name] — Chat Moderator Playbook** — standalone document the chat moderator can use independently without reading the full script
4. **[Webinar Name] — Timing Summary (One-Pager)** — a single-page overview showing section names, timestamps, durations, and key cues — designed to be taped next to the presenter's monitor during the live event
5. **[Webinar Name] — Engagement & Trial Close Map** — a visual map showing every chat prompt, poll, and trial close plotted against the timeline, with engagement-type labels

Flag any sections where the user's source material was thin and provide specific strengthening recommendations with draft copy.

## Step 6: Propose Experiments

```
FutureProof:save_experiment(skill="full-run-of-show-assembler", experiment={
  hypothesis: "Moving the first trial close from minute 14 to minute 10 (end of origin story) increases offer-section engagement by warming commitment earlier",
  variants: [
    "control: first trial close at Framework Introduction (min 14)",
    "variant: first trial close at end of Origin Story (min 8), with a second added at Framework Introduction"
  ],
  measurement: "Chat engagement rate during offer section, CTA click-through rate, and conversion rate across minimum 3 webinar runs",
  expected_impact: "10–20% increase in chat engagement during offer stack; 5–8% lift in live-session conversion rate"
})
```

```
FutureProof:save_experiment(skill="full-run-of-show-assembler", experiment={
  hypothesis: "Adding a 60-second 'fast action recap' immediately before the hard close — restating only the top 3 value items and the price — reduces decision fatigue and increases conversion vs. the standard full-stack recap",
  variants: [
    "control: full offer stack recap before close",
    "variant: 60-second distilled recap (3 items + price + urgency only)"
  ],
  measurement: "CTA click rate within 2 minutes of close, overall session conversion rate",
  expected_impact: "8–12% improvement in close-window conversion"
})
```

## Step 7: Request Research

```
FutureProof:request_research(skill="full-run-of-show-assembler",
  query="2024-2025 high-converting webinar timing structures, optimal section durations by price point tier ($97-$2000+), and engagement prompt frequency benchmarks from practitioners including Amy Porterfield, Russell Brunson, and Stu McLaren",
  reason="Calibrate default timing architecture to current best-practice data and allow price-point-specific timing adjustments in future sessions"
)
```

```
FutureProof:request_research(skill="full-run-of-show-assembler",
  query="Platform-specific webinar engagement features and limitations (Zoom Webinar, WebinarJam, Demio, EverWebinar, GoToWebinar, StreamYard) as of 2025 — polls, chat, offers, countdown timers, handouts, CTA buttons",
  reason="Ensure production cues in the run-of-show are platform-accurate and leverage each tool's unique engagement capabilities"
)
```

## Step 8: Save Session

```
FutureProof:save_session(skill="full-run-of-show-assembler", session={
  summary: "Assembled full run-of-show production document for [webinar name] targeting [ICA segment] with [duration]-minute format on [platform]",
  key_findings: [
    "[e.g., User's teaching pillars were strong but lacked transition language — drafted 6 bridging scripts]",
    "[e.g., No trial closes existed in source material — inserted 5 trial closes across the timeline]",
    "[e.g., Chat moderator playbook created from scratch — user had no prior moderator documentation]",
    "[e.g., Timing adjusted from default 75-min to 90-min to accommodate user's higher price point ($1,997) and additional proof section]"
  ],
  artifacts_delivered: [
    "Master Run-of-Show v1.0",
    "Slide Outline",
    "Chat Moderator Playbook",
    "Timing Summary One-Pager",
    "Engagement & Trial Close Map"
  ],
  user_feedback: null
})
```