# Invoice and Payment Optimization Guide

Practical playbook for faster cash flow, lower fees, and fewer disputes. Use it to design terms, streamline invoices, and implement a collections workflow that protects relationships.

## Table of Contents
- Goals and outcomes
- Core principles
- Net terms strategy
- Payment processors and rails
- International transfers
- Invoice templates and required fields
- Late payment handling
- Retainer billing
- Metrics and reporting
- Automation and operational workflows
- Policy clauses and templates
- 30/60/90-day implementation checklist

## Goals and Outcomes
- Reduce days sales outstanding (DSO) and improve predictability.
- Increase on-time payments by clarifying terms and reducing friction.
- Minimize payment fees and FX losses by choosing the right rails.
- Prevent disputes with clear scope, deliverables, and acceptance criteria.

## Core Principles
1. **Clarity beats complexity.** Clear terms, precise line items, and simple payment options outperform elaborate policies.
2. **Speed is a system.** Automate reminders, standardize invoices, and align internal handoffs.
3. **Risk and reward are linked.** Longer terms or high-risk clients require deposits, milestones, or card-on-file.
4. **Localize for buyers.** Respect regional payment preferences, currencies, and tax requirements.
5. **Document everything.** Approval, delivery, and acceptance records prevent disputes.

## Net Terms Strategy
Net terms define how long a client has to pay after invoicing or acceptance. Use a tiered approach.

### Common Net Terms
- **Net 7/15:** Best for small engagements and early-stage clients.
- **Net 30:** Standard for most SMB and mid-market clients.
- **Net 45/60:** Enterprise buyers; use only with strong credit signals.

### Decision Framework
- **New client + large project:** 30–50% upfront, remaining milestones net 15.
- **Established client with clean history:** Net 30 or net 45.
- **High-risk or low-margin:** Net 7/15 and card or ACH only.

### Start Date for Net Terms
Define it explicitly in the contract and on the invoice:
- **Invoice date** (most common).
- **Delivery date** (for tangible goods).
- **Acceptance date** (for services; requires acceptance process).

### Early Payment Incentives
Offer discounts only when margin allows. Example: **2/10 net 30** (2% discount if paid within 10 days, otherwise due in 30).

### Late Fees and Interest
Include in the contract and invoice to enforceability:
- Flat fee (e.g., $50) after a grace period.
- Monthly interest (e.g., 1.5% per month, where allowed by law).

### Payment Term Clause (Template)
```
Payment Terms: Client agrees to pay all undisputed invoices within 30 days of the invoice date (net 30). Amounts unpaid after 5 calendar days from the due date may incur a late fee of $50 and interest at 1.5% per month on the outstanding balance, where permitted by law.
```

## Payment Processors and Rails
Choose rails by payment size, geography, client preference, and fee sensitivity.

### Common Payment Methods
| Method | Typical Cost | Settlement Speed | Best For | Considerations |
|---|---|---|---|---|
| Card processor | 2.5–3.5% | 1–3 days | Fast payments, small invoices | Chargebacks, higher fees |
| ACH bank transfer | Low/flat | 1–3 days | US clients, mid-size invoices | Requires bank details |
| Wire transfer | Flat fee | Same/next day | Large invoices | Bank fees, more admin |
| Checks | Low | 5–10 days | Legacy buyers | Slow, manual follow-up |
| Local bank transfer | Low | 1–2 days | International clients | Needs local details |

### Selection Criteria
- **Ticket size:** Use ACH/wire for large invoices to lower fees.
- **Client preference:** Offer at least two methods.
- **Risk tolerance:** Card-on-file enables autopay for retainer invoices.
- **Invoice frequency:** Recurring invoices benefit from automatic charging.

### Payment Processor Checklist
- Supports multi-currency or local payouts.
- Offers payment links and customer portals.
- Can store payment methods with consent.
- Provides reconciliation exports and webhooks.
- Supports compliance requirements (PCI, KYC where applicable).

## International Transfers
Cross-border payments add FX risk, intermediary fees, and compliance requirements.

### Currency Strategy
- **Invoice in your home currency** to avoid FX risk.
- **Invoice in client currency** to remove friction; hedge risk via shorter terms.
- If invoicing in client currency, set an **FX refresh window** (e.g., “Currency locked at invoice issue date”).

### Bank Details and Fees
Include the full routing information:
- **SWIFT/BIC** for international wires.
- **IBAN** for EU/UK.
- Intermediary fees (OUR/SHA/BEN): specify who pays.

Suggested line:
```
International wire fees are the client’s responsibility (SHA). Please ensure intermediary bank fees are not deducted from the invoice amount.
```

### Transfer Providers
For low to mid-sized invoices, specialized transfer platforms can reduce FX spread and fees compared to traditional banks. Confirm they support:
- Local account details for payer convenience.
- Proof of payment and reference fields.
- Compliance documentation.

### Tax and Compliance Notes
- Verify VAT/GST requirements for cross-border services.
- Use **reverse charge** notes when applicable.
- Collect tax documentation (W-8/W-9 or local equivalents) early.

## Invoice Templates and Required Fields
Consistent templates reduce disputes and improve receivables.

### Required Fields Checklist
- Seller legal name, address, tax ID
- Buyer name, address, tax ID (if applicable)
- Invoice number and date
- Due date and payment terms
- Line items with clear descriptions, quantities, and rates
- Subtotal, tax, discounts, and total
- Currency and FX statement (if needed)
- Payment instructions and remittance details

