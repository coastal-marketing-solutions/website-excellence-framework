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

`11-qa/output/QA-Test-Report.md`, `11-qa/output/Compliance-Signoff-Record.md`, `11-qa/output/Issue-Log.md`, `11-qa/output/Go-Live-Recommendation.md`

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

- [ ] Every form and calculator tested for correct function, validation, accessibility, spam/abuse handling, success and failure states, duplicate prevention, and end-to-end receipt in the intended CRM/email/scheduling destination by the named operational owner
- [ ] Core Web Vitals pass targets on representative templates, mobile and desktop
- [ ] Automated accessibility scan shows no critical/serious WCAG 2.1 AA violations; manual keyboard navigation confirmed functional site-wide
- [ ] Schema markup validated (no errors) via structured data testing tool
- [ ] XML sitemap submitted-ready, robots.txt correct, no unintended noindex tags
- [ ] After a material publication, migration, or new page-cluster release, sitemap membership and a bounded representative URL sample are verified in the applicable search-engine property across each new template, hierarchy, locale, and risk class; final status, canonical, robots directive, discovered/indexed state, and alternate-page selection are recorded. Submission/inspection is evidence of discovery processing, not a guarantee of indexing or ranking.
- [ ] Representative rendered pages have one intended title, meta description, canonical, robots directive, and coherent schema graph; Capability Ownership Matrix outputs show no theme/plugin/custom-code collisions
- [ ] Link-audit findings classified by actual response and link purpose before remediation; bot-blocked 401/403/429 results and unchecked URLs are not mislabeled as broken without secondary verification
- [ ] Design fidelity spot-checked against approved templates for every page type
- [ ] Compliance/Standards Liaison has completed final site-wide Compliance Sign-Off Record against the active Industry Module's full Regulatory & Compliance Landscape
- [ ] All P0/P1 Issue Log items remediated and re-tested; any open P2 items documented with client-accepted risk
- [ ] Analytics/tag/plugin-integration connected accounts verified as correct **for this specific client site**, not assumed correct because the plugin/tool is configured correctly in general — mandatory wherever the operator manages more than one active client site through any shared tool connection
- [ ] Paid plugins/integrations verified across all five states: code installed, code active, subscription current, intended account connected, and exact site/property assigned to the paid entitlement; premium badge/capability and authenticated update path confirmed from both site and vendor account where available
- [ ] Analytics/marketing/remarketing tags verified as **consent-gated, not merely firing correctly** (Governance, Sec. 15.4, RETRO-008) — load the site pre-consent and directly confirm no tracking cookies are set and no analytics network request fires; then confirm both the decline path (tags stay off) and the accept path (tags fire, cookies appear) work correctly. "Verified firing" alone is not sufficient QA sign-off for any tag capable of setting a tracking cookie.
- [ ] Meaningful business events (for example qualified form completion, booked appointment, completed checkout, or verified phone/email interaction) tested in debug/realtime reporting with documented names and parameters; no personally identifiable information is sent in analytics event names, URLs, or parameters
- [ ] Representative imported/bulk-edited pages are re-read from the public or authenticated destination after a fresh load; titles, slugs, status, body sections, links, metadata, schema, and language routes match the approved source record
- [ ] Every templated or cloned locality page sample has its map, geographic embed/query, coordinates, local imagery, captions/alt text, and named geography checked against that page; no inherited locality data remains from the source template
- [ ] Launch monitoring owner, first 24-hour/72-hour checks, alert thresholds, and rollback triggers are documented for uptime, forms/lead routing, analytics consent, indexation, redirects, and critical templates
- [ ] Search Discovery Setup (Stage Gate 11.5, Sec. 10.1) is prepared for go-live: the account that will own each search-engine property and local profile is decided, the SEO plugin's verification and analytics settings are confirmed with no duplicate analytics code, and every owner-only step is on the Action Items Sheet (Handoff and Action Items Sheet cadence, AI Workflows Sec. 2.6)
- [ ] Every third-party custom domain passes DNS/TLS/callback/cookie/canonical checks and an alternate-route bypass test; the provider/preview/origin URL cannot evade required authentication
- [ ] Content Freshness Register reviewed for launch: overdue or event-expired claims are refreshed, qualified, archived, redirected, consolidated, or noindexed before sign-off
- [ ] A representative sample of pages actually Published (not just staged in Draft) and re-tested post-Publish before the full go-live moment, specifically to surface Publish-only defects (see Sec. 14 addendum) while there's still time to fix them

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
- Treating a CMS/import log, cached admin table, or same-session editor view as the public truth without a fresh read-path check.
- Launching without an owner for the first post-release monitoring window, so a broken form, misrouted lead, accidental noindex, redirect loop, or analytics/privacy defect remains undetected.
- Treating a form's on-screen success message as proof of conversion while the notification, CRM record, booking, or assigned-owner receipt silently fails.
- Treating “PRO installed” as proof of a paid entitlement without checking the connected vendor account and exact site assignment.
- Protecting only a branded custom hostname while an unprotected provider or preview URL reaches the same private application.
- Leaving a time-sensitive guide live indefinitely because it was accurate on its original publication date.
- Signing off analytics/tag QA as soon as the tag is confirmed to fire, without separately confirming it only fires with consent — a real-world engagement ran unconsented tracking in production for days because "firing correctly" was treated as equivalent to "compliant," when it is not (Governance, Sec. 15.4, RETRO-008).

