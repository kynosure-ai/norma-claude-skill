---
title: NIS2 Governance e Accountability
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: CISO / Legal
approver: Consiglio di Amministrazione
framework: NIS2
language: IT
documentType: policy
directive_articles:
  - Art. 20 - Governance
  - Art. 32 - Misure di vigilanza ed esecuzione (soggetti essenziali)
  - Art. 33 - Misure di vigilanza ed esecuzione (soggetti importanti)
  - Considerando 77-78 - Responsabilità organi di gestione
national_transposition: D.Lgs. 138/2024
cross_references:
  - 'ISO 27001:2022 Clausola 5'
  - D.Lgs. 231/2001 (Responsabilità amministrativa)
  - Art. 34 NIS2 - Misure e sanzioni
  - D.Lgs. 138/2024 Art. 23 - Governance
related_documents:
  - document: NIS2 Incident Reporting
    path: ../incidents/nis2-incident-reporting.md
  - document: NIS2 Risk Management Measures
    path: ../risk/nis2-risk-management-measures.md
  - document: NIS2 Business Continuity Plan
    path: ../continuity/nis2-business-continuity-plan.md
  - document: NIS2 Supply Chain Security
    path: ../supply-chain/nis2-supply-chain-security.md
  - document: NIS2 Compliance Checklist
    path: ../compliance/nis2-compliance-checklist.md
  - document: NIS2 Scope & Applicability
    path: ../context/nis2-scope-applicability.md
  - document: NIS2 Internal Audit Programme
    path: ../audit/nis2-internal-audit-programme.md
status: Bozza
subset: true
---

# NIS2 Governance & Accountability

## 1. Introduzione

### 1.1 Scopo

{{company_name}} riconosce che la governance della cybersecurity costituisce un elemento fondamentale per la protezione del patrimonio informativo aziendale e per la conformità ai requisiti della Direttiva (UE) 2022/2555. L'Articolo 20 della NIS2 introduce un cambio di paradigma significativo, attribuendo agli organi di gestione la responsabilità diretta per l'approvazione e la supervisione delle misure di sicurezza informatica, con potenziali conseguenze personali in caso di inadempimento.

Il presente documento definisce il framework di governance e accountability che {{company_name}} adotta per rispondere a tali requisiti normativi. La struttura organizzativa qui delineata assicura che la sicurezza delle informazioni sia integrata nei processi decisionali al più alto livello, con linee di reporting chiare verso il Consiglio di Amministrazione e meccanismi di supervisione efficaci. L'organizzazione stabilisce ruoli e responsabilità specifici per garantire che ogni funzione comprenda il proprio contributo alla postura di sicurezza complessiva.

Questo framework di governance risponde inoltre all'obbligo di formazione dei membri degli organi di gestione previsto dall'Articolo 20.2 NIS2, assicurando che il Board disponga delle conoscenze necessarie per valutare i rischi cyber e supervisionare l'efficacia delle misure implementate. La struttura qui definita si integra con il modello organizzativo ai sensi del D.Lgs. 231/2001, ove applicabile, rafforzando la cultura della compliance e della responsabilità a tutti i livelli dell'organizzazione.

### 1.2 Contesto Normativo

L'Art. 20 NIS2 introduce requisiti stringenti per gli organi di gestione:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    NIS2 ART. 20 - GOVERNANCE                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Art. 20.1 - APPROVAZIONE E SUPERVISIONE                                    │
│  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                    │
│                                                                             │
│  Gli organi di gestione delle entità essenziali e importanti               │
│  ► APPROVANO le misure di gestione dei rischi di cybersecurity             │
│  ► SUPERVISIONANO la loro attuazione                                       │
│  ► POSSONO ESSERE RITENUTI RESPONSABILI per le violazioni                  │
│                                                                             │
│  ─────────────────────────────────────────────────────────────────────     │
│                                                                             │
│  Art. 20.2 - FORMAZIONE OBBLIGATORIA                                        │
│  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                        │
│                                                                             │
│  I membri degli organi di gestione sono tenuti a:                          │
│  ► Seguire una FORMAZIONE sulla cybersecurity                              │
│  ► Acquisire conoscenze e competenze sufficienti per:                      │
│    • Identificare i rischi                                                 │
│    • Valutare le pratiche di gestione del rischio                          │
│    • Comprendere l'impatto sui servizi forniti                             │
│                                                                             │
│  ► INCORAGGIARE formazione analoga per i dipendenti                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 1.3 Implicazioni per la Leadership

