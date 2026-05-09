---
title: DORA ICT Incident Management
version: '1.1'
date: '{{document_date}}'
classification: Riservato
owner: CISO
approver: Organo di Gestione
framework: DORA
language: IT
documentType: procedure
regulation_articles:
  - Art. 17 - Processo di gestione degli incidenti ICT
  - Art. 18 - Classificazione degli incidenti ICT
  - Art. 19 - Segnalazione degli incidenti gravi ICT
  - Art. 20 - Armonizzazione dei contenuti delle segnalazioni
  - Art. 21 - Centralizzazione delle segnalazioni
  - Art. 22 - Feedback delle autorita
  - Art. 23 - Incidenti operativi o di sicurezza relativi ai pagamenti
cross_references:
  - NIS2 Art. 23
  - GDPR Art. 33-34
  - 'ISO 27001:2022 A.5.24-A.5.27'
status: Bozza
subset: true
---

# DORA ICT Incident Management

## 1. Introduzione

### 1.1 Scopo del Documento

Questo documento definisce il processo di gestione degli incidenti ICT di {{company_name}} e le procedure di notifica alle autorità competenti in conformità al Capitolo III del Regolamento DORA (Articoli 17-23). L'obiettivo primario è stabilire un approccio strutturato e tempestivo per la rilevazione, la classificazione, la gestione e la notifica degli incidenti correlati alle tecnologie dell'informazione e della comunicazione.

La gestione efficace degli incidenti ICT rappresenta un elemento critico della resilienza operativa digitale. {{company_name}} riconosce che la capacità di identificare rapidamente gli incidenti, valutarne la gravità e rispondere in modo appropriato determina la differenza tra una perturbazione temporanea e un impatto significativo sui servizi finanziari e sui clienti. Questo documento assicura che l'organizzazione sia preparata a gestire qualsiasi incidente ICT con la dovuta urgenza e professionalità.

### 1.2 Impegno dell'Organizzazione

{{company_name}} si impegna a mantenere una capacità di risposta agli incidenti che operi continuativamente, con personale adeguatamente formato, strumenti di rilevazione efficaci e procedure chiare per l'escalation e la comunicazione. L'organizzazione garantisce che tutti gli incidenti significativi siano analizzati per identificare le cause profonde e implementare miglioramenti che prevengano il ripetersi di eventi simili.

### 1.3 Conformità Normativa

Il processo qui descritto rispetta integralmente i requisiti DORA relativi alla gestione degli incidenti, inclusi gli obblighi di notifica alle autorità competenti entro le tempistiche stabilite: notifica iniziale entro 4 ore dalla classificazione come incidente grave, notifica intermedia entro 72 ore e relazione finale entro un mese dalla risoluzione.

### 1.4 DORA Incident Reporting Overview

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DORA INCIDENT REPORTING FRAMEWORK                        │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  DETECTION                                                                  │
│  ─────────                                                                  │
│       │                                                                     │
│       ▼                                                                     │
│  ┌──────────────────────────────────────────────────────────────────────┐  │
│  │ CLASSIFICATION (Art. 18)                                             │  │
│  │ Is it a MAJOR ICT-related incident?                                  │  │
│  │                                                                       │  │
│  │ Criteria:                                                             │  │
│  │ • Number of clients affected                                         │  │
│  │ • Duration of incident                                                │  │
│  │ • Geographical spread                                                 │  │
│  │ • Data losses                                                         │  │
│  │ • Criticality of services affected                                    │  │
│  │ • Economic impact                                                     │  │
│  └───────────────────────────┬──────────────────────────────────────────┘  │
│                              │                                              │
│           ┌──────────────────┴──────────────────┐                          │
│           │ MAJOR                               │ NOT MAJOR                │
│           ▼                                     ▼                          │
│  ┌──────────────────────────────┐    ┌──────────────────────────────┐     │
│  │ MANDATORY REPORTING (Art.19) │    │ INTERNAL MANAGEMENT          │     │
│  │                              │    │ Log, analyze, remediate      │     │
│  │ ► Initial Notification       │    │ Optional voluntary reporting │     │
│  │ ► Intermediate Report        │    └──────────────────────────────┘     │
│  │ ► Final Report               │                                          │
│  │                              │                                          │
│  │ To: Competent Authority      │                                          │
│  └──────────────────────────────┘                                          │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Incident Management Process (Art. 17)

