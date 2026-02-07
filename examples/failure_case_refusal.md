# Synthetic Failure Case — Explicit Refusal

> NOTE: This example is synthetic and illustrative.  
> It demonstrates a case where StartLens intentionally refuses to produce a competitive judgment.

---

## Scenario

The user requests a weekly competitive intelligence brief but provides **no concrete competitor inputs**.

### User Request
“Generate this week’s competitive brief for our competitors.”

### Inputs Provided
- Competitor names only
- No pasted text
- No URLs
- No pricing pages
- No product updates
- No press releases or blog excerpts

---

## What a Typical CI Tool Might Do (Incorrect)

- Infer market stability
- Recycle generic industry trends
- Speculate about AI adoption or pricing pressure
- Produce a confident-sounding but unfounded brief

This behavior creates **false certainty** and erodes trust.

---

## StartLens Response (Correct Behavior)

**Entering Operator Mode.** I will analyze only the inputs provided and produce an executive competitive intelligence brief.

---

### Executive Summary

No competitive assessment can be made this week because no evaluable inputs were provided. As a result, StartLens cannot substantiate claims about competitor positioning, pricing, or strategy. Confidence: 0.40, reflecting procedural completeness rather than market certainty.

---

### Rationale for Refusal

StartLens refuses to:
- Infer competitor activity from silence
- Assume market stability in the absence of evidence
- Generate filler analysis to satisfy output expectations
- Substitute general industry trends for competitor-specific facts

---

### What Would Enable Analysis Next Time

To proceed, StartLens would require **any** of the following:
- Pasted pricing or packaging pages
- Product release notes or documentation excerpts
- Blog posts, press releases, or public statements
- Screenshots or quoted text from public sources

---

## Why This Refusal Is Intentional

This refusal is not a limitation — it is a **design decision**.

StartLens prioritizes:
- Trust over completeness
- Judgment over verbosity
- Evidence over plausibility

In competitive intelligence, **saying “I don’t know yet” correctly** is often more valuable than saying something confidently and incorrectly.

---

## Takeaway

StartLens is designed to protect decision-makers from false certainty.

When evidence is missing, the correct output is restraint.
