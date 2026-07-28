# INDUSTRY MODULE — CASH HOME BUYER / REAL ESTATE INVESTOR

*Website Excellence Framework (WEF) v1.0 — Module Version 1.0*

*Authored via the New Module Development Process (Core Methodology, Governance, Section 13.6)*

---

## Development Note (New Module Development Process Record)

Per Governance, Section 13.6, this Module was authored as follows:

1. **Closest existing Module identified as structural starting point:** the **Real Estate Module** — both serve residential property transactions and share IA/trust-signal DNA. However, the business model is materially different (this Module's client *is* the buyer, purchasing directly from a homeowner for cash, with no MLS listing, no agent representation of the seller, and no buyer financing contingency), so the Regulatory & Compliance Landscape, Persona Library, and Content Model required substantial original authoring rather than a light adaptation.
2. **Research conducted** against: (a) Carrot.com's published SEO methodology and help-center documentation, the dominant website-platform vendor for this vertical; (b) the live site structure of [bluewavehomebuyers.com](https://www.bluewavehomebuyers.com/) (a Carrot-built regional cash buyer, cited by the requesting user as a representative example); (c) competitor archetypes including HomeVestors/"We Buy Ugly Houses," algorithmic iBuyers (Opendoor, Offerpad), and cash-buyer comparison aggregators (Houzeo, iBuyer.com); (d) current state real estate wholesaling/disclosure law, TCPA telemarketing rules, and FTC/state Attorney General enforcement history against predatory home-buying practices targeting distressed homeowners.
3. Findings are cited inline below where they directly informed a specific requirement.
4. Submitted directly to the Methodology Governance Board as **Change Request CR-007** (see Front Matter Revision Log) and approved for addition to the permanent Industry Modules library at v1.0, per Section 13.6 Step 4 — there was no live client engagement to attach the draft phase to (Step 3), so the draft-to-final step was compressed into a single authoring pass; this is noted here for audit transparency rather than treated as a shortcut to be repeated by default. Future refinements should still follow the full engagement-validated Change Request path (Governance, Sec. 9.5) where possible.

---

## 1. Module Overview & Applicability

This Module applies to businesses that purchase residential (and occasionally small multifamily or land) properties **directly from homeowners for cash** — commonly self-described as "we buy houses," "cash home buyers," or "sell my house fast" companies. This includes:

- **Buy-and-hold or fix-and-flip investors** who take title and close with their own or private/hard-money capital.
- **Wholesalers** who contract to purchase equitable interest in a property and assign or double-close the contract to an end buyer, typically without ever taking title themselves.
- **Hybrid "buy-box" companies** (the Blue Wave Home Buyers profile) operating regionally, typically built on Carrot.com or a similar investor-website SaaS platform, with a lead-generation-first website design.

**Explicitly out of scope / requires a different Module or a documented blend:**

- **Traditional real estate brokerage/agent representation** (listing on MLS, representing a buyer or seller in a commission-based transaction) — use the **Real Estate Module**. A brokerage with an in-house cash-buying arm should blend Real Estate (primary) with this Module (secondary), per Governance Section 1.5.
- **Large-scale algorithmic iBuyer platforms** (Opendoor-style instant-offer technology companies) — a materially different business model (proprietary pricing algorithms, narrow automated buy-box, venture-backed scale, in-house transaction/title operations) that this Module's Competitive Landscape Notes (Section 4) treat as a *competitor archetype*, not as the client profile this Module is written for. A future dedicated iBuyer-Platform Module would be a reasonable addition if the firm takes on that kind of client.

**Platform Note:** Carrot.com is the dominant proprietary SaaS platform in this vertical and its published SEO research (Section 7) is a primary evidence source for this Module. Carrot is not, however, the WEF default technology stack (Governance, Sec. 13.4). Where a prospective client is already running on Carrot, the Project Charter must make an explicit, logged Decision Register entry on **whether to remain on Carrot or migrate to the WEF default stack** (WordPress/GeneratePress/GenerateBlocks). Carrot offers vertical-specific out-of-box tooling (lead-routing CRM, investor-specific landing page types) at a recurring SaaS cost and with less design/ownership control; the WEF default stack offers full design control, no per-site platform fee, and consistency with the firm's broader delivery capability, at the cost of rebuilding Carrot's investor-specific CRM/lead-routing functionality via the Integration Requirements Spec (Development discipline, SG10). Neither is a universally correct default — this is a genuine Charter-level decision, not a foregone conclusion.

## 2. Regulatory & Compliance Landscape

This is one of the higher regulatory-intensity Modules in the library, and — distinctively among this library's Modules — a meaningful share of that intensity comes from **consumer-protection and predatory-practice enforcement history specific to this business model**, not just professional licensing.

- **State real estate wholesaling and equitable-interest disclosure laws.** A wave of new state statutes (Oregon, Maryland, Oklahoma, Ohio, Tennessee, and others enacted new requirements in 2025) require a wholesaler to disclose, in writing and often in a specific format (e.g., Ohio requires a standalone disclosure in bold 12-point font), that they hold only an equitable interest and not legal title, and that they intend to assign or resell that interest. Several states grant the seller a statutory right to cancel the contract without penalty (commonly within 3 business days of receiving the disclosure) if this disclosure is missed. **Texas** treats marketing a property for sale without disclosing an equitable-interest position as unlicensed brokerage activity. Verify the client's specific state(s) of operation against current law at engagement start — this is an actively legislating area (Governance, Sec. 13.7 currency review applies with particular force here).
- **Real estate license thresholds.** Several states cap the number of wholesale transactions an unlicensed individual/entity may conduct per year before a real estate license (or a specific wholesaler registration) is required. Confirm the client's transaction volume and structure against their state's specific threshold.
- **FTC and state Attorney General predatory-practice enforcement.** The FTC has brought 40+ cases since 2008 against foreclosure-rescue and mortgage-relief scams, and more than 20 state enforcement actions (including a widely cited Illinois Attorney General campaign) have targeted "we buy houses"-style operators for high-pressure tactics, misleading value representations, and targeting of financially distressed, elderly, and — per multiple cited actions — disproportionately Black and Latinx homeowners and neighborhoods. **A well-known national franchise (HomeVestors/"We Buy Ugly Houses") has had individual franchisees subject to allegations of targeting elderly and ill homeowners.** This history is the single most important piece of context for this Module: it means the burden of proof for *not* looking predatory is higher here than in almost any other Module in this library, and it directly shapes Sections 5, 8, and 9 below.
- **State foreclosure-consultant / homeowner bill of rights statutes.** Many states (following California's lead) separately regulate anyone contacting a homeowner specifically *because* they are in foreclosure — often requiring a specific contract form, banning upfront fees, and granting rescission rights. These rules can apply on top of, not instead of, the general wholesaling disclosure rules above if the client's marketing specifically targets pre-foreclosure homeowners (which, per the Persona Library, it typically does).
- **TCPA (Telephone Consumer Protection Act)** — governs any cold calling or texting of homeowner leads (commonly sourced via skip-tracing distressed-property/absentee-owner lists in this industry's broader marketing practice, separate from the website itself). Cold calls/texts require Do-Not-Call Registry scrubbing, are restricted to 8 a.m.–9 p.m. local time for the recipient, and require express consent for most real estate cold-outreach use cases since the established-business-relationship exception rarely applies to first-contact outreach. While the *website* itself is primarily an inbound-lead-capture instrument, its lead forms are frequently the source of the "prior express written consent" the business relies on for *subsequent* outbound texting/calling — meaning SMS/call consent language on every lead form is a compliance-load-bearing piece of copy, not boilerplate.
- **Fair Housing Act** — applies to marketing and content exactly as in the Real Estate Module: no persona-targeting or content language that could function as steering by protected class, including in any geo-targeted advertising built on top of the site.
- **Escrow/trust handling of earnest money** — where the client's process involves an earnest money deposit, state-specific escrow/trust account handling rules apply; the "How It Works" page (Section 9) should describe this accurately rather than vaguely.

**Known claim-risk language patterns:** urgency-manufacturing framing that exploits distress rather than informs ("the bank will take your home — act now!"), unsubstantiated superiority claims ("we always pay more than [named competitor/iBuyer]"), "we pay full market value" (inherently in tension with the investor margin the business model requires — a well-known FTC/state-AG scrutiny trigger), and any implication of a guaranteed timeline or guaranteed offer amount before an actual property evaluation.

## 3. Persona Library

| Persona | Primary Need | Top Decision Drivers | Top Objections |
|---|---|---|---|
| Pre-Foreclosure Homeowner | Sell before auction/repossession | Speed, avoiding public auction and further credit damage, discretion | Distrust that the buyer is "vulturing" on their distress; fear of scams given this vertical's known predatory history |
| Inherited Property / Probate Heir | Liquidate a property they didn't choose to own, often long-distance | Convenience, not managing repairs/cleanout/utilities on a vacant property, ease of splitting proceeds among co-heirs | Emotional attachment to a family property; uncertainty about their legal authority to sell during probate |
| Tired Landlord | Exit a rental property, sometimes with tenants still in place | As-is sale including with tenants occupying, no repair requirement, avoiding an eviction process before sale | Getting a fair price relative to market value; uncertainty about capital gains or 1031 alternatives |
| Divorcing Co-Owner(s) | Liquidate jointly owned property quickly and neutrally | Speed, a process that doesn't require the ex-spouses to coordinate extensively, neutrality | Fairness of the offer to both parties; needing mutual agreement to proceed |
| Distressed-Property Owner (fire, flood, hoarder, major deferred maintenance) | Sell a property that would be difficult to sell on the open market | Genuine as-is purchase regardless of condition, no repair or cleanout obligation | Fear that the buyer is exploiting the property's condition for an unreasonably low offer |
| Downsizing Senior | Move without the burden of prepping, staging, and showing a home | Simplicity, no showings, flexible closing/move-out timeline | Trusting an unfamiliar buyer over a known local realtor; getting fair value |

## 4. Competitive Landscape Notes

Four distinct competitor archetypes, per direct research:

1. **National franchise brands** (e.g., HomeVestors/"We Buy Ugly Houses") — strong paid-media and brand-recognition dominance, but franchise-level execution and reputation are inconsistent, and the brand carries a documented history of individual-franchisee predatory-practice allegations that creates a trust deficit this Module's client can differentiate against honestly.
2. **Algorithmic iBuyers** (Opendoor, Offerpad, and similar) — strong instant-offer technology and UX, but a narrow, automated buy-box that excludes older, rural, or damaged properties, and charge service fees in the 5–8% range on top of closing costs — materially different from the zero-fee true-cash-buyer model, and a legitimate, honest differentiation point (per research: "if your home has fire damage, code violations, an inherited title, tenants in place, or simply needs work, you'll usually be told the iBuyer can't make an offer").
3. **Local/regional independent investors**, typically Carrot-built (the client's own likely peer set) — genuine local-market authenticity and personal story, but research found the common failure pattern is stopping at a handful of city pages and a generic "how it works" page without building out the deeper niche/situational topical authority (foreclosure, probate, divorce, etc.) that Carrot's own published methodology recommends — this is the single most consistent, evidence-backed white-space opportunity in this vertical. A second common failure pattern is templated visual sameness, since many competitors run the same Carrot theme with minimal customization.
4. **Comparison/aggregator content sites** (Houzeo, iBuyer.com, Anytime Estimate, and similar "best cash home buyer companies" ranking content) — these functionally gatekeep top-of-funnel search traffic for head terms; the client's realistic SEO win is hyper-local, long-tail, and situational content these aggregators do not (and structurally cannot, at national scale) cover in local depth.

**Table stakes:** a "how it works" 3-step process explanation, a no-obligation-offer statement, some testimonials, and at least a few city-specific landing pages. **Common differentiator gap (research-confirmed):** genuine niche/situational topical authority content, honest and specific cash-offer-vs-alternatives comparison content, and visible, non-generic proof of local presence (named principals, a local phone number rather than a call-center 800 number, real — not stock — property photos).

## 5. Positioning & Messaging Patterns

Proven, differentiated angles: "the local, honest alternative to the franchise buyer with a track record of lowballing"; "the buyer who takes the houses no one else will — fire damage, hoarder, tenant-occupied, condemned"; "see exactly how we calculate your cash offer" (transparency-led, directly countering the "lowball" objection common to every persona in Section 3); "we're a real local team, not a call center or an algorithm."

**Avoid** the generic "we buy houses fast for cash, no fees, no repairs" headline — this is, essentially verbatim, every competitor's homepage headline per the competitive research above, and provides zero differentiation.

**Flag for compliance, with unusual weight in this Module specifically:** any urgency-manufacturing framing around foreclosure, eviction, or financial distress must be reviewed for whether it *informs* a homeowner of their real timeline and options or *pressures* them — given this vertical's specific FTC/state-AG enforcement history (Section 2), this is not a stylistic nicety but the single highest compliance-risk category in the entire Module. "We pay full market value" and any comparative superiority claim against a named or implied competitor requires a substantiable basis before publication.

## 6. Information Architecture Patterns

Typical required page types, informed directly by Carrot's published site-structure guidance and the observed bluewavehomebuyers.com pattern: Home; How It Works; Our Company/About (with named principals); Reviews/Testimonials; FAQ; Compare (Cash Offer vs. Realtor vs. iBuyer); **City/service-area pages — one per target city or county** (Carrot's own research explicitly recommends granular city-level pages over a single statewide page, and this is the primary local-SEO structural pattern in this vertical); **Niche/situation pillar pages** — one per seller situation (Foreclosure, Probate/Inherited Property, Divorce, Tired Landlord, Fire/Water Damage, Hoarder House, Tax Liens, Vacant/Abandoned Property, Downsizing), each following a pillar-plus-supporting-cluster pattern per Carrot's own documented "Niche Topic Page" methodology; Blog/Resource library; required compliance pages (state equitable-interest/wholesaling disclosure page where applicable, Privacy Policy, Terms of Use, Accessibility Statement, and SMS/TCPA consent language attached to every lead-capture form rather than isolated to a single legal page).

## 7. SEO & Keyword Strategy

High-value topical clusters, directly evidenced by research: hyper-local commercial-intent terms ("sell my house fast [city]," "we buy houses [city]," "cash home buyers [city]") — research confirms generic national terms are dominated by Zillow/Realtor.com-scale sites, so local long-tail is where an independent investor actually wins; **niche/situational clusters** built pillar-plus-cluster per persona (foreclosure, probate, divorce, tired landlord, fire/water damage, hoarder house, tax liens) — Carrot's own content strategy explicitly recommends exactly one pillar page per niche topic, supported by long-tail cluster posts that link back to it, never competing with the city/location pages for the same keyword groups; and honest comparison content ("cash offer vs. realtor vs. iBuyer in [city]").

Recommended schema: `LocalBusiness` (schema.org has no dedicated "real estate investor" type; `LocalBusiness` with an accurate `areaServed` per city page is the pragmatic choice, occasionally paired with `RealEstateAgent`-adjacent properties where a data point genuinely fits), `FAQPage` for niche/situation pages, `Review`/`AggregateRating` (only where testimonials are genuinely sourced and verifiable — given this vertical's documented reputation-manipulation risk, never populate this schema from unverified or incentivized-without-disclosure reviews), `BreadcrumbList`.

**AI-search note:** situational FAQ content ("what happens if I inherit a house that's in foreclosure") is well-suited to citation by AI Overviews and conversational AI search, since it reads as genuinely informational rather than purely commercial — this is a meaningful reason to invest in the niche pillar pages beyond their direct-search value, consistent with Carrot's own emerging emphasis on AEO/GEO in this vertical.

**Claim-risk keyword patterns:** avoid "guaranteed highest offer" or "stop foreclosure guaranteed" as literal page targets; situational urgency terms (e.g., "stop foreclosure") should be paired with genuinely informational, non-coercive content per Section 5's compliance flag.

## 8. Trust Signal Requirements

"As-is, no repairs, no cleanout" claims paired with concrete, specific proof (real — not stock — photos of actual purchased distressed properties, with seller privacy respected). A clear, plain-language explanation of exactly how the cash offer is calculated (typically: after-repair value minus estimated repair costs minus the investor's required margin) — research indicates this single disclosure most directly counters the "lowball" distrust objection shared across every persona in Section 3, and is also the strongest defensive posture against predatory-practice scrutiny. Zero-fee/zero-commission statements stated specifically, and, in any comparison content, contrasted only against accurately sourced realtor-commission and iBuyer-service-fee figures. A **local address and a local phone number** (a national 800/call-center number is a documented trust red flag in this specific vertical). Named principals with real photos and a genuine local track record (years in business, number of homes purchased). Genuine, verifiable testimonials/reviews — a Google Business Profile embed or BBB accreditation (if actually held) rather than a page of unverifiable text quotes. An explicit "no upfront fees" statement, directly countering the foreclosure-rescue-scam pattern described in Section 2. The state-required equitable-interest/wholesaling disclosure, where applicable, displayed clearly and not buried in a footer link.

## 9. Content Model & Page Types

| Page Type | Required Content Elements |
|---|---|
| City/Service-Area Page | Local market context, the core 3-step process recap, a city-specific testimonial if genuinely available, local phone number, FAQ block, embedded cash-offer request form with SMS/TCPA consent language |
| Niche/Situation Pillar Page (e.g., Foreclosure, Probate, Divorce, Tired Landlord) | Plain-language explanation of the seller's actual situation and their real range of options — not only "sell to us" (briefly and honestly noting alternatives, e.g., forbearance/loan modification for a foreclosure page, before presenting the cash-sale option) — which both builds more genuine trust and is materially more defensible against predatory-practice scrutiny than a pitch-only page; supporting FAQ block; CTA |
| Compare Page (Cash Offer vs. Realtor vs. iBuyer) | Honest, accurately sourced side-by-side on fees, typical timeline, as-is/condition acceptance, and certainty of close — no fabricated or unsubstantiated competitor figures |
| How It Works Page | The full process in detail (typically: contact → property evaluation → cash offer within a stated timeframe → seller chooses closing date → close), what documents are needed, and what the earnest money/escrow handling actually looks like |
| Reviews/Testimonials Page | Genuinely sourced reviews only; aggregate rating schema populated only from a real, verifiable source |
| About/Our Company Page | Named principals with photos, years in business, local story, and any state-required broker/wholesaler license or disclosure information |
| Compliance Page(s) | State equitable-interest/wholesaling disclosure (where the client's state requires it), Privacy Policy, Terms of Use, Accessibility Statement, and TCPA/SMS consent language reference |

## 10. Stage Gate Injection Map

| Core Stage Gate | What This Module Supplies |
|---|---|
| SG1 Discovery | Persona Library (Sec. 3), Regulatory Landscape seed (Sec. 2) — including confirming the client's actual state wholesaling-disclosure obligations and whether their process is title-purchase or assignment-based |
| SG2 Competitive Intelligence | Competitive Landscape Notes (Sec. 4) — the four-archetype competitive set |
| SG3 Strategic Direction | Positioning & Messaging Patterns (Sec. 5), with the compliance flag on urgency/coercive framing given particular weight |
| SG4 Information Architecture | IA Patterns (Sec. 6) — city pages and niche/situation pillar pages as the two core structural pillars |
| SG5 SEO Blueprint | SEO & Keyword Strategy (Sec. 7) — hyper-local plus niche/situational cluster model |
| SG6 UX & Conversion | Trust Signal Requirements (Sec. 8); the cash-offer request form's SMS/TCPA consent language is a Module-specific, compliance-load-bearing UX element |
| SG7/7.5 Design | Trust Signal visual treatment (Sec. 8) — real photography over stock imagery, local-team presentation over faceless/corporate presentation |
| SG8/9 Content & Copy | Content Model (Sec. 9), full Regulatory Landscape (Sec. 2), and the Section 5 predatory-practice-language compliance flag applied with particular scrutiny to any foreclosure/distress-adjacent page |
| SG11 QA | Full Regulatory Landscape final checklist (Sec. 2) — state disclosure presence, TCPA consent language presence on every lead form, no unverified review/aggregate-rating schema |
| SG11.5 Growth | Persona validation (Sec. 3); niche/situation pillar expansion following the same pillar-plus-cluster discipline |

## 11. Module-Specific Prompt Library Additions

**Prompt CHB.1 — Predatory/Coercive Language Compliance Scan**

```
Review the attached page copy for [Client Name]'s cash home buyer
website. Given this vertical's documented FTC and state Attorney General
enforcement history against predatory practices targeting financially
distressed, elderly, and vulnerable homeowners, flag any language that:
(a) manufactures urgency or panic rather than informing the reader of
their actual timeline and options, (b) implies the offer is the seller's
only option without acknowledging real alternatives (forbearance, loan
modification, listing traditionally), (c) makes an unsubstantiated
superiority or "full market value" claim, or (d) could be read as
targeting a specific protected class or neighborhood under the Fair
Housing Act. For each flagged instance, suggest a more transparent,
informational alternative and route the finding to the Compliance/
Standards Liaison for final language approval — do not assert replacement
language as final yourself.
```

**Prompt CHB.2 — Niche/Situation Pillar Page Generation**

```
Generate a niche/situation pillar page for [Client Name]'s cash home
buyer website addressing the "[situation — e.g., Foreclosure / Probate /
Divorce / Tired Landlord]" persona. Structure: (1) a plain-language,
genuinely informational explanation of the situation and the homeowner's
realistic range of options — including at least one honest alternative
to selling to this client — before introducing the cash-sale option;
(2) how this client's process specifically fits this situation; (3) an
FAQ block suited to citation by AI-mediated search; (4) a CTA. Do not
fabricate statistics, timelines, or legal claims about the situation
(e.g., foreclosure timelines vary by state and by loan type) — flag any
factual claim needing verification rather than asserting it.
```

**Prompt CHB.3 — State Wholesaling Disclosure Applicability Check**

```
Given [Client Name]'s state(s) of operation and their transaction
structure (title-purchase vs. contract-assignment/wholesale), determine
whether a written equitable-interest/wholesaling disclosure is currently
required before contract execution, whether a specific format is
mandated (e.g., standalone document, minimum font size), and whether the
seller has a statutory rescission right if the disclosure is omitted.
Cite the specific current statute if known; otherwise flag this
explicitly for confirmation with the client's real estate counsel before
the Compliance Content Checklist (Development discipline, SG8) is
finalized — do not assert a state's requirement without a verifiable,
current source.
```

## 12. Module Version History

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-07-23 | Initial module authored via the New Module Development Process (Governance, Sec. 13.6), using the Real Estate Module as the structural starting point. Grounded in research on Carrot.com's published SEO/site-structure methodology, the live structure of bluewavehomebuyers.com, competitor archetypes (national franchise, iBuyer, local independent, aggregator), and current state wholesaling-disclosure, TCPA, and FTC/state-AG predatory-practice enforcement findings. Approved via Change Request CR-007. |

---

*This module extends the Industry Modules library for WEF v1.0. See [00-Module-Template-and-Index.md](00-Module-Template-and-Index.md) for the full library index.*
