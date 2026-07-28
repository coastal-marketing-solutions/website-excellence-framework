# Contributing to the Website Excellence Framework

Thanks for considering a contribution. This framework covers regulated industries where accuracy genuinely matters — the most valuable contributions are corrections and additions from people who actually work in the industry a given Module covers.

## Preferred path: open an Issue

Most contributions should start as an [Issue](../../issues), even if you already know the exact fix. This keeps a public record of what was flagged, by whom, and why — consistent with how this framework treats its own Decision Register internally.

A good issue includes:

1. **Which file** the problem or suggestion applies to (e.g., `Industry-Modules/Module-Law-Firm.md`, Section 2).
2. **What's wrong or missing**, stated plainly.
3. **A source**, wherever you're asserting a fact — a statute citation, a regulator's page, a link to a live competitor site the framework should reference. Claims without a source are treated as flags for further research, not as confirmed fixes.
4. **Your read on the fix**, if you have one — even a rough suggestion is useful.

## Proposing a new Industry Module

Every Module follows the same fixed 12-part template (see [`Industry-Modules/00-Module-Template-and-Index.md`](Industry-Modules/00-Module-Template-and-Index.md)):

1. Module Overview & Applicability
2. Regulatory & Compliance Landscape
3. Persona Library
4. Competitive Landscape Notes
5. Positioning & Messaging Patterns
6. Information Architecture Patterns
7. SEO & Keyword Strategy
8. Trust Signal Requirements
9. Content Model & Page Types
10. Stage Gate Injection Map
11. Module-Specific Prompt Library Additions
12. Module Version History

If you're proposing a new vertical, open an Issue naming the industry, why it's distinct enough from the existing Modules to warrant its own (rather than being a persona/niche inside one), and — ideally — a couple of real example sites in that space. You don't need to fill out all 12 sections yourself; a strong Issue describing the gap is enough to start from.

## Pull requests

PRs are welcome, especially for:

- Corrections to a single Module's **Regulatory & Compliance Landscape** section (the most time-sensitive content in the framework — see each Module's own note that this section should be reviewed at least annually).
- Filling in a documented **Module Gap**.
- Fixing broken cross-references between files.

Please keep PRs scoped to one Module or one Core Methodology file at a time — this framework is deliberately structured so that a change to, say, the Medical/Healthcare Module never requires touching the Core, and reviews are easier when PRs respect that boundary.

**Do not restructure the fixed templates** (the 19-part Stage Gate template in the Core, or the 12-part Module template) without opening an Issue first — these structures are what let every Module and every Stage Gate stay mutually consistent, and a structural change has ripple effects across the whole library.

## What not to submit

- Legal, tax, or regulatory conclusions stated as fact without a citable source. Flag uncertainty explicitly (this framework's own convention, seen throughout, is `[COMPLIANCE REVIEW NEEDED]` or `[unverified estimate]`) rather than asserting a claim confidently.
- Vendor-specific promotional content. The default technology stack (Governance §13.4) is documented as a firm default, not an endorsement to be expanded with unrelated product pitches.
- Anything you don't have the right to license under CC BY-NC 4.0 (see [`LICENSE`](LICENSE)) — by submitting a PR, you're agreeing your contribution can be published under that license.

## Code of conduct

Be specific, be sourced, and assume good faith. Disagreements about regulatory interpretation are normal and useful — resolve them with citations, not assertions.
