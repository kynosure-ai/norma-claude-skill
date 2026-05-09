---
title: Programma di Audit Interni BCMS
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{audit_manager}}'
approver: '{{senior_management}}'
framework: ISO22301
iso_clauses:
  - Clausola 9.2 - Audit interno
  - Clausola 9.2.1 - Generale
  - Clausola 9.2.2 - Programma di audit interno
cross_references:
  - 'ISO 19011:2018 - Guidelines for auditing management systems'
  - NIS2 Art. 21(2)(c) - Continuità operativa e gestione delle crisi
  - DORA Art. 11 - Risposta e ripristino
  - DORA Art. 25 - Test dei piani di continuità operativa ICT
  - ISO 27001 A.5.35 - Revisione indipendente della sicurezza
status: Da compilare
subset: true
---

# Programma di Audit Interni BCMS

## 1. Scopo e Obiettivi

### 1.1 Scopo

Il presente documento definisce il programma per pianificare, condurre e gestire gli audit interni del Sistema di Gestione per la Continuità Operativa di {{company_name}}. L'audit interno rappresenta uno strumento fondamentale per ottenere una valutazione obiettiva dell'efficacia del BCMS, identificando sia le aree di conformità sia le opportunità di miglioramento prima che vengano rilevate da terze parti o, peggio, da incidenti reali.

Il programma è progettato per verificare sistematicamente la conformità ai requisiti della norma ISO 22301:2019, assicurando che il sistema di gestione sia implementato e mantenuto secondo gli standard internazionali riconosciuti. Gli audit valutano l'efficacia delle strategie e dei piani di continuità, andando oltre la mera verifica documentale per accertare che le soluzioni implementate siano effettivamente in grado di garantire il recovery entro i tempi definiti.

L'identificazione delle opportunità di miglioramento costituisce un output fondamentale del processo di audit, alimentando il ciclo PDCA del sistema di gestione. Il programma integra la verifica dei requisiti specifici derivanti dalla Direttiva NIS2 e dal Regolamento DORA, assicurando che l'organizzazione mantenga la conformità normativa. I risultati degli audit forniscono input essenziali per il riesame della direzione, supportando decisioni informate sul miglioramento del BCMS.

### 1.2 Obiettivi dell'Audit

| Obiettivo | Output |
|-----------|--------|
| Verificare conformità a ISO 22301 | Finding di conformità/non conformità |
| Valutare efficacia BIA e BC Strategy | Evidence di coerenza parametri |
| Verificare adeguatezza BCP/DRP | Gap analysis rispetto a RTO/RPO |
| Validare risultati esercitazioni | Analisi trend performance |
| Verificare compliance DORA/NIS2 | Status normativo |
| Supportare miglioramento continuo | Raccomandazioni |

### 1.3 KPI del Programma Audit

| KPI | Target | Frequenza |
|-----|--------|-----------|
| Copertura requisiti ISO 22301 | 100% annuale | Annuale |
| Copertura processi critici (BIA) | 100% in 2 anni | Annuale |
| Audit eseguiti vs pianificati | >95% | Trimestrale |
| Finding chiusi entro SLA | >90% | Trimestrale |
| Finding critici aperti | 0 | Mensile |
| Partecipazione a esercitazioni | 100% aree critiche | Annuale |

---

## 2. Governance del Programma

### 2.1 Ruoli e Responsabilità

| Ruolo | Responsabilità |
|-------|----------------|
| **Direzione** | Approvazione programma, risorse, review risultati |
| **Audit Manager** | Gestione programma, selezione auditor, reporting |
| **Lead Auditor** | Pianificazione audit, coordinamento team, report |
| **Auditor** | Esecuzione audit, raccolta evidence, finding |
| **Auditee** | Fornire accesso, informazioni, risposte a finding |
| **BC Manager** | Supporto tecnico, prioritizzazione, remediation |

### 2.2 Requisiti Auditor

**Competenze richieste:**

| Area | Lead Auditor | Auditor |
|------|--------------|---------|
| Certificazione ISO 22301 LA | Richiesta | Preferita |
| Esperienza audit BCMS | >3 anni | >1 anno |
| Conoscenza BIA/BCP/DRP | Avanzata | Buona |
| Competenze tecniche IT/DR | Buone | Base |
| Formazione ISO 19011 | Completata | Completata |
| Conoscenza DORA/NIS2 | Buona | Base |

