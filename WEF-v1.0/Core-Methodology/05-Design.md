# CORE METHODOLOGY — DESIGN

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

Design covers the transformation of approved architecture and UX flows into an approved, buildable visual design system. It comprises Stage Gate 7 (Visual Design System) and Stage Gate 7.5 (Prototype Validation), the latter being a compound sub-gate containing four distinct validation activities: the Design Tournament, Benchmark Validation, Future-Proofing Review, and Executive Approval. Both follow the fixed 19-part template defined in the Research chapter's introduction.

Design work in WEF is never presented as a single option, in any industry. The methodology's central design discipline is **comparative evaluation under a fixed rubric** — candidates compete, competition is scored, and the client makes an informed choice among genuinely differentiated, fully-realized options rather than approving or rejecting a single proposal. The only thing that changes between a mortgage lender and a law firm at this stage is the specific visual conventions and trust-signal treatment the active Industry Module calls for — the tournament mechanic itself is universal.

---

# STAGE GATE 7 — VISUAL DESIGN SYSTEM

## 1. Purpose

Produce a complete, GeneratePress/GenerateBlocks-buildable visual design system: typography, color, spacing, component library, and page-template designs that express the approved positioning while satisfying performance, accessibility, and conversion requirements set in prior gates.

## 2. Business Objectives

- Translate positioning and messaging pillars (Stage Gate 3) into a visual identity that is distinct from the competitive set mapped in Stage Gate 2.
- Produce a component-based design system, not one-off page designs, so that GenerateBlocks patterns can be built once and reused across the full sitemap.
- Ensure every design decision is compatible with the Core Web Vitals targets set in the SEO & Architecture discipline.

## 3. Inputs

Sitemap & Navigation Model (SG4), UX Pattern Library & Conversion Flows (SG6), Positioning & Messaging Pillars (SG3), Trust Signal Placement Plan (SG6), Competitive Intelligence visual evidence (SG2), active Industry Module's Trust Signal Requirements (visual treatment) and visual conventions

## 4. Outputs

