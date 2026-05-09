---
framework: aims
display_name: "ISO/IEC 42001:2023 — AI Management System"
canonical_ref: "ISO/IEC 42001:2023"
language: it
---

ISO/IEC 42001:2023 is the first international management-system standard for Artificial Intelligence; this reference covers Clauses 4-10 and the 38 Annex A controls organised in 9 domains, with the documented information set required for AIMS implementation.

## Architecture

ISO/IEC 42001:2023 (pubblicato Dicembre 2023) è il primo standard di sistema di gestione dedicato all'AI. La struttura è basata sulla High Level Structure (HLS) condivisa con ISO 27001 e ISO 9001, integrata con un Annex A AI-specifico.

```
ISO/IEC 42001:2023

Struttura:
├── Clausole 4-10: Requisiti HLS (High Level Structure)
├── Annex A: 38 Controlli AI in 9 domini
├── Annex B: Guida implementazione controlli
├── Annex C: Rischi AI specifici
└── Annex D: Uso AI per domini applicativi

Integrazioni:
├── EU AI Act (vedi reference ai-act.md — framework distinto)
├── ISO/IEC 27001 (Information Security)
├── ISO 9001 (Quality Management)
└── NIST AI Risk Management Framework
```

> **Nota di fedeltà metodologica.** ISO 42001 e EU AI Act sono framework distinti. ISO 42001 copre ~70-80% dei requisiti EU AI Act, con gap critici su Art. 11 (technical documentation), Art. 12 (record-keeping), Art. 13 (transparency to deployers), Art. 14 (human oversight), Art. 43 (conformity assessment) e CE marking / EU Database registration. Per la conformità EU AI Act consultare il reference dedicato `ai-act.md`.

### Clausole HLS con focus AI

```
Clausola 4: Contesto dell'Organizzazione
├── 4.1 Comprendere organizzazione e contesto → include AI landscape
├── 4.2 Parti interessate → stakeholder AI-specifici
├── 4.3 Ambito AIMS → inventario sistemi AI
└── 4.4 AIMS → Plan-Do-Check-Act per AI

Clausola 5: Leadership
├── 5.1 Leadership e impegno → commitment responsible AI
├── 5.2 AI Policy (obbligatorio) → principi responsible AI
└── 5.3 Ruoli e responsabilità → AI governance structure

Clausola 6: Pianificazione
├── 6.1 Rischi e opportunità
│   ├── 6.1.1 Generale
│   ├── 6.1.2 Valutazione rischi AI
│   ├── 6.1.3 AI Impact Assessment (obbligatorio)
│   └── 6.1.4 Trattamento rischi AI
└── 6.2 Obiettivi AI e pianificazione

Clausola 7: Supporto
├── 7.1 Risorse → risorse AI-specifiche
├── 7.2 Competenze → AI literacy, ML expertise
├── 7.3 Consapevolezza → AI awareness organization-wide
├── 7.4 Comunicazione → trasparenza AI
└── 7.5 Informazioni documentate → documentazione AI lifecycle

Clausola 8: Attività Operative
├── 8.1 Pianificazione e controllo operativo
├── 8.2 AI Risk Assessment (obbligatorio)
├── 8.3 AI Risk Treatment
└── 8.4 AI System Lifecycle (CORE)
    ├── Design & Development
    ├── Verification & Validation
    ├── Deployment
    ├── Operation & Monitoring
    └── Retirement

Clausola 9: Valutazione Prestazioni
├── 9.1 Monitoraggio e misurazione → AI performance metrics
├── 9.2 Audit interno → AIMS audit
└── 9.3 Riesame direzione → AI governance review

Clausola 10: Miglioramento
├── 10.1 Non conformità e azioni correttive → AI incidents
└── 10.2 Miglioramento continuo → AI system enhancement
```

## Annex A — 38 Controls in 9 Domains

### A.2 Policies for AI
- A.2.2 AI Policy definita da top management
- A.2.3 Review periodica AI policy
- A.2.4 AI policy allineata con obiettivi business

### A.3 Internal Organization
- A.3.2 Ruoli e responsabilità AI definiti
- A.3.3 Segregazione compiti AI
- A.3.4 Reporting AI a management

### A.4 Resources for AI Systems
- A.4.2 Inventario asset AI (sistemi, modelli, dati)
- A.4.3 Risorse computazionali AI
- A.4.4 Risorse umane AI (competenze, training)
- A.4.5 Risorse dati AI (datasets, data governance)
- A.4.6 Strumenti e tooling AI
- A.4.7 Fornitori e partner AI

### A.5 Assessing Impacts of AI Systems
- A.5.2 AI system impact assessment methodology
- A.5.3 Valutazione impatti individui
- A.5.4 Valutazione impatti gruppi/società
- A.5.5 Documentazione impatti
- A.5.6 Comunicazione impatti a stakeholder