**Indipendenza:**
- L'auditor non può verificare la propria area di responsabilità
- L'auditor non può verificare piani di cui è owner
- Rotazione auditor ogni 3 anni per stessa area
- Conflitti di interesse dichiarati e gestiti

---

## 3. Pianificazione Triennale

### 3.1 Ciclo di Audit

```
┌─────────────────────────────────────────────────────────────┐
│               CICLO AUDIT TRIENNALE BCMS                    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ANNO 1: Copertura completa framework                      │
│  ├── Tutti i requisiti clausole 4-10                       │
│  ├── BIA processi critici (MTPD ≤24h)                     │
│  ├── Piani BC/DR per sistemi Tier 1                       │
│  └── Risultati esercitazioni                               │
│                                                             │
│  ANNO 2: Focus su efficacia e DORA                         │
│  ├── Requisiti con finding precedenti                      │
│  ├── Processi priorità alta (MTPD 24-72h)                 │
│  ├── Verifica RTO/RPO effettivi vs target                 │
│  └── Compliance DORA Art. 11, 25                          │
│                                                             │
│  ANNO 3: Completamento e maturità                          │
│  ├── Processi rimanenti                                    │
│  ├── Supply chain continuity                               │
│  ├── Verifica remediation                                  │
│  └── Preparazione certificazione/rinnovo                   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 3.2 Matrice Copertura Clausole ISO 22301

| Clausola | Requisito | Anno 1 | Anno 2 | Anno 3 |
|----------|-----------|--------|--------|--------|
| **4.1** | Contesto organizzazione | ✓ | | ✓ |
| **4.2** | Parti interessate | ✓ | | ✓ |
| **4.3** | Ambito BCMS | ✓ | ✓ | ✓ |
| **4.4** | BCMS | ✓ | ✓ | ✓ |
| **5.1** | Leadership e impegno | ✓ | | ✓ |
| **5.2** | Politica | ✓ | ✓ | ✓ |
| **5.3** | Ruoli e responsabilità | ✓ | | ✓ |
| **6.1** | Rischi e opportunità | ✓ | ✓ | ✓ |
| **6.2** | Obiettivi continuità | ✓ | ✓ | ✓ |
| **6.3** | Pianificazione modifiche | ✓ | ✓ | |
| **7.1** | Risorse | ✓ | | ✓ |
| **7.2** | Competenza | ✓ | ✓ | ✓ |
| **7.3** | Consapevolezza | ✓ | ✓ | ✓ |
| **7.4** | Comunicazione | ✓ | ✓ | ✓ |
| **7.5** | Informazioni documentate | ✓ | ✓ | ✓ |
| **8.1** | Pianificazione operativa | ✓ | ✓ | ✓ |
| **8.2** | BIA e Risk Assessment | ✓ | ✓ | ✓ |
| **8.3** | BC Strategy | ✓ | ✓ | ✓ |
| **8.4** | BC Plans (BCP, DRP, CMP) | ✓ | ✓ | ✓ |
| **8.5** | Esercitazioni e test | ✓ | ✓ | ✓ |
| **8.6** | Valutazione documentazione | ✓ | ✓ | ✓ |
| **9.1** | Monitoring e misurazione | ✓ | ✓ | ✓ |
| **9.2** | Audit interno | ✓ | ✓ | ✓ |
| **9.3** | Management review | ✓ | ✓ | ✓ |
| **10.1** | Non conformità e azioni correttive | ✓ | ✓ | ✓ |
| **10.2** | Miglioramento continuo | ✓ | ✓ | ✓ |

### 3.3 Piano Audit Elementi BCMS

| Elemento | Focus Audit | Anno 1 | Anno 2 | Anno 3 |
|----------|-------------|--------|--------|--------|
| BIA | Metodologia, MTPD/RTO/RPO | ✓ | ✓ | ✓ |
| BC Risk Assessment | Minacce, impatti, trattamento | ✓ | ✓ | |
| BC Strategy | Adeguatezza, copertura | ✓ | ✓ | ✓ |
| BCP | Completezza, aggiornamento | ✓ | ✓ | ✓ |
| IT DRP | RTO/RPO, runbook, backup | ✓ | ✓ | ✓ |
| Crisis Management Plan | CMT, comunicazione | ✓ | | ✓ |
| Esercitazioni | Copertura, risultati, lesson learned | ✓ | ✓ | ✓ |
| Supply Chain BC | Fornitori critici, SLA | | ✓ | ✓ |

**Criteri di prioritizzazione:**
1. Processi con MTPD ≤4h = Ogni anno
2. Processi con incident passati = Priorità aumentata
3. Nuove strategie/piani = Primo anno di implementazione
4. Elementi con finding precedenti = Review più frequente

---

## 4. Piano Audit Annuale {{document_year}}

### 4.1 Calendario Audit

| ID | Audit | Scope | Periodo | Lead Auditor | Giorni |
|----|-------|-------|---------|--------------|--------|
| A1 | Governance BCMS | Clausole 4, 5 | Q1 | {{contact_name}} | 2 |
| A2 | BIA e Risk Assessment | Clausole 8.2 | Q1 | {{contact_name}} | 3 |
| A3 | BC Strategy | Clausola 8.3 | Q2 | {{contact_name}} | 2 |
| A4 | Business Continuity Plans | Clausola 8.4, BCP | Q2 | {{contact_name}} | 3 |
| A5 | IT Disaster Recovery | Clausola 8.4, DRP | Q2 | {{contact_name}} | 3 |
| A6 | Crisis Management | Clausola 8.4, CMP | Q3 | {{contact_name}} | 2 |
| A7 | Esercitazioni | Clausola 8.5 | Q3 | {{contact_name}} | 2 |
| A8 | Risorse e Competenze | Clausola 7 | Q4 | {{contact_name}} | 2 |
| A9 | Monitoring e Review | Clausole 9, 10 | Q4 | {{contact_name}} | 2 |

### 4.2 Audit Post-Esercitazione

| Esercitazione | Timing Audit | Focus |
|---------------|--------------|-------|
| Tabletop | +2 settimane | Lesson learned recepiti |
| Simulation | +4 settimane | Verifica azioni correttive |
| Full test DR | +4 settimane | RTO/RPO effettivi vs target |

### 4.3 Risorse

| Risorsa | Q1 | Q2 | Q3 | Q4 | Totale |
|---------|----|----|----|----|--------|
| Giorni audit pianificati | 5 | 8 | 4 | 4 | 21 |
| Lead Auditor (giorni) | 5 | 8 | 4 | 4 | 21 |
| Auditor supporto (giorni) | 3 | 5 | 2 | 2 | 12 |
| Budget stimato (€) | | | | | |

### 4.4 Trigger per Audit Straordinari

| Trigger | Azione |
|---------|--------|
| Incidente grave con attivazione BCP | Audit entro 30gg da chiusura |
| Esercitazione con esito negativo | Audit follow-up immediato |
| Cambio significativo processi critici | Rivalutazione piano |
| Finding critico non risolto | Follow-up audit |
| Nuova normativa (es. DORA) | Audit compliance |
| Audit esterno imminente | Pre-audit interno |

---

## 5. Processo di Audit

### 5.1 Fasi dell'Audit

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│ PIANIFICAZIONE│───►│ PREPARAZIONE │───►│  ESECUZIONE  │
│   2 sett     │    │   1 sett     │    │  1-4 giorni  │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│   CHIUSURA   │◄───│  REPORTING   │◄───│  FOLLOW-UP   │
│   1 sett     │    │   2 sett     │    │  Continuo    │
└──────────────┘    └──────────────┘    └──────────────┘
```