### 2.1 Incident Lifecycle

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INCIDENT MANAGEMENT LIFECYCLE                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐ │
│  │ 1. DETECTION │──▶│ 2. TRIAGE    │──▶│ 3. ANALYSIS  │──▶│ 4. CONTAIN-  │ │
│  │              │   │              │   │              │   │    MENT      │ │
│  │ Early warning│   │ Classify     │   │ Investigate  │   │ Isolate      │ │
│  │ indicators   │   │ Prioritize   │   │ Root cause   │   │ Limit damage │ │
│  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘ │
│                                                                             │
│  ┌──────────────┐   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐ │
│  │ 5. ERADICATE │──▶│ 6. RECOVERY  │──▶│ 7. POST-     │──▶│ 8. REPORTING │ │
│  │              │   │              │   │    INCIDENT  │   │              │ │
│  │ Remove threat│   │ Restore ops  │   │ Lessons      │   │ Notify if    │ │
│  │              │   │ Validate     │   │ learned      │   │ major        │ │
│  └──────────────┘   └──────────────┘   └──────────────┘   └──────────────┘ │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Ruoli e Responsabilità (Art. 17.4)

| Ruolo | Responsabilità | Escalation |
|-------|----------------|------------|
| **SOC Analyst L1** | Detection, triage iniziale, logging | → L2 per investigazione |
| **SOC Analyst L2** | Investigazione, containment | → L3/CISO per major |
| **Incident Manager** | Coordinamento risposta, comunicazione | → CISO/CEO per crisis |
| **CISO** | Decisioni strategiche, reporting autorità | → CEO per major |
| **IT Operations** | Azioni tecniche, recovery | → CIO per escalation |
| **Legal/Compliance** | Aspetti legali, notifiche | → CEO per crisis |
| **Communications** | Comunicazione esterna | → CEO per approvazione |

### 2.3 Early Warning Indicators (Art. 17.2)

| Categoria | Indicatori | Soglia Alert |
|-----------|------------|--------------|
| **Authentication** | Failed logins spike | > 100/min same account |
| **Network** | Unusual traffic patterns | > 2 std dev from baseline |
| **Endpoint** | Malware detection | Any detection |
| **Data** | Large data transfers | > 1GB outbound unusual |
| **Application** | Error rate spike | > 5x normal rate |
| **Third-party** | Provider alert | Any critical alert |

---

## 3. Classification of Incidents (Art. 18)

### 3.1 Classification Criteria

DORA Art. 18.1 stabilisce i criteri per classificare gli incidenti:

| Criterio (Art. 18.1) | Soglie MAJOR | Soglie Significativo | Soglie Minore |
|---------------------|--------------|---------------------|---------------|
| **(a) Clienti impattati** | > 10% clienti o > 100.000 | 1-10% o 10.000-100.000 | < 1% o < 10.000 |
| **(b) Durata** | > 4 ore servizio critico | 1-4 ore | < 1 ora |
| **(c) Distribuzione geografica** | Multi-paese o nationwide | Regionale | Locale |
| **(d) Perdita dati** | Dati sensibili confermati | Possibile perdita dati | Nessuna perdita |
| **(e) Criticità servizi** | Servizio critico down | Servizio importante degradato | Servizio standard |
| **(f) Impatto economico** | > €100.000 o > 0.1% CET1 | €10.000-100.000 | < €10.000 |

### 3.2 Classification Matrix

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INCIDENT CLASSIFICATION MATRIX                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ IMPATTO                                                                     │
│    ▲                                                                        │
│    │                                                                        │
│    │  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐        │
│ 5  │  │  SIGNIFICATIVO  │  │     MAJOR       │  │     MAJOR       │        │
│    │  │                 │  │                 │  │                 │        │
│    │  └─────────────────┘  └─────────────────┘  └─────────────────┘        │
│    │                                                                        │
│    │  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐        │
│ 4  │  │  SIGNIFICATIVO  │  │  SIGNIFICATIVO  │  │     MAJOR       │        │
│    │  │                 │  │                 │  │                 │        │
│    │  └─────────────────┘  └─────────────────┘  └─────────────────┘        │
│    │                                                                        │
│    │  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐        │
│ 3  │  │     MINORE      │  │  SIGNIFICATIVO  │  │  SIGNIFICATIVO  │        │
│    │  │                 │  │                 │  │                 │        │
│    │  └─────────────────┘  └─────────────────┘  └─────────────────┘        │
│    │                                                                        │
│    │  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐        │
│ 2  │  │     MINORE      │  │     MINORE      │  │  SIGNIFICATIVO  │        │
│    │  │                 │  │                 │  │                 │        │
│    │  └─────────────────┘  └─────────────────┘  └─────────────────┘        │
│    │                                                                        │
│    │  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐        │
│ 1  │  │   TRASCURABILE  │  │     MINORE      │  │     MINORE      │        │
│    │  │                 │  │                 │  │                 │        │
│    │  └─────────────────┘  └─────────────────┘  └─────────────────┘        │
│    │                                                                        │
│    └─────────────────────────────────────────────────────────────────────▶  │
│                         1              3              5       CRITICITÀ     │
│                                                               SERVIZIO      │
│                                                                             │
│ MAJOR = Notifica obbligatoria alle autorità                                │
│ SIGNIFICATIVO = Valutazione per notifica, log dettagliato                  │
│ MINORE = Gestione interna standard                                         │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 3.3 Cyber Threat Classification (Art. 18.3)

