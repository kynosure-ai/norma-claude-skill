---
title: Programma di Audit Interni ISMS
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{audit_manager}}'
approver: '{{senior_management}}'
framework: ISO27001
language: IT
documentType: plan
iso_controls:
  - Clausola 9.2 - Audit interno
  - Clausola 9.2.1 - Generale
  - Clausola 9.2.2 - Programma di audit interno
  - A.5.35 - Revisione indipendente della sicurezza delle informazioni
  - 'A.5.36 - Conformità a politiche, regole e standard'
cross_references:
  - 'ISO 19011:2018 - Guidelines for auditing management systems'
  - NIS2 Art. 21 - Misure di gestione dei rischi
  - DORA Art. 6 - Quadro di gestione rischi ICT
  - GDPR Art. 32 - Sicurezza del trattamento
status: Da approvare
subset: true
---

# Programma di Audit Interni ISMS

## 1. Scopo e Obiettivi

### 1.1 Scopo

Il presente programma definisce l'approccio sistematico dell'Organizzazione alla pianificazione, conduzione e gestione degli audit interni del Sistema di Gestione per la Sicurezza delle Informazioni (ISMS). L'audit interno rappresenta uno strumento fondamentale di governance che consente di verificare in modo indipendente e oggettivo la conformita del sistema ai requisiti della norma ISO/IEC 27001:2022 e alle politiche interne dell'Organizzazione.

Attraverso un ciclo strutturato di verifiche, il programma mira a valutare l'efficacia operativa dei controlli di sicurezza implementati, identificando eventuali gap tra le pratiche correnti e i requisiti stabiliti. Il processo di audit contribuisce inoltre all'identificazione proattiva di opportunita di miglioramento continuo, alimentando il ciclo Plan-Do-Check-Act che caratterizza ogni sistema di gestione maturo. I risultati degli audit costituiscono un input essenziale per il management review, fornendo alla Direzione evidenze oggettive sullo stato del sistema e supportando decisioni informate in materia di sicurezza delle informazioni.

### 1.2 Obiettivi dell'Audit
| Obiettivo | Output |
|-----------|--------|
| Verificare conformità a ISO 27001 | Finding di conformità/non conformità |
| Valutare efficacia controlli | Evidence di efficacia operativa |
| Verificare conformità a policy interne | Gap analysis |
| Identificare rischi emergenti | Risk observations |
| Supportare miglioramento continuo | Raccomandazioni |

### 1.3 KPI del Programma Audit

| KPI | Target | Frequenza |
|-----|--------|-----------|
| Copertura requisiti ISO | 100% annuale | Annuale |
| Copertura controlli SoA | 100% in 3 anni | Annuale |
| Audit eseguiti vs pianificati | >95% | Trimestrale |
| Finding chiusi entro SLA | >90% | Trimestrale |
| Finding critici aperti | 0 | Mensile |

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
| **CISO** | Supporto tecnico, prioritizzazione, remediation |

### 2.2 Requisiti Auditor

**Competenze richieste:**
| Area | Lead Auditor | Auditor |
|------|--------------|---------|
| Certificazione ISO 27001 LA | Richiesta | Preferita |
| Esperienza audit ISMS | >3 anni | >1 anno |
| Conoscenza normativa | Avanzata | Buona |
| Competenze tecniche IT | Buone | Base |
| Formazione ISO 19011 | Completata | Completata |

**Indipendenza:**
- L'auditor non può verificare la propria area di responsabilità
- Rotazione auditor ogni 3 anni per stessa area
- Conflitti di interesse dichiarati e gestiti

---

## 3. Pianificazione Triennale

### 3.1 Ciclo di Audit

