---
title: Checklist di Conformità NIS2
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: CISO / DPO
approver: Alta Direzione
framework: NIS2
language: IT
documentType: checklist
directive_articles:
  - Art. 20 - Governance
  - Art. 21 - Misure di gestione del rischio cybersecurity
  - Art. 23 - Obblighi di notifica
  - Art. 24 - Utilizzo schemi di certificazione
  - Art. 25 - Normazione
national_transposition: D.Lgs. 138/2024
cross_references:
  - 'ISO 27001:2022'
  - NIST CSF 2.0
  - Linee guida ENISA
  - D.Lgs. 138/2024 - Recepimento NIS2 Italia
related_documents:
  - document: NIS2 Scope & Applicability
    path: ../context/nis2-scope-applicability.md
  - document: NIS2 Governance & Accountability
    path: ../governance/nis2-governance-accountability.md
  - document: NIS2 Risk Management Measures
    path: ../risk/nis2-risk-management-measures.md
  - document: NIS2 Incident Reporting
    path: ../incidents/nis2-incident-reporting.md
  - document: NIS2 Business Continuity Plan
    path: ../continuity/nis2-business-continuity-plan.md
  - document: NIS2 Supply Chain Security
    path: ../supply-chain/nis2-supply-chain-security.md
  - document: NIS2 Internal Audit Programme
    path: ../audit/nis2-internal-audit-programme.md
  - document: NIS2 ISMS Integration Guide
    path: ../context/nis2-isms-integration-guide.md
  - document: NIS2 ACN Registration Checklist
    path: ./nis2-acn-registration-checklist.md
status: Bozza
subset: true
---

# NIS2 Compliance Checklist

## 1. Scopo

La presente checklist costituisce uno strumento operativo per la verifica sistematica della conformità ai requisiti della Direttiva (UE) 2022/2555, comunemente nota come NIS2, e della relativa trasposizione nazionale attraverso il D.Lgs. 138/2024. {{company_name}} utilizza questo documento per condurre assessment periodici del proprio stato di conformità, identificando gap e prioritizzando le azioni correttive necessarie.

La checklist copre tutti gli ambiti normativi rilevanti, dalla governance e accountability degli organi di gestione previste dall'Articolo 20, alle dieci categorie di misure di gestione del rischio elencate nell'Articolo 21.2, fino agli obblighi di notifica incidenti stabiliti dall'Articolo 23. L'organizzazione utilizza i risultati dell'assessment per alimentare il processo di miglioramento continuo e per dimostrare alle autorità competenti l'impegno verso la piena conformità normativa.

## 2. Informazioni Organizzazione

| Campo | Valore |
|-------|--------|
| **Ragione Sociale** | [INSERIRE] |
| **Settore (Annex I/II)** | [INSERIRE] |
| **Classificazione Entità** | ☐ Essenziale / ☐ Importante |
| **Data Assessment** | {{document_date}} |
| **Responsabile Compilazione** | {{contact_name}} |
| **Ultima Revisione** | {{document_date}} |

---

## 2. Governance e Accountability (Art. 20)

### 2.1 Responsabilità Organi di Gestione

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| GOV-01 | Gli organi di gestione approvano le misure di cybersecurity | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-02 | Gli organi di gestione supervisionano l'implementazione delle misure | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-03 | Gli organi di gestione possono essere ritenuti responsabili per violazioni | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-04 | I membri degli organi di gestione seguono formazione sulla cybersecurity | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-05 | È incoraggiata formazione periodica per tutti i dipendenti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 2.2 Struttura Organizzativa

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| GOV-06 | È nominato un responsabile per la sicurezza delle informazioni | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-07 | Sono definiti ruoli e responsabilità per la cybersecurity | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-08 | È istituito un comitato/funzione per la gestione dei rischi cyber | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| GOV-09 | Reporting periodico agli organi di gestione è previsto | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

---

## 3. Misure di Gestione del Rischio Cybersecurity (Art. 21)

