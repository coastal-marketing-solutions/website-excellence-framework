# COMPONENT LIBRARY — FEEDBACK

*Website Excellence Framework (WEF) v1.0 — see `00-Component-Library-Index.md` for schema and governance*

---

## CL-FDBK-001 — Badge

**Purpose / When to Use:** A small uppercase pill used as an "eyebrow" label above a heading (e.g., a section category label) or as a status flag on a card (e.g., "Featured," "New").

**When NOT to Use:** Don't use Badge for anything requiring user interaction or removal — that's Tag (CL-FDBK-002). Don't use more than one Badge per component instance; it's an accent, not a layout element.

**Interface:**
```
<Badge tone="accent|solid|outline">Label</Badge>
```
`accent` — default subtle-accent-color treatment. `solid` — high-contrast solid fill, for use on light backgrounds. `outline` — for use on dark/brand-color backgrounds where a solid fill would be too heavy.

**Design Token Dependencies:** Accent color token, type-scale token (label/caption size), radius token (pill shape).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Simple inline element with a custom CSS class per tone; no interactivity required.

**Compliance Sensitivity:** None on its own — if used to flag regulated content (e.g., a rate disclaimer trigger), the label copy itself should trace back to the Compliance Content Checklist (Development, SG8), not be invented ad hoc.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — used as a category eyebrow above loan-program section headings.

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.

---

## CL-FDBK-002 — Tag

**Purpose / When to Use:** A dismissible filter chip — e.g., an active filter in a location/service-area or category filter UI.

**When NOT to Use:** Don't use for a static, non-removable label — that's Badge (CL-FDBK-001).

**Interface:**
```
<Tag onRemove={handler}>Label</Tag>
```

**Design Token Dependencies:** Neutral/accent color tokens, type-scale token, radius token.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Requires a small amount of interactive JS for the remove action — on the default stack, a lightweight script enqueued alongside the pattern; on a static/custom-code alternative stack, implement per that stack's interactivity convention (see Design Constraints Package, Sec. 2, Structural/Buildability Constraints).

**Compliance Sensitivity:** None.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — scoped for a city/service-area filter UI (filter interaction itself not built in that engagement; component scaffolded for future use).

**Industry Module Fit:** Most useful for any Module with a filterable directory/listing page (service areas, practice areas, specialties, product catalog).

**Status:** Active. **Version:** v1.0.
