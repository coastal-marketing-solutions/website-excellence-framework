# CORE METHODOLOGY — UX & CONVERSION

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

This chapter covers Stage Gate 6: UX & Conversion. It follows the fixed 19-part Stage Gate template defined in the Research chapter's introduction. This gate designs the audience-facing user experience — primary conversion flows, page-level UX patterns, and the friction-reduction mechanics that convert anonymous traffic into qualified leads or desired actions — and it is where the active Industry Module's Trust Signal Requirements have their single biggest impact on the engagement.

---

# STAGE GATE 6 — UX & CONVERSION

## 1. Purpose

Design the audience-facing user experience: primary conversion flows (quote/estimate requests, consultation booking, application starts, contact/schedule), page-level UX patterns, and the friction-reduction mechanics that convert anonymous traffic into qualified leads.

## 2. Business Objectives

- Minimize friction in the path from landing page to qualified lead action for each priority persona.
- Define calculator/tool and interactive feature specifications that serve genuine audience decision-making (not just lead-capture bait).
- Establish trust-building UX patterns appropriate to the client's industry, using the active Industry Module's Trust Signal Requirements as the baseline.

## 3. Inputs

Sitemap & Navigation Model (Stage Gate 4), Keyword-to-Page Map (Stage Gate 5), Client Personas (Stage Gate 1), Positioning & Messaging Pillars (Stage Gate 3), active Industry Module's Trust Signal Requirements and typical calculators/tools

## 4. Outputs

- Primary Conversion Flow Diagrams (one per priority persona/offering combination)
- Calculator & Interactive Tool Specifications
- Page-Level UX Pattern Library (wireframe-level, pre-visual-design)
- Trust Signal Placement Plan
- Conversion Measurement & Operational Handoff Contract (events, consent, destination, owner, response expectation, and failure fallback)

## 5. Required Documents

`/06-ux-conversion/conversion-flows-v1.md`, `/06-ux-conversion/calculator-specs-v1.md`, `/06-ux-conversion/ux-pattern-library-v1.md`, `/06-ux-conversion/trust-signal-plan-v1.md`, `/06-ux-conversion/conversion-measurement-contract-v1.md`

## 6. Responsible Roles

UX Designer (lead), Strategy Consultant (persona alignment), Information Architect (structural consistency)

## 7. Required Specialists

Developer (feasibility check on calculator logic and any practice-management/CRM integration points), Compliance/Standards Liaison (mandatory review of calculator/tool outputs and any language implying a guarantee, outcome, or commitment per the active Industry Module)

## 8. Decision Authority

