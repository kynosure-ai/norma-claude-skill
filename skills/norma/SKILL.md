---
name: norma
description: EU compliance methodology and templates. Use this skill when the user asks about EU AI Act, ISO 42001 (AIMS), ISO 27001 (ISMS), ISO 22301 (BCMS), ISO 27701 (PIMS), NIS2 Directive, DORA, CRA (Cyber Resilience Act), GDPR-adjacent topics, or any combination — gap analysis, control mapping, policy/procedure drafting, risk assessment, conformity assessment, AI risk classification, third-party assessment, business continuity, privacy impact assessment, incident response, vulnerability disclosure, SBOM, or generic "compliance" requests with no specific framework named. Also use for cross-framework mapping (NIST AI RMF, ENISA, GDPR Art. 30 RoPA), high-risk AI Annex III classification, Statement of Applicability authoring, or template selection across the 8 supported frameworks. Provides 32 curated templates and 8 framework methodologies adapted from the NORMA corpus by Kynosure.
license: MIT (with not-legal-advice disclaimer; see LICENSE)
---

> **Important / Importante:** This skill provides compliance template drafting and gap-analysis support based on public regulations and standards. It is **not legal advice**. Outputs must be reviewed by qualified legal/compliance professionals before use in production. Questo skill non costituisce consulenza legale: le bozze prodotte vanno sempre validate da professionisti qualificati. See LICENSE for full disclaimer.

## How to use this skill

This skill is a **router**, not a content blob. When the user asks a compliance question, identify the framework(s) and document type from the request, then load the matching `frameworks/<name>.md` reference for methodology and the matching `templates/<framework>/<file>.md` for a starter draft. Compose the response using both inputs plus a clear caveat about local applicability and the standing reminder that legal review is required.

The router shape keeps this entry point compact (Anthropic guidance: ≤500 lines) and pushes deep methodology into reference files that load only when relevant. Token cost per invocation is roughly the size of `SKILL.md` plus whatever single framework/template you actually consult — not the cost of all 8 frameworks at once.

## Quick reference (framework × resource)

Every link below resolves to a real file or directory bundled with this plugin. When the user's question matches a row, load that row's `frameworks/<name>.md` for methodology and consult the `templates/<framework>/` directory for matching starter drafts (see `INDEX.md` for the full template inventory).

| Framework | Methodology file | Templates folder | Trigger when user mentions |
|-----------|------------------|------------------|----------------------------|
| EU AI Act 2024/1689 | `frameworks/ai-act.md` | `templates/aims/` (combined slice — see note) | "AI Act", "high-risk AI", "Annex III", "conformity assessment", "CE marking", "EU Database", "GPAI", "FRIA", "Art. 27" |
| ISO/IEC 42001:2023 (AIMS) | `frameworks/aims.md` | `templates/aims/` | "ISO 42001", "AIMS", "AI Management System", "Statement of Applicability", "AIIA", "AI Impact Assessment", "Annex A 38 controls" |
| ISO/IEC 27001:2022 (ISMS) | `frameworks/isms.md` | `templates/isms/` | "ISO 27001", "ISMS", "information security policy", "Annex A 93 controls", "internal audit programme" |
| ISO 22301:2019 (BCMS) | `frameworks/bcms.md` | `templates/bcms/` | "ISO 22301", "BCMS", "business continuity", "BIA", "BCP", "crisis management", "DR plan", "RTO", "RPO" |
| ISO/IEC 27701:2019 (PIMS) | `frameworks/pims.md` | `templates/pims/` | "ISO 27701", "PIMS", "privacy management", "DPIA", "RoPA", "Art. 30 GDPR", "controller", "processor", "due diligence" |
| NIS2 Directive 2022/2555 | `frameworks/nis2.md` | `templates/nis2/` | "NIS2", "Art. 21", "essential entity", "important entity", "incident reporting", "Art. 23", "vendor questionnaire" |
| DORA Reg. 2022/2554 | `frameworks/dora.md` | `templates/dora/` | "DORA", "ICT risk", "third-party register", "TLPT", "Art. 28", "financial entity", "ICT incident" |
| CRA Reg. 2024/2847 | `frameworks/cra.md` | `templates/cra/` | "CRA", "Cyber Resilience Act", "product cybersecurity", "Annex I", "SBOM", "CVD", "vulnerability disclosure" |

