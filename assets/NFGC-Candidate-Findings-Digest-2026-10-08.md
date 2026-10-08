# NFGC Candidate Findings Digest — input for the next CR (unnumbered draft)

> **Draft, not canon. No CR number is claimed.** CR-033 through CR-037 are already in flight on other branches (`wef-cr-033-stage-transition-check`, `wef-cr-034-search-authority-tracking`, `wef-cr-035-037-measurement`), and per `WEF-Multi-Context-Reconciliation-Protocol.md` the single integrator assigns numbers. This file packages the candidate findings (17 log rows, grouped below into 19 items) from the first WEF-retrofitted site (`nfgc-website`, nationwidefgc.com) so they can be merged into whichever CR the integrator chooses. Source of record: `nfgc-website/_config/WEF-Candidate-Findings.md` (commit `9c1c8a4` on `main`, 2026-10-08). Written at the owner's request (action items sheet item `process__framework`: "draft it, no merge").
>
> Evidence level: every finding below was observed on a real engagement. Nothing here has been reviewed by the Methodology Governance Board.

## A. Deployment and version control (Governance Sec. 5 / 11; Development Sec. 10.5; `kb-conformance` NFGC mode)

| # | Finding | Evidence | Proposed rule text |
|---|---|---|---|
| A1 | **A repo whose root deploys must never also carry the KB.** NFGC's repo root is the WordPress child theme and the host auto-deploys `main`; adding the KB made every KB file a file in the live theme folder (publicly readable, owner-verified). | 2026-10-06: Hostinger deployed commit `10f6cceb` containing the KB; owner's check showed a KB file served as text. | "If the repo root is deployed, keep KB files on a branch that does not deploy, or deploy from a dedicated `deploy` branch containing only the code. Document which in `_build/README.md`." |
| A2 | **Verify the host's deploy branch in the host panel before merging to a deploying branch.** The merge followed the owner's statement that the host had been switched; the panel still showed `main`. | Same incident. | "Before any merge to a branch that auto-deploys, read the host's Git settings (or latest deployment record) and quote the branch in the PR. The owner's word is not the check." |
| A3 | **A `deploy` branch may be an orphan commit of the code-only files.** GitHub rejected a branch sharing history with `main` because of email-privacy rules on old commit authors. | `git push` declined; an orphan commit was accepted. | Allow the pattern; release procedure = `git checkout deploy && git checkout main -- <code paths> && git commit && git push`. |
| A4 | **Code that never reached git is lost on rollback.** The D-057 rollback wiped the contact form and CSS rules that existed only on the live server. | `style.css`/`functions.php` comments D-057, D-064/D-066; commits `a3724b6`, `6be6e8a`. | "Nothing ships without being committed first; syncing live → git is incident response, not workflow." |
| A5 | **One-shot admin scripts must expire and carry no secrets.** Four were pushed to an auto-deploying branch; three were removed, one stayed with a hardcoded trigger token. | `inc/prog-rankmath-tune.php` (removed 2026-10-08, `BL-002`). | "A one-shot needs a nonce trigger, an expiry and a removal commit scheduled the same day (a Backlog row)." |

## B. Build and QA rules (Development Sec. 10 / 10.5; QA Optimization Sec. 11)