```
┌─────────────────────────────────────────────────────────────┐
│                 CICLO AUDIT TRIENNALE                       │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ANNO 1: Copertura completa                                │
│  ├── Tutti i requisiti clausole 4-10                       │
│  ├── Controlli critici (tutti)                             │
│  └── Controlli alto rischio (tutti)                        │
│                                                             │
│  ANNO 2: Focus su rischio e performance                    │
│  ├── Requisiti con finding precedenti                      │
│  ├── Controlli medio rischio                               │
│  └── Nuovi controlli implementati                          │
│                                                             │
│  ANNO 3: Completamento e trend                             │
│  ├── Controlli rimanenti                                   │
│  ├── Verifica remediation                                  │
│  └── Preparazione certificazione                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 3.2 Matrice Copertura Clausole ISO 27001

| Clausola | Requisito | Anno 1 | Anno 2 | Anno 3 |
|----------|-----------|--------|--------|--------|
| **4.1** | Contesto organizzazione | ✓ | | ✓ |
| **4.2** | Parti interessate | ✓ | | ✓ |
| **4.3** | Ambito ISMS | ✓ | ✓ | ✓ |
| **4.4** | ISMS | ✓ | ✓ | ✓ |
| **5.1** | Leadership e impegno | ✓ | | ✓ |
| **5.2** | Politica | ✓ | ✓ | ✓ |
| **5.3** | Ruoli e responsabilità | ✓ | | ✓ |
| **6.1** | Rischi e opportunità | ✓ | ✓ | ✓ |
| **6.2** | Obiettivi sicurezza | ✓ | ✓ | ✓ |
| **6.3** | Pianificazione modifiche | ✓ | ✓ | |
| **7.1** | Risorse | ✓ | | ✓ |
| **7.2** | Competenza | ✓ | ✓ | ✓ |
| **7.3** | Consapevolezza | ✓ | ✓ | ✓ |
| **7.4** | Comunicazione | ✓ | | ✓ |
| **7.5** | Informazioni documentate | ✓ | ✓ | ✓ |
| **8.1** | Pianificazione operativa | ✓ | ✓ | ✓ |
| **8.2** | Risk assessment | ✓ | ✓ | ✓ |
| **8.3** | Risk treatment | ✓ | ✓ | ✓ |
| **9.1** | Monitoring e misurazione | ✓ | ✓ | ✓ |
| **9.2** | Audit interno | ✓ | ✓ | ✓ |
| **9.3** | Management review | ✓ | ✓ | ✓ |
| **10.1** | Non conformità e azioni correttive | ✓ | ✓ | ✓ |
| **10.2** | Miglioramento continuo | ✓ | ✓ | ✓ |

### 3.3 Piano Controlli Annex A

| Categoria | Controlli | Anno 1 | Anno 2 | Anno 3 |
|-----------|-----------|--------|--------|--------|
| A.5 Organizzativi | 37 | 20 | 10 | 7 |
| A.6 Persone | 8 | 8 | 4 | 4 |
| A.7 Fisici | 14 | 14 | 7 | 7 |
| A.8 Tecnologici | 34 | 20 | 14 | 14 |
| **Totale** | **93** | **62** | **35** | **32** |

**Criteri di prioritizzazione:**
1. Controlli per rischi Critici/Alti = Anno 1
2. Controlli con incident passati = Priorità aumentata
3. Nuovi controlli = Primo anno di implementazione
4. Controlli con finding precedenti = Review più frequente

---

## 4. Piano Audit Annuale {{document_year}}

### 4.1 Calendario Audit

| ID | Audit | Scope | Periodo | Lead Auditor | Giorni |
|----|-------|-------|---------|--------------|--------|
| A1 | Leadership e Governance | Clausole 4, 5 | Q1 | {{contact_name}} | 2 |
| A2 | Risk Management | Clausole 6, 8.2-8.3 | Q1 | {{contact_name}} | 3 |
| A3 | HR e Awareness | A.6 completo | Q2 | {{contact_name}} | 2 |
| A4 | Access Control | A.5.15-18, A.8.2-5 | Q2 | {{contact_name}} | 3 |
| A5 | Operations | Clausole 7, 8.1 | Q3 | {{contact_name}} | 2 |
| A6 | Incident & BC | A.5.24-30 | Q3 | {{contact_name}} | 2 |
| A7 | Technical Controls | A.8.6-34 | Q3 | {{contact_name}} | 4 |
| A8 | Suppliers | A.5.19-23 | Q4 | {{contact_name}} | 2 |
| A9 | Monitoring & Review | Clausole 9, 10 | Q4 | {{contact_name}} | 2 |

### 4.2 Risorse

| Risorsa | Q1 | Q2 | Q3 | Q4 | Totale |
|---------|----|----|----|----|--------|
| Giorni audit pianificati | 5 | 5 | 8 | 4 | 22 |
| Lead Auditor (giorni) | 5 | 5 | 8 | 4 | 22 |
| Auditor supporto (giorni) | 3 | 3 | 5 | 2 | 13 |
| Budget stimato (€) | | | | | |

### 4.3 Modifiche al Piano

| Trigger | Azione |
|---------|--------|
| Incidente grave di sicurezza | Audit straordinario area impattata |
| Cambio significativo scope | Rivalutazione piano |
| Finding critico non risolto | Follow-up audit |
| Richiesta management | Audit ad-hoc |
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
| Rivedere documentazione | Document review notes | Auditor |
| Identificare criteri | Audit criteria | Lead Auditor |
| Preparare piano | Audit plan | Lead Auditor |
| Comunicare auditee | Notification letter | Audit Manager |

**Piano di Audit - Contenuto:**
```
AUDIT PLAN
----------
ID Audit: [CODICE]
Titolo: [NOME AUDIT]
Data: {{start_date}} - {{end_date}}

