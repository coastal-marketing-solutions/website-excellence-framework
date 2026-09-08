# Governance — 5. Knowledge Base

*Core Methodology — Governance, Sec. 5. Part of [`01-governance/`](CONTEXT.md) — the router for this chapter.*

---

## 5. Knowledge Base

### 5.1 Purpose

The Knowledge Base (KB) is the single persistent store of every artifact, research finding, deliverable, and decision produced during the engagement. It is what makes WEF engagements AI-collaborable and cross-industry-reusable: any model can be given a defined KB path plus the active Industry Module and immediately have full context for the current state of the engagement.

### 5.2 Standard Folder Structure

```
/clients/{client-name}/wef/
├── CLAUDE.md                     (L0 — always-loaded orientation, Sec. 5.2.1)
├── CONTEXT.md                    (L1 — full Stage Gate map, Sec. 5.2.1)
├── 01-research/                  (Stage Gate 1)
│   ├── CONTEXT.md                (L2 — stage contract)
│   └── output/                   (L4 — this stage's deliverables)
├── 02-competitive/               (Stage Gate 2)
│   ├── CONTEXT.md
│   └── output/
├── 03-strategy/                  (Stage Gate 3)
├── 04-architecture/              (Stage Gate 4)
├── 05-seo-blueprint/             (Stage Gate 5)
├── 06-ux-conversion/             (Stage Gate 6)
├── 07-design-system/             (Stage Gate 7)
├── 07.5-prototype-validation/    (Stage Gate 7.5)
├── 08-content-spec/              (Stage Gate 8)
├── 09-copywriting/               (Stage Gate 9)
├── 10-ai-build-package/          (Stage Gate 10)
├── 10.5-wp-implementation/       (Stage Gate 10.5)
├── 11-qa/                        (Stage Gate 11)
├── 11.5-post-launch/             (Stage Gate 11.5)
│                                  (each Stage Gate folder above follows the same
│                                   CONTEXT.md + output/ pattern shown for 01/02;
│                                   create a stage's folder only when that stage
│                                   actually begins — do not scaffold ahead, Sec. 5.2.1)
├── _config/                      (L3 — engagement-specific, stable across every stage)
│   ├── project-charter.md            (names active Industry Module(s))
│   ├── decision-register.md
│   ├── compliance-constraints-log.md
│   ├── open-questions.md
│   ├── assumptions-log.md
│   └── project-backlog.md
├── _references/                  (L3 — domain reference, shared across engagements)
│   └── README.md                     (pointers to the WEF framework + active Industry Module(s))
└── blueprint/
    └── master-website-blueprint.md
```

Note that this per-client structure is unchanged in *intent* from a single-industry framework — the industry-specific knowledge lives in the framework-level `/Industry-Modules/` library, referenced from the Charter, not duplicated into every client's KB folder. What changed in this revision (Sec. 5.2.1) is the addition of an explicit navigation layer on top of the folder structure itself, and the consolidation of the engagement's cross-stage governance documents (Charter, Decision Register, and their siblings) into a single `_config/` location instead of a lone `00-charter/`.

### 5.2.1 The Context Navigation Layer (CLAUDE.md / CONTEXT.md)