| Requisito NIS2 | Implicazione Pratica |
|----------------|---------------------|
| Approvazione misure | CdA/Management deve formalmente approvare policy e misure |
| Supervisione | Reporting periodico al board, KPI monitorati |
| Responsabilità personale | Membri CdA potenzialmente responsabili per inadempimenti |
| Formazione obbligatoria | Training cybersecurity per tutti i membri del board |

---

## 2. Struttura di Governance

### 2.1 Organigramma Cybersecurity

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    GOVERNANCE STRUCTURE                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                     ┌──────────────────────────┐                            │
│                     │ CONSIGLIO DI             │  Responsabilità ultima    │
│                     │ AMMINISTRAZIONE          │  Approvazione, Supervisione│
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│                     ┌───────────┴──────────────┐                            │
│                     │ COMITATO RISCHI /        │  Oversight tecnico         │
│                     │ AUDIT COMMITTEE          │  Review periodica          │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│          ┌──────────────────────┼──────────────────────┐                   │
│          │                      │                      │                   │
│          ▼                      ▼                      ▼                   │
│  ┌───────────────┐    ┌────────────────┐    ┌───────────────┐             │
│  │ CEO/AD        │    │ CIO            │    │ CFO           │             │
│  │ Sponsor       │    │ IT Strategy    │    │ Budget        │             │
│  │ esecutivo     │    │                │    │ Risk Transfer │             │
│  └───────┬───────┘    └────────┬───────┘    └───────────────┘             │
│          │                     │                                           │
│          │           ┌─────────┴─────────┐                                 │
│          │           │                   │                                 │
│          │           ▼                   ▼                                 │
│          │   ┌───────────────┐   ┌───────────────┐                        │
│          │   │ CISO          │   │ DPO           │                        │
│          │   │ Security      │   │ Privacy       │                        │
│          │   │ Program       │   │ Compliance    │                        │
│          │   └───────┬───────┘   └───────────────┘                        │
│          │           │                                                     │
│          │           ▼                                                     │
│          │   ┌───────────────┐                                            │
│          │   │ SECURITY      │   Operazioni security quotidiane           │
│          │   │ TEAM / SOC    │   Incident response                        │
│          │   └───────────────┘   Monitoring                               │
│          │                                                                 │
│          ▼                                                                 │
│  ┌────────────────────────────────────────────────────────────────────┐   │
│  │                    BUSINESS UNITS / RISK OWNERS                    │   │
│  │  Ownership dei rischi, implementazione controlli operativi         │   │
│  └────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Ruoli e Responsabilità

#### Consiglio di Amministrazione / Management Body

| Responsabilità NIS2 | Attività Specifiche | Frequenza |
|---------------------|---------------------|-----------|
| **Approvazione** | Approvare Information Security Policy | Annuale |
| | Approvare budget cybersecurity | Annuale |
| | Approvare risk appetite/tolerance | Annuale |
| | Approvare piani di remediation critici | Ad hoc |
| **Supervisione** | Ricevere report su stato cybersecurity | Trimestrale |
| | Monitorare KPI security | Trimestrale |
| | Review incidenti significativi | Ad hoc |
| | Validare risk assessment | Annuale |
| **Formazione** | Completare training cybersecurity | Annuale |
| | Partecipare a tabletop exercises | Annuale |

#### CEO / Amministratore Delegato

| Responsabilità | Attività |
|----------------|----------|
| Executive Sponsor | Champion della cybersecurity a livello esecutivo |
| Accountability | Responsabile ultimo verso stakeholder e autorità |
| Risorse | Assicurare risorse adeguate per il programma security |
| Cultura | Promuovere cultura della sicurezza |

#### CISO (Chief Information Security Officer)

| Responsabilità | Attività |
|----------------|----------|
| **Strategia** | Definire e implementare strategia di cybersecurity |
| **Risk Management** | Gestire processo di risk assessment e treatment |
| **Compliance** | Assicurare conformità a NIS2 e normative |
| **Incident Management** | Coordinare risposta agli incidenti |
| **Awareness** | Gestire programma di security awareness |
| **Reporting** | Reporting al board e autorità |
| **Vendor Management** | Supervisionare security della supply chain |

