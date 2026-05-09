---
title: DORA ICT Third-Party Risk Management
version: '1.1'
date: '{{document_date}}'
classification: Riservato
owner: CISO / Procurement
approver: Organo di Gestione
framework: DORA
language: IT
documentType: procedure
regulation_articles:
  - Art. 28 - Principi generali
  - Art. 29 - Valutazione preliminare
  - Art. 30 - Disposizioni contrattuali fondamentali
  - Art. 31-44 - Quadro di sorveglianza per CTPP critici
cross_references:
  - 'ISO 27001:2022 A.5.19-A.5.23'
  - NIS2 Art. 21.2.d
status: Bozza
subset: true
---

# DORA ICT Third-Party Risk Management

## 1. Introduzione

### 1.1 Scopo del Documento

Questo documento definisce il framework di gestione del rischio ICT di terze parti di {{company_name}} in conformità al Capitolo V del Regolamento DORA (Articoli 28-44). Il framework stabilisce principi, processi e controlli per la gestione dei rapporti con i fornitori di servizi ICT, riconoscendo che la dipendenza da terze parti introduce rischi significativi che devono essere identificati, valutati e gestiti in modo appropriato.

La crescente dipendenza del settore finanziario da fornitori ICT esterni, inclusi provider di servizi cloud, managed service provider e sviluppatori software, richiede un approccio strutturato alla gestione del rischio di controparte. {{company_name}} riconosce che la propria resilienza operativa digitale dipende in modo significativo dalla resilienza dei propri fornitori critici e si impegna a mantenere una supervisione efficace di tutta la catena di fornitura ICT.

### 1.2 Principi Fondamentali

{{company_name}} mantiene la piena responsabilità per la gestione del rischio ICT anche quando le funzioni sono esternalizzate a fornitori terzi. Questo principio cardine del DORA significa che l'esternalizzazione non trasferisce la responsabilità, e l'organizzazione deve assicurare che i propri fornitori rispettino standard di sicurezza e resilienza adeguati. Il presente framework implementa controlli proporzionati al rischio che ciascun fornitore rappresenta per l'operatività dell'entità.

### 1.3 Impegno della Direzione

L'organo di gestione approva la strategia di gestione del rischio ICT di terze parti e supervisiona la sua implementazione. I contratti con fornitori che supportano funzioni critiche o importanti richiedono l'approvazione formale dell'alta direzione, e il registro dei contratti ICT è mantenuto aggiornato e disponibile per le autorità di vigilanza.

### 1.4 Scope DORA Chapter V

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DORA ICT THIRD-PARTY RISK FRAMEWORK                      │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ ART. 28: GENERAL PRINCIPLES                                                 │
│ ───────────────────────────                                                 │
│ • Retain full responsibility for ICT risk                                   │
│ • Risk-based approach to managing ICT third-party                          │
│ • Maintain Register of all ICT contracts                                    │
│ • Report annually to competent authority                                    │
│                                                                             │
│ ART. 29: PRELIMINARY ASSESSMENT                                             │
│ ───────────────────────────────                                             │
│ • Risk assessment before contracting                                        │
│ • Concentration risk assessment                                             │
│ • Substitutability evaluation                                               │
│                                                                             │
│ ART. 30: KEY CONTRACTUAL PROVISIONS                                         │
│ ────────────────────────────────────                                        │
│ • Mandatory clauses for all ICT contracts                                   │
│ • Additional clauses for critical/important functions                       │
│                                                                             │
│ ART. 31-44: OVERSIGHT FRAMEWORK (for CTPP)                                  │
│ ───────────────────────────────────────────                                 │
│ • Critical ICT Third-Party Providers                                        │
│ • Lead Overseer designation                                                 │
│ • Direct oversight by ESAs                                                  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. ICT Third-Party Strategy (Art. 28.2)

### 2.1 Strategy Elements

| Elemento | Descrizione | Owner |
|----------|-------------|-------|
| Risk appetite third-party | Tolleranza rischio outsourcing ICT | CRO |
| Concentration limits | Max esposizione per provider/geo | CISO |
| Critical function policy | Criteri per outsourcing funzioni critiche | CISO |
| Exit strategy approach | Framework per exit planning | CIO |
| Due diligence standards | Requisiti valutazione provider | CISO |

### 2.2 Classification Funzioni

