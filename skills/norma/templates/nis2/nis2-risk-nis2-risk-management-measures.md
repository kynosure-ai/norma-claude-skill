---
title: NIS2 Misure di Gestione del Rischio
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: CISO
approver: Alta Direzione
framework: NIS2
language: IT
documentType: procedure
directive_articles:
  - Art. 21 - Misure di gestione del rischio cybersecurity
  - Considerando 79-83 - Approccio alla gestione del rischio
national_transposition: D.Lgs. 138/2024
cross_references:
  - 'ISO 27001:2022'
  - 'ISO 27005:2022'
  - NIST CSF 2.0
  - Linee guida ENISA Risk Management
  - D.Lgs. 138/2024 Art. 24 - Misure di gestione del rischio
related_documents:
  - document: NIS2 Governance & Accountability
    path: ../governance/nis2-governance-accountability.md
  - document: NIS2 Incident Reporting
    path: ../incidents/nis2-incident-reporting.md
  - document: NIS2 Business Continuity Plan
    path: ../continuity/nis2-business-continuity-plan.md
  - document: NIS2 Supply Chain Security
    path: ../supply-chain/nis2-supply-chain-security.md
  - document: NIS2 Compliance Checklist
    path: ../compliance/nis2-compliance-checklist.md
  - document: NIS2 ISMS Integration Guide
    path: ../context/nis2-isms-integration-guide.md
status: Bozza
subset: true
---

# NIS2 Risk Management Measures

## 1. Introduzione

### 1.1 Scopo

{{company_name}} riconosce che la gestione efficace dei rischi di cybersecurity costituisce un pilastro fondamentale per la protezione dei servizi essenziali e importanti forniti ai propri stakeholder. L'Articolo 21 della Direttiva (UE) 2022/2555 stabilisce un quadro completo di misure tecniche, operative e organizzative che le entità soggette alla NIS2 devono implementare, adottando un approccio proporzionato al rischio e allo stato dell'arte delle tecnologie disponibili.

Il presente documento definisce le misure che {{company_name}} implementa per rispondere ai dieci ambiti specifici elencati nell'Articolo 21.2, dalla gestione del rischio alla sicurezza della supply chain, dalla business continuity alla crittografia. L'approccio adottato segue il principio "all-hazards" richiesto dalla Direttiva, considerando non solo le minacce cyber, ma anche i rischi fisici e ambientali che possono compromettere la sicurezza dei sistemi informativi e di rete.

L'organizzazione calibra l'intensità delle misure in base ai criteri di proporzionalità stabiliti dall'Articolo 21.1, tenendo conto dell'esposizione al rischio, delle dimensioni aziendali, della probabilità di incidenti e della gravità dei potenziali impatti economici e sociali. Questo documento costituisce il riferimento operativo per l'implementazione dei controlli e per la dimostrazione di conformità alle autorità competenti.

### 1.2 Ambito di Applicazione

- Tutti i sistemi informativi e di rete che supportano servizi critici
- Processi operativi correlati alla sicurezza delle informazioni
- Personale, fornitori e terze parti con accesso ai sistemi

### 1.3 Riferimenti Normativi

| Riferimento | Descrizione |
|-------------|-------------|
| NIS2 Art. 21 | Misure di gestione del rischio cybersecurity |
| D.Lgs. 138/2024 | Recepimento NIS2 in Italia |
| ISO 27001:2022 | Sistema di gestione sicurezza informazioni |
| ISO 27005:2022 | Gestione del rischio sicurezza informazioni |
| ENISA Guidelines | Linee guida settoriali |

---

## 2. Framework di Risk Management

### 2.1 Approccio All-Hazards

In conformità al Recital 79 NIS2, l'organizzazione adotta un approccio "all-hazards" che considera:

```
┌─────────────────────────────────────────────────────────────────┐
│                    ALL-HAZARDS APPROACH                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐          │
│  │   CYBER      │  │   FISICO     │  │  AMBIENTALE  │          │
│  │   THREATS    │  │   THREATS    │  │   THREATS    │          │
│  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘          │
│         │                 │                 │                   │
│         ▼                 ▼                 ▼                   │
│  ┌─────────────────────────────────────────────────┐           │
│  │            RISK ASSESSMENT UNIFICATO            │           │
│  └──────────────────────┬──────────────────────────┘           │
│                         │                                       │
│                         ▼                                       │
│  ┌─────────────────────────────────────────────────┐           │
│  │          MISURE PROPORZIONATE AL RISCHIO        │           │
│  └─────────────────────────────────────────────────┘           │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 2.2 Principio di Proporzionalità

Le misure sono determinate considerando (Art. 21.1):

| Fattore | Descrizione | Valutazione |
|---------|-------------|-------------|
| **Esposizione al rischio** | Probabilità e frequenza minacce | {{risk_assessment_value}} |
| **Dimensione dell'entità** | Numero dipendenti, fatturato | {{risk_assessment_value}} |
| **Probabilità incidenti** | Storico, threat intelligence | {{risk_assessment_value}} |
| **Gravità impatti** | Economico, sociale, safety | {{risk_assessment_value}} |
| **Stato dell'arte** | Tecnologie disponibili | {{risk_assessment_value}} |
| **Costo implementazione** | Budget, risorse necessarie | {{risk_assessment_value}} |
| **Standard applicabili** | Norme europee/internazionali | {{risk_assessment_value}} |

---

## 3. Misure Art. 21.2 - Dettaglio Implementativo

### 3.1 Politiche di Analisi Rischi e Sicurezza (Art. 21.2.a)

#### 3.1.1 Documentazione Richiesta

| Documento | Contenuto | Stato | Owner |
|-----------|-----------|-------|-------|
| Information Security Policy | Principi, obiettivi, commitment | ☐ Da creare ☐ Esistente | |
| Risk Assessment Methodology | Criteri, scale, processo | ☐ Da creare ☐ Esistente | |
| Risk Register | Registro rischi identificati | ☐ Da creare ☐ Esistente | |
| Risk Treatment Plan | Piano trattamento rischi | ☐ Da creare ☐ Esistente | |
| Acceptable Use Policy | Uso accettabile risorse IT | ☐ Da creare ☐ Esistente | |

#### 3.1.2 Processo di Risk Assessment

```
┌─────────────────────────────────────────────────────────────────┐
│                   RISK ASSESSMENT PROCESS                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   ┌───────────────┐                                             │
│   │ 1. CONTEXT    │  • Asset inventory                         │
│   │ ESTABLISHMENT │  • Threat landscape                        │
│   └───────┬───────┘  • Vulnerability assessment                │
│           │                                                     │
│           ▼                                                     │
│   ┌───────────────┐                                             │
│   │ 2. RISK       │  • Threat identification                   │
│   │ IDENTIFICATION│  • Vulnerability identification            │
│   └───────┬───────┘  • Consequence identification              │
│           │                                                     │
│           ▼                                                     │
│   ┌───────────────┐                                             │
│   │ 3. RISK       │  • Likelihood assessment                   │
│   │ ANALYSIS      │  • Impact assessment                       │
│   └───────┬───────┘  • Risk level determination                │
│           │                                                     │
│           ▼                                                     │
│   ┌───────────────┐                                             │
│   │ 4. RISK       │  • Risk prioritization                     │
│   │ EVALUATION    │  • Acceptance criteria comparison          │
│   └───────┬───────┘                                             │
│           │                                                     │
│           ▼                                                     │
│   ┌───────────────┐                                             │
│   │ 5. RISK       │  • Mitigation                              │
│   │ TREATMENT     │  • Transfer (insurance)                    │
│   └───────────────┘  • Avoidance / Acceptance                  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

#### 3.1.3 Scala di Valutazione

**Probabilità:**