**Client sign-off required** on Primary Conversion Flow Diagrams before Design begins — UX flows are expensive to change once visual design work starts.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Trust Signal Requirements** before designing the Trust Signal Placement Plan, and its typical **calculators/interactive tools** (found in the Module's Content Model & Page Types or a dedicated tools section) before specifying calculators — do not invent a generic "contact form" experience when the vertical has a well-established, higher-converting tool pattern (e.g., an affordability calculator, a case-value estimator, a project-cost estimator, a symptom/intake checker, a plan-fee comparison tool).

## 10. Workflow

```
[1] Map each priority persona's ideal conversion path from entry point to
    qualified lead action, in wireframe-level detail (no visual design
    yet)
        │
        ▼
[2] Specify calculator/interactive tool logic using the Module's typical
    tools as a starting point: inputs, outputs, disclaimer requirements,
    and what happens to the output (lead capture trigger? informational
    only?)
        │
        ▼
[3] Define page-level UX patterns reused across the site (hero patterns,
    CTA patterns, form patterns, FAQ patterns, trust-signal patterns)
        │
        ▼
[4] Define Trust Signal Placement Plan using the Module's Trust Signal
    Requirements: where credentials, licensing/registration info,
    security badges, reviews, and practitioner/staff credentials appear
    across templates
        │
        ▼
[5] Compliance/Standards review of calculator outputs and flow copy
        │
        ▼
[6] Define measurement, consent, routing, response expectation, and
    failure fallback for each meaningful action
        │
        ▼
[7] Client review and sign-off on conversion flows
        │
        ▼
[8] Exit Criteria → Design discipline scheduled
```

## 11. Checklist

- [ ] Active Industry Module's Trust Signal Requirements and typical calculators/tools reviewed before drafting
- [ ] A conversion flow diagram exists for every priority persona/offering combination identified in Stage Gate 3
- [ ] Every calculator/tool has a fully specified input/output/disclaimer set, reviewed by the Compliance/Standards Liaison
- [ ] UX Pattern Library covers, at minimum: hero, primary CTA, lead capture form, FAQ accordion, practitioner/staff bio card, trust signal bar, comparison/data table
- [ ] Trust Signal Placement Plan specifies exact template locations, not just "include trust signals somewhere," and matches the Module's Trust Signal Requirements
- [ ] Every primary conversion action has a named event, trigger, destination/owner, consent category, no-PII parameter rule, user-facing success/failure state, and operational response expectation
- [ ] Lead-routing, booking, notification, and fallback paths have been tested or explicitly marked as a build dependency; the site never promises a response time the operating team has not confirmed
- [ ] Client has formally signed off on conversion flows

## 12. Prompt(s)

**Prompt 6.1 — Conversion Flow Design**

```
You are the UX Designer for [Client Name] in the [Industry Module name]
vertical. For the persona "[Persona Name]" seeking "[Offering]", design a
wireframe-level conversion flow from first landing-page view to qualified
lead action. Specify each screen/step, the single primary action available
at each step, what friction-reduction technique is used (e.g., progressive
disclosure, save-and-resume, minimal upfront information requirements),
and where in the flow trust signals (per the [Industry Module]'s Trust
Signal Requirements) should appear. Do not specify visual design — this is
structure and content of steps only.
```

**Prompt 6.2 — Calculator/Tool Specification**

```
Specify a [tool type, per the Industry Module's typical tools — e.g.,
"affordability calculator," "case-value estimator," "project-cost
estimator"] for [Client Name]'s site. Define: required inputs, optional
inputs, the calculation logic in plain language (not code), the output
presentation, required disclaimer language placement (flag for
Compliance/Standards Liaison review — do not draft final disclaimer legal
text yourself), and whether the output triggers a lead capture prompt or
remains purely informational. State any assumption that needs compliance
confirmation explicitly.
```

## 13. Examples

*Generic conversion flow pattern (condensed):*

```
Landing Page (offering hub, organic entry)
   → Primary CTA: interactive tool (per Module), no contact info
     required to see result
   → Tool Result Screen: estimated result + soft CTA "Get a personalized
     [quote/consultation/assessment]" (contact info required)
   → Request Form (3 fields, progress-saved)
   → Confirmation Screen: expected response time + trust signal
     (practitioner/staff photo/bio preview)
```

See each Industry Module for fully worked, vertical-specific conversion flows and calculator specifications.

## 14. Common Mistakes

- Requiring contact information before any value (a calculator/tool result) is delivered, which increases bounce on cost-sensitive or hesitant personas.
- Designing calculators/tools that function as disguised lead-gen forms with no genuine value — audiences detect this and it damages trust.
- Skipping compliance review of calculator/tool disclaimer placement, creating rework at QA & Optimization.
- Ignoring the active Industry Module's known high-converting tool pattern and defaulting to a generic contact form when the vertical supports something far more effective.
- Treating a successful form submission as the business outcome without verifying that the lead reaches the right owner, that the user sees a clear next step, and that a failure path exists when email, CRM, scheduling, or telephony is unavailable.

## 15. Best Practices

- Give genuine value (a real estimate/result) before asking for contact information wherever compliance and business model allow it — this is consistently one of the highest-leverage trust and conversion levers available, across every industry this framework serves.
- Reuse a small number of well-designed UX patterns across many pages rather than one-off page designs — this both improves usability consistency and reduces Development-phase build complexity.
- Design save-and-resume for any multi-step flow; high-consideration decisions (a loan, a legal engagement, a medical relationship, a major purchase) are rarely completed in a single session.
- Treat the Conversion Measurement & Operational Handoff Contract as part of the UX, not a tag-manager afterthought. The visitor's confirmation state, response expectation, privacy/consent choice, and fallback contact path are part of the experience.

## 16. Review Process

UX Designer presents flows to Engagement Lead and Compliance/Standards Liaison jointly; Developer confirms technical feasibility of calculator/tool logic and any integration points before client presentation.

## 17. Quality Assurance

Primary Eight-Dimension focus: **Conversion**, **Accessibility** (flow must be fully keyboard/screen-reader navigable), **Brand** (flow tone consistent with positioning).

## 18. Exit Criteria

- [ ] All five Required Documents approved
- [ ] Compliance/Standards Liaison has signed off on calculator/tool logic and disclaimer placement
- [ ] Client has formally approved Primary Conversion Flow Diagrams

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all five Required Documents saved v1.0
- Blueprint: "UX Flows" section populated with flow references and pattern library
- Decision Register: log client-approved conversion flow decisions as `DEC-SG6-00x` (rated Costly to Reverse — changes after Design begins trigger a Change Request)

UX flows are translated into visual form in the Design discipline, stress-tested in Prototype Validation, and measured against real conversion data in Post-Launch Growth Program, where flow adjustments are proposed as data-driven experiments rather than opinion-driven redesigns.

---

*End of UX & Conversion. Continue to Core Methodology — Design.*
