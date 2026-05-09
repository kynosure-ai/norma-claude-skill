---
title: EU AI Act Compliance Checklist
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: AI Governance Lead
approver: '{{approver_name}}'
framework: EU AI Act (Regulation 2024/1689)
regulation_reference: EU AI Act - Regulation (EU) 2024/1689
effective_dates:
  - '2025-02-02: Prohibited AI practices'
  - '2025-08-02: GPAI, governance, penalties'
  - '2026-08-02: High-risk systems (Annex III)'
  - '2027-08-02: High-risk (Annex I products)'
cross_references:
  - document: AIMS Scope
    path: ../context/aims-scope.md
  - document: AI System Inventory
    path: ../registers/ai-system-inventory.md
  - document: AI Risk Assessment
    path: ../risk-assessment/ai-risk-assessment-methodology.md
status: draft
review_frequency: quarterly
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# EU AI Act Compliance Checklist
## Lista di Controllo Conformità Regolamento UE sull'Intelligenza Artificiale

## 1. Introduzione

### 1.1 Scopo

Questa checklist fornisce uno strumento operativo completo per verificare la conformita di {{company_name}} al Regolamento (UE) 2024/1689 sull'Intelligenza Artificiale, comunemente noto come EU AI Act. Il documento costituisce lo strumento principale attraverso il quale l'Organizzazione effettua una valutazione sistematica della propria postura di compliance rispetto alla normativa europea piu significativa in materia di intelligenza artificiale, identificando i requisiti applicabili, verificando lo stato di implementazione e documentando eventuali gap da colmare.

La checklist copre tutti i principali obblighi previsti dal Regolamento, dalla classificazione dei sistemi AI secondo le categorie di rischio alla verifica dei requisiti specifici per i sistemi ad alto rischio, dagli obblighi di trasparenza per i sistemi a rischio limitato ai requisiti di AI literacy applicabili a tutto il personale coinvolto. Il documento supporta inoltre la preparazione ai conformity assessment, sia interni sia condotti da organismi notificati, e traccia gli obblighi post-market inclusi il monitoraggio continuo e la segnalazione degli incidenti alle autorita competenti. Attraverso l'utilizzo regolare di questa checklist, l'Organizzazione mantiene evidenza documentata del proprio percorso di compliance nel rispetto delle scadenze progressive di applicazione del Regolamento.

### 1.2 Timeline di Applicazione

