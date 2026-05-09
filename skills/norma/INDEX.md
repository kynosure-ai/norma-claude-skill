# NORMA Skill Index

Catalog navigation for the 32 templates × 8 framework methodologies bundled in this plugin. SKILL.md is the router; this file is the inventory you consult when SKILL.md says "see INDEX.md".

> **Important:** Not legal advice. See `SKILL.md` for the full disclaimer and `LICENSE` for the operative terms.

## Per-framework template inventory

The 32 templates are organised in **7 framework subdirectories** under `templates/`. The `aims/` directory is a combined editorial slice covering both ISO/IEC 42001:2023 and EU AI Act 2024/1689 use cases — the EU AI Act compliance checklist lives there because it shares structural artifacts (controls, governance roles, AI system inventory) with the AIMS templates. **The frameworks/ tree, by contrast, splits AI Act and ISO 42001 into two distinct reference files** — methodology stays separate even where editorial templates merge.

### `templates/aims/` — ISO 42001:2023 + EU AI Act 2024/1689 (combined slice, 5 templates)

Methodology references: `frameworks/aims.md` (ISO 42001) · `frameworks/ai-act.md` (EU AI Act).

| Template | Document type | Title |
|----------|---------------|-------|
| `aims-context-aims-scope.md` | scope | AIMS Scope — Ambito del Sistema di Gestione AI |
| `aims-context-aims-roles-responsibilities.md` | RACI / governance | AIMS Roles & Responsibilities |
| `aims-assessments-ai-impact-assessment.md` | assessment | AI Impact Assessment (AIIA) |
| `aims-data-bias-assessment-procedure.md` | procedure | Procedura di Valutazione e Mitigazione del Bias |
| `aims-compliance-eu-ai-act-compliance-checklist.md` | checklist | EU AI Act Compliance Checklist |

### `templates/isms/` — ISO/IEC 27001:2022 ISMS (5 templates)

Methodology reference: `frameworks/isms.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `isms-policies-cloud-security-policy.md` | policy | Politica di Sicurezza del Cloud |
| `isms-policies-supplier-security-policy.md` | policy | Politica di Sicurezza per i Fornitori |
| `isms-procedures-incident-management.md` | procedure | Procedura di Gestione degli Incidenti di Sicurezza |
| `isms-risk_assessment-risk-assessment-methodology.md` | procedure | Metodologia di Valutazione del Rischio |
| `isms-audit-internal-audit-programme.md` | plan | Programma di Audit Interni ISMS |

### `templates/nis2/` — NIS2 Directive 2022/2555 (5 templates)

Methodology reference: `frameworks/nis2.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `nis2-governance-nis2-governance-accountability.md` | policy | NIS2 Governance e Accountability |
| `nis2-risk-nis2-risk-management-measures.md` | procedure | NIS2 Misure di Gestione del Rischio |
| `nis2-incidents-nis2-incident-reporting.md` | procedure | Procedura di Notifica Incidenti NIS2 |
| `nis2-assessments-vendor-security-questionnaire.md` | questionnaire | Questionario di Sicurezza Fornitori NIS2 |
| `nis2-compliance-nis2-compliance-checklist.md` | checklist | Checklist di Conformità NIS2 |

### `templates/dora/` — DORA Reg. 2022/2554 (5 templates)

Methodology reference: `frameworks/dora.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `dora-governance-dora-governance-oversight.md` | policy | DORA Governance & Oversight |
| `dora-risk-dora-ict-risk-management-framework.md` | procedure | DORA ICT Risk Management Framework |
| `dora-incidents-dora-ict-incident-management.md` | procedure | DORA ICT Incident Management |
| `dora-third_party-dora-ict-third-party-risk.md` | procedure | DORA ICT Third-Party Risk Management |
| `dora-compliance-dora-compliance-checklist.md` | checklist | DORA Compliance Checklist |

### `templates/pims/` — ISO/IEC 27701:2019 PIMS (4 templates)

Methodology reference: `frameworks/pims.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `pims-policies-privacy-policy.md` | policy | Privacy Policy — Sistema di Gestione Privacy |
| `pims-dpia-dpia-template.md` | template | Data Protection Impact Assessment (DPIA) |
| `pims-assessments-processor-due-diligence.md` | assessment | Valutazione Due Diligence Responsabili del Trattamento |
| `pims-audit-pims-internal-audit-programme.md` | plan | Programma Audit Interni PIMS |

### `templates/bcms/` — ISO 22301:2019 BCMS (4 templates)