#### DPO (Data Protection Officer)

| Responsabilità | Attività |
|----------------|----------|
| Privacy Compliance | Assicurare conformità GDPR |
| Coordinamento | Coordinare con CISO per data breach |
| Advisory | Consulenza su privacy by design |

#### Risk Owners (Business)

| Responsabilità | Attività |
|----------------|----------|
| Risk Ownership | Proprietari dei rischi delle proprie aree |
| Control Implementation | Implementare controlli operativi |
| Incident Reporting | Segnalare incidenti e anomalie |
| Compliance | Rispettare policy e procedure |

### 2.3 RACI Matrix Governance

| Attività | CdA | CEO | CISO | CIO | DPO | Risk Owners |
|----------|-----|-----|------|-----|-----|-------------|
| Approvazione Security Policy | A | R | R | C | C | I |
| Approvazione Budget Security | A | R | C | C | I | I |
| Risk Assessment | I | I | A | C | C | R |
| Risk Treatment | I | A | R | C | C | R |
| Incident Response | I | I | A | C | C | R |
| Notifica NIS2 alle Autorità | I | A | R | C | C | I |
| Security Awareness | I | I | A | C | C | R |
| Audit Security | C | I | A | R | C | C |
| Compliance Monitoring | I | I | A | C | R | C |

**Legenda:** R = Responsible, A = Accountable, C = Consulted, I = Informed

---

## 3. Comitato per la Cybersecurity

### 3.1 Istituzione e Mandato

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CYBERSECURITY STEERING COMMITTEE                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ MANDATO                                                                     │
│ ───────                                                                     │
│ Il Comitato per la Cybersecurity è l'organo di governance responsabile     │
│ della supervisione del programma di sicurezza delle informazioni e della   │
│ conformità NIS2, con poteri deliberativi delegati dal CdA.                 │
│                                                                             │
│ COMPOSIZIONE                                                                │
│ ───────────                                                                 │
│ • CEO/AD (Presidente)                                                       │
│ • CISO (Segretario)                                                         │
│ • CIO                                                                       │
│ • CFO                                                                       │
│ • DPO                                                                       │
│ • COO                                                                       │
│ • Legal Counsel                                                             │
│ • [Responsabile Operations critiche]                                        │
│                                                                             │
│ FREQUENZA                                                                   │
│ ─────────                                                                   │
│ • Ordinaria: Trimestrale                                                    │
│ • Straordinaria: Su convocazione per incidenti critici                     │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 3.2 Responsabilità del Comitato

| Area | Responsabilità |
|------|----------------|
| **Strategia** | Validare strategia cybersecurity, allineamento business |
| **Risk Oversight** | Approvare risk appetite, review risk register |
| **Budget** | Validare allocazione budget security |
| **Policy** | Approvare policy e major changes |
| **Compliance** | Monitorare conformità NIS2, GDPR, altre normative |
| **Incidents** | Review incidenti significativi, lessons learned |
| **Reporting** | Preparare reporting per CdA |

### 3.3 Agenda Tipo

| Punto | Contenuto | Presenter | Tempo |
|-------|-----------|-----------|-------|
| 1 | Approvazione verbale precedente | Segretario | 5 min |
| 2 | Dashboard KPI Security | CISO | 15 min |
| 3 | Risk Register Update | CISO | 20 min |
| 4 | Incidenti e Near Miss | CISO | 15 min |
| 5 | Compliance Status (NIS2, GDPR) | CISO/DPO | 15 min |
| 6 | Progetti Security in corso | CISO/CIO | 15 min |
| 7 | Budget e Risorse | CFO/CISO | 10 min |
| 8 | Varie ed eventuali | All | 5 min |

---

## 4. Reporting al Board

