---
title: AI Impact Assessment (AIIA)
product: Kynosure.ai
framework: ISO42001
version: '1.0'
clausola: 6.1.3
controlliAnnexA:
  - A.5.2
  - A.5.3
  - A.5.4
  - A.5.5
  - A.5.6
aiActCategory: high-risk
documentType: assessment
lastUpdated: '2025-01-03'
language: IT
author: Kynosure.ai
licenza: CC BY-NC-SA 4.0
crossReference:
  - EU AI Act Art.9
  - ISO 42001 8.2
  - NIST AI RMF
subset: true
---

# AI Impact Assessment (AIIA)

## Informazioni Documento

| Campo | Valore |
|-------|--------|
| Codice Documento | {{company_name}}-AIIA-[ID SISTEMA] |
| Versione | 1.0 |
| Data Assessment | {{document_date}} |
| Data Prossima Revisione | [GG/MM/AAAA + 12 mesi max] |
| Classificazione | Riservato |
| Proprietario | [AI System Owner] |
| Valutatore | [AI Governance Lead / Assessor] |
| Stato | [Bozza / In Review / Approvato / Scaduto] |

## Storico Revisioni

| Ver. | Data | Autore | Modifiche |
|------|------|--------|-----------|
| 1.0 | [Data] | [Nome] | Prima emissione |
| | | | |

---

## 1. Scopo

Questo documento presenta la valutazione degli impatti (AI Impact Assessment - AIIA) del sistema AI {{system_name}}, in conformita alla clausola 6.1.3 di ISO/IEC 42001:2023 e ai requisiti dell'EU AI Act per i sistemi ad alto rischio.

L'AIIA valuta sistematicamente gli impatti potenziali del sistema AI su individui, gruppi e societa, identificando misure di mitigazione e determinando l'accettabilita del rischio complessivo.

---

## 2. Informazioni Sistema AI

### 2.1 Identificazione

| Campo | Valore |
|-------|--------|
| Nome Sistema | [Nome descrittivo] |
| ID Sistema | [AI-SYS-XXX] |
| Versione | [X.Y.Z] |
| AI System Owner | [Nome / Ruolo] |
| Team Responsabile | [Nome team] |
| Data Prima Release | [GG/MM/AAAA o "Non ancora deployato"] |

### 2.2 Descrizione Funzionale

**Scopo del Sistema**:
> [Descrivere in 2-3 frasi cosa fa il sistema e quale problema risolve]

**Tipo di AI**:
- [ ] Machine Learning - Classificazione
- [ ] Machine Learning - Regressione
- [ ] Machine Learning - Clustering
- [ ] Deep Learning - Neural Networks
- [ ] Natural Language Processing (NLP)
- [ ] Computer Vision
- [ ] AI Generativa (GenAI / LLM)
- [ ] Sistema Esperto / Rule-based
- [ ] Reinforcement Learning
- [ ] Altro: [specificare]

**Architettura/Modello**:
> [Es. Transformer, CNN, XGBoost, Random Forest, GPT-based, custom model]

**Output del Sistema**:
> [Tipo di output: predizioni, classificazioni, raccomandazioni, contenuti generati, decisioni, score]

### 2.3 Dati

| Aspetto | Descrizione |
|---------|-------------|
| Dati di Training | [Descrizione dataset, dimensione, periodo, fonte] |
| Dati di Input (runtime) | [Tipo di dati elaborati in produzione] |
| Dati Personali | [ ] SI / [ ] NO - Se SI: [categorie dati, base giuridica GDPR] |
| Dati Sensibili | [ ] SI / [ ] NO - Se SI: [Art. 9 GDPR categories] |
| Provenienza Dati | [Fonte: interni, acquistati, pubblici, crowdsourced] |

### 2.4 Contesto Operativo

| Aspetto | Descrizione |
|---------|-------------|
| Ambiente | [ ] Development / [ ] Staging / [ ] Production |
| Scala di Utilizzo | [N. utenti, N. transazioni/giorno, volume dati] |
| Integrazione | [Sistemi collegati, API, database] |
| Canale di Erogazione | [Web app, mobile, API, embedded, batch] |

---

## 3. Stakeholder Analysis

### 3.1 Utenti del Sistema

| Categoria | Descrizione | Numero Stimato |
|-----------|-------------|----------------|
| Utenti Interni | [Chi usa il sistema internamente] | [N] |
| Utenti Esterni | [Clienti, partner che interagiscono] | [N] |
| Operatori | [Chi gestisce/supervisiona il sistema] | [N] |

