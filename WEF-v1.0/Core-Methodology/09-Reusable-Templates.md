# CORE METHODOLOGY — REUSABLE TEMPLATES

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Reusable Templates is the fillable-template counterpart to the rest of the Core Methodology. Where those chapters explain *why* and *when* each artifact is produced, this chapter provides the *actual blank template* a consultant or AI model fills in. Every template here is referenced by name from a specific Stage Gate; none are decorative, and none are industry-specific — vertical-specific example content lives in the Industry Modules, not here. Copy the relevant template into the Knowledge Base path indicated in the originating Stage Gate's "Required Documents" section and complete it in place — do not rename fields or restructure tables, since downstream automation and cross-engagement comparison depend on structural consistency.

---

## 1. Prompt Library

See AI Workflows, Section 4, for the full Prompt Library master index. Prompt text is authoritative in its originating Stage Gate chapter.

---

## 2. Decision Register Template

```markdown
# Decision Register — [Client Name] — [Active Industry Module(s)]

| Decision ID | Date | Decision Summary | Rationale | Alternatives Considered | Decided By | Stage Gate | Impacts | Reversibility | Status |
|---|---|---|---|---|---|---|---|---|---|
| DEC-SG1-001 | | | | | | | | Reversible/Costly/Irreversible | Active/Superseded |
```
*(Governance, Section 4)*

## 3. Decision Templates — Change Request

```markdown
# Change Request — CR-[###]

**Submitted By:**
**Date:**
**Scope:** Core Methodology / Industry Module: [name] / Engagement-Level
**Section/Artifact Affected:**
**Current State:**
**Proposed Change:**
**Rationale:**
**Impact if Not Approved:**
**Impact on Schedule/Scope/Budget (engagement-level CRs only):**
**Governance Board / Engagement Lead Decision:** Approved / Rejected / Deferred
**Decision Rationale:**
**Date Decided:**
```
*(Governance, Section 13.2)*

---

## 4. Review Templates

### 4.1 Stage Gate Exit Review Template

```markdown
# Stage Gate Exit Review — [Stage Gate Name/Number] — [Client Name]

**Active Industry Module(s):**
**Reviewer(s):**
**Date:**

## Checklist Status
[Paste the Stage Gate's Checklist from the manual; mark each item Pass/Fail/N/A]

## Exit Criteria Status
[Paste Exit Criteria; mark each Met/Not Met]

## Outstanding Items
| Item | Owner | Due Date |
|---|---|---|

## Decision
[ ] Gate approved — proceed to next Stage Gate
[ ] Gate approved with conditions (list below)
[ ] Gate not approved — remediation required before re-review

**Conditions/Remediation Notes:**
**Approved By:**
```

### 4.2 Design Critique Template (internal, pre-tournament)

```markdown
# Internal Design Critique — [Direction Name] — [Client Name]

**Reviewers:**
**Date:**

| Dimension | Score (1-5) | Notes |
|---|---|---|
| Performance | | |
| Accessibility | | |
| SEO | | |
| Conversion | | |
| Brand/Differentiation | | |
| Scalability | | |
| Maintainability | | |
| GP/GB Compatibility | | |

**Overall Recommendation:** Ready for tournament / Needs revision (specify)
```

---

## 5. Scoring Rubrics

### 5.1 Competitor Scoring Matrix (Stage Gate 2)

```markdown
| Competitor | Content Depth (1-5) | Technical SEO (1-5) | UX/Conversion (1-5) | Design (1-5) | Trust Signals (1-5) | Local Relevance (1-5) | Total (/30) | Notes |
|---|---|---|---|---|---|---|---|---|
```

### 5.2 Design Tournament Scoring Matrix (Stage Gate 7.5)

```markdown
| Dimension | Direction A | Direction B | Direction C | Notes |
|---|---|---|---|---|
| Performance | | | | |
| Accessibility | | | | |
| SEO | | | | |
| Conversion | | | | |
| Brand | | | | |
| Scalability | | | | |
| Maintainability | | | | |
| GP/GB Compatibility | | | | |
| Differentiation from Competitors | | | | |
| **Total (of 45)** | | | | |
```

### 5.3 Eight-Dimension Quality Scorecard (Governance Sec. 12.2 — reusable at any gate)

```markdown
| Dimension | Score (1-5) | Evidence/Justification |
|---|---|---|
| Performance | | |
| Accessibility | | |
| SEO | | |
| Conversion | | |
| Brand | | |
| Scalability | | |
| Maintainability | | |
| WordPress/GP/GB Compatibility & AI Readiness | | |
```

