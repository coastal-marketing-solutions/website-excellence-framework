# {Client Name} Website Blueprint

## What This Is
{One to two sentences: who the client is, what this engagement is, which WEF Industry Module(s) govern it (Governance Sec. 1.4/1.5).}

## Current State
**Active stage: 01-research (WEF Stage Gate 1 — Discovery & Market Research).** {One sentence on where things stand.} See `CONTEXT.md` for the full stage map.

## Structure
```
{Client Name} Website Blueprint/
  AGENTS.md              # You are here.
  CONTEXT.md              # Full WEF Stage Gate map.
  HANDOFF.md              # Resume point; refresh per AI Workflows Sec. 2.6.
  90-audits/              # Not a Stage Gate: dated audit reports of any kind (index in README.md).
  91-addenda/             # Not a Stage Gate: scope addenda, one folder each.
  92-handoffs/            # Not a Stage Gate: superseded handoffs and sheet snapshots.
  01-research/            # SG1 — the only stage folder that exists at initialization.
    CONTEXT.md
    01-WEF-Intake.md      # Client-supplied intake (from the `intake` skill).
    output/
  _config/                # Charter, Decision Register, and other cross-stage governance docs.
  _references/            # Pointers to the WEF framework and active Industry Module(s).
  blueprint/              # Master Website Blueprint (fills in as Stage Gates close).
```

## How to Use
1. Read this file first, then `CONTEXT.md` for the full stage map.
2. Go to the active stage's `CONTEXT.md` before touching its `output/`.
3. Read `_config/Project-Charter.md` and `_config/Decision-Register.md` before starting any new stage's work.
4. Only create the next stage folder when that stage actually begins (Governance Sec. 5.2.1 Rule 2).
5. Every new decision goes in `_config/Decision-Register.md`.
6. Anything discovered here that looks like a reusable framework improvement goes in `_config/WEF-Candidate-Findings.md`.

## Action items sheet
{Link to the `<domain> – Action Items Sheet` once created. Every question or approval for the client lives there, never only in chat or in the handoff. Process answers with the `action-items-sheet` skill or the equivalent; act only on answered, non-skipped items.}

## Audits, addenda and handoff history
The `90-`, `91-` and `92-` folders are containers, not Stage Gates, and exist from the start (Governance Sec. 5.2.1 Rule 2 applies only to numbered gate folders). File every audit in `90-audits/`, every scope addendum in `91-addenda/`, and move superseded handoffs to `92-handoffs/`.

## Handoff cadence
`HANDOFF.md` is refreshed at the end of every session, at every Stage Gate close, after every batch of live-site changes, and before any go-live action (AI Workflows Sec. 2.6). The client receives the sheet link at least weekly while the build is active.

## Layer Annotations (ICM)
- `AGENTS.md`: L0 (always loaded, orientation)
- `CONTEXT.md`: L1 (stage-gate routing)
- Stage `CONTEXT.md` files: L2 (stage contracts)
- `_config/` files: L3 (engagement-specific reference)
- `_references/` files: L3 (domain reference — the WEF framework itself)
- Stage `output/` and client-supplied source material: L4 (working artifacts)
