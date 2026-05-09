---
title: AIMS Scope - Ambito del Sistema di Gestione AI
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: AI Governance Lead
approver: '{{approver_name}}'
framework: 'ISO 42001:2023'
iso_clauses:
  - 4.1 - Understanding the organization and its context
  - 4.2 - Understanding the needs and expectations of interested parties
  - 4.3 - Determining the scope of the AI management system
  - 4.4 - AI management system
eu_ai_act:
  - Art. 4 - AI literacy
  - Art. 6 - Classification rules for high-risk AI systems
  - Art. 9 - Risk management system
cross_references:
  - document: AI Policy
    path: ../policies/ai-policy.md
  - document: AI System Inventory
    path: ../registers/ai-system-inventory.md
  - document: ISMS Scope
    path: ../../isms/context/scope-statement.md
status: draft
review_frequency: annual
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# AIMS Scope
## Ambito del Sistema di Gestione per l'Intelligenza Artificiale

## 1. Introduzione

### 1.1 Scopo del Documento

Questo documento definisce l'ambito del Sistema di Gestione per l'Intelligenza Artificiale (AIMS) di {{company_name}} in conformita alla clausola 4.3 di ISO/IEC 42001:2023. Il documento fornisce una descrizione chiara e completa dei confini organizzativi, tecnici e funzionali all'interno dei quali l'AIMS opera, identificando i sistemi AI coperti dal sistema di gestione e le relative esclusioni.

### 1.2 Obiettivi

L'obiettivo principale di questo documento e stabilire con precisione i confini e l'applicabilita dell'AIMS, definendo in modo inequivocabile quali sistemi AI, processi, funzioni e sedi rientrano nel perimetro di gestione. Il documento identifica inoltre l'integrazione dell'AIMS con altri sistemi di gestione gia presenti in azienda, quali il Sistema di Gestione per la Sicurezza delle Informazioni, il Sistema di Gestione per la Privacy e il Sistema di Gestione per la Qualita, assicurando coerenza e sinergia tra le diverse componenti della governance aziendale. Infine, il documento garantisce la conformita con il Regolamento Europeo sull'Intelligenza Artificiale e le ulteriori normative applicabili, definendo le interfacce con le parti interessate interne ed esterne.

---

## 2. Contesto dell'Organizzazione (4.1)

### 2.1 Profilo Organizzativo

| Campo | Descrizione |
|-------|-------------|
| **Denominazione** | {{company_name}} |
| **Settore** | {{industry_sector}} |
| **Dimensione** | {{employee_count}} dipendenti, fatturato € {{annual_revenue}} |
| **Sedi** | {{company_locations}} |
| **Mercati** | {{company_markets}} |

### 2.2 Contesto Esterno

