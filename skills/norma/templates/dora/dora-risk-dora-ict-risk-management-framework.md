---
title: DORA ICT Risk Management Framework
version: '1.1'
date: '{{document_date}}'
classification: Riservato
owner: CISO
approver: Organo di Gestione
framework: DORA
language: IT
documentType: procedure
regulation_articles:
  - Art. 5 - Quadro di gestione del rischio ICT
  - 'Art. 6 - Sistemi, protocolli e strumenti ICT'
  - Art. 7 - Identificazione
  - Art. 8 - Protezione e prevenzione
  - Art. 9 - Rilevamento
  - Art. 10 - Risposta e ripristino
  - Art. 11 - Politiche di backup
  - Art. 12 - Apprendimento ed evoluzione
  - Art. 13 - Comunicazione
cross_references:
  - 'ISO 27001:2022'
  - NIS2 Art. 21
status: Bozza
subset: true
---

# DORA ICT Risk Management Framework

## 1. Introduzione

### 1.1 Scopo del Documento

Questo documento definisce il framework di gestione del rischio ICT di {{company_name}} in conformità al Capitolo II del Regolamento DORA (Articoli 5-16). Il framework stabilisce le strategie, le policy, le procedure e i controlli necessari per garantire la resilienza operativa digitale dell'organizzazione, proteggendo i servizi finanziari critici da minacce e perturbazioni ICT.

La gestione del rischio ICT rappresenta il cuore della conformità DORA, richiedendo un approccio sistematico che copra l'intero ciclo di vita della sicurezza: dall'identificazione degli asset e delle minacce, attraverso la protezione e il rilevamento, fino alla risposta agli incidenti e al recupero delle operazioni. {{company_name}} adotta questo framework per assicurare che tutti gli aspetti del rischio ICT siano gestiti in modo coerente, proporzionato e allineato agli obiettivi di business.

### 1.2 Ambito di Applicazione

Il presente framework si applica a tutti i sistemi, le applicazioni, le infrastrutture e i dati ICT di {{company_name}}, inclusi quelli gestiti da fornitori terzi a supporto di funzioni critiche o importanti. L'ambito comprende le interconnessioni con sistemi esterni, le dipendenze tecnologiche e i flussi informativi che supportano i servizi finanziari offerti dall'organizzazione.

### 1.3 Impegno della Direzione

L'organo di gestione di {{company_name}} riconosce la propria responsabilità ultima per l'implementazione e la supervisione di questo framework, impegnandosi ad allocare risorse adeguate, a partecipare a programmi di formazione specifici sul rischio ICT e a ricevere reportistica periodica sull'efficacia dei controlli e sullo stato del rischio.

### 1.4 Struttura del Framework

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DORA ICT RISK MANAGEMENT FRAMEWORK                       │
│                    Based on NIST CSF Functions                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                              ┌─────────────┐                                │
│                              │  GOVERNANCE │                                │
│                              │   Art. 5.2  │                                │
│                              └──────┬──────┘                                │
│                                     │                                       │
│  ┌──────────────────────────────────┼──────────────────────────────────┐   │
│  │                                  │                                  │   │
│  ▼                                  ▼                                  ▼   │
│ ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌────────┐│
│ │ IDENTIFY   │  │ PROTECT    │  │ DETECT     │  │ RESPOND    │  │RECOVER ││
│ │ Art. 7     │  │ Art. 8     │  │ Art. 9     │  │ Art. 10    │  │Art. 10 ││
│ │            │  │            │  │            │  │            │  │Art. 11 ││
│ └────────────┘  └────────────┘  └────────────┘  └────────────┘  └────────┘│
│                                                                             │
│                              ┌─────────────┐                                │
│                              │   LEARN &   │                                │
│                              │   EVOLVE    │                                │
│                              │   Art. 12   │                                │
│                              └─────────────┘                                │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Governance e Management Body (Art. 5.2)

### 2.1 Responsabilità del Management Body

