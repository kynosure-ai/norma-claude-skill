---
title: Programma Audit Interni PIMS
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: Data Protection Officer
approver: '{{approver_name}}'
framework: 'ISO 27701:2019'
iso_clauses:
  - 9.2 - Internal audit
  - 5.2.1 - Understanding the organization and its context
  - 6.1.2 - Privacy risk assessment
isms_integration:
  - document: Internal Audit Programme ISMS
    path: ../../isms/audit/internal-audit-programme.md
gdpr_articles:
  - Art. 5.2 - Accountability
  - Art. 24 - Responsibility of controller
  - Art. 32 - Security of processing
cross_references:
  - document: PIMS Scope
    path: ../context/pims-scope.md
  - document: Privacy Risk Assessment
    path: ../risk-assessment/privacy-risk-assessment.md
  - document: RoPA
    path: ../registers/record-of-processing-activities.md
related_documents:
  - pims-scope
  - privacy-risk-assessment
  - record-of-processing-activities
  - pims-management-review
  - pims-roles-responsibilities
  - data-breach-notification-procedure
  - privacy-policy
status: draft
review_frequency: annual
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# Programma Audit Interni PIMS

## 1. Introduzione

### 1.1 Scopo

Questo documento definisce il programma di audit interni per il Privacy Information Management System (PIMS) in conformita alla Clausola 9.2 della norma ISO/IEC 27701:2019 e ai principi della ISO 19011:2018 per la conduzione degli audit. L'Organizzazione riconosce l'audit interno come strumento essenziale per verificare sistematicamente che il Sistema di Gestione Privacy sia conforme ai requisiti normativi, sia efficacemente implementato e mantenuto, e contribuisca al raggiungimento degli obiettivi di protezione dei dati personali definiti dalla Direzione.

Il programma di audit si integra coerentemente con il programma di audit del Sistema di Gestione della Sicurezza delle Informazioni (ISMS) secondo ISO 27001, ottimizzando le risorse e garantendo una visione unificata della postura di conformita dell'Organizzazione in materia di sicurezza e privacy. Gli audit verificano l'efficacia dei controlli privacy implementati sia per il ruolo di Controller (Annex A) che per il ruolo di Processor (Annex B), identificano non conformita e aree di miglioramento, supportano il principio di accountability previsto dall'Art. 5.2 del GDPR attraverso la produzione di evidenze documentali oggettive, e preparano l'Organizzazione per audit di terza parte, audit di certificazione e ispezioni dell'Autorita Garante per la Protezione dei Dati Personali.

### 1.3 Ambito

Il programma copre:
- Tutti i processi del PIMS definiti nello scope
- Controlli specifici per Controller (Annex A ISO 27701)
- Controlli specifici per Processor (Annex B ISO 27701)
- Integrazione con audit ISMS (ISO 27001)
- Requisiti GDPR applicabili

---

## 2. Framework Audit PIMS

### 2.1 Integrazione ISMS-PIMS

