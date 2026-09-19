# Stage Ledger — {Client Name}

*Source of truth for stage status (Governance Sec. 5.3 rules 6–9; `RETRO-022`). Update at **every** stage transition and **every** session close. Present = the file exists at the stated path, verified by listing the folder — a similarly named or "equivalent" file does not count. An unopened stage folder is not evidence about a stage; this ledger is. Before starting stage N+1, complete the Stage Transition Check for stage N.*

## Project-specific gates mapped to the spine (Sec. 1.8)

| Project gate / milestone | Follows WEF stage(s) | Required Documents that must exist before it is presented | Approval logged as |
|---|---|---|---|
| {e.g., "Gate A — strategy decision"} | {SG1–SG5} | {every Required Document in those chapters} | {DEC-…} |

## Required Documents

*Paths are relative to the KB root. Copy `{ClientName}` per the KB naming convention. Status values: Not started · Draft vX.Y · Approved v1.0 · Waived (GOVERNANCE-EXCEPTION ID).*

| Stage | Required Document (path) | Present (Y/N) | Status / version | Notes |
|---|---|---|---|---|
| SG1 | `01-research/output/Discovery-Report.md` | N | Not started | |
| SG1 | `01-research/output/Client-Personas.md` | N | Not started | |
| SG1 | `01-research/output/Current-State-Digital-Audit.md` | N | Not started | |
| SG1 | `01-research/output/Digital-Estate-and-Access-Map.md` | N | Not started | |
| SG1 | `_config/Compliance-Constraints-Log.md` | N | Not started | |
| SG2 | `02-competitive/output/Competitive-Intelligence-Report.md` | N | Not started | |
| SG2 | `02-competitive/output/Competitor-Scoring-Matrix.md` | N | Not started | |
| SG2 | `02-competitive/output/White-Space-Map.md` | N | Not started | |
| SG3 | `03-strategy/output/Strategic-Direction-Brief.md` | N | Not started | |
| SG3 | `03-strategy/output/Positioning-Statement.md` | N | Not started | |
| SG3 | `03-strategy/output/Messaging-Pillars.md` | N | Not started | |
| SG4 | `04-architecture/output/Sitemap.md` | N | Not started | |
| SG4 | `04-architecture/output/URL-Structure-Standard.md` | N | Not started | |
| SG4 | `04-architecture/output/Navigation-Model.md` | N | Not started | |
| SG4 | `04-architecture/output/Content-Taxonomy.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Keyword-to-Page-Map.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Topical-Cluster-Model.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Technical-SEO-Requirements.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Schema-Markup-Plan.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Entity-AI-Search-Brief.md` | N | Not started | |
| SG5 | `05-seo-blueprint/output/Search-Visibility-Operations-Plan.md` | N | Not started | |
| SG5 | `{ClientName}_Master_Content_Workbook.xlsx` (skeleton) | N | Not started | |
| SG6 | `06-ux-conversion/output/Conversion-Flows.md` | N | Not started | |
| SG6 | `06-ux-conversion/output/Calculator-Specs.md` | N | Not started | |
| SG6 | `06-ux-conversion/output/UX-Pattern-Library.md` | N | Not started | |
| SG6 | `06-ux-conversion/output/Trust-Signal-Plan.md` | N | Not started | |
| SG6 | `06-ux-conversion/output/Conversion-Measurement-Contract.md` | N | Not started | |
| SG7 | `07-design-system/output/Design-System-Spec.md` | N | Not started | |
| SG7 | `07-design-system/output/Component-Library.md` | N | Not started | |
| SG7 | `07-design-system/output/Page-Templates.md` | N | Not started | |
| SG7 | `07-design-system/output/GeneratePress-GenerateBlocks-Notes.md` (or platform equivalent) | N | Not started | |
| SG7 | `07-design-system/output/Design-Constraints-Package.md` | N | Not started | |
| SG7 | Rendered Homepage + one hub template, per direction (≥2 directions) | N | Not started | Name the tool; store the file |
| SG7.5 | `07.5-prototype-validation/output/Design-Tournament-Scorecard.md` | N | Not started | |
| SG7.5 | `07.5-prototype-validation/output/Benchmark-Validation-Report.md` | N | Not started | |
| SG7.5 | `07.5-prototype-validation/output/Future-Proofing-Review.md` | N | Not started | |
| SG7.5 | `07.5-prototype-validation/output/Executive-Approval-Record.md` | N | Not started | |
| SG8 | `08-content-spec/output/Per-Page-Content-Specifications.md` | N | Not started | |
| SG8 | `08-content-spec/output/Content-Depth-Standard.md` | N | Not started | |
| SG8 | `08-content-spec/output/Compliance-Content-Checklist.md` | N | Not started | |
| SG8 | `{ClientName}_Master_Content_Workbook.xlsx` (enriched) | N | Not started | |
| SG9 | `09-copywriting/output/final-copy/{page-slug}.md` (one per page) | N | Not started | |
| SG9 | `09-copywriting/output/Voice-Tone-Guide.md` | N | Not started | |
| SG9 | `09-copywriting/output/Compliance-Clearance-Log.md` | N | Not started | |
| SG9 | `{ClientName}_Master_Content_Workbook.xlsx` (finalized) | N | Not started | |
| SG10 | `10-ai-build-package/output/Build-Package.md` | N | Not started | |
| SG10 | `10-ai-build-package/output/Build-Manifest.md` | N | Not started | |
| SG10 | `10-ai-build-package/output/Component-Pattern-Mapping.md` | N | Not started | |
| SG10 | `10-ai-build-package/output/Integration-Requirements.md` | N | Not started | |
| SG10.5 | `10.5-wp-implementation/output/Server-Config-Record.md` | N | Not started | |
| SG10.5 | `10.5-wp-implementation/output/Plugin-Config-Record.md` | N | Not started | |
| SG10.5 | `10.5-wp-implementation/output/Performance-Config-Record.md` | N | Not started | |
| SG10.5 | `10.5-wp-implementation/output/Content-Release-Record.md` | N | Not started | |
| SG11 | `11-qa/output/QA-Test-Report.md` | N | Not started | |
| SG11 | `11-qa/output/Compliance-Signoff-Record.md` | N | Not started | |
| SG11 | `11-qa/output/Issue-Log.md` | N | Not started | |
| SG11 | `11-qa/output/Go-Live-Recommendation.md` | N | Not started | |
| SG11.5 | `11.5-post-launch/output/Growth-Program-Plan.md` | N | Not started | |
| SG11.5 | `11.5-post-launch/output/KPI-Dashboard-Spec.md` | N | Not started | |
| SG11.5 | `11.5-post-launch/output/Experiment-Log.md` | N | Not started | |
| SG11.5 | `11.5-post-launch/output/Retrospective-Learnings.md` | N | Not started | |

## Exit Criteria

*Copy each stage's Exit Criteria (chapter Sec. 18) plus the Universal Exit Criteria (Research chapter intro) as rows when the stage opens.*

| Stage | Exit criterion | Met / Open / Waived | Evidence | Approver | Date |
|---|---|---|---|---|---|
| | | | | | |

## Stage Transition Checks

| Date | Transition (N → N+1) | Predecessor documents all present? | Missing (if any) | Action (stop / GOVERNANCE-EXCEPTION ID) | Checked by |
|---|---|---|---|---|---|
| | | | | | |
