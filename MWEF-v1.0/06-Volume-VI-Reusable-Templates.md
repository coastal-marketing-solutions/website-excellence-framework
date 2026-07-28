# VOLUME VI — REUSABLE TEMPLATE LIBRARY

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume VI is the fillable-template counterpart to Volumes II–V. Where those Volumes explain *why* and *when* each artifact is produced, this Volume provides the *actual blank template* a consultant or AI model fills in. Every template here is referenced by name from a specific Stage Gate; none are decorative. Copy the relevant template into the Knowledge Base path indicated in the originating Stage Gate's "Required Documents" section and complete it in place — do not rename fields or restructure tables, since downstream automation and cross-engagement comparison depend on structural consistency.

---

## 1. Prompt Library (Master Index)

All Stage Gate prompts from Volumes II–V are indexed here by number for quick lookup. This index is additive — the authoritative prompt text lives in its originating Stage Gate chapter.

| Prompt ID | Stage Gate | Purpose |
|---|---|---|
| 1.1 | SG1 | Borrower Persona Synthesis |
| 1.2 | SG1 | Current-State Digital Audit Synthesis |
| 2.1 | SG2 | Competitor Scoring |
| 2.2 | SG2 | White Space Synthesis |
| 3.1 | SG3 | Positioning Candidate Generation |
| 3.2 | SG3 | Messaging Pillar Development |
| 4.1 | SG4 | Sitemap Generation |
| 4.2 | SG4 | URL Structure Standard |
| 5.1 | SG5 | Keyword-to-Page Mapping |
| 5.2 | SG5 | Topical Cluster Model |
| 5.3 | SG5 | Schema Markup Plan |
| 6.1 | SG6 | Conversion Flow Design |
| 6.2 | SG6 | Calculator Specification |
| 7.1 | SG7 | Design System Foundation |
| 7.2 | SG7 | Component Library Specification |
| 7.5.1 | SG7.5 | Design Tournament Scorecard Generation |
| 7.5.2 | SG7.5 | Future-Proofing Stress Test |
| 8.1 | SG8 | Page Content Brief Generation |
| 8.2 | SG8 | Compliance Content Checklist |
| 9.1 | SG9 | Page Copywriting |
| 9.2 | SG9 | Meta Title/Description Generation |
| 10.1 | SG10 | Build Manifest Generation |
| 10.2 | SG10 | Component-to-Pattern Mapping |
| 10.5.1 | SG10.5 | Build Execution (Code-Generation Model) |
| 10.5.2 | SG10.5 | Performance Configuration Review |
| 11.1 | SG11 | QA Test Plan Generation |
| 11.2 | SG11 | Issue Log Triage |
| 11.5.1 | SG11.5 | Growth Program Prioritization |
| 11.5.2 | SG11.5 | Retrospective & Methodology Learnings |

**Prompt Discipline Standard:** Every prompt used in an engagement must (1) name the client and role explicitly, (2) attach the relevant Knowledge Base documents rather than relying on the model's memory of prior conversation turns, (3) include an explicit instruction against fabricating statistics, credentials, or claims, and (4) be logged (which prompt ID, which model, which date) if its output becomes a Knowledge Base deliverable.

---

## 2. Decision Register Template

```markdown
# Decision Register — [Client Name]

| Decision ID | Date | Decision Summary | Rationale | Alternatives Considered | Decided By | Stage Gate | Impacts | Reversibility | Status |
|---|---|---|---|---|---|---|---|---|---|
| DEC-SG1-001 | | | | | | | | Reversible/Costly/Irreversible | Active/Superseded |
```
*(Volume I, Section 4)*

## 3. Decision Templates — Change Request

```markdown
# Change Request — CR-[###]

**Submitted By:**
**Date:**
**Manual Section / Engagement Artifact Affected:**
**Current State:**
**Proposed Change:**
**Rationale:**
**Impact if Not Approved:**
**Impact on Schedule/Scope/Budget (engagement-level CRs only):**
**Governance Board / Engagement Lead Decision:** Approved / Rejected / Deferred
**Decision Rationale:**
**Date Decided:**
```
*(Volume I, Section 13.2)*