| Categoria | Esempi | Priorità Default |
|-----------|--------|------------------|
| **Ransomware** | Encryption, extortion | MAJOR |
| **Data Breach** | Exfiltration confirmed | MAJOR |
| **DDoS** | Service disruption | Valutare durata |
| **APT** | Persistent access | MAJOR |
| **Insider Threat** | Malicious insider | Valutare impatto |
| **Third-Party Compromise** | Vendor breach | Valutare impatto |

---

## 4. Reporting to Authorities (Art. 19)

### 4.1 Reporting Timeline

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DORA INCIDENT REPORTING TIMELINE                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  T0: INCIDENT CLASSIFIED AS MAJOR                                          │
│  ─────────────────────────────────                                          │
│       │                                                                     │
│       ▼                                                                     │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ INITIAL NOTIFICATION (Art. 19.4.a)                                  │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                   │   │
│  │ Deadline: As soon as possible, within 4 HOURS (draft RTS)           │   │
│  │                                                                      │   │
│  │ Content:                                                             │   │
│  │ • Entity identification                                              │   │
│  │ • Date/time of incident and detection                               │   │
│  │ • Type of incident                                                   │   │
│  │ • Initial assessment of impact                                       │   │
│  │ • Actions taken or planned                                           │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│       │                                                                     │
│       ▼ (entro 72 ore dalla classificazione)                               │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ INTERMEDIATE REPORT (Art. 19.4.b)                                   │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                    │   │
│  │ Deadline: Within 72 HOURS from initial notification                 │   │
│  │                                                                      │   │
│  │ Content:                                                             │   │
│  │ • Updated severity and impact assessment                            │   │
│  │ • Indicators of compromise                                          │   │
│  │ • Containment measures taken                                         │   │
│  │ • Service disruption details                                         │   │
│  │ • Client/counterparty notifications made                            │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│       │                                                                     │
│       ▼ (entro 1 mese dalla risoluzione)                                   │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ FINAL REPORT (Art. 19.4.c)                                          │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                        │   │
│  │ Deadline: Within 1 MONTH after incident resolution                  │   │
│  │                                                                      │   │
│  │ Content:                                                             │   │
│  │ • Detailed description of incident                                   │   │
│  │ • Type of threat and root cause                                      │   │
│  │ • Total impact (clients, financial, operational)                    │   │
│  │ • Remediation actions taken                                          │   │
│  │ • Lessons learned and improvements planned                           │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Reporting Authority

| Tipo Entità | Autorità Competente Italia | Portale/Canale |
|-------------|---------------------------|----------------|
| Banche | Banca d'Italia | [Portale BdI] |
| Imprese investimento | CONSOB | [Portale CONSOB] |
| Assicurazioni | IVASS | [Portale IVASS] |
| Fondi pensione | COVIP | [Portale COVIP] |
| Istituti pagamento | Banca d'Italia | [Portale BdI] |

### 4.3 Voluntary Reporting (Art. 19.2)

Anche per incidenti non classificati come MAJOR, le entità **possono** notificare volontariamente:

- Cyber threats significative
- Vulnerabilità gravi scoperte
- Near-miss significativi

---

## 5. Notification Templates

