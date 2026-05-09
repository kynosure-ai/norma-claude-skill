---
title: Procedura di Valutazione e Mitigazione del Bias
product: Kynosure.ai
framework: ISO42001
version: '1.0'
clausola: '8.2'
controlliAnnexA:
  - A.7.6
  - A.5.3
  - A.6.6
aiActCategory: high-risk
documentType: procedure
lastUpdated: '2025-01-03'
language: IT
author: Kynosure.ai
licenza: CC BY-NC-SA 4.0
crossReference:
  - EU AI Act Art.10(2f)
  - NIST AI RMF
  - IEEE 7003
subset: true
---

# Procedura di Valutazione e Mitigazione del Bias

## Informazioni Documento

| Campo | Valore |
|-------|--------|
| Codice Documento | {{company_name}}-PRO-AIMS-003 |
| Versione | 1.0 |
| Data Emissione | {{document_date}} |
| Data Prossima Revisione | [GG/MM/AAAA + 1 anno] |
| Classificazione | Interno |
| Proprietario | [AI Governance Lead] |
| Approvato da | [AI Ethics Committee / Top Management] |

## Storico Revisioni

| Ver. | Data | Autore | Modifiche |
|------|------|--------|-----------|
| 1.0 | [Data] | [Nome] | Prima emissione |

---

## 1. Scopo

Questa procedura definisce il processo strutturato per identificare, valutare, mitigare e monitorare il bias nei dati e nei modelli AI di {{company_name}}, garantendo che le decisioni algoritmiche siano eque e prive di discriminazioni ingiustificate verso individui o gruppi. Il bias rappresenta una delle sfide piu critiche nell'ambito dell'intelligenza artificiale, potendo determinare impatti significativi sui diritti fondamentali delle persone quando i sistemi AI influenzano decisioni in ambiti quali l'accesso al credito, l'occupazione, i servizi sanitari o la giustizia.

La procedura supporta la conformita ai controlli A.7.6, A.5.3 e A.6.6 di ISO/IEC 42001:2023, che richiedono all'Organizzazione di implementare processi per l'identificazione e la mitigazione dei bias nei sistemi AI. Per i sistemi classificati come high-risk, la procedura assicura il rispetto dell'Articolo 10 comma 2 lettera f del Regolamento Europeo sull'Intelligenza Artificiale, che impone l'esame dei dataset per l'identificazione di possibili bias che potrebbero compromettere la salute e la sicurezza delle persone, incidere negativamente sui diritti fondamentali o portare a discriminazioni vietate. L'applicazione sistematica di questa procedura consente all'Organizzazione di sviluppare e operare sistemi AI in linea con i principi di fairness e AI etica adottati.

---

## 2. Ambito

La presente procedura si applica a tutti i dataset utilizzati per il training dei modelli AI dell'Organizzazione, nonche a tutti i modelli sviluppati internamente o acquisiti da fornitori esterni, indipendentemente dalla tecnologia utilizzata o dal dominio applicativo. L'ambito copre l'intero ciclo di vita dei sistemi AI, dalla fase di progettazione e raccolta dati attraverso lo sviluppo e il training, fino al deployment in produzione e al monitoraggio continuo delle performance in termini di equita.

La procedura trova applicazione prioritaria per i sistemi classificati come High-Risk ai sensi del Regolamento Europeo sull'Intelligenza Artificiale, per i quali i requisiti di fairness sono piu stringenti e le conseguenze di eventuali bias piu significative per gli individui impattati. Per i sistemi a rischio limitato o minimo, l'Organizzazione applica la procedura in forma proporzionata al livello di rischio, garantendo comunque una valutazione sistematica delle potenziali distorsioni algoritmiche.

| Categoria | Applicazione |
|-----------|--------------|
| Dataset per training AI | Analisi distribuzione, representation bias, label bias |
| Modelli sviluppati internamente | Assessment completo pre-deployment |
| Modelli acquisiti da fornitori | Valutazione fairness in acceptance testing |
| Sistemi High-Risk | Procedura completa con approvazione Ethics Committee |
| Sistemi Limited/Minimal Risk | Procedura proporzionata al rischio |

---

## 3. Definizioni

