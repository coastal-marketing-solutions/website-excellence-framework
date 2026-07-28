# CORE METHODOLOGY — QA & OPTIMIZATION

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

This chapter covers the final two Stage Gates of every WEF engagement: Quality Assurance and the Post-Launch Growth Program. Both follow the fixed 19-part template defined in the Research chapter's introduction. Stage Gate 11 carries the last mandatory compliance/professional-standards checkpoint before launch, in any regulated vertical — it cannot be waived regardless of schedule pressure.

---

# STAGE GATE 11 — QUALITY ASSURANCE

## 1. Purpose

Formally validate the staged website against every standard set across the engagement — functional, performance, accessibility, SEO, compliance, and brand fidelity — before go-live authorization.

## 2. Business Objectives

- Catch and remediate defects before they reach visitors or search engines index a flawed site.
- Provide the client with an evidence-based go-live recommendation, not a subjective "looks ready" assessment.
- Establish the compliance sign-off record required, in any regulated vertical, before the site goes live.

## 3. Inputs

Staging site (SG10.5), all prior Stage Gate approved specifications (used as the QA reference standard), Compliance Clearance Log (SG9), active Industry Module's Regulatory & Compliance Landscape (final QA checklist)

## 4. Outputs

- QA Test Report (functional, performance, accessibility, SEO)
- Compliance Sign-Off Record (final, site-wide)
- Issue Log (defects found, severity, remediation status)
- Go-Live Recommendation

## 5. Required Documents

`/11-qa/qa-test-report-v1.md`, `/11-qa/compliance-signoff-record-v1.md`, `/11-qa/issue-log-v1.md`, `/11-qa/go-live-recommendation-v1.md`

## 6. Responsible Roles

QA Analyst (lead), Developer (remediation), SEO Specialist (SEO QA), Visual Designer (design fidelity QA)

## 7. Required Specialists

Compliance/Standards Liaison (**mandatory final sign-off wherever the active Industry Module flags the vertical as regulated** — this is the last compliance gate before launch)

## 8. Decision Authority

**Client sign-off required for go-live.** The named Decision Authority approves the Go-Live Recommendation; Compliance/Standards Liaison sign-off on the Compliance Sign-Off Record is a hard prerequisite that cannot be waived regardless of client urgency, wherever applicable.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's full **Regulatory & Compliance Landscape** as the final site-wide compliance QA checklist — this is the last opportunity to catch a missing disclosure, credential display, or required statement before launch.

## 10. Workflow

```
[1] Functional QA: every form, calculator, navigation path, and
    integration tested against the Build Manifest and Conversion Flows
        │
        ▼
[2] Performance QA: Core Web Vitals tested on production-equivalent
    staging across representative templates (mobile + desktop)
        │
        ▼
[3] Accessibility QA: automated scan + manual keyboard/screen-reader
    testing against WCAG 2.1 AA
        │
        ▼
[4] SEO QA: schema validation, meta tag audit, internal linking audit,
    XML sitemap/robots.txt verification, indexation settings check
        │
        ▼
[5] Design Fidelity QA: staging compared page-by-page against Stage
    Gate 7.5 approved design system
        │
        ▼
[6] Compliance QA: final site-wide review against the active Industry
    Module's Regulatory & Compliance Landscape, the Compliance Clearance
    Log, and the Compliance Content Checklist
        │
        ▼
[7] Issue Log compiled, severity-rated, remediated, re-tested
        │
        ▼
[8] Go-Live Recommendation drafted → client review → sign-off
```

## 11. Checklist

- [ ] Every form and calculator tested for correct function, validation, and error states
- [ ] Core Web Vitals pass targets on representative templates, mobile and desktop
- [ ] Automated accessibility scan shows no critical/serious WCAG 2.1 AA violations; manual keyboard navigation confirmed functional site-wide
- [ ] Schema markup validated (no errors) via structured data testing tool
- [ ] XML sitemap submitted-ready, robots.txt correct, no unintended noindex tags
- [ ] Design fidelity spot-checked against approved templates for every page type
- [ ] Compliance/Standards Liaison has completed final site-wide Compliance Sign-Off Record against the active Industry Module's full Regulatory & Compliance Landscape
- [ ] All P0/P1 Issue Log items remediated and re-tested; any open P2 items documented with client-accepted risk