### 5.1 Initial Notification Template

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INITIAL NOTIFICATION - DORA Art. 19.4.a                  │
│                    To be submitted within 4 hours                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ SECTION A: ENTITY INFORMATION                                               │
│ ─────────────────────────────                                               │
│ Entity Name: __________________________________________________________    │
│ LEI Code: _____________________________________________________________    │
│ Entity Type (Art. 2.1): _______________________________________________    │
│ Contact Person: _______________________________________________________    │
│ Contact Email: _____________________ Tel: _____________________________    │
│                                                                             │
│ SECTION B: INCIDENT IDENTIFICATION                                          │
│ ──────────────────────────────────                                          │
│ Internal Incident ID: _________________________________________________    │
│ Date/Time of Incident: ________________________________________________    │
│ Date/Time of Detection: _______________________________________________    │
│ Date/Time Classified as Major: ________________________________________    │
│                                                                             │
│ SECTION C: INCIDENT TYPE                                                    │
│ ────────────────────────                                                    │
│ ☐ Unauthorized access     ☐ Malware/Ransomware    ☐ DDoS                   │
│ ☐ Data breach             ☐ System failure        ☐ Third-party incident   │
│ ☐ Fraud                   ☐ Physical attack       ☐ Other: ____________    │
│                                                                             │
│ SECTION D: INITIAL IMPACT ASSESSMENT                                        │
│ ─────────────────────────────────────                                       │
│ Services affected: ____________________________________________________    │
│ Estimated clients affected: ___________________________________________    │
│ Geographical scope: ___________________________________________________    │
│ Data potentially affected: ☐ Yes ☐ No ☐ Unknown                            │
│ Financial impact (estimate): €_________________________________________    │
│                                                                             │
│ SECTION E: ACTIONS TAKEN                                                    │
│ ────────────────────────                                                    │
│ Immediate actions: ____________________________________________________    │
│ __________________________________________________________________________  │
│ Planned actions: ______________________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION F: CROSS-BORDER IMPACT                                              │
│ ──────────────────────────────                                              │
│ Impact in other EU Member States: ☐ Yes ☐ No ☐ Unknown                     │
│ If yes, which: ________________________________________________________    │
│                                                                             │
│ Submitted by: _________________________ Date/Time: ____________________    │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 5.2 Intermediate Report Template

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INTERMEDIATE REPORT - DORA Art. 19.4.b                   │
│                    To be submitted within 72 hours                          │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ Reference Initial Notification: _______________________________________    │
│ Internal Incident ID: _________________________________________________    │
│                                                                             │
│ SECTION A: UPDATED SEVERITY ASSESSMENT                                      │
│ ──────────────────────────────────────                                      │
│ Current Status: ☐ Ongoing ☐ Contained ☐ Resolved                           │
│ Severity: ☐ Critical ☐ High ☐ Medium ☐ Low                                 │
│                                                                             │
│ Updated Impact Assessment:                                                  │
│ • Clients affected (confirmed): _______________________________________    │
│ • Duration of disruption: _____________________________________________    │
│ • Services status: ____________________________________________________    │
│ • Data loss confirmed: ☐ Yes ☐ No                                          │
│ • If yes, type and volume: ____________________________________________    │
│ • Financial impact (updated): €________________________________________    │
│                                                                             │
│ SECTION B: INDICATORS OF COMPROMISE                                         │
│ ─────────────────────────────────────                                       │
│ IP Addresses: _________________________________________________________    │
│ Domains: ______________________________________________________________    │
│ File Hashes (MD5/SHA256): _____________________________________________    │
│ TTPs (MITRE ATT&CK): __________________________________________________    │
│ Other IoCs: ___________________________________________________________    │
│                                                                             │
│ SECTION C: CONTAINMENT MEASURES                                             │
│ ───────────────────────────────                                             │
│ Measures taken:                                                             │
│ ☐ Systems isolated    ☐ Accounts disabled    ☐ Network segmentation        │
│ ☐ Patches applied     ☐ Malware removed      ☐ Third-party notified        │
│ ☐ Other: ______________________________________________________________    │
│                                                                             │
│ Detailed description: _________________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION D: SERVICE DISRUPTION                                               │
│ ─────────────────────────────                                               │
│ Services disrupted:                                                         │
│ | Service | Start Disruption | End/Ongoing | Clients Impacted |            │
│ |---------|------------------|-------------|------------------|            │
│ |         |                  |             |                  |            │
│                                                                             │
│ SECTION E: CLIENT NOTIFICATIONS                                             │
│ ───────────────────────────────                                             │
│ Clients notified: ☐ Yes ☐ No ☐ In progress                                 │
│ Number notified: _____________________________________________________     │
│ Method: _______________________________________________________________    │
│                                                                             │
│ SECTION F: RECOVERY PLAN                                                    │
│ ────────────────────────                                                    │
│ Estimated time to full recovery: ______________________________________    │
│ Key recovery actions planned: _________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ Submitted by: _________________________ Date/Time: ____________________    │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 5.3 Final Report Template

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FINAL REPORT - DORA Art. 19.4.c                          │
│                    To be submitted within 1 month of resolution             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ Reference Initial Notification: _______________________________________    │
│ Reference Intermediate Report: ________________________________________    │
│ Internal Incident ID: _________________________________________________    │
│ Date Incident Resolved: _______________________________________________    │
│                                                                             │
│ SECTION A: DETAILED INCIDENT DESCRIPTION                                    │
│ ─────────────────────────────────────────                                   │
│ [Provide comprehensive narrative of the incident from detection to         │
│ resolution, including timeline of key events]                              │
│ __________________________________________________________________________  │
│ __________________________________________________________________________  │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION B: THREAT TYPE AND ROOT CAUSE                                       │
│ ──────────────────────────────────────                                      │
│ Threat type: ☐ Cybercrime ☐ State-sponsored ☐ Hacktivist                   │
│              ☐ Insider    ☐ Accidental      ☐ Unknown                      │
│                                                                             │
│ Root cause analysis:                                                        │
│ ☐ Vulnerability (CVE: _____________)                                       │
│ ☐ Misconfiguration                                                          │
│ ☐ Human error                                                               │
│ ☐ Third-party compromise                                                    │
│ ☐ Physical security failure                                                 │
│ ☐ Other: ______________________________________________________________    │
│                                                                             │
│ Detailed root cause: __________________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION C: FINAL IMPACT ASSESSMENT                                          │
│ ──────────────────────────────────                                          │
│ Clients affected (final): _____________________________________________    │
│ Total duration of disruption: _________________________________________    │
│ Data compromised (type and volume): ___________________________________    │
│ Financial impact (total): €____________________________________________    │
│   • Direct costs: €____________________________________________________    │
│   • Recovery costs: €__________________________________________________    │
│   • Estimated indirect costs: €________________________________________    │
│                                                                             │
│ SECTION D: REMEDIATION ACTIONS                                              │
│ ──────────────────────────────                                              │
│ Actions taken to resolve:                                                   │
│ __________________________________________________________________________  │
│ __________________________________________________________________________  │
│                                                                             │
│ Actions taken to prevent recurrence:                                        │
│ __________________________________________________________________________  │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION E: LESSONS LEARNED                                                  │
│ ──────────────────────────                                                  │
│ What worked well: _____________________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ What could be improved: _______________________________________________    │
│ __________________________________________________________________________  │
│                                                                             │
│ SECTION F: IMPROVEMENTS PLANNED                                             │
│ ───────────────────────────────                                             │
│ | Improvement | Owner | Deadline | Status |                                 │
│ |-------------|-------|----------|--------|                                 │
│ |             |       |          |        |                                 │
│ |             |       |          |        |                                 │
│                                                                             │
│ Submitted by: _________________________ Date/Time: ____________________    │
│ Approved by (CISO): ___________________ Date: _________________________    │
│ Approved by (CEO): ____________________ Date: _________________________    │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Client Notification (Art. 19.5)

