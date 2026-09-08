# Board Decision Memo — CR-029: Governance Chapter Navigability

**For:** Methodology Governance Board
**From:** Framework maintenance (via `icm-architect` review pass, finding **F-8**)
**Date:** 2026-09-07
**Decision needed by:** next Board review
**DECISION (2026-09-07):** **Option C** — split + pointer stub + deferred opportunistic reference sweep. Implemented in CR-029 (`WEF-v1.0/_change-requests/CR-029.md`); deferred sweep tracked in [`CR-029-Reference-Sweep-Checklist.md`](CR-029-Reference-Sweep-Checklist.md).
**Companion documents:** [`WEF-ICM-Architecture-Review-2026-09-07.md`](WEF-ICM-Architecture-Review-2026-09-07.md) §F-8 · [`CR-029-DRAFT-Governance-Chapter-Split.md`](CR-029-DRAFT-Governance-Chapter-Split.md)

This memo exists because F-8 is the one audit finding the reviewer explicitly declined to
implement or even fully design without the Board. It is a structural change to the single most
cross-referenced chapter in the manual, and Governance Sec. 13.3 reserves that call for the
Board. The other seven findings (F-1–F-7 in CR-027, F-4 in CR-028) are merged.

---

## 1. The problem

`WEF-v1.0/Core-Methodology/01-Governance.md` is **one 885-line file (~40k tokens)** carrying
~15 distinct jobs: project initialization, roles/RACI, charter, decision register, knowledge-base
structure, blueprint, backlog, documentation standards, module integration, project memory,
version control, firm-level QA, 13 governance policies (Sec. 13 alone runs Sec. 13.1–13.6.x),
risk, and the Retrospective Register + Cross-Engagement Contribution Pipeline.

Two ICM invariants bear on it:

- **Invariant 1 — one folder, one job.** Fifteen jobs in one file.
- **Invariant 7 — load only what the step needs (~2k–8k tokens per step).** A task that needs
  only the Decision Register schema (Sec. 4.2, ~15 lines) currently pulls the whole 40k-token
  chapter into context.

**Evidence this is not purely theoretical:** RETRO-013 and RETRO-014 both trace partly to *"a
rule that lived in this file was not re-read at the point it applied."* A more navigable chapter
is a partial structural mitigation for that failure class — though not a complete one (those
retros also have dedicated checklist fixes already shipped).

**Counter-argument the Board should weigh:** the chapter is *reference material*, read
selectively. A disciplined reader (human or AI) already jumps to the section they need via
search or a ToC. If that discipline holds in practice, the token-budget cost is theoretical and
the change is not worth its price.

---

## 2. What the change would cost

| Dimension | Detail |
|---|---|
| Files created | ~16 (`01-governance/CONTEXT.md` + 15 section files) |
| Cross-reference sweep | **~201 `Governance, Sec. X` references across ~40 files** — every Core chapter, most Industry Modules, the Component Library, Reusable Templates, all four skills, and the engagement-KB templates |
| Highest-density files | `99-Back-Matter.md` (34), `06-Development.md` (22), `05-Design.md` (16), `09-Reusable-Templates.md` (13) |
| Section-number stability | Preserved — `Sec. 13.5` stays `Sec. 13.5` *inside* `13-policies.md`, so a stale reference still resolves semantically; it just doesn't name the file |
| Reversibility | Low once merged — reverting means re-sweeping 201 references back |
| Live-engagement impact | Every active engagement KB's `CLAUDE.md` / `CONTEXT.md` points at `Governance Sec. X`; those would drift until each engagement is touched |

The sweep is the bulk of both the work and the risk. A missed or mis-targeted reference is a
silent broken pointer.

---

## 3. Options

### Option A — Generated in-file ToC + anchor links (low risk)

Keep `01-Governance.md` as one file. Add a maintained (ideally script-generated) table of
contents at the top with anchor links to every `##` and `###` heading. Optionally add "↑ top"
links at each section break.

- **Cost:** ~1 file touched, no cross-reference sweep, no engagement-KB drift.
- **Benefit:** Most of the *navigation* win for a human reader. Zero help for the
  token-budget / selective-load problem — an AI step still loads the whole file.
