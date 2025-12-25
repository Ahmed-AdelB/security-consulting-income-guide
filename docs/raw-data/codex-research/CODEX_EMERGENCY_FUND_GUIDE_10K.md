# Emergency Fund & Runway Calculator for Consultants

This guide helps independent consultants size a cash reserve, add an income-volatility buffer, and account for insurance. Use it as a worksheet or plug the formulas into a spreadsheet.

## 1) Gather Inputs

**Personal Monthly Expenses (PME)**
- Housing, utilities, groceries, transportation
- Debt minimums (student loans, credit cards)
- Health care out-of-pocket, childcare

**Business Fixed Monthly Costs (BFC)**
- Software subscriptions, coworking, phone/internet
- Contractors you must retain
- Minimum tax/quarterly set-asides

**Insurance Monthly Premiums (IMP)**
- Health, disability, professional liability, cyber

**Available Liquid Cash (ALC)**
- Cash in business/personal checking + savings (exclude retirement)

**Income History (last 6–12 months)**
- Monthly net income after variable business costs and taxes

## 2) Choose a Base Coverage Window

Pick the number of months you want to be able to cover essentials with zero income.

- **Lower volatility, strong pipeline:** 3–4 months
- **Typical consulting volatility:** 6 months
- **High volatility or niche demand:** 9–12 months

Call this **Coverage Months (CM)**.

## 3) Calculate Base Emergency Fund

**Monthly Essential Burn (MEB)**

```
MEB = PME + BFC + IMP
```

**Base Emergency Fund (BEF)**

```
BEF = MEB × CM
```

## 4) Add an Income Volatility Buffer

Use one of the approaches below. If unsure, start with the **Gap Method**.

### Option A: Gap Method (simple, realistic)

1. Calculate **Average Monthly Net Income (AMNI)** from the last 6–12 months.
2. Identify **Lowest Month Income (LMI)** in the same period.
3. Compute **Income Gap (IG)**:

```
IG = max(0, AMNI − LMI)
```

4. Choose **Gap Months (GM)** equal to typical lead-time to win work (1–3 months).

**Volatility Buffer (VB)**

```
VB = IG × GM
```

### Option B: Percentage Method (fast)

Pick a volatility factor based on how lumpy your income is:

- Stable retainers: 10% of BEF
- Mixed retainers + projects: 20% of BEF
- Project-only or seasonal: 30% of BEF

```
VB = BEF × Volatility Factor
```

## 5) Insurance Considerations

Add reserves for risks that would increase burn or slow income recovery.

**Recommended Add-ons**
- **Health insurance deductible/out-of-pocket max:** Add 1–2 months of PME if your plan has high exposure.
- **Disability elimination period:** If benefits start after 60–90 days, add 2–3 months of MEB.
- **Professional liability deductible:** Add your deductible amount if it could be triggered.
- **Business interruption:** If you lack coverage, add 1–2 months of BFC.

Call the total **Insurance Reserve (IR)**.

## 6) Final Emergency Fund Target

```
Emergency Fund Target (EFT) = BEF + VB + IR
```

## 7) Runway Calculator

Runway tells you how long your liquid cash lasts under conservative assumptions.

**Conservative Monthly Burn (CMB)**

```
CMB = MEB + (IR ÷ CM)
```

**Runway (months)**

```
Runway = ALC ÷ CMB
```

If your runway is below your chosen CM, increase your reserve or reduce burn.

## 8) Quick Worksheet (fill-in)

- PME: $____
- BFC: $____
- IMP: $____
- MEB: $____
- CM: ____ months
- BEF: $____
- VB method: Gap / Percentage
- VB: $____
- IR: $____
- **EFT: $____**
- ALC: $____
- **Runway: ____ months**

## 9) Example (illustrative)

- PME = $4,200
- BFC = $800
- IMP = $600
- MEB = $5,600
- CM = 6
- BEF = $33,600

Income volatility (Gap Method):
- AMNI = $7,500
- LMI = $4,000
- IG = $3,500
- GM = 2
- VB = $7,000

Insurance reserve:
- Disability elimination period = 2 months of MEB
- IR = $11,200

**EFT = $33,600 + $7,000 + $11,200 = $51,800**

Runway if ALC = $38,000:

```
CMB = 5,600 + (11,200 ÷ 6) = 7,467
Runway = 38,000 ÷ 7,467 = 5.1 months
```

## 10) How to Use This in Practice

- Recalculate quarterly and after major income changes.
- Keep the emergency fund in liquid, low-risk accounts.
- If you must use it, set a replenishment plan (e.g., 10–20% of each invoice).
- Pair this with a pipeline target (e.g., 3× monthly revenue in qualified leads).
