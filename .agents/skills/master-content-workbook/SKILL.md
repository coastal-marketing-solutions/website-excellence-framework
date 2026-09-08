---
name: master-content-workbook
description: Build, enrich, and finalise the single `{ClientName}_Master_Content_Workbook.xlsx` for a WEF engagement — one spreadsheet consolidating the Content Plan, per-category page detail, Keyword Map, Local SEO Keyword Bank, Compliance Checklist, and (at SG9) Blog/Vlog/YouTube modules, so a non-technical stakeholder can review the whole content plan without opening the Knowledge Base's markdown. Runs in three modes matched to the gate: SKELETON (SG5), ENRICH (SG8), FINALISE (SG9). Use when the user says "build the content workbook," "update the master content workbook," "workbook for SG5/SG8/SG9," or reaches one of those gates. The workbook is built once and extended in place — never regenerated from scratch.
---

# Master Content Workbook (SG5 / SG8 / SG9)

One file, `{ClientName}_Master_Content_Workbook.xlsx`, at the Knowledge Base root. It is a
**derived view** — every value in it already exists in a gate's markdown output; the workbook
just consolidates it into one reviewable place (Reusable Templates Sec. 8.4). It is built at SG5
and **extended in place** at SG8 and SG9. Never regenerate it: a rebuild silently drops any
hand-correction a stakeholder made in the sheet.

Spreadsheet mechanics — creating sheets, Excel Tables, data-validation dropdowns, number
formats, freezing panes, the reopen-once check — are the **`xlsx` skill's** job. This skill
decides *what goes in* and *from which artifact*; call the `xlsx` skill for *how*.

