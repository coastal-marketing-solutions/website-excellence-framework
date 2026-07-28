# VOLUME IV — DESIGN

*Mortgage Website Excellence Framework (MWEF) v1.0*

---

## Volume Introduction

Volume IV governs the transformation of approved architecture and UX flows (Volume III) into an approved, buildable visual design system. It comprises Stage Gate 7 (Visual Design System) and Stage Gate 7.5 (Prototype Validation), the latter being a compound sub-gate containing four distinct validation activities: the Design Tournament, Benchmark Validation, Future-Proofing Review, and Executive Approval. All Stage Gates follow the fixed 19-part template defined in Volume II's introduction.

Design work in MWEF is never presented as a single option. The methodology's central design discipline is **comparative evaluation under a fixed rubric** — candidates compete, competition is scored, and the client makes an informed choice among genuinely differentiated, fully-realized options rather than approving or rejecting a single proposal.

---

# STAGE GATE 7 — VISUAL DESIGN SYSTEM

## 1. Purpose

Produce a complete, GeneratePress/GenerateBlocks-buildable visual design system: typography, color, spacing, component library, and page-template designs that express the approved positioning while satisfying performance, accessibility, and conversion requirements set in prior gates.

## 2. Business Objectives

- Translate positioning and messaging pillars (Stage Gate 3) into a visual identity that is distinct from the competitive set mapped in Stage Gate 2.
- Produce a component-based design system, not one-off page designs, so that GenerateBlocks patterns can be built once and reused across the full sitemap.
- Ensure every design decision is compatible with the Core Web Vitals targets set in Stage Gate 5.

## 3. Inputs

Sitemap & Navigation Model (SG4), UX Pattern Library & Conversion Flows (SG6), Positioning & Messaging Pillars (SG3), Trust Signal Placement Plan (SG6), Competitive Intelligence visual evidence (SG2)

## 4. Outputs

- Design System Specification (typography, color, spacing, grid)
- Component Library (buttons, cards, forms, calculators, navigation, footer)
- Key Page Template Designs (home, product pillar, persona hub, loan officer profile, guide/blog, contact/application)
- GeneratePress/GenerateBlocks Implementation Notes

## 5. Required Documents

`/07-design-system/design-system-spec-v1.md`, `/07-design-system/component-library-v1.md`, `/07-design-system/page-templates-v1.md`, `/07-design-system/generatepress-generateblocks-notes-v1.md`

## 6. Responsible Roles

Visual Designer (lead), UX Designer (flow fidelity check), Developer (buildability consult)

## 7. Required Specialists

Compliance Liaison (confirm trust signal and disclosure visual treatment meets requirements), SEO Specialist (confirm heading structure and template semantics support Stage Gate 5 architecture)

## 8. Decision Authority

Design candidates produced in this gate are **not individually approved** — they are carried forward as-is into Stage Gate 7.5, where client approval actually occurs. This gate's exit criteria concern completeness and internal quality, not client sign-off.

## 9. Workflow

```
[1] Establish design principles from positioning (mobile-first,
    accessibility-first, performance-first — Volume I philosophy)
        │
        ▼
[2] Develop typography and color system with accessibility contrast
    validation (WCAG 2.1 AA minimum)
        │
        ▼
[3] Build component library as reusable GenerateBlocks-pattern-ready
    modules
        │
        ▼
[4] Design key page templates using the component library
        │
        ▼
[5] Document GeneratePress/GenerateBlocks Implementation Notes (Sec. 14)
        │
        ▼
[6] Internal design review → prepare 2-3 distinct design directions for
    Stage Gate 7.5 Design Tournament
```

## 10. Checklist

- [ ] Typography system defined (type scale, font pairing, line-height, responsive scaling)
- [ ] Color system passes WCAG 2.1 AA contrast on all text/background combinations
- [ ] Component library covers every UX pattern defined in Stage Gate 6
- [ ] All key page templates designed using only components in the library (no bespoke one-off elements)
- [ ] GeneratePress/GenerateBlocks Implementation Notes specify exact patterns, global styles, and site library structure
- [ ] At least 2 genuinely distinct design directions prepared for the Stage Gate 7.5 tournament

## 11. Prompt(s)

**Prompt 7.1 — Design System Foundation**

```
You are the Visual Designer for [Client Name], a mortgage lender. Using the
approved positioning "[insert]" and messaging pillars, and referencing the
competitive visual evidence archive (avoid imitating any single competitor),
propose a design system foundation: typography (2-3 font families max,
full type scale), color palette (primary, secondary, semantic colors for
success/warning/error, full accessible neutral scale), spacing scale (base
unit and multiples), and grid/breakpoint system.

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
3. Loan officer bio card
4. Trust signal bar (licensing/NMLS/security badges)
5. FAQ accordion
6. Rate/comparison table
7. Calculator input/output module
8. Navigation (header, mega-menu if applicable, footer, mobile menu)

For each, note the GenerateBlocks pattern type (Container, Grid, Button,
Query Loop, etc.) that should be used to build it.
```