| Responsabilità (Art. 5.2) | Implementazione | Evidenza |
|---------------------------|-----------------|----------|
| **(a)** Definire, approvare, supervisionare il framework | CdA approva framework, revisione annuale | Verbale CdA |
| **(b)** Responsabilità ultima per ICT risk management | Accountability esplicita nel framework | Documento governance |
| **(c)** Approvare budget adeguato per ICT security | Budget line dedicata, approvazione annuale | Budget approvato |
| **(d)** Approvare policy ICT audit | Policy audit approvata, piano audit | Verbale/Policy |
| **(e)** Approvare ICT BC Policy e DR Plans | Approvazione formale BCP/DRP | Verbale/Policy |
| **(f)** Ricevere reporting adeguato | Report periodici al board | Report/Verbali |
| **(g)** Formazione su ICT risk | Training periodico board | Attestati formazione |

### 2.2 Ruoli Chiave ICT Risk

| Ruolo | Responsabilità | Requisiti DORA |
|-------|----------------|----------------|
| **Chief Information Security Officer (CISO)** | Gestione operativa ICT risk framework | Competenze adeguate, indipendenza |
| **ICT Risk Manager** | Risk assessment, monitoring, reporting | Esperienza ICT risk |
| **ICT Security Function** | Implementazione controlli, incident response | Risorse adeguate, segregazione |
| **Internal Audit ICT** | Assurance indipendente | Indipendenza, competenze |
| **Compliance** | Monitoraggio conformità DORA | Conoscenza normativa |

### 2.3 Governance Structure

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    ICT RISK GOVERNANCE STRUCTURE                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                     ┌──────────────────────────┐                            │
│                     │ MANAGEMENT BODY (CdA)    │                            │
│                     │ • Approva framework      │                            │
│                     │ • Supervisione           │                            │
│                     │ • Budget                 │                            │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│                     ┌───────────┴──────────────┐                            │
│                     │ ICT RISK COMMITTEE       │                            │
│                     │ • CEO, CIO, CISO, CFO    │                            │
│                     │ • CRO, Compliance        │                            │
│                     └───────────┬──────────────┘                            │
│                                 │                                           │
│    ┌────────────────────────────┼────────────────────────────┐             │
│    │                            │                            │             │
│    ▼                            ▼                            ▼             │
│ ┌──────────────┐       ┌──────────────┐       ┌──────────────┐             │
│ │ CISO         │       │ CIO          │       │ CRO          │             │
│ │ ICT Security │       │ ICT Ops      │       │ Risk Mgmt    │             │
│ └──────────────┘       └──────────────┘       └──────────────┘             │
│                                                                             │
│         ┌──────────────────────────────────────────────┐                   │
│         │                                              │                   │
│         ▼                                              ▼                   │
│ ┌──────────────────┐                       ┌──────────────────┐            │
│ │ ICT SECURITY     │                       │ INTERNAL AUDIT   │            │
│ │ FUNCTION         │                       │ ICT              │            │
│ │ (Art. 6.4)       │                       │ (Art. 5.2.d)     │            │
│ └──────────────────┘                       └──────────────────┘            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 3. ICT Risk Management Strategy

### 3.1 Digital Operational Resilience Strategy (Art. 5.4)

| Elemento Strategia | Descrizione | Owner |
|-------------------|-------------|-------|
| **Obiettivi di resilienza** | Definizione target RTO/RPO per servizi critici | CISO |
| **Risk appetite ICT** | Tolleranza al rischio per diverse categorie | CRO |
| **Priorità investimenti** | Focus aree (detection, protection, recovery) | CIO/CISO |
| **Evoluzione tecnologica** | Roadmap modernizzazione, legacy management | CIO |
| **Third-party strategy** | Approccio a outsourcing ICT | CISO/CIO |

### 3.2 Risk Appetite Statement

| Categoria Rischio | Appetite | Tolleranza | Limite |
|-------------------|----------|------------|--------|
| Disponibilità servizi critici | Basso | Downtime < 4h/anno | Max 24h singolo evento |
| Integrità dati | Zero tolerance | Zero perdita dati | Nessuna perdita |
| Confidenzialità | Basso | Zero breach dati sensibili | Nessun breach |
| Rischio terze parti | Medio | Concentration < 30% | Max 2 critical per funzione |
| Cyber attack | Basso | Zero major incident | Nessun impatto su servizi |

