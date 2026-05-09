---
title: Metodologia di Valutazione del Rischio
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{security_officer_title}}'
approver: '{{senior_management}}'
framework: ISO27001
language: IT
documentType: procedure
iso_controls:
  - Clausola 6.1.2 - Valutazione del rischio
  - Clausola 8.2 - Valutazione del rischio sicurezza informazioni
  - A.5.7 - Threat intelligence
cross_references:
  - 'ISO 31000:2018 - Risk management'
  - NIS2 Art. 21(2)(a) - Politiche analisi rischi
  - DORA Art. 6 - Quadro gestione rischi ICT
  - GDPR Art. 32 - Sicurezza del trattamento
status: Da approvare
subset: true
---

# Metodologia di Valutazione del Rischio per la Sicurezza delle Informazioni

## 1. Informazioni Documento

| Campo | Valore |
|-------|--------|
| **Codice Documento** | {{company_name}}-MET-ISMS-001 |
| **Versione** | 1.0 |
| **Data Emissione** | {{document_date}} |
| **Data Prossima Revisione** | [GG/MM/AAAA + 1 anno] |
| **Classificazione** | Interno |
| **Proprietario** | [Responsabile Sicurezza Informazioni] |
| **Approvato da** | [Direzione Generale] |
| **Stato** | [Bozza / In Revisione / Approvato] |

### Storico Revisioni

| Ver. | Data | Autore | Modifiche |
|------|------|--------|-----------|
| 1.0 | {{document_date}} | {{contact_name}} | Prima emissione |
| | | | |

---

## 2. Scopo

{{company_name}} riconosce che la gestione efficace del rischio costituisce il fondamento su cui si costruisce l'intero Sistema di Gestione per la Sicurezza delle Informazioni. La capacità di identificare, analizzare, valutare e trattare i rischi in modo sistematico permette all'Organizzazione di allocare le risorse in modo ottimale, concentrando gli investimenti di sicurezza dove possono generare il massimo beneficio in termini di riduzione dell'esposizione al rischio.

Il presente documento definisce la metodologia adottata dall'Organizzazione per la gestione del rischio, stabilendo criteri oggettivi e scale di valutazione che garantiscono risultati comparabili e coerenti nel tempo. L'approccio metodologico assicura la ripetibilità delle valutazioni e la tracciabilità delle decisioni, permettendo alla Direzione di prendere decisioni informate basate su evidenze quantitative e qualitative. La metodologia risulta conforme ai requisiti della norma ISO/IEC 27001:2022, alle linee guida ISO 31000 per la gestione del rischio e ai requisiti specifici della Direttiva NIS2, del Regolamento DORA e del GDPR in materia di analisi e trattamento dei rischi.

---

## 3. Ambito di Applicazione

Questa metodologia si applica a:
- Tutti gli asset informativi inclusi nel perimetro ISMS
- Tutti i processi di business che trattano informazioni
- Tutti i sistemi e le infrastrutture IT
- Le relazioni con terze parti (fornitori, partner)
- I nuovi progetti e le modifiche significative

---

## 4. Riferimenti Normativi

| Standard | Descrizione |
|----------|-------------|
| ISO/IEC 27001:2022 | Clausole 6.1.2, 6.1.3, 8.2, 8.3 |
| ISO/IEC 27005:2022 | Gestione del rischio sicurezza informazioni |
| ISO 31000:2018 | Risk management - Linee guida |
| NIST SP 800-30 | Guide for Conducting Risk Assessments |

---

## 5. Termini e Definizioni

| Termine | Definizione |
|---------|-------------|
| **Rischio** | Effetto dell'incertezza sugli obiettivi, espresso come combinazione di probabilità e impatto |
| **Asset** | Qualsiasi elemento che abbia valore per l'Organizzazione |
| **Minaccia** | Causa potenziale di un incidente indesiderato |
| **Vulnerabilità** | Debolezza che può essere sfruttata da una minaccia |
| **Impatto** | Conseguenza di un evento sulla riservatezza, integrità o disponibilità |
| **Probabilità** | Possibilità che un evento si verifichi |
| **Controllo** | Misura che modifica il rischio |
| **Rischio Inerente** | Rischio in assenza di controlli |
| **Rischio Residuo** | Rischio rimanente dopo l'applicazione dei controlli |
| **Propensione al Rischio** | Livello di rischio che l'Organizzazione è disposta ad accettare |