---

## 6. Architecture Templates

### 6.1 Sitemap Template

```markdown
# Sitemap — [Client Name] — [Active Industry Module]

| Page | URL | Parent | Depth (clicks from home) | Persona Served | Offering Served | Page Type |
|---|---|---|---|---|---|---|
| Home | / | — | 0 | All | All | Core |
```

### 6.2 URL Structure Standard Template

```markdown
# URL Structure Standard — [Client Name]

| Page Type | Pattern | Example | Notes |
|---|---|---|---|
```

### 6.3 Content Taxonomy Template

```markdown
# Content Taxonomy — [Client Name]

**Categories:**
**Tags:**

| Entity | Related Entities | Related Pages |
|---|---|---|
```

---

## 7. SEO Templates

### 7.1 Keyword-to-Page Map Template

```markdown
| Page URL | Primary Keyword | Secondary Keywords | Search Intent | Competitiveness | Content Angle |
|---|---|---|---|---|---|
```

### 7.2 Topical Cluster Model Template

```markdown
# Topical Cluster Model — [Client Name]

## Cluster: [Cluster Name]
**Pillar Page:** [URL]
**Cluster Pages:**
- [URL] — links to pillar via: [anchor text/context]

**Internal Linking Diagram:**
[ASCII or list-based representation]
```

### 7.3 Technical SEO Requirements Template

```markdown
# Technical SEO Requirements — [Client Name]

| Requirement | Target/Standard | Verification Method |
|---|---|---|
| LCP | < 2.5s | PageSpeed Insights / WebPageTest |
| INP | < 200ms | PageSpeed Insights / CrUX |
| CLS | < 0.1 | PageSpeed Insights |
| Indexation | All priority pages indexable; no unintended noindex | Search Console coverage report |
| Canonicalization | Self-referencing canonical on all pages | Manual/crawler audit |
```

---

## 8. Content Templates

### 8.1 Content Brief Template (Stage Gate 8)

```markdown
# Content Brief — [Page Name/URL]

**Primary Keyword:**
**Secondary Keywords:**
**Search Intent:**
**Persona Served:**

**Heading Outline:**
- H1:
- H2:
  - H3:

**Required Sections (purpose):**
1.

**Internal Linking Targets:**

**Calculator/Tool Embed:**

**Compliance Requirements:**

**Target Word Count:**
```

### 8.2 Content Depth Standard Template

```markdown
| Page Type | Minimum Word Count | Required Structural Elements |
|---|---|---|
| Pillar Page | | |
| Cluster Page | | |
| Location/Service-Area Page | | |
| Compliance Page | | |
```

---

## 9. Metadata Templates

```markdown
# Meta Tag Register — [Client Name]

| Page URL | Meta Title (≤60 char) | Meta Description (≤155 char) | Canonical URL | Robots Directive |
|---|---|---|---|---|
```

---

## 10. Schema Templates

```markdown
# Schema Markup Plan — [Client Name] — [Active Industry Module]

| Page Type | Schema Type(s) | Required Properties | Recommended Properties | Data Source/Owner |
|---|---|---|---|---|
| Homepage | Organization + [Module-specific type] | name, url, logo, telephone, address, identifier | sameAs (social profiles) | Marketing |
| Practitioner/Staff Profile | Person | name, jobTitle, telephone, identifier (per Module) | image, sameAs | HR/Compliance |
| Location Page | LocalBusiness, Service | areaServed, provider | | SEO Specialist |
| Guide/FAQ | FAQPage, Article | mainEntity (Q&A pairs), author, datePublished | | Copywriter |
```

See each Industry Module's SEO & Keyword Strategy section for the specific recommended schema types for that vertical.

---

## 11. QA Templates

### 11.1 QA Test Plan Template

```markdown
# QA Test Plan — [Client Name]

| Test ID | Feature/Page | Action | Expected Result | Pass/Fail | Notes |
|---|---|---|---|---|---|
```

### 11.2 Issue Log Template

```markdown
# Issue Log — [Client Name]

| Issue ID | Description | Page/Location | Category | Severity (P0/P1/P2) | Owner | Remediation | Status |
|---|---|---|---|---|---|---|---|
```

### 11.3 Compliance Sign-Off Record Template

```markdown
# Compliance Sign-Off Record — [Client Name] — [Active Industry Module]

| Page/Section | Reviewed By | Date | Status (Cleared/Cleared with Changes/Rejected) | Notes |
|---|---|---|---|---|
```

