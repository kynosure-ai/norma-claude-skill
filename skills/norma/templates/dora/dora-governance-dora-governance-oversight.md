---
title: DORA Governance & Oversight
version: '1.1'
date: '{{document_date}}'
classification: Riservato
owner: CISO / Compliance
approver: Organo di Gestione
framework: DORA
language: IT
documentType: policy
regulation_articles:
  - Art. 5.2 - Responsabilita dell'organo di gestione
  - Art. 6.4 - Funzione di sicurezza ICT
  - Art. 13 - Comunicazione
  - Art. 28 - Governance terze parti
cross_references:
  - 'ISO 27001:2022 Clausola 5'
  - NIS2 Art. 20
status: Bozza
subset: true
---

# DORA Governance & Oversight

## 1. Introduzione

### 1.1 Scopo del Documento

Questo documento definisce il framework di governance e supervisione per la resilienza operativa digitale di {{company_name}} in conformità agli articoli 5.2, 6.4, 13 e 28 del Regolamento DORA. La governance efficace della resilienza digitale costituisce un pilastro fondamentale della conformità DORA, riconoscendo che la responsabilità ultima per la gestione del rischio ICT ricade sull'organo di gestione dell'entità finanziaria.

{{company_name}} riconosce che la resilienza operativa digitale non può essere delegata completamente alle funzioni tecniche, ma richiede un coinvolgimento attivo e informato del più alto livello decisionale. Questo documento stabilisce le strutture, i ruoli, le responsabilità e i processi necessari per garantire una supervisione efficace della gestione del rischio ICT e della resilienza operativa digitale.

### 1.2 Impegno dell'Organo di Gestione

L'organo di gestione di {{company_name}} si impegna a mantenere la responsabilità ultima per la gestione del rischio ICT, assicurando risorse adeguate, formazione continua dei membri e supervisione attiva dell'implementazione del framework di resilienza digitale. Tale impegno si traduce in approvazioni formali delle policy, revisioni periodiche dell'efficacia dei controlli e partecipazione diretta nelle decisioni strategiche relative alla sicurezza ICT.

## 2. Management Body Responsibilities (Art. 5.2)

### 2.1 Responsabilità Chiave

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    MANAGEMENT BODY RESPONSIBILITIES                         │
│                    DORA Art. 5.2                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ (a) DEFINE, APPROVE, SUPERVISE ICT RISK FRAMEWORK                          │
│     • Approve ICT Risk Management Policy                                    │
│     • Approve digital operational resilience strategy                       │
│     • Review framework effectiveness annually                               │
│                                                                             │
│ (b) ULTIMATE RESPONSIBILITY                                                 │
│     • Accountable for ICT risk management implementation                   │
│     • Cannot delegate ultimate responsibility                               │
│     • Personal liability for non-compliance                                 │
│                                                                             │
│ (c) ADEQUATE BUDGET                                                         │
│     • Approve sufficient ICT security budget                                │
│     • Ensure resources for digital resilience                               │
│     • Review budget adequacy annually                                       │
│                                                                             │
│ (d) ICT AUDIT POLICY                                                        │
│     • Approve ICT audit plans and policy                                    │
│     • Ensure independent ICT audit capability                               │
│     • Review audit findings                                                 │
│                                                                             │
│ (e) BUSINESS CONTINUITY                                                     │
│     • Approve ICT BC Policy and DR Plans                                    │
│     • Ensure testing of plans                                               │
│     • Review test results                                                   │
│                                                                             │
│ (f) REPORTING                                                               │
│     • Receive regular ICT risk reports                                      │
│     • Be informed of major incidents                                        │
│     • Review third-party risk status                                        │
│                                                                             │
│ (g) TRAINING                                                                │
│     • Undergo ICT risk training                                             │
│     • Maintain adequate knowledge                                           │
│     • Update training regularly                                             │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 1.2 Governance Maturity Assessment

