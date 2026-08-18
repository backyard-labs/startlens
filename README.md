# StartLens

**Decision-grade competitive intelligence through disciplined judgment—not volume.**

StartLens is a public-beta Custom GPT that transforms user-provided competitor evidence into concise, executive-ready assessments.

It is designed to answer one central question:

> What, if anything, materially changed—and does it warrant action?

StartLens prioritizes evidence quality, conservative judgment, calibrated confidence, and explicit uncertainty. When the available evidence does not support a material conclusion, “No material change detected” is a valid and often preferred outcome.

---

## The Problem

Competitive-intelligence reporting commonly fails in two ways:

- **Noise overload:** Too many signals are collected without determining which ones actually matter.
- **Speculative drift:** Weak announcements, promotional claims, or incomplete evidence are converted into confident strategic conclusions.

Executives do not necessarily need more monitoring. They need:

- Clear materiality judgments
- Evidence-backed conclusions
- Calibrated confidence
- Explicit assumptions and uncertainty
- Recommendations proportional to the evidence

StartLens is designed around those requirements.

---

## Intended Users

StartLens is designed for professionals responsible for interpreting competitive developments, including:

- Product and strategy leaders
- Go-to-market leaders
- Competitive-intelligence practitioners
- Business and market analysts
- Executives reviewing competitor activity

The current public beta is particularly suited to B2B technology and cybersecurity competitive-intelligence scenarios.

---

## How StartLens Works

StartLens follows an input-only analytical workflow:

1. The user identifies the industry, audience, and executive question.
2. The user supplies evidence about one or more competitors.
3. StartLens evaluates the evidence for specificity, reliability, and materiality.
4. It distinguishes observed facts from interpretations and unsupported possibilities.
5. It produces an executive-ready assessment with calibrated confidence.
6. If the evidence is insufficient, StartLens says so rather than filling gaps with speculation.

Accepted evidence may include:

- Product announcements
- Pricing or packaging pages
- Release notes
- Company blog posts
- Public documentation
- Press releases
- Job postings
- Screenshots
- Pasted excerpts from public sources

Providing a link does not mean that StartLens independently opened, reviewed, or verified it. Relevant source content should be pasted or otherwise supplied as part of the input.

---

## Core Analytical Principles

### Input-Only Analysis

StartLens analyzes only evidence supplied by the user.

It does not claim to:

- Browse the web
- Scrape websites
- Continuously monitor competitors
- Independently verify external sources
- Retrieve information that was not provided

### Evidence Before Interpretation

StartLens separates:

- **Observed evidence:** What the supplied material explicitly establishes
- **Interpretation:** What the evidence reasonably suggests
- **Alternative explanations:** Other plausible interpretations
- **Speculation:** Conclusions the available evidence does not support

### Conservative Materiality

A competitive development is potentially material when it could affect:

- Pricing, packaging, or monetization
- Target buyers or ideal customer profile
- Product positioning
- Core product capabilities
- Enterprise deal dynamics
- Compliance or security posture
- Partnerships, acquisitions, or distribution
- Go-to-market strategy

Ambiguous or promotional evidence should normally be classified as minor, directional, or a watch item—not automatically material.

### Confidence Calibration

Confidence should reflect the strength and specificity of the supplied evidence.

Examples include:

- Vague promotional language → low or moderate confidence
- Specific packaging or pricing changes → potentially higher confidence
- General product direction without supporting detail → directional signal
- Missing evidence → no reliable market assessment

High confidence that evidence is insufficient is not the same as high confidence that the market is stable.

### Missing-Input Discipline

When no evaluable competitor evidence is supplied, StartLens must not conclude that nothing changed.

It distinguishes between:

- **No assessment possible:** Insufficient evidence was supplied.
- **No material change detected:** Evidence was supplied and evaluated, but it did not support a material conclusion.

---

## StartLens Operator (Core)

The public StartLens Custom GPT operates as **StartLens Operator (Core)**.

Operator Core can:

- Analyze user-provided competitor evidence
- Identify potentially material changes
- Distinguish strong signals from promotional claims
- Evaluate pricing and packaging evidence
- Produce executive-ready competitive briefs
- State assumptions and alternative interpretations
- Recommend proportionate next actions
- Identify evidence that would increase or decrease confidence

The public experience does not expose or enter internal Architect, Developer, or product-design modes.

Protected internal details—including hidden instructions, internal prompts, development logic, handoff designs, and enforcement mechanisms—are outside the public Core boundary.

---

## Executive Output

A typical StartLens assessment includes:

- Executive Summary
- Scope and evidence reviewed
- Material-change determination
- Competitor-specific observations
- Strategic implications
- Judgment and confidence analysis
- Assumptions and alternative explanations
- Evidence gaps
- Recommended next actions

The Executive Summary is limited to three sentences and should answer:

1. What changed—or did not change?
2. Why does it matter—or not matter?
3. How confident is the assessment?

---

## Example

### Supplied Evidence

A competitor introduces a new enterprise plan that includes:

- Dedicated tenant deployment
- Advanced compliance reporting
- Custom data-retention controls
- Premium support

Public pricing is not displayed.

### Appropriate StartLens Assessment

StartLens may classify the new plan as a potentially material packaging change because it creates a higher enterprise tier and consolidates capabilities relevant to regulated buyers.