- Design System Specification (typography, color, spacing, grid)
- Component Library (buttons, cards, forms, calculators, navigation, footer)
- Key Page Template Designs (home, offering pillar, persona hub, practitioner/staff profile, guide/blog, contact/application)
- GeneratePress/GenerateBlocks Implementation Notes (or the Charter-confirmed alternative stack's equivalent — see the Design Constraints Package Appendix)
- **Design Constraints Package** — the structured, tool-agnostic constraint set that any AI design tool (Claude Design, OpenAI Design, Figma, Canva, Adobe Express/Firefly, or equivalent) must design *within*, and that any AI coding agent (Claude Code, Codex, Manus, GitHub Copilot, or equivalent) must be given as context before implementing or editing the site. See the Design Constraints Package Specification Appendix at the end of this chapter for full contents.

## 5. Required Documents

`/07-design-system/design-system-spec-v1.md`, `/07-design-system/component-library-v1.md`, `/07-design-system/page-templates-v1.md`, `/07-design-system/generatepress-generateblocks-notes-v1.md` (or platform-equivalent), `/07-design-system/design-constraints-package-v1.md`

## 6. Responsible Roles

Visual Designer (lead), UX Designer (flow fidelity check), Developer (buildability consult)

## 7. Required Specialists

Compliance/Standards Liaison (confirm trust signal and disclosure visual treatment meets the active Industry Module's requirements), SEO Specialist (confirm heading structure and template semantics support the SEO & Architecture discipline's output)

## 8. Decision Authority

Design candidates produced in this gate are **not individually approved** — they are carried forward as-is into Stage Gate 7.5, where client approval actually occurs. This gate's exit criteria concern completeness and internal quality, not client sign-off.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's **Trust Signal Requirements** (for visual prominence/placement conventions) and any documented industry visual conventions (e.g., a professional, restrained palette is often expected in law and medicine; a warmer, more approachable palette often performs better in home services) before finalizing the design system foundation.

## 10. Workflow

```
[1] Establish design principles from positioning (mobile-first,
    accessibility-first, performance-first)
        │
        ▼
[2] Develop typography and color system with accessibility contrast
    validation (WCAG 2.1 AA minimum), informed by the Module's visual
    conventions
        │
        ▼
[3] Build component library as reusable GenerateBlocks-pattern-ready
    modules
        │
        ▼
[4] Design key page templates using the component library
        │
        ▼
[5] Document GeneratePress/GenerateBlocks Implementation Notes (Sec. 15)
        │
        ▼
[6] Internal design review → prepare 2-3 distinct design directions for
    Stage Gate 7.5 Design Tournament
```

## 11. Checklist

- [ ] Active Industry Module's Trust Signal Requirements and visual conventions reviewed before drafting
- [ ] Typography system defined (type scale, font pairing, line-height, responsive scaling)
- [ ] Color system passes WCAG 2.1 AA contrast on all text/background combinations
- [ ] Component library covers every UX pattern defined in Stage Gate 6
- [ ] All key page templates designed using only components in the library (no bespoke one-off elements)
- [ ] GeneratePress/GenerateBlocks Implementation Notes specify exact patterns, global styles, and site library structure
- [ ] At least 2 genuinely distinct design directions prepared for the Stage Gate 7.5 tournament

## 12. Prompt(s)

**Prompt 7.1 — Design System Foundation**

```
You are the Visual Designer for [Client Name] in the [Industry Module
name] vertical. Using the approved positioning "[insert]" and messaging
pillars, the competitive visual evidence archive (avoid imitating any
single competitor), and the [Industry Module]'s visual conventions and
Trust Signal Requirements, propose a design system foundation: typography
(2-3 font families max, full type scale), color palette (primary,
secondary, semantic colors for success/warning/error, full accessible
neutral scale), spacing scale (base unit and multiples), and grid/
breakpoint system.

Constraints: must render cleanly in GeneratePress Premium's Site Library
and Global Styles system; must pass WCAG 2.1 AA contrast; must support a
mobile-first responsive build in GenerateBlocks.
```

**Prompt 7.2 — Component Library Specification**

```
Using the design system foundation above and the UX Pattern Library from
Stage Gate 6, specify the following components at implementation-ready
detail (states: default, hover, focus, active, disabled; responsive
behavior at mobile/tablet/desktop breakpoints):
1. Primary and secondary buttons
2. Lead capture form (single-step and multi-step variants)
3. Practitioner/staff bio card
4. Trust signal bar (per the [Industry Module]'s Trust Signal
   Requirements)
5. FAQ accordion
6. Comparison/data table
7. Calculator/tool input-output module
8. Navigation (header, mega-menu if applicable, footer, mobile menu)

For each, note the GenerateBlocks pattern type (Container, Grid, Button,
Query Loop, etc.) that should be used to build it.
```

## 13. Examples

*Generic type scale pattern:*

| Token | Size (rem) | Use |
|---|---|---|
| `--font-size-h1` | 2.75 | Page H1, hero headline |
| `--font-size-h2` | 2.0 | Section headers |
| `--font-size-body` | 1.0625 | Body copy (17px base for readability on higher-consideration content) |
| `--font-size-small` | 0.875 | Disclaimers, fine print |

See each Industry Module for vertical-specific visual convention notes (e.g., typical color psychology, imagery style, and level of visual formality observed to perform well in that vertical's competitive set).

## 14. Common Mistakes

- Designing beautiful one-off hero sections that cannot be reproduced as reusable GenerateBlocks patterns, creating Development-phase build debt.
- Choosing decorative fonts or low-contrast color combinations that fail accessibility standards on a site where legal risk from inaccessibility is elevated, as it is in most regulated verticals this framework serves.
- Presenting only one design direction, collapsing the Stage Gate 7.5 tournament into a rubber-stamp approval rather than a genuine comparative decision.
- Ignoring the active Industry Module's visual conventions and defaulting to house style regardless of what actually builds trust in that vertical.
- Building every page from hand-duplicated markup instead of a reusable component/pattern — a single structural defect (e.g., an incorrect heading hierarchy) then has to be fixed page-by-page site-wide instead of once, at the source (Governance, Sec. 15.4, RETRO-004 — this happened in a real engagement).
- Deferring the actual AI design-tool execution (not just the written spec) past launch under deadline pressure, then having to build a live site's design retrofit around copy and URLs that are already indexed and converting (Governance, Sec. 15.4, RETRO-001).
- Letting Development begin on the pages that happen to be designed already while treating the rest of the sitemap as "come back to it later" — this quietly converts SG7.5 from a hard gate into a soft one (Governance, Sec. 15.4, RETRO-002).

## 15. Best Practices

- Treat GeneratePress Global Styles (colors, typography, and spacing defined once at the theme level) as the source of truth, with GenerateBlocks patterns consuming those global tokens rather than hardcoding values — this is the single highest-leverage maintainability decision in the entire build.
- Design disclaimer/fine-print typography with the same care as headline typography; in most Industry Modules this text carries real legal or professional-standards weight and is read carefully by cautious visitors.
- Build the practitioner/staff bio card and trust signal bar components early — they appear on nearly every template and their quality disproportionately affects perceived trustworthiness.

## 16. Review Process

Internal design critique with UX Designer and Developer before templates are finalized; Compliance/Standards Liaison confirms trust-signal visual prominence meets the active Industry Module's disclosure visibility requirements.

## 17. Quality Assurance

Primary Eight-Dimension focus: **Accessibility**, **Brand**, **WordPress/GeneratePress/GenerateBlocks Compatibility**. All eight dimensions are formally re-scored in Stage Gate 7.5.

## 18. Exit Criteria

- [ ] Design System Specification and Component Library complete per Checklist
- [ ] At least 2 distinct design directions ready for tournament
- [ ] Developer has confirmed buildability of all components in GenerateBlocks

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v0.x (draft status — not yet approved; approval happens at SG7.5)
- Blueprint: not yet updated (Blueprint reflects only approved states; wait for SG7.5)
- Decision Register: log design direction rationale as `DEC-SG7-00x` (draft status)

Design directions produced here are the direct input to the Stage Gate 7.5 Design Tournament immediately following.

---

# STAGE GATE 7.5 — PROTOTYPE VALIDATION

## 1. Purpose

Subject the design direction(s) produced in Stage Gate 7 to rigorous, structured validation before any production build work begins: a head-to-head Design Tournament, a Benchmark Validation against performance/accessibility/SEO standards, a Future-Proofing Review against the site's 3-5 year growth trajectory, and formal Executive Approval. This is the single most important quality gate in the entire methodology — no engagement, in any industry, proceeds to Development without clearing it.

## 2. Business Objectives

- Ensure the client makes an informed, comparative decision rather than an instinctive reaction to a single design.
- Catch performance, accessibility, or scalability defects before they are baked into a full site build.
- Secure unambiguous, documented executive sign-off that unlocks Development discipline work.

## 3. Inputs

Design System Specification, Component Library, Page Template Designs (all from Stage Gate 7, minimum 2 distinct directions)

## 4. Outputs

- Design Tournament Scorecard
- Benchmark Validation Report
- Future-Proofing Review Memo
- Executive Approval Record (signed)

## 5. Required Documents

`/07.5-prototype-validation/design-tournament-scorecard-v1.md`, `/07.5-prototype-validation/benchmark-validation-report-v1.md`, `/07.5-prototype-validation/future-proofing-review-v1.md`, `/07.5-prototype-validation/executive-approval-record-v1.md`

## 6. Responsible Roles

Visual Designer (presents candidates), Engagement Lead (facilitates tournament and executive approval), Developer (benchmark validation), SEO Specialist (benchmark validation)

## 7. Required Specialists

Compliance/Standards Liaison (final disclosure/trust-signal visual sign-off), QA Analyst (early involvement — benchmark validation overlaps with QA & Optimization criteria applied early)

## 8. Decision Authority

**Client executive sign-off is mandatory and is the hard gate for this entire discipline.** The named Decision Authority must sign the Executive Approval Record. No Development-phase work begins without it.

## 9. Module Injection Point(s)

> **Module Injection Point:** The Design Tournament Scoring Matrix's "Differentiation from Competitors" row should be evaluated against the active Industry Module's Competitive Landscape Notes; the Future-Proofing Review should specifically test the design against the Module's typical multi-location/multi-offering growth pattern for this vertical (e.g., additional licensed states for a mortgage lender, additional practice areas for a law firm, additional service lines for a home services company).

## 10. Workflow — The Four Validation Activities

```
                    STAGE GATE 7.5 — PROTOTYPE VALIDATION
   ┌─────────────────────────────────────────────────────────────────┐
   │                                                                   │
   │  [A] DESIGN TOURNAMENT                                            │
   │      2-3 fully realized design directions scored head-to-head     │
   │      on a fixed rubric (Sec. 12) by both firm and client          │
   │      reviewers                                                    │
   │                          │                                        │
   │                          ▼                                        │
   │  [B] BENCHMARK VALIDATION                                          │
   │      Winning direction stress-tested against performance,          │
   │      accessibility, and SEO-technical benchmarks (Sec. 10.2)       │
   │                          │                                        │
   │                          ▼                                        │
   │  [C] FUTURE-PROOFING REVIEW                                        │
   │      Winning direction evaluated against 3-5 year scale scenario  │
   │      (Sec. 10.3), informed by the Module's typical growth pattern  │
   │                          │                                        │
   │                          ▼                                        │
   │  [D] EXECUTIVE APPROVAL                                            │
   │      Formal client sign-off session; Executive Approval Record    │
   │      signed by named Decision Authority                            │
   │                                                                   │
   └─────────────────────────────────────────────────────────────────┘
                          │
                          ▼
                Development discipline (Stage Gate 8) begins
```

### 10.1 Design Tournament Procedure

1. Present 2–3 fully realized design directions (not sketches — complete key-page-template renders) side by side.
2. Score each direction on the **Design Tournament Scoring Matrix** (Sec. 13) across all Eight Dimensions (Governance, Sec. 12.2) plus differentiation-from-competitors.
3. Both firm reviewers and client stakeholders score independently before discussing, to avoid anchoring bias.
4. Reconcile scores in a joint working session; the highest-scoring direction advances, though the client may request specific element cross-pollination — any such hybrid must be re-scored before proceeding.

### 10.2 Benchmark Validation Procedure

The winning design direction is validated against fixed, non-negotiable benchmarks before it proceeds:

| Benchmark | Standard | Method |
|---|---|---|
| Performance | Projected LCP < 2.5s, INP < 200ms, CLS < 0.1 on representative templates | Static prototype tested via PageSpeed Insights / WebPageTest against a built HTML approximation |
| Accessibility | WCAG 2.1 AA | Automated scan (axe or equivalent) + manual keyboard navigation check |
| SEO-Technical | Heading hierarchy, semantic HTML structure intact per template | Manual review by SEO Specialist against the SEO & Architecture discipline's requirements |
| Mobile Usability | No horizontal scroll, tap targets ≥ 44px, readable without zoom | Manual device/viewport testing |

### 10.3 Future-Proofing Review Procedure

Evaluate the winning direction against a defined future-scale scenario documented in the Future-Proofing Review Memo, using the active Industry Module's typical growth pattern:

- What happens to the navigation and template system if the client adds more locations/service areas and more offerings, per the Module's typical growth trajectory for this vertical?
- Does the component library support a 5x increase in blog/guide content without visual degradation?
- Are there any hardcoded (non-token-based) design decisions that would require a full redesign rather than a parameter change to scale?

### 10.4 Executive Approval Procedure

Formal session with the named Decision Authority. The Executive Approval Record captures: which direction was approved, any conditions attached to approval, the Benchmark Validation and Future-Proofing Review results as attached evidence, and the signature/date.

## 11. Checklist

- [ ] Minimum 2 fully realized design directions presented (not concepts/sketches)
- [ ] Design Tournament Scorecard completed by both firm and client reviewers independently before reconciliation
- [ ] Benchmark Validation Report shows all four benchmarks (Sec. 10.2) at passing status, or documents a specific remediation plan for any that fail
- [ ] Future-Proofing Review Memo completed, informed by the active Industry Module's growth pattern, and no unresolved scalability red flags remain
- [ ] Executive Approval Record signed by the named Decision Authority

## 12. Prompt(s)

**Prompt 7.5.1 — Design Tournament Scorecard Generation**

```
You are facilitating a Design Tournament for [Client Name]'s website
redesign in the [Industry Module name] vertical. Given the attached
descriptions/renders of Design Direction A and Design Direction B, score
each 1-5 on: Performance (perceived weight/complexity), Accessibility
(contrast, structure clarity), SEO (semantic clarity, heading logic),
Conversion (CTA clarity, friction), Brand (distinctiveness vs. competitive
set from Stage Gate 2), Scalability (component reuse evident),
Maintainability (design token discipline evident), WordPress/
GeneratePress/GenerateBlocks Compatibility, and Differentiation from
Competitors (using the [Industry Module]'s Competitive Landscape Notes).
Provide a one-sentence justification per score. Do not simply average
toward a tie — identify the genuine strengths and weaknesses of each
direction even if the final scores are close.
```

**Prompt 7.5.2 — Future-Proofing Stress Test**

```
Given the approved design direction's component library and template
designs, stress-test it against this scale scenario, informed by the
[Industry Module]'s typical growth pattern for this vertical: the client
expands from [current locations/offerings] to [projected locations/
offerings] over the next 3 years, and grows its content library from
[current page count] to 5x that count. Identify any component or template
that would require a full redesign (not just new content) to accommodate
this growth, and propose the specific design token or pattern change
needed now to prevent that future rework.
```

## 13. Examples

*Generic Design Tournament Scoring Matrix:*

| Dimension | Direction A | Direction B | Notes |
|---|---|---|---|
| Performance | 4 | 5 | B uses fewer custom web fonts and lighter hero imagery |
| Accessibility | 4 | 4 | Both pass AA; A has marginally tighter link-underline contrast |
| SEO | 4 | 4 | Equivalent heading structure |
| Conversion | 3 | 5 | B's CTA hierarchy is clearer; A has competing CTAs above the fold |
| Brand | 5 | 3 | A is more distinctive vs. competitive set; B reads closer to a known competitor's pattern |
| Scalability | 4 | 5 | B's card component handles variable content length better |
| Maintainability | 4 | 5 | B's token discipline is cleaner |
| GP/GB Compatibility | 5 | 5 | Both fully buildable |
| **Total (of 40)** | **33** | **36** | Client requested A's hero color treatment applied to B — re-score as hybrid before final approval |

## 14. Common Mistakes

- Skipping independent scoring and going straight to group discussion, which allows the loudest stakeholder's preference to dominate.
- Treating Benchmark Validation as a formality rather than gating criteria — a design that fails Core Web Vitals projections at this stage is dramatically cheaper to fix than after Development builds it.
- Allowing "executive approval" to happen informally in a hallway conversation instead of producing the signed Executive Approval Record — this creates disputes later about what was actually approved.
- Running the Future-Proofing Review against a generic growth scenario instead of the active Industry Module's actual typical pattern for that vertical.

## 15. Best Practices

- Build both/all tournament candidates to comparable fidelity — a polished Direction A against a rough Direction B is not a fair tournament and produces a biased result.
- When the client requests a hybrid of elements from multiple directions, always re-score the hybrid explicitly rather than assuming it inherits the higher of the two scores.
- Attach the Benchmark Validation Report and Future-Proofing Review Memo directly to the Executive Approval Record as evidence — this protects both the firm and the client if scope questions arise later.

## 16. Review Process

Engagement Lead facilitates the full sequence (Sec. 10.1–10.4); QA Analyst independently verifies the Benchmark Validation Report's technical claims before it is presented to the client.

## 17. Quality Assurance

All Eight Dimensions (Governance, Sec. 12.2) are formally scored in this gate — this is the methodology's designated comprehensive quality checkpoint before production begins, regardless of industry.

## 18. Exit Criteria

- [ ] Design Tournament completed with reconciled scores
- [ ] Benchmark Validation Report shows passing status or documented remediation plan
- [ ] Future-Proofing Review Memo completed with no unresolved red flags
- [ ] Executive Approval Record signed by named Decision Authority
- [ ] Approved design (System, Component Library, Page Templates) covers **100% of the Stage Gate 4-approved sitemap** — not a representative subset. Any page left undesigned at this point requires a `GOVERNANCE-EXCEPTION` Decision Register entry naming the page(s) and rationale before Development may begin on the rest of the site (Governance, Sec. 15.4, RETRO-002)
- [ ] The AI design-tool pass itself (Prompts 7.1/7.2, tournament candidates) has actually been executed against real deliverables — not deferred to "after launch" for schedule reasons (Governance, Sec. 15.4, RETRO-001)

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Design System" section populated with the approved direction, superseding any draft SG7 entries
- Decision Register: `DEC-SG7.5-001` (Executive Approval) logged as **Irreversible** — any post-approval design direction change is a major Change Request requiring re-running this gate

The approved design system is the binding input to Development (AI Build Package and WordPress Implementation Blueprint). It is not revisited until Post-Launch Growth Program proposes data-driven, incremental refinements — never a wholesale redesign without re-running this gate.

---

## Appendix — GeneratePress Implementation Guidance

- Use **GeneratePress Global Styles** (Customizer → Global Colors, Global Typography) to encode every token from the Design System Specification exactly once. Never apply one-off inline color or font overrides in individual GenerateBlocks patterns.
- Use the **Site Library** to save every approved component as a reusable pattern (Global block where the same instance must update everywhere — e.g., the trust signal bar — vs. Local block where instances vary per page).
- Use **Element hooks** (GeneratePress Premium's Elements module) for the trust signal bar, header, and footer so they are maintained in exactly one place and inherited across all templates defined at the Information Architecture gate.
- Confirm **Typography** settings use `clamp()`-based fluid type scaling where GeneratePress supports it, to satisfy the mobile-first requirement without a proliferation of breakpoint-specific overrides.

This appendix applies identically regardless of the active Industry Module — it is a platform-implementation detail of the default technology stack (Governance, Sec. 13.4), not a vertical-specific concern.

## Appendix — Design Constraints Package Specification

### Why This Deliverable Exists

Every prior appendix in this chapter assumes the default stack (WordPress/GeneratePress/GenerateBlocks). This deliverable is what makes Design's output usable *no matter which stack is confirmed* (Governance, Sec. 13.4.1) — including a future engagement built as a custom PHP/HTML site, or on any other stack a client or the framework's own operator later chooses. It is also the deliverable that solves a specific, real problem this framework was built to prevent: an AI design tool (Claude Design, OpenAI Design, Figma, Canva, Adobe Express/Firefly, or equivalent) produces a design candidate that looks right, but the AI coding agent that later implements or edits it (Claude Code, Codex, Manus, GitHub Copilot, or equivalent) has no shared source of truth for what it may and may not change — leading exactly to the kind of already-decided-copy overwrite and structural drift documented in Governance, Sec. 15.4 (RETRO-001, RETRO-004).

The Design Constraints Package is produced once, at Stage Gate 7 (before the design tournament, and revised only if the tournament's outcome changes a constraint), and is then the **required context package** for every downstream AI tool touching the site's design or code — at initial build (SG10/10.5) and at every post-launch AI-assisted edit for the life of the site.

### Required Contents

1. **Platform Target Declaration** — the exact, Charter-confirmed technology stack (Governance, Sec. 13.4.1), stated explicitly and unambiguously. Example: "WordPress + GeneratePress Premium + GenerateBlocks Pro" or "Custom PHP/HTML, no CMS, static asset pipeline via [tool]." Every downstream tool reads this first — nothing in the package should be interpreted against an assumed default.
2. **Structural/Buildability Constraints** — what the target platform can and cannot render, stated as hard rules, not suggestions:
   - Default stack: Gutenberg-native blocks only (Group, Heading, Paragraph, Buttons, Columns, Query Loop), built as GenerateBlocks patterns consuming GeneratePress Global Styles — no arbitrary raw HTML/JS the block editor can't represent.
   - Alternative stack (e.g., Custom PHP/HTML): the equivalent hard rules for that stack — component/template file structure, templating approach, CSS methodology (e.g., a defined utility-class or BEM convention), build/deploy pipeline constraints (e.g., must pass through the confirmed GitHub → hosting deploy path).
   - Container widths, breakpoints, and grid/spacing units, stated as fixed values.
3. **Design Tokens, Machine-Readable** — typography, color, and spacing tokens exported in a format an AI coding agent can consume directly (CSS custom properties and/or a JSON token file), not only as swatches in a design tool's proprietary format. This is what lets Claude Code, Codex, Manus, or any other build tool implement pixel-accurate output without re-deriving values from a screenshot.
4. **Accessibility & Compliance Visual Constraints** — the WCAG conformance level required (WCAG 2.1 AA minimum per this chapter's Sec. 10.2 default), plus any locked visual treatment the active Industry Module's Trust Signal Requirements mandate (disclosure prominence, required contrast ratios on compliance-critical elements).
5. **The Do-Not-Break List** — the single highest-leverage section of this deliverable. An explicit, named list of elements that must never be altered by any downstream AI tool without a logged Change Request: locked brand colors/gradients, the compliance footer and its exact required text, NAP (name/address/phone) data, schema markup fields, and any other element where an unreviewed AI edit would create legal, compliance, or brand risk. Every item is named specifically — "the CTA button gradient" is not specific enough; "Primary CTA fill: `linear-gradient(135deg, [token-a] → [token-b])`, Navy text, mandatory Navy border — do not alter without a Change Request" is.
6. **AI Tool Handoff Instructions** — an explicit, standing instruction, restated in every prompt or task given to an AI coding agent: *"This package is required context for any task that creates, edits, or reviews this site's design or markup. Do not paraphrase or regenerate copy that has already cleared compliance review (Sec. 06, SG9). Do not alter anything on the Do-Not-Break List without a logged Change Request. If the confirmed platform (Sec. 1 above) differs from what a prior session assumed, stop and confirm before proceeding."*

### Governance Rule

No AI design tool (Sec. 08, AI Workflows, Sec. 3.4) begins producing tournament candidates, and no AI coding agent begins implementation or post-launch editing work, without this package as loaded context. This applies at initial build (SG10/10.5) and to every subsequent AI-assisted change for the life of the site — it does not expire at launch.

### Maintenance

The Design Constraints Package is a living document. Any approved design change (a new component, a token change, an addition to the Do-Not-Break List) updates it via the same Change Request/Decision Register discipline as any other approved deliverable (Governance, Sec. 4, Sec. 13.2) — it is never allowed to silently drift from what the live site actually reflects, for the same reason Governance Sec. 13.4.1 requires the technology stack itself to stay in sync with the Charter.

## Appendix — GenerateBlocks Implementation Guidance

- Build every reusable UX pattern (Stage Gate 6) as a **GenerateBlocks pattern**, composed of Container, Grid, and Button blocks with CSS classes tied to Global Style tokens — not ad hoc inline styles per instance.
- Use the **Query Loop** block for any repeating content (practitioner/staff directory, guide/blog listings, testimonials) rather than manually duplicating card markup — this directly satisfies the Scalability dimension.
- Name every GenerateBlocks class systematically (e.g., `.gb-card--staff-profile`, `.gb-cta--primary`) and document the naming convention in the GeneratePress/GenerateBlocks Implementation Notes — this is what makes the Development discipline's AI Build Package unambiguous for a build model or developer to implement correctly.
- Test every pattern's responsive behavior at the exact breakpoints defined in the Design System Specification grid, not just "looks fine" at arbitrary window widths.

---

*End of Design. Continue to Core Methodology — Development.*