---

## 6. Ruoli e Responsabilità

| Ruolo | Responsabilità nella Gestione del Rischio |
|-------|------------------------------------------|
| **Direzione** | Approvare metodologia, definire propensione al rischio, allocare risorse |
| **Risk Owner** | Responsabile del rischio, autorizza trattamento e accettazione |
| **CISO** | Coordinare processo, mantenere registro, reporting |
| **Asset Owner** | Identificare asset, partecipare a valutazione, implementare controlli |
| **IT Security** | Supporto tecnico, identificazione vulnerabilità, implementazione controlli |
| **Process Owner** | Identificare rischi di processo, implementare controlli operativi |

---

## 7. Processo di Risk Management

### 7.1 Overview del Processo

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    PROCESSO DI RISK MANAGEMENT                           │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌───────────┐ │
│  │  CONTESTO   │───►│IDENTIFICAZ. │───►│   ANALISI   │───►│VALUTAZIONE│ │
│  │             │    │   RISCHI    │    │   RISCHI    │    │  RISCHI   │ │
│  └─────────────┘    └─────────────┘    └─────────────┘    └─────┬─────┘ │
│                                                                   │      │
│                                                                   ▼      │
│  ┌─────────────┐    ┌─────────────┐                        ┌───────────┐ │
│  │ MONITORAGGIO│◄───│COMUNICAZIONE│◄───────────────────────│TRATTAMENTO│ │
│  │  & REVIEW   │    │ & REPORTING │                        │  RISCHI   │ │
│  └─────────────┘    └─────────────┘                        └───────────┘ │
└─────────────────────────────────────────────────────────────────────────┘
```

### 7.2 Frequenza delle Attività

| Attività | Frequenza | Trigger Aggiuntivi |
|----------|-----------|-------------------|
| Risk Assessment completo | Annuale | - |
| Review registro rischi | Trimestrale | - |
| Valutazione nuovi asset/progetti | Ad evento | Nuovi sistemi, cambiamenti significativi |
| Rivalutazione dopo incidente | Ad evento | Incidenti di sicurezza |
| Update threat landscape | Semestrale | Nuove minacce rilevanti |

---

## 8. Identificazione dei Rischi

### 8.1 Identificazione Asset

#### Categorie di Asset

| Categoria | Esempi | Attributi da Documentare |
|-----------|--------|--------------------------|
| **Informazioni** | Database clienti, documentazione tecnica, segreti commerciali | Classificazione, formato, ubicazione |
| **Software** | Applicazioni business, sistemi operativi, strumenti | Versione, licenza, criticità |
| **Hardware** | Server, endpoint, apparati rete | Ubicazione, configurazione |
| **Servizi** | Cloud, hosting, SaaS | Provider, SLA, dipendenze |
| **Persone** | Competenze chiave, ruoli critici | Backup, knowledge transfer |
| **Intangibili** | Reputazione, brand, relazioni | Valore stimato |

### 8.2 Catalogo Minacce

| ID | Categoria | Minaccia | Fonte | Trend |
|----|-----------|----------|-------|-------|
| T01 | Cyber | Ransomware | Esterna | ↑ |
| T02 | Cyber | Phishing | Esterna | ↑ |
| T03 | Cyber | APT/Targeted attack | Esterna | → |
| T04 | Cyber | DDoS | Esterna | → |
| T05 | Cyber | Malware generico | Esterna | → |
| T06 | Cyber | Insider threat - malevolo | Interna | → |
| T07 | Cyber | Insider threat - errore | Interna | → |
| T08 | Cyber | Supply chain attack | Esterna | ↑ |
| T09 | Fisica | Furto apparecchiature | Esterna | → |
| T10 | Fisica | Accesso non autorizzato | Esterna/Interna | → |
| T11 | Ambientale | Incendio | Naturale | → |
| T12 | Ambientale | Allagamento | Naturale | → |
| T13 | Ambientale | Interruzione energia | Infrastruttura | → |
| T14 | Tecnica | Guasto hardware | Tecnica | → |
| T15 | Tecnica | Bug software | Tecnica | → |
| T16 | Tecnica | Errore configurazione | Umana | → |
| T17 | Compliance | Violazione normativa | Interna | → |
| T18 | Business | Indisponibilità fornitore critico | Esterna | → |

**Legenda Trend**: ↑ In aumento, → Stabile, ↓ In diminuzione

### 8.3 Identificazione Vulnerabilità

| Fonte | Frequenza | Output |
|-------|-----------|--------|
| Vulnerability scan | Mensile | Report vulnerabilità tecniche |
| Penetration test | Annuale | Report e remediation plan |
| Audit interni | Annuale | Finding e NC |
| Gap analysis | Ad hoc | Gap rispetto a standard/best practice |
| Incident analysis | Per evento | Root cause, vulnerabilità sfruttate |
| Threat intelligence | Continuo | Nuove vulnerabilità note |

---

## 9. Analisi dei Rischi

### 9.1 Scala di Impatto (1-5)

| Livello | Valore | Riservatezza | Integrità | Disponibilità |
|---------|--------|--------------|-----------|---------------|
| **Trascurabile** | 1 | Dati pubblici | Errori minori, correggibili | < 1 ora, nessun impatto |
| **Basso** | 2 | Dati interni, no PII | Correggibile senza perdita | 1-4 ore, impatto limitato |
| **Medio** | 3 | PII limitati (< 100) | Perdita parziale, ripristino possibile | 4-24 ore, impatto moderato |
| **Alto** | 4 | Dati sensibili, breach significativo | Perdita rilevante, ripristino complesso | 1-7 giorni, impatto significativo |
| **Critico** | 5 | Breach massivo, dati Art.9 | Perdita irreversibile | > 7 giorni, minaccia sopravvivenza |

### 9.2 Scala di Probabilità (1-5)

| Livello | Valore | Descrizione | Frequenza Indicativa |
|---------|--------|-------------|---------------------|
| **Molto Bassa** | 1 | Evento raro, mai accaduto | < 1 volta ogni 10 anni |
| **Bassa** | 2 | Possibile ma improbabile | 1 volta ogni 5-10 anni |
| **Media** | 3 | Occasionale, già nel settore | 1 volta ogni 1-5 anni |
| **Alta** | 4 | Probabile, già in organizzazione | 1-10 volte all'anno |
| **Molto Alta** | 5 | Frequente o quasi certo | > 10 volte all'anno |

### 9.3 Matrice di Rischio 5x5

```
                              IMPATTO
              │   1      2       3       4       5
              │ Trasc.  Basso  Medio   Alto  Critico