```
┌──────────────────────────────────────────────────────────────────────┐
│                    FRAMEWORK AUDIT INTEGRATO                         │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌─────────────────────────────────────────────────────────────────┐│
│  │                    AUDIT PROGRAMME                              ││
│  └─────────────────────────────────────────────────────────────────┘│
│                              │                                       │
│         ┌────────────────────┴────────────────────┐                 │
│         ▼                                         ▼                 │
│  ┌──────────────────┐                   ┌──────────────────┐       │
│  │   AUDIT ISMS     │                   │   AUDIT PIMS     │       │
│  │   (ISO 27001)    │                   │   (ISO 27701)    │       │
│  │                  │                   │                  │       │
│  │ • Annex A        │                   │ • Annex A (7.x)  │       │
│  │ • Clausole 4-10  │                   │ • Annex B (8.x)  │       │
│  │ • SOA            │◄─── Integrati ───►│ • Clausole 5-8   │       │
│  └──────────────────┘                   │ • GDPR mapping   │       │
│                                         └──────────────────┘       │
│                              │                                       │
│                              ▼                                       │
│  ┌─────────────────────────────────────────────────────────────────┐│
│  │              AUDIT COMBINATI (ove possibile)                    ││
│  │  • Ottimizzazione risorse                                       ││
│  │  • Visione integrata sicurezza + privacy                        ││
│  │  • Report consolidato                                           ││
│  └─────────────────────────────────────────────────────────────────┘│
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 2.2 Tipologie di Audit PIMS

| Tipo | Frequenza | Ambito | Responsabile |
|------|-----------|--------|--------------|
| **Audit Completo PIMS** | Annuale | Tutti i requisiti ISO 27701 + GDPR | Lead Auditor esterno/interno |
| **Audit Processo** | Semestrale | Singoli processi privacy | Auditor interno |
| **Audit Conformità GDPR** | Annuale | Requisiti GDPR specifici | DPO / Consulente |
| **Audit Fornitori** | Annuale/Contrattuale | Responsabili del trattamento | Privacy Team |
| **Audit Post-Incidente** | Ad hoc | Processo violato | DPO |
| **Audit Pre-Certificazione** | Pre-audit | Gap analysis completa | Consulente esterno |

---

## 3. Pianificazione Annuale

### 3.1 Piano Audit Annuale {{document_year}}

| Q | Mese | Tipo Audit | Ambito | Priorità | Auditor | Stato |
|---|------|------------|--------|----------|---------|-------|
| Q1 | Gen | Audit Processo | Gestione Consensi (7.2.3) | Alta | {{contact_name}} | [ ] Pianificato |
| Q1 | Feb | Audit Processo | DSAR Procedure (7.3.x) | Alta | {{contact_name}} | [ ] Pianificato |
| Q1 | Mar | Audit Fornitori | Top 5 Responsabili | Media | {{contact_name}} | [ ] Pianificato |
| Q2 | Apr | Audit Processo | Data Breach (6.13.1) | Alta | {{contact_name}} | [ ] Pianificato |
| Q2 | Mag | Audit Processo | Transfer Assessment (7.5) | Media | {{contact_name}} | [ ] Pianificato |
| Q2 | Giu | Audit Conformità | GDPR Principles (Art. 5) | Alta | DPO | [ ] Pianificato |
| Q3 | Lug | Audit Processo | Privacy Risk Assessment | Media | {{contact_name}} | [ ] Pianificato |
| Q3 | Ago | - | Pausa estiva | - | - | - |
| Q3 | Set | Audit Processo | RoPA Completezza | Alta | {{contact_name}} | [ ] Pianificato |
| Q4 | Ott | Audit Completo | Full PIMS Audit | Alta | {{contact_name}} | [ ] Pianificato |
| Q4 | Nov | Follow-up | Verifica azioni correttive | Alta | {{contact_name}} | [ ] Pianificato |
| Q4 | Dic | Management Review | Presentazione risultati | - | DPO | [ ] Pianificato |

### 3.2 Criteri di Prioritizzazione

| Fattore | Peso | Criteri Alta Priorità |
|---------|------|----------------------|
| Rischio Privacy | 30% | Trattamenti ad alto rischio (DPIA required) |
| Requisiti Legali | 25% | Obblighi GDPR con sanzioni elevate |
| Incidenti Precedenti | 20% | Aree con NC o breach passati |
| Cambiamenti | 15% | Processi modificati nell'ultimo anno |
| Tempo dall'Ultimo Audit | 10% | > 12 mesi senza verifica |

### 3.3 Risorse Audit

| Risorsa | Disponibilità | Qualifica |
|---------|---------------|-----------|
| Lead Auditor Interno | {{contact_name}} | ISO 27001 LA, formazione privacy |
| Auditor Interno 1 | {{contact_name}} | Formazione audit, conoscenza GDPR |
| Auditor Interno 2 | {{contact_name}} | Formazione audit, conoscenza processi |
| DPO | {{contact_name}} | Observer / Consulted |
| Consulente Esterno | [SOCIETÀ] | ISO 27701 Lead Auditor certificato |

---

## 4. Checklist Audit per Area

### 4.1 Audit Governance Privacy (Clausole 5.2-5.4)

| # | Requisito | Evidenze Richieste | Conforme | NC | Note |
|---|-----------|-------------------|----------|-----|------|
| 5.2.1 | Scope PIMS definito e documentato | Documento scope, confini, applicabilità | [ ] | [ ] | |
| 5.2.2 | Esigenze parti interessate identificate | Registro stakeholder privacy | [ ] | [ ] | |
| 5.2.3 | Requisiti legali determinati | Registro normativo, compliance matrix | [ ] | [ ] | |
| 5.2.4 | Ruolo controller/processor definito | Documentazione ruoli, nomine | [ ] | [ ] | |
| 5.3 | Leadership commitment | Policy firmata, risorse allocate | [ ] | [ ] | |
| 5.4.1 | Ruoli e responsabilità assegnati | Organigramma, job description, RACI | [ ] | [ ] | |
| 5.4.2 | DPO nominato (se richiesto) | Nomina formale, comunicazione Garante | [ ] | [ ] | |

### 4.2 Audit Controlli Controller (Annex A - 7.x)

| # | Controllo | Evidenze Richieste | Conforme | NC | Note |
|---|-----------|-------------------|----------|-----|------|
| **7.2 Condizioni raccolta e trattamento** | | | | | |
| 7.2.1 | Identificazione finalità | RoPA con finalità documentate | [ ] | [ ] | |
| 7.2.2 | Base giuridica identificata | Mapping basi giuridiche per trattamento | [ ] | [ ] | |
| 7.2.3 | Consenso gestito correttamente | Record consensi, form, revoche | [ ] | [ ] | |
| 7.2.4 | PIA/DPIA condotta quando richiesta | DPIA documentate, soglie definite | [ ] | [ ] | |
| 7.2.5 | Contratti con processor | DPA firmati, clausole complete | [ ] | [ ] | |
| 7.2.6 | Joint controller agreement | Accordi congiunti se applicabile | [ ] | [ ] | |
| 7.2.7 | RoPA mantenuto | Registro aggiornato, completo | [ ] | [ ] | |
| 7.2.8 | Privacy by design implementata | Evidenze PbD nei progetti | [ ] | [ ] | |
| **7.3 Obblighi verso interessati** | | | | | |
| 7.3.1 | Obblighi informativa determinati | Informative complete, accessibili | [ ] | [ ] | |
| 7.3.2 | Informativa fornita | Modalità distribuzione, versioning | [ ] | [ ] | |
| 7.3.3 | Meccanismi modifica/revoca consenso | Preference center, canali revoca | [ ] | [ ] | |
| 7.3.4 | Accesso ai dati garantito | Procedura, template risposta | [ ] | [ ] | |
| 7.3.5 | Rettifica implementata | Procedura, SLA | [ ] | [ ] | |
| 7.3.6 | Cancellazione implementata | Procedura, criteri retention | [ ] | [ ] | |
| 7.3.7 | Diritto opposizione gestito | Procedura, template | [ ] | [ ] | |
| 7.3.8 | Portabilità implementata | Formato export, procedura | [ ] | [ ] | |
| 7.3.9 | Decisioni automatizzate gestite | Informativa, intervento umano | [ ] | [ ] | |
| 7.3.10 | Comunicazioni terzi | Notifica rettifica/cancellazione | [ ] | [ ] | |
| **7.4 Privacy by Design/Default** | | | | | |
| 7.4.1 | Limitazione raccolta | Minimizzazione implementata | [ ] | [ ] | |
| 7.4.2 | Limitazione trattamento | Solo finalità dichiarate | [ ] | [ ] | |
| 7.4.3 | Accuratezza dati | Processi aggiornamento | [ ] | [ ] | |
| 7.4.4 | Minimizzazione dati | Review periodica necessità | [ ] | [ ] | |
| 7.4.5 | De-identificazione | Pseudonimizzazione, anonimizzazione | [ ] | [ ] | |
| 7.4.6 | Cancellazione temporanea | Soft delete implementato | [ ] | [ ] | |
| 7.4.7 | Cancellazione definitiva | Procedura cancellazione sicura | [ ] | [ ] | |
| 7.4.8 | Retention policy | Policy documentata, automatizzata | [ ] | [ ] | |
| 7.4.9 | Controlli trasmissione | Cifratura, canali sicuri | [ ] | [ ] | |
| **7.5 Condivisione e trasferimenti** | | | | | |
| 7.5.1 | Paesi terzi identificati | Mappatura trasferimenti | [ ] | [ ] | |
| 7.5.2 | Base trasferimento documentata | TIA, SCC, BCR | [ ] | [ ] | |
| 7.5.3 | Terzi destinatari documentati | Lista destinatari, finalità | [ ] | [ ] | |
| 7.5.4 | Record trasferimenti | Log, audit trail | [ ] | [ ] | |

### 4.3 Audit Controlli Processor (Annex B - 8.x)

| # | Controllo | Evidenze Richieste | Conforme | NC | Note |
|---|-----------|-------------------|----------|-----|------|
| **8.2 Condizioni trattamento** | | | | | |
| 8.2.1 | Contratto/istruzioni documentate | DPA ricevuto, istruzioni scritte | [ ] | [ ] | |
| 8.2.2 | Finalità limitate | No trattamento oltre istruzioni | [ ] | [ ] | |
| 8.2.3 | Marketing limitato | No uso dati per marketing proprio | [ ] | [ ] | |
| 8.2.4 | Istruzioni contrastanti segnalate | Procedura escalation | [ ] | [ ] | |
| 8.2.5 | Obbligo riservatezza | Accordi con personale | [ ] | [ ] | |
| 8.2.6 | Sub-processor autorizzati | Lista sub-processor, consenso | [ ] | [ ] | |
| **8.3 Obblighi verso controller** | | | | | |
| 8.3.1 | Notifica trasferimenti | Comunicazione al controller | [ ] | [ ] | |
| 8.4.1 | Assistenza DSAR | Processo supporto controller | [ ] | [ ] | |
| 8.4.2 | Assistenza breach | Notifica tempestiva | [ ] | [ ] | |
| 8.4.3 | Assistenza DPIA | Supporto documentato | [ ] | [ ] | |
| **8.5 Restituzione/cancellazione** | | | | | |
| 8.5.1 | Cancellazione a fine contratto | Procedura, certificazione | [ ] | [ ] | |
| 8.5.2 | Restituzione dati | Formato, modalità | [ ] | [ ] | |

### 4.4 Audit Conformità GDPR

| Art. | Requisito | Evidenze | Conforme | NC | Note |
|------|-----------|----------|----------|-----|------|
| 5.1.a | Liceità, correttezza, trasparenza | Basi giuridiche, informative | [ ] | [ ] | |
| 5.1.b | Limitazione finalità | RoPA, no secondary use | [ ] | [ ] | |
| 5.1.c | Minimizzazione | Data inventory, review | [ ] | [ ] | |
| 5.1.d | Esattezza | Processi aggiornamento | [ ] | [ ] | |
| 5.1.e | Limitazione conservazione | Retention policy, automazione | [ ] | [ ] | |
| 5.1.f | Integrità e riservatezza | Misure tecniche, SOA | [ ] | [ ] | |
| 5.2 | Accountability | Documentazione completa | [ ] | [ ] | |
| 6 | Basi giuridiche | Mapping completo | [ ] | [ ] | |
| 7 | Consenso valido | Form, record, revoche | [ ] | [ ] | |
| 12-22 | Diritti interessati | Procedure, SLA, template | [ ] | [ ] | |
| 24 | Responsabilità titolare | Misure tecniche e organizzative | [ ] | [ ] | |
| 25 | Privacy by design/default | Evidenze implementazione | [ ] | [ ] | |
| 28 | Contratti processor | DPA completi | [ ] | [ ] | |
| 30 | RoPA | Registro completo | [ ] | [ ] | |
| 32 | Sicurezza trattamento | Misure adeguate al rischio | [ ] | [ ] | |
| 33-34 | Notifica breach | Procedura, test, log | [ ] | [ ] | |
| 35 | DPIA | Processo, soglie, documentazione | [ ] | [ ] | |
| 37-39 | DPO | Nomina, indipendenza, risorse | [ ] | [ ] | |
| 44-49 | Trasferimenti | TIA, SCC, garanzie | [ ] | [ ] | |

---

## 5. Processo di Audit

### 5.1 Fasi dell'Audit

```
┌──────────────────────────────────────────────────────────────────────┐
│                      PROCESSO AUDIT PIMS                             │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  FASE 1: PIANIFICAZIONE                                              │
│  ├─→ Definizione ambito e obiettivi                                 │
│  ├─→ Selezione team audit                                           │
│  ├─→ Preparazione checklist                                         │
│  ├─→ Comunicazione agli auditati                                    │
│  └─→ Raccolta documentazione preliminare                            │
│                              │                                       │
│                              ▼                                       │
│  FASE 2: ESECUZIONE                                                  │
│  ├─→ Opening meeting                                                │
│  ├─→ Raccolta evidenze (documenti, interviste, osservazione)       │
│  ├─→ Verifica controlli                                             │
│  ├─→ Identificazione findings                                       │
│  └─→ Closing meeting preliminare                                    │
│                              │                                       │
│                              ▼                                       │
│  FASE 3: REPORTING                                                   │
│  ├─→ Classificazione findings (NC maggiore/minore, osservazione)   │
│  ├─→ Stesura report                                                 │
│  ├─→ Review con auditato                                            │
│  └─→ Emissione report finale                                        │
│                              │                                       │
│                              ▼                                       │
│  FASE 4: FOLLOW-UP                                                   │
│  ├─→ Definizione azioni correttive                                  │
│  ├─→ Assegnazione responsabilità e scadenze                        │
│  ├─→ Monitoraggio implementazione                                   │
│  └─→ Verifica efficacia                                             │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

