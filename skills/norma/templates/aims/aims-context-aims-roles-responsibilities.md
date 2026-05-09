---
title: AIMS Roles & Responsibilities
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: AI Governance Lead
approver: '{{approver_name}}'
framework: 'ISO 42001:2023'
iso_clauses:
  - '5.3 - Organizational roles, responsibilities and authorities'
  - 5.1 - Leadership and commitment
  - A.2.2 - AI policy
  - A.2.3 - Roles and responsibilities
eu_ai_act:
  - Art. 4 - AI literacy
  - Art. 9.4 - Risk management responsibilities
  - Art. 14 - Human oversight
  - Art. 26 - Obligations of deployers
cross_references:
  - document: AIMS Scope
    path: ./aims-scope.md
  - document: AI Policy
    path: ../policies/ai-policy.md
  - document: Human Oversight Procedure
    path: ../procedures/human-oversight-procedure.md
  - document: ISMS Roles & Responsibilities
    path: ../../isms/context/roles-responsibilities.md
status: draft
review_frequency: annual
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# AIMS Roles & Responsibilities
## Ruoli e Responsabilità nel Sistema di Gestione AI

## 1. Introduzione

### 1.1 Scopo

Questo documento definisce i ruoli, le responsabilita e le autorita per il Sistema di Gestione per l'Intelligenza Artificiale di {{company_name}}, in conformita alla clausola 5.3 di ISO/IEC 42001:2023 e ai requisiti del Regolamento Europeo sull'Intelligenza Artificiale. La chiara definizione delle responsabilita costituisce un elemento fondamentale per l'efficace funzionamento del sistema di gestione, assicurando che ogni attivita legata alla governance AI sia assegnata a persone competenti con l'autorita necessaria per svolgere il proprio ruolo.

Il documento stabilisce la struttura di governance AI dell'Organizzazione, identificando i ruoli chiave dalla leadership strategica fino ai team operativi, definendo le responsabilita specifiche di ciascun ruolo e le interazioni tra i diversi attori coinvolti nel ciclo di vita dei sistemi AI. Attraverso questa documentazione, l'Organizzazione garantisce accountability per ogni decisione relativa all'intelligenza artificiale, dalla selezione delle tecnologie all'approvazione del deployment, dalla gestione degli incidenti al monitoraggio continuo delle performance. Il documento supporta inoltre la conformita ai requisiti di supervisione umana e AI literacy previsti dall'EU AI Act, assicurando che il personale assegnato a ruoli critici disponga delle competenze adeguate.

### 1.2 Obiettivi

Il documento persegue l'obiettivo di definire una chiara struttura di governance AI che garantisca supervisione, controllo e responsabilita su tutte le attivita relative all'intelligenza artificiale dell'Organizzazione. Gli obiettivi specifici includono l'assegnazione formale delle responsabilita per la gestione dell'intero ciclo di vita dei sistemi AI, dalla progettazione alla dismissione, garantendo che ogni fase sia presidiata da personale qualificato e autorizzato.

La struttura dei ruoli assicura accountability per tutte le decisioni strategiche e operative relative all'AI, stabilendo linee di reporting chiare e meccanismi di escalation per le situazioni che richiedono intervento a livelli superiori. Il documento definisce inoltre i requisiti di competenza per ogni ruolo e le responsabilita per la formazione continua del personale coinvolto nella gestione dei sistemi AI.

---

## 2. Struttura di Governance AI

### 2.1 Organigramma AIMS