| Area | Requisito | Status | Gap |
|------|-----------|--------|-----|
| Framework approvato | CdA approva ICT risk framework | ☐ C ☐ P ☐ NC | |
| Strategy approvata | Digital resilience strategy | ☐ C ☐ P ☐ NC | |
| Budget adeguato | Budget ICT security approvato | ☐ C ☐ P ☐ NC | |
| Audit policy | Policy audit ICT approvata | ☐ C ☐ P ☐ NC | |
| BC/DR approvati | Piani BC/DR approvati | ☐ C ☐ P ☐ NC | |
| Reporting periodico | Report ICT risk al board | ☐ C ☐ P ☐ NC | |
| Training board | Formazione membri su ICT risk | ☐ C ☐ P ☐ NC | |

---

## 2. Governance Structure

### 2.1 Three Lines Model

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    THREE LINES MODEL FOR ICT RISK                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                        ┌───────────────────────────┐                        │
│                        │ MANAGEMENT BODY           │                        │
│                        │ Accountability, Oversight │                        │
│                        └─────────────┬─────────────┘                        │
│                                      │                                      │
│    ┌─────────────────────────────────┼─────────────────────────────────┐   │
│    │                                 │                                 │   │
│    ▼                                 ▼                                 ▼   │
│ ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐          │
│ │ FIRST LINE       │  │ SECOND LINE      │  │ THIRD LINE       │          │
│ │                  │  │                  │  │                  │          │
│ │ Business Units   │  │ Risk Management  │  │ Internal Audit   │          │
│ │ IT Operations    │  │ ICT Security     │  │ ICT Audit        │          │
│ │ Development      │  │ Compliance       │  │                  │          │
│ │                  │  │                  │  │                  │          │
│ │ • Own risks      │  │ • Policies       │  │ • Independent    │          │
│ │ • Implement      │  │ • Standards      │  │   assurance      │          │
│ │   controls       │  │ • Monitoring     │  │ • Advisory       │          │
│ │ • Report issues  │  │ • Guidance       │  │ • Testing        │          │
│ └──────────────────┘  └──────────────────┘  └──────────────────┘          │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 ICT Security Function (Art. 6.4)

| Requisito | Implementazione |
|-----------|-----------------|
| Funzione dedicata | CISO + Security Team |
| Segregazione da operations | Reporting indipendente da IT Ops |
| Risorse adeguate | FTE, budget, tool |
| Competenze | Certificazioni, training |
| Autorità | Mandate per security decisions |

---

## 3. Committee Structure

### 3.1 ICT Risk Committee

| Elemento | Descrizione |
|----------|-------------|
| **Composizione** | CEO, CIO, CISO, CRO, CFO, Compliance, Legal |
| **Frequenza** | Mensile |
| **Mandate** | Oversight ICT risk, approvazione policy, review incidenti |
| **Reporting** | Al Management Body trimestralmente |

### 3.2 Agenda Tipo ICT Risk Committee

| Punto | Contenuto | Time |
|-------|-----------|------|
| 1 | Approvazione verbale precedente | 5 min |
| 2 | KPI Dashboard ICT Risk | 15 min |
| 3 | Incidents review | 15 min |
| 4 | Risk register update | 20 min |
| 5 | Third-party risk status | 10 min |
| 6 | Compliance status (DORA) | 10 min |
| 7 | Projects update | 10 min |
| 8 | Decisions required | 10 min |

---

## 4. Roles and Responsibilities

### 4.1 Key Roles DORA

| Ruolo | Responsabilità DORA |
|-------|---------------------|
| **Management Body** | Ultimate accountability, approve framework, training |
| **CEO** | Executive sponsor, resource allocation |
| **CIO** | ICT strategy, operations, resilience |
| **CISO** | ICT risk framework, security, incident response |
| **CRO** | Enterprise risk integration, appetite |
| **Compliance** | Regulatory compliance, reporting |
| **Internal Audit** | Independent assurance |
| **DPO** | GDPR coordination |