### 4.1 Framework di Reporting

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BOARD REPORTING FRAMEWORK                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ TRIMESTRALE                                                                 │
│ ───────────                                                                 │
│ ► Executive Summary Cybersecurity                                          │
│ ► KPI Dashboard                                                             │
│ ► Risk Register (top 10 risks)                                             │
│ ► Incident Summary                                                          │
│ ► Compliance Status                                                         │
│ ► Budget Tracking                                                           │
│                                                                             │
│ ANNUALE                                                                     │
│ ───────                                                                     │
│ ► Annual Security Report                                                    │
│ ► Risk Assessment completo                                                  │
│ ► Maturity Assessment                                                       │
│ ► Budget Request prossimo anno                                              │
│ ► Strategic Plan update                                                     │
│                                                                             │
│ AD HOC                                                                      │
│ ──────                                                                      │
│ ► Incidenti critici (immediato)                                            │
│ ► Cambiamenti normativi significativi                                       │
│ ► Vulnerabilità critiche                                                    │
│ ► Richieste budget straordinarie                                            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Template Executive Report

```
┌─────────────────────────────────────────────────────────────────────────────┐
│        CYBERSECURITY EXECUTIVE REPORT - Q[X] {{document_year}}                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ EXECUTIVE SUMMARY                                                           │
│ ─────────────────                                                           │
│ [2-3 frasi sullo stato generale della sicurezza]                           │
│                                                                             │
│ OVERALL SECURITY POSTURE: ☐ VERDE ☐ GIALLO ☐ ROSSO                         │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ KEY METRICS                                                                 │
│ ───────────                                                                 │
│                                                                             │
│ | Metrica               | Target  | Attuale | Trend | Status |             │
│ |-----------------------|---------|---------|-------|--------|             │
│ | Incidenti critici     | 0       |         |  ↑↓→  | ●●●    |             │
│ | MTTD (ore)            | < 24    |         |  ↑↓→  | ●●●    |             │
│ | MTTR (ore)            | < 4     |         |  ↑↓→  | ●●●    |             │
│ | Vulnerabilità Critiche| 0       |         |  ↑↓→  | ●●●    |             │
│ | Patch Compliance      | > 95%   |         |  ↑↓→  | ●●●    |             │
│ | Phishing Click Rate   | < 5%    |         |  ↑↓→  | ●●●    |             │
│ | Training Completion   | 100%    |         |  ↑↓→  | ●●●    |             │
│ | NIS2 Compliance       | 100%    |         |  ↑↓→  | ●●●    |             │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ TOP RISKS                                                                   │
│ ─────────                                                                   │
│                                                                             │
│ 1. [Rischio 1] - Livello: ALTO - Trend: ↑↓→                                │
│    Mitigazione: [azione in corso]                                          │
│                                                                             │
│ 2. [Rischio 2] - Livello: MEDIO - Trend: ↑↓→                               │
│    Mitigazione: [azione in corso]                                          │
│                                                                             │
│ 3. [Rischio 3] - Livello: MEDIO - Trend: ↑↓→                               │
│    Mitigazione: [azione in corso]                                          │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ INCIDENT SUMMARY                                                            │
│ ────────────────                                                            │
│                                                                             │
│ Totale incidenti Q: _____  vs Q precedente: _____ (↑↓→ __%)               │
│ Incidenti significativi: _____                                             │
│ Incidenti con data breach: _____                                           │
│ Notifiche NIS2 effettuate: _____                                           │
│                                                                             │
│ [Descrizione evento più significativo se presente]                         │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ NIS2 COMPLIANCE STATUS                                                      │
│ ──────────────────────                                                      │
│                                                                             │
│ Overall Compliance: _____%                                                  │
│                                                                             │
│ | Area Art. 21           | Status    | Gap  | Deadline Remediation |       │
│ |------------------------|-----------|------|----------------------|       │
│ | Risk policies (21.2.a) |  ●●●      |      |                      |       │
│ | Incident mgmt (21.2.b) |  ●●●      |      |                      |       │
│ | BC/DR (21.2.c)         |  ●●●      |      |                      |       │
│ | Supply chain (21.2.d)  |  ●●●      |      |                      |       │
│ | ... altri ...          |  ●●●      |      |                      |       │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ PROJECTS STATUS                                                             │
│ ───────────────                                                             │
│                                                                             │
│ | Progetto           | Budget | Speso | %Complete | Status | ETA     |     │
│ |--------------------|--------|-------|-----------|--------|---------|     │
│ | [Progetto 1]       |        |       |           | ●●●    |         |     │
│ | [Progetto 2]       |        |       |           | ●●●    |         |     │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ DECISIONI RICHIESTE AL BOARD                                                │
│ ────────────────────────────                                                │
│                                                                             │
│ ☐ [Decisione 1]                                                            │
│ ☐ [Decisione 2]                                                            │
│                                                                             │
│ ═══════════════════════════════════════════════════════════════════════════│
│                                                                             │
│ Preparato da: _____________ (CISO)    Data: _____________                  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 5. Formazione Organi di Gestione

### 5.1 Requisiti NIS2 per la Formazione

L'Art. 20.2 NIS2 richiede che i membri degli organi di gestione:

| Requisito | Descrizione |
|-----------|-------------|
| **Formazione** | Seguire formazione in materia di cybersecurity |
| **Conoscenze** | Acquisire conoscenze per identificare rischi |
| **Competenze** | Valutare pratiche di gestione del rischio |
| **Comprensione** | Comprendere impatto sui servizi dell'entità |

### 5.2 Programma di Formazione Board

| Modulo | Contenuto | Durata | Frequenza | Obbligatorio |
|--------|-----------|--------|-----------|--------------|
| **Fondamenti Cybersecurity** | Threat landscape, rischi cyber, terminologia | 2h | Una tantum | ✓ |
| **NIS2 Overview** | Requisiti NIS2, responsabilità board, sanzioni | 2h | Una tantum + update | ✓ |
| **Risk Management** | Framework risk management, risk appetite, KRI | 2h | Annuale | ✓ |
| **Incident Response** | Processo IR, ruolo del board, comunicazione crisi | 1h | Annuale | ✓ |
| **Tabletop Exercise** | Simulazione gestione incidente cyber | 2h | Annuale | ✓ |
| **Trend e Emerging Threats** | Update su minacce e trend | 1h | Semestrale | ✓ |
| **Case Studies** | Analisi incidenti reali e lessons learned | 1h | Annuale | Raccomandato |

### 5.3 Tracking Formazione

| Membro Board | Ruolo | Modulo 1 | Modulo 2 | Modulo 3 | Modulo 4 | Tabletop | Ultimo Update |
|--------------|-------|----------|----------|----------|----------|----------|---------------|
| [Nome] | Presidente | ☐ | ☐ | ☐ | ☐ | ☐ | |
| [Nome] | AD/CEO | ☐ | ☐ | ☐ | ☐ | ☐ | |
| [Nome] | Consigliere | ☐ | ☐ | ☐ | ☐ | ☐ | |
| [Nome] | Consigliere | ☐ | ☐ | ☐ | ☐ | ☐ | |

---

## 6. Accountability e Responsabilità

### 6.1 Framework di Responsabilità NIS2

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LIABILITY FRAMEWORK NIS2                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ SANZIONI AMMINISTRATIVE                                                     │
│ ─────────────────────────                                                   │
│                                                                             │
│ ┌─────────────────────────────────────────────────────────────────────┐    │
│ │ ENTITÀ ESSENZIALI (Art. 34.4)                                       │    │
│ │ • Fino a €10.000.000 o 2% fatturato mondiale annuo                  │    │
│ │   (il maggiore tra i due)                                           │    │
│ └─────────────────────────────────────────────────────────────────────┘    │
│                                                                             │
│ ┌─────────────────────────────────────────────────────────────────────┐    │
│ │ ENTITÀ IMPORTANTI (Art. 34.5)                                       │    │
│ │ • Fino a €7.000.000 o 1.4% fatturato mondiale annuo                 │    │
│ │   (il maggiore tra i due)                                           │    │
│ └─────────────────────────────────────────────────────────────────────┘    │
│                                                                             │
│ RESPONSABILITÀ PERSONALE MANAGEMENT (Art. 32.6, 33.5)                       │
│ ─────────────────────────────────────────────────────                       │
│                                                                             │
│ Le autorità competenti possono:                                             │
│ ► Richiedere che l'entità renda pubbliche le violazioni                    │
│ ► Nominare un monitoring officer (entità essenziali)                       │
│ ► Imporre sospensione temporanea di certificazioni/autorizzazioni          │
│ ► Richiedere sospensione temporanea dell'esercizio di funzioni             │
│   dirigenziali per le persone fisiche responsabili                         │
│                                                                             │
│ CIRCOSTANZE ATTENUANTI                                                      │
│ ────────────────────────                                                    │
│ • Misure adeguate implementate                                              │
│ • Cooperazione con autorità                                                 │
│ • Segnalazione volontaria                                                   │
│ • Remediation tempestiva                                                    │
│                                                                             │
│ CIRCOSTANZE AGGRAVANTI                                                      │
│ ────────────────────────                                                    │
│ • Violazioni ripetute                                                       │
│ • Mancata notifica incidenti                                                │
│ • Ostruzione alle ispezioni                                                 │
│ • Dolo o colpa grave                                                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 6.2 Deleghe e Procure

| Funzione | Delega | Limiti | Responsabilità Residua CdA |
|----------|--------|--------|----------------------------|
| **CISO** | Gestione operativa security | Budget approvato, policy approvate | Supervisione, approvazione strategica |
| **CIO** | Gestione IT, implementazione controlli | Budget, progetti approvati | Supervisione, direzione strategica |
| **DPO** | Compliance privacy | Autonomia funzionale | Supporto e risorse |
| **HR** | Formazione, procedure disciplinari | Policy aziendali | Supervisione programma |

### 6.3 Assicurazione D&O e Cyber

| Copertura | Descrizione | Verifica |
|-----------|-------------|----------|
| **D&O Insurance** | Protezione amministratori per responsabilità | ☐ Attiva, massimale €_____ |
| **Cyber Insurance** | Copertura danni cyber, incident response | ☐ Attiva, massimale €_____ |
| **Esclusioni** | Verificare esclusioni per dolo, NIS2 violations | ☐ Verificato |

---

## 7. Compliance Monitoring

### 7.1 Framework di Monitoraggio

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    COMPLIANCE MONITORING FRAMEWORK                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                     ┌──────────────────────────┐                            │
│                     │ CONTINUOUS MONITORING    │                            │
│                     │ (Automatizzato)          │                            │
│                     │ • Technical controls     │                            │
│                     │ • Security events        │                            │
│                     │ • Compliance status      │                            │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│                                 ▼                                           │
│                     ┌──────────────────────────┐                            │
│                     │ PERIODIC ASSESSMENT      │                            │
│                     │ (Trimestrale)            │                            │
│                     │ • KPI review             │                            │
│                     │ • Risk register update   │                            │
│                     │ • Control effectiveness  │                            │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│                                 ▼                                           │
│                     ┌──────────────────────────┐                            │
│                     │ INTERNAL AUDIT           │                            │
│                     │ (Annuale)                │                            │
│                     │ • Full compliance review │                            │
│                     │ • Control testing        │                            │
│                     │ • Gap analysis           │                            │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│                                 ▼                                           │
│                     ┌──────────────────────────┐                            │
│                     │ EXTERNAL AUDIT           │                            │
│                     │ (Annuale/Biennale)       │                            │
│                     │ • Independent assessment │                            │
│                     │ • Certification          │                            │
│                     │ • Regulatory readiness   │                            │
│                     └──────────────────────────┘                            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 7.2 KPI Governance

| KPI | Target | Frequenza | Owner |
|-----|--------|-----------|-------|
| Board meeting con agenda security | 100% | Trimestrale | CISO |
| Decisioni security documentate | 100% | Ogni meeting | CISO |
| Training board completato | 100% | Annuale | HR/CISO |
| Report al board consegnato | 100% | Trimestrale | CISO |
| Risk register presentato al board | 100% | Trimestrale | CISO |
| Incidenti critici escalati al board | 100% | Entro 24h | CISO |
| Budget security vs allocato | ≥ 95% | Annuale | CFO |
| Policy approvate vs pianificate | 100% | Annuale | CISO |

---

## 8. Documentazione e Evidenze

### 8.1 Documenti Obbligatori

| Documento | Approvazione | Frequenza Review | Stato |
|-----------|--------------|------------------|-------|
| Information Security Policy | CdA | Annuale | ☐ |
| Risk Assessment Report | Comitato Security | Annuale | ☐ |
| Risk Treatment Plan | CISO + CEO | Annuale | ☐ |
| Business Continuity Plan | CdA | Annuale | ☐ |
| Incident Response Plan | CISO | Annuale | ☐ |
| Security Awareness Program | CISO | Annuale | ☐ |
| Verbali Comitato Security | Comitato | Ogni riunione | ☐ |
| Report al CdA | CISO | Trimestrale | ☐ |
| Registro Formazione Board | HR | Continuo | ☐ |

### 8.2 Retention Documentale

| Tipologia | Retention | Note |
|-----------|-----------|------|
| Verbali CdA | 10 anni | Obbligo civilistico |
| Verbali Comitato Security | 5 anni | Best practice |
| Report Security al Board | 5 anni | Evidenza supervisione |
| Incident Reports | 5 anni | Evidenza per autorità |
| Training Records | 5 anni | Evidenza formazione |
| Risk Assessment | 5 anni | Storico decisioni |
| Audit Reports | 5 anni | Evidenza controlli |

---

## 9. Interazione con Autorità

### 9.1 Autorità Competenti NIS2 in Italia

| Autorità | Competenza | Contatto |
|----------|------------|----------|
| **ACN** | Autorità nazionale NIS2, CSIRT Italia | acn.gov.it |
| **Garante Privacy** | Protezione dati personali | garanteprivacy.it |
| **Autorità di settore** | Requisiti settoriali specifici | [Settoriale] |

### 9.2 Obblighi di Cooperazione

| Obbligo | Descrizione | Responsabile |
|---------|-------------|--------------|
| **Registrazione** | Registrazione presso ACN | Legal/CISO |
| **Notifica incidenti** | Early warning 24h, notification 72h, report 1m | CISO |
| **Audit/Ispezioni** | Cooperazione con ispezioni ACN | CISO/Legal |
| **Richieste informazioni** | Risposta a richieste autorità | Legal/CISO |
| **Remediation** | Attuazione misure richieste da autorità | CISO/CIO |

---

## 10. Integrazione con D.Lgs. 231/2001

### 10.1 Modello Organizzativo 231

Per le società italiane, i requisiti NIS2 possono integrarsi con il Modello 231:

| Area 231 | Integrazione NIS2 |
|----------|-------------------|
| **Organismo di Vigilanza** | Cooperazione con CISO, report su reati informatici |
| **Codice Etico** | Inclusione principi cybersecurity |
| **Parte Speciale** | Protocolli per reati informatici (art. 24-bis) |
| **Flussi informativi** | Reporting incidenti cyber all'OdV |
| **Whistleblowing** | Canale per segnalazioni security |

### 10.2 Reati Rilevanti

| Reato D.Lgs. 231 | Collegamento NIS2 |
|------------------|-------------------|
| Art. 24-bis (Reati informatici) | Prevenzione tramite misure Art. 21 |
| Art. 25-undecies (Ambiente) | Per settori con impatto ambientale |
| Art. 25-bis (Falsità) | Integrità dati e sistemi |

---

## 11. Revisione e Approvazione

### 11.1 Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

### 11.2 Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da (CISO) | | | |
| Verificato da (Legal) | | | |
| Approvato da (CEO) | | | |
| Approvato da (CdA) | | | |

---

## Allegati

- A - Organigramma Cybersecurity
- B - Charter Comitato Cybersecurity
- C - Template Report al Board
- D - Programma Formazione Board
- E - Deleghe e Procure
- F - RACI Matrix Completa

---

*Questo documento deve essere rivisto almeno 1 volta l'anno o in caso di cambiamenti significativi nella governance, normativa o struttura organizzativa. La revisione deve essere completata entro 30 giorni dalla modifica che la ha innescata.*

---

## 12. Requisiti Settoriali di Governance

### 12.1 Energia (Allegato I, Settore 1)

| Requisito | Dettaglio | Autorità di Riferimento |
|-----------|-----------|------------------------|
| Responsabile sicurezza impianti | Nomina obbligatoria di un security manager per impianti critici | ARERA |
| Coordinamento OT/IT | Board oversight sulle misure di sicurezza per sistemi SCADA/ICS | ENTSO-E |
| Piano di emergenza energetico | Approvazione CdA, integrato con BCP NIS2 | MiSE |

### 12.2 Settore Bancario e Finanziario (Allegato I, Settore 4)

| Requisito | Dettaglio | Autorità di Riferimento |
|-----------|-----------|------------------------|
| DORA governance | Organo di gestione approva digital resilience strategy (DORA Art. 5) | Banca d'Italia / BCE |
| ICT risk framework | Board ownership dell'ICT risk management framework | EBA (Linee guida ICT) |
| Reporting BCE | Report periodico alla BCE per enti significativi | BCE / SSM |
| Outsourcing governance | Board approval per outsourcing critico ICT | EBA Outsourcing Guidelines |

### 12.3 Sanitario (Allegato I, Settore 5)

| Requisito | Dettaglio | Autorità di Riferimento |
|-----------|-----------|------------------------|
| Responsabile privacy sanitaria | DPO con competenze specifiche sanitarie | Garante Privacy |
| Governance dispositivi medici | Supervisione sicurezza dispositivi medici connessi | Min. Salute |
| Clinical governance | Integrazione cybersecurity nella clinical governance | Regione / ASL |

### 12.4 Infrastrutture Digitali (Allegato I, Settore 8)

| Requisito | Dettaglio | Autorità di Riferimento |
|-----------|-----------|------------------------|
| SLA governance | Board oversight sugli SLA di sicurezza verso clienti | ACN |
| Qualificazione cloud | Mantenimento qualificazione ACN per servizi cloud PA | ACN / AgID |
| Trasparenza incidenti | Obbligo di comunicazione pubblica in caso di incidenti significativi | AGCOM |

### 12.5 Gestione Servizi ICT B2B (Allegato I, Settore 10)

| Requisito | Dettaglio | Autorità di Riferimento |
|-----------|-----------|------------------------|
| Responsabilità supply chain | Board accountability per sicurezza servizi erogati ai clienti NIS2 | ACN |
| Due diligence governance | Processo formalizzato di security due diligence per nuovi clienti/servizi | ACN |
| Multi-tenant isolation | Board awareness su rischi di compromissione cross-tenant | ENISA |

---

## 13. Documenti Correlati

| Documento | Tipo | Percorso |
|-----------|------|----------|
| NIS2 Incident Reporting | Procedura | `../incidents/nis2-incident-reporting.md` |
| NIS2 Risk Management Measures | Policy | `../risk/nis2-risk-management-measures.md` |
| NIS2 Business Continuity Plan | Piano | `../continuity/nis2-business-continuity-plan.md` |
| NIS2 Supply Chain Security | Policy | `../supply-chain/nis2-supply-chain-security.md` |
| NIS2 Compliance Checklist | Checklist | `../compliance/nis2-compliance-checklist.md` |
| NIS2 Scope & Applicability | Assessment | `../context/nis2-scope-applicability.md` |
| NIS2 Internal Audit Programme | Piano | `../audit/nis2-internal-audit-programme.md` |
| NIS2 ACN Registration Checklist | Checklist | `../compliance/nis2-acn-registration-checklist.md` |
| NIS2 ISMS Integration Guide | Guida | `../context/nis2-isms-integration-guide.md` |

---

## 14. Checklist di Compilazione

Prima di considerare questo documento completo, verificare che tutti i campi siano stati personalizzati:

| # | Placeholder | Sezione | Descrizione |
|---|-------------|---------|-------------|
| 1 | `{{company_name}}` | 1.1 | Ragione sociale dell'organizzazione |
| 2 | `{{document_date}}` | Frontmatter, 4.2, 11.1 | Data emissione documento |
| 3 | `{{document_author}}` | 11.1 | Autore del documento |
| 4 | `{{document_year}}` | 4.2 | Anno di riferimento del report |
| 5 | Organigramma (2.1) | 2.1 | Adattare l'organigramma alla propria struttura |
| 6 | Composizione Comitato (3.1) | 3.1 | Inserire nomi e ruoli effettivi dei membri |
| 7 | Tracking Formazione (5.3) | 5.3 | Inserire nomi membri board e stato formazione |
| 8 | Assicurazioni D&O (6.3) | 6.3 | Inserire massimali e verificare coperture |
| 9 | Sezione 12 | 12 | Selezionare il proprio settore e completare requisiti settoriali |
| 10 | Approvazioni (11.2) | 11.2 | Completare nomi e firme di approvazione |
