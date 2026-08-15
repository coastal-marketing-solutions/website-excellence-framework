---
name: wef-sync
description: Run a Cross-Engagement Contribution sync pass — scan every active engagement's WEF-Candidate-Findings.md for Flagged entries, dedup each against the WEF Revision Log and open GitHub branches/PRs, reserve Change Request numbers for genuinely new findings, and stage one batched branch/PR per cycle. Use when the user asks to "sync WEF findings," "check for cross-engagement updates," "run a WEF sync," or periodically (weekly, or whenever an engagement reaches SG11.5) while more than one engagement is active concurrently.
---

# Cross-Engagement Contribution Sync

Implements Governance Sec. 15.6 (Cross-Engagement Contribution Pipeline). Goal: findings
discovered live across concurrent engagements land in WEF exactly once, as one batched Change
Request per sync pass — never as duplicate, independently-authored branches. See RETRO-013
(Governance, Sec. 15.4) for the actual incident this exists to prevent: three branches carrying
overlapping content for what was ultimately a single Change Request, because nothing checked
whether the finding was already in flight before staging it again.

Read as needed, don't front-load: `../WEF-v1.0/Core-Methodology/01-Governance.md` Sec. 15.4
(RETRO-013), Sec. 15.6 (the pipeline this skill automates); `09-Reusable-Templates.md` Sec. 23.1
(the `WEF-Candidate-Findings.md` template/status schema); `00-Front-Matter.md`'s Revision Log
(source of truth for existing/reserved CR numbers).

## Step 1 — Discover active engagements

List sibling folders next to this repo. An engagement is in scope for sync if it has a
`WEF-Candidate-Findings.md` (in `_config/` or at KB root, per whichever convention that
engagement uses). Skip folders that don't have one yet — pre-initialization engagements, empty
placeholder folders, or archived/inactive ones.

If a folder looks like an active engagement KB (stage-gate folders, a Decision Register) but has
no `WEF-Candidate-Findings.md`, don't silently skip it — flag it to the user at Step 7 as a
candidate to backfill from the Sec. 23.1 template.

## Step 2 — Collect Flagged entries

Read each discovered `WEF-Candidate-Findings.md` and pull every row with Status = `Flagged`.
Track the source engagement against each finding — Step 6 needs it to flip the right row in the
right file.

If nothing is Flagged anywhere, report that and stop. This is a common, legitimate outcome, not
an error condition — don't manufacture a batch just to have something to report.

## Step 3 — Dedup pass (Governance Sec. 15.6, Layer 2)

For each Flagged finding, check both:

1. **Revision Log** (`WEF-v1.0/00-Front-Matter.md`) — does an existing CR already cover this
   Core/Module section or the same underlying pattern? Read the target section's actual content
   and CR history; don't just keyword-match the table.
2. **Open branches/PRs** — `git fetch origin --prune && git branch -a`, and `gh pr list` — is
   another finding already in flight against the same target?

Sort each finding into one of three buckets:

- **Duplicate of an existing (already-merged) CR** — don't re-stage it. Flip the source row to
  `Rejected`, with the existing CR ID and a one-line reason in the Description column.
- **Overlaps an open branch/PR** — reconcile into that existing branch/PR instead of opening a
  second one for the same target. Flip the source row to `Staged` with that branch's CR ID once
  reconciled.
- **Genuinely new** — proceed to Step 4.

## Step 4 — Reserve and batch

Find the highest existing CR number in the Revision Log, including "Working Draft"/"Reserved"
rows (reserve the next number — never reuse one that's merely pending). All genuinely-new
findings from this sync pass share **one** CR number and **one** branch
(`wef-cr-{NNN}-{slug}`), not one each — default to batching per Sec. 15.6 Layer 3's intent.
Split out a separate CR only when a finding is large or contested enough that bundling it would
make the PR hard to review or approve independently; use judgment, and say why if you split.

Add a Revision Log row for the reserved CR (status: "Working Draft" or "Reserved," matching the
table's existing convention) before writing any content, so a concurrent session sees the CR is
already claimed if it checks Layer 2 mid-sync.

## Step 5 — Draft the methodology change

For each finding in the batch, write it up the way RETRO-001 through RETRO-013 are written
(Governance, Sec. 15.4): What Happened, Generalized Risk, Methodology Fix, Status — stripped of
client-identifying detail per Sec. 15.2's schema (a client name never needs to appear; "a live
engagement in the [X] vertical" is enough). Apply the actual Core Methodology/Module edits the
fix calls for. Cite the new RETRO ID(s) and this sync's CR number from every section touched.

## Step 6 — PR and merge

Push the branch, open a PR (`gh pr create`) summarizing the batch — list every finding, its
generalized description, and its source engagement — and follow this repository's standing merge
practice. On merge, flip every source engagement's `WEF-Candidate-Findings.md` row from `Flagged`
to `Merged` with the CR ID. This closing step is why Step 2's per-finding source tracking
matters — without it, there's no way back to the originating file to close the loop.

## Step 7 — Report back

Tell the user: how many findings were found across how many engagements; how many were
duplicates or overlaps (and what they were reconciled into, per Step 3); how many shipped in this
batch and under which CR; which engagements' source logs were updated to `Merged`. If Step 1
surfaced any engagement that looks active but has no `WEF-Candidate-Findings.md` yet, remind the
user it needs backfilling before the next sync pass can see its findings.