## 12. Examples

*Sample type scale excerpt:*

| Token | Size (rem) | Use |
|---|---|---|
| `--font-size-h1` | 2.75 | Page H1, hero headline |
| `--font-size-h2` | 2.0 | Section headers |
| `--font-size-body` | 1.0625 | Body copy (17px base for readability on financial content) |
| `--font-size-small` | 0.875 | Disclaimers, fine print |

## 13. Common Mistakes

- Designing beautiful one-off hero sections that cannot be reproduced as reusable GenerateBlocks patterns, creating Stage Gate 10 build debt.
- Choosing decorative fonts or low-contrast color combinations that fail accessibility standards on a financial services site where legal risk from inaccessibility is elevated.
- Presenting only one design direction, collapsing the Stage Gate 7.5 tournament into a rubber-stamp approval rather than a genuine comparative decision.

## 14. Best Practices

- Treat GeneratePress Global Styles (colors, typography, and spacing defined once at the theme level) as the source of truth, with GenerateBlocks patterns consuming those global tokens rather than hardcoding values — this is the single highest-leverage maintainability decision in the entire build.
- Design disclaimer/fine-print typography with the same care as headline typography; on a mortgage site this text carries real legal weight and is read carefully by cautious borrowers.
- Build the loan officer bio card and trust signal bar components early — they appear on nearly every template and their quality disproportionately affects perceived trustworthiness.

## 15. Review Process

Internal design critique with UX Designer and Developer before templates are finalized; Compliance Liaison confirms trust-signal visual prominence meets disclosure visibility requirements.

## 16. Quality Assurance

Primary Eight-Dimension focus: **Accessibility**, **Brand**, **WordPress/GeneratePress/GenerateBlocks Compatibility**. All eight dimensions are formally re-scored in Stage Gate 7.5.

## 17. Exit Criteria

- [ ] Design System Specification and Component Library complete per Checklist
- [ ] At least 2 distinct design directions ready for tournament
- [ ] Developer has confirmed buildability of all components in GenerateBlocks

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v0.x (draft status — not yet approved; approval happens at SG7.5)
- Blueprint: not yet updated (Blueprint reflects only approved states; wait for SG7.5)
- Decision Register: log design direction rationale as `DEC-SG7-00x` (draft status)

## 19. Future Enhancements

Design directions produced here are the direct input to the Stage Gate 7.5 Design Tournament immediately following.

---

# STAGE GATE 7.5 — PROTOTYPE VALIDATION

## 1. Purpose

Subject the design direction(s) produced in Stage Gate 7 to rigorous, structured validation before any production build work begins: a head-to-head Design Tournament, a Benchmark Validation against performance/accessibility/SEO standards, a Future-Proofing Review against the site's 3-5 year growth trajectory, and formal Executive Approval. This is the single most important quality gate in the entire methodology — no engagement proceeds to Volume V without clearing it.

## 2. Business Objectives

- Ensure the client makes an informed, comparative decision rather than an instinctive reaction to a single design.
- Catch performance, accessibility, or scalability defects before they are baked into a full site build.
- Secure unambiguous, documented executive sign-off that unlocks Volume V production work.

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

Compliance Liaison (final disclosure/trust-signal visual sign-off), QA Analyst (early involvement — benchmark validation overlaps with Stage Gate 11 QA criteria applied early)

## 8. Decision Authority

**Client executive sign-off is mandatory and is the hard gate for this entire Volume.** The named Decision Authority (Project Charter, Volume I Sec. 3.4) must sign the Executive Approval Record. No Stage Gate 8 work begins without it.

## 9. Workflow — The Four Validation Activities

```
                    STAGE GATE 7.5 — PROTOTYPE VALIDATION
   ┌─────────────────────────────────────────────────────────────────┐
   │                                                                   │
   │  [A] DESIGN TOURNAMENT                                            │
   │      2-3 fully realized design directions scored head-to-head     │
   │      on a fixed rubric (Sec. 9.1) by both firm and client         │
   │      reviewers                                                    │
   │                          │                                        │
   │                          ▼                                        │
   │  [B] BENCHMARK VALIDATION                                          │
   │      Winning direction stress-tested against performance,          │
   │      accessibility, and SEO-technical benchmarks (Sec. 9.2)        │
   │                          │                                        │
   │                          ▼                                        │
   │  [C] FUTURE-PROOFING REVIEW                                        │
   │      Winning direction evaluated against 3-5 year scale scenario  │
   │      (Sec. 9.3): more pages, more products, more states            │
   │                          │                                        │
   │                          ▼                                        │
   │  [D] EXECUTIVE APPROVAL                                            │
   │      Formal client sign-off session; Executive Approval Record    │
   │      signed by named Decision Authority                            │
   │                                                                   │
   └─────────────────────────────────────────────────────────────────┘
                          │
                          ▼
                Stage Gate 8 (Content Specification) begins
```