The folder structure in Sec. 5.2 organizes *where* things live. It does not, on its own, tell an AI model *when* to load them or *what order* to read them in — and a large, multi-stage engagement KB left without that navigation layer tends to be read either exhaustively (wasting context budget on stages that aren't relevant to the current task) or incompletely (a model guesses which files matter and guesses wrong). This subsection formalizes a five-layer navigation discipline, adopted from the ICM ("context management") methodology (external reference material, first applied to a live WEF engagement 2026-07-30; see Change Proposal history, Sec. 13.2) and merged with the WEF-native Five-Layer Context Package already defined in AI Workflows Sec. 2.1, which it does not replace.

| Layer | File(s) | Loads | Answers |
|---|---|---|---|
| L0 | `CLAUDE.md` (KB root) | Always, every session | "Where am I? What is this engagement?" |
| L1 | `CONTEXT.md` (KB root) | On entry to the KB | "Where do I go? What's the full Stage Gate map and current stage?" |
| L2 | `CONTEXT.md` (each stage folder) | Only when working in that stage | "What does this specific Stage Gate do — purpose, inputs, outputs, exit criteria?" |
| L3 | `_config/*`, `_references/*` | Loaded selectively, per task | "What rules/decisions/framework content apply?" |
| L4 | Stage `output/*`, client-supplied source material | Loaded selectively, per task | "What am I actually working with or producing right now?" |

**Rules:**

1. `CLAUDE.md` stays under roughly one screen (WEF Best Practice: under ~800 tokens). If it grows longer, content belongs in `CONTEXT.md` or a stage's own `CONTEXT.md` instead.
2. A stage folder (and its `CONTEXT.md` + `output/`) is created **only when that Stage Gate actually begins** — per Sec. 5.2's inline note. Scaffolding all 14 stage folders in advance defeats the purpose of the layer (nothing to route to yet) and clutters the KB root.
3. `_config/` holds what's stable **across every stage** of this specific engagement (Charter, Decision Register, Compliance Constraints Log, Open Questions, Assumptions Log, Project Backlog). `_references/` holds what's stable **across engagements** (pointers into the framework-level `/Industry-Modules/` and Core Methodology, not copies of them). Do not duplicate framework content into `_references/` — link to it.
4. Every stage's `CONTEXT.md` is a trimmed, engagement-specific instance of that Stage Gate's 19-part Core Methodology template (Research Sec. "The Fixed Stage Gate Template"), not a restatement of the whole chapter — link back to the chapter for full detail rather than copying it.
5. When a stage completes, its `CONTEXT.md` status updates to reflect completion (see the template in Reusable Templates, Sec. 21.3) and the root `CONTEXT.md`'s Stage Map table updates to name the new active stage — this is a Knowledge Base Governance Rule (Sec. 5.3), not optional housekeeping.

**Rationale for adoption:** the same context-window-degradation failure mode this layer prevents — a model given too much undifferentiated context blending reference material with source material, or re-deriving decisions already settled — is exactly what AI Workflows Sec. 5 (Verification Standards) and Sec. 3.3 (Common Mistakes) already warn against from the opposite direction (verifying bad output after the fact, rather than structuring the KB to make bad output less likely in the first place). This is a structural, not incremental, complement to that existing discipline.

### 5.3 Knowledge Base Governance Rules

1. Every Stage Gate deliverable is saved to its stage's `output/` folder — never to a personal drive, chat log, or email attachment only.
2. File naming follows the Documentation Standard (Section 8.3) and the Naming Convention Standard (Reusable Templates, Sec. 21.4).
3. The Knowledge Base is read-access for the full team and client sponsor; write-access is role-gated per the RACI in Section 2.3.
4. No deliverable is considered final until it exists in the Knowledge Base in its approved form — a Slack message or verbal approval is not sufficient.
5. The root `CLAUDE.md` and `CONTEXT.md` are living documents (Sec. 5.2.1) — update them at every Stage Gate transition, not just at KB creation. A navigation layer that describes a stale state is worse than no navigation layer, because it actively misdirects.

### 5.4 AI Access Pattern

When briefing an AI model for a Stage Gate task, the standard context package is: (1) Project Charter, (2) Decision Register (filtered to relevant Stage Gates), (3) Master Website Blueprint (current state), (4) the specific Core Methodology Stage Gate chapter, (5) the relevant section(s) of the **active Industry Module**, (6) any Stage Gate inputs listed in that chapter. This is formalized in the LLM Handoff Protocol (AI Workflows chapter), and — as of Sec. 5.2.1 — routed through the KB's own CLAUDE.md/CONTEXT.md navigation layer rather than assembled from scratch by a human at every handoff.