Read as needed, don't front-load: `../WEF-v1.0/Core-Methodology/09-Reusable-Templates.md`
Sec. 8.4 (this workbook's canonical definition), Sec. 21.4 (KB naming convention);
`../WEF-v1.0/Core-Methodology/03-SEO-Architecture.md` Sec. 5 (SG5 Required Documents) and
`../WEF-v1.0/Core-Methodology/06-Development.md` Sec. 5 at SG8 and SG9. The active Industry
Module's **Regulatory & Compliance Landscape** and **SEO & Keyword Strategy** sections seed two
of the sheets — load them from the module named in the Project Charter.

## Step 0 — Locate the KB and pick the mode

1. Find the engagement KB: the `{Client} Website Blueprint/` folder for this engagement. If the
   user hasn't named it, ask. The workbook lives at its root as
   `{ClientName}_Master_Content_Workbook.xlsx` (ClientName in the KB's existing convention —
   match the Charter, no spaces if the other KB filenames have none).
2. Pick the mode from the gate:
   - **SKELETON** — SG5 (SEO Blueprint) just closed or is closing; no workbook exists yet.
   - **ENRICH** — SG8 (Content Specification) is closing; workbook exists in skeleton state.
   - **FINALISE** — SG9 (Copywriting) is closing; workbook exists enriched.
   If a workbook already exists and the user asks for SKELETON, stop and confirm — they may mean
   ENRICH. Never overwrite an existing workbook.
3. If the expected upstream artifacts for the mode are missing, list what's missing and stop —
   the workbook is downstream of them, not a substitute for them.

## Step 1 — SKELETON (SG5)

Inputs: `04-architecture/output/Sitemap.md`, `05-seo-blueprint/output/Keyword-to-Page-Map.md`,
the active Industry Module's Regulatory & Compliance Landscape and SEO & Keyword Strategy.

Create these sheets (via the `xlsx` skill — Excel Tables, header row frozen, dropdowns where noted):

| Sheet | One row per | Columns | Source |
|---|---|---|---|
| `Overview` | — | Client, Active Industry Module(s), Charter date, workbook state (`Skeleton` / `Enriched` / `Finalised`), last-updated, gate that last touched it | Charter |
| `Content Plan` | sitemap page | Page Title, URL Path, Sitemap Category, Page Type, Priority, Primary Keyword, Status (`Planned`/`Spec'd`/`Drafted`/`Approved` — dropdown), Word-Count Target (blank until SG8), Owner | Sitemap (every page, every category — cross-check the count against the Sitemap's own enumerated categories, RETRO-014), Keyword-to-Page Map |
| `Keyword Map` | keyword→page mapping | Keyword, Mapped Page, Intent, Cluster, Priority, Notes | Keyword-to-Page Map |
| `Local SEO Keyword Bank` | location × service | Location, Service/Offering, Keyword Pattern, Target Landing Page, In Sitemap? (dropdown Y/N) | Keyword-to-Page Map location rows + Module SEO & Keyword Strategy |
| `Compliance Checklist` | required disclosure / credential / regulated claim | Item, Regulation/Source, Applies to Page(s), Required Element, Status (`Open`/`Drafted`/`Cleared` — dropdown), Cleared By, Date | Module Regulatory & Compliance Landscape (seed every item, don't filter to "likely relevant") |

Set `Overview` workbook state to `Skeleton`. Save. Run the `xlsx` skill's reopen-once check that
Tables and dropdowns survived.

## Step 2 — ENRICH (SG8)

Inputs: `08-content-spec/output/Per-Page-Content-Specifications.md`,
`08-content-spec/output/Content-Depth-Standard.md`,
`08-content-spec/output/Compliance-Content-Checklist.md`.

Extend in place — do not recreate sheets:

- **`Content Plan`:** fill `Word-Count Target` from the per-page specs; move `Status` to `Spec'd`
  for every page that now has a spec. Flag any sitemap page with no spec (conditional format or a
  `MISSING SPEC` note) rather than silently leaving it blank — that gap is the thing SG8's own
  coverage check exists to catch.
- **New sheet `Page Detail`:** one row per page — Page Title, SEO Title, Meta Description, Hero
  Headline, Hero Subcopy, Key Sections (from the spec's outline), Internal Links Planned,
  Compliance Items (cross-ref to `Compliance Checklist`). Populate from the per-page specs.
- **`Compliance Checklist`:** reconcile against the SG8 Compliance Content Checklist — move items
  to `Drafted` where the spec addresses them.

Set `Overview` state to `Enriched`, update last-updated and gate. Save + reopen-once check.

## Step 3 — FINALISE (SG9)

Inputs: `09-copywriting/output/final-copy/{page-slug}.md` (one per page),
`09-copywriting/output/Voice-Tone-Guide.md`, `09-copywriting/output/Compliance-Clearance-Log.md`.

- **`Page Detail` + `Content Plan`:** fill final SEO Title / Meta Description / Hero copy from the
  final copy files; set `Status` to `Approved` only for pages whose copy is actually cleared in
  the Compliance Clearance Log — do not infer clearance from "copy exists" (RETRO-015: written
  and cleared-to-publish are two decisions). **Lock** all copy columns (`xlsx` skill: protect the
  range) once filled.
- **`Compliance Checklist`:** reconcile against the Compliance Clearance Log — `Cleared` only
  where the log names the item as individually cleared, not under a blanket "looks good"
  (RETRO-016).
- **New sheet `Blog Posts`:** one row per planned post — Working Title, Target Keyword, Cluster,
  Funnel Stage, Status, Owner. From the SG9 content plan / editorial calendar.
- **New sheets `Vlog Scripts` and `YouTube SEO & Publishing`** — **only if the Charter records a
  video budget.** If not, skip them and note "no video scope per Charter" in `Overview`.

Set `Overview` state to `Finalised`, update last-updated and gate. Save. Run the reopen-once
check (Development Sec. 5 at SG9 lists this as a Checklist line).

## Step 4 — Report

Tell the user: mode run, workbook path, sheets created/extended, page count on `Content Plan`
shown as an enumerated per-category breakdown (not a bare total — RETRO-013), any pages missing a
spec or clearance, and the reopen-once result. The workbook is a Required Document for its gate —
the Engagement Lead approves it as part of the gate's exit review.