---

## 4. Review Templates

### 4.1 Stage Gate Exit Review Template

```markdown
# Stage Gate Exit Review — [Stage Gate Name/Number] — [Client Name]

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

### 5.3 Eight-Dimension Quality Scorecard (Firm-Level, Volume I Sec. 12.2 — reusable at any gate)

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
# Sitemap — [Client Name]

| Page | URL | Parent | Depth (clicks from home) | Persona Served | Product Served | Page Type |
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
| Location/State Page | | |
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
# Schema Markup Plan — [Client Name]

| Page Type | Schema Type(s) | Required Properties | Recommended Properties | Data Source/Owner |
|---|---|---|---|---|
| Homepage | Organization, FinancialService | name, url, logo, telephone, address, identifier (NMLS) | sameAs (social profiles) | Marketing |
| Loan Officer Profile | Person | name, jobTitle, telephone, identifier (NMLS ID) | image, sameAs | HR/Compliance |
| Location Page | LocalBusiness, Service | areaServed, provider | | SEO Specialist |
| Guide/FAQ | FAQPage, Article | mainEntity (Q&A pairs), author, datePublished | | Copywriter |
```

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
# Compliance Sign-Off Record — [Client Name]

| Page/Section | Reviewed By | Date | Status (Cleared/Cleared with Changes/Rejected) | Notes |
|---|---|---|---|---|
```

---

## 12. AI Prompt Templates — General-Purpose Frame

Use this frame to construct any Stage-Gate-specific prompt not already in the Prompt Library, ensuring LLM Handoff Protocol compliance (Volume I, Section 9):

```markdown
You are the [ROLE] for [Client Name], a mortgage lender licensed in
[states]. 

Context attached: [Charter Layer excerpt] / [relevant Decision Register
entries] / [current Master Website Blueprint excerpt].

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
| Trust Signal Bar | Hook (below header) | Site-wide | Contains NMLS ID, licensing links |
```

---

## 14. GenerateBlocks Templates

### 14.1 Component-to-Pattern Mapping Template

```markdown
| Component | Block Composition | CSS Classes (token-linked) | Responsive Notes | Dynamic Data Source |
|---|---|---|---|---|
| Loan Officer Card | Container > Grid > Image + Headline + Text + Button | .gb-card--loan-officer | Stack at <768px | Query Loop against Loan Officer CPT |
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

**Company/Lender Overview:**
- Lender type (retail/wholesale/credit union/correspondent):
- NMLS ID(s):
- Licensed states:
- Loan products offered:
- Niche specializations (VA, jumbo, non-QM, first-time buyer programs, etc.):

**Business Objectives:**
- Primary goal for this engagement:
- Quantified success metrics (if known):

**Current Digital Presence:**
- Current website URL (if any):
- Analytics access available (GA4/Search Console)?
- Known pain points with current site:

**Team & Stakeholders:**
- Marketing lead:
- Compliance contact:
- Loan officers available for interview:
- Decision Authority for approvals:

**Compliance Notes:**
- Known advertising restrictions:
- State-specific disclosure requirements known to client:

**Competitors (client-nominated):**
1.
2.
3.
```

### 16.2 Project Charter Template

*(See Volume I, Section 3.2 for required contents; use the following structure)*

```markdown
# Project Charter — [Client Name]

## Engagement Overview
## Business Objectives
## Scope Boundaries (In-Scope / Out-of-Scope)
## Technology Stack
## Compliance Framework
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
2. Project Charter walkthrough & confirmation
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
*(Volume I, Section 14.2 — see that section for standard MWEF risk categories to screen for at initialization)*

---

## 19. Issue Logs

*(See Section 11.2 above — the same Issue Log structure is used at Stage Gate 11 for pre-launch QA and reused for any post-launch defect tracking under Stage Gate 11.5.)*

---

## 20. Change Requests

*(See Section 3 above for the Change Request template, applicable both to firm methodology changes — Volume I Sec. 13.2 — and to engagement-level scope changes.)*

---

*End of Volume VI. Continue to Back Matter — Glossary, References, Index, Appendices.*