### 5.2 Timeline Standard Audit

| Fase | Attività | Durata | Responsabile |
|------|----------|--------|--------------|
| T-4 settimane | Piano audit approvato | 1 giorno | Lead Auditor |
| T-2 settimane | Notifica agli auditati | 1 giorno | Lead Auditor |
| T-1 settimana | Raccolta documentazione | 3 giorni | Auditati |
| T-3 giorni | Review documentazione | 2 giorni | Team Audit |
| Giorno 1 | Opening meeting | 1 ora | Team Audit + Auditati |
| Giorni 1-N | Esecuzione audit | Variabile | Team Audit |
| Ultimo giorno | Closing meeting | 1 ora | Team Audit + Auditati |
| T+1 settimana | Draft report | 3 giorni | Lead Auditor |
| T+2 settimane | Report finale | 2 giorni | Lead Auditor |
| T+4 settimane | Piano azioni correttive | - | Auditati |

---

## 6. Classificazione Findings

### 6.1 Categorie

| Categoria | Definizione | Azione Richiesta | Timeline |
|-----------|-------------|------------------|----------|
| **NC Maggiore** | Mancanza totale o grave inadeguatezza di un requisito; rischio elevato per i diritti degli interessati | Azione correttiva immediata, root cause analysis | 30 giorni |
| **NC Minore** | Parziale inadempimento di un requisito; rischio limitato | Azione correttiva pianificata | 90 giorni |
| **Osservazione** | Area di miglioramento; non ancora non conformità | Considerare per miglioramento | Prossimo ciclo |
| **Best Practice** | Eccellenza identificata | Condividere come esempio | - |