| Livello | Valore | Descrizione | Frequenza Indicativa |
|---------|--------|-------------|---------------------|
| Molto Bassa | 1 | Evento raro | < 1 volta in 10 anni |
| Bassa | 2 | Evento improbabile | 1 volta in 5-10 anni |
| Media | 3 | Evento possibile | 1 volta in 1-5 anni |
| Alta | 4 | Evento probabile | 1-5 volte l'anno |
| Molto Alta | 5 | Evento quasi certo | > 5 volte l'anno |

**Impatto:**

| Livello | Valore | Operativo | Finanziario | Reputazionale | Safety |
|---------|--------|-----------|-------------|---------------|--------|
| Trascurabile | 1 | < 1h downtime | < €10K | Nessuno | Nessuno |
| Minore | 2 | 1-8h downtime | €10K-50K | Locale | Minori |
| Moderato | 3 | 8h-1gg downtime | €50K-250K | Regionale | Significativi |
| Significativo | 4 | 1-5gg downtime | €250K-1M | Nazionale | Gravi |
| Critico | 5 | > 5gg downtime | > €1M | Internazionale | Perdite umane |

**Matrice di Rischio:**

| | Impatto 1 | Impatto 2 | Impatto 3 | Impatto 4 | Impatto 5 |
|---|---|---|---|---|---|
| **Prob. 5** | 5 (M) | 10 (M) | 15 (H) | 20 (VH) | 25 (VH) |
| **Prob. 4** | 4 (L) | 8 (M) | 12 (H) | 16 (H) | 20 (VH) |
| **Prob. 3** | 3 (L) | 6 (M) | 9 (M) | 12 (H) | 15 (H) |
| **Prob. 2** | 2 (L) | 4 (L) | 6 (M) | 8 (M) | 10 (M) |
| **Prob. 1** | 1 (L) | 2 (L) | 3 (L) | 4 (L) | 5 (M) |

**Legenda:** L = Low (1-4), M = Medium (5-10), H = High (11-16), VH = Very High (17-25)

#### 3.1.4 Criteri di Accettazione

| Livello Rischio | Azione Richiesta | Approvazione |
|-----------------|------------------|--------------|
| Low (1-4) | Accettazione con monitoraggio | Risk Owner |
| Medium (5-10) | Trattamento entro 6 mesi | CISO |
| High (11-16) | Trattamento entro 3 mesi | CIO + CISO |
| Very High (17-25) | Trattamento immediato | CEO/AD |

---

### 3.2 Gestione degli Incidenti (Art. 21.2.b)

#### 3.2.1 Capability Requirements

| Capability | Descrizione | Implementazione |
|------------|-------------|-----------------|
| **Detection** | Rilevamento tempestivo incidenti | SIEM, EDR, NDR, SOC |
| **Analysis** | Analisi e classificazione | Playbooks, triage procedures |
| **Containment** | Contenimento impatto | Isolation procedures, segmentation |
| **Eradication** | Eliminazione minaccia | Remediation procedures |
| **Recovery** | Ripristino operatività | DR procedures, backup restore |
| **Lessons Learned** | Miglioramento continuo | Post-incident review |

#### 3.2.2 Classificazione Incidenti

| Categoria | Esempi | Priorità | SLA Response |
|-----------|--------|----------|--------------|
| **P1 - Critical** | Ransomware attivo, breach dati massivo | Critica | 15 min |
| **P2 - High** | Compromissione sistema critico | Alta | 1 ora |
| **P3 - Medium** | Malware isolato, phishing riuscito | Media | 4 ore |
| **P4 - Low** | Tentativo fallito, vulnerability | Bassa | 24 ore |

#### 3.2.3 Incident Response Team

| Ruolo | Responsabilità | Contatto |
|-------|----------------|----------|
| Incident Manager | Coordinamento risposta | {{contact_info}} |
| Security Analyst | Analisi tecnica | {{contact_info}} |
| System Administrator | Azioni tecniche | {{contact_info}} |
| Communications Lead | Comunicazioni interne/esterne | {{contact_info}} |
| Legal Advisor | Aspetti legali, notifiche | {{contact_info}} |
| Executive Sponsor | Decisioni strategiche | {{contact_info}} |

---

### 3.3 Business Continuity (Art. 21.2.c)