### 3.2 Soggetti Impattati (Affected Parties)

| Categoria | Descrizione | Tipo Impatto |
|-----------|-------------|--------------|
| Individui Diretti | [Persone su cui il sistema prende decisioni] | [Decisioni li riguardano direttamente] |
| Individui Indiretti | [Persone i cui dati sono usati per training] | [Privacy, uso dati] |
| Gruppi Specifici | [Gruppi potenzialmente piu impattati] | [Rischio bias/discriminazione] |
| Dipendenti | [Staff il cui lavoro e influenzato] | [Automazione, cambio ruoli] |
| Societa | [Impatto sistemico piu ampio] | [Se applicabile] |

### 3.3 Altri Stakeholder

| Stakeholder | Interesse | Coinvolgimento |
|-------------|-----------|----------------|
| Regolatori | Compliance EU AI Act, GDPR | [Come vengono informati] |
| Management | ROI, rischio reputazionale | [Approvazione richiesta] |
| Legal/Compliance | Conformita normativa | [Review obbligatoria] |
| IT Security | Sicurezza sistema | [Assessment security] |
| [Altri] | [Interesse] | [Coinvolgimento] |

---

## 4. Classificazione del Rischio

### 4.1 Screening EU AI Act

**Il sistema rientra nelle categorie VIETATE (Art. 5)?**

| Pratica Vietata | Applicabile? | Note |
|-----------------|--------------|------|
| Social scoring da parte di autorita pubbliche | [ ] SI / [x] NO | |
| Sfruttamento vulnerabilita (eta, disabilita) | [ ] SI / [x] NO | |
| Manipolazione subliminale | [ ] SI / [x] NO | |
| Identificazione biometrica real-time in spazi pubblici | [ ] SI / [x] NO | |
| Categorizzazione biometrica per inferire dati sensibili | [ ] SI / [x] NO | |
| Scraping non mirato immagini facciali | [ ] SI / [x] NO | |
| Emotion recognition sul lavoro/scuola (non safety) | [ ] SI / [x] NO | |
| Predictive policing basato solo su profiling | [ ] SI / [x] NO | |

> **Se anche 1 = SI → STOP: Il sistema NON puo essere sviluppato/utilizzato**

### 4.2 Screening High-Risk (Annex III EU AI Act)

| Categoria High-Risk | Applicabile? | Note |
|---------------------|--------------|------|
| **Biometria** | | |
| Identificazione biometrica remota | [ ] SI / [ ] NO | |
| Categorizzazione biometrica | [ ] SI / [ ] NO | |
| Emotion recognition | [ ] SI / [ ] NO | |
| **Infrastrutture Critiche** | | |
| Sicurezza componenti critici (trasporti, energia, acqua) | [ ] SI / [ ] NO | |
| **Istruzione e Formazione** | | |
| Accesso a istituti educativi | [ ] SI / [ ] NO | |
| Valutazione studenti/esami | [ ] SI / [ ] NO | |
| Monitoraggio comportamento esami | [ ] SI / [ ] NO | |
| **Occupazione e HR** | | |
| Recruiting e selezione CV | [ ] SI / [ ] NO | |
| Decisioni su promozioni/cessazioni | [ ] SI / [ ] NO | |
| Allocazione task basata su tratti personali | [ ] SI / [ ] NO | |
| Monitoraggio performance lavoratori | [ ] SI / [ ] NO | |
| **Servizi Essenziali** | | |
| Accesso a servizi pubblici essenziali | [ ] SI / [ ] NO | |
| Valutazione creditizia | [ ] SI / [ ] NO | |
| Pricing assicurazioni vita/salute | [ ] SI / [ ] NO | |
| Valutazione emergenze (112, pronto soccorso) | [ ] SI / [ ] NO | |
| **Law Enforcement** | | |
| Valutazione rischio vittima/reato | [ ] SI / [ ] NO | |
| Poligrafo, detection inganno | [ ] SI / [ ] NO | |
| Valutazione affidabilita prove | [ ] SI / [ ] NO | |
| Profiling per indagini | [ ] SI / [ ] NO | |
| **Migrazione e Frontiere** | | |
| Valutazione rischio migratorio | [ ] SI / [ ] NO | |
| Esame domande asilo/visti | [ ] SI / [ ] NO | |
| Identificazione ai confini | [ ] SI / [ ] NO | |
| **Giustizia** | | |
| Assistenza decisioni giudiziarie | [ ] SI / [ ] NO | |
| Risoluzione alternativa dispute | [ ] SI / [ ] NO | |

### 4.3 Determinazione Livello Rischio

