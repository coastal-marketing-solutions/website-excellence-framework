# Governance — 4. Decision Register

*Core Methodology — Governance, Sec. 4. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 4. Decision Register

### 4.1 Purpose

The Decision Register is the append-only ledger of every material decision made during the engagement: what was decided, why, by whom, on what evidence, and what alternatives were rejected. It is the mechanism that lets a consultant (or AI model) joining the engagement mid-stream understand why the sitemap looks the way it does, without re-reading every prior working session — and it is identical in structure across every industry this framework serves.

### 4.2 Decision Register Schema

| Field | Description |
|---|---|
| Decision ID | Sequential, format `DEC-{stage gate}-{sequence}`, e.g., `DEC-SG4-003` |
| Date | Date decided |
| Decision Summary | One-sentence statement of what was decided |
| Rationale | Evidence/reasoning supporting the decision |
| Alternatives Considered | What else was on the table, and why it was rejected |
| Decided By | Named individual(s) |
| Stage Gate | Which Stage Gate this decision belongs to |
| Impacts | Which Blueprint sections, backlog items, or downstream gates this affects |
| Reversibility | Reversible / Costly to Reverse / Irreversible |
| Status | Active / Superseded (with link to superseding Decision ID) |

### 4.3 Governance Rule

Decisions are never deleted, only superseded. If a design decision is later reversed, a new Decision Register entry is created referencing and superseding the original — preserving full engagement history for audit and reuse.

### 4.4 When to Log a Decision

Log a Decision Register entry any time: a strategic direction is chosen among alternatives; a scope boundary is set or changed; a compliance or professional-standards interpretation is applied; a design or architecture pattern is selected over competing options; an Industry Module is selected or blended; or an AI model's recommendation is accepted, modified, or rejected by a human reviewer.

### 4.5 Bias-Scan Step for Irreversible Decisions

Any decision logged with **Reversibility: Irreversible** carries a mandatory one-line bias-scan note before it's marked final: does this decision look right because the evidence supports it, or because it's the option that was easiest to reach, confirms an existing assumption, or matches what every prior similar decision on this engagement already concluded? This is not a philosophical exercise — a real, repeated pattern in this framework's own retrospective findings is every self-generated "lessons learned" entry being marked generalizable to other industries, which is itself a plausible artifact of who's doing the generalizing rather than a property of the findings. The AI Orchestrator or Engagement Lead performs this scan; it does not require a separate named role, but it does require a written note, not a mental check.

### 4.6 Named Trigger Condition for Deferred Tradeoffs

Where a decision explicitly accepts a limitation now in exchange for a cheaper/faster path (a free-tier vendor, a launch-only workaround, a deferred feature), log the **specific future condition** that should trigger revisiting it — not just "revisit later." "Upgrade once monthly traffic exceeds the free API tier's call limit" is checkable; "revisit if it becomes a problem" is not. This is what makes a Costly-to-Reverse decision genuinely reversible in practice rather than reversible in theory but never actually reconsidered.