**Note on the `aims/` templates folder.** This plugin uses **8 framework references** (split: `frameworks/ai-act.md` + `frameworks/aims.md`) but **7 template subdirectories** — `templates/aims/` is a combined editorial slice covering both ISO 42001 and EU AI Act use cases (curation rationale: Annex A controls and AI Act high-risk requirements share most underlying artifacts). When the user asks about EU AI Act specifically, load `frameworks/ai-act.md` for methodology and look inside `templates/aims/` for templates such as `aims-compliance-eu-ai-act-compliance-checklist.md`. When the user asks about ISO 42001, load `frameworks/aims.md` and the same templates folder.

For cross-framework mapping (e.g., "map ISO 42001 controls to AI Act articles", "ISO 27001 ↔ NIS2 Art. 21", "DORA ↔ ISO 27001"), open `INDEX.md` for the cross-framework adjacency table and load the relevant `frameworks/*.md` files in parallel.

## Workflow

When the skill activates on a compliance-flavored request, follow this loop:

1. **Identify framework(s) and document type** from the request. Use the trigger keywords in the Quick Reference table; ask a clarifying question only if the request is genuinely ambiguous (e.g., "compliance policy" with no framework named — surface the 8 supported frameworks and ask which one, or whether multiple apply).
2. **Load the appropriate `frameworks/<name>.md`** for methodology (clause structure, mandatory documented information, control inventory, regulatory timeline). For multi-framework questions, load all relevant references in parallel.
3. **Browse `templates/<framework>/`** and load the closest matching `<file>.md` if a starter draft is wanted. Use `INDEX.md` to navigate when the user asks "what's available?" or when the closest match isn't obvious.
4. **Compose the response** with:
   - Specific clause / control / article citations from the methodology file (e.g., "ISO 42001 Clause 6.1.2", "AI Act Art. 11", "NIS2 Art. 21(2)(d)").
   - The filled or adapted template content (preserve frontmatter; replace `[bracketed placeholders]` and `{{variables}}` with organisation-specific draft values, calling out what the user must validate).
   - A caveat about local / sector applicability where relevant (national NIS2 transposition, sectoral Lex Specialis like DORA superseding NIS2 for financial entities, AI Act provider vs deployer obligations, CRA product classification).
   - A short reminder that the output is a starting draft and must be reviewed by qualified legal / compliance professionals before any production use.

When uncertain about regulatory interpretation, prefer "this is the structural shape; here are the clauses to check; legal review is required" over guessed prescriptions.

## How to author from a template

Templates in this plugin follow a YAML-frontmatter + Markdown-body shape adapted from the NORMA corpus authoring convention. When the user asks "draft me a [doctype] for [framework]" — or when the closest existing template is structurally close but not exact — author or adapt using this convention.

### Template shape standard

```yaml
---
title: "[Document name]"
framework: "ISO27001" | "ISO22301" | "ISO42001" | "ISO27701" | "EU AI Act" | "NIS2" | "DORA" | "CRA"
documentType: "policy" | "procedure" | "template" | "checklist" | "register" | "assessment" | "plan"
version: "1.0"
date: "{{document_date}}"
classification: "Internal" | "Confidential" | "Public"
owner: "[Role responsible]"
approver: "{{approver_name}}"
language: "IT" | "EN"
---
```

Plus the document body skeleton:

```markdown
# [Document title]

## Document Information
| Campo | Valore |
|-------|--------|
| Versione | 1.0 |
| Data | [Data] |
| Classificazione | [Internal/Confidential/Public] |
| Owner | [Role] |

## Revision History
| Ver. | Date | Author | Changes |
|------|------|--------|---------|
| 1.0  | [Date] | [Name] | First issue |

## 1. Purpose
[2-3 clear sentences]

## 2. Scope
[Who/what this applies to]

## 3. Normative References
- [Framework] — [Clause / Article / Control]

## 4. Definitions
| Term | Definition |
|------|------------|

## 5. Responsibilities
| Role | Responsibility |
|------|----------------|

## 6. [Main content]
### 6.1 [Subsection]

## 7. Annexes
```

### Where placeholders go

- `[bracketed placeholders]` — organisation-specific values the user must fill in (role names, dates, scope statements, asset inventories).
- `{{double-braced variables}}` — system-generated values typical of a templating engine, but in a manual workflow treat them the same as bracketed placeholders.
- Tables with empty cells — structural prompts; the user fills rows from their own context.

When adapting, do NOT silently invent organisation-specific content. Either fill the placeholder with a clearly-marked draft value (e.g., `[DRAFT: replace with actual asset inventory]`) and call it out in the response, or leave the placeholder verbatim and tell the user what they need to provide.

### Authoring workflow

1. **Match document type to mandatory information.** Each framework reference file has a "Mandatory Documented Information" table (Tier 1 core / Tier 2 operational / Tier 3 policy). The document type the user asked for should appear there; if it doesn't, the request may be misframed (e.g., "ISO 42001 SLA" — SLAs aren't a 42001 mandatory document; ask whether they meant the AI Service Level / monitoring artifact or a vendor SLA under Annex A).
2. **Find the closest existing template** in `templates/<framework>/` — use `INDEX.md` to scan inventory by document type. If a close match exists, adapt it. If none does, fall back to the framework reference file's "Mandatory Documented Information" table as the structural skeleton and the template-shape standard above as the format.
3. **Cite canonical sources verbatim.** Clause numbers (ISO standards) and article numbers (regulations) should be quoted exactly — that's what the auditor will check. Don't paraphrase "Art. 21(2)(d)" into "the supply-chain measure"; quote the article and add the prose.
4. **Apply the shape standard.** Frontmatter complete; revision history populated even if it's just the v1.0 first issue; mandatory sections present (Purpose / Scope / Normative References / Definitions / Responsibilities / [Main Content] / Annexes).
5. **Validate before delivery** using the quality checklist below.

### Quality checklist

- [ ] Frontmatter complete (title, framework, documentType, version, date, language)
- [ ] Normative references cite specific clauses or articles (not general framework names)
- [ ] Professional plain language; no marketing copy; no first-person voice
- [ ] Placeholders explicit (`[brackets]` or `{{braces}}`); no silent organisation-specific defaults
- [ ] Markdown formatting valid (tables render, headings nested correctly, lists not broken)
- [ ] Naming convention respected (kebab-case slug; framework prefix matches directory)
- [ ] Document body answers the question the user actually asked (not a tangent)

### Per-framework mandatory documents (cheat sheet)

When the user asks "what do we need for [framework]?", the Tier 1 list below is the minimum set the framework reference file expands on:

| Framework | Tier 1 mandatory documents |
|-----------|----------------------------|
| ISO 27001:2022 | Scope ISMS · Information Security Policy · Risk Assessment Methodology · Risk Assessment Results · Risk Treatment Plan · Statement of Applicability (93 controls) · Security Objectives |
| ISO 22301:2019 | Scope BCMS · Legal/regulatory list · BC Policy · BC Objectives & Plans · Business Impact Analysis · Risk Assessment · BC Strategies · Communication Procedures · Business Continuity Plans |
| ISO 27701:2019 | Scope PIMS · Privacy Policy · Privacy Roles & Responsibilities · Privacy Risk Assessment · Privacy Objectives · Record of Processing Activities (RoPA, GDPR Art. 30) · Lawful Bases for Processing |
| ISO 42001:2023 | Scope AIMS · AI Policy · AI Roles & Responsibilities · AI Risk Assessment Methodology · AI Risk Assessment Results · AI Impact Assessment (AIIA) · AI Risk Treatment Plan · Statement of Applicability (38 controls) · AI System Inventory |
| EU AI Act | Risk classification (Annex III mapping) · Technical Documentation (Art. 11 + Annex IV) · Logs (Art. 12) · Instructions for Use (Art. 13) · Human Oversight design (Art. 14) · QMS (Art. 17) · EU Declaration of Conformity (Art. 47) · CE marking (Art. 48) · EU Database registration (Art. 49) |
| NIS2 | NIS2 Scope & Applicability · Risk Management Policy · Information Security Policy · Incident Response Procedure · Business Continuity Plan · Supply Chain Security Policy |
| DORA | ICT Risk Management Framework · Digital Operational Resilience Strategy · ICT Business Continuity Policy · ICT Disaster Recovery Plan · ICT Third-Party Risk Policy · ICT Incident Classification · ICT Third-Party Register (Art. 28.3) |
| CRA | Product Classification · Cybersecurity Risk Assessment · SBOM (machine-readable) · Annex I Mapping · Test Reports · Support Period · EU Declaration of Conformity (Annex V) · Vulnerability Handling Process · CVD Policy |

This cheat-sheet plus the per-framework reference files lets the router answer any "I need a [doctype] for [framework]" prompt without itself carrying the methodology weight.

## Cross-framework mapping

When the user's request crosses framework boundaries (e.g., "map our ISO 27001 controls to NIS2 Art. 21 measures", "ISO 42001 vs EU AI Act gap analysis", "DORA superseding NIS2 for our bank"), don't pick one framework and force-fit. Instead:

1. Open `INDEX.md` for the cross-framework adjacency table — it summarises which framework pairs have load-bearing overlap and which only touch.
2. Load both (or all) relevant `frameworks/*.md` files in parallel.
3. Compose a side-by-side mapping table in the response, citing canonical clause/article anchors on both sides (e.g., "ISO 27001 A.5.19 ↔ NIS2 Art. 21(2)(d)").
4. Call out the divergences explicitly. Conformity to one framework is not automatic conformity to the other — there are always residual gaps (the most load-bearing example: ISO 42001 covers ~70-80% of EU AI Act requirements; gaps remain on Art. 11/12/13/14/43, CE marking, EU Database registration; this is documented in `frameworks/ai-act.md`).

## Languages

- This file (`SKILL.md`) is **English** — discoverable in EN-dominant marketplaces and Anthropic's plugin directory.
- The 8 framework reference files in `frameworks/` have **English section headers** with **Italian prose body**. The Italian prose preserves Kynosure's compliance-corpus voice and the EU regulatory context that's clearest in Italian sources (Normattiva, ACN, AgID, Garante). English headers make navigation language-agnostic.
- Templates in `templates/` are **Italian-first** (matching Kynosure's primary EU audience). When the user prefers English, draft the adaptation in English using the Italian template as the structural reference — content shape transfers cleanly across languages.

If the user explicitly asks for output in English, draft in English. If they don't specify and the conversation is in English, default to English. If the conversation is in Italian, default to Italian.

## Provenance and license

- Methodology and templates are adapted from the **NORMA corpus by Kynosure** (annotated tag `norma-corpus-v1.0.0`). See `PROVENANCE.md` at the plugin root for the full source list, license posture, and audit attestations.
- Code-level artifacts (this `SKILL.md`, manifest files, scripts) are MIT licensed. Corpus content (templates, framework references) is CC BY-SA 4.0 — attribution required, derivatives share-alike. See `LICENSE` for the operative MIT body and the not-legal-advice disclaimer.
- Issues, citation corrections, and corpus-improvement suggestions: open at https://github.com/kynosure-ai/norma-claude-skill/issues.
