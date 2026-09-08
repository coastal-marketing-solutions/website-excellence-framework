# Governance — 13. Governance Policies

*Core Methodology — Governance, Sec. 13. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 13. Governance Policies

### 13.1 Methodology Governance Board

A standing body (minimum 3 senior consultants) responsible for approving changes to the Core Methodology, approving new or revised Industry Modules, adjudicating disputes about Stage Gate exit criteria, and maintaining the default technology stack decision.

### 13.2 Change Proposal Process

1. Any team member may submit a Change Request against the Core Methodology or against a specific Industry Module.
2. The Governance Board reviews within 10 business days (Core changes) or 5 business days (Module changes, given their narrower blast radius).
3. Approved changes are logged in the Revision Log (Front Matter for Core; the Module's own front matter for Module changes) and released as a new version per Section 11.
4. Rejected changes are logged with rationale for future reference.

### 13.3 Engagement-Level Governance

Within a single engagement, the Engagement Lead holds equivalent authority to the Governance Board for engagement-specific interpretation questions, but may not override the Core Methodology's Stage Gate exit criteria, quality standards, default technology stack, or the active Industry Module's compliance requirements without Governance Board sign-off logged as a Decision Register entry tagged `GOVERNANCE-EXCEPTION`.

### 13.4 Default Technology Stack Policy

Unless the Project Charter specifies an alternative, this stack applies regardless of industry:

| Layer | Default |
|---|---|
| Hosting | Hostinger VPS |
| CMS | WordPress |
| Theme Framework | GeneratePress Premium |
| Page Building | GenerateBlocks Pro |
| Asset/Cloud Layer | GenerateCloud |
| SEO Plugin | Rank Math SEO |
| Caching | LiteSpeed Cache |
| CDN / Edge Security | Cloudflare |
| Analytics | Google Analytics 4 |
| Search Monitoring | Google Search Console |
| Tag Management | Google Tag Manager |
| Behavioral Analytics | Microsoft Clarity |
| Cookie Consent / Privacy Compliance | WPConsent (Cookie Banner & Consent Management) |

Any deviation must be documented in the Project Charter with rationale and logged as a Decision Register entry at initialization.

Cloudflare, Microsoft Clarity, and WPConsent are standing default-stack layers as of this revision — every engagement provisions all three unless the Charter documents an explicit exception (Sec. 13.4.1). This is not contingent on the active Industry Module flagging the vertical as regulated: WPConsent applies uniformly because any site collecting lead-form data may reach visitors in jurisdictions with cookie/consent requirements (GDPR, CCPA/CPRA, and similar), and Cloudflare/Clarity are baseline edge-security and behavioral-analytics layers independent of vertical.

### 13.4.1 Active Intake Confirmation (not a silent default)

This stack is a **starting recommendation**, not an assumption the client is deemed to have accepted by not objecting. At Project Initialization (Sec. 1.2, step 5), the Engagement Lead must walk the client through the stack **layer by layer** and obtain an explicit choice for each — "use the WEF default" is a valid, first-class answer, but it must be *selected*, not defaulted into. Record the confirmed choice for every layer (Hosting, CMS, Theme Framework, Page Building, SEO Plugin, Caching, CDN, Analytics, etc.) in the Charter's Technology Stack section, even where every answer is "WEF default." This closes the gap where a stack choice made mid-engagement (a hosting-tier change, a plugin swap) drifts from what the Charter says without anyone treating it as a decision worth logging (see Retrospective RETRO-003, Sec. 15.4). Any change to a previously confirmed layer, at any point in the engagement, is logged as a Decision Register entry at the moment it happens — not reconstructed later from what actually shipped.

**A second, distinct layer must also be confirmed at intake: Content & Code Access Tier** — *how* AI tools and consultants will actually push changes to this specific site, independent of which CMS/theme was chosen. This determines the mechanism Development (Sec. 06, SG10.5) uses for the Content-as-Files Sync Pipeline:

| Tier | Mechanism | Availability | Use For |
|---|---|---|---|
| **1 — Preferred** | SSH + WP-CLI (or the confirmed stack's CLI equivalent) | Requires the host to provide shell access — confirm per specific hosting plan/tier, never assumed. Not guaranteed on entry-level shared hosting even within the same host brand | Full content-as-files export/import, theme file deploy, cache/plugin management — the most reliable, scriptable, diffable path |
| **2 — Fallback** | Platform REST API with an application-level credential (e.g., WordPress Application Passwords) | Available on nearly every modern WP host over HTTPS alone, no shell required | Pushing page/post content and metadata from git-tracked files when Tier 1 is unavailable |
| **3 — Last Resort** | Browser/GUI automation of the platform's native editor | Always available, but the least reliable — see Governance, Sec. 15.4 (RETRO-005) for why this tier alone caused real drift and rework on this framework's first engagement | Only when Tiers 1–2 are both unavailable, or a change genuinely requires visual/WYSIWYG verification the other tiers can't provide |

Confirm and record the available tier(s) for the confirmed host at Project Initialization, the same as any other stack layer — this is not knowable in the abstract from "we use Hostinger," since access varies by specific plan. Default to the highest tier actually available; never default to Tier 3 by omission just because no one checked whether Tier 1 or 2 was possible.

### 13.4.2 Portability — the Default Stack Does Not Create Lock-In

Recommending GeneratePress/GenerateBlocks as the default (Sec. 13.4) is a starting-point convenience, not a commitment that locks every future engagement to this theme framework. The durable, reusable asset this methodology builds is the **Component Library**'s token system and component interfaces (`/Component-Library/`, Design Sec. 9.5) — colors, spacing, typography scales, and component contracts (props/variants/behavior), all defined independent of any theme. GeneratePress Global Styles and GenerateBlocks patterns are **one implementation of those tokens**, not the tokens themselves. Each Component Library entry's "Platform Implementation Note" field is explicitly designed to hold more than one stack's implementation over time — a GeneratePress note today does not preclude adding a Shopify, Webflow, or custom-PHP/HTML implementation note for the same component later, once an engagement actually builds one. Switching a future engagement to a different theme or stack means writing a new Platform Implementation Note against the existing token/interface spec — it does not mean redesigning the Component Library or the Design Constraints Package's token layer from scratch. This is the same portability discipline Sec. 13.4.1's Content & Code Access Tier and Development's Sec. 10.5-Alt (WordPress Implementation Blueprint) already assume — the default stack is a recommendation with a documented off-ramp, not a dependency.

### 13.4.3 Maximize a Selected Plugin's Advanced/Licensed Capabilities — Once Chosen, Use It Fully

The Default Technology Stack (Sec. 13.4) and the standing "native functionality preferred, plugin dependencies minimized" discipline remain the baseline: don't add a plugin to solve something native WordPress/GeneratePress/GenerateBlocks already does cleanly. But once a plugin has cleared that bar and been licensed as part of the confirmed stack — GeneratePress Premium, GenerateBlocks Pro, Rank Math (SEO Plugin default, Sec. 13.4), or any Charter-approved alternative — the engagement should use that plugin's advanced/paid-tier capabilities as fully as its stated goals allow, not just the minimum feature needed for the immediate task. The licensing cost is already sunk once the plugin is selected; configuring it at half-capacity leaves paid value on the table and produces a shallower implementation than what's actually available.

This mirrors the precedent already set for GeneratePress: engagements are expected to explore GeneratePress Premium's advanced modules (Elements, Hooks, Sections, etc.) rather than hand-building custom equivalents in a child theme when the licensed module already covers it, and to document which specific advanced features were actually exercised so the pattern is reusable on the next GeneratePress engagement rather than re-discovered from scratch each time. The same discipline now applies explicitly to Rank Math and to any future default-stack plugin:

- **Before configuring a plugin's basic settings, check whether a licensed advanced/PRO tier is already active** (Plugins → Installed Plugins shows this directly) and consult its documented feature set before assuming only the free-tier feature set is available — free-tier assumptions made without checking are a real, observed failure mode, not a hypothetical one.
- **Treat installation, activation, subscription entitlement, account connection, and site/property assignment as five separate states.** A premium add-on can be installed and active while the base plugin is connected to a free account or while the paid subscription is assigned to a different site. Verify the subscription in the vendor account, the exact connected account in the site, the site's license badge/assignment in the vendor portal, and the premium update channel. The plugin name or presence of premium menu items is not entitlement evidence.
- **Prefer the plugin's native advanced feature over a custom-code equivalent** when both exist and the plugin's advanced tier is already licensed — e.g., a PRO-tier Schema Templates feature over a hand-rolled JSON-LD block, a plugin's native Search Console/Analytics integration over a separate reporting dashboard, a plugin's built-in content/SEO analyzer over a manual audit pass — once the client has confirmed the feature is wanted and it doesn't route around Sec. 13.5's compliance gate.
- **Document which advanced features were actually turned on and why** in the engagement's Decision Register, the same discipline already required for the base plugin choice — this is what makes the usage pattern reusable across future engagements rather than a one-off. A brief "Advanced Features Enabled" note, cross-referenced from the plugin's stack-selection Decision Register entry, is sufficient; it does not need its own Stage Gate document.
- **This does not relax Sec. 13.5 (Compliance & Professional Standards Governance).** An advanced feature that changes what's published live — AI-generated schema/content suggestions, auto-populated business data, bulk title/description rewrites — still requires the same compliance review any other published content requires before going live.

Applies at Governance Board level to the Default Technology Stack (Sec. 13.4) and at Engagement Lead level to any Charter-approved alternative plugin — the principle is "use what's already been paid for, fully, and record what was used," not a mandate to enable every feature regardless of relevance to the engagement.

**Capability Ownership takes precedence over capability maximization.** “Use it fully” means use all relevant, non-conflicting value—not activate every available writer. A licensed feature may operate in read-only, monitor-only, or reporting mode, or remain disabled, when another approved system owns the production output. The Capability Ownership Matrix (Sec. 13.4.4) records that boundary.

### 13.4.4 Capability Ownership, Collision Prevention, and Tool Portability

Using a selected tool fully does not mean allowing multiple tools to publish the same output. Every engagement must maintain a **Capability Ownership Matrix** in the Plugin & Integration Configuration Record. For each externally visible or data-bearing capability, name exactly one production owner, any monitor-only consumers, the fallback behavior if the owner is disabled, and the export/migration path.

At minimum, assign ownership for: page titles and meta descriptions; canonical URLs; XML sitemaps; robots directives; structured data; redirects; translations and `hreflang`; analytics/tag injection; consent management; forms and lead storage; caching/minification; image optimization; and security/firewall rules. A theme fallback may remain available only when it is programmatically suppressed while the designated plugin is active and has been verified not to emit duplicate output.

The following rules are binding:

- **One writer, many readers.** Reporting tools may read the same Search Console, analytics, or SEO data, but only one configured owner may write each class of metadata, schema, tag, redirect, translation, or optimization output.
- **Rendered output is the truth.** An admin-screen setting is not proof. Verify the public HTML, headers, network requests, cookies, sitemap, and structured-data graph after a fresh uncached load.
- **No overlapping plugins by convenience.** Do not run two SEO, translation, analytics-injection, schema, redirect, consent, cache, or form systems with overlapping production responsibility unless a documented boundary makes their outputs mutually exclusive.
- **Fallbacks require a failure test.** If custom code or a theme supplies a fallback when a plugin is inactive, test both states and confirm there is exactly one output in each state.
- **Portability is documented before dependency.** Record where the tool stores its data, what survives deactivation, how to export it, what licensed features cease to function, and the replacement path. Never let a proprietary score or dashboard become the only record of page strategy.
- **Client/account isolation is explicit.** Connected properties, credentials, API keys, and destination accounts are verified per site; shared agency accounts never justify assuming the current property is correct.

Any collision discovered after launch is treated as a production defect, not a cosmetic configuration preference, and is entered in the Issue Log with the affected URLs and generated outputs.

### 13.4.5 Access, Credential, and Environment Boundary

Every engagement must distinguish **who owns a system**, **who operates it**, and **how a tool is authorized to reach it**. The Digital Estate & Access Map records the provider, property/site identifier, business owner, operational custodian, access status, environment (local, staging, production), recovery path, and next action; it never stores passwords, API tokens, application-password values, recovery codes, private keys, or session cookies.

The following controls apply across every stack and industry:

- Use the least-privileged account that can complete the task. Prefer a named client or service account with a scoped role over a shared administrator login.
- Record whether access is reported, verified, expired, or revoked. “The client said it works” is not the same as a verified connection to the correct property, repository, domain, analytics view, CRM, or production site.
- Separate local/development, staging, and production credentials and destinations. A staging credential must not silently point at production, and a production deploy must not target a broad document root unless that exact scope is approved and backed up.
- Store secrets only in the approved credential manager. Never paste them into chat, prompts, source files, XML/CSV imports, screenshots, issue logs, or commit messages. When a temporary application password or token is used, record its purpose and revocation owner—not its value—and revoke it when the task or engagement requires.
- Before an AI tool or browser session makes a state-changing edit, verify the visible domain/property and the intended environment. After the edit, verify persistence from a fresh read path; an in-session success message or stale DOM is not sufficient.
- Before irreversible or bulk production work, verify a recoverable backup/export, define the rollback trigger, and perform a small reversible smoke test. If the access boundary or destination cannot be verified, stop the state-changing action and escalate it as a P0/P1 risk rather than guessing.

This is an operational control, not a request to expose credentials to the consulting team. The goal is auditable authorization and correct targeting while keeping secrets out of the framework and engagement records.

### 13.4.6 Third-Party Custom Domains, Origin Boundaries, and Access Control

A custom domain connected to a hosted application is a routing layer, not proof that the application is hosted in the DNS provider's account or protected by that provider's directory controls. Before connecting any portal, studio, dashboard, booking app, knowledge base, or other third-party service to a client subdomain, document the full request path: registrar → authoritative DNS → edge/proxy → hosted application/origin → identity provider. Name which layer terminates TLS, which layer enforces authentication, and which URLs can reach the same application.

The following controls are binding:

- **Confirm authoritative DNS and record compatibility before cutover.** A hosting-panel “create subdomain” action may create an A, AAAA, ALIAS, or local document root that conflicts with the CNAME or verification record required by the hosted service. Inventory and resolve conflicts deliberately; do not stack records until one happens to work.
- **Preserve a tested fallback until DNS and TLS are verified.** Keep the provider URL available during cutover unless the security model requires otherwise, record TTL and validation records, and define rollback before changing the public hostname.
- **Apply access control at a layer every route actually traverses.** Host-level directory password protection cannot protect a CNAME that routes directly to an external SaaS origin. Use the application's identity controls or a verified edge/access layer in front of the application.
- **Test alternate-route bypass.** If the provider's original hostname, preview URL, deployment URL, or another custom hostname remains reachable, verify that it enforces equivalent authorization or intentionally document it as public. Protecting only the vanity hostname is not effective access control.
- **Verify cookie, callback, canonical, and redirect behavior on the final hostname.** Authentication callbacks, cross-site cookies, CSP/CORS, canonical URLs, analytics properties, and logout/return URLs must use the intended production domain without loops or leakage to another client property.

Record the cutover and bypass test in the Third-Party Custom Domain & Access-Control Record (Reusable Templates, Sec. 15.7). A DNS “success” badge alone is not acceptance evidence.

### 13.5 Compliance & Professional Standards Governance

WEF consultants and AI models never issue final compliance, legal, medical, or financial sign-off in any industry. Every piece of content touching claims, disclosures, licensing statements, or advertising language subject to the active Industry Module's Regulatory & Compliance Landscape must pass through the client's named Compliance/Standards Liaison before publication, formalized as a mandatory review step in Development (Stage Gates 8–9) and QA & Optimization (Stage Gate 11).

**Approval is bound to a defined artifact and revision, not to a topic, page family, campaign, or website forever.** Every clearance entry must identify the exact page/record, language, version or content hash/date, approval scope, approver, and decision. Later pages, translations, videos, posts, material claim changes, changed disclosures, new data, or substantive revisions do not inherit an earlier blanket approval unless the approver explicitly names that future scope. Define which edits are non-substantive (for example typo correction without meaning change) and which invalidate clearance. When in doubt, return the changed artifact for review; never infer that “the site was approved” clears advertising content created afterward.

**Fact-verification and publish-authorization are two separate, sequentially-required approvals for any sensitive identifying information** (a physical office address, a license-linked location, a practitioner's personal details, or comparable) — confirming that a piece of information is *accurate* is a factual question; deciding whether the client wants it *displayed publicly* is a distinct business/risk decision only the client can make. Log each as its own Decision Register entry. Do not treat a verified fact as cleared for publication until the second, separate approval is logged, and do not needlessly withhold a fact whose accuracy is already confirmed once that second approval is obtained (RETRO-015, Sec. 15.4).

**When an approver's response to a clearance log does not explicitly address items the log itself named as requiring the approver's specific confirmation, ask directly which scope was intended before logging clearance status.** A short, real-world approval reply (e.g., "move forward") is frequently more ambiguous than the log's own itemization, and silently treating it as resolving every previously-named open item risks closing out compliance flags that were never individually checked. The resulting Decision Register entry must record both the approval actually granted and, by name, which specifically-flagged items were not demonstrably individually verified, so a later audit or QA pass does not mistake a granted blanket clearance for itemized confirmation it never received (RETRO-016, Sec. 15.4).

### 13.6 New Module Development Process

When an engagement requires an industry not yet covered by an existing Industry Module:

1. Engagement Lead identifies the closest existing module as a structural starting point.
2. A draft module is authored to the fixed Module Template (Industry Modules front matter) — Persona Library, Regulatory & Compliance Landscape, Competitive Landscape Notes, Positioning & Messaging Patterns, Information Architecture Patterns, SEO & Keyword Strategy, Trust Signal Requirements, Content Model & Page Types, Stage Gate Injection Map, Module-Specific Prompt Library Additions.
3. The draft is used on the current engagement in parallel with active development, clearly marked "Draft — v0.x" in the Knowledge Base and Decision Register.
4. At engagement close, the module is finalized, submitted to the Methodology Governance Board as a Change Request, and — once approved — added to the permanent Industry Modules library at v1.0 for reuse on future engagements in that vertical.

### 13.7 Module Currency Review

Because regulatory and professional-standards requirements change over time (and faster in some industries — e.g., mortgage lending, medical/healthcare, financial advisory — than others), every Industry Module's Regulatory & Compliance Landscape section is reviewed at minimum annually, and immediately upon any team member flagging a known regulatory change, regardless of the semiannual Core Methodology review cycle.

### 13.8 Candidate Structural Extensions — Flagged, Not Adopted

Two structural ideas surfaced from external sources (a live engagement's evolved governance and an independently designed AI-driven agency's own team structure) are documented here deliberately as **candidates requiring a real decision, not silently adopted rules** — consistent with the discipline in Sec. 13.6/9.5 that a genuine structural change gets evaluated on its own merits, not folded in because it appeared somewhere plausible-sounding:

- **Pre-execution doctrine audit.** Every review mechanism currently in this framework (the Stage Gate Review Process, the Four-Question Review Standard referenced from prior engagement evidence, Stage Gate 11 QA) runs *after* a deliverable is produced. A pre-execution check — auditing a plan or draft against the Charter/Design Constraints/Compliance Constraint Log *before* work is executed, not only reviewing the finished output — could catch a doctrine violation before time is spent producing something that fails review anyway. Whether this becomes a formal, separately staffed checkpoint or stays an informal habit of the existing Engagement Lead/AI Orchestrator roles is an open question, not a default answer.
- **A formal "New Role Development Process," parallel to Sec. 13.6's New Module Development Process.** As specialist role-splitting deepens (see the Consulting Organization's optional Knowledge Librarian addition above, and the broader pattern of one generalist role splitting into several deep specialists as an engagement scales), a standing process for proposing, trialing, and promoting a new specialist role — rather than each engagement inventing its own role list ad hoc — has real appeal. It also has a real cost: more named roles means more coordination overhead for a small engagement. Do not adopt a larger role roster than a given engagement's scale actually warrants (Sec. 2.1's existing consolidation guidance still governs) without a specific decision that the added rigor is worth it for that engagement.