```
┌──────────────────────────────────────────────────────────────────────┐
│                    GOVERNANCE STRUCTURE AIMS                         │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│                    ┌─────────────────────────┐                      │
│                    │     BOARD / CEO         │                      │
│                    │   (Ultimate Oversight)  │                      │
│                    └───────────┬─────────────┘                      │
│                                │                                     │
│                    ┌───────────▼─────────────┐                      │
│                    │   AI GOVERNANCE         │                      │
│                    │     COMMITTEE           │                      │
│                    │  (Strategic Direction)  │                      │
│                    └───────────┬─────────────┘                      │
│                                │                                     │
│         ┌──────────────────────┼──────────────────────┐             │
│         │                      │                      │             │
│         ▼                      ▼                      ▼             │
│  ┌─────────────┐      ┌─────────────┐      ┌─────────────┐         │
│  │ AI GOVERN- │      │    CISO     │      │    DPO      │         │
│  │ ANCE LEAD  │      │  (Security) │      │  (Privacy)  │         │
│  │ (AI Ethics)│      └──────┬──────┘      └──────┬──────┘         │
│  └──────┬──────┘             │                    │                 │
│         │                    │                    │                 │
│         ▼                    ▼                    ▼                 │
│  ┌─────────────────────────────────────────────────────────┐       │
│  │                    AI WORKING GROUP                      │       │
│  │  • ML Engineers     • Data Scientists    • DevOps       │       │
│  │  • Business Owners  • Legal              • Compliance   │       │
│  └─────────────────────────────────────────────────────────┘       │
│                                                                      │
│  ┌─────────────────────────────────────────────────────────┐       │
│  │                 OPERATIONAL TEAMS                        │       │
│  │  • AI Development Team    • AI Operations Team          │       │
│  │  • Data Engineering       • Quality Assurance           │       │
│  └─────────────────────────────────────────────────────────┘       │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 2.2 Assegnazioni Attuali

| Ruolo | Nome | Funzione | Backup | Data Nomina |
|-------|------|----------|--------|-------------|
| AI Governance Committee Chair | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| AI Governance Lead | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| CISO (per AI Security) | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| DPO (per AI Privacy) | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| Head of Data Science | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| AI Ethics Officer | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |
| {{additional_role}} | {{contact_name}} | {{department}} | {{backup_name}} | {{appointment_date}} |

---

## 3. Descrizione Ruoli

### 3.1 Top Management

**Responsabilità ISO 42001 (5.1)**:

| Responsabilità | Descrizione | Evidenza |
|----------------|-------------|----------|
| Leadership | Dimostrare leadership e impegno verso l'AIMS | Comunicazioni, risorse allocate |
| AI Policy | Stabilire e approvare la politica AI | Policy firmata |
| Integrazione | Integrare i requisiti AIMS nei processi di business | Procedure aggiornate |
| Risorse | Assicurare disponibilità di risorse necessarie | Budget, personale |
| Obiettivi | Definire e comunicare obiettivi AI | Obiettivi documentati |
| Cultura | Promuovere cultura di AI responsabile | Training, comunicazione |
| Miglioramento | Promuovere il miglioramento continuo | Management review |

### 3.2 AI Governance Committee

**Composizione**:
- CEO o delegato (Chair)
- AI Governance Lead
- CISO
- DPO
- CTO / Head of IT
- CFO o delegato
- Legal Counsel
- Rappresentante Business Unit

**Responsabilità**:

| Area | Responsabilità | Frequenza |
|------|----------------|-----------|
| Strategia | Definire la strategia AI dell'organizzazione | Annuale |
| Policy | Approvare/revisionare AI Policy e procedure | Annuale o ad hoc |
| Investimenti | Approvare investimenti AI significativi | Per progetto |
| Rischio | Approvare risk appetite e tolleranza per AI | Annuale |
| High-Risk | Autorizzare deployment sistemi high-risk | Per sistema |
| Incidenti | Supervisionare risposta a incidenti AI gravi | Ad hoc |
| Compliance | Monitorare conformità EU AI Act | Trimestrale |
| Review | Condurre management review AIMS | Annuale |

**Quorum e Decisioni**:
- Quorum: 50% + 1 dei membri
- Decisioni: maggioranza semplice
- Diritto di veto: AI Governance Lead per questioni etiche

### 3.3 AI Governance Lead

**Profilo**:

| Campo | Requisito |
|-------|-----------|
| **Reporting** | Riporta a CEO/COO, accesso diretto a Board |
| **FTE** | {{fte_allocation}} |
| **Qualifiche** | Background in AI/ML, governance, etica, legale |
| **Certificazioni** | Auspicabili: ISO 42001 LA, CISM, CDPO, AI ethics |

**Responsabilità principali**:

```
┌──────────────────────────────────────────────────────────────────────┐
│              RESPONSABILITÀ AI GOVERNANCE LEAD                       │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  GOVERNANCE                          RISK & COMPLIANCE               │
│  ────────────                        ─────────────────               │
│  • Implementare e mantenere AIMS     • Supervisionare AI risk mgmt   │
│  • Coordinare AI Governance Comm.    • Assicurare compliance normativa│
│  • Sviluppare policy e procedure     • Gestire audit AI              │
│  • Gestire documentazione AIMS       • Monitorare EU AI Act          │
│                                                                      │
│  ETICA                               REPORTING                       │
│  ─────                               ─────────                       │
│  • Valutare impatti etici AI         • Report a Top Management       │
│  • Gestire AI ethics review          • Coordinare con CISO e DPO     │
│  • Promuovere AI responsabile        • Reporting a autorità          │
│  • Gestire reclami/segnalazioni      • KPI e metriche AI             │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 3.4 AI System Owner