### 3.1 Politiche di Analisi dei Rischi e Sicurezza (Art. 21.2.a)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| RISK-01 | Esiste una politica di sicurezza delle informazioni documentata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-02 | È implementato un framework di risk assessment | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-03 | Risk assessment periodici sono condotti (almeno annuali) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-04 | I rischi sono valutati per probabilità e impatto | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-05 | Esiste un registro dei rischi documentato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-06 | I criteri di accettazione del rischio sono definiti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| RISK-07 | Il risk treatment plan è documentato e monitorato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.2 Gestione degli Incidenti (Art. 21.2.b)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| INC-01 | Esiste una procedura di incident response documentata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-02 | È definito il processo di rilevamento incidenti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-03 | Sono definiti criteri di classificazione degli incidenti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-04 | Esiste un team di incident response (interno o esterno) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-05 | Sono condotte esercitazioni periodiche di incident response | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-06 | Il processo di escalation è documentato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| INC-07 | Post-incident review è condotta sistematicamente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.3 Business Continuity e Crisis Management (Art. 21.2.c)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| BCM-01 | Esiste un Business Impact Analysis (BIA) documentato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-02 | I servizi critici sono identificati e prioritizzati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-03 | Esistono Business Continuity Plan documentati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-04 | Sono definiti RTO e RPO per i servizi critici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-05 | Esistono Disaster Recovery Plan documentati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-06 | I backup sono eseguiti regolarmente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-07 | I backup sono testati per il ripristino | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-08 | Esiste un Crisis Management Plan | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| BCM-09 | Test/esercitazioni BC/DR sono condotti periodicamente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.4 Supply Chain Security (Art. 21.2.d)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| SCM-01 | Esiste un inventario dei fornitori critici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-02 | I fornitori sono valutati per il rischio cyber | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-03 | I contratti includono requisiti di sicurezza | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-04 | I fornitori sono monitorati per la conformità security | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-05 | I rischi specifici di ogni fornitore sono considerati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-06 | La qualità dei prodotti/servizi è verificata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-07 | Esistono clausole per incident notification dai fornitori | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| SCM-08 | Il processo di offboarding fornitori è definito | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.5 Sicurezza nell'Acquisizione e Sviluppo (Art. 21.2.e)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| DEV-01 | Esistono requisiti di sicurezza per l'acquisizione IT | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-02 | Secure SDLC è implementato per lo sviluppo interno | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-03 | Security testing è condotto (SAST/DAST) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-04 | Vulnerability management è implementato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-05 | Patch management process è definito | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-06 | Hardening standards sono applicati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| DEV-07 | Change management process è documentato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.6 Valutazione dell'Efficacia delle Misure (Art. 21.2.f)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| EFF-01 | KPI/metriche di sicurezza sono definiti e monitorati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| EFF-02 | Vulnerability assessment periodici sono condotti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| EFF-03 | Penetration testing è eseguito periodicamente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| EFF-04 | Audit interni di sicurezza sono condotti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| EFF-05 | I risultati sono analizzati e azioni correttive implementate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| EFF-06 | Security awareness testing è condotto | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.7 Cyber Hygiene e Formazione (Art. 21.2.g)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| HYG-01 | Esiste un programma di security awareness | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-02 | Formazione obbligatoria per tutti i dipendenti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-03 | Formazione specifica per ruoli tecnici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-04 | Simulazioni di phishing sono condotte | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-05 | Policy di password robuste implementate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-06 | Endpoint protection è implementata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HYG-07 | Software aggiornato e patch applicate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.8 Crittografia (Art. 21.2.h)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| CRY-01 | Esiste una politica sulla crittografia | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRY-02 | I dati in transito sono crittografati (TLS 1.2+) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRY-03 | I dati at rest sono crittografati ove appropriato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRY-04 | Key management process è implementato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRY-05 | Algoritmi crittografici approvati sono utilizzati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRY-06 | Certificati sono gestiti (inventario, scadenze) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.9 Sicurezza delle Risorse Umane (Art. 21.2.i)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| HR-01 | Background check per ruoli critici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HR-02 | NDA/accordi di riservatezza firmati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HR-03 | Security onboarding per nuovi dipendenti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HR-04 | Processo di offboarding include revoca accessi | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| HR-05 | Ruoli e responsabilità security documentati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.10 Controllo Accessi (Art. 21.2.i)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| ACC-01 | Esiste una politica di controllo accessi | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| ACC-02 | Principio del least privilege applicato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| ACC-03 | Accessi privilegiati sono gestiti (PAM) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| ACC-04 | Review periodica degli accessi | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| ACC-05 | Autenticazione forte (MFA) per accessi critici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| ACC-06 | Logging degli accessi implementato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.11 Asset Management (Art. 21.2.i)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| AST-01 | Esiste un inventario degli asset IT | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| AST-02 | Gli asset sono classificati per criticità | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| AST-03 | Asset owner sono assegnati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| AST-04 | Procedure di dismissione sicura asset | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| AST-05 | Shadow IT è monitorato/controllato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 3.12 Autenticazione Multi-Fattore e Comunicazioni Sicure (Art. 21.2.j)

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| MFA-01 | MFA implementato per accessi critici | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| MFA-02 | MFA per accesso remoto (VPN) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| MFA-03 | MFA per accesso a sistemi cloud | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| MFA-04 | Continuous authentication considerata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| MFA-05 | Comunicazioni voce/video sicure ove necessario | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| MFA-06 | Emergency communication systems disponibili | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