Methodology reference: `frameworks/bcms.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `bcms-plans-business-continuity-plan.md` | plan | Business Continuity Plan (BCP) |
| `bcms-plans-it-disaster-recovery-plan.md` | plan | IT Disaster Recovery Plan |
| `bcms-plans-crisis-management-plan.md` | plan | Crisis Management Plan |
| `bcms-audit-internal-audit-programme.md` | plan | Programma di Audit Interni BCMS |

### `templates/cra/` — CRA Reg. 2024/2847 (4 templates)

Methodology reference: `frameworks/cra.md`.

| Template | Document type | Title |
|----------|---------------|-------|
| `cra-compliance-cra-annex-i-requirements.md` | checklist | CRA Annex I — Essential Cybersecurity Requirements |
| `cra-technical_documentation-cra-risk-assessment.md` | assessment | CRA Cybersecurity Risk Assessment |
| `cra-technical_documentation-cra-sbom-template.md` | procedure | CRA SBOM Requirements & Template |
| `cra-vulnerability-cra-cvd-policy.md` | policy | CRA Coordinated Vulnerability Disclosure Policy |

**Total:** 32 templates across 7 subdirectories. Selection rationale (breadth-showcase across 8 frameworks, why these 32 of 208) is documented in `PROVENANCE.md` at the plugin root.

## Cross-framework adjacency

Where two frameworks share load-bearing requirements, drafting once and mapping across saves work. The table below summarises which framework pairs have natural overlap and where divergence demands attention.

| Pair | Overlap area | What to reuse | Where they diverge |
|------|--------------|---------------|--------------------|
| **ISO 42001 ↔ EU AI Act** | AI governance, risk management, AI system inventory, transparency, human oversight | AIMS Scope · AIIA · AI Risk Assessment · Roles & Responsibilities · AI Policy | AI Act adds Art. 11 Technical Documentation, Art. 12 logs, Art. 43 conformity assessment, Art. 47 EU Declaration of Conformity, Art. 48 CE marking, Art. 49 EU Database registration. ISO 42001 covers ~70-80% of AI Act; the rest is incremental. |
| **ISO 27001 ↔ NIS2** | Information security policy, risk management, incident response, supply chain security, BCM linkage | ISMS Risk Assessment Methodology · Information Security Policy · Incident Management Procedure · Supplier Security Policy | NIS2 Art. 23 adds 24h early warning + 72h initial notification + 1-month final report (specific timelines); Art. 20 adds management-body accountability and training; NIS2 has national transposition variability (sanctions, registration thresholds). |
| **ISO 27001 ↔ DORA** | ICT risk, third-party risk, incident classification, BCM | ISMS Risk Assessment · Supplier Security Policy · Incident Management Procedure · BCMS BCP | DORA adds the ICT Third-Party Register (Art. 28.3) with prescribed fields, TLPT (Threat-Led Penetration Testing) for significant entities, ICT-incident-specific classification (major incidents) overlaying the ISMS classification, Lex Specialis status over NIS2 for financial entities. |
| **NIS2 ↔ DORA** | Both apply to many financial-sector entities; DORA is Lex Specialis | DORA-specific templates supersede NIS2 templates for financial entities; reuse risk assessment methodology and incident classification structure | DORA goes deeper on ICT (TLPT, third-party register), NIS2 goes broader on cybersecurity overall. Financial-sector entities map DORA primary, NIS2 secondary. |
| **ISO 27001 ↔ ISO 27701** | ISO 27701 is an extension of ISO 27001 + ISO 27002, not a standalone | ISMS scope, policies, risk methodology — extend, don't duplicate | 27701 adds privacy-specific Clause 7 (controller) and Clause 8 (processor) controls, RoPA (GDPR Art. 30 alignment), DPIA, lawful basis, DSR procedures. PIMS without an underlying ISMS is not certifiable. |
| **ISO 27701 ↔ GDPR** | Privacy management; 27701 maps to GDPR Articles | RoPA aligns with Art. 30; DPIA aligns with Art. 35; lawful basis aligns with Art. 6 / 9; DSR procedure aligns with Arts. 15-22 | 27701 is a management-system standard (certifiable); GDPR is a regulation (binding, with regulator enforcement). 27701 conformance is evidence, not legal compliance. |
| **CRA ↔ ISO 27001** | Product cybersecurity vs organisational cybersecurity | Risk assessment methodology, vulnerability disclosure procedure, supplier security | CRA is a product regulation (CE marking required, Annex I essential requirements per product), ISMS is organisational. CRA also requires SBOM (machine-readable) and CVD policy with specific 24h reporting via ENISA single reporting platform; ISMS-level CVD is necessary but insufficient. |
| **ISO 22301 ↔ DORA** | Business continuity for ICT services | BIA · BCP structure · DR strategy | DORA Art. 11 mandates ICT-specific business continuity policy + DR plan with prescribed scope; DORA testing scenarios are stricter (TLPT for significant entities). 22301 BCP is the broader frame; DORA carves the ICT slice with stricter testing. |

When a request crosses two frameworks not listed above, default to: load both `frameworks/*.md` files, look for cross-references in their "Mapping" sections, and surface divergences explicitly.

## How to navigate this index

- **"What's available for [framework]?"** → jump to the matching `templates/<framework>/` section above.
- **"What's the closest template to [doctype]?"** → scan the Document type column for each framework. If multiple match, the framework reference file's Tier 1/2/3 mandatory-information table disambiguates.
- **"Map [framework A] to [framework B]"** → consult the cross-framework adjacency table; load both `frameworks/*.md` files in parallel.
- **"Why these 32 templates and not the other 176?"** → see `PROVENANCE.md` for the strategic-subset selection rationale (breadth-showcase across all 8 frameworks).
