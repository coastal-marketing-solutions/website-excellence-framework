# WEF Three-Engagement Reconciliation Crosswalk — 2026-08-13

## Scope

This crosswalk reconciles reusable framework lessons from:

1. Nationwide Financial Group Corporation (`nationwidefgc.com` / NFGC);
2. Synergy Real Estate Group (`sellyourhomefastsocal.com`); and
3. Itzel Gonzalez Real Estate (`itzelgonzalezrealestate.com`).

The current WEF repository is a shared, uncommitted working tree based on `main` at `668a492`. This document is a reconciliation record, not an adopted change. It does not authorize commit, push, or formal adoption of WEF 1.4 / CR-020.

## Controlling Conclusions

- The three engagements agree that SEO-plugin scores are diagnostics, not ranking, accessibility, compliance, conversion, or business KPIs. Numeric thresholds remain engagement-only.
- The three engagements agree that locality or keyword-variant pages require real service coverage, distinct intent, materially useful content, contextual discovery, substantiated facts, and maintenance ownership. List-driven mass publication is not Core policy.
- The three engagements agree on one production writer per generated capability, with read-only/reporting integrations allowed when documented.
- The three engagements agree that imports, browser edits, AI actions, and CMS success messages require fresh independent read-back and a bounded recovery path.
- The three engagements agree on evidence provenance/freshness, meaningful conversion receipt, consent/no-PII controls, and human-reviewed localization for consequential content.

## Consolidated Disposition

| Theme | NFGC | Synergy | Itzel | Current Working Tree | Disposition |
|---|---|---|---|---|---|
| Plugin-score discipline | Directly evidenced through Rank Math score campaigns | SY-02 | ITZ-05 | SEO 10.1 and QA/SG11.5 | Retain one Core rule; numeric targets engagement-only |
| Evidence-led SEO opportunities | Search Console/Site Kit/Rank Math operating model | SY-03, SY-17 | ITZ-16 partially extends | SEO 10.1; Templates 7.4-7.5 | Retain; add representative post-release indexing evidence |
| Local-page quality gate | County/city prioritization; no ZIP-page inventory | SY-04 | ITZ-04 | SEO 10.2; Template 7.7 | Retain as controlling rule |
| Contextual internal links | Service-area hubs to selected city/program pages | SY-05 | ITZ-18-19 | SEO 10.2 and Best Practices | Retain one rule; no link quotas |
| Link-audit classification | 305-link report was 403-heavy, not 404-heavy | SY-05/SY-18 supporting | ITZ-18 | SEO 10.3; Template 7.6 | Retain; crawler labels are leads, not verdicts |
| Capability ownership | Rank Math/theme/Site Kit/translation collision risk | SY-09/SY-13 | ITZ-06, ITZ-20 | Governance 13.4.4; Template 15.3 | Retain; add explicit precedence over “use licensed features fully” |
| Paid entitlement/site assignment | NFGC Rank Math PRO discovery | Referenced as current-tree addition | ITZ-07 / RETRO-009 | Governance 13.4.3; QA | Retain five-state verification |
| Digital estate/access boundaries | GoDaddy/Hostinger/GitHub/old-host split | SY-13 | ITZ-01, ITZ-21 | Research SG1; Governance 13.4.5-13.4.6 | Retain |
| Evidence provenance/freshness | Program/citation lifecycle | SY-01/SY-12 | ITZ-02-03 | Research standard; Templates 7.8-7.9 | Retain with materiality threshold |
| Deterministic publication and rollback | Content-as-files and CMS persistence | SY-06-08/SY-18 | ITZ-08/ITZ-10 | Development SG10.5; Templates 15.4; AI 5.4 | Retain coherent release lifecycle |
| Conversion operational handoff | Forms/analytics/CRM QA | SY-10 | ITZ-14 | UX SG6; Template 22.1 | Retain; require real destination receipt |
| Localization QA | Weglot/translation ownership and hreflang risk | SY-11 | ITZ-25 | Template 15.6 and QA | Retain tool-neutral rule |
| Post-release observation | Analytics/indexation/404 monitoring | SY-17 | ITZ-16 | QA first-day/third-day checks | Retain; add representative search-engine inspection |
| Geographic embed/map integrity | Location-page accuracy generally | SY-14 concrete cloned-map defect | Supports locality accuracy | Absent | Add concise QA rule and release-record field |
| Linked LocationCard contract | Service-area contextual cards | Supporting component use | ITZ-15 concrete accessibility gap | Component exists without `href` contract | Extend CL-SURF-002; do not create a duplicate component |
| WordPress maintenance window | Plugin ownership/update concerns | Supporting release discipline | ITZ-22 | General controls only | Add proportional platform implementation note |
| Video-to-website governance | Program/FAQ/content reuse applicable | Supporting multimedia reuse | ITZ-23 | Absent | Add optional reusable content template |
| Real-estate school facts | Not applicable to mortgage Core | Real-estate locality relevance | ITZ-24 | Module has general school-info language | Extend Real Estate family only; do not add to Core |

## Genuine Policy Decisions

### DECISION-A — Tier-3 Source of Truth Versus As-Built Mirror

