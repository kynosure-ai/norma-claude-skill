---
framework: ai-act
display_name: "EU AI Act — Regulation (EU) 2024/1689"
canonical_ref: "Regulation (EU) 2024/1689"
language: it
---

The EU AI Act (Regulation 2024/1689) is the EU horizontal AI regulation classifying AI systems by risk and imposing obligations on providers, deployers, importers and distributors; this reference covers risk classification, high-risk requirements, conformity assessment, CE marking, post-market monitoring, EU Database registration, and the regulation timeline.

## Architecture

L'EU AI Act è il primo regolamento orizzontale al mondo sull'AI, in vigore dal 1° agosto 2024 con applicabilità progressiva fino al 2027. Si applica direttamente in tutti gli Stati membri UE senza necessità di recepimento.

```
REGULATION (EU) 2024/1689 - EU AI ACT

Approccio risk-based: 4 categorie
├── Unacceptable Risk (Art. 5)        → VIETATO
├── High Risk (Art. 6 + Annex III)    → Conformity assessment + CE
├── Limited Risk (Art. 50)            → Transparency obligations
└── Minimal Risk                      → No specific obligations

GPAI (General-Purpose AI Models, Art. 51-55)
├── Standard GPAI                     → Technical documentation, copyright
└── GPAI with systemic risk           → Plus: model evaluation, adversarial testing,
                                            incident reporting, cybersecurity
```

> **Nota di scope.** ISO/IEC 42001 (vedi `aims.md`) è un management-system standard; l'EU AI Act è una norma di prodotto/servizio direttamente applicabile. ISO 42001 copre ~70-80% dei requisiti AI Act, ma con gap critici su Art. 11 (technical documentation), Art. 12 (record-keeping/logs), Art. 13 (transparency to deployers), Art. 14 (human oversight), Art. 43 (conformity assessment), Art. 49 (EU Database registration) e CE marking. La conformità AI Act richiede attività incrementali rispetto a 42001.

## Risk Classification

### Practices vietate (Art. 5)

| Pratica | Esempio |
|---------|---------|
| Manipolazione subliminale o sfruttamento di vulnerabilità | Sistemi che inducono comportamenti dannosi |
| Social scoring da parte di autorità pubbliche | Punteggi sociali generalizzati |
| Categorizzazione biometrica per attributi sensibili | Inferenza di razza, opinioni politiche, religione, orientamento sessuale |
| Identificazione biometrica remota in tempo reale in spazi pubblici (con eccezioni law-enforcement strette) | RBI live in piazza |
| Predictive policing basato su profilazione individuale | Predizione reato per individuo |
| Untargeted scraping di immagini facciali da Internet/CCTV | Database facial recognition non consenti |
| Riconoscimento emozioni in workplace e scuole | Eccezioni mediche/safety |

### High-risk systems (Art. 6 + Annex III)

Un sistema è high-risk se:
- (a) è un componente di sicurezza di prodotti già coperti da legislazione UE armonizzata (es. dispositivi medici, machinery, automotive); **oppure**
- (b) è elencato in **Annex III**, che identifica 8 categorie:

| # | Categoria | Esempi |
|---|-----------|--------|
| 1 | Biometric ID & categorization | Remote biometric ID (post-event) |
| 2 | Critical infrastructure | Safety components reti elettriche, gas, acqua, traffico |
| 3 | Education & vocational training | Ammissioni, valutazione, exam-proctoring |
| 4 | Employment, workers management, self-employment access | Recruiting AI, performance evaluation, allocazione task |
| 5 | Access to & enjoyment of essential services | Credit scoring, eligibility welfare, emergency triage, life/health insurance pricing |
| 6 | Law enforcement | Risk assessment vittime, polygraph-like, evidence reliability |
| 7 | Migration, asylum, border control | Visa risk assessment, document authenticity |
| 8 | Administration of justice & democratic processes | AI per ricerca giuridica, tabulazione voti |

Dei 95 requisiti propri AI Act, 18 articoli sono mappati al cross-framework AI Act ↔ ISO 42001 nei domini governance / risk / lifecycle / data / transparency / oversight.

### Limited risk — transparency (Art. 50)

