---
title: Data Protection Impact Assessment (DPIA)
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: Data Protection Officer
approver: '{{approver_name}}'
framework: 'ISO 27701:2019'
iso_clauses:
  - 7.2.5 - Privacy impact assessment
annex_controls:
  - A.7.2.5 - Privacy impact assessment
gdpr_articles:
  - Art. 35 - Data protection impact assessment
  - Art. 36 - Prior consultation
role: controller
cross_references:
  - document: Privacy Risk Assessment
    path: ../risk-assessment/privacy-risk-assessment.md
  - document: RoPA
    path: ../registers/record-of-processing-activities.md
  - document: Privacy Policy
    path: ../policies/privacy-policy.md
  - document: Consent Management
    path: ../procedures/consent-management-procedure.md
related_documents:
  - privacy-risk-assessment
  - record-of-processing-activities
  - privacy-policy
  - consent-management-procedure
  - data-breach-notification-procedure
  - international-data-transfer-assessment
  - pims-scope
status: draft
review_frequency: per_project
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# Data Protection Impact Assessment (DPIA)
## Valutazione d'Impatto sulla Protezione dei Dati

---

## Introduzione

La Data Protection Impact Assessment (DPIA), o Valutazione d'Impatto sulla Protezione dei Dati, costituisce uno strumento fondamentale previsto dall'Art. 35 del Regolamento UE 2016/679 (GDPR) e dal controllo 7.2.5 della norma ISO/IEC 27701:2019 per identificare e mitigare i rischi che un trattamento di dati personali potrebbe comportare per i diritti e le liberta degli interessati. L'Organizzazione e tenuta a condurre una DPIA prima di avviare qualsiasi trattamento che, per la sua natura, ambito, contesto e finalita, possa presentare un rischio elevato, con particolare riferimento ai trattamenti che comportano valutazione sistematica e automatizzata di aspetti personali, al trattamento su larga scala di categorie particolari di dati, e alla sorveglianza sistematica su larga scala di zone accessibili al pubblico.

Il presente template guida l'Organizzazione attraverso tutte le fasi richieste dalla normativa, partendo dalla descrizione sistematica delle operazioni di trattamento previste, delle finalita perseguite e della base giuridica, proseguendo con la valutazione della necessita e proporzionalita dei trattamenti in relazione alle finalita, l'identificazione e valutazione dei rischi per i diritti e le liberta degli interessati, e la definizione delle misure previste per affrontare tali rischi. Il Data Protection Officer viene consultato in conformita all'Art. 35.2 GDPR e fornisce il proprio parere documentato. Qualora il rischio residuo permanga elevato nonostante le misure adottate, l'Organizzazione dovra procedere alla consultazione preventiva dell'Autorita Garante ai sensi dell'Art. 36 GDPR prima di avviare il trattamento.

---

## Sezione A: Informazioni Generali

### A.1 Identificazione DPIA

| Campo | Valore |
|-------|--------|
| **Codice DPIA** | DPIA-[AAAA]-[NNN] |
| **Titolo progetto/trattamento** | [Nome] |
| **Versione** | 1.0 |
| **Data creazione** | {{document_date}} |
| **Data ultimo aggiornamento** | {{document_date}} |
| **Stato** | [ ] Bozza [ ] In revisione [ ] Approvata [ ] Da aggiornare |

### A.2 Team DPIA

| Ruolo | Nome | Funzione | Contatto |
|-------|------|----------|----------|
| **Responsabile DPIA** | [Nome] | [Ruolo] | [Email] |
| **Process Owner** | [Nome] | [Ruolo] | [Email] |
| **IT/Security** | [Nome] | [Ruolo] | [Email] |
| **Legal** | [Nome] | [Ruolo] | [Email] |
| **DPO** | [Nome] | DPO | [Email] |

### A.3 Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 0.1 | [Data] | [Nome] | Bozza iniziale |
| 0.2 | [Data] | [Nome] | Integrazione feedback DPO |
| 1.0 | [Data] | [Nome] | Versione approvata |

---

## Sezione B: Necessità della DPIA

### B.1 Screening Iniziale

**Domanda**: Il trattamento rientra nei casi in cui la DPIA è obbligatoria?

#### Criteri GDPR Art. 35.3

| Criterio | Applicabile | Note |
|----------|-------------|------|
| Valutazione sistematica e automatizzata (profilazione) con effetti giuridici | [ ] Sì [ ] No | |
| Trattamento su larga scala di dati particolari (Art. 9) o penali (Art. 10) | [ ] Sì [ ] No | |
| Sorveglianza sistematica su larga scala di zone accessibili al pubblico | [ ] Sì [ ] No | |

