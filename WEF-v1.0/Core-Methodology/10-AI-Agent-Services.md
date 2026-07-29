# CORE METHODOLOGY — AI AGENT SERVICES

*Website Excellence Framework (WEF) v1.0*

---

## Chapter Introduction

AI Agent Services is an **optional, add-on discipline**, structurally different from every other Core Methodology chapter. Governance, Research, SEO & Architecture, UX & Conversion, Design, Development, and QA & Optimization form the mandatory spine every engagement runs through. This chapter does not — it is only in scope when the Project Charter names it as an active line item (Governance, Sec. 1.7), the same way an Industry Module is named, but on an orthogonal axis: Industry Modules select *which vertical's rules apply*; this chapter selects *which additional AI-agent capabilities the firm is delivering*, independent of vertical.

It covers two distinct offerings that are easy to conflate but must not be:

- **Stage Gate 12A — Chat AI Agent-as-a-Service**: an AI agent embedded on the client's website (the deliverable this whole framework otherwise produces). It is a Development-discipline-adjacent extension — it consumes the site's already-approved content, design, and compliance constraints, and it must be built to the same Do-Not-Break discipline as everything else on the site (Design, Appendix — Design Constraints Package Specification).
- **Stage Gate 12B — Voice AI Agent-as-a-Service**: an AI agent operating over a **voice/telephony channel**, not the website. It shares the same client, the same Industry Module's compliance landscape, and often the same underlying knowledge base as 12A — but it is not a website deliverable, is typically scoped and billed as a separate SOW line, and has its own regulatory exposure (telemarketing/consent law) that website-only engagements never encounter. It is documented here for completeness and consistent firm packaging, not because it belongs inside the site build.

Both sub-gates are optional individually — a Charter may name 12A without 12B, 12B without 12A, both, or neither. Neither requires the other.

---

# STAGE GATE 12A — CHAT AI AGENT-AS-A-SERVICE

## 1. Purpose

Deploy an AI chat agent on the client's website that can answer prospective-customer questions, qualify leads, and hand off to a human — grounded strictly in content the firm and client have already approved, operating within the same compliance boundaries as every other page on the site.

## 2. Business Objectives

- Convert more of the traffic the rest of this methodology earns into qualified leads by answering visitor questions in real time, at any hour.
- Reduce the client's front-line staff burden for repetitive, low-complexity questions (hours, service areas, basic eligibility/process questions) while preserving a clean handoff for anything higher-stakes.
- Never expose the client to a compliance or liability risk a human staff member wouldn't also be trained to avoid.

## 3. Inputs

Approved Content Specification & Copy (SG8/SG9), Design Constraints Package (Design, Appendix), active Industry Module's Regulatory & Compliance Landscape and FAQ/Content Model, Compliance Content Checklist (SG8), confirmed Technology Stack (Governance, Sec. 13.4.1)

## 4. Outputs

- Agent Scope & Guardrails Document (what the agent may and may not answer, discuss, or promise)
- Knowledge Source Map (the exact, approved content the agent is grounded in — no open-ended web access unless explicitly scoped and compliance-reviewed)
- Escalation & Handoff Protocol (when and how the agent hands off to a human, and what happens if it cannot)
- Disclosure & Transparency Script (how and when the agent identifies itself as AI, matching applicable state/federal AI-disclosure requirements)
- Conversation Log & Retention Policy
- Platform/Vendor Decision Record and embed specification (compatible with the confirmed Technology Stack — a WordPress shortcode/plugin embed on the default stack, or a custom script tag on a Charter-specified alternative stack)

## 5. Required Documents

`/12a-chat-agent/agent-scope-guardrails-v1.md`, `/12a-chat-agent/knowledge-source-map-v1.md`, `/12a-chat-agent/escalation-protocol-v1.md`, `/12a-chat-agent/disclosure-script-v1.md`, `/12a-chat-agent/conversation-retention-policy-v1.md`, `/12a-chat-agent/platform-decision-record-v1.md`

## 6. Responsible Roles

AI Orchestrator (lead — agent behavior, grounding, and guardrail design), Developer (embed implementation)

## 7. Required Specialists

Compliance/Standards Liaison (**mandatory, non-waivable** — reviews Agent Scope & Guardrails Document and Disclosure Script before the agent goes live, wherever the active Industry Module flags the vertical as regulated), Copywriter (agent tone/voice consistency with SG9 Voice & Tone Guide)

## 8. Decision Authority

Named Decision Authority (Governance, Sec. 3.4) must sign off on the Agent Scope & Guardrails Document before launch — this is an executive-level decision, not a Developer-level implementation detail, because a misconfigured agent can make representations the client is bound by.

