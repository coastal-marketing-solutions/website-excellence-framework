# WEF ICM Architecture Review

**Date:** 2026-09-07
**Reviewer context:** `icm-architect` skill (Interpretable Context Methodology — Van Clief & McDermott, arXiv:2603.16021), run in **Restructure / audit mode** against the Website Excellence Framework repository at `website-excellence-framework/` (v1.4 working draft).
**Status:** Advisory. Findings **F-1, F-2, F-3, F-5, F-6, F-7** are implemented on branch `wef-cr-027-intake-and-icm-alignment` (see [`CR-027-DRAFT-Intake-Skill-and-ICM-Alignment.md`](CR-027-DRAFT-Intake-Skill-and-ICM-Alignment.md)) as the artifact the Methodology Governance Board reviews via PR — **not merged to `main`** until approved (Governance Sec. 13.2–13.3). Findings **F-4** and **F-8** are staged as separate follow-up Change Requests — [`CR-028-DRAFT-Revision-Log-Migration.md`](CR-028-DRAFT-Revision-Log-Migration.md) and [`CR-029-DRAFT-Governance-Chapter-Split.md`](CR-029-DRAFT-Governance-Chapter-Split.md) — because each is large enough that folding it into CR-027 would make the PR unreviewable, and F-8 needs a Board design discussion, not just sign-off.

---

## 1. What this review measured against

ICM judges a workspace by ten invariants and a cold "walk test." The ones that bear on WEF:

1. One folder, one job; the structure is the documentation.
2. A small, stable entry file that **routes and holds no content** (`CLAUDE.md` / `AGENTS.md`, target < ~60 lines).
3. Numbering encodes order.
4. Every folder-level contract is explicit (`CONTEXT.md`: reads / does / writes / human-checks).
5. Factory vs. product — stable reference material lives structurally apart from per-run artifacts.
6. Every output is an edit surface a human reads before the next step consumes it.
7. Load only what the step needs (~2k–8k tokens per step).
8. Plain text, linkable, queryable; **one home per fact — a link beats a copy**.
9. The filesystem is the state machine; generated indexes are rebuilt by script, never hand-edited.
10. Instantiate by copying a template folder, not a blank page.

**Walk test:** open the root cold, as an agent with no memory — can you answer *where am I* and *where do I go for task X* within the entry file plus at most two more reads?

---

## 2. Verdict

WEF is already an unusually faithful ICM deployment **at the engagement-Knowledge-Base level**. The parts that are working should not be disturbed:

- **The L0–L4 navigation layer (Governance Sec. 5.2.1 + Reusable Templates Sec. 21)** is a correct, well-reasoned adaptation of the five-layer context hierarchy. `CLAUDE.md` capped at ~800 tokens, `_config/` (engagement-stable) split from `_references/` (engagement-independent), stage `CONTEXT.md` as a trimmed instance of the 19-part gate template with a link back rather than a restatement — this is textbook.
- **Numbered Core-Methodology chapters** (`01`…`10`) encode order (invariant 3).
- **The Module Injection Point convention (Governance Sec. 9)** is a clean factory/product seam (invariant 5): the Core is the stable factory, the active Industry Module is the per-vertical configuration, and the injection points are the explicit, marked interface. This is the single best structural idea in the framework.
- **"Create a stage folder only when that stage begins" (Sec. 5.2.1 Rule 2)** correctly refuses speculative depth.
- **`WEF-Candidate-Findings.md` + the `wef-sync` skill** is the beginnings of invariant 9 — deriving state (what's in flight) from files rather than memory.

Where WEF drifts from ICM is almost entirely **at the framework-repository level** — the repo that publishes the methodology is itself not walkable as an ICM — and in **three specific schema-vs-reality drifts** that ICM names as classic decay patterns. None are structural emergencies; all are cheap to fix and get more expensive to fix later.

---

## 3. Findings

Severity: **High** = actively misdirects a reader or has already caused rework; **Medium** = real drift, no incident yet; **Low** = optimization.

### F-1 — The framework repo has no routing entry file *(High, invariant 2 + walk test)*

A cold agent (or new contributor) opening `website-excellence-framework/` gets `README.md` — prose, pitched at GitHub visitors — or `WEF-v1.0/00-Front-Matter.md`, which is ~270 lines of title page, copyright, version history, and a Revision Log. Neither answers *"I need to do X — which file do I open?"* in a small read. There is no `AGENTS.md` / `CLAUDE.md` at the repo root doing pure routing.

The engagement KBs have this file (`CLAUDE.md`); the repo that defines them does not.

**Recommendation:** add a root `AGENTS.md` (with `CLAUDE.md` as a one-line pointer to it, per invariant-2 "never two hand-maintained copies"): identity in two sentences, then a routing table — *task → file*. Core chapters, the Module library + its template, the Component Library, `.agents/skills/`, `assets/` protocols. Target < 60 lines, zero methodology content. Exact proposed file in CR-027 §7.

### F-2 — The file-naming schema contradicts the files it governs *(High, invariant 8; "schema mandating names the files stopped using" — a named ICM anti-pattern)*

- **Governance Sec. 8.3** mandates `{stage-gate-number}-{deliverable-short-name}-v{version}.md` (e.g. `05-seo-topical-map-v1.md`).
- **Reusable Templates Sec. 21.4** says that pattern was **never actually used**, is **superseded**, and every audited engagement (Discover the Alamo, So Cal Realty, Itzel Gonzalez) independently converged on `Title-Case-No-Version.md` inside `output/`.
- **Research Sec. 5 (SG1 Required Documents)** still lists `discovery-report-v1.md`, `client-personas-v1.md`, etc. — the superseded pattern, presented as a live instruction.
- The two real intake artifacts add a **fourth** shape: `01-WEF-Intake.md` (numeric prefix, no version, not Title-Case, not in `output/`).

ICM: *"schema documents that mandate names the actual files stopped using — update the schema or the files, pick one."* Pick 21.4.

**Recommendation (CR-027 §3, §4):** rewrite Sec. 8.3 to defer to Sec. 21.4 as canonical; sweep the `-v1.md` names out of Research / Design / QA Required-Document lists the next time each chapter is touched (21.4 already says to, but nothing tracks it); and have the new `intake` skill settle the intake artifact name as `01-research/01-WEF-Intake.md` explicitly so a fourth pattern doesn't keep propagating by copy.

### F-3 — Broken pointer to a skill that does not exist *(Medium, invariant 8 / reference integrity)*

`00-Front-Matter.md` CR-025 and `09-Reusable-Templates.md` Sec. 8.4 both point to `.agents/skills/master-content-workbook/SKILL.md` for "the exact build/extend procedure." That path is not in the repo (`.agents/skills/` contains only `new-engagement/` and `wef-sync/`). Sec. 8.4 also states the workbook is now a Required Document at SG5/SG8/SG9 — so a live instruction depends on a missing file.

**Recommendation (CR-027 §9):** either add the skill, or downgrade both references to "planned — not yet implemented; until then, build the workbook by hand from the module definitions in [wherever they actually live]." A dangling pointer in a governance chapter is worse than an honest TODO.

### F-4 — The Revision Log is a catalog holding books *(Medium, invariant 2 + 9)*

`00-Front-Matter.md`'s Revision Log is a table whose rows (CR-014 through CR-026) each carry 5–15 lines of prose describing what changed and why. "The catalog holds no books" — a routing/index surface that has absorbed payload. Symptoms already visible:

- **CR-number collisions** — RETRO-017 documents CR-021/RETRO-013 being renumbered to CR-022/RETRO-017 after a concurrent session claimed the same number; CR-024/CR-025 had the same collision. This is exactly the failure ICM predicts for a **hand-maintained index** (invariant 9: "generated indexes are rebuilt by script, never hand-edited").
- The log is now long enough that reading it to answer "what's the highest CR number" — which `wef-sync` Step 4 requires every sync — is itself a non-trivial scan.

**Recommendation (CR-027 §10, flagged as follow-up not done in CR-027):** move each CR's body to `_change-requests/CR-0NN.md`; reduce the Revision Log to a thin table (ID · date · sections · one-line · status · link). Longer term, generate that table from the `_change-requests/` files' frontmatter so it cannot drift. This also gives `wef-sync` a single file to read for the next free number.

### F-5 — Intake is a buried sub-step, not an edit-surface stage *(Medium, invariant 1 + 6 — addressed by the new skill)*

Today, client intake lives inside `new-engagement` Step 1 as conversational Q&A, with "use a completed worksheet if one exists" as an optional branch and **no in-repo template for the completed artifact**. ICM wants intake to be its own job (invariant 1) that emits a file a human reviews and corrects (invariant 6) *before* `new-engagement` consumes it — a clean stage-00 → stage-01 handoff.

The two real artifacts you provided (So Cal Realty's `01-WEF-Intake.md` status doc; the "Juan" email-reply script) show this is *already how the practice works* — it's just not structured.

**Recommendation (built):** the new `.agents/skills/intake/` skill makes intake a discrete, repeatable stage-00 that **generates** the client-facing intake (email-reply or sendable doc, rendered from the canonical worksheet) and **ingests** the answers into a templated `01-research/01-WEF-Intake.md`, then hands off to `new-engagement`. `new-engagement` Step 1 gets a one-paragraph rewrite (CR-027 §8) to name the skill as the strongly-preferred first step — **encouraged, not gated**: if the skill wasn't run, `new-engagement` still falls back to live Q&A exactly as today.

### F-6 — Three drifting copies of one worksheet *(Medium, invariant 8)*

The intake questionnaire now exists as: (a) `09-Reusable-Templates.md` Sec. 16.2 — form-field-tagged, 38 questions; (b) `assets/New-Website-Intake-Worksheet.md` — near-duplicate, 38 questions, no field tags; (c) the So Cal status doc; (d) the "Juan" email script — **39 questions** (adds "top 10–25 priority target locations, ranked," separate from full service area). Four renderings, drifting question counts and numbering, no declared source of truth.

**Recommendation (CR-027 §5, §6):** declare `09-Reusable-Templates.md` Sec. 16.2 the **single source**; add the priority-locations question there (it feeds SG5 local-landing prioritization and the Sec. 16.3 Perplexity brief's "location pages for confirmed area only" instruction — genuinely load-bearing); make `assets/New-Website-Intake-Worksheet.md` a pointer to it or delete it; and have the `intake` skill *render* the email / doc / status-doc forms from Sec. 16.2 rather than anyone maintaining them by hand.

### F-7 — No literal template folder to instantiate from *(Low/Medium, invariant 10)*

`new-engagement` Step 6 builds a new KB by re-deriving the structure from templates scattered across Sec. 16.2, 21.1, 21.2, 21.3, 23.1. ICM invariant 10: *a new unit of work is a copy of a template folder, not a blank page assembled from instructions.*

**Recommendation:** add `assets/templates/engagement-KB/` — the exact skeleton from Sec. 5.2.1 with placeholder-filled `CLAUDE.md` / `CONTEXT.md` / `_config/*` / `01-research/CONTEXT.md`. `new-engagement` Step 6 becomes "copy this folder, then fill placeholders" — shorter, and it cannot drift from the documented structure. (Not in CR-027; low urgency, flagged for a later pass.)

### F-8 — `01-Governance.md` is one 883-line file doing ~15 jobs *(Low, invariant 1 + 7)*

Initialization, roles, charter, decision register, KB structure, blueprint, backlog, doc standards, module integration, project memory, version control, firm QA, 13 governance policies, risk, retrospectives — one file, ~40k tokens. A task needing only the Decision Register schema loads all of it. The retrospectives themselves (RETRO-013/014: a coverage claim checked against the wrong list; a miscount propagating four gates) are partly *"nobody re-read the buried rule."*

**Recommendation:** eventually split into a `governance/` sub-folder (`01-initialization.md`, `02-roles.md`, …) with its own `CONTEXT.md` router — the L1 pattern applied recursively, exactly as `references/core.md` prescribes for any L3 collection that outgrows easy scanning. **Deliberately not in CR-027** — it's a major structural change touching every cross-reference in the manual and deserves its own CR and Board discussion. Listed here so it's on the record.

---

## 4. The walk test, run cold

**Framework repository** (`website-excellence-framework/`):

| Check | Result |
|---|---|
| Open root, answer *where am I* + *where do I go for task X* in entry + ≤2 reads | **FAIL** — no routing entry file (F-1). README is prose; Front-Matter is content. |
| Numbering encodes order | PASS (Core chapters). Modules unnumbered — correct, it's a library. |
| Any routing file carrying content payload | **FAIL** — Revision Log (F-4). |
| Any fact stored in two places | **FAIL** — worksheet ×4 (F-6); naming schema stated two incompatible ways (F-2). |
| Every reference resolves | **FAIL** — `master-content-workbook` pointer (F-3). |

**Engagement Knowledge Base** (any `*Website Blueprint/`):

| Check | Result |
|---|---|
| Open root, answer *where am I* + *where do I go* in entry + ≤2 reads | **PASS** — `CLAUDE.md` → `CONTEXT.md` stage map. |
| Every stage contract names inputs / job / outputs / human check | PASS — Sec. 21.3 template. |
| State derivable by scanning `output/` folders | PASS — Sec. 5.2.1 Rule 5 + the "no stage folder until the stage begins" rule. |
| Any routing file carrying payload | PASS — `CLAUDE.md` capped at ~800 tokens. |
| Instantiate by copying | PARTIAL — scaffolded by a skill from scattered templates, no literal template folder (F-7). |

The engagement KB passes. The repository that publishes the methodology does not — and it should, because the same AI agents that run engagements are the ones who have to navigate the framework repo to do it.

---

## 5. Prioritized recommendations

| # | Action | Finding | Vehicle | Status |
|---|---|---|---|---|
| 1 | Add root `AGENTS.md` routing file (+ `CLAUDE.md` pointer) | F-1 | CR-027 §7 | **done (branch)** |
| 2 | Reconcile Sec. 8.3 → Sec. 21.4 as the one naming convention; sweep every `-v{N}.md` Required-Document name out of Research / UX / Design / Development / QA / AI-Agent-Services | F-2 | CR-027 §3, §4 | **done (branch)** |
| 3 | Mark the never-built `master-content-workbook` skill outstanding; move its procedure inline to Reusable Templates Sec. 8.4; redirect the three dangling `Sec. 9.x` skill refs | F-3 | CR-027 §9 | **done (branch)** |
| 4 | Ship the `intake` skill; rewire `new-engagement` Step 1 to prefer it (not require it); wire the artifact into Governance init checklist + Research SG1 Inputs/Workflow | F-5 | `intake/` + CR-027 §4, §8 | **done (branch)** |
| 5 | Declare Sec. 16.2 the single worksheet source; add the ranked priority-locations question as Q9 (renumber Q10–Q39); wire it into the Sec. 16.3 research brief; make `assets/New-Website-Intake-Worksheet.md` a labelled mirror | F-6 | CR-027 §5, §6 | **done (branch)** |
| 6 | Add `assets/templates/engagement-KB/` skeleton; simplify `new-engagement` Step 6 to "copy + fill" | F-7 | CR-027 §6 (item table) | **done (branch)** |
| 7 | Move CR bodies to `WEF-v1.0/_change-requests/CR-0NN.md`; thin the Revision Log; later, generate it | F-4 | **CR-028 (draft)** | staged |
| 8 | Split `01-Governance.md` into a `01-governance/` sub-folder with its own router | F-8 | **CR-029 (draft)** | staged for Board discussion |

Items 1–6 are on branch `wef-cr-027-intake-and-icm-alignment` and are all additive or reconciling — no Stage Gate exit criteria, persona library, compliance landscape, Eight-Dimension standard, default technology stack, or prior approval is affected. Items 7–8 are drafted as their own Change Requests: F-4's migration is ~22 new files plus a rewrite of the manual's most cross-referenced table, and F-8 touches hundreds of cross-references and needs a Board design decision first.

---

## 6. What was built alongside this review

`.agents/skills/intake/SKILL.md` — a new skill, additive, touching no canon. It is the "flip the switch" entry point: one command that either **generates** a personalized client-facing intake (in the email-reply format you showed me, or as a sendable doc) or **ingests** returned answers (pasted reply, uploaded file, or live conversation) into a templated `{Client} Website Blueprint/01-research/01-WEF-Intake.md`, then hands off to `new-engagement`. It is highly encouraged and never required — `new-engagement` still runs standalone. See the skill's own file for the full contract.