### 9.1 Design Tournament Procedure

1. Present 2–3 fully realized design directions (not sketches — complete key-page-template renders) side by side.
2. Score each direction on the **Design Tournament Scoring Matrix** (Sec. 12) across all Eight Dimensions (Volume I Sec. 12.2) plus differentiation-from-competitors.
3. Both firm reviewers and client stakeholders score independently before discussing, to avoid anchoring bias.
4. Reconcile scores in a joint working session; the highest-scoring direction advances, though the client may request specific element cross-pollination (e.g., "Direction B's layout with Direction A's color system") — any such hybrid must be re-scored before proceeding.

### 9.2 Benchmark Validation Procedure

The winning design direction is validated against fixed, non-negotiable benchmarks before it proceeds:

| Benchmark | Standard | Method |
|---|---|---|
| Performance | Projected LCP < 2.5s, INP < 200ms, CLS < 0.1 on representative templates | Static prototype tested via PageSpeed Insights / WebPageTest against a built HTML approximation |
| Accessibility | WCAG 2.1 AA | Automated scan (axe or equivalent) + manual keyboard navigation check |
| SEO-Technical | Heading hierarchy, semantic HTML structure intact per template | Manual review by SEO Specialist against Stage Gate 5 requirements |
| Mobile Usability | No horizontal scroll, tap targets ≥ 44px, readable without zoom | Manual device/viewport testing |

### 9.3 Future-Proofing Review Procedure

Evaluate the winning direction against a defined future-scale scenario documented in the Future-Proofing Review Memo:

- What happens to the navigation and template system if the client adds 3 more states and 2 more loan products?
- Does the component library support a 5x increase in blog/guide content without visual degradation?
- Are there any hardcoded (non-token-based) design decisions that would require a full redesign rather than a parameter change to scale?

### 9.4 Executive Approval Procedure

Formal session with the named Decision Authority. The Executive Approval Record captures: which direction was approved, any conditions attached to approval, the Benchmark Validation and Future-Proofing Review results as attached evidence, and the signature/date.

## 10. Checklist

- [ ] Minimum 2 fully realized design directions presented (not concepts/sketches)
- [ ] Design Tournament Scorecard completed by both firm and client reviewers independently before reconciliation
- [ ] Benchmark Validation Report shows all four benchmarks (Sec. 9.2) at passing status, or documents a specific remediation plan for any that fail
- [ ] Future-Proofing Review Memo completed and no unresolved scalability red flags remain
- [ ] Executive Approval Record signed by the named Decision Authority

## 11. Prompt(s)

**Prompt 7.5.1 — Design Tournament Scorecard Generation**

```
You are facilitating a Design Tournament for [Client Name]'s mortgage
website redesign. Given the attached descriptions/renders of Design
Direction A and Design Direction B, score each 1-5 on: Performance
(perceived weight/complexity), Accessibility (contrast, structure clarity),
SEO (semantic clarity, heading logic), Conversion (CTA clarity, friction),
Brand (distinctiveness vs. competitive set from Stage Gate 2), Scalability
(component reuse evident), Maintainability (design token discipline
evident), WordPress/GeneratePress/GenerateBlocks Compatibility, and
Differentiation from Competitors. Provide a one-sentence justification per
score. Do not simply average toward a tie — identify the genuine strengths
and weaknesses of each direction even if the final scores are close.
```

**Prompt 7.5.2 — Future-Proofing Stress Test**

```
Given the approved design direction's component library and template
designs, stress-test it against this scale scenario: the client expands
from [current state count] to [current + 3] licensed states and adds
[N] new loan products over the next 3 years, and grows its content
library from [current page count] to 5x that count. Identify any
component or template that would require a full redesign (not just new
content) to accommodate this growth, and propose the specific design
token or pattern change needed now to prevent that future rework.
```

## 12. Examples

*Sample Design Tournament Scoring Matrix:*