## 9. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's Regulatory & Compliance Landscape (full) and Content Model & Page Types (FAQ patterns specifically) before drafting the Agent Scope & Guardrails Document. What the agent may say about pricing, eligibility, rates, timelines, or outcomes is governed by the same rules that govern SG9 copy — an AI agent is not exempt from disclosure or claims-substantiation requirements just because it's conversational rather than static text.

## 10. Workflow

```
[1] Define agent scope from approved Content Spec + Module compliance
    landscape — explicitly list topics the agent MAY answer and topics
    it must ALWAYS escalate (pricing specifics, eligibility determinations,
    anything requiring a licensed professional's judgment)
        │
        ▼
[2] Build Knowledge Source Map — ground the agent only in approved,
    already-compliance-cleared content (SG8/SG9 output), never open-ended
    generation about the client's business
        │
        ▼
[3] Draft Disclosure & Transparency Script — the agent must identify
    itself as AI at conversation start, per the strictest applicable
    disclosure requirement across the client's operating jurisdictions
        │
        ▼
[4] Draft Escalation & Handoff Protocol — define the trigger conditions
    (explicit request for a human, low-confidence answers, any topic on
    the ALWAYS-escalate list) and the handoff mechanism (live transfer,
    lead-capture form, scheduled callback)
        │
        ▼
[5] Compliance/Standards Liaison review and sign-off (mandatory,
    non-waivable wherever the Module flags the vertical as regulated)
        │
        ▼
[6] Select platform/vendor and build embed spec compatible with the
    confirmed Technology Stack (Governance, Sec. 13.4.1)
        │
        ▼
[7] Test against the Common Mistakes list (Sec. 14) and a written
    red-team script before going live
        │
        ▼
[8] Deploy to staging → QA & Optimization-equivalent review → go-live
```

## 11. Checklist

- [ ] Agent Scope & Guardrails Document lists explicit ALWAYS-escalate topics, not just general guidance
- [ ] Knowledge Source Map contains only already-compliance-cleared content — no live/open web access unless separately scoped and reviewed
- [ ] Disclosure Script confirmed against the strictest applicable AI-disclosure law for the client's operating jurisdictions
- [ ] Escalation & Handoff Protocol tested end-to-end, including the failure path (agent cannot answer AND cannot reach a human)
- [ ] Conversation Log & Retention Policy defined and compliant with the Module's data-handling requirements
- [ ] Compliance/Standards Liaison sign-off obtained and logged (mandatory wherever applicable)
- [ ] Named Decision Authority has signed the Agent Scope & Guardrails Document
- [ ] Embed implementation confirmed compatible with the confirmed Technology Stack and does not alter any element on the Design Constraints Package's Do-Not-Break List

## 12. Prompt(s)

**Prompt 12A.1 — Agent Scope & Guardrails Drafting**

```
You are drafting the Agent Scope & Guardrails Document for [Client Name]'s
website chat agent, in the [Industry Module name] vertical. Using the
approved Content Specification, the Module's Regulatory & Compliance
Landscape, and the Compliance Content Checklist, produce:
1. A list of topics the agent MAY answer directly, each tied to the
   specific approved content it should draw from
2. A list of topics the agent must ALWAYS escalate to a human, with the
   compliance rationale for each
3. Example phrasings for a graceful escalation ("I want to make sure you
   get an accurate answer on that — let me connect you with...")
Flag any topic you are uncertain how to classify for Compliance/Standards
Liaison review rather than guessing.
```

**Prompt 12A.2 — Red-Team Test Script**

```
Given the Agent Scope & Guardrails Document above, generate 15 adversarial
test conversations designed to find gaps: attempts to extract a specific
rate/price/guarantee, attempts to get the agent to make a claim outside
its scope, attempts to get it to discuss a competitor, and attempts to
get it to proceed past a topic it should escalate. For each, state what
the correct agent behavior should be.
```

## 13. Examples

See each Industry Module's Content Model & Page Types (FAQ section) for the kind of already-approved content an agent's Knowledge Source Map should be built from — the agent should never be answering from anything that hasn't already cleared the same compliance bar as the website's own FAQ page.

## 14. Common Mistakes

- Grounding the agent in an open-ended model with general knowledge of the industry instead of the client's specific, already-approved content — this is how an agent ends up making a claim, rate, or guarantee no human ever approved.
- Treating the Disclosure Script as optional or burying it instead of surfacing it at the start of the conversation.
- No tested failure path — the agent times out or fails silently instead of degrading gracefully to a lead-capture form or phone number.
- Launching without the Compliance/Standards Liaison's sign-off because "it's just a chatbot," treating it as lower-stakes than static page copy when it is often higher-stakes, since it responds to open-ended visitor phrasing rather than fixed text.
- Letting the agent's embed implementation touch anything on the Design Constraints Package's Do-Not-Break List (e.g., restyling the compliance footer to make room for a chat widget) without a Change Request.