| Livello | Criteri | Risultato |
|---------|---------|-----------|
| **Inaccettabile** | Almeno 1 pratica vietata = SI | [ ] |
| **High-Risk** | Almeno 1 categoria Annex III = SI | [ ] |
| **Limited Risk** | Interazione con persone (chatbot), emotion recognition, deepfake/synthetic | [ ] |
| **Minimal Risk** | Nessuno dei precedenti | [ ] |

**CLASSIFICAZIONE FINALE**: [Inaccettabile / High-Risk / Limited Risk / Minimal Risk]

> **Se High-Risk**: Questo AIIA e OBBLIGATORIO. Procedere con tutte le sezioni seguenti.
> **Se Limited Risk**: Sezioni 5-8 raccomandate. Obblighi trasparenza (Sez. 9).
> **Se Minimal Risk**: Valutazione semplificata possibile. Best practice comunque raccomandate.

---

## 5. Valutazione Impatti su Individui

### 5.1 Impatto su Autonomia

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Il sistema limita la liberta di scelta degli individui? | [ ] Basso / [ ] Medio / [ ] Alto | [Descrizione] | [Misure] |
| Gli individui possono rifiutare/opt-out dal sistema? | [ ] SI / [ ] NO / [ ] Parziale | [Descrizione] | [Misure] |
| Le decisioni sono reversibili? | [ ] SI / [ ] NO / [ ] Parziale | [Descrizione] | [Misure] |

**Valutazione Impatto Autonomia**: [ ] Basso / [ ] Medio / [ ] Alto

### 5.2 Impatto su Dignita

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Il sistema tratta le persone con rispetto? | [ ] SI / [ ] Parziale / [ ] NO | [Descrizione] | [Misure] |
| Ci sono rischi di oggettificazione o de-umanizzazione? | [ ] Basso / [ ] Medio / [ ] Alto | [Descrizione] | [Misure] |
| Il sistema puo causare danno psicologico? | [ ] Basso / [ ] Medio / [ ] Alto | [Descrizione] | [Misure] |

**Valutazione Impatto Dignita**: [ ] Basso / [ ] Medio / [ ] Alto

### 5.3 Impatto su Privacy

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Quantita dati personali raccolti | [ ] Minima / [ ] Moderata / [ ] Estesa | [Categorie dati] | [Minimizzazione] |
| Rischio re-identificazione | [ ] Basso / [ ] Medio / [ ] Alto | [Analisi] | [Anonymization] |
| Rischio inference attack | [ ] Basso / [ ] Medio / [ ] Alto | [Analisi] | [Protezioni] |
| Conformita GDPR | [ ] Conforme / [ ] Gap identificati | [Dettagli] | [Azioni] |
| DPIA richiesta/completata | [ ] Non richiesta / [ ] Richiesta / [ ] Completata | [Riferimento] | |

**Valutazione Impatto Privacy**: [ ] Basso / [ ] Medio / [ ] Alto

### 5.4 Impatto su Sicurezza Fisica

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Il sistema puo causare danni fisici? | [ ] NO / [ ] Indiretto / [ ] Diretto | [Scenari] | [Misure] |
| Safety-critical context? | [ ] NO / [ ] SI | [Descrizione] | [Controlli] |
| Failure modes analizzati? | [ ] SI / [ ] NO | [Riferimento] | |

**Valutazione Impatto Sicurezza**: [ ] Basso / [ ] Medio / [ ] Alto

### 5.5 Impatto Economico su Individui

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Decisioni con impatto finanziario diretto? | [ ] NO / [ ] SI | [Tipo decisioni] | [Controlli] |
| Rischio di perdita economica per errori? | [ ] Basso / [ ] Medio / [ ] Alto | [Scenari] | [Compensazioni] |
| Accesso a servizi/opportunita economiche? | [ ] Non influenzato / [ ] Influenzato | [Descrizione] | [Misure] |

**Valutazione Impatto Economico**: [ ] Basso / [ ] Medio / [ ] Alto

### 5.6 Sintesi Impatti Individuali

| Dimensione | Livello | Trend | Priorita Mitigazione |
|------------|---------|-------|---------------------|
| Autonomia | [B/M/A] | [Stabile/Crescente/Decrescente] | [Alta/Media/Bassa] |
| Dignita | [B/M/A] | | |
| Privacy | [B/M/A] | | |
| Sicurezza | [B/M/A] | | |
| Economico | [B/M/A] | | |
| **COMPLESSIVO** | **[B/M/A]** | | |

---

## 6. Valutazione Impatti su Gruppi e Societa