```
┌──────────────────────────────────────────────────────────────────────┐
│                    EU AI ACT TIMELINE                                │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  2024                2025                2026                2027    │
│    │                   │                   │                   │    │
│    ▼                   ▼                   ▼                   ▼    │
│  Aug 1               Feb 2              Aug 2              Aug 2    │
│  Entry               Prohibited          High-Risk          High-Risk│
│  into Force          AI (Art.5)          (Annex III)        (Annex I)│
│    │                 AI Literacy         Most               Products │
│    │                 (Art.4)             obligations                 │
│    │                   │                   │                   │    │
│    │                 Aug 2                 │                   │    │
│    │                 GPAI                  │                   │    │
│    │                 Governance            │                   │    │
│    │                 Penalties             │                   │    │
│    │                   │                   │                   │    │
│    └───────────────────┴───────────────────┴───────────────────┘    │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 1.3 Ruolo dell'Organizzazione

| Ruolo | Applicabilità | Obblighi Principali |
|-------|---------------|---------------------|
| **Provider** | [ ] Sì [ ] No | Art. 9-15, 16-22, conformity assessment |
| **Deployer** | [ ] Sì [ ] No | Art. 26-27, human oversight, transparency |
| **Importer** | [ ] Sì [ ] No | Art. 23, verifiche pre-commercializzazione |
| **Distributor** | [ ] Sì [ ] No | Art. 24-25, verifiche CE marking |

---

## 2. Classificazione Sistemi AI

### 2.1 Checklist Classificazione

Per ogni sistema AI, determinare la categoria di rischio:

| ID Sistema | Nome | Vietato (Art.5) | High-Risk (Art.6) | Limited (Art.50) | Minimal |
|------------|------|-----------------|-------------------|------------------|---------|
| AI-001 | [Nome] | [ ] | [ ] | [ ] | [ ] |
| AI-002 | [Nome] | [ ] | [ ] | [ ] | [ ] |
| AI-003 | [Nome] | [ ] | [ ] | [ ] | [ ] |

### 2.2 Sistemi AI Vietati (Art. 5) - Deadline: Feb 2025

**Verificare che NESSUN sistema AI dell'organizzazione rientri in queste categorie:**

| # | Pratica Vietata | Presente | Azione |
|---|-----------------|----------|--------|
| 5.1.a | Tecniche subliminali/manipolative che causano danni | [ ] No [ ] Sì → Rimuovere | |
| 5.1.b | Sfruttamento vulnerabilità (età, disabilità, situazione sociale) | [ ] No [ ] Sì → Rimuovere | |
| 5.1.c | Social scoring da autorità pubbliche | [ ] No [ ] Sì → Rimuovere | |
| 5.1.d | Valutazione rischio reati basata solo su profilazione | [ ] No [ ] Sì → Rimuovere | |
| 5.1.e | Scraping non mirato per database riconoscimento facciale | [ ] No [ ] Sì → Rimuovere | |
| 5.1.f | Inferenza emozioni in workplace/education (salvo sicurezza) | [ ] No [ ] Sì → Valutare | |
| 5.1.g | Categorizzazione biometrica per dati sensibili | [ ] No [ ] Sì → Rimuovere | |
| 5.1.h | Identificazione biometrica real-time in spazi pubblici (law enforcement) | [ ] No [ ] Sì → Valutare eccezioni | |

### 2.3 Sistemi High-Risk (Art. 6)

**Annex I - Prodotti regolamentati EU:**

| Categoria | Esempi | Sistema Presente | ID |
|-----------|--------|------------------|-----|
| Macchine | Robot, droni industriali | [ ] | |
| Giocattoli | Giocattoli con AI | [ ] | |
| Imbarcazioni | Navigazione autonoma | [ ] | |
| Ascensori | Manutenzione predittiva | [ ] | |
| Dispositivi medici | Diagnostica AI | [ ] | |
| Dispositivi IVD | Analisi laboratorio | [ ] | |
| Veicoli | ADAS, guida autonoma | [ ] | |
| Aviazione | Manutenzione, safety | [ ] | |
| Ferroviario | Controllo traffico | [ ] | |

**Annex III - Aree ad alto rischio:**

| # | Area | Esempi | Sistema Presente | ID |
|---|------|--------|------------------|-----|
| 1 | **Biometria** | | | |
| 1.a | Identificazione biometrica remota | Face recognition | [ ] | |
| 1.b | Categorizzazione biometrica | Inferenza caratteristiche | [ ] | |
| 1.c | Riconoscimento emozioni | Emotion AI | [ ] | |
| 2 | **Infrastrutture critiche** | | | |
| 2.a | Sicurezza traffico stradale | Semafori intelligenti | [ ] | |
| 2.b | Utilities (acqua, gas, elettricità, riscaldamento) | Gestione rete, manutenzione | [ ] | |
| 2.c | Infrastrutture digitali | Network management | [ ] | |
| 3 | **Educazione** | | | |
| 3.a | Accesso/ammissione istituti | Selezione studenti | [ ] | |
| 3.b | Valutazione studenti | Grading automatico | [ ] | |
| 3.c | Monitoraggio comportamento | Proctoring | [ ] | |
| 3.d | Rilevamento cheating | Anti-plagio AI | [ ] | |
| 4 | **Occupazione** | | | |
| 4.a | Recruiting e selezione | CV screening, interview AI | [ ] | |
| 4.b | Decisioni su promozione/termine | Performance evaluation AI | [ ] | |
| 4.c | Allocazione task basata su AI | Workforce management | [ ] | |
| 4.d | Monitoraggio performance | Productivity tracking | [ ] | |
| 5 | **Servizi essenziali** | | | |
| 5.a | Eligibilità benefici pubblici | Welfare assessment | [ ] | |
| 5.b | Credit scoring | Valutazione creditizia | [ ] | |
| 5.c | Assicurazione vita/salute | Underwriting, pricing | [ ] | |
| 5.d | Servizi emergenza | Dispatch prioritization | [ ] | |
| 6 | **Law enforcement** | | | |
| 6.a | Valutazione rischio vittimizzazione | Predictive policing | [ ] | |
| 6.b | Poligrafi AI | Lie detection | [ ] | |
| 6.c | Valutazione affidabilità prove | Evidence analysis | [ ] | |
| 6.d | Profilazione | Crime prediction | [ ] | |
| 7 | **Migrazione e frontiere** | | | |
| 7.a | Poligrafi AI frontiere | Entry assessment | [ ] | |
| 7.b | Valutazione rischio immigrazione | Risk scoring | [ ] | |
| 7.c | Esame domande asilo | Asylum processing | [ ] | |
| 7.d | Rilevamento documenti | Document verification | [ ] | |
| 8 | **Giustizia** | | | |
| 8.a | Assistenza giudici | Legal research AI, sentencing | [ ] | |
| 8.b | ADR | Arbitrato/mediazione AI | [ ] | |

---

## 3. Obblighi per Sistemi High-Risk

### 3.1 Art. 9 - Sistema di Gestione del Rischio

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 9.1 | Sistema di gestione rischio stabilito, implementato, documentato, mantenuto | [ ] | | |
| 9.2.a | Identificazione e analisi rischi noti e prevedibili | [ ] | | |
| 9.2.b | Stima e valutazione rischi da uso improprio prevedibile | [ ] | | |
| 9.2.c | Valutazione rischi da dati post-market | [ ] | | |
| 9.2.d | Adozione misure di gestione rischio appropriate | [ ] | | |
| 9.3 | Rischio residuo accettabile | [ ] | | |
| 9.4 | Testing appropriato per identificare misure gestione rischio | [ ] | | |
| 9.5 | Testing condizioni realistiche | [ ] | | |
| 9.6 | Rischi da interazione con altri sistemi | [ ] | | |
| 9.7 | Specifica attenzione a rischi per minori | [ ] | | |
| 9.8 | Considerazione per persone con disabilità | [ ] | | |

### 3.2 Art. 10 - Data Governance

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 10.1 | Pratiche data governance per training, validation, testing | [ ] | | |
| 10.2.a | Scelte di design rilevanti | [ ] | | |
| 10.2.b | Processi raccolta dati | [ ] | | |
| 10.2.c | Operazioni preparazione dati (annotation, labeling, cleaning) | [ ] | | |
| 10.2.d | Formulazione assunzioni | [ ] | | |
| 10.2.e | Valutazione disponibilità, quantità, idoneità dati | [ ] | | |
| 10.2.f | Esame bias | [ ] | | |
| 10.2.g | Identificazione data gaps | [ ] | | |
| 10.3 | Dataset rilevanti, sufficientemente rappresentativi, privi di errori, completi | [ ] | | |
| 10.4 | Dataset con proprietà statistiche appropriate per intended purpose | [ ] | | |
| 10.5 | Uso dati personali per bias detection/correction (con garanzie) | [ ] | | |
| 10.6 | Per GPAI: considerare fonti dei dati | [ ] | | |

### 3.3 Art. 11 - Documentazione Tecnica

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 11.1 | Documentazione tecnica redatta prima dell'immissione in mercato | [ ] | | |
| 11.1 | Documentazione mantenuta aggiornata | [ ] | | |
| 11.1 | Contenuto conforme ad Annex IV | [ ] | | |
| 11.2 | Per GPAI integrato: cooperazione con provider GPAI | [ ] | | |

**Contenuto Annex IV (sintesi):**
- [ ] Descrizione generale sistema AI
- [ ] Descrizione elementi e processo di sviluppo
- [ ] Specifiche su monitoring, funzionamento, controllo
- [ ] Descrizione appropriatezza metriche performance
- [ ] Descrizione sistema gestione rischio
- [ ] Modifiche nel ciclo di vita
- [ ] Lista standard armonizzati applicati
- [ ] Dichiarazione UE di conformità

### 3.4 Art. 12 - Tenuta dei Registri (Logging)

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 12.1 | Capacità di logging automatico durante funzionamento | [ ] | | |
| 12.2 | Log che consentano tracciabilità funzionamento | [ ] | | |
| 12.3 | Log permettono monitoraggio per rischi | [ ] | | |
| 12.4 | Formato e design appropriato ai rischi | [ ] | | |

### 3.5 Art. 13 - Trasparenza e Informazioni ai Deployer

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 13.1 | Sistema progettato per funzionamento sufficientemente trasparente | [ ] | | |
| 13.2 | Istruzioni per l'uso con informazioni rilevanti | [ ] | | |
| 13.3.a | Identità e contatti provider | [ ] | | |
| 13.3.b | Caratteristiche, capacità, limitazioni | [ ] | | |
| 13.3.c | Cambiamenti al sistema e performance | [ ] | | |
| 13.3.d | Misure human oversight | [ ] | | |
| 13.3.e | Risorse computazionali, hardware atteso, lifetime | [ ] | | |
| 13.3.f | Input data specifications | [ ] | | |
| 13.3.g | Istruzioni interpretazione output | [ ] | | |
| 13.3.h | Specifiche tecniche | [ ] | | |

### 3.6 Art. 14 - Human Oversight

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 14.1 | Sistemi progettati per supervisione umana effettiva | [ ] | | |
| 14.2 | Misure appropriate al rischio, autonomia, contesto d'uso | [ ] | | |
| 14.3 | Identificare supervisori umani dal provider | [ ] | | |
| 14.4.a | Overseer può comprendere capacità/limitazioni | [ ] | | |
| 14.4.b | Overseer può interpretare output correttamente | [ ] | | |
| 14.4.c | Overseer può decidere di non usare output | [ ] | | |
| 14.4.d | Overseer può interpretare output e decidere override | [ ] | | |
| 14.4.e | Overseer può fermare il sistema | [ ] | | |
| 14.5 | Automation bias awareness | [ ] | | |

### 3.7 Art. 15 - Accuracy, Robustness, Cybersecurity

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 15.1 | Livello appropriato di accuracy, robustness, cybersecurity | [ ] | | |
| 15.2 | Accuracy dichiarata in istruzioni uso | [ ] | | |
| 15.3 | Robustezza contro errori, guasti, inconsistenze | [ ] | | |
| 15.4 | Resilienza contro tentativi di alterare output | [ ] | | |
| 15.5 | Protezione contro attacchi specifici AI (data poisoning, adversarial, model extraction) | [ ] | | |

---

## 4. Obblighi per Deployer (Art. 26-27)

### 4.1 Obblighi Generali Deployer (Art. 26)

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 26.1 | Misure tecniche e organizzative appropriate per human oversight | [ ] | | |
| 26.2 | Personale human oversight ha competenze, training, autorità | [ ] | | |
| 26.3 | Non usare sistema contrariamente a istruzioni uso | [ ] | | |
| 26.4 | Assicurare rilevanza input data | [ ] | | |
| 26.5 | Monitorare funzionamento, segnalare a provider, sospendere se necessario | [ ] | | |
| 26.6 | Mantenere log automatici per almeno 6 mesi | [ ] | | |
| 26.7 | Informare rappresentanti lavoratori e lavoratori interessati | [ ] | | |
| 26.8 | Cooperare con autorità | [ ] | | |

### 4.2 Fundamental Rights Impact Assessment - FRIA (Art. 27)

Per deployer di sistemi high-risk in certi contesti:

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 27.1 | FRIA condotta prima del deployment | [ ] | | |
| 27.2.a | Descrizione processi dove sarà usato | [ ] | | |
| 27.2.b | Periodo e frequenza d'uso previsti | [ ] | | |
| 27.2.c | Categorie di persone e gruppi interessati | [ ] | | |
| 27.2.d | Rischi specifici per gruppi vulnerabili | [ ] | | |
| 27.2.e | Misure human oversight | [ ] | | |
| 27.2.f | Misure in caso di materializzazione rischi | [ ] | | |
| 27.3 | Notifica ad autorità di market surveillance | [ ] | | |
| 27.4 | FRIA considerata nell'AI Impact Assessment esistente | [ ] | | |

---

## 5. Obblighi Trasparenza (Art. 50)

Per sistemi a rischio limitato:

| # | Requisito | Applicabile | Implementato | Evidenza |
|---|-----------|-------------|--------------|----------|
| 50.1 | Chatbot/AI interaction: informare utente che interagisce con AI | [ ] | [ ] | |
| 50.2 | Contenuti AI-generated (audio, immagine, video, testo): disclosure che è AI-generated | [ ] | [ ] | |
| 50.3 | Deepfake: disclosure che è artificialmente generato/manipolato | [ ] | [ ] | |
| 50.4 | Emotion recognition/biometric categorization: informare persone interessate | [ ] | [ ] | |

---

## 6. AI Literacy (Art. 4)

| # | Requisito | Implementato | Evidenza | Gap |
|---|-----------|--------------|----------|-----|
| 4 | Personale con sufficiente AI literacy per sviluppo, deployment, uso | [ ] | | |
| 4 | Misure per assicurare AI literacy proporzionate a ruolo e contesto | [ ] | | |
| 4 | Considerare skill, esperienza, formazione del personale | [ ] | | |

---

## 7. Conformity Assessment

### 7.1 Tipi di Assessment

| Tipo | Applicabilità | Sistema ID | Status |
|------|---------------|------------|--------|
| Self-assessment | Non-Annex I systems | [ ] | [ ] |
| Third-party (Notified Body) | Annex I products, some Annex III | [ ] | [ ] |
| Quality management system | Provider di high-risk | [ ] | [ ] |

### 7.2 Dichiarazione UE di Conformità (Art. 47)

| # | Contenuto Richiesto | Presente |
|---|---------------------|----------|
| 1 | Nome e tipo sistema AI | [ ] |
| 2 | Nome e indirizzo provider | [ ] |
| 3 | Dichiarazione che è responsabilità del provider | [ ] |
| 4 | Dichiarazione che sistema conforme | [ ] |
| 5 | Riferimento a standard armonizzati | [ ] |
| 6 | Data e firma | [ ] |

### 7.3 CE Marking

| Requisito | Implementato |
|-----------|--------------|
| CE marking apposto dove applicabile | [ ] |
| Marcatura visibile, leggibile, indelebile | [ ] |
| Marcatura sul prodotto o etichetta | [ ] |

---

## 8. Post-Market Monitoring (Art. 72)

| # | Requisito | Implementato | Evidenza |
|---|-----------|--------------|----------|
| 72.1 | Sistema di post-market monitoring stabilito | [ ] | |
| 72.2 | Raccolta attiva dati da deployer | [ ] | |
| 72.3 | Analisi dati per conformità continua | [ ] | |
| 72.4 | Documentazione post-market monitoring | [ ] | |
| 72.5 | Azioni correttive se necessario | [ ] | |

---

## 9. Incident Reporting (Art. 73)

| # | Requisito | Implementato | Evidenza |
|---|-----------|--------------|----------|
| 73.1 | Segnalazione serious incidents ad autorità | [ ] | |
| 73.1 | Notifica entro 15 giorni da awareness | [ ] | |
| 73.2 | Contenuto notifica conforme a requisiti | [ ] | |
| 73.3 | Indagine su incidente | [ ] | |

---

## 10. Sanzioni (Awareness)

| Violazione | Sanzione Max |
|------------|--------------|
| Sistemi AI vietati (Art. 5) | €35M o 7% fatturato |
| Obblighi provider/deployer | €15M o 3% fatturato |
| Informazioni incorrette ad autorità | €7.5M o 1.5% fatturato |

---

## 11. Riepilogo Conformità

| Area | N. Requisiti | Conformi | Parziali | Non Conformi | % Conformità |
|------|-------------|----------|----------|--------------|--------------|
| Classificazione | | | | | |
| Risk Management (Art.9) | | | | | |
| Data Governance (Art.10) | | | | | |
| Technical Doc (Art.11) | | | | | |
| Logging (Art.12) | | | | | |
| Transparency (Art.13) | | | | | |
| Human Oversight (Art.14) | | | | | |
| Accuracy/Security (Art.15) | | | | | |
| Deployer Obligations (Art.26) | | | | | |
| FRIA (Art.27) | | | | | |
| AI Literacy (Art.4) | | | | | |
| Conformity Assessment | | | | | |
| Post-Market (Art.72) | | | | | |
| **TOTALE** | | | | | |

---

## 12. Piano di Remediation

| # | Gap | Priorità | Azione | Responsabile | Scadenza |
|---|-----|----------|--------|--------------|----------|
| 1 | | [ ] Alta [ ] Media [ ] Bassa | | | |
| 2 | | [ ] Alta [ ] Media [ ] Bassa | | | |
| 3 | | [ ] Alta [ ] Media [ ] Bassa | | | |

---

## 13. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| AI Governance Lead | [Nome] | _________ | ________ |
| Legal Counsel | [Nome] | _________ | ________ |
| Top Management | [Nome] | _________ | ________ |

---

## Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## Documenti Correlati

| Codice | Documento |
|--------|-----------|
| {{company_name}}-POL-AIMS-001 | AI Policy |
| {{company_name}}-INV-AIMS-001 | AI System Inventory |
| {{company_name}}-AIIA-[ID] | AI Impact Assessment |
| {{company_name}}-MET-AIMS-001 | AI Risk Assessment Methodology |
| {{company_name}}-PRO-AIMS-002 | Human Oversight Procedure |
| {{company_name}}-POL-AIMS-002 | Data Governance Policy |

---

## Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Classificazione sistema AI verificata (Sez. 1-4)
- [ ] Requisiti Art. 9 Risk Management valutati
- [ ] Requisiti Art. 10 Data Governance valutati
- [ ] Requisiti Art. 11-12 Documentazione tecnica e logging valutati
- [ ] Requisiti Art. 13-14 Trasparenza e human oversight valutati
- [ ] Requisiti Art. 15 Accuracy e security valutati
- [ ] Obblighi deployer Art. 26 verificati
- [ ] FRIA Art. 27 completata (se applicabile)
- [ ] AI Literacy Art. 4 verificata
- [ ] Summary score compilato (Sez. 11)
- [ ] Piano remediation definito per gap identificati (Sez. 12)
- [ ] Tutti i `{{placeholder}}` sostituiti con dati reali
- [ ] Approvazioni ottenute (Sez. 13)

---

*Documento basato su Regulation (EU) 2024/1689 - EU AI Act*