#### 3.3.1 Business Impact Analysis (BIA)

| Processo/Servizio | RTO | RPO | MTPD | Criticità | Dipendenze |
|-------------------|-----|-----|------|-----------|------------|
| [Servizio 1] | | | | ☐ Critico ☐ Alto ☐ Medio ☐ Basso | |
| [Servizio 2] | | | | ☐ Critico ☐ Alto ☐ Medio ☐ Basso | |
| [Servizio 3] | | | | ☐ Critico ☐ Alto ☐ Medio ☐ Basso | |

**Legenda:**
- **RTO** (Recovery Time Objective): Tempo massimo per ripristino
- **RPO** (Recovery Point Objective): Massima perdita dati accettabile
- **MTPD** (Maximum Tolerable Period of Disruption): Periodo massimo interruzione

#### 3.3.2 Strategie di Recovery

| Strategia | RTO Tipico | Costo | Scenario |
|-----------|------------|-------|----------|
| Hot Site | < 1 ora | Alto | Servizi mission-critical |
| Warm Site | 1-24 ore | Medio | Servizi critici |
| Cold Site | 24-72 ore | Basso | Servizi importanti |
| Cloud DR | < 4 ore | Variabile | Workload cloud-based |

#### 3.3.3 Backup Strategy

| Tipo Backup | Frequenza | Retention | Verifica | Storage |
|-------------|-----------|-----------|----------|---------|
| Full | Settimanale | 12 mesi | Mensile | Offsite + Cloud |
| Incremental | Giornaliero | 30 giorni | Settimanale | Onsite + Cloud |
| Database | Orario | 7 giorni | Giornaliera | Onsite |
| Config | Ad ogni modifica | Illimitato | Trimestrale | Repository |

---

### 3.4 Supply Chain Security (Art. 21.2.d)

#### 3.4.1 Supplier Classification

| Categoria | Criteri | Valutazione Richiesta | Frequenza Review |
|-----------|---------|----------------------|------------------|
| **Critico** | Accesso a dati sensibili, servizi essenziali | Full assessment + audit | Annuale |
| **Alto** | Accesso a sistemi produzione | Assessment + questionnaire | Annuale |
| **Medio** | Accesso limitato, supporto | Questionnaire | Biennale |
| **Basso** | Nessun accesso IT | Auto-dichiarazione | All'onboarding |

#### 3.4.2 Security Requirements per Contratti

| Requisito | Obbligatorio per | Clausola Tipo |
|-----------|------------------|---------------|
| NDA / Riservatezza | Tutti | Standard |
| Certificazione ISO 27001 | Critici | Preferenziale |
| Incident notification | Critici, Alti | 24-48 ore |
| Audit right | Critici | Annuale |
| Pen test report | Critici | Annuale |
| SBOM (Software) | Sviluppatori | Per release |
| Subcontractor approval | Critici | Pre-autorizzazione |
| Data localization | Dati personali | EU/EEA |
| Exit plan | Tutti | Documentato |

#### 3.4.3 Supplier Risk Assessment

| Fattore | Peso | Score (1-5) | Weighted |
|---------|------|-------------|----------|
| Accesso a dati critici | 25% | | |
| Dipendenza operativa | 20% | | |
| Maturità security fornitore | 20% | | |
| Storico incidenti | 15% | | |
| Concentrazione geografica | 10% | | |
| Sostituibilità | 10% | | |
| **TOTALE** | 100% | | |

---

### 3.5 Sicurezza Acquisizione, Sviluppo, Manutenzione (Art. 21.2.e)

#### 3.5.1 Secure Development Lifecycle (SDLC)

```
┌────────────────────────────────────────────────────────────────────────┐
│                        SECURE SDLC                                     │
├────────────────────────────────────────────────────────────────────────┤
│                                                                        │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌───────┐│
│  │ PLANNING │──▶│  DESIGN  │──▶│   DEV    │──▶│  TEST    │──▶│DEPLOY ││
│  └────┬─────┘   └────┬─────┘   └────┬─────┘   └────┬─────┘   └───┬───┘│
│       │              │              │              │              │    │
│       ▼              ▼              ▼              ▼              ▼    │
│  Security       Threat         SAST/SCA       DAST/IAST      Security │
│  Requirements   Modeling       Code Review    Pen Test       Config   │
│                                                                        │
└────────────────────────────────────────────────────────────────────────┘
```