### Standard Service Invoice Template
```
INVOICE

Seller: {Your Company Name}
Address: {Street, City, State/Region, Country}
Tax ID/VAT: {Tax ID}

Bill To: {Client Name}
Address: {Client Address}
Tax ID/VAT: {Client Tax ID}

Invoice Number: {INV-0001}
Invoice Date: {YYYY-MM-DD}
Due Date: {YYYY-MM-DD}
Payment Terms: {Net 30}
Currency: {USD}

Description | Qty | Rate | Amount
--- | --- | --- | ---
{Service description with date range} | {Hours} | {Rate} | {Amount}

Subtotal: {Amount}
Tax: {Amount}
Total Due: {Amount}

Payment Instructions:
- Bank: {Bank Name}
- Account Name: {Account Name}
- Account Number/IBAN: {Number}
- SWIFT/BIC: {Code}
- Reference: {Invoice Number}

Notes:
- Please remit payment by the due date. Contact {Email} with any questions.
```

### Milestone Invoice Template
```
Milestone: {Discovery Phase Complete}
Deliverables: {List}
Acceptance Date: {YYYY-MM-DD}
Amount Due: {Amount}
```

### Retainer Invoice Template
```
Retainer Period: {YYYY-MM-DD to YYYY-MM-DD}
Retainer Amount: {Amount}
Included Hours/Scope: {Description}
Overage Rate: {Rate}
```

## Late Payment Handling
Build a consistent escalation ladder that preserves relationships while enforcing terms.

### Preventative Practices
- Confirm payment method and billing contact during onboarding.
- Send invoices immediately upon milestone completion.
- Add a short **dispute window** (e.g., 5 business days).
- Require written acceptance for deliverables.

### Dunning Schedule (Example)
- **3 days before due:** Friendly reminder with invoice link.
- **Due date:** “Due today” reminder with payment options.
- **+7 days:** Past-due notice with request for payment date.
- **+14 days:** Escalation to finance lead; offer payment plan if needed.
- **+30 days:** Final notice; pause work; apply late fees if allowed.

### Past-Due Email Template (Short)
```
Subject: Past Due Invoice {INV-0001}

Hi {Name},
Our records show invoice {INV-0001} for {Amount} is now past due. Could you confirm when payment will be processed? Payment options are listed on the invoice. Please let me know if you have any questions or need a copy.
```

### Escalation Options
- Pause work or access if payment exceeds a defined threshold.
- Negotiate a payment plan (documented via addendum).
- Consider collections or legal action only after documented attempts.

## Retainer Billing
Retainers stabilize cash flow but require precise scope and usage tracking.

### Retainer Models
- **Time-based:** Fixed hours each month; overages billed separately.
- **Access-based:** Client pays for guaranteed availability.
- **Project-based:** Retainer covers defined milestones.

### Best Practices
- Bill **in advance** for the upcoming period.
- Provide **monthly usage reports** with remaining balance.
- Define rollover rules (e.g., 25% of unused hours roll over for 30 days).
- Set an overage rate and pre-approval threshold.

### Retainer Clause (Template)
```
Retainer: Client agrees to a monthly retainer of $5,000, billed in advance on the 1st of each month. The retainer includes up to 25 hours of services. Unused hours may roll over up to 25% for 30 days. Additional hours are billed at $200/hour and invoiced monthly.
```

## Metrics and Reporting
Measure outcomes and adjust terms with data.

### Key Metrics
- **DSO (Days Sales Outstanding):** Average days to collect.
- **On-time payment rate:** % paid on or before due date.
- **Aging buckets:** 0–30, 31–60, 61–90, 90+.
- **Dispute rate:** % invoices disputed.
- **Payment mix:** Card vs ACH vs wire.

### Reporting Cadence
- Weekly: Aging summary and top 10 past-due.
- Monthly: DSO trends and payment method costs.
- Quarterly: Review terms, adjust deposit policy, renegotiate high-risk clients.

## Automation and Operational Workflows
Reduce manual effort and eliminate handoff gaps.

### Workflow Design
1. Project completion triggers invoice generation.
2. Invoice gets reviewed for accuracy and sent same day.
3. Payment link included with auto-reminders enabled.
4. Payment confirmation automatically updates CRM/ledger.

### Automation Checklist
- Auto-numbered invoices.
- Template-based line items.
- Payment links embedded.
- Automated reminders.
- Reconciliation and posting to ledger.

## Policy Clauses and Templates
Use consistent policy language across proposals, contracts, and invoices.

### Payment Policy (Short)
```
Invoices are due according to the stated payment terms. Client agrees to notify us of any disputes within 5 business days of receipt. If no notice is received, the invoice is deemed accepted.
```

### Dispute Window Clause
```
Any disputes must be submitted in writing within 5 business days of invoice receipt. Undisputed portions remain payable per the terms.
```

### Suspension of Services Clause
```
If an invoice is more than 30 days past due, we may pause services until the balance is settled.
```

## 30/60/90-Day Implementation Checklist
**First 30 days**
- Define standard net terms and deposit policy.
- Standardize invoice templates and fields.
- Select default payment methods and processor.
- Implement automated reminders.

**Days 31–60**
- Train team on acceptance and billing workflows.
- Add retainer templates and tracking.
- Build monthly reporting for DSO and aging.

**Days 61–90**
- Review payment metrics and refine terms.
- Adjust payment options by client segment.
- Expand localization for international clients.

## Quick Reference: Payment Optimization Summary
- Send invoices immediately upon completion.
- Offer at least two payment options.
- Use shorter net terms for new or risky clients.
- Make payment instructions impossible to miss.
- Automate reminders and follow up consistently.

---

This guide is designed to be adapted. Choose the clauses and workflows that match your legal requirements, client base, and internal capacity.
