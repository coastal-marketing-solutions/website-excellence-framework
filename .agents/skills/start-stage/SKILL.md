---
name: start-stage
description: Trigger a Stage Gate that has not formally started in an existing engagement Knowledge Base, most often Stage Gate 11 (QA) and 11.5 (Post-Launch Growth) for sites whose KB stops at SG10 or SG10.5. Also sweeps all sibling KBs and reports which stage each one is really at. Runs the Stage Transition Check on the previous gate, creates the stage folder from the template, records it in the Stage Ledger, and queues the client-owned steps on the Action Items Sheet.
---

# Start a Stage Gate in an existing engagement

Governance Sec. 5.2.1 Rule 2 creates a stage's folder only when the stage begins, so a build that was
implemented straight from the SG10 Build Package never gets an `11-qa/` or `11.5-post-launch/` folder
unless someone starts it. Nothing in the framework starts it automatically. This skill is that trigger.

Use it when: the user names an engagement and a stage ("start SG11 for the Itzel site"); or asks
which engagements are due for QA / launch discovery setup; or a site went live without SG11.
It does **not** build the site, run the QA itself, or publish anything.

Read as needed, don't front-load: the target stage's chapter in `../WEF-v1.0/Core-Methodology/`
(SG11 and SG11.5: `07-QA-Optimization.md`, Sec. 10.1 for Search Discovery & Local Presence Setup);
`08-AI-Workflows.md` Sec. 2.6 (Handoff File and Action Items Sheet cadence);
`09-Reusable-Templates.md` Sec. 21.3 (stage `CONTEXT.md`).

## Mode A: sweep (read-only, always safe)

Ask for, or discover, the folder(s) that hold engagement KBs (sibling directories with an `AGENTS.md`
and `_config/`). For each one report, without changing anything:

| Column | How |
|---|---|
| Stage folders present | list `0*`, `10*`, `11*`, `12*` folders; note non-standard names (for example `10-build`, `11-scope-addendum`) |
| Furthest approved stage | `_config/Stage-Ledger.md` if present; else the furthest folder whose `output/` holds its Required Documents |
| Live? | the URL in the Charter or `AGENTS.md`; fetch it once (HTTP status, indexable or `noindex`) |
| Missing | `11-qa/`, `11.5-post-launch/`, `HANDOFF.md`, Action Items Sheet link, Stage Ledger, `90-audits/`, `91-addenda/`, `92-handoffs/` |
| Misplaced | audit reports, scope addenda or old handoffs sitting in stage folders, `_config/`, `assets/` or under non-standard numbers (for example `11-scope-addendum`, `12-audit-results`); list them with the proposed destination, move nothing |
| Recommended next | the lowest stage that should be started (usually SG11 if live or staging-complete) |

Output a single table and stop. Do not create anything in sweep mode. Non-WEF layouts (no stage
folders, for example a proposal plus `build/`) are reported as "non-standard; map before starting".

## Mode B: start one stage in one engagement

### Step 0: confirm target and read state
Resolve the KB path and the target stage (default: the next stage after the furthest closed one).
Read `AGENTS.md`, `CONTEXT.md`, `HANDOFF.md` if present, `_config/Decision-Register.md` (tail),
and the Stage Ledger. If the stage folder already exists, resume from its `CONTEXT.md` instead.

### Step 1: Stage Transition Check on the previous gate
For the gate before the target, compare the chapter's **Required Documents** list with the files
that actually exist. Produce a short table: document, present, version. Rules:
- Missing documents do not block the start; they become **recorded exceptions** (a Decision Register
  entry `DEC-<stage>-0xx` and a Stage Ledger note), because many live builds skipped paper documents.
- A site that is already live starts SG11 as a **retroactive QA**: say so in the ledger.
- Never mark the previous gate "closed" on its behalf; record "closed by exception" only with the
  Engagement Lead's explicit approval in this session.

### Step 2: create the stage folder from the template
Create `11-qa/` (or the target) with `CONTEXT.md` (purpose, inputs, outputs, Required Documents, exit
criteria linked to the chapter, not restated) and `output/`. For SG11.5 also create
`output/Search-Discovery-Setup-Record.md` as a skeleton from Sec. 10.1 (nine numbered items, each with
owner, status, date). For SG11 create an empty `Issue-Log.md` and `Go-Live-Recommendation.md` skeleton
only if the site is not yet live.

### Step 2b: add the non-gate containers
If `90-audits/`, `91-addenda/` or `92-handoffs/` are missing, create each with its `README.md` from `assets/templates/engagement-KB/`. These are containers, not Stage Gates. Moving existing files into them is a separate step that needs the user's go-ahead; propose the moves, with the Decision Register entry for any renamed folder.

### Step 3: record it
- Append to `_config/Stage-Ledger.md` (create it from the ledger header in the engagement's own
  format if missing): date, stage, status `In progress`, trigger (`start-stage`), and the transition
  exceptions.
- Update `AGENTS.md` Current State (one sentence) and `CONTEXT.md` stage map.
- Refresh `HANDOFF.md` (create from `assets/templates/engagement-KB/HANDOFF.md` if missing).

### Step 4: queue what only the client can do
Add Action Items Sheet entries (use the `action-items-sheet` skill; create the sheet if the engagement
has none) for the owner-only steps: search-engine property ownership and verification, local business
profile name/address/owner account, DBA status, tracked-keyword approval, analytics property, hours.
Items are phrased so the owner can answer without opening another file. Link the sheet in `AGENTS.md`.

### Step 5: report
Tell the user: what was created, the transition exceptions, which items were queued, and the first
three actions for the build team. Do not begin the QA or the setup in the same step unless asked.

## Rules
- One engagement per run; sweeps are the only multi-engagement operation.
- Never create client accounts, enter credentials, accept terms, publish, or submit forms as part of
  starting a stage.
- Never commit or push; leave the changes in the working tree and say so.
- If the engagement keeps non-standard folder names, use its names and note the mapping in `CONTEXT.md`
  rather than renaming.
