# WEF Analytics Gap Review — 2026-10-05

**Status:** Review / proposal input. **Not canon.** Each gap below is a candidate for a follow-on Change
Request (suggested bundle: **CR-035 — Measurement Configuration & Lead Attribution**) once CR-034
(Bing/IndexNow + Moz) is decided.
**Method:**
1. Searched `WEF-v1.0/` and `.agents/` for each topic in a complete web-measurement program.
2. Read what exists today: Reusable Templates Sec. 3 "Meaningful-Action Measurement Plan", the
   Search Visibility Operations Plan (Sec. 7.4), Development's Integration Requirements Spec,
   SG11.5's KPI Dashboard Spec.
3. Checked one live engagement (real estate, 2026-10-05) for the failure each gap would cause.

## What the framework already does well

- **Measurement plan.** Reusable Templates Sec. 3 has the measurement-plan table (event, business
  meaning, trigger, no-PII parameters, consent category, debug test, owner).
- **Ownership and cadence.** Governance Sec. 13.4.4 has "one writer, many readers" and
  "rendered output is the truth". Reusable Templates Sec. 6 has a weekly/monthly/quarterly cadence.
- **Instrumentation is required.** GA4/GSC/GTM/Clarity/WPConsent must fire and be consent-gated
  before SG10.5 exits.
- **Reporting rules.** "Plugin scores are diagnostics, never outcome KPIs."

The gaps are about **configuring GA4 properly, tying leads back to their source, verifying tracking
works, and newer channels**, not about whether analytics exists.

## Coverage search (hits across `WEF-v1.0/` + `.agents/`)

| Topic | Hits | Topic | Hits |
|---|---|---|---|
| key event | 0 | DebugView | 0 |
| Consent Mode | 0 | logged-in / internal traffic | 0 |
| UTM | 0 | event taxonomy / data layer | 0 |
| gclid / click ID | 0 | offline conversion import | 0 |
| cross-domain | 0 | Looker Studio | 0 |
| call tracking | 0 | AI referral (ChatGPT/Perplexity) tracking | 0 |
| data retention (GA4) | 0 (1 hit is a CRM retention field) | CrUX / field data | 1 |

## Gaps, ranked by impact

### G-1 — No GA4 property-configuration checklist (High)
SG10.5 checks that GA4 *fires*. Nothing requires the property to be *configured*:
- **Key events marked.** On the live engagement, `generate_lead` was marked weeks after forms
  went live.
- **Event data retention** raised from the 2-month default to 14 months. Without this, Explorations
  can't look back past 60 days.
- **Search Console linked to GA4.** On the live engagement it was not linked, although Site Kit was
  connected to both, so there were no "Organic Search Queries" reports.
- **Internal-traffic and developer-traffic filters.**
- **Unwanted-referral list:** payment, booking and CRM domains.
- **Enhanced Measurement audited** against the custom events, to avoid double-counting form
  submits and downloads.
- **Reporting identity** chosen.

**Proposal:** a "GA4 Property Configuration" checklist block in Development Sec. 11, plus a
matching row group in the Integration Requirements Spec.

### G-2 — Leads aren't attributed back to their traffic source (High)
Forms post to the CRM, but nothing requires capturing **where the lead came from**: UTM
source/medium/campaign, gclid/gbraid/wbraid, landing page, first referrer. CRM records then can't
report "which channel produced qualified leads". The live engagement's bridge sent only "Submitted
from: [page URL]".

**Proposal:**
- Every lead form gets hidden fields filled from first-touch/last-touch cookies.
- The form-to-CRM hand-off maps them to CRM contact fields.
- The KPI Dashboard reports leads by channel from the CRM, not just GA4 event counts.

### G-3 — Lead quality isn't fed back to analytics (High for anyone running paid ads)
GA4 counts form submits, but the business outcome is a *qualified* lead or a closed deal, and that
happens in the CRM. There's no requirement to send CRM stage changes (Qualified, Won) back to GA4
via Measurement Protocol, or to Google Ads as offline conversions.

**Proposal:** an optional SG11.5 item. When a CRM with pipeline stages exists, define
`qualify_lead` / `close_convert_lead` events sent server-side from the CRM's webhook, keyed by the
captured click ID or GA client ID. The live property already has `qualify_lead` and
`close_convert_lead` in its key-event list, unused.

### G-4 — Conversion surfaces on third-party domains go unmeasured (High)
Booking pages, checkout, chat and scheduling tools often run on the vendor's domain. On the live
engagement, the booking page lives on the CRM's domain. **A booked call, the highest-intent action,
is invisible to GA4.**

**Proposal:** the Integration Requirements Spec must list every off-domain conversion surface and
choose one of:
- (a) GA4 cross-domain measurement, if the vendor allows the site's tag;
- (b) a vendor webhook to Measurement Protocol (`generate_lead`, `lead_type: booking`);
- (c) a thank-you redirect back to the site that fires the event.

Plus an "unwanted referral" entry for the vendor domain.

### G-5 — No tracking-verification protocol that accounts for exclusions (Medium-High)
"Verified firing" doesn't say *how*. Site Kit (and most plugins) exclude logged-in users, so an
admin's test submissions never reach GA4. On the live engagement both labelled tests ran while
logged in, and a second, unexplained GA ID loaded only for logged-in admins.

