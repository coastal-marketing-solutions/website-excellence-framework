# COMPONENT LIBRARY — SURFACES

*Website Excellence Framework (WEF) v1.0 — see `00-Component-Library-Index.md` for schema and governance*

---

## CL-SURF-001 — Card

**Purpose / When to Use:** The base surface primitive underlying every other card-family component in this category (LocationCard, OfferingCard, StaffBioCard) — a bounded content container with a fill, border, radius, and subtle elevation. Use directly for any simple card content that doesn't fit a more specific variant below.

**When NOT to Use:** Don't restyle Card's base treatment (fill/border/radius/elevation) per instance — extend it into a named variant (as the three below do) so the base primitive stays a single, consistent source of truth.

**Interface:**
```
<Card>{content}</Card>
```

**Design Token Dependencies:** Surface-fill color token, border color/width tokens, radius token, elevation/shadow token.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Build as a base Container pattern that LocationCard/OfferingCard/StaffBioCard compose on top of, rather than three independently-styled card patterns — this is what keeps a future brand refresh (new radius, new elevation) a one-place token change instead of a three-pattern edit.

**Compliance Sensitivity:** None on its own.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — base primitive for LoanProgramCard, TeamBioCard, and CityCard (generalized here as OfferingCard, StaffBioCard, and LocationCard).

**Industry Module Fit:** Universal.

**Status:** Active. **Version:** v1.0.

---

## CL-SURF-002 — LocationCard

*(Generalized from the originating engagement's `CityCard`.)*

**Purpose / When to Use:** A card representing one location/service-area in a coverage-area grid — for any Module with a multi-location or multi-service-area footprint (city pages, branch locations, licensed-state coverage).

**When NOT to Use:** Don't use for a single-location "About/Contact" address block — that's a simpler layout, not a repeating grid card.

**Interface:**
```
<LocationCard name="City or Area" region="State/County" href="[canonical detail URL]" image={optional} />
```

**Interaction Contract:** When the card is an entry point to a location detail page, the whole non-interactive card surface activates one semantic link to the approved canonical `href`. Provide visible hover and keyboard-focus states and a minimum 44×44 CSS-pixel target. Do not nest buttons, secondary links, or other interactive controls inside the enclosing link; if secondary actions are required, use a non-enclosing card structure with separately labeled controls. Verify keyboard traversal, single-column mobile behavior, variable location-name length, and the final destination after redirects.

**Design Token Dependencies:** Extends Card (CL-SURF-001); typography tokens for the location name/region.

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Build the coverage-area grid as a **Query Loop** (or platform-equivalent repeating-content mechanism), not hand-duplicated per-city markup — this directly satisfies the Scalability dimension and avoids the defect-propagation failure mode in Governance RETRO-004, especially important here since this is exactly the component type most likely to be duplicated many times (one per city/area). Implement a whole-card link without invalid nested interactive markup; the exact wrapper technique may vary by block/plugin version, but the rendered DOM and keyboard behavior must satisfy the Interaction Contract.

**Compliance Sensitivity:** Low, unless area-specific claims (e.g., licensing coverage) are implied — confirm against the Module's Regulatory & Compliance Landscape if the card asserts anything beyond "we serve this area."

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — as `CityCard`, used in a city/service-area coverage grid; no location photography was supplied in that engagement, so the image slot rendered a placeholder — real imagery is a per-engagement asset requirement, not part of the component itself.

**Industry Module Fit:** High-value for any Module with a multi-location footprint (real estate, home services, medical/healthcare with multiple clinic locations, mortgage lending with multi-state/multi-county coverage).

**Status:** Active. **Version:** v1.1.

---

## CL-SURF-003 — OfferingCard

*(Generalized from the originating engagement's `LoanProgramCard`.)*

**Purpose / When to Use:** A card representing one product, program, service, or practice area in a grid of offerings — the homepage/offerings-page grid pattern (icon, title, short description, "Learn more" link) used across nearly every Industry Module this framework serves.

**When NOT to Use:** Don't use for a detailed offering page's own content — this card is a summary/entry-point into that page, not a substitute for the Content Specification (Development, SG8) that page itself needs.

**Interface:**
```
<OfferingCard icon="[icon-key]" title="Offering Name" description="One-sentence summary." href="[link to detail page]" />
```

**Design Token Dependencies:** Extends Card (CL-SURF-001); icon-roundel accent-color token, display-type token (title), body-type token (description).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Build the offerings grid as a **Query Loop** where the offering count is expected to grow (product catalog, expanding service list); a static Grid pattern is acceptable only where the offering set is small and genuinely fixed.

**Compliance Sensitivity:** Low for the card itself; the description copy should trace back to approved Content Specification/Copy (SG8/SG9), not be invented ad hoc at the component level.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — as `LoanProgramCard`, used in the homepage/program-grid for offerings like Conventional, FHA, VA, and Non-QM loan programs.

**Industry Module Fit:** Universal — a law firm's practice-area grid, a home services company's service grid, a SaaS company's feature/plan grid, and a medical practice's specialty grid are all structurally this same card.

**Status:** Active. **Version:** v1.0.

---

## CL-SURF-004 — StaffBioCard

*(Generalized from the originating engagement's `TeamBioCard`.)*

**Purpose / When to Use:** A card representing one team member/practitioner — photo, name, title, individual credential/license number (where applicable), and contact affordances (phone/email icons) — used in a team directory grid or an individual practitioner profile context.

**When NOT to Use:** Don't use as a substitute for a full individual practitioner profile page where the Module's Content Model calls for one (e.g., a full loan-officer or attorney bio page) — this card is the directory-grid entry point, not the full profile.

**Interface:**
```
<StaffBioCard name="Full Name" title="Role/Title" credentialId="[license/credential #]" phone="..." email="..." photo={optional} />
```

**Design Token Dependencies:** Extends Card (CL-SURF-001); typography tokens (name, title, credential), icon tokens (phone/email affordances).

**Platform Implementation Note(s) — GeneratePress/GenerateBlocks:** Same Query Loop discipline as LocationCard/OfferingCard for a team directory grid of any meaningful size.

**Compliance Sensitivity:** **Moderate to high** — the individual credential/license number field is regulated content in most professional-services Modules (mortgage loan officer NMLS numbers, attorney bar numbers, medical practitioner license numbers); confirm the exact required format and placement against the active Industry Module before treating this as purely cosmetic.

**Known Implementations:** Mortgage Lending Module engagement, 2026-07 — as `TeamBioCard`, with individual NMLS number, phone, and email per loan officer; no real staff photography was supplied in that engagement, so the photo area rendered a neutral placeholder.

**Industry Module Fit:** High-value for any Module built around named, individually-licensed or individually-credentialed practitioners (mortgage lending, law firm, medical/healthcare, financial advisor, real estate).

**Status:** Active. **Version:** v1.0.