---

## 12. AI Prompt Templates — General-Purpose Frame

Use this frame to construct any Stage-Gate-specific prompt not already in the Prompt Library, ensuring LLM Handoff Protocol compliance (AI Workflows, Section 2):

```markdown
You are the [ROLE] for [Client Name] in the [Industry Module name]
vertical.

Context attached: [Charter Layer excerpt] / [relevant Decision Register
entries] / [current Master Website Blueprint excerpt] / [relevant active
Industry Module section(s)].

Task: [specific deliverable requested, referencing the exact Stage Gate
and Required Document it maps to]

Constraints:
- Do not fabricate statistics, credentials, testimonials, or regulatory
  claims
- Flag any compliance-sensitive statement explicitly rather than
  asserting it as final
- Ground every recommendation in the attached source material; label
  inferences explicitly
- Output format: [specify table/markdown structure expected]
```

---

## 13. GeneratePress Templates

### 13.1 Global Styles Token Record

```markdown
# GeneratePress Global Styles Token Record — [Client Name]

| Token | Value | GeneratePress Location |
|---|---|---|
| Primary Color | | Customizer > Colors > Global Palette |
| Secondary Color | | Customizer > Colors > Global Palette |
| Heading Font | | Customizer > Typography > Headings |
| Body Font | | Customizer > Typography > Body |
| Base Spacing Unit | | Customizer > Layout > Spacing |
```

### 13.2 Element Hooks Record

```markdown
| Element Name | Type (Header/Footer/Hook/Block) | Display Rules | Notes |
|---|---|---|---|
| Trust Signal Bar | Hook (below header) | Site-wide | Per active Industry Module's Trust Signal Requirements |
```

---

## 14. GenerateBlocks Templates

### 14.1 Component-to-Pattern Mapping Template

```markdown
| Component | Block Composition | CSS Classes (token-linked) | Responsive Notes | Dynamic Data Source |
|---|---|---|---|---|
| Staff/Practitioner Card | Container > Grid > Image + Headline + Text + Button | .gb-card--staff-profile | Stack at <768px | Query Loop against Staff CPT |
```

### 14.2 Pattern Library Index Template

```markdown
| Pattern Name | Global/Local | Used On Pages | Last Updated |
|---|---|---|---|
```

---

## 15. WordPress Templates

### 15.1 Server/Hosting Configuration Record

```markdown
# Server Configuration Record — [Client Name]

| Setting | Value | Notes |
|---|---|---|
| Hosting Provider | Hostinger VPS | Plan/tier: |
| PHP Version | | |
| WordPress Version | | |
| SSL/TLS | | Via Cloudflare / Origin cert |
| Backup Schedule | | |
```

### 15.2 Plugin & Integration Configuration Record

```markdown
| Plugin/Integration | Version | Purpose | Configuration Notes |
|---|---|---|---|
| GeneratePress Premium | | Theme framework | |
| GenerateBlocks Pro | | Page building | |
| Rank Math SEO | | SEO/schema | |
| LiteSpeed Cache | | Performance | |
```

---

## 16. Client Intake Templates

### 16.1 Client Intake Questionnaire

```markdown
# Client Intake Questionnaire — [Client Name]

**Company/Industry Overview:**
- Industry classification (select or propose Industry Module):
- Business model:
- Service area / jurisdiction(s):
- Offerings:
- Niche specializations:
- Credentials/licenses/registrations held:

**Business Objectives:**
- Primary goal for this engagement:
- Quantified success metrics (if known):

**Current Digital Presence:**
- Current website URL (if any):
- Analytics access available (GA4/Search Console)?
- Known pain points with current site:

**Team & Stakeholders:**
- Marketing lead:
- Compliance/standards contact (if applicable):
- Practitioners/staff available for interview:
- Decision Authority for approvals:

**Compliance/Standards Notes:**
- Known advertising or professional-conduct restrictions:
- Jurisdiction-specific disclosure requirements known to client:

**Competitors (client-nominated):**
1.
2.
3.
```

### 16.2 Project Charter Template

*(See Governance, Section 3.2 for required contents; use the following structure)*

```markdown
# Project Charter — [Client Name]

## Engagement Overview
## Active Industry Module(s)
## Business Objectives
## Scope Boundaries (In-Scope / Out-of-Scope)
## Technology Stack
## Regulatory/Compliance Framework
## Roles & Staffing
## Timeline (by Stage Gate)
## Decision Authority (named individuals per gate)
## Success Metrics
## Assumptions & Dependencies
## Change Control Process Reference

**Approved By (Client):**
**Approved By (Engagement Lead):**
**Date:**
```