#### 3.5.2 Vulnerability Management

| Severità | CVSS | SLA Remediation | Escalation |
|----------|------|-----------------|------------|
| Critical | 9.0-10.0 | 24-72 ore | CISO immediato |
| High | 7.0-8.9 | 7 giorni | CISO settimanale |
| Medium | 4.0-6.9 | 30 giorni | Team Lead |
| Low | 0.1-3.9 | 90 giorni | Backlog |

#### 3.5.3 Patch Management

| Sistema | Finestra Patching | Test Required | Approval |
|---------|-------------------|---------------|----------|
| Production Critical | Weekend pianificato | Staging test | CAB |
| Production Standard | Settimanale | Limited test | Change Manager |
| Development | Bi-settimanale | None | Team Lead |
| Security Patches | Emergency window | Minimal | CISO |

---

### 3.6 Valutazione Efficacia Misure (Art. 21.2.f)

#### 3.6.1 Security Testing Program

| Tipo Test | Frequenza | Scope | Responsabile |
|-----------|-----------|-------|--------------|
| Vulnerability Scan | Mensile | Tutti i sistemi | Security Team |
| Penetration Test | Annuale | Perimetro + critici | External |
| Red Team Exercise | Biennale | Full scope | External |
| Phishing Simulation | Trimestrale | Tutti i dipendenti | Security Team |
| BC/DR Test | Annuale | Servizi critici | IT Operations |
| Tabletop Exercise | Semestrale | Management | CISO |

#### 3.6.2 Security Metrics (KPI)

| KPI | Target | Frequenza | Owner |
|-----|--------|-----------|-------|
| Mean Time to Detect (MTTD) | < 24h | Mensile | SOC |
| Mean Time to Respond (MTTR) | < 4h | Mensile | SOC |
| Patch Compliance Rate | > 95% | Mensile | IT Ops |
| Phishing Click Rate | < 5% | Trimestrale | Security |
| Security Training Completion | 100% | Trimestrale | HR |
| Vulnerability SLA Compliance | > 90% | Mensile | Security |
| Incident Recurrence Rate | < 5% | Trimestrale | CISO |
| Backup Success Rate | > 99% | Mensile | IT Ops |

---

### 3.7 Cyber Hygiene e Formazione (Art. 21.2.g)

#### 3.7.1 Security Awareness Program

| Modulo | Target | Frequenza | Durata | Obbligatorio |
|--------|--------|-----------|--------|--------------|
| Security Fundamentals | Tutti | Annuale | 2h | ✓ |
| Phishing Awareness | Tutti | Semestrale | 1h | ✓ |
| Data Protection | Tutti | Annuale | 1h | ✓ |
| Secure Development | Sviluppatori | Annuale | 4h | ✓ |
| Incident Response | IT Staff | Annuale | 2h | ✓ |
| Executive Security | Management | Annuale | 1h | ✓ |
| Social Engineering | Customer-facing | Semestrale | 1h | ✓ |

#### 3.7.2 Cyber Hygiene Practices

| Practice | Implementazione | Enforcement |
|----------|-----------------|-------------|
| Password Policy | Min 12 char, complexity, no reuse | Technical |
| MFA Enforcement | Tutti gli accessi privilegiati | Technical |
| Screen Lock | Automatico dopo 5 min | GPO |
| Clean Desk | Policy + audit spot | Administrative |
| Software Updates | Automatici, finestre definite | Technical |
| Email Security | SPF, DKIM, DMARC, filtering | Technical |
| Endpoint Protection | EDR su tutti i dispositivi | Technical |

---

### 3.8 Crittografia (Art. 21.2.h)

#### 3.8.1 Cryptographic Standards