---

## 4. Notifica Incidenti (Art. 23)

### 4.1 Processo di Notifica

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| NOT-01 | Processo di notifica al CSIRT/ACN documentato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-02 | Criteri per "incidente significativo" definiti | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-03 | Early warning entro 24h dalla detection | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-04 | Incident notification entro 72h | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-05 | Final report entro 1 mese | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-06 | Template di notifica preparati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-07 | Contatti CSIRT/ACN disponibili 24/7 | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-08 | Notifica agli utenti se necessario | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 4.2 Contenuto Notifiche

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| NOT-09 | Capacità di determinare impatto transfrontaliero | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-10 | Capacità di determinare numero utenti impattati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-11 | Capacità di determinare durata dell'incidente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| NOT-12 | Capacità di determinare estensione geografica | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

---

## 5. Certificazioni e Standard (Art. 24-25)

### 5.1 Certificazioni

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| CRT-01 | ISO 27001 certificazione (raccomandato) | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRT-02 | Schema di certificazione cybersecurity EU considerato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| CRT-03 | Certificazioni di prodotto valutate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 5.2 Standard

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| STD-01 | Standard europei/internazionali adottati | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| STD-02 | Specifiche tecniche documentate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| STD-03 | Best practice di settore implementate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

---

## 6. Registrazione e Cooperazione (Art. 27, 29)

### 6.1 Registrazione

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| REG-01 | Registrazione presso ACN completata | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| REG-02 | Informazioni di registrazione aggiornate | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| REG-03 | Modifiche comunicate tempestivamente | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

### 6.2 Cooperazione con Autorità

| Req ID | Requisito | Stato | Evidenze | Note |
|--------|-----------|-------|----------|------|
| COOP-01 | Punto di contatto per autorità designato | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| COOP-02 | Capacità di rispondere a richieste ACN | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| COOP-03 | Disponibilità a ispezioni/audit | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |
| COOP-04 | Information sharing con settore/ISAC | ☐ Conforme ☐ Parziale ☐ Non conforme ☐ N/A | | |

---

## 7. Requisiti Specifici per Settore

### 7.1 Settori Annex I (Alta Criticità)

| Settore | Requisiti Aggiuntivi | Stato | Note |
|---------|---------------------|-------|------|
| Energia | Requisiti ACER, TSO/DSO | ☐ Verificato | |
| Trasporti | Safety requirements | ☐ Verificato | |
| Banche | EBA guidelines | ☐ Verificato | |
| Sanità | MDR/IVDR integration | ☐ Verificato | |
| Acqua | Essential service provisions | ☐ Verificato | |
| Infrastruttura digitale | Cloud/DC requirements | ☐ Verificato | |
| Pubblica amministrazione | PA specific requirements | ☐ Verificato | |
| Spazio | Space assets security | ☐ Verificato | |

### 7.2 Settori Annex II (Altri Critici)

| Settore | Requisiti Aggiuntivi | Stato | Note |
|---------|---------------------|-------|------|
| Postale | Service continuity | ☐ Verificato | |
| Rifiuti | Environmental safety | ☐ Verificato | |
| Chimica | SEVESO integration | ☐ Verificato | |
| Alimentare | Food safety | ☐ Verificato | |
| Manifatturiero | OT security | ☐ Verificato | |
| Digitale (marketplace/search/social) | DSA integration | ☐ Verificato | |
| Ricerca | IP protection | ☐ Verificato | |

---

## 8. Riepilogo Conformità

### 8.1 Score Card

| Area | Conformi | Parziali | Non Conformi | N/A | % Conformità |
|------|----------|----------|--------------|-----|--------------|
| Governance (Art. 20) | | | | | % |
| Risk Management (Art. 21.2.a) | | | | | % |
| Incident Management (Art. 21.2.b) | | | | | % |
| Business Continuity (Art. 21.2.c) | | | | | % |
| Supply Chain (Art. 21.2.d) | | | | | % |
| Sviluppo Sicuro (Art. 21.2.e) | | | | | % |
| Efficacia Misure (Art. 21.2.f) | | | | | % |
| Cyber Hygiene (Art. 21.2.g) | | | | | % |
| Crittografia (Art. 21.2.h) | | | | | % |
| HR & Access Control (Art. 21.2.i) | | | | | % |
| MFA & Comunicazioni (Art. 21.2.j) | | | | | % |
| Notifica Incidenti (Art. 23) | | | | | % |
| Certificazioni (Art. 24-25) | | | | | % |
| Registrazione (Art. 27) | | | | | % |
| **TOTALE** | | | | | **%** |