- **Reversibility:** Trivial.
- **ICM verdict:** Partial. Addresses "can a reader find the rule" but not "does the step load
  only what it needs."

### Option B — Full split into `01-governance/` + complete cross-reference sweep (high value, high risk)

Implement the CR-029 draft's folder layout. Sweep all ~201 references to the
`Governance — 13-policies.md, Sec. 13.5` form. Update engagement-KB templates and (as a
follow-up rollout) active engagement navigation layers.

- **Cost:** ~16 files created, ~40 files swept, multi-session rollout for live engagements.
- **Benefit:** Full ICM compliance on invariants 1 and 7. `CONTEXT.md` becomes the recursive L1
  router. Each step loads 2k–8k tokens instead of 40k.
- **Reversibility:** Low.
- **ICM verdict:** Complete.

### Option C — Split the file, keep a pointer stub, defer the sweep (staged)

Split into `01-governance/` **and** leave `01-Governance.md` as a thin stub that points to
`01-governance/CONTEXT.md` (mirrors the repo-root `AGENTS.md` / `CLAUDE.md` pattern from CR-027,
and the thin Revision Log from CR-028). Do **not** sweep the 201 references in the same CR;
existing `Governance, Sec. 13.5` references keep resolving because section numbers are stable and
the stub tells a reader where to go. Sweep opportunistically ("next time each chapter is
touched," the same mechanism CR-027 used for the file-naming convention).

- **Cost:** ~17 files created/changed in the CR itself; the sweep amortizes over future edits.
- **Benefit:** Captures the token-budget win immediately for anyone loading via `CONTEXT.md`;
  spreads the reference-sweep risk across many small reviewed edits instead of one 40-file diff.
- **Risk:** A long period where two navigation conventions coexist (`Sec. X` prose refs vs.
  file-named refs). Needs a tracked checklist so the sweep actually finishes, or it becomes
  permanent drift.
- **ICM verdict:** Complete in structure, with a documented migration debt.

---

## 4. Recommendation

**Option C**, unless the Board judges the token-budget problem not worth any structural change —
in which case **Option A** as the floor.

Rationale: the split itself is the part with lasting value and is cleanly reviewable; the
201-reference sweep is where the risk concentrates, and CR-027 already proved that an
opportunistic, per-chapter sweep of a naming change works and stays low-risk. Bundling the sweep
into one CR (Option B) maximizes the chance of a silent miss and produces a diff no reviewer can
actually verify line-by-line.

Option A is a reasonable stop if the Board's read is that selective loading already works in
practice and hundreds of reference edits are not justified by a theoretical budget concern.

---

## 5. Decision points for the Board

1. **Is the problem worth acting on at all?**
   ☐ Yes, structurally (→ Q2) ☐ Yes, but only a ToC (→ Option A) ☐ No, leave as-is

2. **If structural — split now with deferred sweep (C), or all-in-one (B)?**
   ☐ Option C ☐ Option B

3. **If split — keep `01-Governance.md` as a pointer stub, or delete it and make
   `01-governance/CONTEXT.md` the entry?**
   ☐ Stub ☐ Delete + CONTEXT.md is entry

4. **Sweep tracking (Option C only):** who owns the checklist that ensures the 201-reference
   migration completes, and by when?

5. **Live-engagement rollout:** update active engagement navigation layers as part of CR-029, or
   as a separate tracked rollout (as CR-022's candidate-findings backfill was handled)?

---

## 6. What happens after the decision

| Decision | Next step |
|---|---|
| No action | Close CR-029; note the rejection rationale in `_change-requests/CR-029.md` for the record |
| Option A | Implement in one PR; reserve CR-029; no Board re-review needed beyond this memo |
| Option C | Draft the `01-governance/` layout + `CONTEXT.md` router for Board review of the *structure* (not the sweep); reserve CR-029; open the sweep-tracking checklist |
| Option B | Same as C plus the full sweep in the same branch; expect a multi-day review |

CR-029's number is reserved implicitly by this memo's companion draft; the canonical write-up
will be created at `WEF-v1.0/_change-requests/CR-029.md` once the Board picks a direction.
