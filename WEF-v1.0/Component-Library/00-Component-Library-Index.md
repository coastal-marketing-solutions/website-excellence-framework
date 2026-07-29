# COMPONENT LIBRARY — INDEX & GOVERNANCE

*Website Excellence Framework (WEF) v1.0*

---

## Purpose

The Component Library is the cross-engagement, cross-industry registry of every reusable UI component this firm has already designed and built — what it does, when to use it, what it depends on, and where it's already been implemented. It exists to solve a specific, evidenced problem: without it, every engagement's Design discipline (Sec. 05, SG7) re-invents components from scratch, every engagement's Development discipline (Sec. 06, SG10/10.5) has to reverse-engineer how to build them, and every AI coding agent doing the implementation is working against a fresh, unfamiliar vocabulary instead of a previously-solved one (Governance, Sec. 15.4, RETRO-005).

This is the component-level counterpart to two things that already exist in this manual: Industry Modules (`/Industry-Modules/`) capture reusable *vertical knowledge*; the Component Library captures reusable *buildable UI*. Both are optional-but-encouraged inputs an engagement checks before doing net-new work, and both compound in value the more engagements run through this framework.

## Relationship to the Design Constraints Package

The Design Constraints Package (Design, Appendix) is engagement-specific — it declares what one client's site is built from and must not break. The Component Library is firm-wide — it's the pool of already-built components a new engagement's Design Constraints Package should draw from before inventing anything new. A healthy engagement's Design Constraints Package cites Component Library entries by ID wherever a fit exists, and only defines genuinely new components for what the registry doesn't yet cover.

## Governance Rule — Check Before You Build

**Stage Gate 7 (Design, Sec. 10, Workflow step 1) now begins with a Component Library check, not a blank page.** Before designing any component, the Visual Designer (human or AI design tool — Claude Design, OpenAI Design, Figma, Canva, Adobe Express/Firefly, per AI Workflows Sec. 3.4) checks this registry for an existing match. A match doesn't have to be used unmodified — restyling an existing component to a new brand's tokens is expected and cheap. What should not happen routinely is building a structurally new component (a new card layout, a new form pattern) when a structurally equivalent one already exists in the registry, re-solving a problem this firm has already solved.

## Registry Entry Schema