```
┌──────────────────────────────────────────────────────────────────────┐
│                    CONTESTO ESTERNO AI                               │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  NORMATIVO                          TECNOLOGICO                      │
│  ┌────────────────────┐            ┌────────────────────┐           │
│  │ • EU AI Act        │            │ • Evoluzione LLM   │           │
│  │ • GDPR (AI+Privacy)│            │ • MLOps maturity   │           │
│  │ • Direttiva NIS2   │            │ • Cloud AI services│           │
│  │ • Settoriali (*)   │            │ • Open source AI   │           │
│  └────────────────────┘            └────────────────────┘           │
│                                                                      │
│  MERCATO                            SOCIALE                          │
│  ┌────────────────────┐            ┌────────────────────┐           │
│  │ • Competitori AI   │            │ • Aspettative etiche│          │
│  │ • Clienti/Partner  │            │ • Fiducia pubblica  │          │
│  │ • Fornitori AI     │            │ • Workforce impact  │          │
│  │ • Standard settore │            │ • Inclusività       │          │
│  └────────────────────┘            └────────────────────┘           │
│                                                                      │
│  (*) Specificare se applicabili: sanità, finanza, trasporti, etc.  │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 2.3 Contesto Interno

| Area | Fattori Rilevanti |
|------|-------------------|
| **Strategia** | {{ai_strategy_role}} |
| **Cultura** | {{digital_maturity}} |
| **Competenze** | {{ai_skills_assessment}} |
| **Tecnologia** | {{it_infrastructure}} |
| **Governance** | {{governance_structure}} |
| **Risorse** | {{ai_budget_resources}} |

### 2.4 Analisi SWOT AI

| | Positivi | Negativi |
|---|----------|----------|
| **Interni** | **STRENGTHS** | **WEAKNESSES** |
| | {{ai_strengths}} | {{ai_weaknesses}} |
| **Esterni** | **OPPORTUNITIES** | **THREATS** |
| | {{ai_opportunities}} | {{ai_threats}} |

---

## 3. Parti Interessate (4.2)

### 3.1 Identificazione Stakeholder AI

| Stakeholder | Categoria | Esigenze/Aspettative | Priorità |
|-------------|-----------|---------------------|----------|
| **Alta Direzione** | Interno | ROI, compliance, reputazione | Alta |
| **Dipendenti** | Interno | Formazione, job security, strumenti | Alta |
| **Clienti** | Esterno | Trasparenza, qualità, privacy | Alta |
| **Autorità (Garante, ACN)** | Esterno | Conformità normativa | Alta |
| **Fornitori AI** | Esterno | Requisiti contrattuali, SLA | Media |
| **Partner** | Esterno | Interoperabilità, sicurezza | Media |
| **Società civile** | Esterno | Etica, non discriminazione | Media |
| **Investitori** | Esterno | Governance, risk management | Media |

### 3.2 Requisiti delle Parti Interessate

| Fonte | Tipo Requisito | Descrizione | Obbligatorio |
|-------|----------------|-------------|--------------|
| EU AI Act | Legale | Conformità art. 6-51 per sistemi high-risk | Sì |
| GDPR | Legale | Protezione dati personali nei sistemi AI | Sì |
| Clienti | Contrattuale | SLA, trasparenza algoritmica | Sì |
| ISO 42001 | Volontario | Certificazione AIMS | No |
| {{sector_regulation}} | Settoriale | {{sector_requirements}} | {{mandatory}} |

---

## 4. Ambito dell'AIMS (4.3)

### 4.1 Dichiarazione di Scope

> L'AIMS di {{company_name}} si applica alla governance, sviluppo, deployment, operazione e dismissione di tutti i sistemi di Intelligenza Artificiale utilizzati per {{aims_purpose}}, includendo sistemi sviluppati internamente, acquisiti da terzi o utilizzati come servizio (AIaaS).

### 4.2 Confini Organizzativi

```
┌──────────────────────────────────────────────────────────────────────┐
│                    CONFINI AIMS                                      │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────────────────────────────────────────────────────┐│
│  │                    INCLUSO NELLO SCOPE                          ││
│  │                                                                 ││
│  │  FUNZIONI                      PROCESSI                         ││
│  │  ☑ IT / Data Science          ☑ Sviluppo AI (ML pipelines)     ││
│  │  ☑ Business Units [lista]     ☑ Deployment & Operations        ││
│  │  ☑ Compliance / Risk          ☑ Monitoraggio & Manutenzione    ││
│  │  ☑ HR (per formazione)        ☑ Incident Response AI           ││
│  │  ☑ Legal                      ☑ Procurement AI                  ││
│  │  ☑ [Altre funzioni]           ☑ Dismissione sistemi            ││
│  │                                                                 ││
│  │  SEDI                          TECNOLOGIE                       ││
│  │  ☑ [Sede 1]                   ☑ [Cloud provider]               ││
│  │  ☑ [Sede 2]                   ☑ [Piattaforma ML]               ││
│  │  ☑ Remote workers             ☑ [Framework AI]                 ││
│  │                                                                 ││
│  └─────────────────────────────────────────────────────────────────┘│
│                                                                      │
│  ┌─────────────────────────────────────────────────────────────────┐│
│  │                    ESCLUSO DALLO SCOPE                          ││
│  │                                                                 ││
│  │  ☐ [Funzione/Processo escluso 1] - Motivo: [giustificazione]   ││
│  │  ☐ [Funzione/Processo escluso 2] - Motivo: [giustificazione]   ││
│  │  ☐ [Sede esclusa] - Motivo: [giustificazione]                  ││
│  │                                                                 ││
│  └─────────────────────────────────────────────────────────────────┘│
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 4.3 Sistemi AI Inclusi