### 4.2 RACI Matrix DORA

| Attività | MB | CEO | CIO | CISO | CRO | Compl | Audit |
|----------|----|----|-----|------|-----|-------|-------|
| ICT Risk Framework | A | C | C | R | C | C | I |
| Digital Resilience Strategy | A | R | R | R | C | I | I |
| ICT Budget | A | R | C | C | C | I | I |
| Incident Response | I | I | C | A/R | I | C | I |
| Third-Party Risk | A | I | C | R | C | C | I |
| Testing Programme | A | I | C | R | I | I | C |
| Reporting to Authority | I | A | I | R | I | R | I |
| Audit Programme | A | I | C | C | I | I | R |

---

## 5. Board Training Programme

### 5.1 Training Requirements (Art. 5.2.g)

| Modulo | Contenuto | Durata | Frequenza |
|--------|-----------|--------|-----------|
| DORA Overview | Requisiti, responsabilità, sanzioni | 2h | Una tantum + update |
| Cyber Risk Fundamentals | Threat landscape, impatti | 2h | Annuale |
| ICT Risk Governance | Framework, oversight, KPI | 2h | Annuale |
| Incident Management | Ruolo board, comunicazione crisi | 1h | Annuale |
| Third-Party Risk | Oversight outsourcing ICT | 1h | Annuale |
| Tabletop Exercise | Simulazione incidente | 2h | Annuale |

### 5.2 Training Record

| Membro | Ruolo | DORA | Cyber | Governance | Incident | Tabletop | Data |
|--------|-------|------|-------|------------|----------|----------|------|
| | | ☐ | ☐ | ☐ | ☐ | ☐ | |

---

## 6. Reporting Framework

### 6.1 Reporting al Management Body

| Report | Contenuto | Frequenza |
|--------|-----------|-----------|
| **ICT Risk Dashboard** | KPI, trends, status | Trimestrale |
| **Incident Report** | Major incidents, lessons learned | Per evento + trimestrale |
| **Third-Party Report** | Status critical providers | Trimestrale |
| **Compliance Report** | DORA compliance status | Semestrale |
| **Audit Report** | ICT audit findings | Per audit + annuale |
| **Annual Report** | Comprehensive ICT risk review | Annuale |

### 6.2 KPI per Management Body

| KPI | Target | Frequenza |
|-----|--------|-----------|
| Major ICT incidents | 0 | Trimestrale |
| Incident notification SLA | 100% | Trimestrale |
| Critical findings open | 0 | Trimestrale |
| Third-party risk score | Green | Trimestrale |
| DORA compliance | 100% | Semestrale |
| Training completion | 100% | Annuale |
| BC/DR test success | 100% | Annuale |

---

## 7. Decision Framework

### 7.1 Decisioni Riservate al Management Body

| Decisione | Tipo | Documentazione |
|-----------|------|----------------|
| Approvazione ICT Risk Framework | Approvazione | Verbale CdA |
| Approvazione Digital Resilience Strategy | Approvazione | Verbale CdA |
| Budget ICT Security | Approvazione | Verbale CdA |
| Contratti ICT critical | Approvazione | Verbale CdA |
| Risk appetite ICT | Approvazione | Verbale CdA |
| Acceptance rischi High/Critical | Approvazione | Verbale CdA |
| Risposta a incidenti major | Supervisione | Verbale CdA |

### 7.2 Deleghe

| Attività | Delegata a | Limiti |
|----------|-----------|--------|
| Gestione operativa ICT risk | CISO | Framework approvato |
| Approvazione contratti non-critical | CIO | < €[X] annui |
| Incident response operativa | CISO | Escalation per major |
| Acceptance rischi Medium/Low | CRO | Documented |

---

## 8. Supervisory Reporting

### 8.1 Obblighi di Reporting all'Autorità