| Dimension | Direction A | Direction B | Notes |
|---|---|---|---|
| Performance | 4 | 5 | B uses fewer custom web fonts and lighter hero imagery |
| Accessibility | 4 | 4 | Both pass AA; A has marginally tighter link-underline contrast |
| SEO | 4 | 4 | Equivalent heading structure |
| Conversion | 3 | 5 | B's CTA hierarchy is clearer; A has competing CTAs above the fold |
| Brand | 5 | 3 | A is more distinctive vs. competitive set; B reads closer to Competitor A's pattern |
| Scalability | 4 | 5 | B's card component handles variable content length better |
| Maintainability | 4 | 5 | B's token discipline is cleaner |
| GP/GB Compatibility | 5 | 5 | Both fully buildable |
| **Total (of 40)** | **33** | **36** | Client requested A's hero color treatment applied to B — re-score as hybrid before final approval |

## 13. Common Mistakes

- Skipping independent scoring and going straight to group discussion, which allows the loudest stakeholder's preference to dominate.
- Treating Benchmark Validation as a formality rather than gating criteria — a design that fails Core Web Vitals projections at this stage is dramatically cheaper to fix than after Stage Gate 10 build.
- Allowing "executive approval" to happen informally in a hallway conversation instead of producing the signed Executive Approval Record — this creates disputes later about what was actually approved.

## 14. Best Practices

- Build both/all tournament candidates to comparable fidelity — a polished Direction A against a rough Direction B is not a fair tournament and produces a biased result.
- When the client requests a hybrid of elements from multiple directions, always re-score the hybrid explicitly rather than assuming it inherits the higher of the two scores.
- Attach the Benchmark Validation Report and Future-Proofing Review Memo directly to the Executive Approval Record as evidence — this protects both the firm and the client if scope questions arise later.

## 15. Review Process

Engagement Lead facilitates the full sequence (Sec. 9.1–9.4); QA Analyst independently verifies the Benchmark Validation Report's technical claims before it is presented to the client.

## 16. Quality Assurance

All Eight Dimensions (Volume I Sec. 12.2) are formally scored in this gate — this is the methodology's designated comprehensive quality checkpoint before production begins.

## 17. Exit Criteria

- [ ] Design Tournament completed with reconciled scores
- [ ] Benchmark Validation Report shows passing status or documented remediation plan
- [ ] Future-Proofing Review Memo completed with no unresolved red flags
- [ ] Executive Approval Record signed by named Decision Authority

## 18. Knowledge Base / Blueprint / Decision Register Updates

- KB: all four Required Documents saved v1.0
- Blueprint: "Design System" section populated with the approved direction, superseding any draft SG7 entries
- Decision Register: `DEC-SG7.5-001` (Executive Approval) logged as **Irreversible** — any post-approval design direction change is a major Change Request requiring re-running this gate

## 19. Future Enhancements

The approved design system is the binding input to Stage Gate 10 (AI Build Package) and Stage Gate 10.5 (WordPress Implementation Blueprint). It is not revisited until Stage Gate 11.5's Post-Launch Growth Program proposes data-driven, incremental refinements — never a wholesale redesign without re-running this gate.

---

## Volume IV Appendix: GeneratePress Implementation Guidance

- Use **GeneratePress Global Styles** (Customizer → Global Colors, Global Typography) to encode every token from the Design System Specification exactly once. Never apply one-off inline color or font overrides in individual GenerateBlocks patterns.
- Use the **Site Library** to save every approved component as a reusable pattern (Global block where the same instance must update everywhere — e.g., the trust signal bar — vs. Local block where instances vary per page).
- Use **Element hooks** (GeneratePress Premium's Elements module) for the trust signal bar, header, and footer so they are maintained in exactly one place and inherited across all templates defined in Stage Gate 4.
- Confirm **Typography** settings use `clamp()`-based fluid type scaling where GeneratePress supports it, to satisfy the mobile-first requirement without a proliferation of breakpoint-specific overrides.

## Volume IV Appendix: GenerateBlocks Implementation Guidance

- Build every reusable UX pattern (Stage Gate 6) as a **GenerateBlocks pattern**, composed of Container, Grid, and Button blocks with CSS classes tied to Global Style tokens — not ad hoc inline styles per instance.
- Use the **Query Loop** block for any repeating content (loan officer directory, guide/blog listings, testimonials) rather than manually duplicating card markup — this directly satisfies the Scalability dimension.
- Name every GenerateBlocks class systematically (e.g., `.gb-card--loan-officer`, `.gb-cta--primary`) and document the naming convention in the GeneratePress/GenerateBlocks Implementation Notes — this is what makes the Stage Gate 10 AI Build Package unambiguous for a build model or developer to implement correctly.
- Test every pattern's responsive behavior at the exact breakpoints defined in the Design System Specification grid, not just "looks fine" at arbitrary window widths.

---

*End of Volume IV. Continue to Volume V — Production.*