---

## 17. Meeting Templates

### 17.1 Kickoff Meeting Agenda

```markdown
# Kickoff Meeting — [Client Name]

1. Introductions & roles (both firm and client sides)
2. Project Charter walkthrough & confirmation, including active Industry
   Module selection
3. Stage Gate 1 discovery interview scheduling
4. Knowledge Base access walkthrough
5. Communication cadence & escalation path
6. Q&A
```

### 17.2 Stage Gate Review Meeting Agenda

```markdown
# Stage Gate [#] Review — [Client Name]

1. Recap of gate objectives and inputs
2. Walkthrough of deliverables
3. Checklist/Exit Criteria review
4. Decisions requiring sign-off
5. Next Stage Gate preview and schedule
```

---

## 18. Risk Registers

```markdown
# Risk Register — [Client Name]

| Risk ID | Description | Category | Likelihood | Impact | Mitigation Plan | Owner | Status |
|---|---|---|---|---|---|---|---|
```
*(Governance, Section 14.2 — see that section for standard WEF risk categories to screen for at initialization)*

---

## 19. Issue Logs

*(See Section 11.2 above — the same Issue Log structure is used at Stage Gate 11 for pre-launch QA and reused for any post-launch defect tracking under Post-Launch Growth Program.)*

---

## 20. Change Requests

*(See Section 3 above for the Change Request template, applicable to Core Methodology changes, Industry Module changes, and engagement-level scope changes alike — the `Scope` field is what distinguishes them.)*

---

## 21. Context Navigation Templates

Templates for the CLAUDE.md/CONTEXT.md navigation layer defined in Governance Sec. 5.2.1. Adopted from the ICM context-management methodology (external reference material; see Governance Sec. 13.2 Change Proposal history for provenance).

### 21.1 Knowledge Base Root — CLAUDE.md Template

Keep this under ~800 tokens (roughly one screen). If it grows longer, move content into `CONTEXT.md` or a stage's own `CONTEXT.md` instead — this file is a map, not a manual.

```markdown
# [Client Name] Website Blueprint

## What This Is
[One to two sentences: who the client is, what this engagement is, which Industry Module(s) govern it.]

## Current State
**Active stage: [NN-stage-name] ([WEF Stage Gate name]).** [One sentence on where things stand.] See `CONTEXT.md` for the full stage map.

## Structure
```
[Client Name] Website Blueprint/
  CLAUDE.md              # You are here.
  CONTEXT.md              # Full WEF Stage Gate map.
  [NN-stage-name]/         # Created only once this stage begins — see CONTEXT.md
    CONTEXT.md
    output/
  _config/                # Charter, Decision Register, and other cross-stage governance docs
  _references/            # Pointers to the WEF framework and active Industry Module(s)
```

## How to Use
1. Read this file first, then `CONTEXT.md` for the full stage map.
2. Go to the active stage's `CONTEXT.md` before touching its `output/`.
3. Read `_config/project-charter.md` and `_config/decision-register.md` before starting any new stage's work.
4. Only create the next stage folder when that stage actually begins.
5. Every new decision goes in `_config/decision-register.md`.

## Layer Annotations (ICM)
- `CLAUDE.md`: L0 (always loaded, orientation)
- `CONTEXT.md`: L1 (stage-gate routing)
- Stage `CONTEXT.md` files: L2 (stage contracts)
- `_config/` files: L3 (engagement-specific reference)
- `_references/` files: L3 (domain reference — the WEF framework itself)
- Stage `output/` and client-supplied source material: L4 (working artifacts)
```

### 21.2 Knowledge Base Root — CONTEXT.md Template