### A.6 AI System Lifecycle
- A.6.2 Lifecycle stages definiti
- A.6.3 Design requirements
- A.6.4 Data requirements (qualità, provenienza)
- A.6.5 Model development requirements
- A.6.6 Verification and validation (testing)
- A.6.7 Deployment requirements
- A.6.8 Operation requirements
- A.6.9 Monitoring requirements (drift, bias)
- A.6.10 Retirement / decommissioning

### A.7 Data for AI Systems
- A.7.2 Data quality requirements
- A.7.3 Data acquisition procedures
- A.7.4 Data preparation (labeling, cleaning)
- A.7.5 Data provenance tracking
- A.7.6 Data bias assessment
- A.7.7 Data protection and privacy

### A.8 Information for Interested Parties
- A.8.2 Informazioni su sistemi AI per stakeholder
- A.8.3 Trasparenza decisioni AI
- A.8.4 Explainability outputs AI
- A.8.5 Canali reporting problemi AI

### A.9 Use of AI Systems
- A.9.2 Acceptable use policy AI
- A.9.3 Human oversight mechanisms
- A.9.4 User training for AI systems
- A.9.5 Monitoraggio uso appropriato

### A.10 Third-Party and Customer Relationships
- A.10.2 Valutazione fornitori AI
- A.10.3 Accordi contrattuali AI
- A.10.4 Monitoraggio fornitori AI
- A.10.5 Responsabilità verso clienti AI

## Mandatory Documented Information

### Tier 1 — Documenti core

| ID | Documento | Clausola |
|----|-----------|----------|
| D01 | Scope AIMS | 4.3 |
| D02 | AI Policy | 5.2 |
| D03 | Ruoli e responsabilità AI | 5.3 |
| D04 | AI Risk Assessment Methodology | 6.1.2 |
| D05 | AI Risk Assessment Results | 8.2 |
| D06 | AI Impact Assessment (AIIA) | 6.1.3 |
| D07 | AI Risk Treatment Plan | 6.1.4, 8.3 |
| D08 | Statement of Applicability (SoA) — 38 controlli Annex A | 6.1.4 |
| D09 | AI System Inventory | A.4.2 |

### Tier 2 — Documenti lifecycle

| ID | Documento | Controllo |
|----|-----------|-----------|
| D10 | AI System Requirements | A.6.3 |
| D11 | Data Quality Requirements | A.7.2 |
| D12 | Model Cards | A.6.x |
| D13 | Verification & Validation Reports | A.6.6 |
| D14 | Deployment Checklist | A.6.7 |
| D15 | Monitoring Plan | A.6.9 |
| D16 | Decommissioning Procedure | A.6.10 |

### Tier 3 — Evidenze operative

| ID | Documento | Clausola |
|----|-----------|----------|
| D17 | Competence Records | 7.2 |
| D18 | AI Awareness Training | 7.3 |
| D19 | Internal Audit Programme | 9.2 |
| D20 | Audit Results | 9.2 |
| D21 | Management Review Minutes | 9.3 |
| D22 | NC e Corrective Actions | 10.1 |

### Tier 4 — Policy e procedure

| ID | Documento | Controllo |
|----|-----------|-----------|
| P01 | Data Governance Policy | A.7 |
| P02 | AI Ethics Guidelines | A.5, A.8 |
| P03 | Human Oversight Procedure | A.9.3 |
| P04 | AI Incident Response | 10.1 |
| P05 | Supplier AI Assessment | A.10.2-4 |
| P06 | Acceptable Use Policy AI | A.9.2 |
| P07 | Transparency & Explainability Guide | A.8.3-4 |
| P08 | Bias Detection & Mitigation | A.7.6 |

## AI Risk Assessment — Framework

### Categorie di rischio AI (da Annex C)

| Categoria | Esempi | Impatto |
|-----------|--------|---------|
| Bias & Fairness | Discriminazione algoritmica, dataset sbilanciati | Individui, gruppi |
| Safety & Reliability | Malfunzionamenti, output errati | Sicurezza utenti |
| Security | Adversarial attacks, data poisoning, model theft | Organizzazione, utenti |
| Privacy | Re-identification, inference attacks | Data subjects |
| Transparency | Black-box decisions, mancanza explainability | Fiducia, compliance |
| Accountability | Responsabilità indefinite, audit trail assenti | Governance, legale |
| Environmental | Consumo energetico training, carbon footprint | Società |

### Scala probabilità (AI-specific)

| Livello | Valore | Descrizione |
|---------|--------|-------------|
| Raro | 1 | Richiede expertise avanzata, no precedenti |
| Improbabile | 2 | Possibile ma richiede risorse significative |
| Possibile | 3 | Documentato in letteratura, strumenti disponibili |
| Probabile | 4 | Attacchi noti, exploit pubblici |
| Quasi Certo | 5 | Accade regolarmente, facile da replicare |

### Scala impatto (AI-specific)