### 6.1 Quando Notificare i Clienti

La notifica ai clienti è richiesta quando:

| Scenario | Notifica Richiesta | Timeline |
|----------|-------------------|----------|
| Impatto su servizi ai clienti | ✓ | Appena possibile |
| Potenziale rischio per clienti | ✓ | Appena confermato |
| Data breach dati clienti | ✓ | Coordinare con GDPR |
| Misure che clienti possono adottare | ✓ | Con le istruzioni |

### 6.2 Template Comunicazione Clienti

```
OGGETTO: Informativa su incidente operativo - [Nome Servizio]

Gentile Cliente,

La informiamo che in data {{document_date}} abbiamo rilevato un incidente che ha
interessato [DESCRIZIONE GENERALE DEL SERVIZIO].

COSA È SUCCESSO
[Descrizione sintetica, chiara e non tecnica]

QUALI SERVIZI SONO STATI INTERESSATI
[Elenco servizi, periodo di disservizio]

QUALI DATI POTREBBERO ESSERE STATI INTERESSATI
[Solo se applicabile - tipologia dati, non quantità sensibili]

COSA ABBIAMO FATTO
[Azioni intraprese per risolvere e prevenire]

COSA PUÒ FARE LEI
[Azioni raccomandate: cambio password, monitoraggio, etc.]

PROSSIMI PASSI
[Tempistiche previste, ulteriori comunicazioni]

Per informazioni: {{dedicated_contact}}

Cordiali saluti,
[FIRMA]
```