| Report | Contenuto | Frequenza | Destinatario |
|--------|-----------|-----------|--------------|
| Register of ICT Contracts | Tutti i contratti ICT | Su richiesta + annuale | Autorità competente |
| Major Incident Notification | Incidenti major | Initial/Intermediate/Final | Autorità competente |
| TLPT Results | Summary TLPT | Post-TLPT | Autorità competente |
| Critical Provider Notification | Nuovi CTPP | Pre-contratto | Autorità competente |

### 8.2 Preparedness per Ispezioni

| Area | Documentazione Pronta |
|------|----------------------|
| Governance | Verbali, policy approvate, deleghe |
| Risk Framework | Framework, risk register, treatment plan |
| Incident Management | Procedure, log incidenti, notifiche |
| Third-Party | Registro, contratti, assessment |
| Testing | Piano test, report, remediation |
| Training | Record formazione board e staff |

---

## 9. Accountability Framework

### 9.1 Sanzioni DORA

| Violazione | Sanzione Potenziale |
|------------|---------------------|
| Non conformità framework | Administrative penalties |
| Mancata notifica incidenti | Sanzioni pecuniarie |
| Inadeguata governance | Misure correttive, sanzioni |
| Carenze third-party management | Restrizioni operative |

### 9.2 Personal Accountability

I membri del Management Body possono essere personalmente responsabili per:
- Mancata approvazione/supervisione framework
- Inadeguata allocazione risorse
- Mancata formazione
- Ignorare warning/report

---

## 10. Continuous Improvement

### 10.1 Review Cycle

| Attività | Frequenza | Owner |
|----------|-----------|-------|
| Policy review | Annuale | CISO |
| Framework effectiveness | Annuale | Internal Audit |
| Governance maturity | Annuale | Compliance |
| Board training update | Annuale | HR/CISO |
| Benchmark peer | Biennale | CISO |

### 10.2 Improvement Actions

| Fonte | Input | Action |
|-------|-------|--------|
| Audit findings | Gap identificati | Remediation plan |
| Incidents | Lessons learned | Framework update |
| Regulatory feedback | Supervisory observations | Implementation |
| Benchmarking | Best practices | Enhancement |

---

## 11. Documenti Correlati

| Documento | Riferimento |
|-----------|-------------|
| ICT Risk Management Framework | DOC-ICT-001 |
| Digital Resilience Strategy | STR-DRS-001 |
| ICT Risk Committee Charter | CHR-IRC-001 |
| Board Training Programme | PRG-TRN-001 |
| Delegation Matrix | DOC-DEL-001 |

---

## 12. Revisione e Approvazione

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | | | |
| Verificato da | | | |
| Approvato da (CEO) | | | |
| Approvato da (Management Body) | | | |

---

*Questo documento deve essere rivisto annualmente e aggiornato in caso di cambiamenti nella governance, normativa o struttura organizzativa.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| dora-ict-risk-management-framework.md | Framework gestione rischio ICT (Art. 5-16) |
| dora-compliance-checklist.md | Checklist conformita DORA completa |
| dora-scope-applicability.md | Assessment ambito applicazione |
| dora-ict-incident-management.md | Gestione incidenti ICT (Art. 17-23) |
| dora-digital-resilience-testing.md | Test resilienza operativa (Art. 24-27) |
| dora-ict-third-party-risk.md | Rischio terze parti ICT (Art. 28-44) |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter | Data del documento |
| `{{document_author}}` | Revision History | Autore del documento |
| Management body roles | Sez. 2 | Definire responsabilita organo di gestione |
| ICT security function | Sez. 3 | Definire funzione sicurezza ICT (Art. 6.4) |
| Communication framework | Sez. 4 | Piano comunicazione (Art. 13) |
| Training programme | Sez. 5 | Programma formazione management body |
| Third-party governance | Sez. 6 | Governance terze parti ICT (Art. 28) |
| Firme approvazione | Sez. finale | Firme CEO e Management Body |