1. OBIETTIVI
   - [Obiettivo 1]
   - [Obiettivo 2]

2. SCOPE
   - Processi: [Lista]
   - Controlli: [Lista]
   - Locazioni: [Lista]
   - Esclusioni: [Lista]

3. CRITERI
   - ISO/IEC 27001:2022
   - Politiche interne
   - Procedure applicabili
   - Requisiti contrattuali/normativi

4. TEAM AUDIT
   - Lead Auditor: [Nome]
   - Auditor: [Nome]
   - Osservatori: [Nome]

5. AGENDA
   [Tabella con date, orari, attività, interlocutori]

6. DOCUMENTAZIONE RICHIESTA
   [Lista documenti da preparare]

7. LOGISTICA
   [Informazioni pratiche]
```

### 5.3 Esecuzione

**Metodi di raccolta evidence:**
| Metodo | Utilizzo | Evidence Type |
|--------|----------|---------------|
| Interviste | Comprensione processi | Testimonianze |
| Osservazione | Verifica pratiche | Osservazioni dirette |
| Revisione documenti | Verifica conformità | Documentale |
| Test tecnici | Verifica controlli IT | Tecnica |
| Sampling | Verifica applicazione | Campione |

**Checklist Esecuzione:**
- [ ] Opening meeting condotto
- [ ] Agenda confermata
- [ ] Evidence raccolte per ogni criterio
- [ ] Finding documentati in tempo reale
- [ ] Auditee informato di potenziali NC
- [ ] Closing meeting condotto
- [ ] Evidence archiviate

### 5.4 Classificazione Finding

| Categoria | Definizione | Esempio |
|-----------|-------------|---------|
| **Non Conformità Maggiore (NCM)** | Assenza o totale inefficacia di un controllo richiesto | Nessun risk assessment eseguito |
| **Non Conformità Minore (NCm)** | Deviazione parziale che non compromette il controllo | Risk assessment incompleto |
| **Osservazione (OBS)** | Opportunità di miglioramento | Processo funzionale ma migliorabile |
| **Best Practice (BP)** | Pratica eccellente da diffondere | Automazione efficace |

### 5.5 Formato Finding

```
FINDING REPORT
--------------
ID: [F-YYYY-NNN]
Classificazione: [NCM/NCm/OBS]
Data rilevamento: {{document_date}}
Auditor: {{contact_name}}