---

## 4. Identification (Art. 7)

### 4.1 Asset Inventory

#### 4.1.1 ICT Asset Classification

| Categoria | Esempi | Criticità | Owner |
|-----------|--------|-----------|-------|
| **Infrastruttura** | Server, storage, network | ☐ Critical ☐ Important ☐ Standard | |
| **Applicazioni** | Core banking, trading, payment | ☐ Critical ☐ Important ☐ Standard | |
| **Dati** | Customer data, transaction data | ☐ Critical ☐ Important ☐ Standard | |
| **Terze Parti** | Cloud, MSP, vendor | ☐ Critical ☐ Important ☐ Standard | |

#### 4.1.2 Asset Register Template

| ID | Nome Asset | Tipo | Criticità | Owner | Funzione Supportata | Dipendenze | Location |
|----|------------|------|-----------|-------|---------------------|------------|----------|
| | | | | | | | |

### 4.2 Business Function Mapping

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    BUSINESS-ICT MAPPING                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────────────┐                                                    │
│  │ BUSINESS FUNCTIONS  │  Funzioni di business critiche/importanti         │
│  │ (Art. 7.1)          │  identificate e classificate                      │
│  └──────────┬──────────┘                                                    │
│             │                                                               │
│             ▼                                                               │
│  ┌─────────────────────┐                                                    │
│  │ ICT ASSETS          │  Asset ICT a supporto delle funzioni              │
│  │ (Art. 7.2)          │  mappati e classificati                           │
│  └──────────┬──────────┘                                                    │
│             │                                                               │
│             ▼                                                               │
│  ┌─────────────────────┐                                                    │
│  │ INTERCONNECTIONS    │  Dipendenze interne/esterne                       │
│  │ (Art. 7.3)          │  documentate                                      │
│  └──────────┬──────────┘                                                    │
│             │                                                               │
│             ▼                                                               │
│  ┌─────────────────────┐                                                    │
│  │ RISK SOURCES        │  Minacce, vulnerabilità, scenari                  │
│  │ (Art. 7.4)          │  identificati                                     │
│  └─────────────────────┘                                                    │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.3 ICT Risk Assessment

#### 4.3.1 Threat Landscape

| Categoria Minaccia | Esempi | Probabilità | Impatto Potenziale |
|--------------------|--------|-------------|-------------------|
| **Malware** | Ransomware, trojan, spyware | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |
| **Phishing** | Spear phishing, BEC | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |
| **DDoS** | Volumetric, application layer | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |
| **Insider Threat** | Malicious, accidental | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |
| **Third-Party** | Supply chain, vendor breach | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |
| **Physical** | Natural disaster, power failure | ☐ H ☐ M ☐ L | ☐ H ☐ M ☐ L |

#### 4.3.2 Risk Assessment Methodology

| Fase | Attività | Output |
|------|----------|--------|
| 1. Contesto | Identificare scope, criteri | Context document |
| 2. Identificazione | Asset, minacce, vulnerabilità | Risk inventory |
| 3. Analisi | Probabilità × Impatto | Risk rating |
| 4. Valutazione | Confronto con appetite | Prioritized risks |
| 5. Trattamento | Mitigare, trasferire, accettare | Treatment plan |

---

## 5. Protection and Prevention (Art. 8)

### 5.1 Security Controls Framework

| Dominio | Controlli Chiave | DORA Ref | Status |
|---------|------------------|----------|--------|
| **Identity & Access** | MFA, PAM, RBAC, Identity Governance | Art. 8.4-8.5 | ☐ |
| **Data Protection** | Encryption (rest/transit), DLP, Classification | Art. 8.6-8.7 | ☐ |
| **Network Security** | Segmentation, Firewalls, IDS/IPS | Art. 8.8-8.9 | ☐ |
| **Endpoint Security** | EDR, Hardening, Patch Management | Art. 8.2-8.3 | ☐ |
| **Application Security** | SAST, DAST, WAF, Secure SDLC | Art. 8 | ☐ |
| **Physical Security** | Access control, CCTV, Environmental | Art. 8 | ☐ |