| Sistema | Obbligo |
|---------|---------|
| AI che interagisce con persone (chatbot) | Informare l'utente che sta parlando con AI |
| Riconoscimento emozioni o categorizzazione biometrica | Informare le persone esposte |
| Generative AI / deepfakes | Marchiare output generato come artificiale (esistono eccezioni artistiche/satiriche) |
| AI-generated text di rilevanza pubblica | Disclosure pubblica |

## High-Risk System Requirements (Art. 8-15)

| Articolo | Requisito |
|----------|-----------|
| Art. 9 | Risk Management System lungo l'intero lifecycle |
| Art. 10 | Data and data governance — quality, relevance, representativeness, bias mitigation, training/validation/test set documentation |
| Art. 11 | **Technical Documentation** — preparata prima dell'immissione sul mercato; mantenuta aggiornata; struttura in Annex IV |
| Art. 12 | **Record-keeping (logs)** — automatic logging delle operazioni durante l'intero lifecycle |
| Art. 13 | **Transparency to deployers** — istruzioni per l'uso, caratteristiche/limitazioni, performance, oversight, expected lifetime, maintenance |
| Art. 14 | **Human Oversight** — misure proporzionate al rischio; effective oversight by natural persons during operation |
| Art. 15 | Accuracy, robustness, cybersecurity — incluso resilience contro adversarial attacks e data poisoning |

## Conformity Assessment & CE Marking

### Conformity assessment paths (Art. 43)

| Categoria sistema | Procedura |
|-------------------|-----------|
| Annex III sistemi biometrici (categorie 1) | Notified body assessment (third-party) — Annex VII |
| Altri Annex III | Internal control con Q.M.S. — Annex VI (self-assessment), purché si applichino harmonised standards |
| Componenti di sicurezza in legislazione UE armonizzata (es. machinery, medical devices) | Procedura del relativo regolamento settoriale, integrata con AI Act requirements |

### Output conformity assessment

1. **EU Declaration of Conformity** (Art. 47) firmata dal provider — Annex V format
2. **CE marking** apposta sul prodotto/sistema (Art. 48)
3. **Registration** nell'**EU Database for High-Risk AI Systems** (Art. 49 + 71)
4. **Quality Management System** (Art. 17) operativo lungo l'intero lifecycle
5. **Post-Market Monitoring System** (Art. 72) — raccolta dati performance reali, evidenze su bias drift, incident detection

## Provider, Deployer, Importer, Distributor

| Ruolo | Obblighi chiave |
|-------|-----------------|
| **Provider** (sviluppa il sistema o lo immette sul mercato/servizio sotto il proprio nome) | Tutti gli obblighi Art. 8-21: quality/risk system, technical doc, conformity assessment, CE, registration EU Database, post-market monitoring, incident reporting |
| **Deployer** (usa il sistema sotto la propria autorità, eccetto uso personale non professionale) | Art. 26: usare il sistema secondo istruzioni provider, monitorare operazione, garantire human oversight, conservare log, informare i lavoratori se applicabile, condurre **Fundamental Rights Impact Assessment** (FRIA, Art. 27) per certi deployer pubblici / settori |
| **Importer** | Art. 23: verificare che il provider non-EU abbia eseguito la conformity, che la CE marking sia presente, che la documentation sia completa |
| **Distributor** | Art. 24: verificare CE marking, documentation, e azionare ritiro se non conforme |

## GPAI Models (Art. 51-55)

I modelli General-Purpose AI con systemic risk (impatto significativo, capacità ad alto livello — soglia indicativa: cumulative compute > 10^25 FLOPs) sono soggetti a obblighi rinforzati:

- Technical documentation completa per regulators (Art. 53.1.a + Annex XI)
- Information disclosure a downstream providers (Art. 53.1.b + Annex XII)
- Copyright compliance policy (Art. 53.1.c)
- Detailed summary of training data (Art. 53.1.d)
- Per GPAI con systemic risk (Art. 55): model evaluation, adversarial testing, incident reporting all'AI Office, cybersecurity protections

## Timeline

| Data | Milestone |
|------|-----------|
| 1° agosto 2024 | Entrata in vigore |
| **2 febbraio 2025** | Divieti pratiche unacceptable (Art. 5) + AI literacy per operatori (Art. 4) |
| **2 agosto 2025** | GPAI provisions (Art. 51-55) + governance (AI Office, AI Board, Notified Bodies designation) + penalties (Art. 99-101) |
| **2 agosto 2026** | High-risk systems Annex III — full compliance |
| **2 agosto 2027** | High-risk systems integrati in legislazione UE armonizzata (Art. 6.1.a) — full compliance |

