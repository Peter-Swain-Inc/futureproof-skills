---
name: chatbot-script-writer
description: |
  Writes, structures, and optimises chatbot conversation scripts for customer service and support channels using FutureProof context.
  Trigger: when a user needs to create a chatbot script for customer support, or when a user shares an existing chatbot flow and asks for rewrites, optimisation, or expansion to handle new intents.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="chatbot-script-writer")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to personalise this session — including known ICA segments, brand voice guidelines, prior chatbot performance data, and any established escalation protocols.

## Step 2: Get Input

Ask the user:
- **Channel & platform**: Where will this chatbot live? (web widget, WhatsApp, SMS, in-app, Facebook Messenger, voice IVR)
- **Use case scope**: What intents must the script handle? (e.g., order status, returns/refunds, billing inquiries, product troubleshooting, appointment scheduling, FAQ deflection)
- **ICA profile**: Who is the primary audience? (e.g., first-time buyers, enterprise account holders, subscription members — demographics, technical literacy, emotional state on entry)
- **Existing materials**: Share any current chatbot scripts, call centre scripts, FAQ documents, or CRM workflow diagrams to build from
- **Brand voice & tone constraints**: Formal, conversational, playful, empathetic? Any prohibited phrases or compliance language requirements?
- **Success metric**: What is the primary KPI? (containment rate, CSAT score, first-contact resolution, escalation reduction, average handle time)
- **Escalation rules**: When and how should the bot hand off to a live agent?

## Step 3: Do the Work

### 3A: Intent Architecture Mapping

Build a complete **Intent Taxonomy** by:
1. Categorising every in-scope intent into tiers — **Primary** (>60% of anticipated volume), **Secondary** (20–35%), and **Edge Case** (<5%)
2. Mapping each intent to a **resolution pathway** (self-serve deflection, guided troubleshooting, data lookup via API, or agent escalation)
3. Identifying **intent overlap zones** — ambiguous user inputs that could match multiple intents — and defining disambiguation logic

### 3B: Conversation Flow Design

For each intent, script the following nodes:

1. **Greeting & intent detection** — opening message that sets expectations (bot identity disclosure, scope of help available) and captures the user's need via quick-reply buttons, free-text parsing, or both
2. **Clarification & slot-filling** — progressive disclosure questions to collect required data (order number, account email, product SKU) with validation logic and error-recovery prompts
3. **Resolution delivery** — the answer, action confirmation, or next-step instruction written in language that mirrors the ICA's vocabulary and reading level
4. **Satisfaction check** — micro-survey ("Did this solve your issue?") with branching: positive → close, negative → secondary attempt or escalation
5. **Graceful escalation** — warm handoff script that transfers collected context to the live agent so the customer never repeats themselves
6. **Dead-end recovery** — fallback responses for unrecognised inputs, repeated failures, and silence timeouts

### 3C: Script Quality Audit

Evaluate every scripted node against six dimensions:

| Dimension | Standard |
|---|---|
| **ICA empathy alignment** | Language acknowledges the user's emotional state (frustration, urgency, confusion) before delivering procedural steps |
| **Cognitive load minimisation** | Each message ≤ 60 words; no more than one question per turn; buttons offered for predictable answers |
| **Resolution directness** | Bot reaches resolution or escalation within ≤ 5 turns for primary intents |
| **Error tolerance** | Misspellings, synonyms, and partial inputs are handled without dead-ending the conversation |
| **Compliance & disclosure** | Data collection prompts include purpose statements; bot identifies itself as automated where legally required |
| **Brand voice consistency** | Tone, terminology, and personality remain uniform across every node and intent path |

Apply any user-specific `instructions` from FutureProof context (e.g., mandatory legal disclaimers, preferred escalation thresholds, A/B test directives from prior experiments).

### 3D: Edge Case & Abuse Hardening