## 12. Prompt(s)

**Prompt 11.1 — QA Test Plan Generation**

```
You are the QA Analyst for [Client Name]'s website launch in the
[Industry Module name] vertical. Using the Build Manifest and Conversion
Flow diagrams, generate a functional test plan covering every form,
calculator, and primary navigation path. For each test case, specify: the
action taken, the expected result, and the pass/fail criteria. Include
edge cases (invalid input handling, required field validation, mobile
viewport behavior) for every calculator and lead capture form.
```

**Prompt 11.2 — Issue Log Triage**

```
Given the attached raw QA findings for [Client Name]'s site, and the
[Industry Module]'s Regulatory & Compliance Landscape, organize them into
an Issue Log with columns: Issue ID, Description, Page/Location, Category
(Functional/Performance/Accessibility/SEO/Compliance/Design), Severity
(P0 = blocks launch, P1 = fix before launch if feasible, P2 = post-launch
acceptable), and a recommended remediation. Flag any compliance-category
issue as automatically P0 regardless of apparent severity.
```

## 13. Examples

*Generic Issue Log entry pattern:*

| Issue ID | Description | Page | Category | Severity | Remediation |
|---|---|---|---|---|---|
| ISS-014 | Required credential/license identifier not visible in footer on mobile viewport (hidden behind collapsed menu) | Site-wide (mobile) | Compliance | P0 | Move identifier display outside collapsible footer menu; re-test on 3 device widths |

See each Industry Module's Regulatory & Compliance Landscape for the specific identifiers/disclosures/statements that generate this class of finding in that vertical (NMLS ID for mortgage lending, license number for real estate/law/medicine, registration/CRD number for financial advisors, etc.).

## 14. Common Mistakes

- Treating compliance issues as negotiable severity based on launch timeline pressure — compliance issues are categorically P0 in this methodology, in every regulated vertical.
- Testing only on desktop, missing mobile-specific defects (a majority of research/discovery traffic across most of these verticals is mobile).
- Allowing "it looks done" to substitute for the structured test plan — undocumented QA is not defensible if a defect surfaces post-launch.
- Running compliance QA against a generic checklist instead of the active Industry Module's actual, current Regulatory & Compliance Landscape.

## 15. Best Practices

- Run accessibility and compliance QA as dedicated passes, not folded into general functional testing, since they require different expertise and a different failure tolerance (zero for compliance).
- Re-test every remediated P0/P1 issue explicitly rather than assuming a fix worked — regression risk is real, especially with caching layers involved.
- Present the Go-Live Recommendation with the full Issue Log attached, including any client-accepted P2 risk, so the launch decision is fully informed and documented.

## 16. Review Process

QA Analyst compiles findings; Engagement Lead reviews Issue Log severity ratings; Compliance/Standards Liaison independently completes final sign-off; client reviews Go-Live Recommendation for final approval.

## 17. Quality Assurance

This gate formally re-verifies all Eight Dimensions (Governance, Sec. 12.2) site-wide — it is the methodology's final comprehensive checkpoint, in any industry.

## 18. Exit Criteria

- [ ] All Required Documents complete
- [ ] Compliance Sign-Off Record completed and signed (where applicable)
- [ ] All P0 issues remediated and re-tested; no open P0 items
- [ ] Client has approved Go-Live Recommendation

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "QA Status" section finalized with sign-off record
- Decision Register: log go-live approval as `DEC-SG11-001`; log any client-accepted open P2 risk explicitly as `DEC-SG11-002`

Post-launch, the QA test plan is reused for regression testing after any Post-Launch Growth Program change.

---

# STAGE GATE 11.5 — POST-LAUNCH GROWTH PROGRAM