## Penalties (Art. 99)

| Violazione | Sanzione massima |
|------------|------------------|
| Pratiche vietate (Art. 5) | €35M o 7% turnover globale annuale |
| Non-conformità altri obblighi providers/deployers/importers/distributors/notified bodies | €15M o 3% turnover |
| Informazioni inesatte/incomplete a notified bodies o autorità | €7.5M o 1% turnover |

PMI e startup beneficiano di sanzioni proporzionalmente ridotte.

## EU Database for High-Risk AI Systems (Art. 49 + 71)

Database pubblico gestito dalla Commissione UE. I provider devono registrare prima dell'immissione sul mercato:
- Identità del provider
- Trade name e specifiche identificazione del sistema AI
- Annex III categoria
- Stato dell'AI system (sul mercato / non più sul mercato)
- EU Declaration of Conformity (URL o copia)
- Notified Body certificate (se applicabile)
- Member States in cui il sistema è disponibile

Per i deployer public-authority (Art. 49.2): obbligo registrazione separata per uso di sistemi high-risk.

## Mapping to ISO/IEC 42001

| EU AI Act requisito | Clausola/controllo ISO 42001 corrispondente |
|---------------------|--------------------------------------------|
| Art. 9 Risk Management System | 6.1.2, 6.1.4, 8.2, 8.3 |
| Art. 10 Data governance | A.7 (intero dominio) |
| Art. 11 Technical Documentation | A.6.x (lifecycle), Model Cards |
| Art. 12 Logging | A.6.8, A.6.9 |
| Art. 13 Transparency to deployers | A.8.3, A.8.4 |
| Art. 14 Human Oversight | A.9.3 |
| Art. 15 Accuracy / Robustness / Cybersecurity | A.6.6 (V&V), integrazione con ISO 27001 |
| Quality Management System (Art. 17) | AIMS completo |
| Post-Market Monitoring (Art. 72) | A.6.9 + 9.1 |

I gap che 42001 NON copre e che richiedono attività AI-Act-specifica:
- Conformity assessment formale (Art. 43)
- CE marking
- EU Database registration (Art. 49)
- Notified Body engagement (per certe categorie)
- Fundamental Rights Impact Assessment (Art. 27, deployer)
- GPAI-specific obligations (Art. 51-55)

## Implementation Notes

- L'autoclassificazione è il primo gate: senza una mappatura fra i sistemi AI dell'organizzazione e Annex III + Art. 5 + Art. 50, l'organizzazione non può sapere quali obblighi le si applicano. Questa mappatura è prerequisito di ogni altro lavoro.
- Le PMI possono usare Annex VI (internal control) se si applicano harmonised standards, con costi inferiori al notified-body assessment; la Commissione e CEN-CENELEC stanno pubblicando harmonised standards (es. EN ISO/IEC 42001 atteso) per supportare questo path.
- Il confine fra Provider e Deployer va presidiato contrattualmente: se un'organizzazione integra un GPAI in un proprio prodotto e lo immette sul mercato sotto il proprio nome, diventa Provider per quel prodotto e assume gli obblighi corrispondenti.
- Il post-market monitoring (Art. 72) chiude il loop: è il meccanismo che fa diventare la conformità un processo continuo invece di un evento di certificazione.
- AI literacy (Art. 4) è già applicabile dal 2 febbraio 2025 e si applica a tutti gli operatori, non solo high-risk: tutti i providers e deployers devono garantire un livello sufficiente di AI literacy del personale che opera o usa sistemi AI.

## References

- Regulation (EU) 2024/1689 — Artificial Intelligence Act
- Annex I (Union harmonisation legislation), II, III, IV (Technical Documentation), V (EU Declaration of Conformity), VI/VII (Conformity Assessment), VIII (registration), XI/XII (GPAI documentation)
- AI Office (DG CONNECT) and AI Board guidance
- EU Database for High-Risk AI Systems (in via di pubblicazione)
- Per il management-system layer: vedi `aims.md` (ISO/IEC 42001:2023)
- ENISA AI threat landscape reports