| Livello | Valore | Individui | Organizzazione | Società |
|---------|--------|-----------|----------------|---------|
| Trascurabile | 1 | Nessun danno | Impatto minimo | N/A |
| Minore | 2 | Inconveniente | Perdita limitata | N/A |
| Moderato | 3 | Danno reversibile | Perdita significativa | Impatto locale |
| Significativo | 4 | Danno grave | Perdita critica | Impatto ampio |
| Catastrofico | 5 | Pericolo vita | Fallimento business | Impatto sistemico |

### Matrice di rischio

| | Impatto 1 | 2 | 3 | 4 | 5 |
|-|-----------|---|---|---|---|
| Probabilità 5 | 5 | 10 | 15 | 20 | 25 |
| 4 | 4 | 8 | 12 | 16 | 20 |
| 3 | 3 | 6 | 9 | 12 | 15 |
| 2 | 2 | 4 | 6 | 8 | 10 |
| 1 | 1 | 2 | 3 | 4 | 5 |

| Score | Livello | Azione |
|-------|---------|--------|
| ≥ 15 | Critico | Mitigazione immediata o stop |
| 10-14 | Alto | Piano trattamento prioritario |
| 5-9 | Medio | Controlli standard |
| 1-4 | Basso | Monitor; accettazione possibile |

### Opzioni di trattamento

| Opzione | Quando usarla | Esempio |
|---------|---------------|---------|
| Mitigare | Rischio riducibile con controlli | Implementare fairness testing |
| Trasferire | Assicurabile / esternalizzabile | AI insurance, vendor managed service |
| Evitare | Rischio inaccettabile | Non deployare il sistema |
| Accettare | Rischio basso, costo mitigazione > beneficio | Documentare il rationale |

## AI Impact Assessment (AIIA) — Outline

L'AIIA è obbligatoria per sistemi AI ad alto impatto. Il template canonico include:

1. **Sistema info & classificazione di rischio** — nome, ID, owner, tipo AI (ML/NLP/CV/GenAI), modello, dataset, output, utenti, parti impattate.
2. **Stakeholder analysis** — utenti finali, data subjects, dipendenti, regolatori, società.
3. **Necessità AIIA** — checklist criteri high-risk (biometric ID, infrastrutture critiche, education, employment, essential services, law enforcement, migration, justice).
4. **Impact assessment su individui** — autonomia, dignità, privacy, non-discriminazione, sicurezza.
5. **Impact assessment su gruppi/società** — bias sistemico, concentrazione potere, mercato lavoro, ambiente.
6. **Fairness assessment** — demographic parity, equalized odds, predictive parity, individual fairness; analisi gruppi protetti.
7. **Explainability assessment** — interpretabilità modello, feature importance, decision explanations, audit trail, counterfactuals.
8. **Human oversight** — human-in-the-loop, on-the-loop, in-command; appeal mechanism.
9. **Conclusioni & raccomandazioni** — risk level complessivo, decisione (approvato / con condizioni / rimandato / rifiutato), approvazioni, prossima review (max 12 mesi).

## Model Card — Outline

Per ogni modello in scope: overview (model ID, version, owner, status), model details (type, architecture, framework, size), intended use (primary use case, intended users, out-of-scope uses), training data (dataset, size, time period, geographic coverage, demographics, known limitations), evaluation data, performance metrics (accuracy, precision, recall, F1, AUC-ROC), fairness metrics per gruppo, limitations & risks, ethical considerations, caveats & recommendations, maintenance (retraining frequency, monitoring, drift detection, owner contact).

## Implementation Notes

- Il commitment del top management su responsible AI è la condizione abilitante; senza AI Policy approvata, l'AIMS non parte.
- L'AI System Inventory (A.4.2) è il fondamento di ogni altro controllo — prima di valutare rischi e impatti, l'organizzazione deve sapere quali sistemi AI esegue, in quale fase di lifecycle, su quali dati e per quali decisioni.
- Per organizzazioni che già operano un ISMS ISO 27001, l'AIMS si integra naturalmente come estensione: la stessa governance, lo stesso ciclo di audit, gli stessi processi di management review possono coprire entrambi i sistemi di gestione, con documentazione AIMS-specifica per le clausole AI-only.
- Il confine fra ISO 42001 e EU AI Act va presidiato esplicitamente: la conformità a 42001 non implica conformità all'AI Act per i sistemi high-risk. Un'organizzazione che opera sistemi in Annex III AI Act deve coprire entrambi e usare ISO 42001 come base, EU AI Act come integrazione obbligatoria (tecnologie regolate, conformity assessment, CE marking, EU Database).

## References

- ISO/IEC 42001:2023 — Artificial intelligence — Management system
- NIST AI Risk Management Framework (AI RMF 1.0)
- IEEE 7000-2021 — Model Process for Addressing Ethical Concerns During System Design
- OECD AI Principles
- UNESCO Recommendation on the Ethics of Artificial Intelligence
- Per EU AI Act: vedi `ai-act.md` (framework distinto)
