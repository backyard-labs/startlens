# StartLens QA / Regression Harness (Lightweight)

## Goal
Ensure StartLens outputs remain consistent with the Operator Spec (v1.1) across updates, with minimal overhead.

## How to Use
Run these test cases after any change to:
- Custom GPT instructions
- Operator prompt wording
- Brief template structure

Log pass/fail in the bottom table.

## Pass/Fail Criteria (Global)
PASS requires:
- No web-browsing claims
- No invented facts or timelines
- Confidence calibrated per evidence
- Exec Summary <= 3 sentences
- “No material change” allowed/preferred when weak evidence

FAIL triggers include:
- Suggesting real-world changes without user inputs
- High confidence when inputs are missing or vague
- Scope expansion beyond provided competitors
- Executive summary redundancy or > 3 sentences

---

## Test Case 1 — Missing Inputs (Canonical)
Input:
- “Generate this week’s competitive brief. No competitor inputs provided.”

Expected:
- Operator Mode declaration (first activation)
- Explicit “assessment not possible due to missing inputs”
- Confidence ≤ 0.50 and framed as procedural completeness

---

## Test Case 2 — Marketing Noise Only
Inputs:
- Competitor A: “We are thrilled about momentum and adoption.”
- Competitor B: “Big things coming. Stay tuned.”
- Competitor C: “We continue investing in our people.”

Expected:
- Conservative “no material change”
- Low signal-to-noise called out
- Watch items suggested; no strategic leaps

---

## Test Case 3 — Pricing Signal (Opaque Enterprise)
Inputs:
- Competitor A pricing: “Contact sales for enterprise pricing.”

Expected:
- No claim of pricing change
- Interpret as enterprise sales-led/opaque pricing model
- Confidence moderate (evidence limited); request historical diff if needed

---

## Test Case 4 — Product Claim Without Details
Inputs:
- Competitor B: “Introducing our most advanced AI-powered security features yet.”

Expected:
- Classified as directional/product signal, not confirmed differentiation
- Request corroboration (docs, benchmarks, GA, pricing attachment)

---

## Test Case 5 — Mixed Concrete + Vague
Inputs:
- A: “Enterprise Plus tier added” (pricing page)
- B: “Piloting AI capabilities with select customers”
- C: “Analysts note growing presence”

Expected:
- A treated as most material, but still conservative if no feature table
- B labeled pilot (future-facing)
- C treated as perception signal, low operational detail
- Clear next-week watch items

---

## Regression Log

| Date | Change made | Tests run (1–5) | Result (Pass/Fail) | Notes |
|------|-------------|------------------|--------------------|-------|
|      |             |                  |                    |       |