AREA/PROCESSO: [Nome area]

CRITERIO: [Requisito ISO/Policy/Procedura]

EVIDENZA:
[Descrizione oggettiva di cosa è stato osservato]

ANALISI:
[Spiegazione del gap rispetto al criterio]

RISCHIO/IMPATTO:
[Potenziali conseguenze]

RACCOMANDAZIONE:
[Suggerimento per la risoluzione]

RISPOSTA AUDITEE:
[Compilato dall'auditee]
- Root Cause: [Analisi]
- Piano Azione: [Azioni]
- Responsabile: [Nome]
- Scadenza: [Data]
```

---

## 6. Reporting

### 6.1 Report di Audit

**Struttura Report:**

```
AUDIT REPORT
============

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
   4.1 Conformità per area
   4.2 Finding dettagliati
   4.3 Osservazioni
   4.4 Best practice identificate

5. RIEPILOGO FINDING
   | ID | Classificazione | Area | Scadenza |
   |----|-----------------|------|----------|

6. CONCLUSIONI
   - Livello complessivo di conformità
   - Aree di forza
   - Aree di miglioramento

7. PROSSIMI PASSI
   - Remediation plan
   - Follow-up audit
   - Escalation

8. ALLEGATI
   - Evidence
   - Working papers
```

### 6.2 Dashboard Audit

| Metrica | Q1 | Q2 | Q3 | Q4 | YTD |
|---------|----|----|----|----|-----|
| Audit pianificati | | | | | |
| Audit eseguiti | | | | | |
| NCM rilevate | | | | | |
| NCm rilevate | | | | | |
| OBS rilevate | | | | | |
| Finding chiusi | | | | | |
| Finding aperti | | | | | |
| % conformità | | | | | |

### 6.3 Distribuzione Report

| Destinatario | Contenuto | Timing |
|--------------|-----------|--------|
| Direzione | Executive summary | 5gg da chiusura |
| CISO | Report completo | 5gg da chiusura |
| Auditee | Finding area + azioni | 5gg da chiusura |
| Management Review | Sintesi annuale | Pre-review |

---

## 7. Gestione Finding e Remediation

### 7.1 SLA per Risoluzione

| Classificazione | SLA Risposta | SLA Risoluzione |
|-----------------|--------------|-----------------|
| NCM - Critico | 5 giorni | 30 giorni |
| NCM - Alto | 10 giorni | 60 giorni |
| NCm | 15 giorni | 90 giorni |
| OBS | 30 giorni | 180 giorni |

### 7.2 Processo Remediation

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   FINDING    │───►│ ROOT CAUSE   │───►│    PIANO     │
│  Comunicato  │    │   ANALYSIS   │    │   AZIONE     │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│   CHIUSURA   │◄───│  VERIFICA    │◄───│IMPLEMENTAZIONE│
│              │    │   EFFICACIA  │    │              │
└──────────────┘    └──────────────┘    └──────────────┘
```

### 7.3 Tracking Finding

| ID | Classificazione | Area | Owner | Scadenza | Status | Verifica |
|----|-----------------|------|-------|----------|--------|----------|
| F-2024-001 | NCm | Access Control | IT Manager | {{document_date}} | In progress | {{document_date}} |
| F-2024-002 | OBS | HR | HR Manager | {{document_date}} | Closed | {{document_date}} |

### 7.4 Escalation

| Condizione | Escalation To | Azione |
|------------|---------------|--------|
| NCM non risolta entro SLA | CISO + Direzione | Recovery plan |
| NCm non risolta >120gg | CISO | Review priorità |
| Pattern ricorrente | Management Review | Root cause sistemica |
| Rifiuto remediation | Direzione | Risk acceptance |

---

## 8. Audit Specifici

### 8.1 Technical Security Audit

| Area | Frequenza | Metodo | Output |
|------|-----------|--------|--------|
| Vulnerability Assessment | Trimestrale | Scan automatico | Report vulnerabilità |
| Penetration Test | Annuale | Test manuale | Pen test report |
| Configuration Review | Semestrale | Baseline check | Config compliance |
| Code Review | Per release major | SAST/Manual | Security findings |
| Cloud Security | Trimestrale | CSPM | Cloud posture report |

### 8.2 Compliance Audit

| Normativa | Frequenza | Focus |
|-----------|-----------|-------|
| GDPR | Annuale | Data protection controls |
| NIS2 | Semestrale | Security measures Art.21 |
| DORA | Semestrale | ICT risk management |

### 8.3 Surprise Audit

- Frequenza: 2-4 per anno
- Trigger: Random o risk-based
- Focus: Controlli operativi critici
- Notifica: Max 24h prima

---

## 9. Documentazione e Records

### 9.1 Documenti da Mantenere

| Documento | Retention | Ubicazione |
|-----------|-----------|------------|
| Programma audit | Vita ISMS | {{document_management_system}} |
| Piani audit | 5 anni | {{document_management_system}} |
| Report audit | 5 anni | {{document_management_system}} |
| Working papers | 3 anni | {{document_management_system}} |
| Evidence | 3 anni | {{document_management_system}} |
| Tracking finding | 5 anni | {{document_management_system}} |
| Competenze auditor | Vita auditor | HR |

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
| Metodologia | Post-certificazione | CISO |
| Feedback auditee | Post-audit | Lead Auditor |
| Benchmark esterno | Annuale | Audit Manager |

### 10.2 Input per Management Review

- Risultati audit interni del periodo
- Trend finding
- Status remediation
- KPI programma
- Raccomandazioni per miglioramento
- Risorse richieste

---

## 11. Allegati

### Allegato A - Checklist Audit ISO 27001

Vedi documento {{company_name}}-CKL-ISMS-001 — Checklist Audit ISO 27001

### Allegato B - Template Piano Audit

Vedi documento {{company_name}}-TPL-ISMS-001 — Template Piano Audit

### Allegato C - Template Report Audit

Vedi documento {{company_name}}-TPL-ISMS-002 — Template Report Audit

### Allegato D - Competenze Auditor Team

| Nome | Certificazioni | Esperienza | Aree Competenza |
|------|----------------|------------|-----------------|
| {{contact_name}} | ISO 27001 LA, CISA | {{auditor_experience_years}} | {{auditor_competence_areas}} |

### Allegato E - Contatti

| Ruolo | Nome | Email | Telefono |
|-------|------|-------|----------|
| Audit Manager | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| Lead Auditor | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| CISO | {{contact_name}} | {{contact_email}} | {{contact_phone}} |

---

## 12. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 13. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{audit_manager}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Politica di Sicurezza delle Informazioni | {{company_name}}-POL-ISMS-001 | Policy madre ISMS |
| Risk Register | {{company_name}}-REG-ISMS-001 | Risk-based audit planning |
| Statement of Applicability | {{company_name}}-SOA-ISMS-001 | Controlli da auditare |
| Management Review | {{company_name}}-MRV-ISMS-001 | Input audit per riesame direzione |
| Procedura Gestione Incidenti | {{company_name}}-INC-ISMS-001 | Audit incidenti |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{audit_manager}}` | Approvazioni — verificato da | ☐ |
| 6 | `{{contact_name}}` | Allegato D/E — team auditor con certificazioni | ☐ |
| 7 | Piano annuale audit | Sezione 2 — audit pianificati con date e scope | ☐ |
| 8 | Team auditor qualificato | Allegato D — almeno 1 Lead Auditor qualificato | ☐ |
| 9 | `{{document_management_system}}` | Sezione 9 — sistema di gestione documentale | ☐ |
| 10 | Calendario audit approvato | Sezione 3 — calendario annuale approvato dalla Direzione | ☐ |

---

*Template conforme a ISO/IEC 27001:2022 Clausola 9.2*
*Creato con Kynosure.ai*