| # | Finding | Evidence | Proposed rule text |
|---|---|---|---|
| B1 | **A global title-suppression filter plus a content-swap renderer can remove every H1.** Section 6 hid the theme title on all pages; Section 21 replaced the body of 82+ pages with a renderer that emitted no H1. | 36 of 36 crawled area pages and the hub had zero `<h1>`; fixed by emitting it in the renderer (commit `b900ed3`). | "Any template that replaces page content must own the H1. SG11: verify exactly one H1 per template in rendered HTML." |
| B2 | **No hardcoded page IDs in schema or behavior code.** | Section 17 allowlists 14 post IDs; `/llms.txt` code lists more. | "Use slug, meta or taxonomy rules; IDs differ per environment." |
| B3 | **Every sitemap URL must return 200 without a redirect.** | `/es/` listed in the sitemap but 301s to `/`. | Add to the SG5 sitemap build and SG11 link QA. |
| B4 | **Consent ownership collision (second instance).** | Theme cookie banner, WPConsent plugin banner and Site Kit consent mode all present; Site Kit also emitted AdSense tags. | "Assign one owner per capability in the Plugin-Config-Record; test banner count in a fresh browser after every plugin update." |
| B5 | **llms.txt takeover pattern.** | Rank Math's generated file was `noindex`, mis-ordered and tagline-described; replaced by a curated 200 response and `/llms-full.txt` (Section 22). | Entity-AI-Search-Brief checklist item; candidate snippet. |
| B6 | **Test the lead path end to end, including email authentication.** | Forms use `wp_mail` from the web server; SPF authorizes only Google; DMARC `p=quarantine` strict; no submission stored. | "SG11: submit each form (owner-initiated), confirm inbox delivery and a stored copy; check SPF/DKIM/DMARC alignment for the sending path." |

## C. Mortgage Lending Module (`Module-Mortgage-Lending.md`)

| # | Finding | Proposed addition |
|---|---|---|
| C1 | **Compliance-block pattern library** (Compliance Footer, CA-only statement, Non-QM business-purpose + nationwide, Eligibility Plug, inline disclaimer, Trust Bar, Dual CTA) shipped as block patterns. | Component Library entries under Marketing & Trust. |
| C2 | **Two-line lender: state-licensed consumer + nationwide business-purpose; California broker with a DRE corporate license.** The Module assumes NMLS only. | Sec. 2/5/8: show DRE license and broker-of-record numbers; split consumer vs business-purpose claims by state; "verify the licensed-state list" as a named step (NFGC owner states all 50 states, unverified: `BL-053`). |
| C3 | **Annual loan-limit refresh** drives ~100 pages from a code map. | Sec. 9 content model + SG11.5 operations: name an owner and a January trigger. |

## D. Method and tooling (Research Evidence Standard; `kb-conformance`)

| # | Finding | Proposed change |
|---|---|---|
| D1 | **Summarizing fetch tools mis-count.** The sitemap re-count gave 115; the tool said 120 and 87. | Evidence Standard: counts and URL lists come from raw files. |
| D2 | **External crawls of a production site must be throttled.** 1 req/s drew Cloudflare 429; 1 per 12 s still drew 429 every ~15 pages. | Prefer Search Console / owner exports; add "do not crawl faster than X; check the edge rate rules" to research and QA prompts. |
| D3 | **Retroactive KB reconstruction works without the original documents** when every file says *observed ≠ approved*, unknowns are PENDING, and a `DEC-KB` waiver covers gaps. 56 required documents and 0 checker errors were reached on a site with no surviving KB. | Keep the "source priority" and header text as the standard NFGC recipe. |
| D4 | **`check.py` rejects `SG7.5-Exit-Approval-Summary.md`** (dot in the gate name fails the Title-Case regex). | Allow `SG7.5` / `SG10.5` / `SG11.5` in the exit-summary pattern. |
| D5 | **Owner questions as a db-backed "action items sheet"** (items in a database, one owner-written answers document, a "process my answers" prompt). 48 questions, 40 answered in one pass, decisions logged by item id. | Adopt as the standard home for owner questions; handoffs point to it. |

## Suggested path
1. Integrator assigns a CR number (or splits: A1–A5 and B1–B6 → Development/QA CR; C1–C3 → Module CR; D1–D5 → Method/tooling CR).
2. Resolve overlaps with `CR-033-DRAFT-Engagement-KB-Conformance.md` (A1–A3 and D3–D4 extend its NFGC mode) and with the in-flight CR-034..037 branches before editing canon.
3. Board review as usual; this digest changes no canon by itself.