### 6.1 Impatto su Gruppi Specifici

| Gruppo | Impatto Potenziale | Livello | Evidenze | Mitigazione |
|--------|-------------------|---------|----------|-------------|
| [Gruppo demografico 1] | [Descrizione impatto] | [B/M/A] | [Dati] | [Misure] |
| [Gruppo demografico 2] | [Descrizione impatto] | [B/M/A] | [Dati] | [Misure] |
| [Gruppo vulnerabile] | [Descrizione impatto] | [B/M/A] | [Dati] | [Misure] |
| [Minoranze] | [Descrizione impatto] | [B/M/A] | [Dati] | [Misure] |

### 6.2 Impatto Sistemico

| Aspetto | Valutazione | Evidenze | Mitigazione |
|---------|-------------|----------|-------------|
| Concentrazione di potere/informazioni | [ ] Basso / [ ] Medio / [ ] Alto | [Analisi] | [Misure] |
| Effetti sul mercato del lavoro | [ ] Nessuno / [ ] Trasformazione / [ ] Sostituzione | [Analisi] | [Misure] |
| Impatto su concorrenza/mercato | [ ] Basso / [ ] Medio / [ ] Alto | [Analisi] | [Misure] |
| Effetti su democrazia/dibattito pubblico | [ ] Nessuno / [ ] Possibile / [ ] Significativo | [Analisi] | [Misure] |

### 6.3 Impatto Ambientale

| Aspetto | Valore | Benchmark | Mitigazione |
|---------|--------|-----------|-------------|
| Consumo energetico training | [kWh / MWh] | [vs. industry average] | [Ottimizzazioni] |
| Consumo energetico inference | [kWh/giorno] | [vs. alternative] | [Ottimizzazioni] |
| Carbon footprint stimato | [kg CO2e] | [Offsetting?] | [Azioni] |
| Infrastruttura richiesta | [Descrizione] | | [Efficienza] |

**Valutazione Impatto Ambientale**: [ ] Basso / [ ] Medio / [ ] Alto

### 6.4 Sintesi Impatti Collettivi

| Dimensione | Livello | Priorita Mitigazione |
|------------|---------|---------------------|
| Gruppi specifici | [B/M/A] | [Alta/Media/Bassa] |
| Sistemico | [B/M/A] | |
| Ambientale | [B/M/A] | |
| **COMPLESSIVO** | **[B/M/A]** | |

---

## 7. Fairness Assessment

### 7.1 Gruppi Protetti Analizzati

| Attributo Protetto | Gruppi Identificati | Dati Disponibili |
|-------------------|---------------------|------------------|
| Genere | [M/F/Altro] | [ ] SI / [ ] NO / [ ] Proxy |
| Eta | [Fasce] | [ ] SI / [ ] NO / [ ] Proxy |
| Etnia/Nazionalita | [Gruppi] | [ ] SI / [ ] NO / [ ] Proxy |
| Disabilita | [Categorie] | [ ] SI / [ ] NO / [ ] Proxy |
| [Altro rilevante] | [Gruppi] | [ ] SI / [ ] NO / [ ] Proxy |

### 7.2 Metriche di Fairness

| Metrica | Definizione | Valore Misurato | Threshold | Status |
|---------|-------------|-----------------|-----------|--------|
| **Demographic Parity** | P(Y=1\|A=0) = P(Y=1\|A=1) | [Ratio o diff %] | < 20% diff | [ ] PASS / [ ] FAIL |
| **Equalized Odds** | TPR e FPR uguali tra gruppi | [Valori] | < 10% diff | [ ] PASS / [ ] FAIL |
| **Predictive Parity** | PPV uguale tra gruppi | [Valori] | < 10% diff | [ ] PASS / [ ] FAIL |
| **Calibration** | Probabilita calibrate per gruppo | [Valori] | | [ ] PASS / [ ] FAIL |
| **Individual Fairness** | Individui simili → output simili | [Score] | > 0.8 | [ ] PASS / [ ] FAIL |

### 7.3 Analisi Disparita

| Confronto Gruppi | Outcome Positivo A | Outcome Positivo B | Ratio | Accettabile? |
|-----------------|-------------------|-------------------|-------|--------------|
| [Gruppo A vs B] | [%] | [%] | [A:B] | [ ] SI / [ ] NO |
| [Gruppo C vs D] | [%] | [%] | [C:D] | [ ] SI / [ ] NO |

### 7.4 Bias nel Dataset