### 6.2 Esempi di Classificazione PIMS

| Esempio Finding | Classificazione | Motivazione |
|----------------|-----------------|-------------|
| RoPA non esistente | NC Maggiore | Obbligo legale Art. 30 |
| RoPA incompleto (mancano 2 campi) | NC Minore | Parziale adempimento |
| RoPA non aggiornato da 8 mesi | Osservazione | Rischio obsolescenza |
| Consensi senza timestamp | NC Maggiore | Prova non valida |
| DPIA non effettuata per trattamento alto rischio | NC Maggiore | Art. 35 violato |
| DPIA senza consultazione DPO | NC Minore | Processo incompleto |
| Informativa difficile da trovare sul sito | Osservazione | Trasparenza migliorabile |
| Breach procedure testata trimestralmente | Best Practice | Oltre requisito minimo |

---

## 7. Template Audit Report

### 7.1 Struttura Report

```
═══════════════════════════════════════════════════════════════════════
                    AUDIT REPORT - PIMS
                    [TITOLO AUDIT]
═══════════════════════════════════════════════════════════════════════

INFORMAZIONI AUDIT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Riferimento:        [AUDIT-PIMS-ANNO-NNN]
Data esecuzione:    {{document_date}}
Ambito:             [DESCRIZIONE AMBITO]
Standard riferimento: ISO 27701:2019, GDPR

TEAM AUDIT
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Lead Auditor:       {{contact_name}}
Auditor:            {{contact_name}}
Observer:           {{contact_name}} (DPO)

SOMMARIO ESECUTIVO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Sintesi risultati, conclusione generale]

STATISTICHE FINDINGS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
NC Maggiori:        [N]
NC Minori:          [N]
Osservazioni:       [N]
Best Practices:     [N]

DETTAGLIO FINDINGS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

FINDING #1
────────────────────────────────────────────────────────────────────
Riferimento:    [F-001]
Classificazione: [NC Maggiore/Minore/Osservazione]
Requisito:      [Clausola ISO 27701 / Art. GDPR]
Descrizione:    [Descrizione della non conformità]
Evidenza:       [Evidenza oggettiva raccolta]
Rischio:        [Impatto potenziale]
Raccomandazione: [Azione suggerita]

[Ripetere per ogni finding]

CONCLUSIONI E RACCOMANDAZIONI
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[Valutazione complessiva, priorità, prossimi passi]

FIRME
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Lead Auditor:       _________________ Data: _________
Responsabile Area:  _________________ Data: _________
DPO (per presa visione): _________________ Data: _________
```