### 5.2 Vulnerability Management

| Attività | Frequenza | Owner | SLA |
|----------|-----------|-------|-----|
| Vulnerability Scan (internal) | Settimanale | Security Team | - |
| Vulnerability Scan (external) | Mensile | Security Team | - |
| Patch Critical Vulnerabilities | ASAP | IT Ops | 24-72h |
| Patch High Vulnerabilities | Priorità | IT Ops | 7 giorni |
| Patch Medium Vulnerabilities | Pianificato | IT Ops | 30 giorni |
| Penetration Testing | Annuale | External | - |

### 5.3 Access Control Policy

| Principio | Implementazione |
|-----------|-----------------|
| **Least Privilege** | Accessi minimi necessari, review trimestrale |
| **Separation of Duties** | Controlli incompatibili segregati |
| **Need-to-Know (Art. 6.8)** | Accesso a dati solo se necessario |
| **MFA (Art. 8.4)** | Obbligatorio per accessi critici |
| **PAM** | Gestione centralizzata accessi privilegiati |

---

## 6. Detection (Art. 9)

### 6.1 Detection Capabilities

| Capability | Tool/Processo | Coverage | Status |
|------------|---------------|----------|--------|
| **SIEM** | [Tool] | Log aggregation, correlation | ☐ Attivo |
| **EDR** | [Tool] | Endpoint detection | ☐ Attivo |
| **NDR** | [Tool] | Network detection | ☐ Attivo |
| **UEBA** | [Tool] | User behavior analytics | ☐ Attivo |
| **Threat Intel** | [Feeds] | External intelligence | ☐ Attivo |

### 6.2 Monitoring Scope

| Area | Cosa Monitorare | Retention |
|------|-----------------|-----------|
| **Authentication** | Login success/failure, MFA | 12 mesi |
| **Privileged Access** | Admin actions, sudo, PAM | 24 mesi |
| **Network** | Traffic flows, connections | 6 mesi |
| **Application** | Transactions, errors, access | 12 mesi |
| **Security Tools** | AV, FW, IDS alerts | 12 mesi |

### 6.3 Alert Triage Process

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DETECTION & TRIAGE PROCESS                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────────┐                                                       │
│  │ DETECTION        │  SIEM, EDR, NDR generate alerts                      │
│  │ (automated)      │                                                       │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ TRIAGE           │  SOC Analyst (L1) - 15 min SLA                       │
│  │ (Art. 9.2)       │  False positive? Escalate?                           │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ├──────────────────────────────────────┐                         │
│           │ True Positive                        │ False Positive          │
│           ▼                                      ▼                         │
│  ┌──────────────────┐                   ┌──────────────────┐               │
│  │ INVESTIGATION    │                   │ TUNING           │               │
│  │ SOC Analyst (L2) │                   │ Reduce noise     │               │
│  └────────┬─────────┘                   └──────────────────┘               │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ INCIDENT         │  → Escalate to Incident Response                     │
│  │ DECLARATION      │                                                       │
│  └──────────────────┘                                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 7. Response and Recovery (Art. 10)

### 7.1 ICT Business Continuity Policy

| Elemento | Descrizione | Owner |
|----------|-------------|-------|
| **Scope** | Tutti i servizi ICT critici e importanti | CISO |
| **Obiettivi** | RTO/RPO definiti per criticità | Business + IT |
| **Governance** | Ruoli e responsabilità BC | BC Manager |
| **Testing** | Almeno annuale (Art. 5.9) | BC Manager |
| **Review** | Annuale o post-incidente | CISO |

### 7.2 RTO/RPO per Servizio

| Servizio | Criticità | RTO | RPO | Strategia Recovery |
|----------|-----------|-----|-----|-------------------|
| [Servizio 1] | Critical | h | h | Hot standby |
| [Servizio 2] | Critical | h | h | Warm standby |
| [Servizio 3] | Important | h | h | Cold standby |
| [Servizio 4] | Standard | h | h | Rebuild |

### 7.3 ICT Response and Recovery Plans