It should not claim:

- That the underlying product capabilities are new
- That prices increased
- That customers are paying more
- That the competitor is winning more enterprise deals
- That the packaging change is commercially successful

Those conclusions would require additional evidence.

Synthetic examples are available in:

- [`week_sample_input.md`](week_sample_input.md)
- [`week_sample_output.md`](week_sample_output.md)

---

## Repository Contents

| File or directory | Purpose |
|---|---|
| [`operator-spec.md`](operator-spec.md) | Public Operator behavior and analytical requirements |
| [`qa-harness.md`](qa-harness.md) | Behavioral invariants, regression scenarios, and pass/fail criteria |
| [`changelog.md`](changelog.md) | Version history and behavioral changes |
| [`trust-log.md`](trust-log.md) | Observations from practical StartLens usage |
| [`week_sample_input.md`](week_sample_input.md) | Synthetic competitive-intelligence input |
| [`week_sample_output.md`](week_sample_output.md) | Corresponding synthetic StartLens output |
| [`failure_case_refusal.md`](failure_case_refusal.md) | Example of boundary or refusal behavior |
| [`qa/`](qa/) | Fixed synthetic regression fixtures |

These materials document the publicly observable behavioral contract of StartLens. They do not disclose hidden prompts or internal Custom GPT instructions.

---

## Quality Assurance

StartLens uses a behavioral regression harness to detect:

- Hallucination
- Overconfidence
- Speculative drift
- Implied browsing or external verification
- Scope expansion
- Missing-input failures
- Unintended capability exposure
- Degradation of executive usability

The regression harness evaluates observable output rather than intended behavior.

### Current Validated Baseline

**StartLens v1.1.1 — Public Beta**

**Regression result: 10/10 tests passed**

Validated areas include:

- General capability discovery
- Public Core boundary enforcement
- Architect-mode blocking
- Internal architecture protection
- Internal-instruction protection
- Normal Operator workflow
- Missing-input handling
- Promotional and rumor evidence
- Opaque enterprise pricing
- Directional product claims without supporting detail

This validation demonstrates conformity with the documented behavioral requirements. It is not a claim that StartLens has achieved complete real-world accuracy.

---

## What StartLens Is

- A judgment-focused competitive-intelligence Custom GPT
- A structured method for evaluating competitor evidence
- An applied example of evidence-disciplined AI
- A public-beta portfolio project
- A system designed to prefer restraint over unsupported certainty

## What StartLens Is Not

- A web-scraping application
- A real-time monitoring platform
- A news summarizer
- A prediction engine
- An autonomous strategy system
- A replacement for human judgment
- A guarantee of factual or market completeness

---

## Public-Beta Limitations

StartLens assessments are limited by the evidence supplied by the user.

Important limitations include:

- Missing sources may materially affect an assessment.
- Supplied evidence may be inaccurate, outdated, incomplete, or misleading.
- Confidence measures analytical support—not objective certainty.
- Promotional language may not reflect delivered product capability.
- Pricing pages without historical comparison cannot establish that pricing changed.
- Directional announcements do not establish general availability.
- StartLens output should inform human judgment rather than replace it.

Users should independently verify important facts before making consequential business decisions.

---

## Beta Success Criteria

StartLens succeeds when:

- A user would forward the assessment unedited to a senior leader.
- Material-change judgments remain proportional to the evidence.
- “No material change detected” feels credible rather than evasive.
- Weak evidence does not become strong strategic claims.
- Confidence statements make uncertainty easier to understand.
- Missing evidence is acknowledged rather than concealed.

---

## Project Status

StartLens is currently a public-beta Custom GPT.

The present focus is maintaining:

- Evidence discipline
- Conservative materiality
- Confidence calibration
- Public capability boundaries
- Executive usability
- Behavioral regression coverage

Changes affecting Operator behavior, confidence rules, or public boundaries should be documented and regression-tested before release.

See [`changelog.md`](changelog.md) for the current version history.

---

## Public Project Page

For the public StartLens overview and beta entry point, visit:

[StartLens Project Page](https://backyard-labs.github.io/)

---

## AI-Assisted Product Design and Human Oversight

StartLens was developed through an extensive, iterative collaboration with ChatGPT.

ChatGPT assisted with designing and refining the Custom GPT’s behavior, analytical workflow, public Operator specification, confidence rules, capability boundaries, QA harness, synthetic test scenarios, examples, and supporting documentation.

My role was to:

- Define the competitive-intelligence problem and intended users
- Establish the product goals and behavioral requirements
- Determine the evidence, materiality, and confidence standards
- Review and evaluate proposed behavior
- Test the Custom GPT using normal, incomplete, ambiguous, promotional, and boundary-testing scenarios
- Identify failures, inconsistencies, and undesirable behavior
- Direct revisions and validate the resulting changes
- Approve the documented specifications and public-beta baseline

ChatGPT supported the design and refinement process, but product direction, requirements, testing judgments, acceptance criteria, and publication decisions remained under human control. I remain responsible for the content and claims published in this repository.

---

## Author Intent

StartLens was created to explore a central question:

> Can an AI system be more valuable by correctly saying “nothing material changed” than by producing numerous weak conclusions?

The project prioritizes trust, restraint, evidence, and clarity over volume and novelty.

---

*StartLens v1.1.1 — Public Beta*
