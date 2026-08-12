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

### 2.5 Context Window Loading Discipline

Sections 2.1–2.4 define *what* the Five-Layer Context Package contains. This subsection defines *when* each layer should actually be loaded into a working context window — a distinct question the Package's contents alone don't answer, and the most common way a technically-correct handoff still degrades in practice. Adopted from the ICM context-management methodology (external reference material; see Governance Sec. 5.2.1 for the parallel Knowledge Base folder-layer adoption, and Sec. 13.2 for the Change Proposal record).

**Not every layer loads at the same time.** The Charter Layer and a filtered slice of the History Layer are near-constant (comparable to Governance Sec. 5.2.1's L0/L1). The Module Layer and Task Layer are loaded per Stage Gate, not once for the whole engagement (comparable to L2). Reference material *within* the Module or Task layers that doesn't change across an engagement (a Module's Regulatory Landscape section, a locked Design Constraints Package) behaves like L3; State-Layer material specific to the current run (the live Master Website Blueprint, the specific deliverable being produced) behaves like L4.

**Practical rules:**

1. **Separate reference from source explicitly.** When a handoff package mixes stable reference material (an Industry Module section, a locked brand guideline) with source material meant to be transformed (a client's raw interview notes, a draft to be revised), label them: "REFERENCE (constraints, do not transform):" vs. "SOURCE (transform this into the output):". A model given both undifferentiated sometimes treats reference material as content to rewrite, or source content as a rule to follow — this is the single most common Groundedness/Module-Consistency failure this labeling prevents (see Sec. 5.1).
2. **Front-load what matters most.** Attention degrades toward the middle of a long context window. Put the Charter Layer's non-negotiable constraints and the current Task Layer instruction at the beginning of a handoff, not buried after several attached documents.
3. **Filter the History Layer deliberately, every time — never omit it, never load it whole.** Sec. 2.2 already requires filtering History to relevant Decision Register entries; the rule here is the failure mode on the *other* side — a filtered-to-nothing History Layer is as dangerous as an unfiltered one, since it re-opens settled decisions as if for the first time.
4. **Use the Knowledge Base as external memory, not the conversation.** Per Governance Sec. 5.2.1, a well-structured KB lets a model read what it needs, when it needs it, rather than everything being pasted into one long-running conversation. If a single working session has accumulated more than roughly 10–15 exchanges of unrelated back-and-forth, and the next task is a genuinely new Stage Gate or a new client, start a fresh session pointed at that stage's `CONTEXT.md` rather than continuing in an increasingly noisy one.
5. **A rough token budget**, useful as a sanity check rather than a hard rule: routing layers (Charter + filtered History + Task) ≈10–15% of the context budget; stable reference (Module sections, Design Constraints Package, brand/voice guidelines) ≈20–30%; source/state material specific to this run (Blueprint, draft content, client-supplied files) ≈30–40%; the remainder reserved for the model's own output and reasoning. If reference material alone is consuming the majority of a handoff's budget, split it or point the model at only the specific Module section this Stage Gate's Module Injection Point actually calls for (AI Workflows Sec. 2.1 Item 4), not the Module's full text.

**Session-to-session consistency:** because a new session has no memory of a prior one, any consistency an engagement has achieved (a settled voice, a settled set of constraints) exists only in what's written down — the Charter, the Decision Register, a Module section, a locked Design Constraints Package — not in the model's memory of having produced it before. Treat "the model got this right last time" as a reason to *write the rule down* in the appropriate L2/L3 file, not as a reason to skip writing it down.

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
- Automating a working handoff pattern before it scales — automation (a task running without human involvement) and scaling (capacity increasing without proportional effort) are not the same thing, and an automated handoff that skips Sec. 2.4's human-in-the-loop requirement to move faster is a compliance/quality risk, not an efficiency gain.
- Building a KB structure or handoff pattern that only the person who built it can navigate — Sec. 5.2.1's CLAUDE.md/CONTEXT.md layer exists specifically so a different consultant, a client, or a future AI session can pick up an engagement without the departed team member's undocumented mental model.

### 3.4 Named AI Tool Roster by Discipline

Sections 3.1–3.3 describe *roles* ("Design Model," "Build Model") generically so this chapter stays platform-independent as tools change. This section names the actual products the roster currently maps to, so an engagement doesn't have to reinvent tool selection at every Stage Gate. Update this table (via Change Request, Sec. 13.2) as the tooling landscape shifts — it is expected to change faster than the rest of this chapter.

| Discipline / Stage Gate | Role | Current Tool(s) |
|---|---|---|
| Design (SG7/SG7.5) | Visual/structural design generation | **Claude Design** — primary/default for this framework. Other tools an engagement may use instead of, or as additional tournament candidates alongside, Claude Design: **OpenAI Design** (ChatGPT/GPT design-canvas output), **Figma** (Figma Design, plus its AI-assisted modes — e.g., Figma Make/Figma AI — for from-prompt generation), **Canva** (Canva AI / Magic Design, useful particularly for brand-guideline-constrained candidates and rapid on-brand variation), **Adobe Express / Firefly** (Adobe's generative design tooling, strong for asset-heavy or print-adjacent brand systems), and the same SG10 roster below (v0, Lovable, Bolt, Framer AI, Uizard, Relume) where a tool's output is fidelity-appropriate for a tournament candidate rather than only a build target. Used to produce the actual rendered mockup candidates for the Design Tournament (Sec. 10.1, Design chapter), not just the written Design System Specification. A written spec alone does not satisfy SG7's Required Documents — an actual AI-tool design pass is required before SG7.5 (Governance, Sec. 15.4, RETRO-001) |
| Development / AI Build Package (SG10) | Platform-specific build-prompt generation | Claude Design, OpenAI Design, v0, Lovable, Bolt, Figma AI, Replit, Webflow AI, Framer AI, Uizard, Relume — SG10's Build Manifest is written as a **Universal Prompt** (platform-agnostic, minimum ~500 words) first, then adapted per platform actually in use on the engagement. Not every platform is used on every engagement; the Universal Prompt is the one deliverable that is always produced |
| Development / WordPress Implementation (SG10.5) | Code-generation against the approved default (or Charter-specified) stack | **Claude Code, Codex, Manus, GitHub Copilot**, or an equivalent AI coding agent, executing directly against GeneratePress/GenerateBlocks (or the Charter-confirmed alternative stack, Governance Sec. 13.4.1). Every such agent must be given the **Design Constraints Package** (Design, Appendix) as loaded context before it touches design or markup — at initial build and at every post-launch AI-assisted edit thereafter |

**Rule:** The Design discipline's AI-tool pass (Claude Design or another tool from the roster above) must produce real candidate output before SG7.5's Design Tournament — a written specification describing what the design *would* look like is not a substitute and does not satisfy Design's Exit Criteria (Sec. 05, Sec. 18). Which specific tool(s) are used is an engagement-level choice (log it as a Decision Register entry, same discipline as the technology-stack choice in Governance Sec. 13.4.1) — Claude Design is this framework's default recommendation, not a mandate.

**The Design Constraints Package is the handoff artifact between the two rows above.** It is what lets an AI design tool's output (Claude Design, OpenAI Design, Figma, Canva, Adobe Express/Firefly) be implemented correctly by an AI coding agent (Claude Code, Codex, Manus, GitHub Copilot) regardless of which specific tools were used on either side, and regardless of which technology stack the Charter confirmed (Governance, Sec. 13.4.1) — including a non-WordPress build such as a custom PHP/HTML site. See Design, Appendix — Design Constraints Package Specification for full contents and the governance rule requiring it as context for every downstream AI task.

**Before either row above does net-new work, check the firm-wide Component Library (`/Component-Library/`, Design Sec. 9.5).** A large share of what an AI design tool would otherwise invent from scratch, and what an AI coding agent would otherwise have to reverse-engineer how to build, is already specified there — component interface, design-token dependencies, platform implementation notes, and known working implementations — from prior engagements. Point any AI design or coding tool at the relevant Component Library entry by ID before asking it to design or build a component type this firm has already solved.

**Tool roster currency:** This list is expected to change faster than any other part of this chapter. Update it via Change Request (Governance, Sec. 13.2) whenever a materially new AI design or build tool becomes relevant to engagement work, rather than letting the roster go stale.

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