| Piano | Scope | Trigger | Owner |
|-------|-------|---------|-------|
| **Incident Response Plan** | Tutti gli incidenti ICT | Detection alert | CISO |
| **Disaster Recovery Plan** | Perdita DC primario | Disaster declaration | CIO |
| **Crisis Management Plan** | Eventi di crisi | Major incident | CEO |
| **Communication Plan** | Comunicazione stakeholder | Incidente significativo | Comms |

---

## 8. Backup Policies (Art. 11)

### 8.1 Backup Strategy

| Tipo Dato | Frequenza | Retention | Location | Encryption |
|-----------|-----------|-----------|----------|------------|
| Database critici | Orario | 30 giorni | DR site + Cloud | AES-256 |
| File server | Giornaliero | 90 giorni | DR site | AES-256 |
| Email | Giornaliero | 7 anni | Cloud | AES-256 |
| Configurazioni | Ad ogni modifica | Illimitato | Git repository | - |
| Log | Real-time | 12 mesi | SIEM | - |

### 8.2 Backup Requirements (Art. 11.4)

| Requisito | Implementazione | Status |
|-----------|-----------------|--------|
| Backup site geograficamente separato | DR site a > 100km | ☐ |
| Separate risk profile | Diverso provider/location | ☐ |
| Restore testing periodico | Test mensile | ☐ |
| Immutability (ransomware protection) | Air-gapped o immutable storage | ☐ |

### 8.3 Restore Testing

| Test | Frequenza | Ultimo Test | Risultato | Prossimo |
|------|-----------|-------------|-----------|----------|
| Database restore | Mensile | {{document_date}} | ☐ Pass ☐ Fail | {{document_date}} |
| Full system restore | Trimestrale | {{document_date}} | ☐ Pass ☐ Fail | {{document_date}} |
| DR failover | Annuale | {{document_date}} | ☐ Pass ☐ Fail | {{document_date}} |

---

## 9. Learning and Evolving (Art. 12)

### 9.1 Continuous Improvement Process

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LEARNING & IMPROVEMENT CYCLE                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│        ┌──────────────────┐                                                 │
│        │ INCIDENTS        │  Post-incident reviews                         │
│        │ (Art. 12.1)      │  Lessons learned                               │
│        └────────┬─────────┘                                                 │
│                 │                                                           │
│                 ▼                                                           │
│        ┌──────────────────┐                                                 │
│        │ TESTING RESULTS  │  Pen test, vuln assessment                     │
│        │ (Art. 12.2)      │  TLPT findings                                 │
│        └────────┬─────────┘                                                 │
│                 │                                                           │
│                 ▼                                                           │
│        ┌──────────────────┐                                                 │
│        │ THREAT INTEL     │  New threats, TTPs                             │
│        │ (Art. 12.4-5)    │  Industry sharing                              │
│        └────────┬─────────┘                                                 │
│                 │                                                           │
│                 ▼                                                           │
│        ┌──────────────────┐                                                 │
│        │ FRAMEWORK UPDATE │  Policy, controls, training                    │
│        │ (Art. 12.3)      │                                                │
│        └────────┬─────────┘                                                 │
│                 │                                                           │
│                 ▼                                                           │
│        ┌──────────────────┐                                                 │
│        │ TRAINING UPDATE  │  Staff awareness, technical                    │
│        │ (Art. 12.4)      │  training                                      │
│        └──────────────────┘                                                 │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 9.2 Threat Intelligence

| Fonte | Tipo | Frequenza | Owner |
|-------|------|-----------|-------|
| CERT-EU | Alerts, advisories | Real-time | SOC |
| FS-ISAC | Financial sector intel | Daily | Threat Intel |
| Vendor feeds | IoC, signatures | Real-time | Security Tools |
| Dark web monitoring | Credential leaks | Daily | Threat Intel |

---

## 10. Communication (Art. 13)

### 10.1 Crisis Communication Plan