Per ogni sistema AI deve essere nominato un System Owner.

**Responsabilità**:

| Area | Descrizione |
|------|-------------|
| **Accountability** | Responsabile end-to-end del sistema AI |
| **Classificazione** | Determinare classificazione EU AI Act |
| **Risk Management** | Assicurare valutazione e trattamento rischi |
| **Compliance** | Garantire conformità a policy e normative |
| **Performance** | Monitorare KPI e performance del sistema |
| **Lifecycle** | Gestire l'intero ciclo di vita (dev → dismissione) |
| **Human Oversight** | Definire requisiti di supervisione umana |
| **Documentation** | Mantenere Model Card e documentazione |
| **Incident** | Gestire incidenti relativi al sistema |

### 3.5 ML Engineer / AI Developer

**Responsabilità**:

| Fase | Responsabilità |
|------|----------------|
| **Design** | Applicare principi di AI by design |
| **Sviluppo** | Implementare modelli secondo best practice |
| **Testing** | Eseguire test di fairness, robustezza, sicurezza |
| **Documentazione** | Produrre documentazione tecnica |
| **Deployment** | Seguire procedure di deployment approvate |
| **Monitoraggio** | Monitorare drift e performance in produzione |
| **Manutenzione** | Eseguire retraining e aggiornamenti |

### 3.6 Data Scientist / Data Engineer

**Responsabilità**:

| Area | Responsabilità |
|------|----------------|
| **Data Quality** | Assicurare qualità dati di training/inference |
| **Bias Assessment** | Valutare e mitigare bias nei dati |
| **Data Governance** | Rispettare policy di data governance |
| **Privacy** | Applicare tecniche di privacy-preserving ML |
| **Lineage** | Documentare data lineage e provenance |
| **Annotation** | Supervisionare processi di labeling |

### 3.7 Human Overseer

Per sistemi che richiedono supervisione umana (Art. 14 EU AI Act).

**Responsabilità**:

| Responsabilità | Descrizione |
|----------------|-------------|
| **Monitoring** | Monitorare funzionamento del sistema AI |
| **Interpretation** | Interpretare correttamente gli output AI |
| **Override** | Capacità di ignorare, sovrascrivere o invertire decisioni AI |
| **Stop** | Autorità di fermare il sistema se necessario |
| **Escalation** | Escalare anomalie secondo procedure |
| **Logging** | Documentare interventi e decisioni |

### 3.8 Business Process Owner

**Responsabilità**:

| Area | Responsabilità |
|------|----------------|
| **Requisiti** | Definire requisiti di business per sistemi AI |
| **Accettazione** | Validare che il sistema soddisfi i requisiti |
| **Uso** | Assicurare uso appropriato nel processo |
| **Formazione** | Garantire formazione degli utenti |
| **Feedback** | Fornire feedback su performance e problemi |