#### Criteri EDPB/Garante (almeno 2 = DPIA obbligatoria)

| # | Criterio | Applicabile |
|---|----------|-------------|
| 1 | Valutazione o scoring, inclusa profilazione | [ ] Sì [ ] No |
| 2 | Processo decisionale automatizzato con effetti significativi | [ ] Sì [ ] No |
| 3 | Monitoraggio sistematico | [ ] Sì [ ] No |
| 4 | Dati sensibili o altamente personali | [ ] Sì [ ] No |
| 5 | Trattamento su larga scala | [ ] Sì [ ] No |
| 6 | Matching o combinazione di dataset | [ ] Sì [ ] No |
| 7 | Dati di soggetti vulnerabili | [ ] Sì [ ] No |
| 8 | Uso innovativo o nuove tecnologie | [ ] Sì [ ] No |
| 9 | Trattamento che impedisce esercizio diritti/accesso servizi | [ ] Sì [ ] No |

**Totale criteri applicabili**: [N]

### B.2 Decisione

| Esito Screening | Selezione |
|-----------------|-----------|
| DPIA obbligatoria | [ ] |
| DPIA volontaria (best practice) | [ ] |
| DPIA non necessaria | [ ] |

**Motivazione**: [Spiegare la decisione]

---

## Sezione C: Descrizione del Trattamento

### C.1 Descrizione Generale

**Natura del trattamento** (cosa fate con i dati):

[Descrivere le operazioni di trattamento: raccolta, registrazione, organizzazione, strutturazione, conservazione, adattamento, modifica, estrazione, consultazione, uso, comunicazione, diffusione, raffronto, interconnessione, limitazione, cancellazione, distruzione]

**Ambito del trattamento** (scala):

| Aspetto | Dettaglio |
|---------|-----------|
| Volume dati stimato | [Es. 10.000 record] |
| Numero interessati | [Es. 5.000 persone] |
| Area geografica | [Es. Italia, UE, Globale] |
| Durata trattamento | [Es. Continuativo, 3 anni] |

**Contesto del trattamento**:

