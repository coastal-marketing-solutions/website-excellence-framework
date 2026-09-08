# Governance — 14. Risk Management

*Core Methodology — Governance, Sec. 14. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 14. Risk Management

### 14.1 Purpose

Provides a standard mechanism for identifying, tracking, and mitigating risks to engagement success — schedule, compliance, technical, or client-relationship risks — before they become issues. Identical in structure across every industry; the specific risk content varies by the active Industry Module.

### 14.2 Risk Register Schema

| Field | Description |
|---|---|
| Risk ID | Format `RISK-{sequence}` |
| Description | What could go wrong |
| Category | Schedule / Compliance / Technical / Client Relationship / Scope / Module Gap |
| Likelihood | Low / Medium / High |
| Impact | Low / Medium / High |
| Mitigation Plan | Specific action(s) to reduce likelihood or impact |
| Owner | Who is responsible for monitoring/mitigating |
| Status | Open / Mitigated / Realized (became an Issue) / Closed |

### 14.3 Standard WEF Risk Categories to Screen For

- **Compliance/professional-standards drift**: content or design implying claims, guarantees, or outcomes without required qualifying language — specifics vary by Industry Module, but the risk category is universal.
- **Scope creep at Information Architecture/UX gates**: site structure growing beyond Charter-approved page counts without a Change Request.
- **Client bottleneck risk**: dependency on a single client stakeholder (e.g., for practitioner bios, compliance review) with no backup path.
- **Platform lock-in risk**: build decisions that would be costly to reverse if the client later leaves the default stack.
- **AI hallucination risk**: AI-produced statistics, competitor claims, or regulatory statements presented as fact without a verifiable source — screened for explicitly at every Stage Gate's Review Process.
- **Module Gap risk**: the active Industry Module lacks coverage for a situation the engagement has encountered, and the gap has not yet been escalated per Section 9.5.

### 14.4 Escalation Policy

Any risk rated High/High is escalated to the Engagement Lead within 24 hours of identification and reviewed at the next standing engagement meeting regardless of normal cadence.
