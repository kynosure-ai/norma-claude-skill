---
framework: isms
display_name: "ISO/IEC 27001:2022 — Information Security Management System"
canonical_ref: "ISO/IEC 27001:2022"
language: it
---

ISO/IEC 27001:2022 is the international standard for Information Security Management Systems; this reference covers Clauses 4-10 (HLS) and the 93 Annex A controls in 4 categories, plus the documented information set required for certification.

## Architecture

ISO/IEC 27001:2022 specifica i requisiti per stabilire, implementare, mantenere e migliorare in continuo un Information Security Management System (ISMS). La struttura segue la High Level Structure condivisa con tutti i management-system standards (ISO 9001, 22301, 42001, 27701).

### Clausole HLS

```
Clausola 4: Contesto dell'Organizzazione
├── 4.1 Comprendere l'organizzazione e il suo contesto
├── 4.2 Comprendere le esigenze delle parti interessate
├── 4.3 Determinare l'ambito dell'ISMS
└── 4.4 ISMS

Clausola 5: Leadership
├── 5.1 Leadership e impegno
├── 5.2 Politica (obbligatorio)
└── 5.3 Ruoli, responsabilità e autorità

Clausola 6: Pianificazione
├── 6.1 Azioni per affrontare rischi e opportunità
│   ├── 6.1.2 Valutazione rischio (obbligatorio)
│   └── 6.1.3 Trattamento rischio (obbligatorio)
├── 6.2 Obiettivi e pianificazione
└── 6.3 Pianificazione modifiche (nuovo 2022)

Clausola 7: Supporto
├── 7.1 Risorse
├── 7.2 Competenze (evidenze richieste)
├── 7.3 Consapevolezza
├── 7.4 Comunicazione
└── 7.5 Informazioni documentate

Clausola 8: Attività operative
├── 8.1 Pianificazione e controllo
├── 8.2 Valutazione rischio (obbligatorio)
└── 8.3 Trattamento rischio (obbligatorio)

Clausola 9: Valutazione prestazioni
├── 9.1 Monitoraggio, misurazione, analisi (obbligatorio)
├── 9.2 Audit interno (obbligatorio)
└── 9.3 Riesame della direzione (obbligatorio)

Clausola 10: Miglioramento
├── 10.1 Non conformità e azioni correttive (obbligatorio)
└── 10.2 Miglioramento continuo
```

## Annex A — 93 Controls in 4 Categories

La revisione 2022 riorganizza i controlli da 14 domini (2013) a 4 macrocategorie. Sono **11 i controlli new in 2022**, marcati nell'elenco. I controlli sono ora etichettati anche con 5 attributi (Type, IS Properties, Cybersecurity Concepts, Operational Capabilities, Security Domains) per facilitare filtering e mapping.

### A.5 Organizational Controls (37)
A.5.1 Politiche di sicurezza · A.5.2 Ruoli e responsabilità · A.5.3 Separazione dei compiti · A.5.4 Responsabilità della direzione · A.5.5 Contatto con le autorità · A.5.6 Contatto con gruppi specialistici · **A.5.7 Threat intelligence (NEW)** · A.5.8 Sicurezza nei progetti · A.5.9 Inventario asset · A.5.10 Uso accettabile · A.5.11 Restituzione asset · A.5.12 Classificazione · A.5.13 Etichettatura · A.5.14 Trasferimento informazioni · A.5.15 Controllo accessi · A.5.16 Gestione identità · A.5.17 Informazioni di autenticazione · A.5.18 Diritti di accesso · A.5.19 Sicurezza fornitori · A.5.20 Sicurezza accordi fornitori · **A.5.21 ICT supply chain (NEW)** · A.5.22 Monitoraggio fornitori · **A.5.23 Cloud security (NEW)** · A.5.24 Pianificazione gestione incidenti · A.5.25 Valutazione eventi · A.5.26 Risposta incidenti · A.5.27 Apprendimento da incidenti · A.5.28 Raccolta evidenze · A.5.29 Sicurezza durante interruzioni · **A.5.30 ICT readiness for business continuity (NEW)** · A.5.31 Requisiti legali e contrattuali · A.5.32 Proprietà intellettuale · A.5.33 Protezione record · A.5.34 Privacy e PII · A.5.35 Revisione indipendente sicurezza · A.5.36 Conformità a politiche · A.5.37 Procedure operative documentate.

### A.6 People Controls (8)
A.6.1 Screening · A.6.2 Termini e condizioni · A.6.3 Awareness e formazione · A.6.4 Processo disciplinare · A.6.5 Responsabilità cessazione/cambio · A.6.6 Accordi di riservatezza · **A.6.7 Lavoro remoto (NEW)** · A.6.8 Segnalazione eventi.

### A.7 Physical Controls (14)
A.7.1 Perimetri sicurezza fisica · A.7.2 Controlli ingresso fisico · A.7.3 Sicurezza uffici/strutture · **A.7.4 Monitoraggio sicurezza fisica (NEW)** · A.7.5 Protezione minacce ambientali · A.7.6 Lavoro in aree sicure · A.7.7 Scrivania/schermo puliti · A.7.8 Posizionamento apparecchiature · A.7.9 Asset fuori sede · A.7.10 Supporti di memorizzazione · A.7.11 Servizi di supporto · A.7.12 Sicurezza cablaggio · A.7.13 Manutenzione apparecchiature · A.7.14 Dismissione sicura.

### A.8 Technological Controls (34)
A.8.1 Dispositivi endpoint · A.8.2 Accessi privilegiati · A.8.3 Restrizione accesso informazioni · A.8.4 Accesso codice sorgente · A.8.5 Autenticazione sicura · A.8.6 Gestione capacità · A.8.7 Protezione malware · A.8.8 Vulnerability management · **A.8.9 Configuration management (NEW)** · **A.8.10 Cancellazione informazioni (NEW)** · **A.8.11 Data masking (NEW)** · **A.8.12 Data leakage prevention (NEW)** · A.8.13 Backup · A.8.14 Ridondanza · A.8.15 Logging · **A.8.16 Monitoring activities (NEW)** · A.8.17 Sincronizzazione orologi · A.8.18 Uso utility privilegiate · A.8.19 Installazione software · A.8.20 Sicurezza reti · A.8.21 Sicurezza servizi di rete · A.8.22 Segregazione reti · **A.8.23 Web filtering (NEW)** · A.8.24 Crittografia · A.8.25 Sviluppo sicuro lifecycle · A.8.26 Requisiti sicurezza applicazioni · A.8.27 Architettura sicura · **A.8.28 Codifica sicura (NEW)** · A.8.29 Test sicurezza · A.8.30 Sviluppo in outsourcing · A.8.31 Separazione ambienti · A.8.32 Change management · A.8.33 Dati di test · A.8.34 Protezione sistemi audit.

## Mandatory Documented Information

### Tier 1 — documenti core

| ID | Documento | Clausola | Note |
|----|-----------|----------|------|
| D01 | Scope ISMS | 4.3 | Compare sul certificato |
| D02 | Information Security Policy | 5.2 | Approvata dal top management |
| D03 | Risk Assessment Methodology | 6.1.2 | Criteri, scala, ownership |
| D04 | Risk Assessment Results | 8.2 | Registro rischi vivo |
| D05 | Risk Treatment Plan | 6.1.3, 8.3 | Azioni, responsabili, timeline |
| D06 | Statement of Applicability (SoA) | 6.1.3(d) | 93 controlli con giustificazioni |
| D07 | Obiettivi di sicurezza | 6.2 | SMART, misurabili |

### Tier 2 — evidenze operative (per audit)

| ID | Documento | Clausola |
|----|-----------|----------|
| D08 | Competence Records | 7.2 |
| D09 | Monitoring Results | 9.1 |
| D10 | Internal Audit Programme | 9.2 |
| D11 | Internal Audit Results | 9.2 |
| D12 | Management Review Minutes | 9.3 |
| D13 | Nonconformity Records | 10.1 |
| D14 | Corrective Action Results | 10.1 |

### Tier 3 — policy e procedure derivate dall'Annex A

| ID | Documento | Controllo Annex A |
|----|-----------|-------------------|
| P01 | Access Control Policy | A.5.15-18 |
| P02 | Asset Inventory | A.5.9 |
| P03 | Acceptable Use Policy | A.5.10 |
| P04 | Classification Policy | A.5.12-13 |
| P05 | Supplier Security Policy | A.5.19-23 |
| P06 | Incident Management Procedure | A.5.24-28 |
| P07 | Business Continuity / ICT Readiness | A.5.29-30 |
| P08 | Backup Policy | A.8.13 |
| P09 | Secure Development Policy | A.8.25-31 |
| P10 | Remote Working Policy | A.6.7 |

## Risk Assessment Methodology

### Scala probabilità

| Livello | Valore | Descrizione |
|---------|--------|-------------|
| Molto bassa | 1 | < 10% in 1 anno; mai accaduto |
| Bassa | 2 | 10-30%; potrebbe accadere |
| Media | 3 | 30-60%; già accaduto nel settore |
| Alta | 4 | 60-90%; accaduto nell'organizzazione |
| Molto alta | 5 | > 90%; accade regolarmente |

### Scala impatto

| Livello | Valore | Confidenzialità | Integrità | Disponibilità |
|---------|--------|-----------------|-----------|---------------|
| Trascurabile | 1 | No dati sensibili | Correggibile | < 1 ora |
| Basso | 2 | Dati interni | Ripristinabile | < 4 ore |
| Medio | 3 | Dati clienti limitati | Perdita parziale | < 1 giorno |
| Alto | 4 | Dati sensibili | Perdita significativa | < 1 settimana |
| Critico | 5 | Breach massivo | Irreversibile | > 1 settimana |

### Matrice di rischio

```
        Impatto →
Prob.    1    2    3    4    5
  ↓
  5      5   10   15   20   25  ← Critico (≥ 15)
  4      4    8   12   16   20  ← Alto (10-14)
  3      3    6    9   12   15  ← Medio (5-9)
  2      2    4    6    8   10  ← Basso (2-4)
  1      1    2    3    4    5  ← Accettabile (1)
```

### Opzioni di trattamento

| Opzione | Quando usarla |
|---------|---------------|
| Mitigare | Rischio riducibile con controlli |
| Trasferire | Assicurazione, outsourcing |
| Evitare | Cessare l'attività rischiosa |
| Accettare | Rischio ≤ soglia, giustificare |

## Statement of Applicability (SoA)

Lo SoA è il documento di sintesi dell'ISMS e mappa ognuno dei 93 controlli Annex A indicando applicabilità, stato, giustificazione, owner e collegamento al risk register.

```
| # | Controllo | Nome | Applicabile | Stato | Giustificazione | Owner | Rif. Rischio |
|---|-----------|------|-------------|-------|-----------------|-------|--------------|
| A.5.1 | Politiche sicurezza | SI | Implementato | Richiesto da ISMS | CISO | R-001 |
| A.5.7 | Threat intelligence | NO | N/A | Risorse non dedicate (PMI) | - | - |
```

Stati di implementazione: **Implementato** (operativo e monitorato), **Parzialmente** (in corso, alcune lacune), **Pianificato** (nel Risk Treatment Plan), **N/A** (non applicabile, giustificare sempre).

## SME Implementation Notes

### Timeline indicativa (PMI)

| Fase | Durata |
|------|--------|
| Gap analysis | 2-4 settimane |
| Documentazione core | 4-8 settimane |
| Risk assessment | 2-4 settimane |
| SoA + Treatment Plan | 2-4 settimane |
| Implementazione controlli | 8-16 settimane |
| Audit interno | 1-2 settimane |
| Stage 1 audit (documentation review) | 1 settimana |
| Stage 2 audit (operational) | 1-2 settimane |

### Quick wins

1. Information Security Policy (1-2 pagine strategiche, approvata dal CEO)
2. Asset inventory (anche solo Excel, ma vivo)
3. Risk assessment via workshop facilitato
4. Review degli account esistenti (privilege creep, leavers)
5. Test restore di un backup (controllo concreto, non solo procedurale)
6. Awareness training di 1 ora a tutto il personale

### Errori comuni da evitare

- SoA generico senza giustificazioni specifiche per controllo
- Risk assessment annuale senza trigger di revisione (M&A, breach, nuovi sistemi)
- Policy troppo lunghe che nessuno legge
- Controlli "sulla carta" non verificati operativamente
- Mancanza di evidenze (log, verbali, report) — il certificatore chiede prove

## Implementation Notes

- Lo Scope (4.3) determina cosa entra e cosa esce dall'ISMS, e per estensione dal certificato. Definirlo male all'inizio costa caro al primo audit di sorveglianza.
- Annex A è una baseline, non una checklist obbligatoria. Lo SoA è il documento dove si motiva ogni esclusione: il principio cardine è "applicare ciò che il rischio richiede".
- I controlli new-2022 (threat intelligence, ICT supply chain, cloud, ICT readiness, configuration mgmt, info deletion, data masking, DLP, monitoring, web filtering, secure coding) riflettono il panorama post-2013 e sono quelli su cui i certificatori concentrano l'attenzione nelle re-certificazioni dal vecchio standard.
- Per organizzazioni che già operano un BCMS (ISO 22301), un PIMS (ISO 27701), un AIMS (ISO 42001) o un QMS (ISO 9001), il Management Review (9.3) e l'Internal Audit Programme (9.2) possono essere integrati su un unico ciclo per ridurre il sovraccarico amministrativo.

## References

- ISO/IEC 27001:2022 — Information security, cybersecurity and privacy protection — Information security management systems — Requirements
- ISO/IEC 27002:2022 — Information security controls (guidance per Annex A)
- ISO/IEC 27005 — Information security risk management
- ISO/IEC 27017 (Cloud) e ISO/IEC 27018 (PII in cloud) come complementari