## 15. Best Practices

- Run accessibility and compliance QA as dedicated passes, not folded into general functional testing, since they require different expertise and a different failure tolerance (zero for compliance).
- Re-test every remediated P0/P1 issue explicitly rather than assuming a fix worked — regression risk is real, especially with caching layers involved.
- Present the Go-Live Recommendation with the full Issue Log attached, including any client-accepted P2 risk, so the launch decision is fully informed and documented.
- Treat release verification as a separate evidence pass: check the source artifact, destination record, rendered page, headers/schema, and meaningful-action path. A green plugin score or successful import is not a substitute for this chain.
- Schedule a short post-release observation window (at minimum first-day and third-day checks) with named owners and explicit rollback criteria. Convert recurring alerts into a monitored-control decision rather than relying on memory.
- Use a real test lead routed to a controlled destination for final form QA, then confirm receipt with the operational owner and remove or label the test record according to the client's data-handling procedure.

**Draft status hides real build gaps that only surface at Publish — plan a Publish rehearsal, don't rely on Draft-status QA alone.** Where a compliance strategy deliberately holds every page in Draft until a single bulk pre-launch review (a legitimate, confirmed real-world pattern — batching sign-off rather than clearing pages one at a time), be aware of its real cost: defects that only manifest on Publish — slug collisions, a missing static-front-page configuration, an unbuilt navigation menu that was never exercised while pages were invisible — stay completely undetected throughout the entire build and QA phase and surface for the first time at the exact moment of go-live, when there's the least slack to fix them. This happened multiple times, independently, on a single real engagement. Mitigate it with a **Publish rehearsal**: actually Publish a representative subset of pages (then optionally revert to Draft if the compliance strategy requires it) before the real go-live moment, specifically to exercise the Publish-only code paths early, rather than trusting Draft-status QA to have caught everything.

## 16. Review Process

QA Analyst compiles findings; Engagement Lead reviews Issue Log severity ratings; Compliance/Standards Liaison independently completes final sign-off; client reviews Go-Live Recommendation for final approval.

## 17. Quality Assurance

This gate formally re-verifies all Eight Dimensions (Governance, Sec. 12.2) site-wide — it is the methodology's final comprehensive checkpoint, in any industry.

## 18. Exit Criteria

- [ ] All Required Documents complete
- [ ] Compliance Sign-Off Record completed and signed (where applicable)
- [ ] All P0 issues remediated and re-tested; no open P0 items
- [ ] Client has approved Go-Live Recommendation
- [ ] Handoff file and Action Items Sheet current as of go-live: no open decision the launch depends on, and each open item has an owner and a date

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "QA Status" section finalized with sign-off record
- Decision Register: log go-live approval as `DEC-SG11-001`; log any client-accepted open P2 risk explicitly as `DEC-SG11-002`
- Audit reports produced at this gate (accessibility, SEO, performance, design fidelity, compliance) are filed in `90-audits/` as `Audit-YYYY-MM-DD-<type>.md` and listed in that folder's `README.md`, not left inside this stage's `output/`

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
- Search Discovery Setup Record (an appendix to the Growth Program Plan; Sec. 10.1)
- Engagement Retrospective & Methodology Learnings Memo

