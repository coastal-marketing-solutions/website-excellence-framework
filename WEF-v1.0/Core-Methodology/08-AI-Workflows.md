# CORE METHODOLOGY — AI WORKFLOWS

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

AI Workflows is the discipline that makes the rest of this framework AI-collaborable in practice, not just in principle. It consolidates the LLM Handoff Protocol, the multi-model collaboration patterns used across a multi-week engagement, the master Prompt Library index, and the AI output verification standards that apply at every Stage Gate. Every other Core Methodology chapter references this one; this chapter does not reference a specific Stage Gate, because it governs *how* AI is used at all of them, in any industry.

---

## 1. Purpose of a Dedicated AI Workflows Discipline

WEF engagements assume that different Stage Gates may be executed with the assistance of different AI models — for example, a research-oriented model for Discovery through Strategic Direction, a design-oriented model for the Design discipline, and a code-generation-oriented model for the Development discipline's build gates. Left ungoverned, this creates two failure modes: **context loss** (a new model instance doesn't know what was already decided) and **specification drift** (a second model's paraphrase of a first model's output subtly changes meaning). This chapter exists to prevent both, identically regardless of which Industry Module is active.

---

## 2. The LLM Handoff Protocol

### 2.1 The Five-Layer Context Package

Every AI model handoff must include, in this order:

1. **Charter Layer** — Project Charter in full, including the named active Industry Module(s). Establishes non-negotiable business objectives, regulatory/professional-standards constraints, and decision authority.
2. **History Layer** — Decision Register entries relevant to the task at hand, filtered by Stage Gate tag. Establishes what has already been decided and why, so the model does not re-litigate settled questions.
3. **State Layer** — Current Master Website Blueprint. Establishes the present factual state of the site's architecture, design, and content.
4. **Module Layer** — The relevant section(s) of the **active Industry Module**, per that Stage Gate's Module Injection Point(s). This is the layer that did not exist in a single-industry framework and is what allows the same Core Methodology prompts to produce correct, vertical-appropriate output.
5. **Task Layer** — The specific Core Methodology Stage Gate chapter, including its Prompt(s) subsection, plus any specific human instruction for the current task.

### 2.2 Handoff Checklist

- [ ] Charter Layer attached and current (no unresolved Charter Change Requests pending)
- [ ] History Layer filtered to relevant Decision Register entries — not the entire register, to preserve context window budget, but never omitted
- [ ] State Layer confirmed as the latest approved Blueprint version
- [ ] Module Layer includes the exact Industry Module section(s) this Stage Gate's Module Injection Point calls for — never omitted, and never a human's summary of the Module in place of its actual text
- [ ] Task Layer includes exact Stage Gate chapter and explicit deliverable expected
- [ ] Human AI Orchestrator reviews model output against the Stage Gate's Quality Assurance criteria before it is logged as a deliverable
- [ ] Any AI-proposed deviation from a prior Decision Register entry, or from the active Industry Module, is flagged explicitly to the human Engagement Lead, not silently applied

### 2.3 Model-to-Model Consistency Rule