| ID Sistema | Nome | Tipo | Classificazione EU AI Act | Provider | In Scope |
|------------|------|------|---------------------------|----------|----------|
| AI-001 | [Nome] | [ML/GenAI/RPA] | [ ] Vietato [ ] High-risk [ ] Limited [ ] Minimal | [Interno/Vendor] | ☑ |
| AI-002 | [Nome] | [Tipo] | [Classificazione] | [Provider] | ☑ |
| AI-003 | [Nome] | [Tipo] | [Classificazione] | [Provider] | ☑ |
| AI-00N | [Nome] | [Tipo] | [Classificazione] | [Provider] | ☑ |

> **Nota**: L'inventario completo è mantenuto nel documento AI System Inventory

### 4.4 Sistemi AI Esclusi

| ID Sistema | Nome | Motivo Esclusione | Approvato da |
|------------|------|-------------------|--------------|
| [ID] | [Nome] | [Giustificazione dettagliata] | [Nome/Ruolo] |

**Criteri di esclusione ammessi**:
- Sistema non operativo/dismesso
- Sistema in fase di PoC non in produzione
- Sistema gestito interamente da terza parte senza accesso ai dati
- Sistema a rischio minimo senza impatto su diritti fondamentali

### 4.5 Confini Tecnici

| Componente | Incluso | Responsabile | Note |
|------------|---------|--------------|------|
| **Infrastruttura** | | | |
| Data Center on-premise | [ ] Sì [ ] No | [Team] | |
| Cloud [Provider] | [ ] Sì [ ] No | [Team] | Region: [regione] |
| Edge devices | [ ] Sì [ ] No | [Team] | |
| **Piattaforme** | | | |
| [Piattaforma ML] | [ ] Sì [ ] No | [Team] | |
| [LLM API] | [ ] Sì [ ] No | [Team] | |
| **Dati** | | | |
| Training data | [ ] Sì [ ] No | [Team] | |
| Operational data | [ ] Sì [ ] No | [Team] | |
| Model artifacts | [ ] Sì [ ] No | [Team] | |

---

## 5. Classificazione Sistemi AI (EU AI Act)

### 5.1 Framework di Classificazione