| Termine | Definizione |
|---------|-------------|
| **Bias** | Distorsione sistematica che produce risultati iniqui o discriminatori |
| **Fairness** | Assenza di discriminazione ingiusta verso individui o gruppi |
| **Attributo Protetto** | Caratteristica per cui la discriminazione e vietata (genere, eta, etnia, etc.) |
| **Disparate Impact** | Effetto sproporzionatamente negativo su un gruppo protetto |
| **Disparate Treatment** | Trattamento differenziato esplicito basato su attributo protetto |
| **Proxy Variable** | Variabile correlata con attributo protetto che puo veicolare bias |

---

## 4. Tipi di Bias

### 4.1 Bias nei Dati

| Tipo | Descrizione | Esempio | Fase |
|------|-------------|---------|------|
| **Selection Bias** | Campione non rappresentativo della popolazione | Dataset da fonte non random | Collection |
| **Representation Bias** | Gruppi sotto/sovra-rappresentati | Minoranze sottorappresentate | Collection |
| **Measurement Bias** | Errori sistematici nella misurazione | Strumenti meno accurati per certi gruppi | Collection |
| **Label Bias** | Etichette riflettono pregiudizi umani | Annotatori con bias impliciti | Labeling |
| **Historical Bias** | Dati riflettono discriminazioni passate | Dati HR con storico discriminatorio | Source |
| **Aggregation Bias** | Modello unico per gruppi eterogenei | Un modello per contesti diversi | Design |
| **Sampling Bias** | Campionamento non casuale | Oversampling di maggioranza | Sampling |

### 4.2 Bias Algoritmici

| Tipo | Descrizione | Esempio |
|------|-------------|---------|
| **Algorithmic Bias** | Modello amplifica pattern discriminatori | Amplificazione correlazioni spurie |
| **Optimization Bias** | Funzione obiettivo non considera fairness | Ottimizza solo accuracy |
| **Evaluation Bias** | Metriche valutazione non catturano disparita | Accuracy aggregata nasconde gap |
| **Deployment Bias** | Sistema usato in contesto diverso da training | Modello US applicato in EU |
| **Feedback Loop Bias** | Predizioni influenzano dati futuri | Predictive policing |

---

## 5. Processo di Bias Assessment

### 5.1 Overview del Processo

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         BIAS ASSESSMENT PROCESS                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐ │
│  │1. DEFINE │──▶│2. ANALYZE│──▶│3. MEASURE│──▶│4.MITIGATE│──▶│5. MONITOR│ │
│  │ CONTEXT  │   │   DATA   │   │ FAIRNESS │   │   BIAS   │   │ ONGOING  │ │
│  └──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘ │
│       │              │              │              │              │        │
│       ▼              ▼              ▼              ▼              ▼        │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐ │
│  │Protected │   │   Data   │   │ Fairness │   │Mitigation│   │Monitoring│ │
│  │Attributes│   │  Bias    │   │ Metrics  │   │  Plan    │   │Dashboard │ │
│  │ Defined  │   │  Report  │   │  Report  │   │          │   │          │ │
│  └──────────┘   └──────────┘   └──────────┘   └──────────┘   └──────────┘ │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 6. Step 1: Definire il Contesto

### 6.1 Identificare gli Attributi Protetti

Determinare quali attributi sono rilevanti per il contesto:

| Attributo | Base Normativa | Rilevante per Sistema? |
|-----------|----------------|------------------------|
| Genere | GDPR Art. 9, Costituzione | [ ] SI / [ ] NO |
| Eta | GDPR Art. 9, L. 903/77 | [ ] SI / [ ] NO |
| Origine etnica/razziale | GDPR Art. 9, Costituzione | [ ] SI / [ ] NO |
| Religione | GDPR Art. 9 | [ ] SI / [ ] NO |
| Orientamento sessuale | GDPR Art. 9 | [ ] SI / [ ] NO |
| Disabilita | L. 68/99, GDPR Art. 9 | [ ] SI / [ ] NO |
| Nazionalita | Costituzione | [ ] SI / [ ] NO |
| Stato di salute | GDPR Art. 9 | [ ] SI / [ ] NO |
| Opinioni politiche | GDPR Art. 9 | [ ] SI / [ ] NO |
| Condizione economica | - | [ ] SI / [ ] NO |
| [Altro specifico dominio] | [Base] | [ ] SI / [ ] NO |

