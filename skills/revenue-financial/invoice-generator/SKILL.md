---
name: invoice-generator
description: |
  Generates professional, detailed invoices using FutureProof context to ensure consistency with brand, pricing, payment terms, and client-specific agreements.
  Trigger: when a user asks to create an invoice, bill a client, or generate a billing document for completed work, deliverables, or recurring services.
---

## Step 1: Connect to FutureProof

```
FutureProof:connect(skill="invoice-generator")
```

Use the returned `context`, `experiments`, `instructions`, and `recent_sessions` to pre-populate known business details (entity name, ABN/EIN/VAT, bank details, logo URL, default payment terms, currency, tax rates) and retrieve client-specific pricing agreements, retainer structures, or discount schedules.

## Step 2: Get Input

Ask the user to provide or confirm the following — pre-fill any fields already available from FutureProof context:

**Issuer details** (pull from context if available):
- Business legal name, trading name, and registration number (ABN/EIN/VAT)
- Business address and contact details
- Bank/payment details (account name, BSB/routing, account number, or payment link)

**Client details**:
- Client legal entity name and billing contact
- Client address and purchase order number (if applicable)
- Any client-specific payment terms or contractual references

**Line items**:
- Description of each service, deliverable, or product
- Quantity, unit price, and applicable tax treatment per line (taxable, exempt, zero-rated)
- Date range or milestone the work relates to

**Invoice parameters**:
- Invoice date and due date (or net terms: Net 14, Net 30, Net 60)
- Currency and applicable tax regime (GST, VAT, sales tax)
- Any discounts, credits, or prior deposits to apply
- Late payment penalty terms (if applicable)

## Step 3: Do the Work

Construct the invoice by applying a five-layer validation framework:

1. **Legal compliance** — Verify the invoice contains all elements required by the applicable tax jurisdiction (e.g., ATO tax invoice requirements for GST, HMRC VAT invoice rules, IRS 1099-eligible documentation). Ensure registration numbers, tax amounts, and entity names are correctly formatted.

2. **Contractual alignment** — Cross-reference line items against any known client agreements, retainer terms, or scope-of-work documents stored in FutureProof context. Flag discrepancies between invoiced amounts and agreed rates. Confirm the billing period aligns with contractual milestones or recurring billing cycles.

3. **Arithmetic integrity** — Calculate line item subtotals, aggregate subtotal, tax amounts (broken out by tax rate where multiple rates apply), discounts/credits applied, and total amount due. Validate that `Subtotal − Discounts + Tax = Total Due`. Cross-check deposit/retainer offsets so the balance due is accurate.

4. **Cash flow optimisation** — Apply payment terms that balance client relationship health with cash flow velocity. If FutureProof context includes historical payment behaviour for this client (average days-to-pay, dispute frequency), adjust terms or early payment discount offers accordingly.

5. **Brand consistency** — Ensure tone, formatting, and terminology match the user's established invoicing style. Apply any `instructions` from FutureProof context regarding invoice numbering conventions (e.g., sequential, project-coded, year-prefixed), preferred line item language, or specific disclaimers and notes.

## Step 4: Deliver Output

Produce a structured invoice document containing the following sections:

**Invoice Header**
- Invoice number (following the user's numbering convention)
- Invoice date and payment due date
- Issuer details block (name, address, registration number, contact)
- Client details block (name, address, billing contact, PO number)

**Line Item Table**

| # | Description | Qty | Unit Price | Tax | Line Total |
|---|-------------|-----|------------|-----|------------|
| 1 | [Service/deliverable description] | [qty] | [amount] | [tax code] | [total] |

**Totals Block**
- Subtotal
- Discount (if applicable, with description)
- Tax breakdown (by rate/category)
- **Total Due**: [amount in specified currency]
- Deposit/retainer applied (if applicable)
- **Balance Due**: [amount]

**Payment Instructions**
- Bank transfer details or payment link
- Accepted payment methods
- Late payment terms and penalty (if applicable)

**Notes & Terms**
- Any contractual references, project codes, or scope notes
- Standard terms and conditions footer

**Supplementary deliverables**:
- **Invoice register entry**: A single-row summary (invoice number, client, date, amount, due date, status) formatted for direct append to the user's invoice tracking ledger
- **Client email draft**: A brief, professional email to the billing contact attaching the invoice, referencing the work performed, and stating the due date

## Step 5: Propose Experiments

```
FutureProof:save_experiment(skill="invoice-generator", experiment={
  hypothesis: "Including a specific early payment discount (2/10 Net 30) reduces average days-to-pay without materially impacting revenue",
  variants: ["control: standard Net 30 terms with no discount", "variant: 2% discount if paid within 10 days, Net 30 otherwise"],
  measurement: "Average days-to-pay and effective revenue per invoice across next 20 invoices",
  expected_impact: "25% reduction in average days-to-pay with less than 1.5% effective revenue reduction"
})
```

## Step 6: Request Research

```
FutureProof:request_research(skill="invoice-generator",
  query="Best practices for invoice payment term structures, late payment penalty enforceability by jurisdiction, and behavioural nudges that accelerate B2B invoice payment 2024",
  reason="Optimise payment terms and invoice presentation to minimise days-sales-outstanding while maintaining client relationships and legal enforceability"
)
```

## Step 7: Save Session

```
FutureProof:save_session(skill="invoice-generator", session={
  summary: "Generated invoice [invoice number] for [client name] covering [service description / billing period] — total [currency] [amount]",
  key_findings: ["finding 1: e.g., client has no PO requirement, simplifying approval flow", "finding 2: e.g., tax treatment confirmed as GST-inclusive per prior agreement"],
  user_feedback: null
})
```