## 1. Purpose

Establish the structured, data-driven optimization program for the first 90 days (and ongoing) after launch — closing the loop from strategic hypothesis (Research discipline) through measured real-world performance.

## 2. Business Objectives

- Validate or invalidate the personas, positioning, and conversion assumptions made in Research, SEO & Architecture, and Design against real behavioral data.
- Establish a KPI dashboard and experiment cadence so improvement is continuous rather than one-time.
- Feed validated learnings back into both the client's Knowledge Base and, where applicable, the active Industry Module, for reuse in future engagements in that vertical.

## 3. Inputs

Live production site, GA4/Search Console/Clarity data (accumulating from launch), Success Metrics defined in Project Charter, Master Website Blueprint (full, as of launch), active Industry Module's Persona Library and Content Model (for expansion)

## 4. Outputs

- 90-Day Growth Program Plan
- KPI Dashboard Specification
- Experiment Log (A/B or sequential test tracking)
- Engagement Retrospective & Methodology Learnings Memo

## 5. Required Documents

`/11.5-post-launch/growth-program-plan-v1.md`, `/11.5-post-launch/kpi-dashboard-spec-v1.md`, `/11.5-post-launch/experiment-log-v1.md`, `/11.5-post-launch/retrospective-learnings-v1.md`

## 6. Responsible Roles

Strategy Consultant (lead — reconnects growth work to original strategic hypotheses), SEO Specialist (ranking/traffic monitoring), UX Designer (conversion experiment design)

## 7. Required Specialists

Developer (implement experiment variants), Compliance/Standards Liaison (review any new content/experiment copy per the same standard as Stage Gate 9)

## 8. Decision Authority

Engagement Lead approves the Growth Program Plan; ongoing experiment decisions follow the same Decision Register discipline as the rest of the engagement, with client informed per the cadence set in the Project Charter.

## 9. Module Injection Point(s)

> **Module Injection Point:** Compare production behavior against the active Industry Module's **Persona Library** to confirm or refine which archetypes actually match this client's real audience; any confirmed refinement is a candidate to propose back into the Module (Governance, Sec. 9.5) so future engagements in the same vertical start from better-validated personas. New content additions should continue to follow the Module's **Content Model & Page Types**.

## 10. Workflow

```
[1] Confirm KPI Dashboard is correctly capturing Success Metrics from
    the Project Charter (traffic, conversion rate, ranking positions,
    Core Web Vitals in production)
        │
        ▼
[2] Baseline first 2-4 weeks of production data
        │
        ▼
[3] Compare actual audience behavior against the Stage Gate 1 personas
    (and the active Industry Module's Persona Library) and Stage Gate 3
    positioning assumptions; note confirmations and surprises
        │
        ▼
[4] Prioritize a 90-day experiment roadmap (content additions, UX
    refinements, new topical cluster expansion) using the same Content
    Depth Standard (SG8) and Design System (SG7.5) discipline — no ad
    hoc changes outside the governed system
        │
        ▼
[5] Execute experiments; log each in the Experiment Log with hypothesis,
    result, and decision
        │
        ▼
[6] At 90 days (or Charter-defined interval), produce the Engagement
    Retrospective & Methodology Learnings Memo, including any proposed
    refinement to the active Industry Module
```

## 11. Checklist

- [ ] KPI Dashboard verified accurate against Project Charter Success Metrics
- [ ] Baseline production data captured before first experiment begins
- [ ] Every experiment logged with a clear hypothesis and success criterion before it starts, not just a result after the fact
- [ ] Any new content follows Stage Gate 8/9 discipline (brief → compliance-cleared copy), not ad hoc publishing
- [ ] Retrospective Memo completed and submitted to the firm's Knowledge Base for cross-engagement reuse, with any Module refinement proposed via Change Request

## 12. Prompt(s)

**Prompt 11.5.1 — Growth Program Prioritization**