[Descrivere il contesto: rapporto con interessati, loro aspettative, posizione di controllo/dipendenza, esperienza precedente, stato dell'arte tecnologia]

**Finalità del trattamento**:

| # | Finalità | Descrizione |
|---|----------|-------------|
| 1 | [Finalità primaria] | [Descrizione] |
| 2 | [Finalità secondaria] | [Descrizione] |

### C.2 Flusso dei Dati

```
[Inserire diagramma flusso dati]

Esempio:
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│  RACCOLTA   │───►│ ELABORAZIONE│───►│ CONSERVAZIONE│
│             │    │             │    │             │
│ • Form web  │    │ • Sistema X │    │ • Database Y│
│ • App       │    │ • Analytics │    │ • Backup    │
└─────────────┘    └─────────────┘    └─────────────┘
       │                  │                  │
       ▼                  ▼                  ▼
┌─────────────┐    ┌─────────────┐    ┌─────────────┐
│ INTERESSATO │    │ PROCESSOR   │    │ TERZA PARTE │
└─────────────┘    └─────────────┘    └─────────────┘
```

### C.3 Categorie di Dati

| Categoria | Dati Specifici | Particolari (Art. 9) | Fonte |
|-----------|----------------|---------------------|-------|
| Identificativi | Nome, cognome, CF | No | Interessato |
| Contatto | Email, telefono | No | Interessato |
| [Altra categoria] | [Dettaglio] | [Sì/No] | [Fonte] |

### C.4 Categorie di Interessati

| Categoria | Stima Numerosità | Vulnerabili |
|-----------|------------------|-------------|
| [Es. Clienti] | [N] | [ ] Sì [ ] No |
| [Es. Dipendenti] | [N] | [ ] Sì [ ] No |
| [Es. Minori] | [N] | [X] Sì [ ] No |

### C.5 Destinatari

| Destinatario | Categoria | Paese | Finalità | Base Giuridica |
|--------------|-----------|-------|----------|----------------|
| [Nome] | Controller/Processor/Terzo | [Paese] | [Finalità] | [Base] |

### C.6 Tecnologie Utilizzate

| Tecnologia | Descrizione | Fornitore | Rischi Specifici |
|------------|-------------|-----------|------------------|
| [Sistema X] | [Descrizione] | [Fornitore] | [Rischi] |
| [Cloud Y] | [Descrizione] | [Fornitore] | [Rischi] |

---

## Sezione D: Necessità e Proporzionalità

### D.1 Base Giuridica

| Finalità | Base Giuridica | Art. GDPR | Documentazione |
|----------|----------------|-----------|----------------|
| [Finalità 1] | [Consenso/Contratto/Obbligo/LI] | Art. 6.1.[x] | [Riferimento] |
| [Finalità 2] | [Base] | Art. 6.1.[x] | [Riferimento] |

**Per dati particolari (Art. 9)**:

| Finalità | Condizione Art. 9.2 | Documentazione |
|----------|---------------------|----------------|
| [Se applicabile] | [Condizione] | [Riferimento] |

### D.2 Valutazione Necessità

| Principio | Valutazione | Evidenza |
|-----------|-------------|----------|
| **Finalità legittime e determinate** | [ ] Conforme [ ] Parziale [ ] Non conforme | [Evidenza] |
| **Minimizzazione dati** | [ ] Conforme [ ] Parziale [ ] Non conforme | [Quali dati sono strettamente necessari?] |
| **Limitazione conservazione** | [ ] Conforme [ ] Parziale [ ] Non conforme | [Policy retention applicata] |
| **Qualità dati** | [ ] Conforme [ ] Parziale [ ] Non conforme | [Procedure aggiornamento] |

### D.3 Valutazione Proporzionalità

**Il trattamento è proporzionato rispetto alle finalità?**

| Aspetto | Valutazione |
|---------|-------------|
| Esistono alternative meno intrusive? | [Analisi alternative considerate] |
| I benefici giustificano i rischi? | [Analisi costi-benefici] |
| Le misure di sicurezza sono adeguate al rischio? | [Analisi adeguatezza] |

### D.4 Diritti degli Interessati

| Diritto | Come Garantito | Procedura |
|---------|----------------|-----------|
| Informazione | [Es. Privacy notice sul form] | [Riferimento] |
| Accesso | [Es. Portale self-service] | [Riferimento] |
| Rettifica | [Es. Richiesta via email] | [Riferimento] |
| Cancellazione | [Es. Procedura automatica] | [Riferimento] |
| Limitazione | [Es. Flag nel sistema] | [Riferimento] |
| Portabilità | [Es. Export JSON/CSV] | [Riferimento] |
| Opposizione | [Es. Link unsubscribe] | [Riferimento] |
| No decisioni automatizzate | [Se applicabile] | [Riferimento] |

---

## Sezione E: Consultazione Stakeholder

### E.1 Consultazione DPO

| Data | Parere | Raccomandazioni |
|------|--------|-----------------|
| [Data] | [Sintesi parere] | [Lista raccomandazioni] |

### E.2 Consultazione Interessati (se effettuata)

| Metodo | Data | Partecipanti | Esito |
|--------|------|--------------|-------|
| [Es. Survey] | [Data] | [N] | [Sintesi feedback] |
| [Es. Focus group] | [Data] | [N] | [Sintesi feedback] |

**Motivazione se non consultati**: [Spiegare perché non appropriato/possibile]

### E.3 Altre Consultazioni

| Stakeholder | Data | Feedback |
|-------------|------|----------|
| [Es. IT Security] | [Data] | [Feedback] |
| [Es. Legal] | [Data] | [Feedback] |
| [Es. Business] | [Data] | [Feedback] |

---

## Sezione F: Identificazione e Valutazione Rischi

### F.1 Metodologia di Valutazione

**Scala Probabilità**:
| Livello | Valore | Descrizione |
|---------|--------|-------------|
| Improbabile | 1 | Evento raro, < 1 volta ogni 5 anni |
| Poco probabile | 2 | Evento occasionale, 1 volta ogni 1-5 anni |
| Probabile | 3 | Evento frequente, 1+ volte all'anno |
| Molto probabile | 4 | Evento molto frequente, più volte all'anno |

**Scala Gravità** (impatto su interessati):
| Livello | Valore | Descrizione |
|---------|--------|-------------|
| Trascurabile | 1 | Nessun impatto significativo |
| Limitato | 2 | Disagio temporaneo, facilmente rimediabile |
| Significativo | 3 | Danno significativo ma superabile |
| Massimo | 4 | Danno irreversibile o molto difficile da superare |

**Matrice Rischio** (Probabilità × Gravità):

```
         GRAVITÀ
        1   2   3   4
      ┌───┬───┬───┬───┐
    4 │ 4 │ 8 │12 │16 │  Rischio Alto: 9-16
P     ├───┼───┼───┼───┤  Rischio Medio: 4-8
R   3 │ 3 │ 6 │ 9 │12 │  Rischio Basso: 1-3
O     ├───┼───┼───┼───┤
B   2 │ 2 │ 4 │ 6 │ 8 │
      ├───┼───┼───┼───┤
    1 │ 1 │ 2 │ 3 │ 4 │
      └───┴───┴───┴───┘
```

### F.2 Identificazione Rischi

#### Rischi per Confidenzialità

| ID | Rischio | Fonte Minaccia | Impatto su Interessati |
|----|---------|----------------|------------------------|
| R-C1 | Accesso non autorizzato ai dati | Attaccante esterno | Divulgazione dati personali |
| R-C2 | Data breach da insider | Dipendente malevolo | Esposizione informazioni sensibili |
| R-C3 | Divulgazione accidentale | Errore umano | Perdita privacy |
| R-C4 | [Altro rischio] | [Fonte] | [Impatto] |

#### Rischi per Integrità

| ID | Rischio | Fonte Minaccia | Impatto su Interessati |
|----|---------|----------------|------------------------|
| R-I1 | Modifica non autorizzata | Attacco/Errore | Decisioni basate su dati errati |
| R-I2 | Corruzione dati | Malware/Bug | Dati inaffidabili |
| R-I3 | [Altro rischio] | [Fonte] | [Impatto] |

#### Rischi per Disponibilità

| ID | Rischio | Fonte Minaccia | Impatto su Interessati |
|----|---------|----------------|------------------------|
| R-D1 | Perdita dati | Guasto/Ransomware | Impossibilità esercizio diritti |
| R-D2 | Indisponibilità sistema | Outage | Ritardo servizi |
| R-D3 | [Altro rischio] | [Fonte] | [Impatto] |

#### Rischi Specifici Privacy

| ID | Rischio | Fonte | Impatto su Interessati |
|----|---------|-------|------------------------|
| R-P1 | Profilazione eccessiva | Design sistema | Discriminazione |
| R-P2 | Conservazione oltre necessario | Mancanza policy | Esposizione prolungata |
| R-P3 | Trasferimento extra-UE non conforme | Fornitore | Protezione inadeguata |
| R-P4 | Mancato rispetto diritti | Processo inadeguato | Violazione diritti fondamentali |
| R-P5 | [Altro rischio] | [Fonte] | [Impatto] |

### F.3 Valutazione Rischi Ante Misure

| ID | Rischio | Probabilità | Gravità | Rischio (P×G) | Livello |
|----|---------|-------------|---------|---------------|---------|
| R-C1 | Accesso non autorizzato | 3 | 4 | 12 | Alto |
| R-C2 | Data breach insider | 2 | 4 | 8 | Medio |
| R-C3 | Divulgazione accidentale | 3 | 3 | 9 | Alto |
| R-I1 | Modifica non autorizzata | 2 | 3 | 6 | Medio |
| R-D1 | Perdita dati | 2 | 4 | 8 | Medio |
| R-P1 | Profilazione eccessiva | [P] | [G] | [Score] | [Livello] |
| R-P2 | Conservazione eccessiva | [P] | [G] | [Score] | [Livello] |
| R-P3 | Trasferimento non conforme | [P] | [G] | [Score] | [Livello] |
| R-P4 | Violazione diritti | [P] | [G] | [Score] | [Livello] |

---

## Sezione G: Misure di Mitigazione

### G.1 Misure per Rischi Identificati

| ID Rischio | Misura | Tipo | Responsabile | Stato | Deadline |
|------------|--------|------|--------------|-------|----------|
| R-C1 | Crittografia dati at-rest e in-transit | Tecnica | IT Security | Implementata | - |
| R-C1 | MFA per accesso sistema | Tecnica | IT | Implementata | - |
| R-C1 | Vulnerability assessment periodico | Tecnica | IT Security | In corso | [Data] |
| R-C2 | Principio minimo privilegio | Organizzativa | IT | Implementata | - |
| R-C2 | Logging e monitoring accessi | Tecnica | IT Security | Implementata | - |
| R-C3 | Training privacy dipendenti | Organizzativa | HR/Privacy | Annuale | [Data] |
| R-C3 | Classificazione dati | Organizzativa | Privacy Team | Implementata | - |
| R-I1 | Backup regolari | Tecnica | IT | Implementata | - |
| R-I1 | Controllo integrità | Tecnica | IT | Da implementare | [Data] |
| R-D1 | Disaster recovery | Tecnica | IT | Implementata | - |
| R-D1 | Test restore periodici | Tecnica | IT | Trimestrale | - |
| R-P1 | Review algoritmo profilazione | Organizzativa | Data Team | Da fare | [Data] |
| R-P2 | Implementazione retention automatica | Tecnica | IT | Da implementare | [Data] |
| R-P3 | TIA e SCC aggiornate | Organizzativa | Legal | Completata | - |
| R-P4 | Procedura DSAR aggiornata | Organizzativa | Privacy | Implementata | - |

### G.2 Dettaglio Misure Chiave

#### Misura: [Nome Misura]

| Aspetto | Dettaglio |
|---------|-----------|
| **Descrizione** | [Descrizione dettagliata] |
| **Rischi mitigati** | [Lista ID rischi] |
| **Efficacia attesa** | [Alta/Media/Bassa] |
| **Costo implementazione** | [Stima] |
| **Costo operativo** | [Stima annuale] |
| **Responsabile** | [Nome/Ruolo] |
| **Timeline** | [Date] |
| **KPI/Verifica** | [Come verificare efficacia] |

---

## Sezione H: Rischio Residuo

### H.1 Valutazione Rischi Post Misure

| ID | Rischio | P Ante | G Ante | Score Ante | P Post | G Post | Score Post | Livello |
|----|---------|--------|--------|------------|--------|--------|------------|---------|
| R-C1 | Accesso non autorizzato | 3 | 4 | 12 | 2 | 3 | 6 | Medio |
| R-C2 | Data breach insider | 2 | 4 | 8 | 1 | 3 | 3 | Basso |
| R-C3 | Divulgazione accidentale | 3 | 3 | 9 | 2 | 2 | 4 | Basso |
| R-I1 | Modifica non autorizzata | 2 | 3 | 6 | 1 | 2 | 2 | Basso |
| R-D1 | Perdita dati | 2 | 4 | 8 | 1 | 2 | 2 | Basso |
| R-P1 | Profilazione eccessiva | [P] | [G] | [Score] | [P] | [G] | [Score] | [Livello] |

### H.2 Riepilogo Rischio Residuo

| Livello Rischio | Ante Misure | Post Misure |
|-----------------|-------------|-------------|
| Alto (9-16) | [N] rischi | [N] rischi |
| Medio (4-8) | [N] rischi | [N] rischi |
| Basso (1-3) | [N] rischi | [N] rischi |

### H.3 Accettabilità Rischio Residuo

**Il rischio residuo è accettabile?**

| Valutazione | Selezione |
|-------------|-----------|
| Sì - Rischio residuo accettabile | [ ] |
| Sì con monitoraggio - Rischio tollerabile con sorveglianza | [ ] |
| No - Necessarie ulteriori misure | [ ] |
| No - Consultazione Autorità richiesta (rischio elevato residuo) | [ ] |

---

## Sezione I: Parere DPO

### I.1 Parere Formale

**Data parere**: {{document_date}}

**Sintesi valutazione DPO**:

[Il DPO inserisce qui la propria valutazione sulla DPIA, includendo:
- Completezza dell'analisi
- Adeguatezza delle misure
- Conformità normativa
- Eventuali raccomandazioni]

### I.2 Raccomandazioni DPO

| # | Raccomandazione | Priorità | Accolta |
|---|-----------------|----------|---------|
| 1 | [Raccomandazione] | [Alta/Media/Bassa] | [ ] Sì [ ] No |
| 2 | [Raccomandazione] | [Alta/Media/Bassa] | [ ] Sì [ ] No |

**Se raccomandazione non accolta, motivazione**: [Spiegazione]

### I.3 Conclusione DPO

| Esito | Selezione |
|-------|-----------|
| Parere favorevole | [ ] |
| Parere favorevole con raccomandazioni | [ ] |
| Parere negativo - Non procedere | [ ] |
| Necessaria consultazione Autorità Garante | [ ] |

**Firma DPO**: _________________________ **Data**: _____________

---

## Sezione J: Decisione e Approvazione

### J.1 Decisione

| Opzione | Selezione |
|---------|-----------|
| **APPROVATO** - Procedere con il trattamento | [ ] |
| **APPROVATO CON CONDIZIONI** - Procedere dopo implementazione misure | [ ] |
| **RIMANDATO** - Necessarie modifiche alla DPIA | [ ] |
| **RESPINTO** - Non procedere con il trattamento | [ ] |
| **CONSULTAZIONE AUTORITÀ** - Procedere con consultazione Art. 36 | [ ] |

### J.2 Condizioni (se applicabile)

| # | Condizione | Responsabile | Deadline | Stato |
|---|------------|--------------|----------|-------|
| 1 | [Condizione] | [Nome] | [Data] | [ ] Completata |
| 2 | [Condizione] | [Nome] | [Data] | [ ] Completata |

### J.3 Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Responsabile DPIA | | | |
| Process Owner | | | |
| DPO | | | |
| [Direzione se richiesto] | | | |

---

## Sezione K: Monitoraggio e Revisione

### K.1 Piano di Monitoraggio

| Attività | Frequenza | Responsabile |
|----------|-----------|--------------|
| Review efficacia misure | Trimestrale | IT Security |
| Verifica KPI privacy | Mensile | Privacy Team |
| Audit controlli | Annuale | Internal Audit |
| Review DPIA | Annuale o a modifica significativa | Privacy Team |

### K.2 Trigger per Revisione DPIA

La DPIA deve essere rivista quando:
- [ ] Cambia significativamente il trattamento
- [ ] Cambiano le tecnologie utilizzate
- [ ] Cambiano i rischi identificati
- [ ] Si verifica un data breach
- [ ] Cambiano requisiti normativi
- [ ] Trascorso 1 anno dall'ultima revisione

### K.3 Registro Revisioni DPIA

| Data | Motivo | Modifiche | Autore | Approvato |
|------|--------|-----------|--------|-----------|
| | | | | |

---

## Allegati

### Allegato 1: Privacy Notice Associata

[Riferimento o copia]

### Allegato 2: Flusso Dati Dettagliato

[Diagramma dettagliato]

### Allegato 3: Documentazione Consultazioni

[Verbali, survey, feedback]

### Allegato 4: Documentazione Misure Tecniche

[Specifiche tecniche misure implementate]

---

## Documenti Correlati

| Documento | Riferimento | Relazione |
|-----------|-------------|-----------|
| Privacy Risk Assessment | `../risk-assessment/privacy-risk-assessment.md` | Metodologia valutazione rischi privacy |
| RoPA | `../registers/record-of-processing-activities.md` | Registro trattamenti oggetto di DPIA |
| Privacy Policy | `../policies/privacy-policy.md` | Basi giuridiche e finalità trattamento |
| Consent Management | `../procedures/consent-management-procedure.md` | Gestione consensi per trattamenti valutati |
| Data Breach Notification | `../procedures/data-breach-notification-procedure.md` | Procedura in caso di violazione |
| International Transfer Assessment | `../procedures/international-data-transfer-assessment.md` | Valutazione trasferimenti extra-UE |
| PIMS Scope | `../context/pims-scope.md` | Ambito sistema gestione privacy |
| Data Subject Rights | `../procedures/data-subject-rights-procedure.md` | Diritti interessati impattati |

---

## Checklist di Compilazione

Prima di considerare questa DPIA completa, verificare di aver compilato:

- [ ] {{document_date}} — Data emissione e revisione
- [ ] {{approver_name}} — Nome approvatore
- [ ] {{last_review_date}} / {{next_review_date}} — Date revisione
- [ ] Sezione A — Informazioni generali progetto/trattamento
- [ ] Sezione B — Descrizione trattamento con flussi dati
- [ ] Sezione C — Valutazione necessità e proporzionalità (Art. 35(7)(a)-(b))
- [ ] Sezione D — Consultazione interessati (Art. 35(9)) o giustificazione omissione
- [ ] Sezione E — Identificazione rischi con scala di probabilità e impatto
- [ ] Sezione F — Valutazione rischi pre-mitigazione e post-mitigazione
- [ ] Sezione G — Piano misure di mitigazione con responsabili e scadenze
- [ ] Sezione H — Parere DPO documentato (Art. 35(2))
- [ ] Sezione I — Valutazione necessità consultazione preventiva Garante (Art. 36)
- [ ] Sezione J — Approvazione con firme DPO + Process Owner + Direzione
- [ ] Sezione K — Piano di monitoraggio e trigger per revisione DPIA

---

*Template conforme a ISO/IEC 27701:2019 (7.2.5), GDPR Art. 35-36*