| Tipo Bias | Presente? | Descrizione | Mitigazione |
|-----------|-----------|-------------|-------------|
| **Selection bias** | [ ] SI / [ ] NO | [Dettagli] | [Azioni] |
| **Measurement bias** | [ ] SI / [ ] NO | [Dettagli] | [Azioni] |
| **Label bias** | [ ] SI / [ ] NO | [Dettagli] | [Azioni] |
| **Historical bias** | [ ] SI / [ ] NO | [Dettagli] | [Azioni] |
| **Representation bias** | [ ] SI / [ ] NO | [Dettagli] | [Azioni] |

### 7.5 Valutazione Complessiva Fairness

**Status Fairness**: [ ] Adeguato / [ ] Gap Identificati / [ ] Critico

**Gap Identificati**:
1. [Gap 1]
2. [Gap 2]

**Piano di Remediation**:
| Gap | Azione | Owner | Deadline | Status |
|-----|--------|-------|----------|--------|
| [Gap 1] | [Azione] | [Nome] | [Data] | [Aperto/Chiuso] |

---

## 8. Explainability Assessment

### 8.1 Interpretabilita del Modello

| Aspetto | Valutazione | Note |
|---------|-------------|------|
| Tipo di modello | [ ] White-box / [ ] Grey-box / [ ] Black-box | [Architettura] |
| Complessita intrinseca | [ ] Bassa / [ ] Media / [ ] Alta | [Parametri, layers] |
| Interpretabilita nativa | [ ] Alta / [ ] Media / [ ] Bassa | [Es. albero decisionale vs. deep learning] |

### 8.2 Tecniche di Explainability Implementate

| Tecnica | Implementata? | Descrizione | Per Chi |
|---------|---------------|-------------|---------|
| **Feature Importance** | [ ] SI / [ ] NO | [Global importance] | [Sviluppatori, auditor] |
| **SHAP Values** | [ ] SI / [ ] NO | [Local explanations] | [Operatori] |
| **LIME** | [ ] SI / [ ] NO | [Local explanations] | [Operatori] |
| **Attention Visualization** | [ ] SI / [ ] NO | [Per modelli attention-based] | [Sviluppatori] |
| **Counterfactual Explanations** | [ ] SI / [ ] NO | ["Cosa sarebbe servito per..."] | [Utenti finali] |
| **Natural Language Explanations** | [ ] SI / [ ] NO | [Spiegazioni testuali] | [Utenti finali] |
| **Decision Rules Extraction** | [ ] SI / [ ] NO | [Regole approssimate] | [Auditor] |

### 8.3 Spiegazioni per Stakeholder

| Stakeholder | Tipo Spiegazione | Canale | Disponibile? |
|-------------|------------------|--------|--------------|
| Utenti finali | [Cosa e perche] | [UI, documento] | [ ] SI / [ ] NO |
| Operatori/Supervisori | [Dettaglio tecnico] | [Dashboard] | [ ] SI / [ ] NO |
| Auditor/Regolatori | [Documentazione completa] | [Report] | [ ] SI / [ ] NO |
| Soggetti delle decisioni | [Motivi decisione] | [Notifica] | [ ] SI / [ ] NO |

### 8.4 Audit Trail

| Aspetto | Implementato? | Dettagli |
|---------|---------------|----------|
| Logging input/output | [ ] SI / [ ] NO | [Cosa viene loggato] |
| Versioning modello | [ ] SI / [ ] NO | [Sistema di versioning] |
| Tracciabilita decisioni | [ ] SI / [ ] NO | [Collegamento a input specifici] |
| Retention period | [Durata] | [Conformita normativa] |

### 8.5 Valutazione Complessiva Explainability

**Livello Explainability**: [ ] Alto / [ ] Medio / [ ] Basso / [ ] Insufficiente

**Gap Identificati**:
1. [Gap 1]
2. [Gap 2]

**Requisiti EU AI Act (se high-risk)**:
- [ ] Documentazione tecnica disponibile
- [ ] Istruzioni per l'uso chiare
- [ ] Logging automatico funzionante
- [ ] Spiegazioni per affected parties disponibili

---

## 9. Human Oversight Assessment

### 9.1 Livello di Automazione

| Aspetto | Configurazione Attuale |
|---------|----------------------|
| Tipo di decisione | [ ] Raccomandazione / [ ] Decisione supportata / [ ] Decisione automatica |
| Intervento umano | [ ] Sempre richiesto / [ ] Su richiesta / [ ] Solo eccezioni / [ ] Mai |
| Override possibile | [ ] SI, sempre / [ ] SI, con autorizzazione / [ ] NO |

### 9.2 Meccanismi di Supervisione