## 5. Required Documents

`11.5-post-launch/output/Growth-Program-Plan.md`, `11.5-post-launch/output/KPI-Dashboard-Spec.md`, `11.5-post-launch/output/Experiment-Log.md`, `11.5-post-launch/output/Retrospective-Learnings.md`

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
[0] Search Discovery Setup at go-live (Sec. 10.1): search-engine
    properties verified, sitemaps submitted, instant indexing on,
    analytics linked, tracked keywords approved, local profile started
        │
        ▼
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

### 10.1 Search Discovery & Local Presence Setup

Run at go-live and finish within the first week. It makes the site discoverable and measurable; it is recorded as an appendix to the Growth Program Plan. Steps that need the client's own accounts, DNS or verification are **owner-only**: the team supplies the exact values and order, and the client performs the step. The team never creates accounts or accepts terms on the client's behalf, and never enters credentials.

1. **Search Console and Bing Webmaster Tools.** Verify the live site in both (URL-prefix property with the SEO plugin's verification field, or a DNS record for a domain property), record which account owns each, and submit the sitemap index in both. Treat a first-day "couldn't fetch" status as expected for a new property if the sitemap returns HTTP 200 to a search-engine user agent; re-check at 24 to 48 hours.
2. **Instant indexing.** Enable the SEO plugin's IndexNow (or equivalent) module for pages and posts, confirm the key file is reachable, and submit every live URL once. This reaches Bing, Yandex, Naver, Seznam and the other participating engines; Google does not use IndexNow, so Google discovery depends on item 1.
3. **Analytics link without double counting.** Connect the analytics property to the SEO plugin's dashboard for reading data, and keep the plugin's "install analytics code" option **off** when the site already loads a consent-gated tag. A second install duplicates events and can bypass the consent decision verified in Stage Gate 11.
4. **SEO plugin configuration.** Per-page titles and descriptions confirmed; one focus keyword per page taken from the Stage Gate 5 keyword map; a default 1200 by 630 social image; organisation schema completed (contact point, address or service area, `sameAs`); the plugin's local-business module filled in only with facts the client has confirmed; machine-readable summaries such as `llms.txt` checked so entries read as descriptions rather than page labels; robots and sitemap settings reviewed.
5. **Tracked keywords.** Approve a starting list of 8 to 15 phrases in the client's customers' words, from the Stage Gate 5 keyword map, and add them to the rank tracker. Label the list *unvalidated* when no search-volume data was available, and replace guesses with real queries from Search Console after about four weeks.
6. **Local presence.** Decide the public business name (it must match the real-world name; if a fictitious business name is required, file it first), whether the address is shown or hidden (service-area business), the owner account, categories, service areas, hours and description; create and verify the local business profile (the owner completes verification); then claim the map and directory listings that fit the vertical (for example Bing Places, Apple Business Connect, LinkedIn, Facebook, chamber or industry directories) with identical name, address and phone details. Add the profile URLs to `sameAs`.
7. **Contact details in one place.** Publish the business phone and email through a single source (a setting plus shortcode or equivalent) so one change propagates everywhere, and expose them as `tel:` and `mailto:` links. Turn off any email obfuscation that replaces contact links with script-decoded addresses, because crawlers then see no contact point.
8. **Technical hygiene.** Security response headers set at the edge; http, apex, `www` and trailing-slash variants reach the canonical URL in one redirect; unknown URLs return a real 404; the sitemap and pages fetch cleanly with a search-engine user agent.
9. **Record and hand off.** Fill the Search Discovery Setup Record: property owners and dates, what was submitted, what is pending verification, the tracked-keyword list and its status, and the next re-check dates. Every owner-only step and every decision (name, address, hours, owner account) is an item on the Action Items Sheet, and the handoff file points to those ids (AI Workflows Sec. 2.6).

## 11. Checklist

- [ ] Search Discovery Setup Record completed per Sec. 10.1: both search-engine properties verified with sitemaps submitted, instant indexing on and all live URLs submitted, analytics linked with plugin code install off where a consent-gated tag exists, tracked-keyword list approved and recorded, local profile created or its owner-only steps queued, and contact details single-sourced
- [ ] Handoff file and Action Items Sheet refreshed at the 1-, 4- and 12-week points, with open items and owners current
- [ ] KPI Dashboard verified accurate against Project Charter Success Metrics
- [ ] Baseline production data captured before first experiment begins
- [ ] Every experiment logged with a clear hypothesis and success criterion before it starts, not just a result after the fact
- [ ] Any new content follows Stage Gate 8/9 discipline (brief → compliance-cleared copy), not ad hoc publishing
- [ ] Compliance clearance for new or changed content is bound to the exact artifact/revision/language; later content does not inherit an earlier site or batch approval unless its scope explicitly says so
- [ ] Content Freshness Register reviewed on its assigned cadence; event-bound and volatile content has no overdue unhandled entries
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
- Reporting plugin content scores as SEO outcomes, or optimizing them in bulk without query-level evidence, a mapped page purpose, and a post-change review window.
- Comparing a short post-change period with an arbitrary prior period without accounting for seasonality, brand campaigns, migrations, launch annotations, or data latency.
- Expanding a rank tracker until it mirrors every keyword idea instead of maintaining a bounded decision portfolio with a mapped URL and owner for each term.

## 15. Best Practices

- Treat every post-launch content addition as a miniature Stage Gate 8→9 cycle — brief, compliance clearance, then publish — never skip steps because the site is already live.
- Feed every validated learning (both confirmations and surprises) back to the firm's cross-engagement Knowledge Base and, where genuinely generalizable to the vertical, into the active Industry Module via Change Request — this is the mechanism by which the Module library compounds in value over time (Governance, Sec. 9.5, 13.2).
- Run the visibility operating cadence at three resolutions: weekly anomaly/coverage checks; monthly query-page, conversion, internal-link, and content-opportunity review; quarterly portfolio, cannibalization, technical health, and strategy review. Use a consistent comparison window and annotate material site or campaign changes.
- Review near-win queries (commonly positions 4-20) and high-impression/low-click pages before inventing net-new content. Strengthen the best existing page when intent is already represented; create a new page only when the Stage Gate 5 Page-Creation Quality Gate passes.
- Separate leading indicators (indexation, impressions, rank movement, click-through rate, engagement) from meaningful outcomes (qualified leads, booked meetings, purchases, applications, or the Charter-defined equivalent). A change can improve one while harming the other.

## 16. Review Process

Strategy Consultant and Engagement Lead review the Growth Program Plan and Experiment Log at each Charter-defined reporting interval; Compliance/Standards Liaison reviews any new content or experiment copy exactly as in Stage Gate 9.

## 17. Quality Assurance

All Eight Dimensions remain in force for any new work produced during this gate; performance and SEO dimensions are additionally now measured against real data rather than projections.

## 18. Exit Criteria

This gate does not "close" in the same sense as prior gates — it establishes an ongoing program. Its formal completion checkpoint (typically at 90 days or the Charter-defined interval) requires:

- [ ] Search Discovery Setup Record complete; any property or profile still unverified has a named owner and a date on the Action Items Sheet
- [ ] KPI Dashboard operating and reviewed at agreed cadence
- [ ] Search Visibility Operations Plan operating with baseline, opportunity backlog, rank-tracking portfolio, link-audit log, measurement plan, and change annotations current
- [ ] At minimum 3 experiments logged with documented results
- [ ] Retrospective & Methodology Learnings Memo submitted

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents maintained as living documents, versioned per the Governance discipline's Version Control policy
- Blueprint: "Growth Program" section populated and continuously updated
- Decision Register: every shipped experiment logged as a standard Decision Register entry
- Audit reports (SEO, search discovery, content, performance re-audits) are filed in `90-audits/`; scope additions agreed during the program are filed in `91-addenda/`

The Retrospective Memo feeds the firm's Change Request process for both the Core Methodology and the active Industry Module, and the accumulated cross-engagement, cross-industry learnings inform future Research-discipline work more efficiently over time — this is the mechanism by which WEF becomes more valuable, in every vertical it serves, with every engagement run.

---

*End of QA & Optimization. Continue to Core Methodology — AI Workflows.*