```markdown
# Workflow: [Client Name] Website Blueprint

## Overview
[One to two sentences on which WEF Stage Gates apply and which Industry Module(s) govern them — reference Governance Sec. 1.4/1.5 for module selection/blend, if applicable.]

## Stage Map

| Folder | WEF Stage Gate | Purpose | Status |
|---|---|---|---|
| 01-research | SG1 — Discovery & Market Research | Personas, regulatory footprint, current-state audit | [Not started / Active / Complete] |
| 02-competitive | SG2 — Competitive Intelligence | Competitor scoring, White Space map | ... |
| 03-strategy | SG3 — Strategic Direction | Positioning, messaging pillars (client sign-off) | ... |
| 04-architecture | SG4 — Information Architecture | Sitemap, URL structure, taxonomy | ... |
| 05-seo-blueprint | SG5 — SEO Blueprint | Keyword map, topical clusters, schema plan | ... |
| 06-ux-conversion | SG6 — UX & Conversion | User flows, conversion paths, wireframes | ... |
| 07-design-system | SG7 — Design System | Visual identity, component library | ... |
| 07.5-prototype-validation | SG7.5 — Prototype Validation | Design tournament, executive approval | ... |
| 08-content-spec | SG8 — Content Spec | Page-by-page content briefs | ... |
| 09-copywriting | SG9 — Copywriting | Approved on-page copy | ... |
| 10-ai-build-package | SG10 — AI Build Package | Build-ready implementation spec | ... |
| 10.5-wp-implementation | SG10.5 — WP Implementation | Build record | ... |
| 11-qa | SG11 — QA & Optimization | Sign-off | ... |
| 11.5-post-launch | SG11.5 — Post-Launch Growth | KPIs, experiment log | ... |

## How Stages Connect
[Note any engagement-specific sequencing detail beyond the standard WEF spine — most engagements need none.]

## Reference Material
- `_config/project-charter.md`, `decision-register.md`, and siblings — see Sec. 5.2.1.
- `_references/`: pointers to the WEF framework and active Industry Module(s).

## When to Add Stages
[Name any Service Add-On Modules in scope, per Governance Sec. 1.7 — these get their own folder outside the numbered spine, since they don't gate SG1–SG11.5.]
```

### 21.3 Stage Folder — CONTEXT.md Template (Stage Contract)

One per active Stage Gate folder. A trimmed, engagement-specific instance of that gate's 19-part Core Methodology template — link to the full chapter rather than restating it.

```markdown
# Stage Contract: [NN-stage-name] (WEF Stage Gate [N] — [Stage Gate Name])

**Status:** [Not started / Active / Complete]

## Purpose
[One to two sentences, from the Stage Gate chapter's Sec. 1.]

## Inputs
[This stage's actual inputs — prior stage output, specific Module sections, specific client-supplied material — not a restatement of the chapter's generic input list.]

## Outputs (this stage's `output/`)
[List the actual files this stage will/did produce.]

## Exit Criteria
[Copy the relevant checklist items from the Stage Gate chapter's Exit Criteria section, checked off as completed.]

## What the Next Stage Should Read From Here
[Point the next stage at the specific sections/findings that matter most — don't make it re-read everything.]
```

### 21.4 Naming Convention Standard

Applies alongside the Documentation Standard (Governance Sec. 8.3). Choose one consistent pattern per engagement and state it in the root `CLAUDE.md`; the specific format matters less than consistency, since it's what lets an AI model find and name files correctly without a database.

**WEF default pattern:** `descriptive-name-v{N}.md` (already used throughout this framework's own Required Documents naming, e.g. `discovery-report-v1.md`).

**Alternative status-suffix pattern**, useful for content mid-review: `descriptive-name_draft.md` → `descriptive-name_final.md`. Do not mix both patterns within one engagement's KB.

### 21.5 Practice-Level (Multi-Client) Root

Section 5.2 defines one client's KB. A consulting practice running several WEF engagements at once benefits from the same L0/L1 layering **one level up**, at the practice root — this is a firm-operations convenience, not a per-engagement requirement.

```markdown
# [Firm/Practice Name]

[One sentence: what the practice does.]

## Active Engagements
- /clients/[client-1]/wef — [Industry Module]. Phase: [current Stage Gate].
- /clients/[client-2]/wef — [Industry Module]. Phase: [current Stage Gate].

## Framework
- /wef — the WEF Core Methodology + Industry Module library itself (read-only reference, not engagement-specific).

## Routing
| Task | Go to | Read |
|---|---|---|
| Work for [Client 1] | /clients/[client-1]/wef | CLAUDE.md, CONTEXT.md |
| Work for [Client 2] | /clients/[client-2]/wef | CLAUDE.md, CONTEXT.md |
| Add/revise an Industry Module | /wef/WEF-v1.0/Industry-Modules | 00-Module-Template-and-Index.md |

## Critical Rules
- Never reference one client's Decision Register, Charter, or compliance findings in another client's workspace.
- A new engagement copies the KB structure (Governance Sec. 5.2) and gets its own `_config/`, not a shared one.
```

---

*End of Core Methodology. Continue to Industry Modules.*