| Meccanismo | Implementato? | Descrizione | Responsabile |
|------------|---------------|-------------|--------------|
| **Human-in-the-loop** | [ ] SI / [ ] NO | [Approvazione ogni decisione] | [Ruolo] |
| **Human-on-the-loop** | [ ] SI / [ ] NO | [Monitoraggio, override disponibile] | [Ruolo] |
| **Human-in-command** | [ ] SI / [ ] NO | [Controllo completo start/stop] | [Ruolo] |
| **Kill switch** | [ ] SI / [ ] NO | [Arresto emergenza sistema] | [Ruolo] |
| **Escalation path** | [ ] SI / [ ] NO | [Processo per casi dubbi] | [Ruolo] |

### 9.3 Processo di Appello

| Aspetto | Configurazione |
|---------|----------------|
| Diritto di appello comunicato | [ ] SI / [ ] NO |
| Canale per richiedere review | [Email/Form/Altro] |
| SLA risposta | [Tempistica] |
| Decisore dell'appello | [Ruolo/Comitato] |
| Documentazione esito | [ ] SI / [ ] NO |

### 9.4 Competenze Operatori

| Aspetto | Status |
|---------|--------|
| Training specifico completato | [ ] SI / [ ] NO / [ ] In corso |
| Comprensione limiti del sistema | [ ] Verificata / [ ] Da verificare |
| Capacita di identificare errori | [ ] Alta / [ ] Media / [ ] Bassa |
| Autorevolezza per override | [ ] Definita / [ ] Da definire |

### 9.5 Valutazione Complessiva Human Oversight

**Livello Human Oversight**: [ ] Adeguato / [ ] Parziale / [ ] Insufficiente

**Gap Identificati**:
1. [Gap 1]
2. [Gap 2]

---

## 10. Valutazione Rischi Specifici AI

### 10.1 Rischi Tecnici

| Rischio | Probabilita | Impatto | Livello | Mitigazione | Status |
|---------|-------------|---------|---------|-------------|--------|
| **Model drift** | [1-5] | [1-5] | [Score] | [Azioni] | [Aperto/Mitigato] |
| **Data quality degradation** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Adversarial attacks** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Data poisoning** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Model theft/extraction** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Overfitting** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Distribution shift** | [1-5] | [1-5] | [Score] | [Azioni] | |

### 10.2 Rischi Operativi

| Rischio | Probabilita | Impatto | Livello | Mitigazione | Status |
|---------|-------------|---------|---------|-------------|--------|
| **Uso improprio** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Over-reliance** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Automation bias** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Skill degradation operatori** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Mancata manutenzione** | [1-5] | [1-5] | [Score] | [Azioni] | |

### 10.3 Rischi Reputazionali e Legali

| Rischio | Probabilita | Impatto | Livello | Mitigazione | Status |
|---------|-------------|---------|---------|-------------|--------|
| **Danno reputazionale** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Non-compliance normativa** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Contenzioso legale** | [1-5] | [1-5] | [Score] | [Azioni] | |
| **Sanzioni amministrative** | [1-5] | [1-5] | [Score] | [Azioni] | |

### 10.4 Matrice Rischio Complessiva

| Probabilita ↓ / Impatto → | 1 Trascurabile | 2 Minore | 3 Moderato | 4 Significativo | 5 Catastrofico |
|---------------------------|----------------|----------|------------|-----------------|----------------|
| **5 Quasi Certo** | 5 | 10 | 15 | 20 | 25 |
| **4 Probabile** | 4 | 8 | 12 | 16 | 20 |
| **3 Possibile** | 3 | 6 | 9 | 12 | 15 |
| **2 Improbabile** | 2 | 4 | 6 | 8 | 10 |
| **1 Raro** | 1 | 2 | 3 | 4 | 5 |

| Score | Livello | Azione Richiesta |
|-------|---------|------------------|
| >= 15 | Critico | Mitigazione immediata o stop deployment |
| 10-14 | Alto | Piano trattamento prioritario, approvazione management |
| 5-9 | Medio | Controlli standard, monitoraggio |
| 1-4 | Basso | Accettazione possibile, monitoraggio periodico |

**Rischio Residuo Complessivo**: [ ] Basso / [ ] Medio / [ ] Alto / [ ] Critico

---

## 11. Piano di Monitoraggio

### 11.1 KPI e Metriche

