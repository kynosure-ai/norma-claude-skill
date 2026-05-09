---
framework: pims
display_name: "ISO/IEC 27701:2019 — Privacy Information Management System"
canonical_ref: "ISO/IEC 27701:2019"
language: it
---

ISO/IEC 27701:2019 extends ISO/IEC 27001/27002 with privacy-specific requirements for a Privacy Information Management System (PIMS); this reference covers the Controller / Processor split (Clauses 7-8 / Annex A and B), GDPR mapping, RoPA structure, DPIA outline, data-subject-rights procedure and the documented information set required for certification.

## Architecture

ISO/IEC 27701:2019 è una **estensione** di ISO/IEC 27001/27002, non uno standard standalone. La certificazione 27701 presuppone una certificazione ISO 27001:2022 attiva — il PIMS si innesta sull'ISMS esistente e ne riusa governance, ciclo di audit e procedimenti di management review.

```
ISO/IEC 27701:2019

Struttura:
├── Clausola 5: PIMS requirements        → estende ISO 27001 (clausole 4-10)
├── Clausola 6: PIMS guidance            → estende ISO 27002 (controlli sicurezza)
├── Clausola 7: Guidance per PII Controller (titolare GDPR)
├── Clausola 8: Guidance per PII Processor (responsabile GDPR)
│
├── Annex A: Controlli aggiuntivi PII Controller (mappati a Clausola 7)
├── Annex B: Controlli aggiuntivi PII Processor (mappati a Clausola 8)
├── Annex C: Mapping a ISO 29100 (Privacy Framework)
├── Annex D: Mapping a GDPR
├── Annex E: Mapping a ISO 27018 / ISO 29151
└── Annex F: Estensione 27001/27002 per privacy
```

### Controller vs Processor

| Aspetto | PII Controller | PII Processor |
|---------|----------------|---------------|
| Definizione | Determina finalità e mezzi del trattamento | Tratta PII per conto del Controller |
| Riferimento ISO | Clausola 7, Annex A | Clausola 8, Annex B |
| Equivalente GDPR | Titolare del trattamento | Responsabile del trattamento |
| Responsabilità chiave | Basi giuridiche, diritti interessati, DPIA | Sicurezza, sub-processor, supporto al Controller |

## Clause 7 — PII Controller Controls (Annex A)

```
7.2 Condizioni di raccolta e trattamento
├── 7.2.1 Identificare e documentare finalità (GDPR Art. 5)
├── 7.2.2 Identificare basi giuridiche (GDPR Art. 6)
├── 7.2.3 Determinare quando/come ottenere consenso (GDPR Art. 7)
├── 7.2.4 Ottenere e registrare consenso
├── 7.2.5 Privacy Impact Assessment → DPIA (GDPR Art. 35)
├── 7.2.6 Contratti con PII Processor (GDPR Art. 28)
├── 7.2.7 Joint Controller (GDPR Art. 26)
└── 7.2.8 Record trattamenti (GDPR Art. 30)

7.3 Obblighi verso data subjects
├── 7.3.1 Determinare e adempiere obblighi
├── 7.3.2 Informazioni da fornire (GDPR Art. 13-14)
├── 7.3.3 Fornire informazioni
├── 7.3.4 Meccanismo modifica/revoca consenso
├── 7.3.5 Meccanismo obiezione
├── 7.3.6 Accesso, rettifica, cancellazione (GDPR Art. 15-17)
├── 7.3.7 Obbligo informare terze parti
├── 7.3.8 Copie PII (portabilità) (GDPR Art. 20)
├── 7.3.9 Gestire richieste
└── 7.3.10 Decisioni automatizzate (GDPR Art. 22)

7.4 Privacy by design e default
├── 7.4.1 Limitare raccolta
├── 7.4.2 Limitare trattamento
├── 7.4.3 Accuratezza e qualità
├── 7.4.4 Minimizzazione obiettivi
├── 7.4.5 Anonimizzazione e cancellazione
├── 7.4.6 File temporanei
├── 7.4.7 Retention
├── 7.4.8 Smaltimento
└── 7.4.9 Controlli trasmissione

7.5 Condivisione, trasferimento, divulgazione
├── 7.5.1 Identificare basi per trasferimento
├── 7.5.2 Paesi/organizzazioni destinatari
├── 7.5.3 Record trasferimenti
└── 7.5.4 Record divulgazione terze parti
```

## Clause 8 — PII Processor Controls (Annex B)