---

## 4. Matrice RACI

### 4.1 Governance e Policy

| Attività | Board | AI Gov Comm | AI Gov Lead | CISO | DPO | System Owner |
|----------|-------|-------------|-------------|------|-----|--------------|
| Approvazione AI Policy | A | R | R | C | C | I |
| Definizione strategia AI | A | R | C | C | C | I |
| Nomina ruoli AIMS | A | R | I | I | I | I |
| Budget AIMS | A | R | C | I | I | I |
| Risk appetite AI | A | R | C | C | C | I |

### 4.2 Risk Management

| Attività | AI Gov Lead | CISO | DPO | System Owner | ML Engineer |
|----------|-------------|------|-----|--------------|-------------|
| Metodologia risk assessment | A | C | C | I | I |
| Valutazione rischi per sistema | C | C | C | A/R | C |
| Classificazione EU AI Act | A | C | C | R | C |
| AI Impact Assessment | A | C | C | R | C |
| Trattamento rischi | C | C | C | A | R |

### 4.3 Lifecycle Management

| Attività | System Owner | ML Engineer | Data Scientist | QA | DevOps |
|----------|--------------|-------------|----------------|-----|--------|
| Requisiti AI | A | C | C | C | I |
| Design & sviluppo | A | R | R | C | C |
| Testing | A | C | C | R | C |
| Deployment | A | C | I | C | R |
| Monitoring | A | R | C | C | R |
| Retraining | A | R | R | C | C |
| Decommissioning | A | R | C | C | R |

### 4.4 Compliance & Audit

| Attività | AI Gov Lead | CISO | DPO | Internal Audit | System Owner |
|----------|-------------|------|-----|----------------|--------------|
| Compliance monitoring | A/R | C | C | C | R |
| Internal audit AIMS | C | C | C | A/R | C |
| Gestione NC | A | C | C | I | R |
| Reporting autorità | A/R | C | C | I | C |
| Management review | R | C | C | C | C |

**Legenda**: R=Responsible, A=Accountable, C=Consulted, I=Informed

---

## 5. Competenze Richieste

### 5.1 Matrice Competenze per Ruolo

| Competenza | AI Gov Lead | System Owner | ML Engineer | Data Scientist | Human Overseer |
|------------|-------------|--------------|-------------|----------------|----------------|
| AI/ML Fundamentals | ●●●○○ | ●●○○○ | ●●●●● | ●●●●● | ●●○○○ |
| AI Ethics | ●●●●● | ●●●○○ | ●●●○○ | ●●●○○ | ●●●○○ |
| EU AI Act | ●●●●● | ●●●●○ | ●●●○○ | ●●○○○ | ●●○○○ |
| ISO 42001 | ●●●●● | ●●●○○ | ●●○○○ | ●●○○○ | ●○○○○ |
| Risk Management | ●●●●○ | ●●●●○ | ●●○○○ | ●●○○○ | ●●○○○ |
| Data Governance | ●●●○○ | ●●○○○ | ●●●○○ | ●●●●● | ●○○○○ |
| Cybersecurity | ●●●○○ | ●●○○○ | ●●●○○ | ●●○○○ | ●○○○○ |
| Privacy/GDPR | ●●●●○ | ●●●○○ | ●●○○○ | ●●●○○ | ●●○○○ |
| Domain Knowledge | ●●○○○ | ●●●●● | ●●●○○ | ●●●○○ | ●●●●● |

**Legenda**: ○=Non richiesto, ●=Base, ●●=Intermedio, ●●●=Avanzato, ●●●●=Esperto, ●●●●●=Master

### 5.2 Formazione Obbligatoria