| Uso | Algoritmo Approvato | Lunghezza Chiave Min | Deprecato |
|-----|---------------------|---------------------|-----------|
| Symmetric Encryption | AES | 256-bit | DES, 3DES, RC4 |
| Asymmetric Encryption | RSA, ECDSA | RSA-2048, ECDSA-256 | RSA-1024 |
| Hashing | SHA-256, SHA-3 | 256-bit | MD5, SHA-1 |
| TLS | TLS 1.2, TLS 1.3 | - | TLS 1.0, 1.1, SSL |
| Key Exchange | ECDHE, DHE | ECDHE-256, DHE-2048 | Static DH |

#### 3.8.2 Encryption Requirements

| Dati | At Rest | In Transit | In Use |
|------|---------|------------|--------|
| Dati personali (GDPR) | ✓ AES-256 | ✓ TLS 1.2+ | Consider |
| Credenziali | ✓ Hashed + Salt | ✓ TLS 1.2+ | N/A |
| Dati finanziari | ✓ AES-256 | ✓ TLS 1.2+ | Consider |
| Backup | ✓ AES-256 | ✓ TLS 1.2+ | N/A |
| Email sensibili | Recommended | ✓ TLS | S/MIME optional |

#### 3.8.3 Key Management

| Processo | Responsabile | Frequenza |
|----------|--------------|-----------|
| Key Generation | Security Team | On demand |
| Key Distribution | Automated (KMS) | As needed |
| Key Rotation | Automated | Annuale / policy |
| Key Revocation | Security Team | On incident |
| Key Backup | IT Operations | Con backup dati |
| Key Destruction | Security Team | End of life |

---

### 3.9 Sicurezza Risorse Umane e Controllo Accessi (Art. 21.2.i)

#### 3.9.1 HR Security Controls

| Fase | Controllo | Implementazione |
|------|-----------|-----------------|
| **Pre-employment** | Background check | Ruoli critici |
| | Verifica qualifiche | Tutti |
| | NDA | Tutti |
| **During employment** | Security training | Annuale |
| | Access review | Trimestrale |
| | Performance monitoring | Continuo |
| **Termination** | Exit interview | Tutti |
| | Access revocation | Immediato (24h) |
| | Asset return | Ultimo giorno |
| | Knowledge transfer | Pianificato |

#### 3.9.2 Access Control Model

| Principio | Implementazione |
|-----------|-----------------|
| **Least Privilege** | Accessi minimi necessari per il ruolo |
| **Need-to-Know** | Accesso a informazioni solo se necessario |
| **Separation of Duties** | Separazione funzioni incompatibili |
| **Dual Control** | Doppia approvazione per operazioni critiche |

#### 3.9.3 Privileged Access Management (PAM)

| Controllo | Implementazione | Tool |
|-----------|-----------------|------|
| Privileged Account Inventory | Censimento completo | {{tool_name}} |
| Just-in-Time Access | Accessi temporanei | {{tool_name}} |
| Session Recording | Registrazione sessioni admin | {{tool_name}} |
| Password Vaulting | Gestione centralizzata password | {{tool_name}} |
| Privileged Access Review | Revisione trimestrale | {{process_name}} |

---

### 3.10 MFA e Comunicazioni Sicure (Art. 21.2.j)

#### 3.10.1 Multi-Factor Authentication

| Sistema/Accesso | MFA Richiesto | Metodo Preferito |
|-----------------|---------------|------------------|
| VPN | ✓ Obbligatorio | TOTP / Push |
| Cloud Admin Console | ✓ Obbligatorio | FIDO2 / Push |
| Email (web) | ✓ Obbligatorio | TOTP / Push |
| Privileged Systems | ✓ Obbligatorio | FIDO2 / Smart Card |
| Critical Applications | ✓ Obbligatorio | Risk-based |
| Standard Workstation | Recommended | Windows Hello |

#### 3.10.2 Secure Communications