```
8.2 Condizioni di raccolta e trattamento
├── 8.2.1 Accordi con cliente (Controller)
├── 8.2.2 Limitazione finalità del processor
├── 8.2.3 Marketing e pubblicità (vincoli)
├── 8.2.4 Istruzioni violate
├── 8.2.5 Obblighi verso il cliente
└── 8.2.6 Record trattamento

8.3 Obblighi verso data subjects
├── 8.3.1 Obblighi
└── 8.3.2 Fornire copie/informazioni su richiesta

8.4 Privacy by design e default
├── 8.4.1 File temporanei
├── 8.4.2 Restituire/eliminare PII (a fine contratto)
└── 8.4.3 Controlli trasmissione

8.5 Condivisione, trasferimento, divulgazione
├── 8.5.1 Basi per trasferimento tra giurisdizioni
├── 8.5.2 Paesi destinatari
├── 8.5.3 Record trasferimenti
├── 8.5.4 Record divulgazione
├── 8.5.5 Notifica richieste divulgazione
├── 8.5.6 Divulgazioni legalmente vincolanti
├── 8.5.7 Divulgazione sub-contractors
└── 8.5.8 Cambio sub-contractor
```

## Mandatory Documented Information

### Tier 1 — documenti core

| ID | Documento | Clausola | Note |
|----|-----------|----------|------|
| D01 | Scope PIMS | 5.2.3 | Ruolo Controller / Processor |
| D02 | Privacy Policy | 5.3.2 | Integrata con IS Policy |
| D03 | Ruoli e responsabilità privacy | 5.3.3 | DPO, Privacy Team |
| D04 | Privacy Risk Assessment | 5.4.1 | Risk specifici PII |
| D05 | Obiettivi privacy | 5.4.2 | SMART, misurabili |
| D06 | Record of Processing Activities (RoPA) | 7.2.8 / 8.2.6 | GDPR Art. 30 |
| D07 | Basi giuridiche del trattamento | 7.2.2 | Per ogni trattamento |

### Tier 2 — documenti Controller-specific

| ID | Documento |
|----|-----------|
| D08 | Privacy Notice (per data subjects) |
| D09 | Consent Management Procedure |
| D10 | DPIA Template |
| D11 | Data Subject Rights Procedure |
| D12 | Retention Schedule |
| D13 | International Transfer Procedure (SCCs, adequacy, safeguards) |

### Tier 3 — documenti Processor-specific

| ID | Documento |
|----|-----------|
| D14 | Data Processing Agreement (DPA) |
| D15 | Sub-processor Management |
| D16 | PII Return / Deletion Procedure |

### Tier 4 — procedure operative

| ID | Documento | Riferimento GDPR |
|----|-----------|------------------|
| P01 | Data Breach Response Procedure | Art. 33-34 (notifica 72h) |
| P02 | PII Inventory Management | Art. 30 |
| P03 | Access to PII Procedure | Art. 5 |
| P04 | Anonymization / Pseudonymization Guide | Art. 32 |
| P05 | Privacy Training Programme | Art. 39 |

## GDPR Mapping (key)

### Principi GDPR (Art. 5) → controlli ISO 27701

| Principio GDPR | Controllo / Clausola ISO 27701 |
|----------------|--------------------------------|
| Liceità, correttezza, trasparenza | 7.2.1, 7.2.2, 7.3.2, 7.3.3 |
| Limitazione delle finalità | 7.2.1, 7.4.4, 8.2.2 |
| Minimizzazione dei dati | 7.4.1, 7.4.2 |
| Esattezza | 7.4.3 |
| Limitazione della conservazione | 7.4.5, 7.4.7 |
| Integrità e riservatezza | 6.x (controlli sicurezza ISMS) |
| Responsabilizzazione | 7.2.8, 5.7, DPIA |

### Basi giuridiche (Art. 6) → documentazione

| Base | Documentazione richiesta |
|------|--------------------------|
| Consenso | Registro consensi, evidenze, meccanismo di revoca |
| Contratto | Collegamento a clausole contrattuali |
| Obbligo legale | Riferimento alla norma specifica |
| Interessi vitali | Documentazione del caso specifico |
| Interesse pubblico | Atto / regolamento autorizzativo |
| Legittimo interesse | LIA — Legitimate Interest Assessment |

### Diritti degli interessati (Art. 15-22) → procedure

| Diritto | Art. GDPR | Clausola ISO 27701 | Deadline |
|---------|-----------|--------------------|----------|
| Informazione | 13-14 | 7.3.2, 7.3.3 | Al momento della raccolta |
| Accesso | 15 | 7.3.6 | 30 giorni |
| Rettifica | 16 | 7.3.6 | 30 giorni |
| Cancellazione | 17 | 7.3.6, 7.4.5 | 30 giorni |
| Limitazione | 18 | 7.3.5 | 30 giorni |
| Portabilità | 20 | 7.3.8 | 30 giorni |
| Opposizione | 21 | 7.3.5 | Senza ritardo |
| No decisioni automatizzate | 22 | 7.3.10 | 30 giorni |

## Record of Processing Activities (RoPA)