---

## 8. Gestione Azioni Correttive

### 8.1 Template Piano Azioni Correttive

| Finding | Azione Correttiva | Responsabile | Scadenza | Stato | Verifica |
|---------|-------------------|--------------|----------|-------|----------|
| F-001 | [Descrizione azione] | [Nome] | [Data] | [ ] Aperta | [Data verifica] |
| F-002 | [Descrizione azione] | [Nome] | [Data] | [ ] Aperta | [Data verifica] |

### 8.2 Processo Follow-up

```
┌──────────────────────────────────────────────────────────────────────┐
│                    PROCESSO FOLLOW-UP                                │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Finding Identificato                                                │
│         │                                                            │
│         ▼                                                            │
│  ┌─────────────────────────────────────────────────────┐            │
│  │  ROOT CAUSE ANALYSIS                                │            │
│  │  • 5 Whys                                          │            │
│  │  • Fishbone diagram                                │            │
│  │  • Identificazione causa radice                    │            │
│  └──────────────────────────┬──────────────────────────┘            │
│                              │                                       │
│                              ▼                                       │
│  ┌─────────────────────────────────────────────────────┐            │
│  │  DEFINIZIONE AZIONE CORRETTIVA                      │            │
│  │  • Azione immediata (contenimento)                 │            │
│  │  • Azione correttiva (eliminare causa)             │            │
│  │  • Azione preventiva (evitare ricorrenza)          │            │
│  └──────────────────────────┬──────────────────────────┘            │
│                              │                                       │
│                              ▼                                       │
│  ┌─────────────────────────────────────────────────────┐            │
│  │  IMPLEMENTAZIONE                                    │            │
│  │  • Responsabile assegnato                          │            │
│  │  • Risorse allocate                                │            │
│  │  • Timeline definita                               │            │
│  └──────────────────────────┬──────────────────────────┘            │
│                              │                                       │
│                              ▼                                       │
│  ┌─────────────────────────────────────────────────────┐            │
│  │  VERIFICA EFFICACIA                                 │            │
│  │  • Evidenza implementazione                        │            │
│  │  • Test efficacia                                  │            │
│  │  • Chiusura finding                                │            │
│  └─────────────────────────────────────────────────────┘            │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## 9. Audit Fornitori (Processor)

### 9.1 Criteri Selezione Fornitori da Auditare

| Criterio | Peso | Punteggio (1-5) | Note |
|----------|------|-----------------|------|
| Volume dati trattati | 25% | | |
| Categorie dati (particolari) | 25% | | |
| Criticità per il business | 20% | | |
| Storico incidenti | 15% | | |
| Ultimo audit | 15% | | |
| **TOTALE PONDERATO** | 100% | | |

**Soglia audit obbligatorio**: Score > 3.5

### 9.2 Checklist Audit Processor

| # | Area | Verifica | Conforme | NC | Note |
|---|------|----------|----------|-----|------|
| 1 | **Contrattuale** | | | | |
| 1.1 | DPA firmato | [ ] Sì [ ] No | [ ] | [ ] | |
| 1.2 | Clausole Art. 28 complete | [ ] Sì [ ] No | [ ] | [ ] | |
| 1.3 | Sub-processor autorizzati | [ ] Sì [ ] No | [ ] | [ ] | |
| 2 | **Organizzativo** | | | | |
| 2.1 | Referente privacy nominato | [ ] Sì [ ] No | [ ] | [ ] | |
| 2.2 | Personale formato | [ ] Sì [ ] No | [ ] | [ ] | |
| 2.3 | Policy privacy esistente | [ ] Sì [ ] No | [ ] | [ ] | |
| 3 | **Tecnico** | | | | |
| 3.1 | Misure sicurezza adeguate | [ ] Sì [ ] No | [ ] | [ ] | |
| 3.2 | Cifratura dati | [ ] Sì [ ] No | [ ] | [ ] | |
| 3.3 | Controllo accessi | [ ] Sì [ ] No | [ ] | [ ] | |
| 3.4 | Log e audit trail | [ ] Sì [ ] No | [ ] | [ ] | |
| 4 | **Incidenti** | | | | |
| 4.1 | Procedura breach | [ ] Sì [ ] No | [ ] | [ ] | |
| 4.2 | SLA notifica | [ ] Sì [ ] No | [ ] | [ ] | |
| 5 | **Trasferimenti** | | | | |
| 5.1 | Paesi terzi identificati | [ ] Sì [ ] No | [ ] | [ ] | |
| 5.2 | Garanzie implementate | [ ] Sì [ ] No | [ ] | [ ] | |

---

## 10. KPI e Metriche

### 10.1 KPI Programma Audit

| KPI | Formula | Target | Frequenza |
|-----|---------|--------|-----------|
| Completamento piano | Audit eseguiti / Audit pianificati × 100 | 100% | Annuale |
| Tempestività report | Report emessi entro SLA / Totale audit × 100 | 95% | Trimestrale |
| Tasso NC maggiori | NC maggiori / Totale findings × 100 | < 10% | Annuale |
| Chiusura azioni | Azioni chiuse in tempo / Totale azioni × 100 | > 90% | Trimestrale |
| Efficacia azioni | Azioni efficaci / Azioni verificate × 100 | > 95% | Semestrale |
| Recidiva | NC ricorrenti / Totale NC × 100 | < 5% | Annuale |
| Copertura PIMS | Requisiti auditati / Totale requisiti × 100 | 100% (3 anni) | Annuale |

### 10.2 Dashboard Audit PIMS

```
┌──────────────────────────────────────────────────────────────────────┐
│                    DASHBOARD AUDIT PIMS {{document_year}}                       │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  STATO PIANO AUDIT                    FINDINGS PER CATEGORIA         │
│  ┌────────────────────────┐           ┌────────────────────────┐    │
│  │ ████████████░░░░ 75%  │           │ NC Maggiori    ██ 3    │    │
│  │ 9/12 audit completati │           │ NC Minori   █████ 12   │    │
│  └────────────────────────┘           │ Osservazioni ███ 8     │    │
│                                       └────────────────────────┘    │
│                                                                      │
│  TREND NC (ultimi 3 anni)             AZIONI CORRETTIVE             │
│  ┌────────────────────────┐           ┌────────────────────────┐    │
│  │ 2022: ████████ 18     │           │ Aperte:     ████ 8     │    │
│  │ 2023: █████ 12        │           │ In corso:   ██ 4       │    │
│  │ 2024: ███ 7           │           │ Chiuse:     ███████ 15 │    │
│  │ ↓ Trend positivo      │           │ Scadute:    █ 2        │    │
│  └────────────────────────┘           └────────────────────────┘    │
│                                                                      │
│  TOP 5 AREE CON NC                                                   │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │ 1. Gestione consensi (7.2.3)           ████████ 4 NC        │   │
│  │ 2. RoPA completezza (7.2.7)            ██████ 3 NC          │   │
│  │ 3. Retention policy (7.4.8)            ████ 2 NC            │   │
│  │ 4. Contratti processor (7.2.5)         ████ 2 NC            │   │
│  │ 5. Informativa trasparenza (7.3.2)     ██ 1 NC              │   │
│  └──────────────────────────────────────────────────────────────┘   │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## 11. Competenze Auditor PIMS