| KPI | Target | Frequenza Monitoraggio | Alert Threshold |
|-----|--------|----------------------|-----------------|
| Model accuracy | >= [X]% | [Continuo/Giornaliero/Settimanale] | < [Y]% |
| Fairness metric (principale) | < [X]% diff | [Frequenza] | > [Y]% |
| Latency | < [X] ms | [Continuo] | > [Y] ms |
| Error rate | < [X]% | [Frequenza] | > [Y]% |
| Data drift score | < [X] | [Frequenza] | > [Y] |
| User complaints | < [X]/mese | [Mensile] | > [Y] |
| Override rate | [Range atteso] | [Frequenza] | [Anomalie] |

### 11.2 Processo di Review

| Tipo Review | Frequenza | Responsabile | Output |
|-------------|-----------|--------------|--------|
| Performance monitoring | Continuo | [ML Ops] | Dashboard alerts |
| Fairness audit | [Trimestrale] | [AI Ethics] | Report fairness |
| AIIA review | [Annuale o su cambiamenti] | [AI Governance] | AIIA aggiornato |
| Incident review | Post-incidente | [AI System Owner] | Root cause analysis |

### 11.3 Trigger per Re-assessment

L'AIIA deve essere rivalutato quando:
- [ ] Cambiamenti significativi al modello (retraining, nuova architettura)
- [ ] Cambio di use case o ampliamento scope
- [ ] Nuovi dati di training con caratteristiche diverse
- [ ] Incidenti significativi o near-miss
- [ ] Cambiamenti normativi rilevanti
- [ ] Feedback significativo da stakeholder
- [ ] Scadenza temporale (max 12 mesi)

---

## 12. Conclusioni e Raccomandazioni

### 12.1 Sintesi Valutazione

| Area | Livello Rischio | Trend | Note |
|------|-----------------|-------|------|
| Impatti su Individui | [B/M/A] | [↑↓→] | |
| Impatti su Gruppi/Societa | [B/M/A] | [↑↓→] | |
| Fairness | [Adeguato/Gap/Critico] | | |
| Explainability | [Alto/Medio/Basso] | | |
| Human Oversight | [Adeguato/Parziale/Insufficiente] | | |
| Rischi AI-specific | [B/M/A/Critico] | | |

### 12.2 Livello di Rischio Complessivo

**RISCHIO COMPLESSIVO**: [ ] Basso / [ ] Medio / [ ] Alto / [ ] Inaccettabile

### 12.3 Raccomandazioni Prioritarie

| # | Raccomandazione | Priorita | Owner | Deadline |
|---|-----------------|----------|-------|----------|
| 1 | [Azione prioritaria 1] | [Alta/Media/Bassa] | [Nome/Ruolo] | [Data] |
| 2 | [Azione prioritaria 2] | | | |
| 3 | [Azione prioritaria 3] | | | |
| 4 | [Azione prioritaria 4] | | | |
| 5 | [Azione prioritaria 5] | | | |

### 12.4 Condizioni per Deployment

| Condizione | Status | Note |
|------------|--------|------|
| Tutti i rischi critici mitigati | [ ] SI / [ ] NO | [Se NO, quali] |
| Fairness metrics entro threshold | [ ] SI / [ ] NO | |
| Human oversight definito | [ ] SI / [ ] NO | |
| Monitoraggio configurato | [ ] SI / [ ] NO | |
| Training operatori completato | [ ] SI / [ ] NO | |
| Documentazione completa | [ ] SI / [ ] NO | |
| Appello mechanism attivo | [ ] SI / [ ] NO | |

---

## 13. Decisione

### 13.1 Esito Assessment

- [ ] **APPROVATO** - Procedere con deployment
- [ ] **APPROVATO CON CONDIZIONI** - Deployment subordinato a:
  1. [Condizione 1]
  2. [Condizione 2]
- [ ] **RIMANDATO** - Azioni richieste prima di nuova valutazione:
  1. [Azione 1]
  2. [Azione 2]
- [ ] **RIFIUTATO** - Rischi inaccettabili. Motivazione:
  > [Motivazione dettagliata]

### 13.2 Approvazioni

| Ruolo | Nome | Firma | Data | Esito |
|-------|------|-------|------|-------|
| AI System Owner | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |
| AI Governance Lead | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |
| AI Ethics Committee | [Nome/Referente] | | [Data] | [ ] Parere positivo / [ ] Parere negativo |
| CISO | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |
| DPO | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |
| Legal | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |
| Top Management | [Nome] | | [Data] | [ ] Approvo / [ ] Non approvo |

### 13.3 Prossima Revisione

**Data Prossima Revisione Obbligatoria**: [Data - max 12 mesi]

**Trigger Revisione Anticipata**: [Elencare condizioni specifiche]

---

## 14. Documenti Correlati