### RoPA Controller (GDPR Art. 30.1) — campi

Per ogni attività di trattamento: ID, nome/descrizione, titolare (nome, indirizzo, contatti), DPO, eventuali co-titolari; finalità e base giuridica con riferimento Art. 6; categorie di interessati e dati (incluso flag dati particolari); destinatari (categoria, paese, garanzie come DPA, SCCs); retention per categoria con base giuridica; misure di sicurezza (cifratura, controllo accessi, backup); trasferimenti extra-UE con base e data di valutazione.

### RoPA Processor (GDPR Art. 30.2) — campi

Trattamento per Controller (nome, contatti, DPO, rappresentante UE se controller extra-UE); categorie di trattamento (hosting, support, ecc.); trasferimenti per conto del Controller con garanzie; sub-processor (nome, servizio, paese, autorizzazione generale o specifica); misure di sicurezza specifiche per il servizio.

## DPIA — Outline

Una DPIA (Data Protection Impact Assessment, GDPR Art. 35) è obbligatoria per trattamenti ad alto rischio. La struttura canonica:

1. **Informazioni generali** — data, responsabile, DPO coinvolto, versione.
2. **Necessità della DPIA** — checklist criteri di attivazione (profilazione automatizzata, dati particolari su larga scala, sorveglianza spazi pubblici, nuova tecnologia, minori/dipendenti, matching/combining, decisioni automatizzate con effetti legali).
3. **Descrizione del trattamento** — natura, ambito (scala/volume), contesto (rapporto con interessati), finalità.
4. **Consultazione degli interessati** — metodo (survey, focus group), feedback DPO.
5. **Necessità e proporzionalità** — finalità lecita, minimizzazione, limitazione conservazione, qualità dei dati, base giuridica.
6. **Identificazione dei rischi** — tabella con sorgente, impatto, probabilità, score.
7. **Misure di mitigazione** — per ogni rischio: misura, responsabile, stato.
8. **Rischio residuo** — score pre/post mitigazione, accettabilità.
9. **Parere del DPO**.
10. **Decisione** — approvato / con condizioni / rimandato / consultazione autorità (per rischio alto residuo). Firma responsabile + DPO.

## Data Subject Rights Procedure — Outline

Una procedura DSR robusta copre: canali autorizzati di ricezione (email privacy@..., form online, posta); informazioni da raccogliere (identità, tipo di richiesta, dati interessati, formato preferito); verifica dell'identità (account autenticato, documento, verifica telefonica); registrazione e tracking con ID univoco e deadline (+30 giorni); checklist per tipo di richiesta (Accesso, Cancellazione, Portabilità) — es. per Cancellazione: verificare diritto applicabile, eccezioni (obbligo legale, difesa in giudizio), notifica destinatari, cancellazione da backup pianificata; timeline (conferma ricezione 3 gg lavorativi, risposta standard 30 gg, estensione +60 gg per casi complessi con motivazione); template di risposta; documentazione conservata per ogni richiesta (richiesta originale, verifica identità, log azioni, risposta inviata, comunicazioni successive, retention X anni).

## Implementation Notes

- 27701 senza 27001 in essere è formalmente impossibile da certificare. Per organizzazioni che vogliono affrontare GDPR con un management-system approach ma non hanno ancora un ISMS, il path corretto è 27001 prima, 27701 dopo (o in parallelo, con 27001 come requisito di certificazione finale).
- L'integrazione fra Privacy Risk Register e Information Security Risk Register è la decisione architetturale più importante: tenerli separati duplica il lavoro; integrarli rischia di far prevalere ottica security su ottica diritti dell'interessato. Best practice: registri integrati ma con tag privacy-specific che facilitino il reporting al DPO.
- Il DPO è il punto di contatto fra ISMS, PIMS e GDPR governance. Il suo coinvolgimento nelle DPIA, nei management review e nella scelta di basi giuridiche è non negoziabile.
- Il DPA è il documento contrattuale critico per il Processor: deve coprire tutti i requisiti GDPR Art. 28 (oggetto, durata, natura/finalità, tipi di PII, categorie di interessati, obblighi e diritti del Controller, istruzioni documentate, sicurezza, sub-processor, supporto, return/delete, audit). Mancanze qui sono il primo finding tipico in audit DPO.

## References

- ISO/IEC 27701:2019 — Security techniques — Extension to ISO/IEC 27001 and ISO/IEC 27002 for privacy information management
- Regolamento (UE) 2016/679 (GDPR)
- ISO/IEC 29100 — Privacy framework
- ISO/IEC 29151 — Code of practice for PII protection
- ISO/IEC 27018 — PII in public clouds
- EDPB (European Data Protection Board) Guidelines
- Article 29 Working Party Opinions (legacy ma ancora autorevoli su molti punti)