**Current doctrine:** governed files are the source of truth even when GUI entry is the available implementation tier.

**Observed conflict:** the Itzel engagement sometimes captured files only after editing the live CMS. Those files were an as-built mirror, not an authoring source of truth.

**Recommended resolution:** define two clearly named modes:

1. **Authoring-source mode (compliant default):** reviewed files precede and govern CMS writes.
2. **Verified-mirror mode (temporary exception):** when no deterministic round trip exists, capture the as-built record immediately after a fresh read-back; label it a mirror, log the risk/exception, and migrate to authoring-source mode when a verified round trip becomes available.

Never call mode 2 the source of truth. This preserves operational honesty without making GUI-only engagements impossible.

**Decision:** Approved by the user on 2026-08-13 for working-draft integration. Formal adoption remains subject to Methodology Governance Board approval.

### DECISION-B — WordPress Draft Parent Selector

**Current doctrine:** the WordPress parent-page picker only searches Published pages.

**Observed conflict:** the behavior occurred in the Itzel build, but current WordPress documentation does not establish it as universal; editor, version, role, plugin, or import path may affect behavior.

**Recommended resolution:** replace the absolute claim with an environment-qualified implementation warning. Require a hierarchy preflight for Draft-only nested builds across the planned editor, Quick Edit, API/CLI, or importer path. If Draft parents are unavailable, record the temporary flat state and reconcile parent ID, slug/permalink, breadcrumb, canonical, menu, redirect, and internal links before publication.

**Decision:** Approved by the user on 2026-08-13 for working-draft integration. Formal adoption remains subject to Methodology Governance Board approval.

## Non-Policy Additions Ready for Working-Draft Integration

1. Add an explicit sentence that Capability Ownership takes precedence over maximizing licensed capabilities: use all relevant, non-conflicting value; do not activate every writer.
2. Add representative post-release search-engine verification covering sitemap membership, final status, canonical, robots, inspection result, template/hierarchy/locale/risk sampling, and follow-up. State that submission or inspection does not guarantee indexing or ranking.
3. Extend `CL-SURF-002 LocationCard` with a canonical `href`, semantic whole-card link contract, visible focus/hover states, minimum target size, no nested interactive controls, mobile/text-length testing, and destination verification.
4. Add concise locality data-integrity QA for maps, geographic embeds, coordinates, geographic queries, and local visuals after cloning or templating.
5. Add a proportional WordPress maintenance/change-window implementation note using backup, version/inventory, dependency/owner, small-group update, smoke test, cache handling, inactive-software removal review, and recovery evidence.
6. Add an optional Video-to-Website Deployment Brief covering mapped page/query, scripts, evidence/freshness, locale/human review, claims/clearance, CTA, transcript/captions, embed/supporting article, internal links, metadata/schema, exact revision approval, ownership, and retirement trigger.
7. Extend the Real Estate Module's school guidance: neutral attributed data, publisher/metric/scale/date, district context versus address-specific attendance assignment, direct district verification, and Fair Housing review.

## Attribution Summary

- **NFGC-originated or strongly evidenced:** Rank Math/Site Kit evidence loop; plugin-score limitations; 403-heavy link-audit false positives; 404 probe handling; selective city-page program; county/city hub linking; capability collisions; meaningful analytics events; Digital Estate split across registrar/host/repository/legacy provider.
- **Synergy-originated or strongly evidenced:** deterministic XML/import release sequence; page-by-page judgment boundary; cloned-map locality defect; synced structural patterns; support-guide/problem-hub scaling; Spanish funnel planning; source distinction in competitor research.
- **Itzel-originated or strongly evidenced:** paid-entitlement/site assignment; artifact/revision/language-bound approval; custom-domain origin/access-control boundary; freshness classes; all-post-type content manifests; linked LocationCard behavior; representative indexing verification; WordPress maintenance note; video deployment brief; factual school-assignment boundary; Tier-3 mirror terminology conflict; Draft-parent evidence qualification.
- **Integrator-originated:** multi-context reconciliation protocol and combined three-way crosswalk.

## Items Explicitly Kept Out of Core

- Numeric Rank Math score targets.
- Exact city, neighborhood, county, or ZIP inventories.
- Mortgage program, NMLS, loan, licensing, or disclosure facts outside the Mortgage Lending Module.
- California real-estate, brokerage, MLS/IDX, school, foreclosure, probate, or Fair Housing details outside the Real Estate-family Modules.
- Vendor quirks such as WP All Import Free field limitations or a particular Rank Math admin control unless independently repeated and maintained as a versioned implementation note.
- Client names, profiles, routing destinations, approval authorities, response-time promises, analytics property IDs, and vendor-account identities.

## Current Status

- Crosswalk complete.
- Decisions A and B approved by the user and integrated into the shared working draft.
- All seven non-policy additions are integrated: capability-ownership precedence, representative indexing verification, LocationCard interaction/accessibility, geographic data integrity, proportional WordPress maintenance, an optional video deployment brief, and the Real Estate school-information boundary.
- WEF 1.4 / CR-020 remains a working draft pending formal approval.
- No commit or push authorized or performed by the canonical integrator.