| Classificazione | Definizione (Art. 3.22) | Requisiti Aggiuntivi |
|-----------------|-------------------------|---------------------|
| **Critical** | Se disruption impatta significativamente performance finanziaria, continuità servizi, compliance | Full Art. 30.3, exit plan, audit right |
| **Important** | Supporta funzioni di business rilevanti | Art. 30.2-3 selezionati |
| **Standard** | Supporto operativo normale | Art. 30.2 base |

---

## 3. Register of Information (Art. 28.3)

### 3.1 Template Registro Contratti ICT

| Campo | Descrizione |
|-------|-------------|
| **ID Contratto** | Identificativo univoco |
| **Provider** | Ragione sociale, LEI, paese |
| **Tipo Servizio** | Cloud, MSP, SW, HW, etc. |
| **Funzione Supportata** | Funzione business/ICT |
| **Classificazione** | Critical / Important / Standard |
| **Data Inizio** | Data efficacia contratto |
| **Data Scadenza** | Termine o rinnovo auto |
| **Valore Annuo** | € valore contrattuale |
| **Subcontractor** | Se presenti, dettagli |
| **Data Location** | Paese/i processing dati |
| **Exit Plan** | Disponibile ☐ Sì ☐ No |
| **Ultimo Assessment** | Data ultima valutazione |
| **Risk Rating** | High / Medium / Low |

### 3.2 Reporting all'Autorità (Art. 28.3)

Il registro deve essere disponibile per l'autorità competente:
- Su richiesta
- Report annuale sui contratti ICT critical/important
- Notifica nuovi contratti critical (alcuni regimi)

---

## 4. Preliminary Assessment (Art. 29)

### 4.1 Pre-Contract Risk Assessment

| Fattore (Art. 29.2) | Valutazione | Score (1-5) |
|---------------------|-------------|-------------|
| **(a)** Criticità funzione supportata | | |
| **(b)** Rischi operativi | | |
| **(c)** Concentration risk | | |
| **(d)** Sub-outsourcing | | |
| **(e)** Data location | | |
| **(f)** Sostituibilità | | |
| **TOTALE** | | /30 |

### 4.2 Concentration Risk Assessment

| Parametro | Valore | Soglia | Status |
|-----------|--------|--------|--------|
| % spesa ICT con top provider | % | < 30% | ☐ OK ☐ Alert |
| N. funzioni critical con stesso provider | | < 3 | ☐ OK ☐ Alert |
| N. provider per funzione critical | | ≥ 2 | ☐ OK ☐ Alert |
| Dipendenza geografica | | Diversificata | ☐ OK ☐ Alert |

### 4.3 Due Diligence Checklist

| Area | Check | Status |
|------|-------|--------|
| **Financials** | Stabilità finanziaria, bilanci | ☐ |
| **Security** | Certificazioni (ISO 27001, SOC2) | ☐ |
| **Compliance** | GDPR, settoriale, DORA-ready | ☐ |
| **Operational** | SLA capability, track record | ☐ |
| **BCM** | BC/DR capability, test results | ☐ |
| **Subcontractor** | Chain visibility, controls | ☐ |
| **Legal** | Jurisdictions, liability | ☐ |
| **References** | Client references nel settore | ☐ |

---

## 5. Key Contractual Provisions (Art. 30)

### 5.1 Clausole Obbligatorie - Tutti i Contratti (Art. 30.2)

| Clausola | Requisito | Check |
|----------|-----------|-------|
| **(a)** Descrizione completa | Funzioni, servizi, SLA | ☐ |
| **(b)** Location | Dove dati processati/stored | ☐ |
| **(c)** Data protection | Misure protezione dati | ☐ |
| **(d)** SLA | KPI quantitativi e qualitativi | ☐ |
| **(e)** Incident notification | Obbligo notifica incidenti | ☐ |
| **(f)** Cooperazione autorità | Supporto a ispezioni/audit | ☐ |
| **(g)** Termination rights | Diritti di recesso | ☐ |
| **(h)** Exit plan | Transition/exit assistance | ☐ |

### 5.2 Clausole Aggiuntive - Critical/Important (Art. 30.3)

| Clausola | Requisito | Check |
|----------|-----------|-------|
| **(a)** Audit rights (entità) | Diritto audit on-site | ☐ |
| **(b)** Audit rights (autorità) | Access per autorità | ☐ |
| **(c)** Security measures | Misure sicurezza specifiche | ☐ |
| **(d)** BCM provider | BC/DR del provider | ☐ |
| **(e)** TLPT participation | Partecipazione a TLPT | ☐ |
| **(f)** Subcontracting | Restrizioni, pre-approval | ☐ |