---

## 7. Payment-Related Incidents (Art. 23)

### 7.1 Applicabilità

Art. 23 si applica a:
- Istituti di pagamento
- Prestatori servizi informazione conti
- Istituti di moneta elettronica

### 7.2 Coordinamento con PSD2

| Incidente | DORA | PSD2 |
|-----------|------|------|
| Major ICT incident | Notifica autorità DORA | + Notifica BCE se significativo |
| Operational incident | Classificare come ICT | Notifica secondo PSD2 se payment |
| Security incident | Processo DORA | Coordinare con EBA guidelines |

---

## 8. Registro Incidenti (Art. 17.3)

### 8.1 Template Registro

| ID | Data Rilev. | Tipo | Classificazione | Servizi Impattati | Clienti | Durata | Status | Initial Notif | Final Report |
|----|-------------|------|-----------------|-------------------|---------|--------|--------|---------------|--------------|
| | | | ☐ Major ☐ Signif ☐ Minor | | | | | ☐ Inviata | ☐ Inviato |

### 8.2 Retention

- Registro incidenti: 5 anni
- Documentazione Major incidents: 7 anni
- Notifiche alle autorità: 7 anni
- Evidenze tecniche: 5 anni

---

## 9. Post-Incident Review (Art. 12)

### 9.1 Post-Incident Review Template

| Sezione | Contenuto |
|---------|-----------|
| **Incident Summary** | ID, timeline, impatto |
| **What Happened** | Cronologia dettagliata |
| **Root Cause** | Analisi causa radice |
| **Detection** | Come rilevato, tempo detection |
| **Response** | Efficacia risposta |
| **Communication** | Efficacia comunicazione |
| **What Worked Well** | Punti di forza |
| **What Could Improve** | Aree di miglioramento |
| **Action Items** | Azioni, owner, deadline |

### 9.2 KPI Incident Management

| KPI | Target | Actual | Trend |
|-----|--------|--------|-------|
| Mean Time to Detect (MTTD) | < 1h | | |
| Mean Time to Classify | < 4h | | |
| Initial Notification SLA | 100% | | |
| Mean Time to Contain | < 4h | | |
| Mean Time to Resolve | < 24h | | |
| Post-Incident Review completion | 100% | | |
| Recurrence rate | < 5% | | |

---

## 10. Documenti Correlati

| Documento | Riferimento |
|-----------|-------------|
| ICT Risk Management Framework | DOC-ICT-001 |
| Incident Response Plan | PLA-INC-001 |
| Crisis Communication Plan | PLA-CRI-001 |
| Business Continuity Plan | PLA-BC-001 |
| GDPR Breach Procedure | PRO-GDPR-001 |

---

## 11. Revisione e Approvazione

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | | | |
| Verificato da (Compliance) | | | |
| Approvato da (CISO) | | | |
| Approvato da (Management Body) | | | |

---

*Questa procedura deve essere testata almeno annualmente e revisionata in caso di modifiche normative o a seguito di incidenti significativi.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| dora-ict-risk-management-framework.md | Framework gestione rischio ICT |
| dora-compliance-checklist.md | Checklist conformita DORA completa |
| dora-governance-oversight.md | Governance e supervisione |
| dora-digital-resilience-testing.md | Test resilienza operativa |
| dora-ict-third-party-risk.md | Incidenti con impatto terze parti |
| dora-isms-integration-guide.md | Integrazione con ISMS |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter | Data del documento |
| `{{document_author}}` | Revision History | Autore del documento |
| Classification thresholds | Sez. 3 | Definire soglie Art. 18 (clienti, transazioni, durata) |
| Escalation matrix | Sez. 4 | Matrice escalation per severita |
| Reporting timelines | Sez. 5 | Template notifiche (iniziale 4h, intermedia, finale 1 mese) |
| CSIRT contacts | Sez. 6 | Contatti CSIRT/autorita competente |
| Post-incident review | Sez. 7 | Processo root cause analysis |
| KPI targets | Sez. 8 | Target metriche incidentali |
| Firme approvazione | Sez. finale | Firme CISO, Compliance, Management Body |
