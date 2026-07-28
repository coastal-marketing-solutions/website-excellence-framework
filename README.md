# Website Excellence Framework (WEF)

**An open, AI-assisted consulting methodology for designing, building, optimizing, and scaling high-performing websites across regulated and specialized industries.**

This repository publishes the full framework so working practitioners — consultants, agents, brokers, developers, SEO specialists, and compliance professionals across the industries it covers — can review it, challenge it, and improve it.

## What's here

```
WEF-v1.0/
├── 00-Front-Matter.md          Title page, purpose, architecture overview, how to use this
├── 99-Back-Matter.md           Glossary, references, index, appendices
├── Core-Methodology/           Industry-agnostic: the same 9 files apply to every engagement
│   ├── 01-Governance.md
│   ├── 02-Research.md
│   ├── 03-SEO-Architecture.md
│   ├── 04-UX-Conversion.md
│   ├── 05-Design.md
│   ├── 06-Development.md
│   ├── 07-QA-Optimization.md
│   ├── 08-AI-Workflows.md
│   └── 09-Reusable-Templates.md
└── Industry-Modules/           Vertical-specific: pick one (or blend two) per engagement
    ├── 00-Module-Template-and-Index.md
    ├── Module-Mortgage-Lending.md
    ├── Module-Real-Estate.md
    ├── Module-Law-Firm.md
    ├── Module-Medical-Healthcare.md
    ├── Module-Home-Services.md
    ├── Module-Financial-Advisor.md
    ├── Module-SaaS.md
    ├── Module-Cash-Home-Buyer.md
    ├── Module-Distressed-Property-Advocate.md
    ├── Module-Expired-Listings-Commercial.md
    ├── Module-Probate-Real-Estate-Investor.md
    ├── Module-Real-Estate-Development.md
    └── Module-Commercial-Real-Estate.md

MWEF-v1.0/                      Historical reference: the original single-industry
                                 (mortgage-only) manual this framework grew out of.
                                 Preserved unmodified; superseded in scope by WEF-v1.0.
```

**Start here:** [`WEF-v1.0/00-Front-Matter.md`](WEF-v1.0/00-Front-Matter.md) — it explains the Core + Modules architecture, the consulting philosophy, and how the two parts fit together.

## The core idea

Most of what makes a website excellent — governance discipline, research rigor, information architecture, SEO structure, UX conversion mechanics, design-system quality, build discipline, QA rigor, and AI-assisted production workflow — is identical whether the client is a mortgage lender, a law firm, a commercial real estate brokerage, or a SaaS company. Only the specifics change: who the audience is, what regulations apply, what the content and keyword model should look like, and what trust signals a buyer needs to see.

So the **Core Methodology** defines a fixed sequence of Stage Gates that every engagement runs, unchanged. Each **Industry Module** supplies exactly the vertical-specific inputs — personas, regulatory landscape, competitive patterns, positioning, content model, trust signals — that those Stage Gates consume at explicit, marked **Module Injection Points**. Add a new industry by writing a new Module to the fixed template; the Core never has to change.

## Why this is public

This framework makes specific, sometimes consequential claims about regulated industries — state wholesaling disclosure laws, SEC Regulation D general solicitation rules, probate court-confirmation mechanics, HIPAA-adjacent intake handling, and more. It was built with real research, but it was built by one team, and regulatory detail is exactly the kind of thing that benefits from practitioners who actually work in these industries catching what's wrong, outdated, or missing in a specific state or specific niche.

**If you work in one of the covered industries and something in the relevant Module is wrong, incomplete, or has changed** — that's the most valuable kind of contribution this repo can get.

## How to contribute

**Open an [Issue](../../issues)** — this is the preferred way to flag a problem or propose an addition. Good issues look like:

- *"The Ohio wholesaling disclosure requirement in `Module-Cash-Home-Buyer.md` needs updating — the font-size requirement changed in [citation]."*
- *"Module Gap: the Law Firm Module doesn't cover bankruptcy practice — here's what's different about that niche."*
- *"The Probate Module's overbid-increment example is California-specific; can we add a comparison table for other states?"*
- *"Proposing a new Industry Module for [industry] — here's a competitor site and the regulatory basics."*

Please cite a source (a statute, a regulator's guidance page, a live competitor site) wherever you're asserting a fact — this framework tries hard not to assert unverified claims, and contributions should hold the same bar.

Pull requests are welcome too, especially for well-scoped corrections to a single Module's Regulatory & Compliance Landscape section — but if you're not comfortable editing markdown directly, an Issue describing the problem is just as valuable and someone can turn it into an edit.

## What this is not

This framework — including every Industry Module's Regulatory & Compliance Landscape section — does not constitute legal, financial, medical, or regulatory compliance advice. It identifies the regulatory frameworks *typically* applicable to a vertical as a starting orientation for a consulting team; it is not a substitute for a client's own qualified counsel, and every engagement run under this methodology treats it that way (see the Governance chapter's mandatory Compliance/Standards Liaison checkpoints).

## License

Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0). See [`LICENSE`](LICENSE). In short: share it, adapt it, use it on real client engagements, just credit the source and don't resell the framework itself commercially without permission.