| Tipo Comunicazione | Soluzione | Crittografia |
|--------------------|-----------|--------------|
| Email interna | Exchange/M365 | TLS + S/MIME optional |
| Email esterna | Gateway encryption | TLS required |
| Instant Messaging | Teams / Slack | E2E encryption |
| Video Conference | Teams / Zoom | E2E encryption |
| Voice (VoIP) | Teams / SIP | SRTP |
| File Sharing | SharePoint / OneDrive | At-rest + in-transit |
| Emergency Comms | {{emergency_comms_solution}} | Encrypted |

---

## 4. Implementazione e Monitoraggio

### 4.1 Piano di Implementazione

| Priorità | Misura | Stato Attuale | Target | Owner | Deadline |
|----------|--------|---------------|--------|-------|----------|
| 1 | Risk Assessment | | | | |
| 1 | Incident Response | | | | |
| 1 | MFA Implementation | | | | |
| 2 | Vulnerability Management | | | | |
| 2 | Security Awareness | | | | |
| 2 | Backup & DR | | | | |
| 3 | Supply Chain Security | | | | |
| 3 | PAM Implementation | | | | |

### 4.2 Monitoraggio Continuo

| Attività | Frequenza | Output |
|----------|-----------|--------|
| Security Dashboard Review | Giornaliera | Anomaly detection |
| KPI Review | Mensile | Performance report |
| Risk Register Update | Trimestrale | Updated risk register |
| Control Effectiveness Review | Semestrale | Control assessment |
| Framework Review | Annuale | Updated framework |

---

## 5. Documentazione Correlata

| Documento | Riferimento |
|-----------|-------------|
| Information Security Policy | POL-SEC-001 |
| Risk Assessment Methodology | PRO-RISK-001 |
| Incident Response Plan | PLA-INC-001 |
| Business Continuity Plan | PLA-BC-001 |
| Supplier Security Policy | POL-SUP-001 |
| Access Control Policy | POL-ACC-001 |
| Cryptographic Policy | POL-CRY-001 |

---

## 6. Revisione e Approvazione

### 6.1 Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

### 6.2 Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | | | |
| Verificato da | | | |
| Approvato da | | | |

---

*Questo documento deve essere rivisto almeno 1 volta l'anno o in caso di modifiche significative al contesto di rischio, all'organizzazione o al framework normativo. Le scale di rischio e i criteri di accettazione devono essere approvati dal CdA.*

---

## 7. Requisiti Settoriali per le Misure di Sicurezza

### 7.1 Energia (Allegato I, Settore 1)

| Misura Aggiuntiva | Dettaglio | Standard/Riferimento |
|-------------------|-----------|---------------------|
| Sicurezza OT/SCADA | Segregazione rete OT/IT, monitoraggio protocolli industriali | IEC 62443, NERC CIP |
| Physical security impianti | Controllo accessi fisici a cabine, centrali, sottostazioni | D.Lgs. 81/2008 |
| Resilienza rete elettrica | Ridondanza N+1 per sistemi di controllo | Reg. UE 2019/943 |
| Continuità fornitura | RTO <= 4 ore per servizi essenziali di distribuzione | ARERA delibere |

### 7.2 Settore Bancario e Finanziario (Allegato I, Settore 4)

| Misura Aggiuntiva | Dettaglio | Standard/Riferimento |
|-------------------|-----------|---------------------|
| TLPT (Threat-Led Penetration Testing) | Test avanzati su base intelligence per enti significativi | DORA Art. 26, TIBER-EU |
| ICT concentration risk | Valutazione rischio concentrazione fornitori ICT | DORA Art. 29 |
| Digital resilience testing | Programma test resilienza digitale annuale | DORA Art. 24-25 |
| Transaction monitoring | Monitoraggio frodi real-time su transazioni | PSD2, Circ. Banca d'Italia 285 |

### 7.3 Sanitario (Allegato I, Settore 5)

