---
framework: bcms
display_name: "ISO 22301:2019 — Business Continuity Management System"
canonical_ref: "ISO 22301:2019"
language: it
---

ISO 22301:2019 is the international standard for Business Continuity Management Systems; this reference covers Clauses 4-10, the BIA & risk-assessment framework, the Business Continuity Plan structure, exercise programmes, and the documented information set required for certification.

## Architecture

ISO 22301:2019 specifica i requisiti per stabilire, implementare, mantenere e migliorare un Business Continuity Management System (BCMS), con l'obiettivo di proteggere l'organizzazione da disruption, ridurre la probabilità che si verifichino e assicurare il recovery dei processi critici nei tempi target. Adotta la High Level Structure (HLS).

### Clausole HLS

```
Clausola 4: Contesto dell'Organizzazione
├── 4.1 Comprendere l'organizzazione e il suo contesto
├── 4.2 Esigenze parti interessate
│   └── 4.2.2 Requisiti legali e regolamentari (obbligatorio)
├── 4.3 Determinare l'ambito BCMS (obbligatorio)
└── 4.4 Sistema di gestione continuità operativa

Clausola 5: Leadership
├── 5.1 Leadership e impegno
├── 5.2 Politica (obbligatorio)
└── 5.3 Ruoli, responsabilità e autorità

Clausola 6: Pianificazione
├── 6.1 Azioni per affrontare rischi e opportunità
├── 6.2 Obiettivi continuità e piani (obbligatorio)
└── 6.3 Pianificazione modifiche

Clausola 7: Supporto
├── 7.1 Risorse
├── 7.2 Competenze (obbligatorio - evidenze)
├── 7.3 Consapevolezza
├── 7.4 Comunicazione
└── 7.5 Informazioni documentate

Clausola 8: Attività Operative (CORE)
├── 8.1 Pianificazione e controllo operativo
├── 8.2 Business Impact Analysis e Risk Assessment
│   ├── 8.2.2 BIA (obbligatorio)
│   └── 8.2.3 Risk Assessment (obbligatorio)
├── 8.3 Strategie e soluzioni
│   ├── 8.3.2 Determinare strategie
│   └── 8.3.3 Soluzioni continuità (obbligatorio)
├── 8.4 Piani e procedure
│   ├── 8.4.2 Struttura risposta
│   ├── 8.4.3 Warning e comunicazione (obbligatorio)
│   ├── 8.4.4 Business Continuity Plans (obbligatorio)
│   └── 8.4.5 Recovery
└── 8.5 Esercitazioni e test (obbligatorio)

Clausola 9: Valutazione prestazioni
├── 9.1 Monitoraggio e misurazione (obbligatorio)
├── 9.2 Audit interno (obbligatorio)
└── 9.3 Riesame della direzione (obbligatorio)

Clausola 10: Miglioramento
├── 10.1 Non conformità e azioni correttive (obbligatorio)
└── 10.2 Miglioramento continuo
```

## Mandatory Documented Information

### Tier 1 — documenti core

| ID | Documento | Clausola |
|----|-----------|----------|
| D01 | Scope BCMS | 4.3 |
| D02 | Lista requisiti legali / regolamentari | 4.2.2 |
| D03 | Business Continuity Policy | 5.2 |
| D04 | Obiettivi BC e piani | 6.2 |
| D05 | Business Impact Analysis (BIA) | 8.2.2 |
| D06 | Risk Assessment Results | 8.2.3 |
| D07 | Strategie e soluzioni BC | 8.3.3 |
| D08 | Procedure di comunicazione e warning | 8.4.3 |
| D09 | Business Continuity Plans | 8.4.4 |

### Tier 2 — evidenze operative

| ID | Documento | Clausola |
|----|-----------|----------|
| D10 | Competence Records | 7.2 |
| D11 | Programme di esercitazioni | 8.5 |
| D12 | Risultati esercitazioni | 8.5 |
| D13 | Monitoring Results | 9.1 |
| D14 | Internal Audit Programme + risultati | 9.2 |
| D15 | Management Review Minutes | 9.3 |
| D16 | NC e Corrective Actions | 10.1 |

### Tier 3 — piani e procedure operative

| ID | Documento |
|----|-----------|
| P01 | Crisis Management Plan |
| P02 | IT Disaster Recovery Plan |
| P03 | Emergency Response Plan |
| P04 | Communication Plan |
| P05 | Supplier Continuity Plan |
| P06 | Workplace Recovery Plan |
| P07 | Staff Welfare Plan |

## Business Impact Analysis (BIA) — Framework

La BIA è la pietra angolare del BCMS: identifica i processi critici, li ordina per criticità, definisce le metriche di recovery (RTO/RPO/MTPD/MBCO) e le risorse minime necessarie.

### Step 1 — Identificazione processi e impatti per timeframe

Per ogni processo critico, descrivere owner, dipendenze interne ed esterne, e quantificare l'impatto dell'interruzione lungo dimensioni finanziarie, operative, reputazionali e legali, su scaglioni temporali tipici (0-4 ore, 4-24 ore, 1-3 giorni, 3-7 giorni, > 7 giorni).

### Step 2 — Metriche di recovery

| Metrica | Sigla | Definizione | Come calcolarla |
|---------|-------|-------------|------------------|
| Maximum Tolerable Period of Disruption | MTPD / MAO | Tempo massimo tollerabile prima di danni irreversibili | Analisi impatti finanziari, legali, reputazionali |
| Recovery Time Objective | RTO | Tempo target per ripristinare il processo | RTO ≤ MTPD (con margine di sicurezza) |
| Recovery Point Objective | RPO | Quantità massima di dati / transazioni che si possono perdere | Analisi backup frequency vs valore dati |
| Minimum Business Continuity Objective | MBCO | Livello minimo di servizio accettabile durante la crisi | % capacità normale richiesta |

### Step 3 — Risorse critiche per processo

Per ogni processo: personale (ruoli, N minimo, cross-training), IT systems (componenti, DR site), dati (recovery point, backup location), facilities (siti alternativi, postazioni), equipment (fornitori backup), fornitori (SLA, alternative).

### Step 4 — Output BIA consigliato

```
| # | Processo | Criticità | MTPD | RTO | RPO | MBCO | Risorse Chiave |
|---|----------|-----------|------|-----|-----|------|-----------------|
| 1 | Vendite online | Critico | 4h | 2h | 15min | 50% | ERP, sito, team vendite |
| 2 | Produzione | Alto | 24h | 8h | 4h | 30% | Impianto, materie prime |
| 3 | HR/Payroll | Medio | 7gg | 3gg | 24h | N/A | Sistema paghe |
```

## Business Continuity Plan — Outline

Un BCP è un documento operativo che assume di essere letto in mezzo a una crisi. La struttura canonica include:

1. **Informazioni generali** — scopo, ambito, distribuzione, storico revisioni.
2. **Governance BC** — struttura organizzativa di crisi, ruoli e responsabilità, autorità e delega, escalation matrix.
3. **Attivazione del piano** — trigger eventi, criteri di attivazione, chi può attivare, procedura di dichiarazione di crisi.
4. **Team di risposta** — Crisis Management Team (CMT), Emergency Response Team, IT Recovery Team, Communications Team, Business Recovery Team — ognuno con leader, backup, responsabilità chiare.
5. **Fasi di risposta** — Fase 1 risposta immediata (0-4h: valutazione, attivazione team, comunicazione iniziale, contenimento); Fase 2 gestione crisi (4-72h: workaround, comunicazione stakeholder, monitoring, decisioni strategiche); Fase 3 recovery (72h-2 settimane: ripristino sistemi, ritorno alla normalità); Fase 4 ritorno alla normalità (chiusura crisi, lessons learned, aggiornamento piani).
6. **Procedure specifiche per scenario** — link a runbook dettagliati.
7. **Risorse di recovery** — siti alternativi, contatti emergenza, fornitori critici, IT backup.
8. **Comunicazione** — template messaggi, canali, stakeholder matrix, media relations.
9. **Allegati** — contact list aggiornata, checklist attivazione, moduli incident log, mappe siti.

## Exercise Programme

ISO 22301 richiede esercitazioni regolari (8.5). La progressione tipica copre cinque livelli di complessità.

| Tipo | Complessità | Durata | Frequenza | Partecipanti |
|------|-------------|--------|-----------|--------------|
| Alert Exercise | Bassa | 30 min | Trimestrale | Contact tree |
| Start Exercise | Media | 2-4 ore | Semestrale | BC Team |
| Tabletop Exercise | Media | 4-8 ore | Annuale | Management + BC Team |
| Walkthrough | Media-Alta | 1 giorno | Annuale | Team operativi |
| Full-Scale Drill | Alta | 1-2 giorni | Biennale | Tutta organizzazione |

Un tabletop ben progettato si articola in inject (eventi narrativi che evolvono nel tempo, es. inject 1 a T+0, inject 2 a T+30min, inject 3 a T+2h), con domande di discussione per ciascun team-pivot. L'output è una matrice "cosa ha funzionato / cosa migliorare" per area (comunicazione, decision-making, procedure, risorse) e una lista di azioni correttive con responsabile e scadenza.

## KPI

### KPI operativi

| KPI | Target | Frequenza |
|-----|--------|-----------|
| RTO Achievement | > 95% | Per test |
| Plan Currency (piani aggiornati entro scadenza) | 100% | Mensile |
| Training Completion | 100% | Annuale |
| Contact List Accuracy | > 98% | Trimestrale |
| Exercise Completion | 100% pianificate eseguite | Annuale |
| Incident Response Time | < 30 min attivazione team | Per evento |

### KPI strategici

| KPI | Target |
|-----|--------|
| Business disruption | < X ore totali / anno |
| Recovery success rate | > 95% recovery entro RTO |
| Stakeholder confidence (survey) | > 80% |
| Audit findings (NC maggiori) | 0 |

## Test Scenarios

| Scenario | Impatto | Processi testati |
|----------|---------|------------------|
| Failure data center | IT/Dati | DR, backup, comunicazione |
| Indisponibilità sede | Facilities | Workplace recovery, remote work |
| Cyber attack / Ransomware | IT/Operations | Incident response, DR, comunicazione |
| Failure fornitore critico | Supply chain | Supplier continuity |
| Evento naturale | Facilities/Staff | Emergency response, staff welfare |
| Pandemia | Staff | Remote work, HR continuity |

## SME Implementation Notes

### Timeline indicativa (PMI)

| Fase | Durata |
|------|--------|
| Scope e Policy | 2 settimane |
| BIA | 3-4 settimane |
| Risk Assessment | 2 settimane |
| Strategie BC | 2 settimane |
| BC Plans | 4-6 settimane |
| Esercitazione tabletop | 1 settimana |
| Audit interno | 1 settimana |

### Quick wins

1. Contact list emergenza testata (non solo compilata)
2. Backup IT verificato con test restore reale
3. Procedura di comunicazione di crisi (1 pagina)
4. Accordo di supporto emergenza con fornitore IT
5. Identificazione di 3-5 processi critici con BIA snella

### Errori comuni da evitare

- BIA condotta senza i business owner (output sterile, non actionable)
- RTO troppo aggressivi rispetto alle risorse disponibili
- Piani mai testati (tabletop almeno annuale è il minimo)
- Contact list non aggiornate (responsabilità HR + BC Manager)
- Nessun sito alternativo identificato
- Dipendenza da singole persone chiave (single points of human failure)

## Implementation Notes

- 22301 si integra naturalmente con ISO 27001 A.5.29-30 (Information Security during disruption + ICT readiness for business continuity): l'organizzazione che già opera un ISMS può estenderlo a BCMS riusando policy, governance e ciclo di audit.
- Il BIA va aggiornato ad ogni cambio significativo (M&A, nuova line of business, dismissione, cambio fornitore critico) e almeno annualmente. È più importante che sia vivo che perfetto.
- I BC Plans vanno testati entro 3 mesi dalla prima emissione: un piano non testato è un piano non valido.

## References

- ISO 22301:2019 — Security and resilience — Business continuity management systems — Requirements
- ISO 22313:2020 — Guidance per ISO 22301
- ISO/TS 22317 — BIA guidelines
- BCI Good Practice Guidelines
- NIST SP 800-34 — Contingency Planning Guide