### 5.2 Pianificazione (Pre-Audit)

**Attività:**

| Attività | Output | Responsabile |
|----------|--------|--------------|
| Definire obiettivi | Audit objectives | Audit Manager |
| Identificare scope | Audit scope statement | Lead Auditor |
| Rivedere BIA/piani | Document review notes | Auditor |
| Rivedere esito esercitazioni | Exercise analysis | Auditor |
| Preparare piano | Audit plan | Lead Auditor |
| Comunicare auditee | Notification letter | Audit Manager |

**Piano di Audit - Contenuto:**
```
AUDIT PLAN BCMS
---------------
ID Audit: {{audit_id}}
Titolo: {{audit_title}}
Data: {{start_date}} - {{end_date}}

1. OBIETTIVI
   - {{audit_objective_1}}
   - {{audit_objective_2}}

2. SCOPE
   - Processi: {{audit_scope_processes}}
   - Piani: {{audit_scope_plans}}
   - Sistemi: {{audit_scope_systems}}
   - Esclusioni: {{audit_scope_exclusions}}

3. CRITERI
   - ISO 22301:2019
   - DORA Art. 11, 25 (se applicabile)
   - NIS2 Art. 21(2)(c) (se applicabile)
   - Politiche interne
   - BIA parameters (MTPD/RTO/RPO)

4. TEAM AUDIT
   - Lead Auditor: {{lead_auditor}}
   - Auditor: {{auditor}}
   - Technical Expert: {{technical_expert}} (per DR audit)

5. AGENDA
   Compilare tabella con date, orari, attività, interlocutori.

6. DOCUMENTAZIONE RICHIESTA
   - BIA aggiornata
   - BCP/DRP pertinenti
   - Report esercitazioni
   - Incident log
   - Risk register BC

7. LOGISTICA
   Compilare con informazioni pratiche (sale, strumenti, accessi).
```

