# Regression: Material Change

This dataset is synthetic and fixed for regression testing.

Purpose: verify that StartLens distinguishes one concrete material packaging change from weaker promotional and directional signals.

Dataset:

Industry: B2B cybersecurity SaaS

Persona: VP Product / Head of Strategy

Primary Executive Question:
What materially changed this week that could affect positioning, enterprise deals, or roadmap priorities?

Competitor 1: Northstar Secure

Source:
Public pricing page

Date:
2026-08-11

Update:
Northstar Secure added a new "Enterprise Plus" plan above its existing Standard, Pro, and Enterprise tiers.

The Enterprise Plus tier includes:

- Dedicated tenant option
- 24/7 premium support
- Advanced compliance reporting
- Custom data-retention controls

Pricing is not publicly listed and requires contacting sales.

---

Competitor 2: VectorShield

Source:
Product announcement

Date:
2026-08-10

Update:
"VectorShield is excited to introduce our most advanced AI-powered threat detection experience yet. The latest release helps security teams work faster, investigate smarter, and stay ahead of evolving threats."

No feature specifications, benchmarks, customer examples, pricing changes, release documentation, or general-availability details were included in the announcement.

---

Competitor 3: CloudHarbor Security

Source:
Company blog and careers page

Date:
2026-08-09

Update:
CloudHarbor Security stated that it is "expanding its cloud security platform to meet growing enterprise demand."

The company also posted four new engineering roles:

- Senior Cloud Detection Engineer
- Staff Kubernetes Security Engineer
- Principal Identity Security Engineer
- Senior Platform Reliability Engineer

The blog did not provide launch dates, product names, pricing changes, customer metrics, or specific roadmap commitments.

Expected Behavior:

* Northstar Secure should be treated as the strongest and likely material signal.
* VectorShield should be treated as promotional or weakly substantiated.
* CloudHarbor Security should be treated as directional but not a confirmed product change.
* The overall result should not be "No material change detected."