| Ruolo | Formazione | Frequenza | Durata |
|-------|------------|-----------|--------|
| **Tutti** | AI Literacy (Art. 4 EU AI Act) | Una tantum + refresh annuale | 4 ore |
| AI Governance Lead | ISO 42001 Lead Implementer | Una tantum | 40 ore |
| AI Governance Lead | EU AI Act Compliance | Annuale | 8 ore |
| System Owner | AI Risk Management | Annuale | 8 ore |
| ML Engineer | Responsible AI Development | Annuale | 16 ore |
| Human Overseer | Human-AI Collaboration | Per sistema | 4-8 ore |
| Top Management | AI Strategy & Governance | Annuale | 4 ore |

---

## 6. Comunicazione e Reporting

### 6.1 Canali di Comunicazione

| Da | A | Contenuto | Frequenza | Canale |
|----|---|-----------|-----------|--------|
| AI Gov Lead | Board | Report stato AIMS | Trimestrale | Presentazione |
| AI Gov Lead | AI Gov Committee | Dashboard KPI | Mensile | Report |
| System Owner | AI Gov Lead | Stato sistemi | Mensile | Report |
| ML Engineer | System Owner | Technical updates | Settimanale | Meeting |
| Human Overseer | System Owner | Anomalie/interventi | Real-time | Ticket + escalation |
| Any | AI Gov Lead | Segnalazioni etiche | Ad hoc | Canale dedicato |

### 6.2 Escalation Path

```
┌──────────────────────────────────────────────────────────────────────┐
│                    ESCALATION PATH AI                                │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  LIVELLO 1: OPERATIVO                                               │
│  ──────────────────────                                              │
│  Trigger: Anomalia operativa, drift moderato                        │
│  Gestito da: ML Engineer / DevOps                                   │
│  Tempo: < 4 ore                                                      │
│              │                                                       │
│              │ Se non risolto o impatto significativo               │
│              ▼                                                       │
│  LIVELLO 2: SISTEMA                                                  │
│  ─────────────────────                                               │
│  Trigger: Malfunzionamento sistema, bias rilevato                   │
│  Gestito da: System Owner                                           │
│  Tempo: < 24 ore                                                     │
│              │                                                       │
│              │ Se impatto alto o questione etica                    │
│              ▼                                                       │
│  LIVELLO 3: GOVERNANCE                                               │
│  ─────────────────────                                               │
│  Trigger: Violazione policy, incidente grave, danno a interessati  │
│  Gestito da: AI Governance Lead                                     │
│  Tempo: < 72 ore                                                     │
│              │                                                       │
│              │ Se impatto critico o reputazionale                   │
│              ▼                                                       │
│  LIVELLO 4: EXECUTIVE                                                │
│  ─────────────────────                                               │
│  Trigger: Crisi, notifica autorità, impatto legale/reputazionale   │
│  Gestito da: AI Governance Committee / CEO                          │
│  Tempo: Immediato                                                    │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## 7. Conflitti di Interesse

### 7.1 Principio di Separazione

Per garantire indipendenza e oggettività:

| Ruolo | Non può essere combinato con |
|-------|------------------------------|
| AI Governance Lead | ML Engineer, System Owner |
| Internal Auditor AIMS | Qualsiasi ruolo operativo AIMS |
| AI Ethics Reviewer | Sviluppatore del sistema in esame |
| Human Overseer | Sviluppatore del sistema supervisionato |

### 7.2 Gestione Conflitti

1. Dichiarazione annuale conflitti di interesse
2. Ricusazione in caso di conflitto specifico
3. Escalation a AI Governance Committee per casi dubbi
4. Documentazione delle decisioni

---

## 8. Integrazione con Altri Sistemi

### 8.1 Mapping Ruoli

| Ruolo AIMS | Corrispondente ISMS | Corrispondente PIMS |
|------------|--------------------|--------------------|
| AI Governance Lead | ISMS Manager | - |
| CISO | CISO | - |
| DPO | - | DPO |
| System Owner | Asset Owner | Treatment Owner |
| Internal Auditor | Internal Auditor | Internal Auditor |
| Top Management | Top Management | Top Management |

### 8.2 Responsabilità Condivise

| Area | AIMS | ISMS | PIMS | Coordinatore |
|------|------|------|------|--------------|
| Risk Management | AI-specific risks | Security risks | Privacy risks | Risk Manager |
| Incident Response | AI incidents | Security incidents | Data breach | CSIRT Lead |
| Training | AI literacy | Security awareness | Privacy awareness | HR |
| Audit | AIMS controls | ISMS controls | PIMS controls | Internal Audit |
| Vendor Management | AI suppliers | IT suppliers | Processors | Procurement |

---

## 9. Revisione e Aggiornamento

### 9.1 Trigger di Revisione

- Cambiamenti organizzativi
- Turnover in ruoli chiave
- Risultati audit
- Aggiornamenti normativi (EU AI Act)
- Almeno annualmente

### 9.2 Processo di Aggiornamento

1. Identificazione necessità di modifica
2. Draft aggiornamento
3. Consultazione stakeholder
4. Approvazione AI Governance Committee
5. Comunicazione
6. Formazione se necessario

---

## 10. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| AI Governance Lead | {{ai_governance_lead}} | | {{document_date}} |
| HR Director | {{hr_director}} | | {{document_date}} |
| Top Management | {{senior_management}} | | {{document_date}} |

---

## Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## Appendice A: Template Nomina Ruolo AIMS

```
LETTERA DI NOMINA