### 5.3 Esecuzione

**Metodi di raccolta evidence:**

| Metodo | Utilizzo BCMS | Evidence Type |
|--------|---------------|---------------|
| Interviste | Comprensione processi, ruoli CMT | Testimonianze |
| Osservazione | Esercitazioni, DR test | Osservazioni dirette |
| Revisione documenti | BIA, BCP, DRP, CMP | Documentale |
| Test tecnici | Backup restore, failover | Tecnica |
| Walkthrough | Procedure operative | Simulazione |
| Sampling | Backup, log, comunicazioni | Campione |

**Checklist Esecuzione:**
- [ ] Opening meeting condotto
- [ ] Agenda confermata con BC Manager
- [ ] Evidence raccolte per ogni criterio
- [ ] Finding documentati in tempo reale
- [ ] Auditee informato di potenziali NC
- [ ] Verifica parametri BIA vs piani
- [ ] Verifica risultati esercitazioni
- [ ] Closing meeting condotto
- [ ] Evidence archiviate

### 5.4 Classificazione Finding

| Categoria | Definizione | Esempio BCMS |
|-----------|-------------|--------------|
| **Non Conformità Maggiore (NCM)** | Assenza o totale inefficacia di requisito | Nessuna BIA eseguita |
| **Non Conformità Minore (NCm)** | Deviazione parziale che non compromette sistema | BIA non aggiornata dopo cambio processi |
| **Osservazione (OBS)** | Opportunità di miglioramento | Documentazione DRP migliorabile |
| **Best Practice (BP)** | Pratica eccellente da diffondere | Automazione DR efficace |

### 5.5 Formato Finding

```
FINDING REPORT
--------------
ID: {{finding_id}}
Classificazione: {{finding_classification}}
Data rilevamento: {{document_date}}
Auditor: {{contact_name}}

AREA/PROCESSO: {{finding_process}}

CRITERIO: {{finding_criterion}}

EVIDENZA:
{{finding_evidence}}

ANALISI:
{{finding_gap_analysis}}

RISCHIO/IMPATTO:
{{finding_risk_impact}}

RACCOMANDAZIONE:
{{finding_recommendation}}

RISPOSTA AUDITEE:
- Root Cause: {{root_cause_analysis}}
- Piano Azione: {{corrective_actions}}
- Responsabile: {{action_owner}}
- Scadenza: {{action_deadline}}
```

---

## 6. Audit Specifici BCMS

### 6.1 Audit BIA

**Scope:**

| Elemento | Verifica |
|----------|----------|
| Metodologia | Coerenza con ISO 22301 8.2.2 |
| Copertura | Tutti i processi nel scope BCMS |
| MTPD | Determinazione corretta per processo |
| RTO | RTO < MTPD verificato |
| RPO | Coerenza con frequenza backup |
| MBCO | Definito per processi critici |
| Dipendenze | Mappate (IT, fornitori, persone) |
| Aggiornamento | Entro 12 mesi o post-cambio |

**Checklist BIA:**
- [ ] Tutti i processi in scope analizzati
- [ ] Owner processo intervistati
- [ ] Impatti quantificati (finanziari, operativi, reputazionali)
- [ ] Scale di impatto documentate e approvate
- [ ] MTPD giustificati e approvati dalla Direzione
- [ ] RTO coerenti con MTPD
- [ ] RPO coerenti con politiche backup
- [ ] Dipendenze critiche identificate
- [ ] Risorse minime (MBCO) definite