### 6.2 Definire Gruppi per Analisi

Per ogni attributo rilevante:

| Attributo | Gruppi | Dati Disponibili |
|-----------|--------|------------------|
| Genere | M, F, Non-binary, Unknown | [ ] Diretto / [ ] Proxy / [ ] Non disponibile |
| Eta | 18-25, 26-35, 36-50, 51-65, 65+ | [ ] Diretto / [ ] Proxy / [ ] Non disponibile |
| [Altro] | [Gruppi] | [ ] Diretto / [ ] Proxy / [ ] Non disponibile |

### 6.3 Identificare Proxy Variables

Variabili che potrebbero essere correlate con attributi protetti:

| Proxy Potenziale | Attributo Correlato | Correlazione Stimata |
|------------------|---------------------|---------------------|
| CAP/Zona | Etnia, reddito | [Alta/Media/Bassa] |
| Nome | Genere, etnia | [Alta/Media/Bassa] |
| Universita | Status economico | [Alta/Media/Bassa] |
| [Altro] | [Attributo] | [Livello] |

### 6.4 Definire il Contesto Decisionale

| Aspetto | Descrizione |
|---------|-------------|
| **Decisione AI** | [Cosa decide il sistema] |
| **Outcome Favorevole** | [Qual e l'outcome positivo] |
| **Outcome Sfavorevole** | [Qual e l'outcome negativo] |
| **Impatto su Individui** | [Come sono impattati] |
| **Stakeholder Vulnerabili** | [Gruppi piu a rischio] |
| **Requisiti Legali** | [Normative specifiche] |

---

## 7. Step 2: Analizzare i Dati per Bias

### 7.1 Analisi Distribuzione

Per ogni attributo protetto, analizzare:

**Template Analisi Distribuzione**:

| Gruppo | N. Records | % Dataset | % Popolazione Target | Gap | Status |
|--------|------------|-----------|---------------------|-----|--------|
| [Gruppo A] | [N] | [X%] | [Y%] | [+/- Z%] | [OK/Warning/Critical] |
| [Gruppo B] | [N] | [X%] | [Y%] | [+/- Z%] | [OK/Warning/Critical] |

**Soglie**:
- OK: Gap < 10%
- Warning: Gap 10-20%
- Critical: Gap > 20%

### 7.2 Analisi Label Distribution

Per ogni outcome:

| Gruppo | N. Positive | N. Negative | % Positive | Base Rate Diff |
|--------|-------------|-------------|------------|----------------|
| [Gruppo A] | [N] | [N] | [X%] | (baseline) |
| [Gruppo B] | [N] | [N] | [X%] | [+/- Y%] |

### 7.3 Analisi Feature Distribution

Per features potenzialmente problematiche:

| Feature | Gruppo A Mean | Gruppo B Mean | Difference | Significant? |
|---------|---------------|---------------|------------|--------------|
| [Feature 1] | [X] | [Y] | [Z] | [ ] SI / [ ] NO |
| [Feature 2] | [X] | [Y] | [Z] | [ ] SI / [ ] NO |

### 7.4 Identificazione Bias nei Dati

**Checklist Bias Dati**:

- [ ] Selection bias: Dati provengono da fonte rappresentativa?
- [ ] Representation bias: Tutti i gruppi adeguatamente rappresentati?
- [ ] Measurement bias: Stessa qualita misurazione per tutti i gruppi?
- [ ] Label bias: Labeling consistente tra gruppi?
- [ ] Historical bias: Dati riflettono discriminazioni passate?
- [ ] Proxy variables: Identificate e documentate?

---

## 8. Step 3: Misurare Fairness

### 8.1 Metriche di Fairness

#### 8.1.1 Metriche di Gruppo (Group Fairness)

| Metrica | Formula | Interpretazione | Threshold |
|---------|---------|-----------------|-----------|
| **Demographic Parity** | P(Y=1\|A=0) = P(Y=1\|A=1) | Stessa probabilita outcome positivo | Diff < 0.1 |
| **Equalized Odds** | TPR e FPR uguali tra gruppi | Stessi tassi errore | Diff < 0.1 |
| **Equal Opportunity** | TPR uguale tra gruppi | Stessa sensibilita per positivi | Diff < 0.1 |
| **Predictive Parity** | PPV uguale tra gruppi | Stessa precision | Diff < 0.1 |
| **Calibration** | P(Y=1\|S=s, A) = s | Probabilita calibrate per gruppo | ECE < 0.05 |

#### 8.1.2 Metriche Individuali (Individual Fairness)

| Metrica | Definizione | Misurazione |
|---------|-------------|-------------|
| **Individual Fairness** | Individui simili → outcome simili | Consistency score |
| **Counterfactual Fairness** | Outcome uguale se attributo protetto fosse diverso | Counterfactual analysis |

#### 8.1.3 Metriche Causali

| Metrica | Definizione | Uso |
|---------|-------------|-----|
| **Direct Discrimination** | Effetto diretto attributo → outcome | Causal analysis |
| **Indirect Discrimination** | Effetto via proxy variables | Path analysis |

### 8.2 Template Misurazione Fairness

```markdown
# Fairness Metrics Report
## Sistema: [Nome]
## Data: [Data]

### Configurazione
- Attributo protetto: [Attributo]
- Gruppo privilegiato: [Gruppo A]
- Gruppo non privilegiato: [Gruppo B]
- Outcome positivo: [Definizione]

### Metriche Misurate

| Metrica | Gruppo A | Gruppo B | Differenza | Threshold | Status |
|---------|----------|----------|------------|-----------|--------|
| Base Rate | [X%] | [Y%] | [Z%] | < 20% | [PASS/FAIL] |
| TPR | [X%] | [Y%] | [Z%] | < 10% | [PASS/FAIL] |
| FPR | [X%] | [Y%] | [Z%] | < 10% | [PASS/FAIL] |
| PPV | [X%] | [Y%] | [Z%] | < 10% | [PASS/FAIL] |
| Demographic Parity | - | - | [Z] | < 0.1 | [PASS/FAIL] |
| Equalized Odds | - | - | [Z] | < 0.1 | [PASS/FAIL] |

### Confusion Matrix per Gruppo

**Gruppo A**:
|  | Pred + | Pred - |
|--|--------|--------|
| **Act +** | [TP] | [FN] |
| **Act -** | [FP] | [TN] |

**Gruppo B**:
|  | Pred + | Pred - |
|--|--------|--------|
| **Act +** | [TP] | [FN] |
| **Act -** | [FP] | [TN] |

### Fairness Score Complessivo
[Score aggregato o valutazione qualitativa]

### Findings
1. [Finding 1]
2. [Finding 2]

### Raccomandazioni
1. [Raccomandazione 1]
2. [Raccomandazione 2]
```

### 8.3 Selezione Metrica Appropriata

| Contesto | Metrica Raccomandata | Rationale |
|----------|---------------------|-----------|
| Allocazione risorse | Demographic Parity | Equa distribuzione |
| Screening/Selezione | Equal Opportunity | Non penalizzare qualificati |
| Risk scoring | Equalized Odds | Errori bilanciati |
| Credit scoring | Calibration + PPV | Decisioni accurate |
| Healthcare | Equal Opportunity | Non negare cure a chi ne ha bisogno |

> **Nota**: Non esiste una metrica universale. La scelta dipende dal contesto e dai valori dell'organizzazione. Documentare sempre il rationale.

---

## 9. Step 4: Mitigare il Bias

### 9.1 Tecniche di Mitigazione

#### 9.1.1 Pre-processing (sui Dati)

| Tecnica | Descrizione | Pro | Contro |
|---------|-------------|-----|--------|
| **Resampling** | Over/under-sampling gruppi | Semplice | Overfitting/perdita dati |
| **Reweighting** | Pesi diversi per gruppi | Preserva dati | Complessita training |
| **Relabeling** | Correzione label biased | Corregge label bias | Richiede expertise |
| **Disparate Impact Remover** | Modifica features per ridurre correlazione | Riduce proxy effect | Modifica distribuzione |
| **Fair Representation Learning** | Apprendere rappresentazione fair | Automatico | Complessita |

#### 9.1.2 In-processing (nel Training)

| Tecnica | Descrizione | Pro | Contro |
|---------|-------------|-----|--------|
| **Fairness Constraints** | Vincoli fairness in ottimizzazione | Integrato in training | Trade-off accuracy |
| **Adversarial Debiasing** | Rete avversaria per rimuovere bias | Potente | Complessita |
| **Prejudice Remover** | Regularizzazione per fairness | Flessibile | Tuning difficile |
| **Meta-Fair Classifier** | Meta-learning per fairness | Adattabile | Computazionalmente costoso |

#### 9.1.3 Post-processing (sulle Predizioni)

| Tecnica | Descrizione | Pro | Contro |
|---------|-------------|-----|--------|
| **Threshold Optimization** | Soglie diverse per gruppo | Semplice, non richiede retraining | Richiede attributo a runtime |
| **Calibrated Equalized Odds** | Aggiusta probabilita per fairness | Preserva calibrazione | Complessita |
| **Reject Option Classification** | Revisione umana casi borderline | Human oversight | Scalabilita |

### 9.2 Selezione Strategia di Mitigazione

| Situazione | Strategia Raccomandata |
|------------|------------------------|
| Bias evidente nei dati | Pre-processing (resampling, reweighting) |
| Dati ok ma modello biased | In-processing (constraints) |
| Modello esistente, no retraining | Post-processing (threshold) |
| Bias complesso/multi-source | Combinazione tecniche |
| High-Risk, zero tolerance | Pre + In + Post + Human oversight |

### 9.3 Template Piano di Mitigazione

```markdown
# Bias Mitigation Plan
## Sistema: [Nome]

### Bias Identificati
| ID | Tipo Bias | Severita | Impatto | Priorita |
|----|-----------|----------|---------|----------|
| B-001 | [Tipo] | [H/M/L] | [Descrizione] | [1/2/3] |

### Azioni di Mitigazione
| ID Bias | Azione | Tecnica | Owner | Deadline | Status |
|---------|--------|---------|-------|----------|--------|
| B-001 | [Azione] | [Tecnica] | [Nome] | [Data] | [Status] |

### Trade-off Analysis
| Mitigazione | Impatto Fairness | Impatto Accuracy | Decisione |
|-------------|------------------|------------------|-----------|
| [Tecnica A] | [+X%] | [-Y%] | [Accettare/Rifiutare] |

### Rischi Residui
| Rischio | Probabilita | Impatto | Mitigazione |
|---------|-------------|---------|-------------|
| [Rischio residuo] | [H/M/L] | [H/M/L] | [Controlli] |

### Approvazione
| Ruolo | Nome | Data |
|-------|------|------|
| AI System Owner | | |
| AI Ethics Committee | | |
```

---

## 10. Step 5: Monitorare nel Tempo

### 10.1 Metriche di Monitoraggio

| Metrica | Frequenza | Alert Threshold | Owner |
|---------|-----------|-----------------|-------|
| Demographic Parity | [Settimanale] | Diff > 0.15 | [Nome] |
| Equalized Odds | [Settimanale] | Diff > 0.12 | [Nome] |
| Group outcome rates | [Giornaliero] | Variazione > 10% | [Nome] |
| Complaint rate per gruppo | [Mensile] | Ratio > 2:1 | [Nome] |

### 10.2 Dashboard Fairness

Elementi da includere:
- Fairness metrics trend over time
- Outcome distribution per gruppo
- Alert per threshold superati
- Comparison con baseline

### 10.3 Trigger per Re-assessment

- [ ] Metriche fairness superano threshold
- [ ] Nuovi dati con distribuzione diversa
- [ ] Cambio use case o popolazione
- [ ] Feedback/complaint significativi
- [ ] Retraining del modello
- [ ] Audit interno/esterno
- [ ] Periodico (almeno annuale)

### 10.4 Processo di Escalation

| Livello | Trigger | Azione | Responsabile |
|---------|---------|--------|--------------|
| 1 - Warning | Metrica vicina a threshold | Investigate | ML Engineer |
| 2 - Alert | Threshold superato | Stop & investigate | AI System Owner |
| 3 - Critical | Multiple metriche failed | Stop, escalation | AI Governance Lead |
| 4 - Incident | Impatto su utenti | Incident response | AI Ethics Committee |

---

## 11. Documentazione e Reporting

### 11.1 Bias Assessment Report

Ogni sistema AI deve avere un Bias Assessment Report che include:

1. **Contesto**: Attributi protetti, gruppi, contesto decisionale
2. **Data Analysis**: Distribuzione, representation, proxy
3. **Fairness Metrics**: Metriche misurate, risultati
4. **Findings**: Bias identificati, severita
5. **Mitigations**: Azioni intraprese, tecniche usate
6. **Residual Risk**: Rischi residui, accettazione
7. **Monitoring Plan**: Come verra monitorato
8. **Approvals**: Firme e approvazioni

### 11.2 Integrazione con AIIA

Il Bias Assessment alimenta la sezione 7 (Fairness Assessment) dell'AI Impact Assessment.

### 11.3 Retention

- Bias Assessment Reports: Vita del sistema + 5 anni
- Monitoring data: 3 anni rolling
- Incident reports: 10 anni

---

## 12. Ruoli e Responsabilita

| Ruolo | Responsabilita |
|-------|----------------|
| **AI System Owner** | Assicurare assessment completato, approvare mitigazioni |
| **ML Engineer** | Eseguire analisi tecniche, implementare mitigazioni |
| **Data Scientist** | Analisi dati, calcolo metriche, interpretazione |
| **AI Ethics Committee** | Review assessment, guidance su casi complessi |
| **AI Governance Lead** | Definire standard, review policy, escalation |
| **Legal/Compliance** | Verificare conformita normativa |

---

## 13. Checklist Bias Assessment

### Pre-Development
- [ ] Attributi protetti identificati
- [ ] Gruppi definiti
- [ ] Proxy variables identificate
- [ ] Requisiti fairness definiti
- [ ] Metriche selezionate

### Data Analysis
- [ ] Distribuzione analizzata
- [ ] Representation bias valutato
- [ ] Label bias valutato
- [ ] Historical bias considerato
- [ ] Data quality per gruppo verificata

### Model Evaluation
- [ ] Fairness metrics calcolate
- [ ] Threshold definiti
- [ ] Trade-off accuracy-fairness valutato
- [ ] Intersectional analysis (se rilevante)

### Mitigation
- [ ] Azioni di mitigazione definite
- [ ] Tecniche selezionate
- [ ] Trade-off documentati
- [ ] Rischi residui accettati

### Monitoring
- [ ] Piano monitoraggio definito
- [ ] Dashboard configurata
- [ ] Alert impostati
- [ ] Processo escalation definito

### Documentation
- [ ] Bias Assessment Report completo
- [ ] AIIA aggiornato
- [ ] Model Card aggiornato
- [ ] Approvazioni ottenute

---

## 14. Documenti Correlati

| Codice | Documento |
|--------|-----------|
| {{company_name}}-POL-AIMS-002 | Data Governance Policy |
| {{company_name}}-DOC-AIMS-002 | Data Quality Requirements |
| {{company_name}}-AIIA-[ID] | AI Impact Assessment |
| {{company_name}}-MOD-[ID] | Model Card |
| {{company_name}}-MET-AIMS-001 | AI Risk Assessment Methodology |

---

## Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Ambito assessment definito (sistemi AI target)
- [ ] Attributi protetti identificati per il contesto
- [ ] Metriche fairness selezionate e soglie definite
- [ ] Metodologia di testing documentata
- [ ] Risultati assessment documentati con evidenze
- [ ] Azioni correttive definite per bias identificati
- [ ] Rischi residui valutati e accettati
- [ ] Piano monitoraggio continuo definito
- [ ] Dashboard e alert configurati
- [ ] AIIA e Model Card aggiornati
- [ ] Tutti i `{{placeholder}}` sostituiti con dati reali
- [ ] Approvazioni ottenute

---

*Template fornito da Kynosure.ai - Compliance AI con intelligenza*