### 11.1 Requisiti Auditor Interno

| Competenza | Requisito Minimo | Verificato |
|------------|------------------|------------|
| Formazione audit | Corso ISO 19011 o equivalente | [ ] |
| Conoscenza ISO 27701 | Corso specifico o autoformazione verificata | [ ] |
| Conoscenza GDPR | Formazione documentata | [ ] |
| Esperienza audit | Almeno 2 audit come osservatore | [ ] |
| Indipendenza | Non auditare propria area | [ ] |
| Aggiornamento | Formazione continua annuale | [ ] |

### 11.2 Piano Formazione Auditor

| Argomento | Modalità | Durata | Frequenza |
|-----------|----------|--------|-----------|
| ISO 27701 fundamentals | E-learning / Aula | 8 ore | Una tantum |
| GDPR avanzato | E-learning | 4 ore | Annuale |
| Tecniche di audit | Workshop | 8 ore | Biennale |
| Aggiornamenti normativi | Webinar | 2 ore | Semestrale |
| Case study PIMS | Workshop | 4 ore | Annuale |

---

## 12. Responsabilità

### 12.1 RACI Audit PIMS

| Attività | DPO | Lead Auditor | Auditor | Auditato | Management |
|----------|-----|--------------|---------|----------|------------|
| Approvazione piano annuale | R | C | I | I | A |
| Pianificazione singolo audit | C | R | I | I | I |
| Esecuzione audit | I | A | R | C | I |
| Stesura report | C | A | R | I | I |
| Approvazione report | A | R | C | C | I |
| Definizione azioni correttive | C | I | I | R | A |
| Verifica chiusura NC | A | R | R | C | I |
| Reporting a management | R | C | I | I | A |