### 5.3 Template Clausole Contrattuali DORA

```
ANNEX - DORA CONTRACTUAL PROVISIONS

1. SERVICE DESCRIPTION (Art. 30.2.a)
   [Detailed description of ICT services, functions supported, deliverables]

2. DATA PROCESSING LOCATIONS (Art. 30.2.b)
   Primary location: _______________
   Backup location: _______________
   Any change requires prior written approval.

3. DATA PROTECTION (Art. 30.2.c)
   Provider shall implement and maintain security measures including:
   - Encryption in transit (TLS 1.2+) and at rest (AES-256)
   - Access controls and authentication
   - Logging and monitoring
   - [Additional measures as required]

4. SERVICE LEVELS (Art. 30.2.d)
   | KPI | Target | Measurement | Penalty |
   |-----|--------|-------------|---------|
   | Availability | 99.9% | Monthly | [X]% fee |
   | Response time | <X sec | P95 | - |
   | Support response | <4h P1 | Per incident | - |

5. INCIDENT NOTIFICATION (Art. 30.2.e)
   Provider shall notify Client of any ICT-related incident within:
   - [4] hours for incidents affecting Client's services
   - [24] hours for significant incidents affecting Provider
   Notification shall include: [details required]

6. COOPERATION WITH AUTHORITIES (Art. 30.2.f)
   Provider shall fully cooperate with Client's competent authorities
   and provide access to premises, data, and personnel as required.

7. TERMINATION RIGHTS (Art. 30.2.g)
   Client may terminate this Agreement:
   - With [90] days notice for convenience
   - Immediately for material breach
   - If Provider fails to meet security requirements
   - [Other termination triggers]

8. TRANSITION AND EXIT (Art. 30.2.h)
   Provider shall:
   - Develop and maintain exit plan
   - Support transition for minimum [180] days
   - Return all data in standard format
   - Securely delete all data upon confirmation

FOR CRITICAL/IMPORTANT FUNCTIONS:

9. AUDIT RIGHTS (Art. 30.3.a-b)
   Client and its competent authorities shall have the right to:
   - Conduct on-site audits with [30] days notice
   - Access relevant documentation
   - Interview relevant personnel
   Pooled audits and third-party certifications accepted.

10. SECURITY REQUIREMENTS (Art. 30.3.c)
    Provider shall maintain:
    - ISO 27001 certification (or equivalent)
    - Annual penetration testing
    - Vulnerability management program
    - [Specific security controls]

11. BUSINESS CONTINUITY (Art. 30.3.d)
    Provider shall:
    - Maintain tested BC/DR plans
    - RTO: [X hours] / RPO: [X hours]
    - Annual DR testing with results shared

12. TLPT PARTICIPATION (Art. 30.3.e)
    Provider shall participate in Client's TLPT as required,
    subject to appropriate safeguards and coordination.

13. SUBCONTRACTING (Art. 30.3.f)
    Subcontracting of critical components requires prior written approval.
    Provider remains fully liable for subcontractor performance.
    Current approved subcontractors: [List]
```

---

## 6. Ongoing Monitoring

### 6.1 Monitoring Framework

| Attività | Frequenza | Owner |
|----------|-----------|-------|
| SLA monitoring | Mensile | Vendor Manager |
| Security questionnaire | Annuale | CISO |
| Financial review | Annuale | Procurement |
| Certification check | Semestrale | Compliance |
| Incident review | Per evento | CISO |
| Risk reassessment | Annuale | Risk |
| Audit/review | Annuale (critical) | Audit |

### 6.2 KPI per Provider

| KPI | Target | Soglia Alert | Action |
|-----|--------|--------------|--------|
| SLA compliance | > 99.5% | < 99% | Escalation |
| Security incidents | 0 major | Any major | Review |
| Audit findings | 0 critical | Any critical | Remediation plan |
| Certifications | Valid | Expiring <3m | Verify renewal |

---

## 7. Exit Management

### 7.1 Exit Plan Requirements

| Elemento | Descrizione |
|----------|-------------|
| **Trigger events** | Quando attivare exit plan |
| **Timeline** | Fasi e tempistiche exit |
| **Data migration** | Processo estrazione dati |
| **Alternative providers** | Provider alternativi identificati |
| **Internal capability** | Capacità interna se necessario |
| **Transition support** | Supporto richiesto da provider |
| **Testing** | Test di exit plan |

