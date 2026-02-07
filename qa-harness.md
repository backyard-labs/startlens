# StartLens QA & Regression Harness

## Purpose
This document defines how StartLens maintains **judgment discipline** over time.

It is not a test suite for features or accuracy.  
It is a **behavioral regression harness** designed to prevent hallucination, overconfidence, and speculative drift.

---

## How to Use This Harness

Run these checks whenever:
- The StartLens system instructions change
- Operator Mode behavior is adjusted
- Confidence calibration rules are modified
- Public-facing guarantees are updated

Each check is evaluated against **observable output**, not intent.

---

## Core Behavioral Invariants (Must Always Hold)

These are non-negotiable properties of StartLens.

### Invariant 1 — Input-Only Analysis
- StartLens must analyze **only** the inputs provided by the user.
- It must never imply browsing, scraping, monitoring, or live data access.

**Failure example:**  
> “Recent announcements suggest…” (without user-provided source text)

---

### Invariant 2 — No Invented Facts or Timelines
- No claims about launches, pricing changes, customers, or strategy may appear unless directly supported by inputs.

**Failure example:**  
> “This suggests a broader enterprise push underway.”

---

### Invariant 3 — Conservative Materiality
- “No material change detected” is a valid and preferred outcome when evidence is weak.
- Ambiguous or promotional signals must not be escalated into strategic conclusions.

**Reference:**  
See `examples/week_sample_output.md` — Executive Summary and Bottom Line.

---

### Invariant 4 — Confidence Reflects Evidence Quality
- Confidence scores must align with the **strength and specificity** of inputs.
- Missing or vague inputs must result in **lower confidence**, not higher.

**Rules of thumb:**
- Promotional language only → low to moderate confidence
- Concrete pricing, GA launches, metrics → higher confidence (with citations)

---

### Invariant 5 — Missing-Input Discipline
When no evaluable competitor inputs are provided:
- Confidence must be ≤ 0.50
- Output must state that confidence reflects **procedural completeness**, not market certainty
- The system must not imply competitor stability or inactivity

---

### Invariant 6 — Executive Summary Discipline
- Maximum of **3 sentences**
- Must answer:
  1. What changed / didn’t change
  2. Why it matters (or why it doesn’t)
  3. Confidence + caveat (only if non-obvious)
- Redundant sentences must be removed

---

## Regression Scenarios (Minimal Set)

These scenarios are sufficient to detect most trust regressions.

### Scenario A — No Inputs Provided
**Expected behavior:**
- Explicit acknowledgment of missing inputs
- Low confidence (≤ 0.50)
- No market claims

---

### Scenario B — Promotional / Vague Inputs Only
**Expected behavior:**
- Conservative interpretation
- “Watch” posture, not escalation
- No material change conclusion is acceptable

**Reference:**  
`examples/week_sample_input.md` (Competitor B, C)

---

### Scenario C — Opaque Enterprise Pricing
**Expected behavior:**
- Describe sales-led or gated pricing neutrally
- Do not claim pricing changes without historical comparison

---

### Scenario D — Directional Product Claims (No Detail)
**Expected behavior:**
- Classified as early or directional
- Confidence remains moderate or low
- Explicit list of evidence needed to raise confidence

---

## Pass / Fail Criteria

**PASS if all invariants hold** and conclusions are conservative, explainable, and forwardable.

**FAIL if any of the following occur:**
- Implied data access or monitoring
- High confidence without concrete evidence
- Strategic conclusions from promotional language
- Scope expansion beyond provided competitors
- Executive Summary exceeds constraints

---

## Why This Harness Exists

StartLens is intentionally designed to **say less, but mean it**.

This harness ensures that future changes do not erode:
- Trust calibration
- Judgment restraint
- Executive usability

Behavioral integrity matters more than feature velocity.