### 8.2 Gap Analysis Summary

| Priorità | Gap Identificati | Azione Correttiva | Responsabile | Scadenza |
|----------|------------------|-------------------|--------------|----------|
| Alta | | | | |
| Alta | | | | |
| Media | | | | |
| Media | | | | |
| Bassa | | | | |

### 8.3 Roadmap Conformità

| Fase | Attività | Scadenza Target | Stato |
|------|----------|-----------------|-------|
| 1 | Gap Analysis completato | | ☐ |
| 2 | Piano di remediation approvato | | ☐ |
| 3 | Misure critiche implementate | | ☐ |
| 4 | Registrazione ACN completata | | ☐ |
| 5 | Audit interno NIS2 | | ☐ |
| 6 | Conformità piena raggiunta | | ☐ |

---

## 9. Mapping ISO 27001:2022

| NIS2 Art. 21 | Descrizione | ISO 27001 Controls |
|--------------|-------------|-------------------|
| 21.2.a | Risk analysis & policies | 5.1, 6.1, 6.2, A.5.1 |
| 21.2.b | Incident handling | A.5.24-5.28, A.6.8 |
| 21.2.c | Business continuity | A.5.29-5.30 |
| 21.2.d | Supply chain security | A.5.19-5.23 |
| 21.2.e | Network security, acquisition | A.8.20-8.22, A.8.25-8.31 |
| 21.2.f | Effectiveness assessment | 9.1-9.3, A.5.35-5.36 |
| 21.2.g | Cyber hygiene & training | A.6.3, A.7.2-7.3 |
| 21.2.h | Cryptography | A.8.24 |
| 21.2.i | HR, access control, assets | A.5.9-5.18, A.6.1-6.6, A.7.7-7.14 |
| 21.2.j | MFA, secure communications | A.5.14, A.8.5 |

---

## 10. Firme e Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Compilatore | | | |
| CISO | | | |
| DPO | | | |
| CEO/AD | | | |

---

## Allegati

- [ ] A - Risk Assessment Report
- [ ] B - Incident Response Plan
- [ ] C - Business Continuity Plan
- [ ] D - Supplier Security Register
- [ ] E - Training Records
- [ ] F - Security Policies Index
- [ ] G - Registrazione ACN

---

*Questo checklist deve essere rivisto almeno 1 volta l'anno o in caso di modifiche significative all'organizzazione, ai sistemi o al contesto normativo. Lo scoring deve essere aggiornato trimestralmente.*

---

## 11. Documenti Correlati

| Documento | Tipo | Percorso |
|-----------|------|----------|
| NIS2 Scope & Applicability | Assessment | `../context/nis2-scope-applicability.md` |
| NIS2 Governance & Accountability | Policy | `../governance/nis2-governance-accountability.md` |
| NIS2 Risk Management Measures | Procedura | `../risk/nis2-risk-management-measures.md` |
| NIS2 Incident Reporting | Procedura | `../incidents/nis2-incident-reporting.md` |
| NIS2 Business Continuity Plan | Piano | `../continuity/nis2-business-continuity-plan.md` |
| NIS2 Supply Chain Security | Policy | `../supply-chain/nis2-supply-chain-security.md` |
| NIS2 Internal Audit Programme | Piano | `../audit/nis2-internal-audit-programme.md` |
| NIS2 ISMS Integration Guide | Guida | `../context/nis2-isms-integration-guide.md` |
| NIS2 ACN Registration Checklist | Checklist | `./nis2-acn-registration-checklist.md` |

---

## 12. Checklist di Compilazione

| # | Placeholder | Sezione | Descrizione |
|---|-------------|---------|-------------|
| 1 | `{{company_name}}` | Varie | Ragione sociale dell'organizzazione |
| 2 | `{{document_date}}` | Frontmatter | Data emissione documento |
| 3 | Tutte le sezioni di checklist | 2-8 | Spuntare ogni voce con stato attuale |
| 4 | Gap analysis | 8 | Compilare gap e piani di remediation |
| 5 | Mapping ISO 27001 (9) | 9 | Verificare gap per ogni controllo mappato |
| 6 | Firme (10) | 10 | Completare nomi e firme di approvazione |