### 6.2 Audit BC Plans (BCP)

**Scope:**

| Elemento | Verifica |
|----------|----------|
| Copertura | Piano per ogni processo critico |
| Attivazione | Trigger e criteri chiari |
| Ruoli | CMT definito, contatti aggiornati |
| Procedure | Dettagliate, praticabili |
| Comunicazione | Stakeholder, template |
| Risorse | Alternative sedi, personale |
| Coerenza BIA | RTO/RPO del piano ≤ BIA |
| Test | Esercitazione negli ultimi 12 mesi |

**Checklist BCP:**
- [ ] Piano approvato e versionato
- [ ] Criteri attivazione documentati
- [ ] CMT ruoli e responsabilità definiti
- [ ] Contact list aggiornata (<3 mesi)
- [ ] Procedure step-by-step disponibili
- [ ] Workaround manuali documentati
- [ ] Template comunicazione pronti
- [ ] Piano testato con esercitazione

### 6.3 Audit IT Disaster Recovery (DRP)

**Scope:**

| Elemento | Verifica |
|----------|----------|
| Tiering | Sistemi classificati per criticità |
| RTO/RPO | Definiti per sistema, coerenti con BIA |
| Backup | Strategia 3-2-1-1, test restore |
| DR Site | Capacità, aggiornamento |
| Runbook | Procedure dettagliate |
| Failover | Test periodici |
| Failback | Procedure documentate |
| DORA | Compliance Art. 12 (backup), Art. 25 (test) |

**Checklist DRP:**
- [ ] Inventario sistemi critici aggiornato
- [ ] RTO/RPO per sistema documentati
- [ ] Backup giornaliero sistemi critici
- [ ] Test restore trimestrale (DORA)
- [ ] DR site sincronizzato
- [ ] Runbook per ogni sistema Tier 1
- [ ] Test failover annuale (minimo)
- [ ] Documentazione failback
- [ ] Log backup verificati

### 6.4 Audit Esercitazioni

**Scope:**

| Elemento | Verifica |
|----------|----------|
| Programma | Piano annuale approvato |
| Copertura | Processi critici testati |
| Tipologie | Mix adeguato (tabletop, simulation, full) |
| Partecipazione | CMT e stakeholder coinvolti |
| Scenari | Realistici, aggiornati |
| Risultati | Documentati, analizzati |
| Lesson Learned | Recepiti in aggiornamento piani |
| DORA | Test annuale (Art. 25), TLPT (Art. 26) |

**Checklist Esercitazioni:**
- [ ] Piano esercitazioni approvato
- [ ] Almeno 1 esercitazione/anno per processo critico
- [ ] Test DR almeno annuale per sistemi Tier 1
- [ ] After Action Report prodotti
- [ ] Lesson learned tracciati
- [ ] Azioni correttive implementate
- [ ] KPI performance tracciati (RTO effettivo)
- [ ] Trend performance analizzato

### 6.5 Audit DORA Compliance (per soggetti finanziari)

**Scope:**

| Articolo DORA | Verifica |
|---------------|----------|
| Art. 11(1) | Politica continuità ICT documentata |
| Art. 11(3) | BIA per servizi ICT critici |
| Art. 11(4) | Scenari gravi ma plausibili |
| Art. 11(6) | Funzioni essenziali e critiche identificate |
| Art. 12(1) | Politiche backup documentate |
| Art. 12(2) | Sistemi backup separati, immutabili |
| Art. 12(3) | Test restore periodici |
| Art. 25(1) | Test annuale piani continuità |
| Art. 25(2) | Scenari test appropriati |
| Art. 26 | TLPT per entità significative |

---

## 7. Reporting

### 7.1 Report di Audit

**Struttura Report:**