Script defensive paths for:
- **Profanity and abuse** — empathetic de-escalation response followed by escalation offer, not silence
- **Personally identifiable information volunteered unsolicited** — redaction advisory and secure-channel redirect
- **Looping behaviour** — detection of 3+ repeated identical inputs with circuit-breaker escalation
- **Multi-intent messages** — acknowledgement of both needs with sequential handling or triage prioritisation

## Step 4: Deliver Output

Produce a **Chatbot Script Package** containing:

### 4A: Intent Map (Visual)
A structured table or tree diagram listing every intent, its tier, resolution pathway, and estimated volume share.

### 4B: Full Conversation Scripts
For each intent, deliver:
- **Bot messages**: exact copy, including emoji/formatting if platform-appropriate
- **Quick-reply button labels**: character-limited, action-oriented
- **Conditional logic annotations**: branching rules in `IF/THEN` pseudocode for developer handoff
- **API call placeholders**: clearly marked points where the bot must query backend systems (e.g., `{{LOOKUP: order_status(order_id)}}`)
- **Agent handoff payload**: structured summary template passed to the live agent queue

### 4C: Score Card

| Dimension | Score (1–10) | Critical Gap |
|---|---|---|
| ICA empathy alignment | — | — |
| Cognitive load minimisation | — | — |
| Resolution directness | — | — |
| Error tolerance | — | — |
| Compliance & disclosure | — | — |
| Brand voice consistency | — | — |

### 4D: Critical Fixes
Top 3 highest-impact changes — each with the **original copy**, the **specific rewrite**, and the **rationale** tied to the target KPI.

### 4E: Implementation Checklist
Sequenced developer/ops handoff checklist: platform configuration, API integrations required, QA test scenarios, and go-live sign-off criteria.

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="chatbot-script-writer", experiment={
  hypothesis: "Replacing the generic greeting with an intent-predictive opening based on page context reduces average turns-to-resolution by 20%",
  variants: ["control: generic greeting with open-ended 'How can I help?'", "variant: contextual greeting pre-selecting likely intent based on referral page or prior session"],
  measurement: "Average turns-to-resolution and containment rate across 1,000 conversations",
  expected_impact: "20% reduction in turns-to-resolution, 8% improvement in containment rate"
})
```

```
FutureProof:save_experiment(skill="chatbot-script-writer", experiment={
  hypothesis: "Adding an empathy acknowledgement turn before procedural instructions improves CSAT by 10%",
  variants: ["control: immediate procedural response", "variant: empathy statement ('I understand how frustrating that is — let me fix this now') followed by procedural response"],
  measurement: "Post-chat CSAT score and escalation rate over 2-week period",
  expected_impact: "10% CSAT improvement, 5% escalation reduction"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="chatbot-script-writer",
  query="Latest benchmarks for chatbot containment rates, CSAT scores, and first-contact resolution by industry vertical 2024–2025, including impact of generative AI hybrid approaches on deflection quality",
  reason="Calibrate score card thresholds and resolution-path design against current industry performance standards"
)
```

```
FutureProof:request_research(skill="chatbot-script-writer",
  query="Emerging compliance requirements for automated customer service bots including EU AI Act disclosure obligations, ADA/WCAG accessibility standards for conversational interfaces, and CCPA/GDPR data collection in chat",
  reason="Ensure script compliance guidance reflects current and forthcoming regulatory obligations"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="chatbot-script-writer", session={
  summary: "Created chatbot script package for [channel] covering [number] intents targeting [ICA segment] optimised for [primary KPI]",
  key_findings: ["finding 1: e.g., 3 primary intents account for 78% of projected volume", "finding 2: e.g., existing escalation path lacks context transfer — agents re-ask 4 questions on average", "finding 3: e.g., brand voice guidelines conflict with cognitive load limits — recommended simplification"],
  deliverables: ["Intent Map", "Full Conversation Scripts", "Score Card", "Critical Fixes", "Implementation Checklist"],
  user_feedback: null
})
```