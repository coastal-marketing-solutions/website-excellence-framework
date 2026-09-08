> **ARCHIVED (CR-032, 2026-09-07).** This is the original proposal draft. The adopted,
> canonical record is [`WEF-v1.0/_change-requests/CR-027.md`](../../WEF-v1.0/_change-requests/CR-027.md).
> Kept for provenance; internal links below may be stale.

# Change Request — CR-027 *(IMPLEMENTED ON BRANCH — PENDING GOVERNANCE BOARD APPROVAL)*

**Submitted By:** `icm-architect` review pass (see [`WEF-ICM-Architecture-Review-2026-09-07.md`](WEF-ICM-Architecture-Review-2026-09-07.md))
**Date:** 2026-09-07
**Implementation:** branch `wef-cr-027-intake-and-icm-alignment` → PR [#13](https://github.com/coastal-marketing-solutions/website-excellence-framework/pull/13). The canon edits below are applied on that branch as the concrete artifact the Governance Board reviews; **not merged to `main`** until approved (Governance Sec. 13.2–13.3). Findings **F-4** and **F-8** from the companion review are deliberately *not* in this branch — they are staged as [`CR-028-DRAFT-Revision-Log-Migration.md`](CR-028-DRAFT-Revision-Log-Migration.md) and [`CR-029-DRAFT-Governance-Chapter-Split.md`](CR-029-DRAFT-Governance-Chapter-Split.md).
**Scope:** Core Methodology + Front Matter + `.agents/skills/` + new repo-root file
**Section/Artifact Affected:** `00-Front-Matter.md` (Revision Log); `01-Governance.md` Sec. 8.3, Sec. 1.2/1.3; `02-Research.md` SG1 Sec. 3 + Sec. 10; `09-Reusable-Templates.md` Sec. 8.4, Sec. 16.1, Sec. 16.2; `.agents/skills/new-engagement/SKILL.md` Step 1; new `AGENTS.md` + `CLAUDE.md` at repo root
**Governance Board / Engagement Lead Decision:** _Pending_
**Decision Rationale:** _Pending_
**Date Decided:** _Pending_

---

## Summary

Additive + reconciling changes generalised from live practice (three real engagements) and an ICM audit of the framework repository. Two threads:

1. **Systematise intake** — make client intake a discrete, repeatable stage-00 with a templated edit-surface artifact and a dedicated skill (`.agents/skills/intake/`, already built as additive; this CR only *wires it in*). Add one question to the canonical worksheet (priority target locations).
2. **Close three ICM schema-vs-reality drifts** — reconcile the file-naming convention to the one every engagement actually uses; fix a dangling skill pointer; give the framework repository the routing entry file its own engagement KBs already have.

**Does not** alter any Stage Gate's exit criteria, persona library, compliance landscape, Eight-Dimension standard, default technology stack, or any prior engagement approval. No re-approval of completed Stage Gate work is required.

**Impact if not approved:** intake stays an unstructured sub-step re-litigated per engagement (RETRO-style rework risk on Section 2 facts); the naming schema keeps contradicting the files (an ICM-named decay pattern); the `master-content-workbook` reference stays broken; AI agents keep navigating the framework repo without a map.

**Explicitly deferred to later CRs** (named in the review, not done here): moving CR bodies out of the Revision Log into `_change-requests/` files and generating the log; adding a literal `assets/templates/engagement-KB/` skeleton; splitting `01-Governance.md` into a `governance/` sub-folder.

---

## Item table

| ID | Section | Relationship | Change |
|---|---|---|---|
| §1 | Front Matter — Revision Log | New row | Add CR-027 row (thin), status "Working Draft" |
| §2 | Front Matter — Version History | Note | Fold CR-027 into the pending v1.4 reconciliation note, do not mint a new version line |
| §3 | Governance Sec. 8.3 | Supersedes | Rewrite to defer to Reusable Templates Sec. 21.4 as the one naming convention |
| §4 | Research SG1 Sec. 3 + Sec. 10 | Complementary | Name the `intake` skill / `01-WEF-Intake.md` artifact as a first-class SG1 input |
| §5 | Reusable Templates Sec. 16.1 | Complementary | Note that the skill renders the email / doc / status-doc forms from Sec. 16.2 |
| §6 | Reusable Templates Sec. 16.2 | New gap | Insert the priority-target-locations question; renumber the section |
| §7 | New `AGENTS.md` + `CLAUDE.md` at repo root | New gap | Add a routing entry file for the framework repository |
| §8 | `new-engagement` SKILL.md Step 1 | Complementary | Name `intake` as the strongly-preferred first step — encouraged, not gated |
| §9 | Reusable Templates Sec. 8.4 + Front Matter CR-025 | Conflict — decision required | The `master-content-workbook` skill referenced does not exist; adopt one of two fixes |

---

## §1 — Front Matter, Revision Log: new row

Append after the CR-026 row (keep the existing thin-table shape; the prose lives in *this* file, not the log — see review F-4):

```markdown
| CR-027 (Working Draft) | 2026-09-07 | Governance (Sec. 8.3, Sec. 1.2/1.3); Research (SG1 Sec. 3, Sec. 10); Reusable Templates (Sec. 16.1, Sec. 16.2 renumbered, Sec. 8.4); new repo-root `AGENTS.md`/`CLAUDE.md`; `.agents/skills/new-engagement/SKILL.md` Step 1; new `.agents/skills/intake/SKILL.md` | Systematised client intake as a stage-00 skill (`intake`) that generates the client-facing questionnaire and ingests answers into a templated `01-research/01-WEF-Intake.md` edit surface, wired as the strongly-preferred (not required) first step of `new-engagement` and as a named SG1 input. Added one question to the canonical Intake Worksheet (Sec. 16.2): client-ranked priority target locations, distinct from full service area, feeding SG5 local-landing prioritisation and the Sec. 16.3 research brief. Reconciled the file-naming convention: Governance Sec. 8.3 now defers to Reusable Templates Sec. 21.4 (`Title-Case-No-Version.md` in `output/`), the pattern all three audited engagements actually use. Added a routing entry file to the framework repository itself (previously only engagement KBs had one). Fixed/So flagged the dangling `master-content-workbook` skill reference. Additive/reconciling; no Stage Gate exit criteria, compliance landscape, or prior approval affected. **Pending formal Governance Board approval.** | Pending Methodology Governance Board approval |
```

## §2 — Front Matter, Version History

Do **not** add a new Version History line. Per the CR-022 note, v1.4 (Working Draft) is already reserved for the pending CR-020/021/022 batch; add CR-027 to the list of change requests to reconcile into version numbering at the next Board review, in the same "resolve together, not unilaterally" spirit.

---

## §3 — Governance Sec. 8.3, rewrite

**Current State:**

```markdown
### 8.3 File Naming Convention

`{stage-gate-number}-{deliverable-short-name}-v{version}.md`

Example: `05-seo-topical-map-v1.md`, `07-design-system-spec-v2.md`
```

**Proposed Change:**

```markdown
### 8.3 File Naming Convention

The canonical convention is defined in **Reusable Templates, Sec. 21.4** and is
`Title-Case-No-Version.md`, saved inside each Stage Gate folder's `output/`
subdirectory — e.g. `04-architecture/output/Sitemap.md`,
`05-seo-blueprint/output/Keyword-to-Page-Map.md`. Client-supplied source inputs
(a returned intake, a research brief) sit at the stage-folder root rather than in
`output/` — e.g. `01-research/01-WEF-Intake.md`.

The earlier `{stage-gate-number}-{deliverable-short-name}-v{version}.md` pattern
is **superseded** (all three audited engagements independently converged on the
convention above; see Sec. 21.4). Any remaining `-v{N}.md` Required-Document name
in this chapter, Design, or QA & Optimization is a not-yet-reconciled artifact of
the old pattern — substitute the real Title-Case name the next time that chapter
is edited; do not create a literal `-v1.md` file.

In-document version tracking (v0.x → v1.0 → …) continues per Sec. 8.4 and
Sec. 11 — versions live in the document's metadata block, not the filename.
```

**Rationale:** ICM anti-pattern — a schema mandating names the files stopped using. Sec. 21.4 already made this call and updated its own chapter's Required-Document lines; Sec. 8.3 was left pointing the other way. This makes 21.4 the single home for the rule and turns 8.3 into a pointer.

---

## §4 — Research SG1: name the intake artifact as an input

**Sec. 3 (Inputs) — Current State** includes:
`- Client intake questionnaire (Reusable Templates — Client Intake Templates)`

**Proposed Change** — replace that line with:

```markdown
- Completed client intake — preferably produced by the `intake` skill
  (`.agents/skills/intake/`) as `01-research/01-WEF-Intake.md`, or any
  equivalent completed Client Intake Worksheet (Reusable Templates, Sec. 16.2).
  If intake was run only as live Q&A during initialization, the same answers
  must still be written to `01-research/01-WEF-Intake.md` before this gate
  starts — SG1 reconciles *against* that file, it does not re-collect the facts.
```

**Sec. 10 (Workflow) — Current State**, step [1]:
`[1] Client Intake Questionnaire returned`

**Proposed Change:**

```markdown
[1] Completed intake present at 01-research/01-WEF-Intake.md
    (generated + ingested by the `intake` skill, or written there from
    live Q&A). Section 2 (Service Area & Licensing) fields are filled
    or explicitly marked "not sure" — never blank, never guessed.
```

**Rationale:** makes the stage-00 → SG1 handoff an explicit ICM contract (invariant 6) and gives Sec. 16.2's rationale ("every fact gathered here once should never need to be re-asked") a concrete artifact to point at.

---

## §5 — Reusable Templates Sec. 16.1, add one paragraph

Append to Sec. 16.1 ("Purpose and Design Principles"):

```markdown
**Rendering the worksheet for a client.** This section is the single source of
truth for the intake questions. The `intake` skill (`.agents/skills/intake/`)
renders it into whatever form a given client needs — a plain-text email-reply
script, a sendable document, or an online form's field list — and ingests the
answers back into the engagement's `01-research/01-WEF-Intake.md`. Do not
maintain a second hand-edited copy of the question set; if a question changes,
it changes here and every rendering follows.
```

**Rationale:** review F-6 — four drifting copies today. This names one home.

---

## §6 — Reusable Templates Sec. 16.2, insert the priority-locations question

**Placement:** immediately after Q8 ("What cities, counties, states, or regions do you actually serve?"), as the new Q9; renumber Q9–Q38 to Q10–Q39 (and the parallel copy in `assets/New-Website-Intake-Worksheet.md`, or retire that file per F-6).

**Exact text to insert:**

```markdown
9. If your business serves a geographic area, which specific cities or
   locations are your highest priority to be found in online? — [Paragraph]
   *(List your top 10–25 target locations, ranked roughly by importance if you
   can. This is separate from the question above: that one is everywhere you're
   willing to serve; this is where you most want to win business. Skip this if
   you're not tied to specific geographies — e.g., a fully remote or nationwide
   business.)*
```

**Downstream wiring (same CR):**

- **Sec. 16.3 (Perplexity Deep Research Brief)** — in the "Fixed facts" block, add:
  `- Ranked priority locations (win-business targets): [from Worksheet Q9]`
  and in "What to produce" item 3, change "location pages for the *confirmed*
  service area only" to "location pages for the confirmed service area, built
  and prioritised in the client's Q9 ranked order where one was given."
- **SEO & Architecture SG5** — no text change required now; the ranked list is
  consumed where local-landing pages are prioritised. Flag for the SG5 author
  to reference Q9 explicitly next time that chapter is touched.

**Rationale:** the "Juan" intake already asks this in the field; it's a real practice need (which locations to build and prioritise first), and it directly de-risks the exact Sec. 16.3 failure that section was written to prevent (a research pass inventing or misordering geography). Adding it to canon closes F-6 rather than letting the skill carry a question the worksheet lacks.

---

## §7 — New repo-root routing entry file

**Create `AGENTS.md` at the repository root:**

```markdown
# Website Excellence Framework — repository map

WEF is an industry-agnostic **Core Methodology** (numbered Stage Gates, run in
order, every engagement) plus a library of pluggable **Industry Modules** (one
selected per engagement). This file routes; it holds no methodology content.

## Where things live

| Path | What it is |
|---|---|
| `WEF-v1.0/00-Front-Matter.md` | Intro, architecture, Revision Log. Read once. |
| `WEF-v1.0/Core-Methodology/01…10` | The Stage Gate spine, in order. |
| `WEF-v1.0/Industry-Modules/` | Vertical packs; `00-Module-Template-and-Index.md` first. |
| `WEF-v1.0/Component-Library/` | Cross-industry reusable UI components. |
| `.agents/skills/` | Runnable skills — see routing table below. |
| `assets/` | Protocols and worksheets that support the method but aren't canon. |

## Route by task

| I want to… | Go to |
|---|---|
| Start a new client website | `.agents/skills/intake/` → then `.agents/skills/new-engagement/` |
| Collect / process a client's intake answers | `.agents/skills/intake/SKILL.md` |
| Initialise the engagement KB after intake | `.agents/skills/new-engagement/SKILL.md` |
| Run a Stage Gate | `WEF-v1.0/Core-Methodology/` — the chapter for that gate, with the active Industry Module open alongside |
| Add or fix an Industry Module | `WEF-v1.0/Industry-Modules/00-Module-Template-and-Index.md` |
| Roll engagement findings back into the framework | `.agents/skills/wef-sync/SKILL.md` |
| Reconcile changes from several engagements/contexts at once | `assets/WEF-Multi-Context-Reconciliation-Protocol.md` |
| Propose a methodology change | `WEF-v1.0/Core-Methodology/09-Reusable-Templates.md` Sec. 3 (Change Request template) |

## Rules

- Core Methodology changes go through a Change Request + Governance Board
  (Governance Sec. 13.1–13.2). Never edit canon silently.
- Industry-specific facts live in Industry Modules, never in the Core.
- One home per fact — link, don't copy.
```

**Create `CLAUDE.md` at the repository root** (one line, per invariant 2 — never two hand-maintained entry files):

```markdown
See [AGENTS.md](AGENTS.md) — the repository map and task router.
```

**Rationale:** review F-1 + walk test. The engagement KBs have this (`CLAUDE.md` L0); the repo defining them does not, so an AI agent opening the framework repo has to read prose to orient.

---

## §8 — `new-engagement` SKILL.md, Step 1 rewrite

**Current State** — Step 1 opens: *"Ask the user first whether a completed Client Intake Worksheet … already exists … If one exists, use it as the source of truth and skip the live conversational Q&A …"*

**Proposed Change** — replace the first paragraph of Step 1 with:

```markdown
## Step 1 — Intake: prefer the `intake` skill; fall back to live Q&A

The strongly-preferred first step is the **`intake` skill**
(`.agents/skills/intake/`). It produces `01-research/01-WEF-Intake.md` — the
templated, human-reviewed intake artifact this step consumes. Check whether it
has already been run for this client:

- **`01-research/01-WEF-Intake.md` exists** → use it as the source of truth.
  Skip the live Q&A below; only ask follow-ups for fields it marks "not sure"
  or leaves blank.
- **It does not exist** → recommend running `intake` now (it takes the same
  answers, in the same order, and writes the artifact this step needs). This is
  encouraged, not mandatory — if the user wants to proceed immediately, run the
  Section-by-section Q&A below as a live conversation, and **write the answers
  into `01-research/01-WEF-Intake.md` as you go** so the artifact still exists
  for SG1 and is never re-collected later.

Either path: anything not yet known is marked **PENDING** / "not sure", never
guessed or invented (Documentation Standard — fabricated license numbers,
metrics, or competitor data are a hard no).
```

Leave the rest of Step 1 (the load-bearing Section 2 warning, the live-conversation fallback question list) unchanged.

**Rationale:** review F-5. Makes `intake` the front door without turning it into a gate — `new-engagement` still works standalone for a user who declines it.

---

## §9 — Dangling `master-content-workbook` reference — decision required

**Current State:** `09-Reusable-Templates.md` Sec. 8.4 and `00-Front-Matter.md` CR-025 both point to `.agents/skills/master-content-workbook/SKILL.md` for the workbook build/extend procedure and the exact prompt. **That file does not exist in the repository.** Sec. 8.4 also states the workbook is now a Required Document at SG5/SG8/SG9 — so a live instruction depends on a missing file.

**Option A — build the skill** (preferred if the workbook procedure is stable enough to write down). Create `.agents/skills/master-content-workbook/SKILL.md` with the build/extend procedure, module definitions, and prompt currently only described in prose. No text change to Sec. 8.4.

**Option B — downgrade the references** until the skill exists. In Sec. 8.4, replace the last sentence with:

```markdown
Full procedure, module definitions, and the exact build/extend prompt are being
consolidated into `.agents/skills/master-content-workbook/SKILL.md` (not yet
implemented as of CR-027). Until it lands, build the workbook by hand from the
Content Plan (SG5), per-page specs (SG8), Keyword Map (SG5), Local SEO Keyword
Bank (SG5), and Compliance Checklist, consolidated into one `.xlsx`; extend the
same file at SG8 and SG9 rather than regenerating it.
```

and add a Project Backlog note in the framework's own tracking that the skill is outstanding.

**Recommended:** Option B now (honest, unblocks readers immediately), Option A as a fast follow once someone can write the procedure down accurately. Either way, a governance chapter must not point at a file that isn't there.

---

## Validation checklist (for the integrator, before this CR is marked adopted)

- [ ] CR-027 number re-checked against the Revision Log immediately before merge (Sec. 15.6 dedup discipline — CR-021/022/024/025 all collided).
- [ ] Sec. 16.2 renumbering applied consistently everywhere the old Q-numbers are cited (Sec. 16.3 "from Worksheet Q7/Q8/Q9/Q26" references shift).
- [ ] `assets/New-Website-Intake-Worksheet.md` either updated in lockstep or converted to a pointer to Sec. 16.2.
- [ ] Root `AGENTS.md` links all resolve; `CLAUDE.md` is the one-line pointer, not a copy.
- [ ] `new-engagement` Step 1's downstream steps still read correctly after the Step 1 head swap.
- [ ] Markdown fences/tables valid; `git diff --check` clean.
- [ ] Review the rendered result, not just the diff — the `intake` → `new-engagement` → SG1 path walks cleanly end to end.