Data: {{document_date}}

A: {{appointee_name}}
Da: {{senior_management}}
Oggetto: Nomina a {{role}} nel Sistema di Gestione AI (AIMS)

Con la presente La nominiamo {{role}} nell'ambito del Sistema di Gestione
per l'Intelligenza Artificiale (AIMS) di {{company_name}}.

RESPONSABILITÀ ASSEGNATE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
{{assigned_responsibilities}}

AUTORITÀ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
{{granted_authorities}}

RISORSE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
{{allocated_resources}}

REPORTING
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Riporta a: {{role}}
Collabora con: {{collaborating_roles}}

FORMAZIONE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Formazione richiesta: {{required_training}}
Scadenza completamento: {{document_date}}

DECORRENZA
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
La nomina ha effetto dal: {{document_date}}

La preghiamo di confermare l'accettazione firmando la presente.

Top Management: _________________ Data: _________

Accettazione: _________________ Data: _________
```

---

## Documenti Correlati

| ID Documento | Titolo | Relazione |
|--------------|--------|-----------|
| {{company_name}}-DOC-AIMS-001 | AIMS Scope | Framework: perimetro del sistema di gestione |
| {{company_name}}-POL-AIMS-001 | Politica per l'Intelligenza Artificiale | Policy: principi e responsabilita |
| {{company_name}}-PRO-AIMS-003 | Procedura Supervisione Umana | Operativo: ruoli di human oversight |
| {{company_name}}-GOV-AIMS-001 | AI Competence & Awareness | Formazione: requisiti competenze |
| {{company_name}}-AUD-AIMS-001 | Programma Audit Interni AIMS | Audit: verifica efficacia ruoli |

---

## Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Assegnazioni attuali per tutti i ruoli con nome, funzione, backup, data nomina
- [ ] FTE allocation per AI Governance Lead ({{fte_allocation}})
- [ ] Matrice RACI verificata con tutti i ruoli (Sezione 4)
- [ ] Matrice competenze per ruolo con livelli effettivi (Sezione 5.1)
- [ ] Formazione obbligatoria pianificata per ogni ruolo (Sezione 5.2)
- [ ] Canali di comunicazione e frequenze (Sezione 6.1)
- [ ] Conflitti di interesse dichiarati e gestiti (Sezione 7)
- [ ] Mapping ruoli con ISMS/PIMS (Sezione 8.1)
- [ ] Template nomina compilabile per ciascun ruolo (Appendice A)
- [ ] Approvazioni firmate da {{ai_governance_lead}}, {{hr_director}}, {{senior_management}}

---

*Documento conforme a ISO/IEC 42001:2023 Clausola 5.3 e EU AI Act Art. 4*