| Field | Description |
|---|---|
| Component ID | Format `CL-{CATEGORY}-{sequence}`, e.g. `CL-SURF-002` |
| Name | Generic, reusable name — never a client-specific name |
| Category | One of: Core, Feedback, Forms, Marketing & Trust, Surfaces, Navigation *(extensible — propose a new category via the Change Request process, Sec. 13.2 below)* |
| Purpose / When to Use | What problem it solves and the situation that calls for it |
| When NOT to Use | Explicit anti-patterns — misuse is as important to document as correct use |
| Interface | The prop/variant contract, in the same generic pseudo-JSX shorthand used throughout this registry (framework-agnostic — it describes the component's *shape*, not a mandate to build in React; the actual implementation target is the confirmed technology stack, Governance Sec. 13.4.1) |
| Design Token Dependencies | Which Design Constraints Package token categories it consumes (color, type, spacing) — never hardcoded values |
| Platform Implementation Note(s) | **One entry per stack this component has actually been built on** — e.g., a GeneratePress/GenerateBlocks note and, once built, a separate Custom-PHP/HTML or other-stack note for the same component. Never overwrite an existing stack's note when adding a new one; append. This is what keeps the registry theme-portable (Governance, Sec. 13.4.2) — the token/interface fields above are the durable, stack-independent asset, and this field is the only stack-specific part of an entry |
| Compliance Sensitivity | Whether this component is a near-automatic **Do-Not-Break List** candidate (Design, Appendix) — components carrying regulatory disclosure content almost always are |
| Known Implementations | Engagement, Industry Module, and date for every confirmed real-world use — the evidence trail that keeps this registry grounded, not speculative |
| Industry Module Fit | Which Industry Modules this suits well, and any it doesn't |
| Status | Active / Experimental / Deprecated |
| Version History | Brief changelog |

## Category Files

| File | Contents |
|---|---|
| `Category-Core.md` | Foundational primitives used inside nearly every other component (Button, Icon) |
| `Category-Feedback.md` | Small status/label elements (Badge, Tag) |
| `Category-Forms.md` | Form field primitives (Input, Select, Checkbox, Radio, Switch) |
| `Category-Marketing-Trust.md` | Conversion and compliance-carrying components (TrustBar, ComplianceFooter, LeadCaptureForm) |
| `Category-Surfaces.md` | Card-family layout components (Card, LocationCard, OfferingCard, StaffBioCard) |

Categories mirror Claude Design's own native export taxonomy (`core/`, `feedback/`, `forms/`, `marketing/`, `surfaces/`) deliberately — this keeps a Claude Design export's folder structure and this registry's category structure in sync, so promoting a component from a fresh engagement export into the registry is a near-direct copy, not a re-organization exercise.

## New Component Promotion Process

Mirrors the New Module Development Process (Governance, Sec. 13.6), scaled down:

1. A component is built for a specific engagement, inside that engagement's own Design Constraints Package / component library.
2. At or before Stage Gate 11.5 (Post-Launch Growth) close-out, the Engagement Lead or AI Orchestrator reviews the engagement's components against this registry and flags any that are **structurally novel and not client-specific** (no hardcoded business logic, no client-specific copy baked into the component itself — data belongs in props/content, not in the component).
3. Flagged components are generalized (client-specific example values replaced with generic placeholders, per the pattern every existing entry in this registry already follows) and added to the relevant Category file via Change Request (Sec. 13.2 below), citing the originating engagement as the first Known Implementation.
4. A component that is genuinely client-specific (baked-in business logic, one-off layout that doesn't generalize) is *not* promoted — it stays local to that engagement's own Design Constraints Package. Forcing every component into the shared registry defeats the purpose; only genuinely reusable ones belong here.

## Change Request Process

Adding, modifying, or deprecating a registry entry follows the same Change Request discipline as the Core Methodology and Industry Modules (Governance, Sec. 13.2) — reviewed by the Methodology Governance Board, logged in this file's own revision log below, released as a new version. A component is never silently edited; a breaking change to an existing entry's interface increments its Version History and flags every existing Known Implementation for a compatibility check before the new version is treated as safe to reuse elsewhere.

## Master Component Table (current)

| ID | Name | Category | Status | First Seen |
|---|---|---|---|---|
| CL-CORE-001 | Button | Core | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-CORE-002 | Icon | Core | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FDBK-001 | Badge | Feedback | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FDBK-002 | Tag | Feedback | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FORM-001 | Input | Forms | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FORM-002 | Select | Forms | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FORM-003 | Checkbox | Forms | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FORM-004 | Radio | Forms | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-FORM-005 | Switch | Forms | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-MKTG-001 | TrustBar | Marketing & Trust | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-MKTG-002 | ComplianceFooter | Marketing & Trust | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-MKTG-003 | LeadCaptureForm | Marketing & Trust | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-SURF-001 | Card | Surfaces | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-SURF-002 | LocationCard | Surfaces | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-SURF-003 | OfferingCard | Surfaces | Active | Mortgage Lending Module engagement, 2026-07 |
| CL-SURF-004 | StaffBioCard | Surfaces | Active | Mortgage Lending Module engagement, 2026-07 |

This is the registry's seed set — all 16 entries promoted from the framework's first full engagement (mortgage lending vertical), generalized from their original client-specific implementation. This is expected to be the smallest this registry ever is; every future engagement is a candidate source of new entries via the Promotion Process above.

## Revision Log

| Change ID | Date | Description | Approved By |
|---|---|---|---|
| CR-016 | 2026-07-28 | Initial Component Library established: this index plus 5 Category files, seeded with 16 components generalized from the framework's first full engagement (Mortgage Lending Module) and its Claude Design export. | Methodology Governance Board |

---

*Return to Core Methodology or the active Industry Module as needed. This library has no fixed "next chapter" — it is referenced from Design (Sec. 05) and Development (Sec. 06), not read sequentially.*