When a second AI model picks up work from a first (e.g., a build-oriented model implementing a design-oriented model's output), the receiving model must be given the *producing* model's actual output as State Layer — never a human's paraphrase of it. Paraphrasing across handoffs is the single largest source of specification drift observed across WEF pilot engagements, in every industry tested.

### 2.4 Human-in-the-Loop Requirement

No AI-produced deliverable exits a Stage Gate without human review against that gate's exit criteria. The LLM Handoff Protocol accelerates production; it does not remove the human quality gate defined in each Stage Gate's "Review Process" subsection.

---

## 3. Multi-Model Collaboration Patterns

### 3.1 Typical Model Role Assignment

While any single capable model can run the entire methodology, engagements at scale often assign different models (or different configurations of the same model family) to different disciplines, matched to their comparative strength:

| Discipline | Typical Model Emphasis |
|---|---|
| Research | Synthesis and pattern-extraction from large unstructured inputs (interview notes, analytics exports) |
| SEO & Architecture | Structured reasoning over keyword/taxonomy relationships |
| UX & Conversion | Flow logic and friction analysis |
| Design | Visual/structural specification (paired with a human Visual Designer — this discipline is never fully autonomous) |
| Development | Code/markup generation against a precise specification |
| QA & Optimization | Structured test-plan generation and triage |
| AI Workflows (this chapter) | Orchestration — often the Engagement Lead or AI Orchestrator's own working model, used to assemble Handoff Protocol packages |

### 3.2 Handoff Sequencing Diagram

```
 Research Model            Design Model              Build Model
 (SG1-SG3)                 (SG7-SG7.5)               (SG10-SG10.5)
      │                          │                          │
      ▼                          ▼                          ▼
 [Charter + History         [Charter + History         [Charter + History
  + State + Module           + State + Module           + State + Module
  + Task layers]             + Task layers,              + Task layers,
      │                       INCLUDING the               INCLUDING the
      │                       Research Model's             Design Model's
      │                       actual SG1-SG3               actual SG7.5
      │                       output as State]             output as State]
      ▼                          ▼                          ▼
  Human review              Human review                Human review
  against SG1-SG3           against SG7/7.5             against SG10/10.5
  exit criteria              exit criteria                exit criteria
      │                          │                          │
      └──────────────────────────┴──────────────────────────┘
                     Decision Register updated at every handoff
```

### 3.3 Common Mistakes

- Re-prompting a fresh model instance mid-engagement without the History and Module Layers, causing it to silently contradict earlier decisions or apply the wrong vertical's assumptions.
- Treating AI output as final without the human review step required in every Stage Gate chapter.
- Allowing context window pressure to justify dropping the Charter or Module Layer — regulatory/professional-standards constraints must never be summarized away.
- Switching Industry Modules mid-engagement (e.g., correcting an initial misclassification) without re-running every Module Injection Point already executed under the wrong Module.

---

## 4. Prompt Library — Master Index

All Stage Gate prompts across the Core Methodology are indexed here by number for quick lookup. This index is additive — the authoritative prompt text lives in its originating Stage Gate chapter. Every prompt in this library is written generically, with `[Industry Module name]` and Module-content placeholders, so the identical prompt template produces correct, vertical-specific output for any active Module.

| Prompt ID | Chapter | Stage Gate | Purpose |
|---|---|---|---|
| 1.1 | Research | SG1 | Persona Synthesis |
| 1.2 | Research | SG1 | Current-State Digital Audit Synthesis |
| 2.1 | Research | SG2 | Competitor Scoring |
| 2.2 | Research | SG2 | White Space Synthesis |
| 3.1 | Research | SG3 | Positioning Candidate Generation |
| 3.2 | Research | SG3 | Messaging Pillar Development |
| 4.1 | SEO & Architecture | SG4 | Sitemap Generation |
| 4.2 | SEO & Architecture | SG4 | URL Structure Standard |
| 5.1 | SEO & Architecture | SG5 | Keyword-to-Page Mapping |
| 5.2 | SEO & Architecture | SG5 | Topical Cluster Model |
| 5.3 | SEO & Architecture | SG5 | Schema Markup Plan |
| 6.1 | UX & Conversion | SG6 | Conversion Flow Design |
| 6.2 | UX & Conversion | SG6 | Calculator/Tool Specification |
| 7.1 | Design | SG7 | Design System Foundation |
| 7.2 | Design | SG7 | Component Library Specification |
| 7.5.1 | Design | SG7.5 | Design Tournament Scorecard Generation |
| 7.5.2 | Design | SG7.5 | Future-Proofing Stress Test |
| 8.1 | Development | SG8 | Page Content Brief Generation |
| 8.2 | Development | SG8 | Compliance Content Checklist |
| 9.1 | Development | SG9 | Page Copywriting |
| 9.2 | Development | SG9 | Meta Title/Description Generation |
| 10.1 | Development | SG10 | Build Manifest Generation |
| 10.2 | Development | SG10 | Component-to-Pattern Mapping |
| 10.5.1 | Development | SG10.5 | Build Execution (Code-Generation Model) |
| 10.5.2 | Development | SG10.5 | Performance Configuration Review |
| 11.1 | QA & Optimization | SG11 | QA Test Plan Generation |
| 11.2 | QA & Optimization | SG11 | Issue Log Triage |
| 11.5.1 | QA & Optimization | SG11.5 | Growth Program Prioritization |
| 11.5.2 | QA & Optimization | SG11.5 | Retrospective & Methodology Learnings |

**Prompt Discipline Standard:** Every prompt used in an engagement must (1) name the client, active Industry Module, and role explicitly, (2) attach the relevant Knowledge Base documents and Module sections rather than relying on the model's memory of prior conversation turns, (3) include an explicit instruction against fabricating statistics, credentials, or claims, and (4) be logged (which prompt ID, which model, which date) if its output becomes a Knowledge Base deliverable.

---

## 5. AI Output Verification Standards

### 5.1 The Three Verification Checks

Every AI-produced deliverable, before being logged as final in the Knowledge Base, must pass three checks:

1. **Groundedness Check** — Is every factual claim traceable to an attached source document, or explicitly labeled `[inference]` / `[unverified estimate]`? Ungrounded factual claims (fabricated statistics, invented testimonials, invented credentials) are an automatic fail, in any industry.
2. **Module Consistency Check** — Does the output correctly reflect the active Industry Module's relevant section(s), rather than generic or wrong-vertical assumptions? This check specifically catches cases where a model trained mostly on one vertical's patterns (e.g., defaulting to mortgage-lending assumptions because they are common in training data) leaks into a different Module's engagement.
3. **Compliance Flag Check** — Does the output correctly flag claim-risk language for Compliance/Standards Liaison review, per Development discipline standards, rather than asserting it as fact?

### 5.2 Verification Ownership

The AI Orchestrator performs all three checks before handing output to the Stage Gate's Responsible Role for their own Review Process (as defined in each Stage Gate chapter). This is an additive check, not a replacement for the Stage Gate's own Review Process.

### 5.3 Common Mistakes

- Accepting AI output that "sounds right" without tracing specific claims back to source documents.
- Skipping the Module Consistency Check on the assumption that "the prompt named the right Module, so the output must be correct" — models can and do default to more common patterns even when correctly instructed.
- Treating AI-flagged compliance language as already resolved rather than as a flag for actual human compliance review.

---

*End of AI Workflows. Continue to Core Methodology — Reusable Templates.*
