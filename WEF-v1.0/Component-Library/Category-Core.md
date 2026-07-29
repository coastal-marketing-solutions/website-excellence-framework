# COMPONENT LIBRARY — CORE

*Website Excellence Framework (WEF) v1.0 — see `00-Component-Library-Index.md` for schema and governance*

---

## CL-CORE-001 — Button

**Purpose / When to Use:** The site's primary CTA control — used site-wide for the main conversion action (e.g., "Apply Now," "Get Started," "Schedule a Consultation") and its secondary companion action (e.g., "Get Pre-Qualified," "Learn More"). Every clickable action that isn't a text link should be a Button variant, not a one-off styled element.

**When NOT to Use:** Don't create a new button style for a single page's CTA — extend the variant system (Sec. Interface below) instead. Don't use `primary` for more than one CTA in the same viewport — competing primary CTAs dilute conversion focus (a documented mistake from the original engagement; see Design, Sec. 14 Common Mistakes).

**Interface:**
```
<Button variant="primary|secondary|inverse" size="sm|md|lg">Label</Button>
```
`primary` — the locked brand CTA treatment (in the originating engagement: gold gradient fill, mandatory contrasting border, hover solidifies to a single accent color). `secondary` — outline treatment, fills solid on hover. `inverse` — for use on dark/brand-color hero or footer sections.

**Design Token Dependencies:** Primary/secondary/accent color tokens, border-width token, radius token, type-scale token (label size).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Build as a Button block with a custom CSS class per variant (e.g., `.gb-cta--primary`), consuming Global Style color tokens — never hardcoded hex values. See Design, Appendix (GenerateBlocks Implementation Guidance).

**Compliance Sensitivity:** Low on its own, but if the `primary` variant's exact treatment was locked as a branded, contrast-verified decision (as in the originating engagement), that specific token combination belongs on the Design Constraints Package's Do-Not-Break List — the *component* is freely reusable, but a *locked instance* of it may not be.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — `primary`/`secondary` pair used as "Apply Now" / "Get Pre-Qualified."

**Industry Module Fit:** Universal — every Industry Module needs a primary CTA control.

**Status:** Active. **Version:** v1.0.

---

## CL-CORE-002 — Icon

**Purpose / When to Use:** A consistent icon system wrapper, used anywhere a small pictorial marker adds scan-ability (trust badges, list items, feature callouts, form field affordances).

**When NOT to Use:** Don't hand-draw or one-off source a new icon set for a single page — pull from the confirmed icon library so visual language stays consistent site-wide.

**Interface:**
```
<Icon name="[icon-key]" size={number} />
```

**Design Token Dependencies:** Icon color inherits from the surrounding text-color token unless explicitly overridden; size follows the spacing/type scale, not arbitrary pixel values.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** On the default stack, implemented as a thin wrapper over an open icon library (the originating engagement used Lucide, loaded via a script include, with icons instantiated on mount) — confirm licensing and self-hosting requirements per Charter before assuming a CDN-loaded script is acceptable in a security-sensitive engagement. On a Charter-confirmed alternative stack, use whatever icon-loading mechanism that stack's Design Constraints Package specifies.

**Compliance Sensitivity:** None.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — Lucide icon set, e.g. `shield-check` for trust signals.

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.