| Misura Aggiuntiva | Dettaglio | Standard/Riferimento |
|-------------------|-----------|---------------------|
| Medical device security | Inventario e patching dispositivi medici connessi | Reg. UE 2017/745 (MDR) |
| Dati sanitari encryption | Crittografia obbligatoria per dati sanitari art. 9 GDPR | GDPR Art. 9, 32 |
| Resilienza cartelle cliniche | RPO = 0, RTO <= 1 ora per sistemi EHR | Min. Salute |
| Patient safety | Procedure di fallback manuale per sistemi critici | Clinical governance |

### 7.4 Infrastrutture Digitali (Allegato I, Settore 8)

| Misura Aggiuntiva | Dettaglio | Standard/Riferimento |
|-------------------|-----------|---------------------|
| Multi-tenant isolation | Isolamento completo tra tenant, no lateral movement | ACN Qualificazione |
| DDoS mitigation | Capacità di mitigazione >= 10x traffico normale | Best practice ENISA |
| Georidondanza | Data center in zone sismiche diverse, distanza >= 200 km | AgID Circ. 1/2019 |
| SLA monitoring | Monitoraggio 24/7 con alerting automatico sotto soglia 99.9% | Contrattuale |

### 7.5 Gestione Servizi ICT B2B (Allegato I, Settore 10)

| Misura Aggiuntiva | Dettaglio | Standard/Riferimento |
|-------------------|-----------|---------------------|
| Client access segregation | Separazione logica accessi per ogni cliente NIS2 | SOC 2 Type II |
| Incident isolation | Capacità di isolare impatto incidente per singolo cliente | Best practice |
| Supply chain transparency | SBOM e disclosure vulnerabilità ai clienti NIS2 | CRA Art. 11 |
| Security service catalog | Catalogo servizi security con SLA definiti per livello | Contrattuale |

---

## 8. Documenti Correlati

| Documento | Tipo | Percorso |
|-----------|------|----------|
| NIS2 Governance & Accountability | Policy | `../governance/nis2-governance-accountability.md` |
| NIS2 Incident Reporting | Procedura | `../incidents/nis2-incident-reporting.md` |
| NIS2 Business Continuity Plan | Piano | `../continuity/nis2-business-continuity-plan.md` |
| NIS2 Supply Chain Security | Policy | `../supply-chain/nis2-supply-chain-security.md` |
| NIS2 Compliance Checklist | Checklist | `../compliance/nis2-compliance-checklist.md` |
| NIS2 Scope & Applicability | Assessment | `../context/nis2-scope-applicability.md` |
| NIS2 ISMS Integration Guide | Guida | `../context/nis2-isms-integration-guide.md` |
| NIS2 Internal Audit Programme | Piano | `../audit/nis2-internal-audit-programme.md` |

---

## 9. Checklist di Compilazione

Prima di considerare questo documento completo, verificare che tutti i campi siano stati personalizzati:

| # | Placeholder | Sezione | Descrizione |
|---|-------------|---------|-------------|
| 1 | `{{company_name}}` | 1.1 | Ragione sociale dell'organizzazione |
| 2 | `{{document_date}}` | Frontmatter, 6.1 | Data emissione documento |
| 3 | `{{document_author}}` | 6.1 | Autore del documento |
| 4 | `{{risk_assessment_value}}` | 2.2 | Valutazioni specifiche di proporzionalità (7 campi) |
| 5 | `{{contact_info}}` | 3.2.3 | Contatti dei membri dell'Incident Response Team (6 campi) |
| 6 | `{{tool_name}}` | 3.9.3 | Nomi dei tool PAM utilizzati (4 campi) |
| 7 | `{{process_name}}` | 3.9.3 | Nome del processo di privileged access review |
| 8 | `{{emergency_comms_solution}}` | 3.10.2 | Soluzione di comunicazione di emergenza |
| 9 | Tabella BIA (3.3.1) | 3.3.1 | Completare RTO/RPO/MTPD per ogni servizio |
| 10 | Piano Implementazione (4.1) | 4.1 | Completare stato, target, owner e deadline per ogni misura |
| 11 | Sezione 7 | 7 | Selezionare il proprio settore e verificare requisiti settoriali |
| 12 | Approvazioni (6.2) | 6.2 | Completare nomi e firme di approvazione |