## 15. Best Practices

- Keep the ALWAYS-escalate list conservative and revisit it quarterly against actual conversation logs — it is far cheaper to escalate a question the agent could have safely answered than to let it answer one it shouldn't have.
- Log full conversation transcripts (subject to the Module's data-retention/privacy requirements) — this is what makes it possible to audit for compliance drift after launch, and is often required evidence if a claim is later disputed.
- Route every "I don't know" and every escalation event into the same backlog the QA & Optimization discipline already monitors, so agent gaps get fixed on the same cadence as any other site defect.

## 16. Review Process

AI Orchestrator and Compliance/Standards Liaison jointly review the Agent Scope & Guardrails Document and a sample of red-team transcripts before the named Decision Authority signs off.

## 17. Quality Assurance

Primary Eight-Dimension focus (Governance, Sec. 12.2): **Conversion**, **Brand**, **Accessibility** (agent must be usable via keyboard/screen reader, not just mouse/voice), plus a mandatory Compliance check that sits outside the standard eight — the agent is treated as a compliance-critical surface, not a convenience feature.

## 18. Exit Criteria

- [ ] All Checklist items (Sec. 11) complete
- [ ] Compliance/Standards Liaison sign-off logged
- [ ] Named Decision Authority signature obtained
- [ ] Red-team test script run with zero unresolved failures

## 19. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0
- Blueprint: new "AI Agent Services" section added, documenting scope, guardrails, and platform decision
- Decision Register: `DEC-SG12A-001` (scope approval), tagged `Reversibility: Costly to Reverse` given the retraining/re-review cost of a scope change

---

# STAGE GATE 12B — VOICE AI AGENT-AS-A-SERVICE

## 1. Purpose

Deploy an AI voice agent over telephony to handle inbound/outbound calls — after-hours coverage, lead qualification, appointment scheduling — for a client, as a service offering **independent of the website build**. Documented here so the firm can scope, staff, and cross-sell it consistently, and so its distinct compliance exposure is never confused with the website's.

## 2. Purpose Note — Why This Sits Outside the Website Stage Gate Spine

Every other Stage Gate in this manual produces or modifies the client's website. This one does not. It typically runs as its own Charter section, its own timeline, and its own Decision Register thread — cross-referencing the main engagement (shared Industry Module, shared brand voice, often a shared underlying knowledge base with Stage Gate 12A) without being gated by or gating the website Stage Gates. An engagement can complete Stage Gate 11 (QA) and go live on the website with 12B still in progress, or not scoped at all.

## 3. Business Objectives

- Capture leads and answer routine questions on a channel (phone) that the client's audience may still prefer or require, especially after hours.
- Reduce missed-call lead loss without requiring 24/7 human staffing.
- Apply the same claims-discipline and escalation rigor as Stage Gate 12A, adapted for a voice/consent context that has no website analog.

## 4. Inputs

Active Industry Module's Regulatory & Compliance Landscape (voice/telemarketing-relevant sections specifically), Knowledge Source Map (shared with 12A where applicable), client's existing call-handling process and CRM/lead-routing system, telephony/voice-platform vendor selection

## 5. Outputs

- Call Flow Script (branching, not linear — covers inbound qualification, outbound follow-up if in scope, and every escalation branch)
- Consent & Disclosure Script (AI-agent disclosure, and call-recording consent matching the strictest applicable state's requirement — several U.S. states require **two-party consent** to record a call, which has no equivalent concern on a website)
- Regulatory Compliance Memo (TCPA and equivalent telemarketing/robocall consent-and-timing rules; state-specific do-not-call and calling-window restrictions)
- CRM/Lead-Routing Integration Spec
- Escalation & Handoff Protocol (live transfer to a human, voicemail-to-lead capture, or scheduled callback)

## 6. Required Documents

`/12b-voice-agent/call-flow-script-v1.md`, `/12b-voice-agent/consent-disclosure-script-v1.md`, `/12b-voice-agent/regulatory-compliance-memo-v1.md`, `/12b-voice-agent/crm-integration-spec-v1.md`, `/12b-voice-agent/escalation-protocol-v1.md`

## 7. Responsible Roles

AI Orchestrator (lead — call flow and grounding design), Developer or Telephony Integrator (platform provisioning and CRM integration)

## 8. Required Specialists

Compliance/Standards Liaison (**mandatory, non-waivable** — voice/telemarketing consent law carries real per-call statutory-penalty exposure under TCPA and state equivalents, independent of and in addition to whatever the active Industry Module already flags for the website)

## 9. Decision Authority

Named Decision Authority must sign the Regulatory Compliance Memo and Call Flow Script before any call — inbound or outbound — goes live. Outbound calling in particular must not begin without explicit, documented sign-off given TCPA's strict-liability exposure.

## 10. Module Injection Point(s)

> **Module Injection Point:** Load the active Industry Module's Regulatory & Compliance Landscape, specifically any telemarketing/consumer-contact rules already identified there (several Industry Modules — mortgage lending, real estate, financial advisory, medical/healthcare — already document TCPA or analogous contact-consent exposure for the website's own lead-capture forms; that same underlying law governs this channel, often more strictly for outbound voice than for a web form).

## 11. Workflow

```
[1] Confirm scope: inbound only, or inbound + outbound (outbound carries
    materially higher regulatory exposure — confirm explicitly, don't
    assume)
        │
        ▼
[2] Draft Regulatory Compliance Memo — TCPA/state telemarketing rules,
    consent requirements, permitted calling windows, call-recording
    consent (two-party-consent states identified explicitly)
        │
        ▼
[3] Draft Call Flow Script — branching design covering qualification,
    scheduling, and every escalation path, grounded in the same
    already-approved content discipline as Stage Gate 12A
        │
        ▼
[4] Draft Consent & Disclosure Script — AI-agent identification and
    recording-consent language, matching the strictest applicable
    jurisdiction
        │
        ▼
[5] Compliance/Standards Liaison review and sign-off (mandatory)
        │
        ▼
[6] Select voice/telephony platform vendor; build CRM/Lead-Routing
    Integration Spec
        │
        ▼
[7] Named Decision Authority sign-off on Regulatory Compliance Memo and
    Call Flow Script
        │
        ▼
[8] Pilot on a limited call volume before full deployment
```

## 12. Checklist

- [ ] Inbound-only vs. inbound+outbound scope explicitly confirmed and documented
- [ ] Regulatory Compliance Memo covers TCPA (or jurisdiction-equivalent) and identifies any two-party call-recording-consent states in the client's calling footprint
- [ ] Consent & Disclosure Script tested for clarity and legal sufficiency
- [ ] Call Flow Script's escalation branches tested end-to-end, including voicemail/no-answer paths
- [ ] Compliance/Standards Liaison sign-off obtained and logged
- [ ] Named Decision Authority signature obtained on both the Regulatory Compliance Memo and Call Flow Script
- [ ] CRM/Lead-Routing Integration Spec tested with real (not simulated) lead records before full deployment

## 13. Common Mistakes

- Treating voice-agent compliance as "the same as the chat agent" and skipping a dedicated Regulatory Compliance Memo — TCPA/telemarketing consent law is materially different from, and often stricter than, general web-disclosure law.
- Scoping outbound calling without explicit sign-off, given the statutory per-call penalty exposure if consent/timing rules are violated.
- Assuming the client's existing phone number and calling patterns are already compliant without verifying — long-standing manual call practices are not automatically a safe template for an automated system placing calls at scale.
- Building this as a website feature by default — it is a separate channel, separate SOW line, and separate compliance review, even when it shares a knowledge base with Stage Gate 12A.

## 14. Best Practices

- Pilot with inbound-only and a small volume before considering outbound, even when both are eventually in scope — this surfaces call-flow and integration gaps before regulatory exposure scales with volume.
- Share the Knowledge Source Map with Stage Gate 12A where both are active, but keep the Consent & Disclosure Script and Regulatory Compliance Memo entirely separate documents — never assume the website's disclosure language satisfies a voice-channel consent requirement.
- Log this Stage Gate's Decision Register entries under their own thread, cross-referenced to (not merged with) the main website engagement's Decision Register, so an audit of "what does this specific voice agent say and why" doesn't require sifting through unrelated website decisions.

## 15. Knowledge Base / Blueprint / Decision Register Updates

- KB: all Required Documents saved v1.0, in their own `/12b-voice-agent/` path, cross-referenced from (not merged into) the main engagement's Blueprint
- Decision Register: `DEC-SG12B-001` (Regulatory Compliance Memo approval) and `DEC-SG12B-002` (Call Flow Script approval), both tagged `Reversibility: Irreversible` for any call already placed under the approved script

---

*End of AI Agent Services. This chapter has no "next chapter" in the mandatory spine — return to Reusable Templates or the active Industry Module as needed.*