```
AUDIT REPORT BCMS
=================

1. EXECUTIVE SUMMARY
   - Conclusione generale
   - Principali finding
   - Raccomandazioni chiave

2. INFORMAZIONI AUDIT
   - ID e titolo
   - Date e durata
   - Team audit
   - Scope e criteri

3. METODOLOGIA
   - Approccio
   - Campionamento
   - Limitazioni

4. RISULTATI
   4.1 Conformità per clausola ISO 22301
   4.2 Status elementi BCMS
       - BIA
       - BC Strategy
       - BCP
       - DRP
       - CMP
       - Esercitazioni
   4.3 Finding dettagliati
   4.4 Osservazioni
   4.5 Best practice identificate

5. RIEPILOGO FINDING
   | ID | Classificazione | Area | Scadenza |
   |----|-----------------|------|----------|

6. COMPLIANCE DORA/NIS2
   - Gap identificati
   - Raccomandazioni

7. CONCLUSIONI
   - Livello complessivo di conformità
   - Efficacia BCMS
   - Aree di miglioramento

8. PROSSIMI PASSI
   - Remediation plan
   - Follow-up audit
   - Escalation

9. ALLEGATI
   - Evidence
   - Working papers
```

### 7.2 Dashboard Audit BCMS

| Metrica | Q1 | Q2 | Q3 | Q4 | YTD |
|---------|----|----|----|----|-----|
| Audit pianificati | | | | | |
| Audit eseguiti | | | | | |
| NCM rilevate | | | | | |
| NCm rilevate | | | | | |
| OBS rilevate | | | | | |
| Finding chiusi | | | | | |
| Finding aperti | | | | | |
| % conformità ISO 22301 | | | | | |
| % conformità DORA | | | | | |

### 7.3 Distribuzione Report

| Destinatario | Contenuto | Timing |
|--------------|-----------|--------|
| Direzione | Executive summary | 5gg da chiusura |
| BC Manager | Report completo | 5gg da chiusura |
| Auditee | Finding area + azioni | 5gg da chiusura |
| Management Review | Sintesi annuale | Pre-review |
| Regolatori (se richiesto) | Sintesi compliance | Su richiesta |

---

## 8. Gestione Finding e Remediation

### 8.1 SLA per Risoluzione

| Classificazione | Impatto su BC | SLA Risposta | SLA Risoluzione |
|-----------------|---------------|--------------|-----------------|
| NCM - RTO/RPO non raggiunti | Critico | 3 giorni | 30 giorni |
| NCM - Altro | Alto | 5 giorni | 45 giorni |
| NCm | Medio | 10 giorni | 60 giorni |
| OBS | Basso | 20 giorni | 90 giorni |

