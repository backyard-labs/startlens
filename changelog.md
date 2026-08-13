# StartLens Changelog

## v1.1.1 — Core Boundary Hardening

- Separated the public StartLens Core experience from internal Architect capabilities:
  - StartLens Operator (Core) is now the default and only public-facing role
  - Removed public access to Architect, Developer, and product-development modes
  - Protected internal architecture, prompts, handoff schemas, storage design, build plans, and enforcement rules
- Updated Operator behavior:
  - Operator remains the active role after brief delivery
  - Public capability questions remain within StartLens Core
  - High-level, publicly observable StartLens behavior can still be explained
- Preserved the existing v1.1 analytical and confidence behavior without intentional changes
- Completed an 8-test boundary and functional regression suite:
  - General capability discovery
  - Agentic CI MVP request
  - Architect Mode invocation
  - Internal architecture request
  - Internal instruction request
  - Normal Operator workflow
  - Missing-input behavior
  - Messy/promotional/rumor evidence
- Regression result: 8/8 tests passed with no observed loss of Core analytical functionality
- Beta observations retained for further testing:
  - Conversation Starters may not be visible across all tested ChatGPT interfaces
  - High confidence in an evidence-insufficiency judgment may require clearer semantics to avoid being mistaken for high confidence in the underlying market state

## v1.1 — Operator Spec (Behavioral Freeze)

- Locked Operator Mode execution discipline:
  - Input-only analysis, no browsing, no scope expansion
  - Exec Summary max 3 sentences with redundancy rule
- Added Missing-Input Confidence Rule:
  - Confidence ≤ 0.50 when no evaluable inputs are provided
  - Confidence explicitly framed as procedural completeness, not market certainty
- Reinforced “No material change detected” as valid/preferred outcome under weak evidence

## v1.0 — Initial Operator Workflow

- Introduced Operator Mode concept and weekly executive CI brief format
- Added Judgment & Confidence Layer across analysis
- Established conservative materiality definition and “watch items” posture