```
┌──────────────────────────────────────────────────────────────────────┐
│              PIRAMIDE RISCHIO EU AI ACT                              │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│                          ▲                                           │
│                         /█\          VIETATI (Art. 5)               │
│                        / █ \         Social scoring, manipolazione  │
│                       /  █  \        biometrica in tempo reale      │
│                      /───█───\                                       │
│                     /    █    \      HIGH-RISK (Art. 6, Annex III)  │
│                    /     █     \     Biometria, infrastrutture      │
│                   /      █      \    critiche, HR, education,       │
│                  /───────█───────\   law enforcement, giustizia     │
│                 /        █        \                                  │
│                /         █         \ LIMITED RISK (Art. 50)         │
│               /          █          \Chatbot, deepfake,             │
│              /───────────█───────────\emotion recognition           │
│             /            █            \                              │
│            /             █             \ MINIMAL RISK               │
│           /              █              \Spam filter, recommender   │
│          ▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔█▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔                           │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 5.2 Distribuzione Sistemi per Categoria

| Categoria EU AI Act | Numero Sistemi | % del Totale | Requisiti Chiave |
|---------------------|----------------|--------------|------------------|
| **Vietati** | 0 | 0% | N/A (non ammessi) |
| **High-Risk** | [N] | [%] | Risk management, data governance, trasparenza, human oversight, accuracy, robustness, cybersecurity |
| **Limited Risk** | [N] | [%] | Obblighi trasparenza (Art. 50) |
| **Minimal Risk** | [N] | [%] | Voluntary codes of conduct |
| **TOTALE** | [N] | 100% | |

### 5.3 Checklist Classificazione High-Risk

Per ogni sistema AI, verificare se ricade in:

**Annex I - Legislazione UE armonizzata**:
- [ ] Macchine (Reg. 2023/1230)
- [ ] Giocattoli (Dir. 2009/48/CE)
- [ ] Dispositivi medici (Reg. 2017/745)
- [ ] Dispositivi medico-diagnostici (Reg. 2017/746)
- [ ] Veicoli (vari regolamenti)
- [ ] Aviazione civile (Reg. 2018/1139)
- [ ] Altri prodotti regolamentati

**Annex III - Aree ad alto rischio**:
- [ ] 1. Biometria (identificazione, categorizzazione, emotion recognition)
- [ ] 2. Infrastrutture critiche (traffico, utilities)
- [ ] 3. Educazione e formazione professionale
- [ ] 4. Occupazione e gestione lavoratori
- [ ] 5. Accesso a servizi essenziali (credito, assicurazione, emergenza)
- [ ] 6. Law enforcement
- [ ] 7. Migrazione e controllo frontiere
- [ ] 8. Amministrazione della giustizia

---

## 6. Integrazione con Altri Sistemi di Gestione

### 6.1 Mappa Integrazione

```
┌──────────────────────────────────────────────────────────────────────┐
│                    INTEGRATED MANAGEMENT SYSTEM                      │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│          ┌─────────────────────────────────────────────┐            │
│          │                    AIMS                      │            │
│          │              (ISO 42001)                     │            │
│          │                                              │            │
│          │   ┌─────────────────────────────────────┐   │            │
│          │   │              ISMS                    │   │            │
│          │   │          (ISO 27001)                 │   │            │
│          │   │                                      │   │            │
│          │   │   ┌───────────────────────────┐    │   │            │
│          │   │   │         PIMS              │    │   │            │
│          │   │   │      (ISO 27701)          │    │   │            │
│          │   │   └───────────────────────────┘    │   │            │
│          │   │                                      │   │            │
│          │   └─────────────────────────────────────┘   │            │
│          │                                              │            │
│          └─────────────────────────────────────────────┘            │
│                                                                      │
│  Elementi Condivisi:                                                 │
│  • Risk Management Framework                                         │
│  • Internal Audit Programme                                          │
│  • Management Review                                                 │
│  • Document Control                                                  │
│  • Competence & Awareness                                            │
│  • Incident Management                                               │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 6.2 Matrice di Integrazione

| Elemento | AIMS (42001) | ISMS (27001) | PIMS (27701) | Responsabile |
|----------|--------------|--------------|--------------|--------------|
| Policy | AI Policy | InfoSec Policy | Privacy Policy | Top Management |
| Risk Assessment | AI Risk Assessment | Security Risk Assessment | Privacy Risk Assessment | Risk Manager |
| Controlli | Annex A (38) | Annex A (93) | Annex A/B | Control Owner |
| Audit | AIMS Audit | ISMS Audit | PIMS Audit | Internal Audit |
| Management Review | Integrato | Integrato | Integrato | Top Management |
| Incident Response | AI Incident | Security Incident | Data Breach | CSIRT/DPO |
| Training | AI Literacy | Security Awareness | Privacy Awareness | HR |

---

## 7. Documentazione dell'AIMS

### 7.1 Struttura Documentale