| Stakeholder | Quando Comunicare | Chi Comunica | Canale |
|-------------|-------------------|--------------|--------|
| Management Body | Major incident | CISO | Email + Meeting |
| Autorità di Vigilanza | Incident reportable | Compliance | Portale ufficiale |
| Clienti | Impatto su servizi | Comms + Business | Email, Web |
| Media | Se pubblico | CEO/Comms | Press release |
| Dipendenti | Durante incident | HR/CISO | Intranet, Email |
| Controparti | Se impattate | Business | Email diretto |

### 10.2 Communication Contacts

| Ruolo | Nome | Contatto | Backup |
|-------|------|----------|--------|
| Spokesperson | | | |
| CISO | | | |
| Legal | | | |
| Compliance | | | |
| Communications | | | |

---

## 11. KPI e Metriche

### 11.1 ICT Risk KPIs

| KPI | Target | Frequenza | Owner |
|-----|--------|-----------|-------|
| Patch compliance (critical) | 100% entro SLA | Mensile | IT Ops |
| Vulnerability remediation rate | > 95% | Mensile | Security |
| Mean Time to Detect (MTTD) | < 24h | Mensile | SOC |
| Mean Time to Respond (MTTR) | < 4h | Mensile | SOC |
| Security incidents | Trend ↓ | Mensile | CISO |
| Phishing click rate | < 5% | Trimestrale | Security |
| BC/DR test success rate | 100% | Annuale | BC Manager |
| Third-party risk assessments | 100% critical | Annuale | CISO |

### 11.2 Reporting

| Report | Destinatario | Frequenza |
|--------|--------------|-----------|
| Security Dashboard | CISO, CIO | Settimanale |
| ICT Risk Report | ICT Risk Committee | Mensile |
| Executive Security Report | Management Body | Trimestrale |
| Annual ICT Risk Report | Management Body, Autorità | Annuale |

---

## 12. Documentazione Correlata

| Documento | Riferimento |
|-----------|-------------|
| ICT Security Policy | POL-ICT-001 |
| Incident Response Plan | PLA-INC-001 |
| Business Continuity Plan | PLA-BC-001 |
| Disaster Recovery Plan | PLA-DR-001 |
| Third-Party Risk Policy | POL-TPR-001 |
| Access Control Policy | POL-ACC-001 |
| Backup Policy | POL-BAK-001 |

---

## 13. Revisione e Approvazione

### 13.1 Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

### 13.2 Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da (CISO) | | | |
| Verificato da (CRO) | | | |
| Verificato da (Internal Audit) | | | |
| Approvato da (CEO) | | | |
| Approvato da (Management Body) | | | |

---

*Questo framework deve essere rivisto almeno annualmente (Art. 5.3) o in caso di incidenti significativi, cambiamenti tecnologici o normativi.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| dora-compliance-checklist.md | Checklist conformita DORA completa |
| dora-governance-oversight.md | Governance e supervisione (Art. 5.2) |
| dora-ict-incident-management.md | Gestione incidenti ICT (Art. 17-23) |
| dora-digital-resilience-testing.md | Test resilienza operativa (Art. 24-27) |
| dora-ict-third-party-risk.md | Rischio terze parti ICT (Art. 28-44) |
| dora-scope-applicability.md | Assessment ambito applicazione |
| dora-isms-integration-guide.md | Integrazione DORA-ISMS |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter | Data del documento |
| `{{document_author}}` | Revision History | Autore del documento |
| ICT asset inventory | Sez. 2 | Inventario asset e sistemi ICT (Art. 7) |
| Risk identification | Sez. 3 | Identificazione rischi ICT |
| Protection measures | Sez. 4 | Misure protezione e prevenzione (Art. 8) |
| Detection capabilities | Sez. 5 | Capacita rilevamento (Art. 9) |
| Response procedures | Sez. 6 | Procedure risposta e ripristino (Art. 10) |
| Backup policies | Sez. 7 | Politiche backup e recovery (Art. 11) |
| Lessons learned | Sez. 8 | Processo apprendimento ed evoluzione (Art. 12) |
| Communication plan | Sez. 9 | Piano comunicazione (Art. 13) |
| Risk tolerance | Sez. 10 | Definire tolleranza rischio ICT |
| Firme approvazione | Sez. finale | Firme CEO, Internal Audit, Management Body |