### 7.2 Exit Checklist

| Fase | Attività | Status |
|------|----------|--------|
| **Pre-Exit** | Notifica formale | ☐ |
| | Attivazione alternative | ☐ |
| | Piano migrazione | ☐ |
| **Data** | Export dati | ☐ |
| | Validazione completezza | ☐ |
| | Conferma cancellazione | ☐ |
| **Access** | Revoca accessi | ☐ |
| | Ritiro credenziali | ☐ |
| **Closure** | Chiusura formale | ☐ |
| | Lessons learned | ☐ |

---

## 8. Critical Third-Party Providers (CTPP)

### 8.1 Identificazione CTPP

I fornitori ICT critici (Art. 31) sono identificati dalle ESAs basandosi su:

| Criterio | Descrizione |
|----------|-------------|
| Impatto sistemico | Impatto su stabilità finanziaria se failure |
| Concentrazione | Numero/tipo entità servite |
| Sostituibilità | Difficoltà sostituzione |
| Interconnessione | Dipendenze critiche |

### 8.2 Implicazioni per Entità con CTPP

Se un provider è designato CTPP:

| Implicazione | Azione Richiesta |
|--------------|------------------|
| Lead Overseer assigned | Coordinamento con overseer |
| Direct oversight | Supporto a ispezioni ESA |
| Recommendations binding | Implementare raccomandazioni |
| Potential restrictions | Possibili limiti all'uso |

---

## 9. Governance

### 9.1 Third-Party Risk Governance

| Comitato/Ruolo | Responsabilità |
|----------------|----------------|
| **Management Body** | Approvazione strategy, critical contracts |
| **ICT Risk Committee** | Oversight third-party risk |
| **CISO** | Security requirements, assessment |
| **CIO** | Operational requirements |
| **Procurement** | Contract negotiation |
| **Legal** | Contract review |
| **Compliance** | Regulatory requirements |

### 9.2 Reporting

| Report | Destinatario | Frequenza |
|--------|--------------|-----------|
| Third-party risk dashboard | ICT Risk Committee | Mensile |
| Critical provider review | Management Body | Trimestrale |
| Register update | Competent Authority | Annuale |
| Incident report | As required | Per evento |

---

## 10. Documenti Correlati

| Documento | Riferimento |
|-----------|-------------|
| Third-Party Risk Policy | POL-TPR-001 |
| Vendor Security Questionnaire | TMP-VSQ-001 |
| Contract Template DORA | TMP-CTR-001 |
| Exit Plan Template | TMP-EXIT-001 |
| Due Diligence Checklist | CHK-DD-001 |

---

## 11. Revisione e Approvazione

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | | | |
| Verificato da | | | |
| Approvato da (CISO) | | | |
| Approvato da (Management Body) | | | |

---

*Questo framework deve essere rivisto annualmente e aggiornato in caso di nuovi contratti critical, cambiamenti normativi o incidenti con third-party.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| dora-ict-risk-management-framework.md | Framework gestione rischio ICT |
| dora-compliance-checklist.md | Checklist conformita DORA completa |
| dora-governance-oversight.md | Governance e supervisione (Art. 28) |
| dora-digital-resilience-testing.md | Test resilienza (incluso test terze parti) |
| dora-ict-incident-management.md | Gestione incidenti (impatto terze parti) |
| dora-scope-applicability.md | Assessment ambito applicazione |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter | Data del documento |
| `{{document_author}}` | Revision History | Autore del documento |
| ICT service provider register | Sez. 2 | Registro fornitori ICT (Art. 28.3) |
| Pre-contractual assessment | Sez. 3 | Valutazione preliminare (Art. 29) |
| Contract clauses | Sez. 4 | Clausole contrattuali fondamentali (Art. 30) |
| Concentration risk | Sez. 5 | Valutazione rischio concentrazione |
| Exit strategies | Sez. 6 | Strategie di uscita per ogni CTPP |
| Subcontracting monitoring | Sez. 7 | Monitoraggio catena subcontracting |
| Critical CTPP oversight | Sez. 8 | Supervisione CTPP critici (Art. 31-44) |
| Firme approvazione | Sez. finale | Firme CISO e Management Body |