──────────────┼─────────────────────────────────────
      5 Molto │   5      10     15      20     25
        Alta  │   ◐      ●      ●       ●      ●
──────────────┼─────────────────────────────────────
P     4 Alta  │   4       8     12      16     20
R            │   ◐      ◐      ●       ●      ●
O  ───────────┼─────────────────────────────────────
B     3 Media │   3       6      9      12     15
A            │   ○      ◐      ◐       ●      ●
B  ───────────┼─────────────────────────────────────
I     2 Bassa │   2       4      6       8     10
L            │   ○      ○      ◐       ◐      ◐
I  ───────────┼─────────────────────────────────────
T     1 Molto │   1       2      3       4      5
À      Bassa  │   ○      ○      ○       ○      ◐
──────────────┴─────────────────────────────────────

LEGENDA:
○ Basso (1-4)     - Accettabile, solo monitoraggio
◐ Medio (5-9)     - Accettabile con piano, trattamento consigliato
● Alto (10-14)    - Non accettabile, trattamento richiesto entro 90gg
● Critico (15-25) - Non accettabile, trattamento immediato
```

### 9.4 Valutazione Controlli Esistenti

| Livello Efficacia | Descrizione | Riduzione Rischio |
|-------------------|-------------|-------------------|
| **Nessuno** | Controllo assente | 0% |
| **Bassa** | Controllo parziale o non verificato | 10-25% |
| **Media** | Controllo implementato ma migliorabile | 25-50% |
| **Alta** | Controllo robusto e verificato | 50-75% |
| **Molto Alta** | Controllo best-in-class, testato | 75-90% |

---

## 10. Criteri di Accettazione del Rischio

La Direzione ha definito i seguenti criteri:

| Livello Rischio | Valore | Accettabilità | Azione Richiesta | Approvazione |
|-----------------|--------|---------------|------------------|--------------|
| **Critico** | 15-25 | Non accettabile | Trattamento immediato | Direzione |
| **Alto** | 10-14 | Non accettabile | Trattamento entro 30 giorni | CISO + Risk Owner |
| **Medio** | 5-9 | Condizionato | Piano trattamento entro 90 giorni | Risk Owner |
| **Basso** | 1-4 | Accettabile | Monitoraggio, trattamento opzionale | Risk Owner |

### Risk Appetite Statement

> {{company_name}} accetta un livello di rischio residuo non superiore a {{risk_appetite_threshold}} per i singoli rischi.
>
> Rischi legati a compliance normativa (GDPR, NIS2) devono essere trattati indipendentemente dal valore numerico.

---

## 11. Trattamento dei Rischi

### 11.1 Opzioni di Trattamento

| Opzione | Descrizione | Quando Applicare |
|---------|-------------|------------------|
| **Mitigare** | Implementare controlli per ridurre probabilità e/o impatto | Rischio riducibile con costo ragionevole |
| **Trasferire** | Trasferire a terzi (assicurazione, outsourcing) | Rischio non gestibile internamente |
| **Evitare** | Eliminare attività/asset che genera il rischio | Rischio non accettabile, trattamento non fattibile |
| **Accettare** | Accettare consapevolmente il rischio residuo | Rischio sotto soglia, trattamento non cost-effective |

### 11.2 Selezione Controlli

I controlli sono selezionati da:
- ISO 27001:2022 Annex A (93 controlli)
- Best practice di settore
- Requisiti normativi specifici

### 11.3 Piano di Trattamento del Rischio

Vedi documento separato: **Risk Treatment Plan** ({{company_name}}-REG-ISMS-002)

---

## 12. Monitoraggio e Revisione

### 12.1 Key Risk Indicators (KRI)

| KRI | Descrizione | Soglia Alert | Fonte Dati |
|-----|-------------|--------------|------------|
| N. vulnerabilità critiche aperte | Vulnerabilità non rimediate | > 0 oltre SLA | Vulnerability scanner |
| Tempo medio patch critiche | MTTR per patch critiche | > 7 giorni | Patch management |
| N. tentativi accesso falliti | Potenziali attacchi | > baseline +2σ | SIEM |
| N. incidenti sicurezza | Incidenti per periodo | > 3/mese | Incident management |
| % sistemi non compliant | Sistemi fuori standard | > 5% | Configuration audit |

### 12.2 Revisione Periodica

| Tipo Revisione | Frequenza | Scope | Output |
|----------------|-----------|-------|--------|
| Review registro rischi | Trimestrale | Tutti i rischi | Registro aggiornato |
| Risk assessment completo | Annuale | Intero perimetro | Report assessment |
| Review metodologia | Annuale | Metodologia stessa | Aggiornamenti se necessari |
| Riesame Direzione | Annuale | Sintesi rischi | Decisioni strategiche |

### 12.3 Trigger per Revisione Straordinaria

- Incidente di sicurezza significativo
- Nuova normativa applicabile
- Cambiamento organizzativo rilevante
- Introduzione di nuove tecnologie
- Risultati di audit o penetration test
- Cambiamento nel panorama delle minacce

---

## 13. Comunicazione e Reporting

| Report | Destinatari | Frequenza | Contenuto |
|--------|-------------|-----------|-----------|
| Risk Dashboard | CISO, IT Management | Mensile | Top 10 rischi, KRI, trend |
| Risk Summary | Direzione | Trimestrale | Sintesi rischi, azioni, escalation |
| Risk Deep Dive | Riesame Direzione | Annuale | Analisi completa, decisioni richieste |

---

## 14. Documenti Correlati

| Codice | Documento | Relazione |
|--------|-----------|-----------|
| {{company_name}}-REG-ISMS-001 | Risk Register | Output del processo |
| {{company_name}}-REG-ISMS-002 | Risk Treatment Plan | Azioni di trattamento |
| {{company_name}}-REG-ISMS-003 | Asset Inventory | Input per identificazione |
| {{company_name}}-SOA-ISMS-001 | Statement of Applicability | Controlli selezionati |
| {{company_name}}-POL-ISMS-001 | Information Security Policy | Criteri accettazione rischio |

---

## 15. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{security_officer_title}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Allegato A: Worksheet Valutazione Rischio

```
┌─────────────────────────────────────────────────────────────────────┐
│                    RISK ASSESSMENT WORKSHEET                         │
├─────────────────────────────────────────────────────────────────────┤
│ ID Rischio: R-_____              Data Valutazione: ___/___/___      │
│ Valutatore: _________________    Risk Owner: ___________________    │
├─────────────────────────────────────────────────────────────────────┤
│ IDENTIFICAZIONE                                                      │
├─────────────────────────────────────────────────────────────────────┤
│ Asset coinvolto: ________________________________________________   │
│ Minaccia: _______________________________________________________   │
│ Vulnerabilità: __________________________________________________   │
│ Descrizione scenario: ___________________________________________   │
├─────────────────────────────────────────────────────────────────────┤
│ ANALISI                                                              │
├─────────────────────────────────────────────────────────────────────┤
│ Impatto su Riservatezza:    [ ]1  [ ]2  [ ]3  [ ]4  [ ]5           │
│ Impatto su Integrità:       [ ]1  [ ]2  [ ]3  [ ]4  [ ]5           │
│ Impatto su Disponibilità:   [ ]1  [ ]2  [ ]3  [ ]4  [ ]5           │
│                                                                      │
│ IMPATTO MASSIMO: _____                                               │
│ Probabilità: [ ]1  [ ]2  [ ]3  [ ]4  [ ]5                           │
│                                                                      │
│ RISCHIO INERENTE (I × P): _____                                      │
├─────────────────────────────────────────────────────────────────────┤
│ CONTROLLI ESISTENTI                                                  │
├─────────────────────────────────────────────────────────────────────┤
│ Controlli in essere: ____________________________________________   │
│ Efficacia controlli: [ ]Nessuna [ ]Bassa [ ]Media [ ]Alta [ ]Molto Alta│
│                                                                      │
│ RISCHIO RESIDUO: _____                                               │
├─────────────────────────────────────────────────────────────────────┤
│ TRATTAMENTO                                                          │
├─────────────────────────────────────────────────────────────────────┤
│ Opzione: [ ]Mitigare [ ]Trasferire [ ]Evitare [ ]Accettare          │
│ Azioni proposte: ________________________________________________   │
│ Rischio target: _____          Deadline: ___/___/___                │
├─────────────────────────────────────────────────────────────────────┤
│ APPROVAZIONE                                                         │
├─────────────────────────────────────────────────────────────────────┤
│ Risk Owner: _________________ Firma: ___________ Data: ___/___/___  │
│ CISO: _______________________ Firma: ___________ Data: ___/___/___  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{security_officer_title}}` | Approvazioni — verificato da | ☐ |
| 6 | `{{contact_name}}` | Approvazioni — redatto da | ☐ |
| 7 | `{{risk_appetite_threshold}}` | Sezione 10 — soglia accettazione rischio (es. 9) | ☐ |
| 8 | Scala impatto calibrata | Sezione 6 — valori finanziari e temporali per la propria realta | ☐ |
| 9 | Scala probabilita calibrata | Sezione 7 — frequenze allineate allo storico aziendale | ☐ |
| 10 | KRI configurati | Sezione 12 — soglie KRI basate su baseline reali | ☐ |

---

*Template conforme a ISO/IEC 27001:2022 Clausole 6.1.2, 8.2*
*Allineato a ISO 31000:2018, ISO 27005:2022, NIS2 Art. 21, DORA Art. 6*
*Creato con Kynosure.ai*