```
AIMS Documentation
├── Governance
│   ├── AIMS Scope (questo documento)
│   ├── AI Policy
│   ├── Roles & Responsibilities
│   └── AI Objectives & KPIs
├── Risk & Compliance
│   ├── AI Risk Assessment Methodology
│   ├── AI Impact Assessment Template
│   ├── Statement of Applicability
│   └── EU AI Act Compliance Checklist
├── Operations
│   ├── AI Lifecycle Procedure
│   ├── Human Oversight Procedure
│   ├── AI Incident Response
│   └── Deployment Checklist
├── Data
│   ├── Data Governance Policy
│   ├── Data Quality Requirements
│   └── Bias Assessment Procedure
├── Third Party
│   ├── Third-Party AI Management
│   └── Vendor Assessment Checklist
├── Performance
│   ├── AI Performance Monitoring
│   ├── Internal Audit Programme
│   └── Management Review
└── Registers
    ├── AI System Inventory
    ├── Model Cards
    └── Training Records
```

### 7.2 Controllo Documenti

Tutti i documenti AIMS seguono le procedure di document control definite nel sistema di gestione integrato, inclusi:
- Identificazione univoca
- Versionamento
- Approvazione formale
- Distribuzione controllata
- Revisione periodica
- Archiviazione e retention

---

## 8. Revisione dello Scope

### 8.1 Trigger di Revisione

Lo scope deve essere rivisto quando:
- Nuovi sistemi AI vengono introdotti
- Sistemi AI vengono dismessi
- Cambiamenti normativi (EU AI Act amendments)
- Modifiche organizzative significative
- Risultati di audit interni/esterni
- Incidenti AI significativi
- Almeno annualmente durante il Management Review

### 8.2 Processo di Modifica

1. Identificazione necessità di modifica
2. Analisi impatto su AIMS
3. Aggiornamento documentazione
4. Approvazione da AI Governance Committee
5. Comunicazione agli stakeholder
6. Aggiornamento inventario sistemi

---

## 9. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| AI Governance Lead | {{ai_governance_lead}} | | {{document_date}} |
| CISO | {{ciso}} | | {{document_date}} |
| DPO | {{dpo}} | | {{document_date}} |
| Top Management | {{senior_management}} | | {{document_date}} |

---

## Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## Documenti Correlati

| ID Documento | Titolo | Relazione |
|--------------|--------|-----------|
| {{company_name}}-POL-AIMS-001 | Politica per l'Intelligenza Artificiale | Framework: politica di riferimento |
| {{company_name}}-INV-AIMS-001 | Inventario Sistemi AI | Dettaglio: sistemi inclusi nello scope |
| {{company_name}}-MET-AIMS-001 | Metodologia Valutazione Rischi AI | Processo: gestione rischi per sistemi in scope |
| {{company_name}}-SOA-AIMS-001 | Statement of Applicability | Controlli: applicabilità dei controlli Annex A |
| {{company_name}}-DOC-ISMS-001 | ISMS Scope | Integrazione: perimetro sicurezza informazioni |

---

## Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Profilo organizzativo: {{industry_sector}}, {{employee_count}}, {{annual_revenue}}, {{company_locations}}, {{company_markets}}
- [ ] Contesto interno: {{ai_strategy_role}}, {{digital_maturity}}, {{ai_skills_assessment}}, {{it_infrastructure}}, {{governance_structure}}, {{ai_budget_resources}}
- [ ] Analisi SWOT AI: {{ai_strengths}}, {{ai_weaknesses}}, {{ai_opportunities}}, {{ai_threats}}
- [ ] Stakeholder e relativi requisiti/aspettative (Sezione 3)
- [ ] Dichiarazione di scope con finalita principali ({{aims_purpose}})
- [ ] Sistemi AI inclusi con classificazione EU AI Act (Sezione 4.3)
- [ ] Sistemi AI esclusi con giustificazione (Sezione 4.4)
- [ ] Confini tecnici definiti (infrastruttura, piattaforme, dati)
- [ ] Distribuzione sistemi per categoria EU AI Act (Sezione 5.2)
- [ ] Matrice integrazione con ISMS/PIMS (Sezione 6.2)
- [ ] Approvazioni firmate da {{ai_governance_lead}}, {{ciso}}, {{dpo}}, {{senior_management}}

---

*Documento conforme a ISO/IEC 42001:2023 Clausole 4.1-4.4*