### 8.2 Processo Remediation

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   FINDING    │───►│ ROOT CAUSE   │───►│    PIANO     │
│  Comunicato  │    │   ANALYSIS   │    │   AZIONE     │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│   CHIUSURA   │◄───│   VERIFICA   │◄───│IMPLEMENTAZIONE│
│              │    │  (test se BC)│    │              │
└──────────────┘    └──────────────┘    └──────────────┘
```

### 8.3 Tracking Finding

| ID | Classificazione | Area | Processo | Owner | Scadenza | Status | Verifica |
|----|-----------------|------|----------|-------|----------|--------|----------|
| F-2024-001 | NCM | DRP | {{finding_process}} | IT Manager | {{document_date}} | In progress | {{document_date}} |
| F-2024-002 | NCm | BIA | {{finding_process}} | BC Manager | {{document_date}} | Closed | {{document_date}} |

### 8.4 Escalation

| Condizione | Escalation To | Azione |
|------------|---------------|--------|
| NCM su RTO/RPO non risolta | Direzione | Recovery plan urgente |
| NCM non risolta entro SLA | BC Manager + Direzione | Risk acceptance |
| NCm non risolta >90gg | BC Manager | Review priorità |
| Pattern ricorrente | Management Review | Root cause sistemica |
| Esercitazione fallita | Direzione | Re-test entro 30gg |

---

## 9. Documentazione e Records

### 9.1 Documenti da Mantenere

| Documento | Retention | Ubicazione |
|-----------|-----------|------------|
| Programma audit | Vita BCMS | {{document_management_system}} |
| Piani audit | 5 anni | {{document_management_system}} |
| Report audit | 5 anni | {{document_management_system}} |
| Working papers | 3 anni | {{document_management_system}} |
| Evidence | 3 anni | {{document_management_system}} |
| Tracking finding | 5 anni | {{document_management_system}} |
| Competenze auditor | Vita auditor | HR |
| Report esercitazioni | 5 anni | {{document_management_system}} |

### 9.2 Protezione Evidence

| Requisito | Implementazione |
|-----------|-----------------|
| Integrità | Hash/signature |
| Riservatezza | Accesso controllato |
| Disponibilità | Backup |
| Tracciabilità | Audit trail |

---

## 10. Miglioramento del Programma

### 10.1 Review del Programma

| Aspetto | Frequenza | Responsabile |
|---------|-----------|--------------|
| Efficacia programma | Annuale | Audit Manager |
| Competenze auditor | Annuale | Audit Manager |
| Metodologia | Post-certificazione | BC Manager |
| Feedback auditee | Post-audit | Lead Auditor |
| Allineamento normativo | Semestrale | Audit Manager |
| Lesson learned esercitazioni | Post-esercitazione | Lead Auditor |

### 10.2 Input per Management Review

- Risultati audit interni del periodo
- Trend finding per area (BIA, BCP, DRP)
- Status remediation
- KPI programma
- Risultati esercitazioni e test
- Gap compliance DORA/NIS2
- Raccomandazioni per miglioramento
- Risorse richieste

---

## 11. Allegati

### Allegato A - Checklist Audit ISO 22301

Checklist dettagliate per clausole ISO 22301, da utilizzare come guida durante l'esecuzione dell'audit.

### Allegato B - Template Piano Audit

Template compilabile per la pianificazione di ciascun audit programmato.

### Allegato C - Template Report Audit

Template compilabile per la redazione del report finale di audit.

### Allegato D - Competenze Auditor Team

| Nome | Certificazioni | Esperienza | Aree Competenza |
|------|----------------|------------|-----------------|
| {{contact_name}} | ISO 22301 LA, CBCI | {{auditor_experience_years}} anni | {{auditor_competence_areas}} |

### Allegato E - Mappatura Audit - BIA

| ID Processo | Processo | MTPD | Ultimo Audit | Prossimo Audit |
|-------------|----------|------|--------------|----------------|
| P01 | {{process_name}} | {{mtpd_hours}}h | {{document_date}} | {{document_date}} |

### Allegato F - Contatti

| Ruolo | Nome | Email | Telefono |
|-------|------|-------|----------|
| Audit Manager | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| Lead Auditor | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| BC Manager | {{contact_name}} | {{contact_email}} | {{contact_phone}} |

---

## 12. Documenti Correlati

| ID Documento | Titolo | Relazione |
|--------------|--------|-----------|
| {{company_name}}-POL-BCMS-001 | Politica di Continuità Operativa | Framework: policy di riferimento per l'audit |
| {{company_name}}-BIA-BCMS-001 | Business Impact Analysis | Input: processi critici e parametri da verificare |
| {{company_name}}-BCP-BCMS-001 | Piano di Continuità Operativa | Oggetto: piano sottoposto ad audit |
| {{company_name}}-DRP-BCMS-001 | Piano di Disaster Recovery IT | Oggetto: piano sottoposto ad audit |
| {{company_name}}-CMP-BCMS-001 | Piano di Crisis Management | Oggetto: piano sottoposto ad audit |
| {{company_name}}-RVA-BCMS-001 | Valutazione Rischi BC | Input: rischi che guidano priorità audit |
| {{company_name}}-MR-BCMS-001 | Verbale Riesame Direzione BCMS | Output: risultati audit come input per riesame |

---

## 13. Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Owner audit nel frontmatter ({{audit_manager}})
- [ ] KPI target del programma validati (Sezione 1.3)
- [ ] Requisiti auditor definiti (anni esperienza, certificazioni)
- [ ] Piano triennale compilato per Anno 1/2/3 (Sezione 3)
- [ ] Calendario audit annuale con lead auditor e giorni (Sezione 4.1)
- [ ] Budget e risorse per ciascun trimestre (Sezione 4.3)
- [ ] Template piano audit compilato con scope e team (Sezione 5.2)
- [ ] SLA per risoluzione finding validati (Sezione 8.1)
- [ ] Sistema documentale indicato ({{document_management_system}}) per tutti i record
- [ ] Competenze auditor compilate (Allegato D): {{auditor_experience_years}}, {{auditor_competence_areas}}
- [ ] Mappatura processi BIA (Allegato E): {{process_name}}, {{mtpd_hours}}
- [ ] Approvazioni firmate da {{contact_name}}, {{audit_manager}}, {{senior_management}}

---

## 14. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 15. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{audit_manager}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |
