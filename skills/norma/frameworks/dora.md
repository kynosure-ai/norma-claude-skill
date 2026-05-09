---
framework: dora
display_name: "DORA — Digital Operational Resilience Act (EU) 2022/2554"
canonical_ref: "Regulation (EU) 2022/2554"
language: it
---

DORA (Digital Operational Resilience Act) is the EU regulation harmonising ICT risk management for financial entities, applicable from 17 January 2025; this reference covers scope, the 5 pillars (ICT risk management, incident management, resilience testing/TLPT, third-party risk, information sharing), the 24h/72h/30-day incident reporting flow, contractual requirements for ICT third-party providers (Article 30), and the ICT third-party register.

## Scope

DORA è un Regolamento UE direttamente applicabile (no recepimento nazionale necessario), in vigore dal 16 gennaio 2023 e applicabile dal **17 gennaio 2025**. Copre 21 categorie di entità finanziarie + i fornitori ICT critici (Critical Third-Party Providers, CTPP) sotto oversight europeo.

### Entità soggette (Art. 2)

```
Entità Finanziarie:
├── Enti creditizi (banche)
├── Istituti di pagamento
├── Istituti di moneta elettronica
├── Imprese di investimento
├── Fornitori servizi crypto-asset (CASP, MiCA)
├── Depositari centrali titoli (CSD)
├── Controparti centrali (CCP)
├── Sedi di negoziazione
├── Gestori fondi (AIFM, UCITS)
├── Imprese di assicurazione e riassicurazione
├── Intermediari assicurativi
├── Enti pensionistici aziendali (IORP)
├── Agenzie di rating del credito
├── Revisori legali
└── Fornitori di servizi ICT critici (Art. 31)

Esclusioni notevoli:
├── Intermediari assicurativi micro (< 10 dipendenti, < €2M fatturato)
└── Alcune entità post-negoziazione
```

### 5 Pilastri

```
Pillar 1 — ICT Risk Management (Art. 5-16)
├── Framework gestione rischi ICT
├── Governance e organizzazione
├── Identificazione asset & rischi
├── Protezione e prevenzione
├── Rilevamento anomalie
└── Risposta e ripristino

Pillar 2 — ICT Incident Management (Art. 17-23)
├── Processo gestione incidenti
├── Classificazione incidenti
├── Notifica autorità (24h / 72h / 30gg)
├── Reporting periodico
└── Lessons learned

Pillar 3 — Digital Operational Resilience Testing (Art. 24-27)
├── Programma test resilienza
├── Vulnerability assessment
├── Threat-Led Penetration Testing (TLPT)
├── Test scenari
└── Test fornitori critici

Pillar 4 — ICT Third-Party Risk (Art. 28-44)
├── Strategia terze parti ICT
├── Due diligence pre-contratto
├── Requisiti contrattuali (Art. 30)
├── Monitoraggio continuo
├── Exit strategy
└── Oversight CTPP da parte delle ESA

Pillar 5 — Information Sharing (Art. 45)
├── Accordi di condivisione
├── Threat intelligence
└── Collaborazione settoriale
```

## Timeline

| Data | Milestone |
|------|-----------|
| 16 gennaio 2023 | DORA in vigore |
| 17 gennaio 2024 | Bozze RTS / ITS pubblicate |
| **17 gennaio 2025** | **DORA applicabile** |
| 17 gennaio 2025 | Registri ICT da notificare alle autorità competenti |
| 17 aprile 2025 | Prima notifica incidenti secondo nuovo formato |
| Periodicamente (3 anni) | TLPT obbligatorio per entità significative |

## Pillar 1 — ICT Risk Management Framework

```
Governance (Art. 5)
├── Responsabilità del management body
├── Ruolo dedicato ICT risk (CIRO/CTO)
├── Linee di riporto chiare
└── Budget adeguato

Identificazione (Art. 8)
├── Inventario asset ICT
├── Mappatura funzioni critiche
├── Identificazione dipendenze
└── Valutazione criticità

Protezione (Art. 9)
├── Policy sicurezza ICT
├── Controllo accessi
├── Gestione cambiamenti
├── Patch management
└── Data protection

Rilevamento (Art. 10)
├── Monitoraggio continuo
├── Anomaly detection
├── Log management
└── Alert & escalation

Risposta (Art. 11)
├── Business continuity plan
├── Disaster recovery plan
├── Comunicazione di crisi
└── Test periodici

Apprendimento (Art. 13)
├── Post-incident review
├── Lessons learned
├── Miglioramento continuo
└── Reporting interno
```

## Pillar 2 — ICT Incident Management

### Classificazione (Art. 18) — soglie indicative per "incidente maggiore"

| Criterio | Soglia |
|----------|--------|
| Clienti impattati | > 10% clienti o > 500.000 |
| Durata | > 2 ore |
| Area geografica | > 2 Stati membri |
| Perdita dati | Dati critici compromessi |
| Impatto economico | > 0.5% CET1 o equivalente |
| Funzioni critiche | Qualsiasi interruzione |

I criteri esatti sono fissati dagli RTS (Regulatory Technical Standards) on incident classification.

### Timeline notifica (Art. 19)

```
T+0:    Incidente rilevato
T+4h:   Classificazione completata
T+24h:  Notifica iniziale (se incidente maggiore)
T+72h:  Report intermedio
T+30gg: Report finale

Contenuto della notifica:
├── ID incidente
├── Data/ora rilevamento
├── Descrizione evento
├── Impatto stimato
├── Funzioni interessate
├── Azioni intraprese
└── Root cause (se nota)
```

### Destinatari della notifica

| Tipo entità | Autorità competente (Italia) |
|-------------|------------------------------|
| Banche, intermediari investimento | Banca d'Italia |
| Imprese assicurazione/riassicurazione | IVASS |
| Sedi di negoziazione, controparti centrali | CONSOB |
| Cross-border | Autorità home + autorità host |

A livello UE, le autorità nazionali aggregano e trasmettono ad ESMA / EBA / EIOPA secondo i meccanismi previsti dagli ITS on incident reporting.

## Pillar 3 — Resilience Testing & TLPT

```
Chi deve eseguire TLPT:
├── Entità significative (criteri ESA)
├── Almeno ogni 3 anni
└── Su funzioni critiche o importanti

Elementi del TLPT:
├── Threat intelligence phase
├── Red team testing
├── Purple team exercise
├── Reporting strutturato
└── Remediation plan

Tester qualificati:
├── Certificazioni riconosciute
├── Indipendenza
├── Esperienza nel settore finanziario
└── Assicurazione adeguata
```

I dettagli di esecuzione TLPT seguono il framework TIBER-EU (Threat Intelligence-Based Ethical Red Teaming) come riferimento, formalizzato dagli RTS DORA su TLPT.

## Pillar 4 — ICT Third-Party Risk

### Obblighi contrattuali (Art. 30)

```
Clausole obbligatorie nei contratti ICT:
├── Descrizione chiara dei servizi
├── Ubicazione dei dati (UE / extra-UE)
├── Livelli di servizio (SLA)
├── Obblighi di reportistica
├── Diritti di audit
├── Diritti di accesso (autorità competenti)
├── Piano di exit
├── Requisiti per i sub-fornitori
├── Notifica incidenti
└── Business continuity del fornitore

Per servizi critici aggiungere:
├── Accesso completo ai dati
├── Assistenza in caso di inadempienza
├── Partecipazione a test di resilienza
├── Exit senza interruzione del servizio
└── Monitoraggio continuo della qualità
```

### Registro fornitori ICT (Art. 28.3)

Le entità finanziarie devono mantenere e fornire all'autorità competente un Registro of Information dei fornitori ICT con:

- Nome del fornitore (con identificativo univoco)
- Servizi forniti
- Funzioni supportate (critiche / importanti / non critiche)
- Data di inizio e fine contratto
- Ubicazione del fornitore e dei dati
- Sub-fornitori (con la stessa granularità)
- Alternative disponibili
- Data ultima valutazione

Il formato del Registro è standardizzato dagli ITS Annex of Information.

### CTPP — Critical Third-Party Provider oversight

I fornitori ICT designati come critici sono soggetti a oversight diretto delle ESA (Lead Overseer designato fra EBA / ESMA / EIOPA), con potere di richiedere informazioni, condurre indagini, raccomandazioni, misure correttive.

## Mapping DORA ↔ ISO/IEC 27001

| DORA Article | ISO 27001 (clausola/controllo) | Gap tipico |
|--------------|--------------------------------|------------|
| Art. 6 (Framework) | 4.4, 6.1.2 | Coinvolgimento del management body |
| Art. 8 (Identification) | A.5.9 | Criticità definita per DORA |
| Art. 9 (Protection) | A.8.x | Change management formale |
| Art. 10 (Detection) | A.8.15, A.8.16 | Real-time monitoring |
| Art. 11 (Response) | A.5.29, A.5.30 | ICT-specific + test periodici |
| Art. 17-23 (Incidents) | A.5.24-28 | Timeline 24h/72h/30gg |
| Art. 26-27 (TLPT) | A.8.29 | TLPT formale obbligatorio |
| Art. 28-44 (Third-party) | A.5.19-23 | Registro + clausole DORA-specific |

Un'entità finanziaria che ha già un ISMS 27001 maturo copre buona parte di Art. 5-16 a livello di controllo; i delta principali riguardano la formalizzazione del registro fornitori secondo gli ITS, i requisiti TLPT, le timeline di incident reporting, e le clausole contrattuali Art. 30.

## Implementation Notes

- DORA armonizza ma non elimina la sovrapposizione con normative settoriali (CRR/CRD per banche, Solvency II per assicurazioni, MiCA per crypto). Le autorità nazionali stanno emanando guidance per chiarire l'integrazione fra cornici.
- Il Registro of Information è uno degli adempimenti più sottovalutati in fase di go-live: la sua compilazione richiede un sforzo non banale di mappatura supply chain ICT, e la prima trasmissione nel 2025 è stata un evento operativo critico per molti player.
- TLPT differisce sostanzialmente da un pen-test ordinario: richiede una threat intelligence iniziale, un team scope definito, indipendenza del red team, coinvolgimento del defender (purple team), e un reporting strutturato. Le entità che eseguivano già TIBER-EU partivano avvantaggiate.
- L'integrazione con il BCMS (ISO 22301) e con l'Incident Response del management ISMS è un'opportunità di riuso, non di duplicazione: il BCP, il DRP e l'incident handling possono essere condivisi tra DORA, NIS2 e Annex A 27001 con DORA-specific overlays per le timeline e il reporting.
- Per le entità che usano cloud provider hyperscale, l'aspetto contrattuale (Art. 30) è il punto critico: molti contratti standard hyperscale non includono di default tutti i requisiti DORA, e le modifiche contrattuali sono spesso un negoziato lungo. Va affrontato con anticipo.

## References

- Regolamento (UE) 2022/2554 — DORA
- RTS on ICT Risk Management Framework
- RTS on ICT Incident Reporting (classification + reporting templates)
- RTS on TLPT
- RTS on Third-Party ICT Arrangements (Art. 28-30)
- ITS on Register of Information (Art. 28.3)
- EBA / ESMA / EIOPA — joint guidelines DORA
- TIBER-EU framework (riferimento operativo per TLPT)