```
Using production KPI data from [Client Name]'s first 30 days live, the
original Client Personas (Stage Gate 1), the [Industry Module]'s Persona
Library, and the Keyword-to-Page Map (Stage Gate 5), identify: (1) which
personas' behavior matched predictions and which diverged, citing
specific metrics; (2) which topical clusters are underperforming their
keyword targets and why (ranking, content depth, or technical issue);
(3) 3-5 prioritized experiment or content-expansion recommendations with
a stated hypothesis and success metric for each. Do not recommend a full
redesign or repositioning without explicit evidence of a fundamental
strategic mismatch — prefer incremental, testable changes.
```

**Prompt 11.5.2 — Retrospective & Methodology Learnings**

```
Produce an Engagement Retrospective for [Client Name]'s WEF engagement in
the [Industry Module name] vertical. Cover: what strategic assumptions
from Stage Gate 3 were validated or invalidated by post-launch data; which
Stage Gates ran smoothly vs. which caused rework, and why; any Core
Methodology improvement recommendation (submit as a Core Change Request);
any Industry Module refinement recommendation — new persona, corrected
compliance detail, better keyword pattern, additional trust signal — to
submit as a Module-level Change Request so future engagements in this
vertical benefit.
```

## 13. Examples

*Generic Experiment Log entry pattern:*

| Experiment ID | Hypothesis | Change | Success Metric | Result | Decision |
|---|---|---|---|---|---|
| EXP-003 | Removing a required field from the calculator's first step will reduce abandonment | A/B test: calculator with reduced first-step fields vs. control | Calculator completion rate | Variant: +18% completion, lead quality unchanged per follow-up | Ship variant site-wide; log as `DEC-SG11.5-004` |

## 14. Common Mistakes

- Making design or content changes directly on production without following the same brief/compliance discipline used pre-launch, quietly eroding the governance system the whole engagement was built on.
- Running experiments without a predefined success metric, leading to post-hoc rationalization of whatever happened.
- Treating the Retrospective Memo as optional paperwork rather than the mechanism that makes the next WEF engagement — in this vertical or any other — better than this one.
- Discovering a genuine Module gap or persona refinement and never proposing it back into the Industry Module, forcing the next engagement in that vertical to rediscover it from scratch.

## 15. Best Practices

- Treat every post-launch content addition as a miniature Stage Gate 8→9 cycle — brief, compliance clearance, then publish — never skip steps because the site is already live.
- Feed every validated learning (both confirmations and surprises) back to the firm's cross-engagement Knowledge Base and, where genuinely generalizable to the vertical, into the active Industry Module via Change Request — this is the mechanism by which the Module library compounds in value over time (Governance, Sec. 9.5, 13.2).

## 16. Review Process

Strategy Consultant and Engagement Lead review the Growth Program Plan and Experiment Log at each Charter-defined reporting interval; Compliance/Standards Liaison reviews any new content or experiment copy exactly as in Stage Gate 9.

## 17. Quality Assurance

All Eight Dimensions remain in force for any new work produced during this gate; performance and SEO dimensions are additionally now measured against real data rather than projections.

## 18. Exit Criteria

This gate does not "close" in the same sense as prior gates — it establishes an ongoing program. Its formal completion checkpoint (typically at 90 days or the Charter-defined interval) requires:

- [ ] KPI Dashboard operating and reviewed at agreed cadence
- [ ] At minimum 3 experiments logged with documented results
- [ ] Retrospective & Methodology Learnings Memo submitted

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents maintained as living documents, versioned per the Governance discipline's Version Control policy
- Blueprint: "Growth Program" section populated and continuously updated
- Decision Register: every shipped experiment logged as a standard Decision Register entry

The Retrospective Memo feeds the firm's Change Request process for both the Core Methodology and the active Industry Module, and the accumulated cross-engagement, cross-industry learnings inform future Research-discipline work more efficiently over time — this is the mechanism by which WEF becomes more valuable, in every vertical it serves, with every engagement run.

---

*End of QA & Optimization. Continue to Core Methodology — AI Workflows.*