**Proposal:** verification = a logged-out or private-window test, plus GA4 **DebugView** or
Realtime, plus a tag inventory in both states, recorded in the measurement plan's "Debug Test"
column.

### G-6 — Consent Mode not specified (Medium-High; High for EU/UK/CA audiences or Google Ads)
WPConsent is mandatory, but **Google Consent Mode v2** (`ad_storage`, `analytics_storage`,
`ad_user_data`, `ad_personalization`) isn't mentioned. Without it, consent-denied visits are lost
rather than modeled, and Google Ads remarketing and conversion features are limited for EEA traffic.

**Proposal:** require the consent tool to emit Consent Mode v2 signals (WPConsent supports this),
with defaults and regional behavior recorded, and verified in Tag Assistant.

### G-7 — No standard event taxonomy or data layer (Medium)
The measurement-plan table is blank by design, so every engagement invents its own event names. The
live engagement produced a good one (`generate_lead`, `contact` for tel:/mailto:, `select_content`,
`tool_start`/`tool_complete`, standard parameters `lead_type`, `form_id`, `page_type`,
`service_interest`, `cta_location`, plus a `dataLayer` contract).

**Proposal:** promote a default taxonomy built on GA4 recommended events, with parameter
conventions and a vendor-adapter rule (form/booking callbacks translate to the neutral contract),
into Reusable Templates Sec. 3.

### G-8 — Phone calls under-measured (Medium; High for local-service verticals)
Many verticals (real estate, home services, legal, medical) convert by phone. At minimum, `tel:`
clicks should be a tracked event. Optionally, call tracking with dynamic number insertion,
**gated on NAP consistency**: the tracked number must never replace the canonical NAP number in
schema, the footer or citations.

**Proposal:** a Module Injection Point in the measurement plan. Each Industry Module states whether
call tracking is expected.

### G-9 — AI-search referrals not segmented (Medium, growing)
WEF has GEO/AI-visibility work (Perplexity, ChatGPT, Copilot appear in Research/SEO), but no way to
**measure** traffic from them.

**Proposal:** a GA4 custom channel group "AI Assistants" (regex on referrers such as chatgpt.com,
perplexity.ai, copilot.microsoft.com, gemini.google.com, claude.ai), set up at SG10.5 and reported
in the KPI Dashboard. This pairs with CR-034's Bing/IndexNow layer.

### G-10 — No default dashboard tool or annotation habit (Medium)
SG11.5 requires a "KPI Dashboard Specification" but names no tool. GA4 annotations (now native)
aren't required when releases ship.

**Proposal:**
- Default to **Looker Studio** (free), combining GA4 + Search Console + the CRM lead export.
- Require a GA4 annotation for every content release, migration or tracking change, so the
  change log and the data line up.

### G-11 — Google Business Profile not measured (Medium; High for local verticals)
GBP is often the top local entry point. Nothing requires UTM-tagging the GBP website link
(`utm_source=google&utm_medium=organic&utm_campaign=gbp`) or linking GBP to GA4 / reviewing GBP
Performance.

**Proposal:** a Local-SEO Module Injection Point in the measurement plan.

### G-12 — Email and CRM links untagged (Low-Medium)
CRM nurture emails link back to the site without UTMs, so return visits show as "direct".

**Proposal:** a rule that every automated email link carries `utm_source=crm&utm_medium=email&utm_campaign=[workflow]`.

### G-13 — Field performance and form-health monitoring (Low-Medium)
- **Core Web Vitals field data** (CrUX via Search Console / PageSpeed) appears once. Low-traffic
  sites have no CrUX data, so lab tests then need to be labelled as lab.
- **No scheduled end-to-end form test** (form → CRM → automation), though the weekly cadence
  mentions "conversion-event health". On the live engagement, the CRM API silently skipped tags and
  stage until checked by hand.

**Proposal:** a weekly synthetic lead test (labelled, logged-out) plus uptime monitoring, in
Reusable Templates Sec. 6's weekly cadence.

## Suggested CR packaging

| CR | Contents | Core or Module |
|---|---|---|
| CR-035 Measurement Configuration & Verification | G-1, G-5, G-6, G-7, G-13 | Core (Development SG10.5, Reusable Templates Sec. 3/6, Governance 13.4.4) |
| CR-036 Lead Attribution & Closed-Loop Reporting | G-2, G-3, G-4, G-10, G-12 | Core (SG10 Integration Requirements Spec, SG11.5) |
| CR-037 Channel Measurement | G-8, G-9, G-11 | Core hook + Industry Module injection points (call tracking, GBP) |

## Apply-now list for the originating engagement (not framework changes)
1. **Link Search Console to GA4.** GA4 is showing that exact recommendation.
2. **Check event data retention** and set it to 14 months.
3. **Add an internal-traffic filter** and the CRM/booking domain to unwanted referrals.
4. **Track bookings** from the CRM's booking page (webhook → Measurement Protocol, or redirect to a
   site thank-you page).
5. **Add hidden source fields** (UTM/gclid/landing page) to forms 1/3/4 and map them in the bridge.
6. **Add an "AI Assistants" custom channel group.**
7. **Add UTMs** to CRM email links and the GBP website link.
8. **Add a `contact` event** for tel:/mailto: clicks. Its own measurement plan defines it, but only `nhb_listings_click` and `generate_lead` are actually implemented (checked in the child-theme `functions.php`).