| Codice | Documento | Status |
|--------|-----------|--------|
| {{company_name}}-POL-AIMS-001 | Politica AI | [Link/Riferimento] |
| {{company_name}}-INV-AIMS-001 | Inventario Sistemi AI | [Link/Riferimento] |
| {{company_name}}-MOD-[ID] | Model Card [Nome Sistema] | [Link/Riferimento] |
| {{company_name}}-DPIA-[ID] | DPIA (se applicabile) | [Link/Riferimento] |
| {{company_name}}-SEC-[ID] | Security Assessment | [Link/Riferimento] |
| | Technical Documentation | [Link/Riferimento] |
| | Test Results / Validation Report | [Link/Riferimento] |

---

## 15. Allegati

- [ ] Allegato A: Fairness Testing Report
- [ ] Allegato B: Security Assessment
- [ ] Allegato C: Technical Documentation Summary
- [ ] Allegato D: Stakeholder Consultation Records
- [ ] Allegato E: Training Records
- [ ] Allegato F: [Altro]

---

## Istruzioni per la Compilazione

> **Nota**: Questo template deve essere compilato per ogni sistema AI classificato high-risk, e raccomandato per tutti i sistemi con impatto significativo.

### Quando Compilare

- **Obbligatorio**: Prima del deployment di qualsiasi sistema high-risk EU AI Act
- **Raccomandato**: Per tutti i sistemi AI con decisioni che impattano individui
- **Review**: Almeno annualmente o su cambiamenti significativi

### Come Compilare

1. **Sezione 2-3**: Raccogliere informazioni dal team tecnico e business owner
2. **Sezione 4**: Classificazione EU AI Act - coinvolgere Legal/Compliance
3. **Sezione 5-6**: Valutazione impatti - workshop con stakeholder
4. **Sezione 7**: Fairness - dati dal team ML, metriche misurate
5. **Sezione 8**: Explainability - input dal team tecnico
6. **Sezione 9**: Human Oversight - definire con Operations
7. **Sezione 10**: Risk Assessment - sessione strutturata
8. **Sezione 11**: Piano monitoraggio - concordare con ML Ops
9. **Sezione 12-13**: Sintesi e decisione - AI Governance Lead + approvatori

### Checklist Pre-Approvazione

- [ ] Tutte le sezioni compilate (nessun placeholder [xxx] residuo)
- [ ] Classificazione EU AI Act verificata con Legal
- [ ] Fairness metrics misurate e documentate
- [ ] Human oversight mechanisms definiti e testati
- [ ] Piano monitoraggio concordato con Operations
- [ ] Tutti gli approvatori hanno firmato
- [ ] Documenti allegati disponibili

### Tips

- Coinvolgere stakeholder diversi per prospettive complete
- Documentare evidenze e fonti per ogni valutazione
- Essere onesti sui gap - meglio identificarli ora che dopo
- Usare "Medio" o "Alto" con parsimonia - giustificare sempre
- Review incrociata con AIIA di sistemi simili per consistenza

---

## Documenti Correlati

| Codice | Documento |
|--------|-----------|
| {{company_name}}-INV-AIMS-001 | AI System Inventory |
| {{company_name}}-MET-AIMS-001 | AI Risk Assessment Methodology |
| {{company_name}}-PRO-AIMS-002 | Human Oversight Procedure |
| {{company_name}}-POL-AIMS-002 | Data Governance Policy |
| {{company_name}}-MOD-[ID] | Model Card |
| {{company_name}}-CHK-EUAIA-001 | EU AI Act Compliance Checklist |

---

## Checklist di Compilazione

Prima di finalizzare il documento, verificare di aver compilato:

- [ ] Informazioni sistema AI e classificazione EU AI Act (Sez. 1-2)
- [ ] Stakeholder e impatti identificati (Sez. 3-4)
- [ ] Diritti fondamentali valutati (Sez. 5)
- [ ] Privacy e protezione dati analizzati (Sez. 6)
- [ ] Safety e sicurezza valutati (Sez. 7)
- [ ] Explainability e trasparenza documentati (Sez. 8)
- [ ] Human oversight mechanisms definiti (Sez. 9)
- [ ] Risk assessment completato (Sez. 10)
- [ ] Piano monitoraggio definito (Sez. 11)
- [ ] Sintesi e decisione documentate (Sez. 12-13)
- [ ] Tutti gli approvatori hanno firmato
- [ ] Tutti i `{{placeholder}}` sostituiti con dati reali

---

*Template fornito da Kynosure.ai - Compliance AI con intelligenza*
