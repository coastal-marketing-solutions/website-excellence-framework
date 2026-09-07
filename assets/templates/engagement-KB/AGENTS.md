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

## Layer Annotations (ICM)
- `AGENTS.md`: L0 (always loaded, orientation)
- `CONTEXT.md`: L1 (stage-gate routing)
- Stage `CONTEXT.md` files: L2 (stage contracts)
- `_config/` files: L3 (engagement-specific reference)
- `_references/` files: L3 (domain reference — the WEF framework itself)
- Stage `output/` and client-supplied source material: L4 (working artifacts)