---

## 13. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## Appendice A: Calendario Audit Triennale

| Area PIMS | Anno 1 | Anno 2 | Anno 3 |
|-----------|--------|--------|--------|
| 5.2-5.4 Governance | ✓ | | ✓ |
| 7.2 Condizioni trattamento | ✓ | ✓ | ✓ |
| 7.3 Diritti interessati | ✓ | ✓ | ✓ |
| 7.4 Privacy by Design | ✓ | | ✓ |
| 7.5 Trasferimenti | ✓ | ✓ | ✓ |
| 8.x Controlli processor | | ✓ | ✓ |
| Fornitori critici | ✓ | ✓ | ✓ |
| Full GDPR compliance | ✓ | | ✓ |

---

## Documenti Correlati

| Documento | Riferimento | Relazione |
|-----------|-------------|-----------|
| PIMS Scope | `../context/pims-scope.md` | Perimetro da auditare |
| Privacy Risk Assessment | `../risk-assessment/privacy-risk-assessment.md` | Prioritizzazione aree da auditare in base al rischio |
| RoPA | `../registers/record-of-processing-activities.md` | Trattamenti da verificare in audit |
| PIMS Management Review | `./pims-management-review.md` | Destinazione risultati audit |
| PIMS Roles & Responsibilities | `../context/pims-roles-responsibilities.md` | Responsabilità audit e indipendenza |
| Data Breach Notification | `../procedures/data-breach-notification-procedure.md` | Verifica procedura breach in audit |
| Privacy Policy | `../policies/privacy-policy.md` | Conformità policy da verificare |
| DPIA Template | `../dpia/dpia-template.md` | Verifica completamento DPIA per trattamenti ad alto rischio |

---

## Checklist di Compilazione

Prima di considerare questo programma di audit completo, verificare di aver compilato:

- [ ] {{document_date}} — Data emissione documento
- [ ] {{document_author}} — Autore del documento
- [ ] {{approver_name}} — Nome approvatore
- [ ] {{last_review_date}} / {{next_review_date}} — Date revisione
- [ ] Sezione 2 — Piano audit annuale con almeno 2 audit interni/anno per aree ad alto rischio
- [ ] Sezione 3-5 — Checklist audit per ogni clausola ISO 27701 applicabile (Cl. 7 Controller / Cl. 8 Processor)
- [ ] Sezione 7 — Processo follow-up con root cause analysis e verifica efficacia
- [ ] Sezione 9 — Criteri selezione processor da auditare con soglia score > 3.5
- [ ] Sezione 10 — KPI programma audit con target definiti
- [ ] Sezione 11 — Requisiti competenze auditor PIMS (ISO 19011 + ISO 27701 + GDPR)
- [ ] Appendice A — Calendario audit triennale con copertura completa
- [ ] Tabella RACI — Responsabilità complete per ogni attività audit

---

*Documento conforme a ISO 27701:2019 Clausola 9.2 e ISO 19011:2018*
