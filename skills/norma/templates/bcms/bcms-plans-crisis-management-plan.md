---
title: Crisis Management Plan
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: '{{crisis_manager}}'
approver: '[CONSIGLIO DI AMMINISTRAZIONE]'
framework: ISO22301
iso_clauses:
  - Clausola 8.4.2 - Struttura di risposta agli incidenti
  - Clausola 8.4.3 - Avvertimento e comunicazione
  - Clausola 8.4.4 - Piani di continuità operativa
cross_references:
  - NIS2 Art. 21(2)(c) - Continuità operativa e gestione delle crisi
  - NIS2 Art. 23 - Obblighi di segnalazione
  - DORA Art. 11 - Risposta e ripristino
  - DORA Art. 19 - Segnalazione degli incidenti
  - GDPR Art. 33-34 - Notifica violazioni
  - ISO 22361 - Crisis management guidelines
status: Da compilare
subset: true
---

# Crisis Management Plan

## 1. Informazioni Documento

| Campo | Valore |
|-------|--------|
| Codice Documento | {{company_name}}-CMP-001 |
| Versione | 1.0 |
| Data Emissione | {{document_date}} |
| Prossima Revisione | [DATA + 12 mesi] |
| Classificazione | **RISERVATO** |
| Proprietario | [CEO / Crisis Manager] |
| Approvato da | [Consiglio di Amministrazione] |
| Ultimo Test | [Data ultima esercitazione] |

### 1.1 Distribuzione Controllata

| # | Ruolo | Nome | Formato |
|---|-------|------|---------|
| 1 | CEO | [Nome] | Digitale + Cartacea |
| 2 | CFO | [Nome] | Digitale + Cartacea |
| 3 | COO | [Nome] | Digitale + Cartacea |
| 4 | CHRO | [Nome] | Digitale + Cartacea |
| 5 | CMO/Comunicazione | [Nome] | Digitale + Cartacea |
| 6 | Legal Counsel | [Nome] | Digitale + Cartacea |
| 7 | BC Manager | [Nome] | Digitale + Cartacea |
| 8 | CISO | [Nome] | Digitale + Cartacea |

> **IMPORTANTE**: Questo piano contiene informazioni sensibili e procedure di gestione delle crisi. Deve essere trattato con la massima riservatezza.

---

## 2. Introduzione

### 2.1 Scopo

Il Crisis Management Plan definisce le strutture organizzative, i processi decisionali e le procedure di comunicazione che {{company_name}} attiva per gestire situazioni che trascendono l'ordinaria gestione delle emergenze. Una crisi si distingue da un semplice incidente per la sua natura strategica: rappresenta una minaccia esistenziale o reputazionale che richiede il coinvolgimento diretto dei vertici aziendali e decisioni che possono determinare il futuro dell'organizzazione.

Il presente piano si applica a eventi che minacciano la reputazione dell'organizzazione, mettendo a rischio la fiducia costruita nel tempo con clienti, partner e pubblico. Copre situazioni con impatto significativo sugli stakeholder, dove le conseguenze dell'evento si estendono oltre i confini operativi per coinvolgere comunità, investitori, autorità o media. Il piano viene attivato quando l'alta direzione deve assumere direttamente la guida della risposta, riconoscendo che le decisioni richieste superano l'autorità delegata ai livelli operativi.

Il piano è progettato per eventi che eccedono la capacità di gestione dei normali processi operativi, dove le procedure standard risultano inadeguate per la scala, la complessità o la velocità di evoluzione della situazione. Particolare attenzione viene dedicata a scenari con potenziale esposizione mediatica, dove la comunicazione diventa elemento critico quanto l'azione operativa, e dove errori di gestione possono amplificare il danno iniziale anziché contenerlo.

### 2.2 Differenza tra Incidente, Emergenza e Crisi

```
┌─────────────────────────────────────────────────────────────────┐
│                    SCALA DEGLI EVENTI                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  INCIDENTE                                                       │
│  ───────────────────────────────────────────────────────────    │
│  • Gestibile con procedure standard                              │
│  • Impatto limitato e contenuto                                  │
│  • Non richiede escalation management                           │
│  • Gestito da: Team operativi                                   │
│                      │                                           │
│                      ▼                                           │
│  EMERGENZA                                                       │
│  ───────────────────────────────────────────────────────────    │
│  • Richiede attivazione BCP                                     │
│  • Impatto significativo su operazioni                          │
│  • Possibile coinvolgimento stakeholder                         │
│  • Gestito da: BC Manager + CMT operativo                       │
│                      │                                           │
│                      ▼                                           │
│  CRISI                                                           │
│  ───────────────────────────────────────────────────────────    │
│  • Minaccia strategica per l'organizzazione                     │
│  • Impatto reputazionale significativo                          │
│  • Attenzione mediatica                                         │
│  • Coinvolgimento stakeholder critici                           │
│  • Gestito da: Crisis Management Team + Board                   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### 2.3 Tipi di Crisi

| Categoria | Esempi | Probabilità | Impatto |
|-----------|--------|-------------|---------|
| **Operativa** | Incidente grave, interruzione prolungata, failure supply chain | Media | Alto |
| **Reputazionale** | Scandalo, bad press, social media crisis | Media | Molto Alto |
| **Cyber/Data Breach** | Ransomware, leak dati, attacco DDoS | Alta | Molto Alto |
| **Legale/Compliance** | Sanzioni, indagini, cause legali | Bassa | Molto Alto |
| **Sicurezza** | Incidente sul lavoro, violenza, terrorismo | Bassa | Critico |
| **Finanziaria** | Crisi liquidità, frode, default fornitore critico | Bassa | Critico |
| **Ambientale** | Inquinamento, disastro naturale | Bassa | Alto |
| **Leadership** | Morte/incapacità CEO, dimissioni improvvise | Bassa | Alto |

---

## 3. Governance della Crisi

### 3.1 Struttura Organizzativa

```
┌─────────────────────────────────────────────────────────────────┐
│                    STRUTTURA CRISIS MANAGEMENT                   │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌───────────────────────────────────────────────────────────┐  │
│  │                   BOARD OF DIRECTORS                       │  │
│  │           (Supervisione strategica, decisioni critiche)    │  │
│  └─────────────────────────┬─────────────────────────────────┘  │
│                            │                                     │
│                            ▼                                     │
│  ┌───────────────────────────────────────────────────────────┐  │
│  │              CRISIS MANAGEMENT TEAM (CMT)                  │  │
│  │                                                            │  │
│  │  Crisis Leader (CEO)                                       │  │
│  │  ├── Deputy Leader (COO/CFO)                              │  │
│  │  ├── Comunicazione (CMO/PR Director)                      │  │
│  │  ├── Legale (General Counsel)                             │  │
│  │  ├── HR (CHRO)                                            │  │
│  │  ├── Operations (COO)                                     │  │
│  │  ├── IT/Security (CIO/CISO)                              │  │
│  │  └── Finance (CFO)                                        │  │
│  └─────────────────────────┬─────────────────────────────────┘  │
│                            │                                     │
│           ┌────────────────┼────────────────┐                   │
│           ▼                ▼                ▼                   │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐             │
│  │ COMMS TEAM  │  │ LEGAL TEAM  │  │ OPS TEAM    │             │
│  │             │  │             │  │             │             │
│  │ • Interna   │  │ • Contratti │  │ • BC/DR     │             │
│  │ • Esterna   │  │ • Regolatori│  │ • IT        │             │
│  │ • Media     │  │ • Assicuraz.│  │ • HR ops    │             │
│  │ • Social    │  │ • Contenzi. │  │ • Facility  │             │
│  └─────────────┘  └─────────────┘  └─────────────┘             │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### 3.2 Crisis Management Team (CMT)

| Ruolo | Nome | Cellulare | Email Personale | Backup |
|-------|------|-----------|-----------------|--------|
| **Crisis Leader** (CEO) | [Nome] | [Num] | [Email] | [Nome] |
| **Deputy Leader** (COO/CFO) | [Nome] | [Num] | [Email] | [Nome] |
| **Communications Lead** | [Nome] | [Num] | [Email] | [Nome] |
| **Legal Counsel** | [Nome] | [Num] | [Email] | [Nome] |
| **HR Lead** | [Nome] | [Num] | [Email] | [Nome] |
| **IT/Security Lead** | [Nome] | [Num] | [Email] | [Nome] |
| **Finance Lead** | [Nome] | [Num] | [Email] | [Nome] |
| **Operations Lead** | [Nome] | [Num] | [Email] | [Nome] |
| **BC Manager** (Coordinator) | [Nome] | [Num] | [Email] | [Nome] |

### 3.3 Responsabilità CMT

| Ruolo | Responsabilità Chiave |
|-------|----------------------|
| **Crisis Leader** | Decisioni strategiche, portavoce principale, comunicazione Board |
| **Deputy Leader** | Supporto al Leader, coordinamento team operativi, supplenza |
| **Communications Lead** | Strategia comunicazione, media relations, messaging |
| **Legal Counsel** | Consulenza legale, gestione regolatori, contratti, responsabilità |
| **HR Lead** | Welfare dipendenti, comunicazione interna, gestione personale |
| **IT/Security Lead** | Gestione incidenti IT, cyber response, continuità sistemi |
| **Finance Lead** | Impatto finanziario, assicurazioni, liquidità, stakeholder finanziari |
| **Operations Lead** | Continuità operativa, supply chain, facility |
| **BC Manager** | Coordinamento operativo, documentazione, logistica, follow-up |

### 3.4 Autorità Decisionale

| Decisione | Chi Decide | Chi Approva |
|-----------|------------|-------------|
| Dichiarazione crisi | CEO + 2 CMT | - |
| Comunicato stampa | Communications Lead | CEO |
| Notifica autorità | Legal Counsel | CEO |
| Spesa emergenza fino a €[X] | CFO | - |
| Spesa emergenza oltre €[X] | CFO | CEO |
| Sospensione operazioni | COO | CEO |
| Cessazione crisi | CEO | Board |

---

## 4. Attivazione della Crisi

### 4.1 Criteri di Attivazione

Il Crisis Management Plan viene attivato quando si verifica **UNO** dei seguenti:

| # | Criterio | Esempi |
|---|----------|--------|
| 1 | **Minaccia reputazionale significativa** | Articoli negativi media nazionali, viralità social negativa |
| 2 | **Impatto su stakeholder critici** | Clienti enterprise, investitori, partner strategici |
| 3 | **Attenzione mediatica** | Richieste stampa, presenza giornalisti |
| 4 | **Coinvolgimento autorità** | Indagini, ispezioni, sanzioni potenziali |
| 5 | **Incidente con vittime/feriti gravi** | Incidenti sul lavoro con conseguenze serie |
| 6 | **Data breach significativo** | Dati sensibili esposti, >10.000 record |
| 7 | **Interruzione prolungata** | Operazioni ferme >24h senza recovery prevedibile |
| 8 | **Evento eccezionale** | Situazione non prevista che richiede decisioni strategiche |

### 4.2 Processo di Escalation a Crisi

```
FLUSSO ESCALATION
═══════════════════════════════════════════════════════════════════

  RILEVAMENTO EVENTO
         │
         ▼
  ┌─────────────────────┐
  │ Valutazione iniziale │
  │ (Manager/BC Manager) │
  └──────────┬──────────┘
             │
             ▼
  ┌─────────────────────────────────────────────┐
  │ CRITERI CRISI SODDISFATTI?                  │
  │                                             │
  │ • Impatto reputazionale?          ☐ Sì/No │
  │ • Stakeholder critici coinvolti?  ☐ Sì/No │
  │ • Attenzione mediatica?           ☐ Sì/No │
  │ • Autorità coinvolte?             ☐ Sì/No │
  │ • Vittime/feriti?                 ☐ Sì/No │
  │ • Data breach significativo?      ☐ Sì/No │
  │                                             │
  │ Se almeno 1 Sì → ATTIVA CMT                │
  └──────────┬──────────────────────┬──────────┘
             │ NO                   │ SÌ
             ▼                      ▼
  ┌─────────────────┐    ┌─────────────────────┐
  │ Gestione BCP    │    │ ATTIVAZIONE CMT     │
  │ (BC Manager)    │    │                     │
  └─────────────────┘    │ 1. Notifica CEO     │
                         │ 2. Convoca CMT      │
                         │ 3. First briefing   │
                         │ 4. War room setup   │
                         └─────────────────────┘
```

### 4.3 Notifica CMT

**Procedura di notifica (responsabile: BC Manager o primo rilevatore senior)**:

1. Chiamare Crisis Leader (CEO): [NUMERO]
2. Se non raggiungibile entro 10 min, chiamare Deputy Leader: [NUMERO]
3. Confermare attivazione CMT
4. Utilizzare messaggio standard:

```
MESSAGGIO ATTIVAZIONE CMT
─────────────────────────────────────────────────────────────────

"{{contact_name}}, sono {{your_name}}.

Stiamo attivando il Crisis Management Team per:
[BREVE DESCRIZIONE SITUAZIONE]

Richiedo convocazione CMT entro [X] minuti.

Conference bridge: [NUMERO] PIN: [PIN]

Attendo conferma."
```

---

## 5. Gestione della Crisi

### 5.1 Prime 2 Ore (Golden Hours)

Le prime ore sono critiche per il controllo della narrativa e la gestione dell'impatto.

#### Checklist Prime 2 Ore

| # | Azione | Responsabile | Entro | ✓ |
|---|--------|--------------|-------|---|
| 1 | Confermare attivazione CMT | BC Manager | T+15min | ☐ |
| 2 | Allertare tutti i membri CMT | BC Manager | T+30min | ☐ |
| 3 | Setup War Room (fisico/virtuale) | BC Manager | T+30min | ☐ |
| 4 | First CMT briefing | Crisis Leader | T+1h | ☐ |
| 5 | Raccolta fatti confermati | Tutti CMT | T+1h | ☐ |
| 6 | Assessment impatto | CMT | T+1.5h | ☐ |
| 7 | Strategia comunicazione iniziale | Comms Lead | T+1.5h | ☐ |
| 8 | Holding statement pronto | Comms Lead | T+2h | ☐ |
| 9 | Identificazione stakeholder prioritari | CMT | T+2h | ☐ |
| 10 | Piano azione immediate | Crisis Leader | T+2h | ☐ |

### 5.2 War Room

#### Setup Fisico

| Elemento | Dettaglio | Status |
|----------|-----------|--------|
| **Location** | [Sala/Indirizzo] | ☐ Ready |
| **Backup location** | [Sala alternativa] | ☐ Ready |
| **Telefoni** | [N.] linee dedicate | ☐ Ready |
| **Video conference** | [Sistema] | ☐ Ready |
| **TV/Monitor** | Per news feed | ☐ Ready |
| **Whiteboard** | Per timeline/azioni | ☐ Ready |
| **Stampante** | Per documenti urgenti | ☐ Ready |
| **Refresh** | Acqua, caffè, snack | ☐ Ready |

#### Setup Virtuale

| Elemento | Dettaglio |
|----------|-----------|
| **Video call** | [Link permanente] |
| **Chat** | [Canale dedicato] |
| **Document sharing** | [Cartella condivisa] |
| **Task tracking** | [Tool/Board] |

### 5.3 Briefing CMT

#### Struttura Briefing Standard (30 minuti)

```
AGENDA BRIEFING CMT
═══════════════════════════════════════════════════════════════════

1. SITUAZIONE ATTUALE (5 min)
   Leader: BC Manager
   • Fatti confermati
   • Sviluppi dall'ultimo briefing
   • Timeline eventi

2. IMPATTO (5 min)
   Leader: Responsabile area coinvolta
   • Impatto operativo
   • Impatto stakeholder
   • Impatto reputazionale

3. COMUNICAZIONE (5 min)
   Leader: Communications Lead
   • Copertura media
   • Social media sentiment
   • Comunicazioni effettuate
   • Messaggi da approvare

4. AZIONI LEGALI/COMPLIANCE (3 min)
   Leader: Legal Counsel
   • Obblighi normativi
   • Notifiche effettuate
   • Rischi legali

5. AZIONI IN CORSO (5 min)
   Leader: Responsabili azione
   • Status azioni assegnate
   • Blocchi/problemi

6. DECISIONI RICHIESTE (5 min)
   Leader: Crisis Leader
   • Decisioni da prendere
   • Approvazioni necessarie

7. NEXT STEPS (2 min)
   Leader: Crisis Leader
   • Azioni da assegnare
   • Prossimo briefing
```

#### Frequenza Briefing

| Fase | Frequenza |
|------|-----------|
| Prime 24 ore | Ogni 2-3 ore |
| Giorni 2-3 | Ogni 4-6 ore |
| Fase stabilizzazione | 2 volte al giorno |
| Fase chiusura | Giornaliero |

### 5.4 Documentazione

#### Crisis Log

Il BC Manager mantiene un log continuo di tutti gli eventi:

```
╔════════════════════════════════════════════════════════════════╗
║                     CRISIS LOG                                  ║
║              Crisi: [NOME CRISI]                                ║
║              Data inizio: {{datetime}}                            ║
╠════════════════════════════════════════════════════════════════╣
║                                                                  ║
║ DATA/ORA    | EVENTO/AZIONE          | RESPONSABILE | NOTE      ║
║ ────────────┼────────────────────────┼──────────────┼────────── ║
║ [GG/MM HH:MM] │ [Descrizione]        │ [Nome]       │ [Note]    ║
║ [GG/MM HH:MM] │ [Descrizione]        │ [Nome]       │ [Note]    ║
║ [GG/MM HH:MM] │ [Descrizione]        │ [Nome]       │ [Note]    ║
║                                                                  ║
╚════════════════════════════════════════════════════════════════╝
```

---

## 6. Comunicazione di Crisi

### 6.1 Principi di Comunicazione

| Principio | Descrizione |
|-----------|-------------|
| **Velocità** | Prima comunicazione entro 1-2 ore |
| **Accuratezza** | Solo fatti verificati, mai speculazioni |
| **Trasparenza** | Ammettere ciò che non si sa, impegno ad aggiornare |
| **Empatia** | Riconoscere impatto su persone, non solo business |
| **Coerenza** | Stesso messaggio su tutti i canali |
| **Controllo** | Una sola voce, messaggi approvati |

### 6.2 Stakeholder e Priorità

| Priorità | Stakeholder | Canale | Responsabile | Timing |
|----------|-------------|--------|--------------|--------|
| **1** | Dipendenti | Email/Intranet/Town Hall | HR Lead | Entro 2h |
| **1** | Vittime/Familiari (se applicabile) | Di persona/Telefono | HR Lead + CEO | Immediato |
| **1** | Board/Investitori | Call dedicata | CEO/CFO | Entro 4h |
| **2** | Clienti enterprise | Telefono + Email | Account Director | Entro 4h |
| **2** | Autorità (se richiesto) | Canali formali | Legal | Da norma |
| **2** | Partner strategici | Telefono | Commercial Lead | Entro 8h |
| **3** | Media | Comunicato/Intervista | Comms Lead + CEO | Entro 4-8h |
| **3** | Clienti generici | Email/Web | Comms Lead | Entro 24h |
| **4** | Pubblico generico | Social/Web | Comms Lead | Ongoing |

### 6.3 Template Comunicazioni

#### Holding Statement (Prima comunicazione)

```
HOLDING STATEMENT
─────────────────────────────────────────────────────────────────

{{company_name}} conferma di essere a conoscenza di
[DESCRIZIONE GENERICA DELL'EVENTO].

La sicurezza [dei nostri dipendenti/dei nostri clienti/delle
informazioni] è la nostra priorità assoluta.

Stiamo lavorando attivamente per [AZIONE GENERICA] e stiamo
collaborando con [AUTORITÀ/ESPERTI] dove appropriato.

Forniremo aggiornamenti non appena saranno disponibili
ulteriori informazioni.

Per informazioni: {{press_contact}}

{{datetime}}
```

#### Comunicazione Dipendenti

```
COMUNICAZIONE INTERNA - [OGGETTO]
─────────────────────────────────────────────────────────────────

Cari colleghi,

Come alcuni di voi sapranno, [DESCRIZIONE SITUAZIONE].

COSA È SUCCESSO
[Fatti confermati - nessuna speculazione]

COSA STIAMO FACENDO
[Azioni concrete in corso]

COSA SIGNIFICA PER VOI
[Impatto diretto sui dipendenti e cosa devono fare]

COSA NON FARE
• Non rilasciare dichiarazioni a media esterni
• Indirizzare tutte le richieste stampa a {{contact}}
• Non speculare sui social media
• Rispettare la riservatezza delle informazioni

VI TERREMO AGGIORNATI
Riceverete un aggiornamento entro [TIMING].

Per domande: {{internal_contact}}

{{ceo_hr_name}}
{{datetime}}
```

#### Q&A Preparati

Per ogni crisi, preparare risposte a domande prevedibili:

| Domanda | Risposta Approvata |
|---------|-------------------|
| Cosa è successo? | [Risposta] |
| Quando è successo? | [Risposta] |
| Chi è coinvolto? | [Risposta] |
| Qual è l'impatto? | [Risposta] |
| Cosa state facendo? | [Risposta] |
| Di chi è la responsabilità? | [Risposta] |
| Come eviterete che si ripeta? | [Risposta] |

### 6.4 Media Management

#### Principi Media Relations

- **UN solo portavoce** designato (normalmente CEO)
- **MAI** dire "no comment" - usare holding statement
- **MAI** speculare o attribuire colpe
- **MAI** mentire - ammettere di non sapere
- **SEMPRE** registrare interviste
- **SEMPRE** briefing pre-intervista

#### Portavoce

| Tipo Media | Portavoce Primario | Backup |
|------------|-------------------|--------|
| Stampa nazionale | CEO | CFO/COO |
| TV | CEO | Communications Director |
| Stampa trade | Communications Director | Product/Service Lead |
| Social Media | Social Media Manager | Communications Director |

### 6.5 Social Media

#### Monitoraggio

- Attivare monitoraggio continuo menzioni
- Alert per keyword specifici
- Report ogni 2 ore in fase acuta

#### Risposta Social

| Tipo Post | Risposta |
|-----------|----------|
| Richiesta informazioni | Indirizzare a comunicazione ufficiale |
| Fake news | Correggere con fatti, link a fonte ufficiale |
| Commento negativo emotivo | Non rispondere direttamente, monitorare |
| Post virale negativo | Escalation immediata a Communications Lead |
| Minacce/Illeciti | Screenshot, report, escalation Legal |

---

## 7. Obblighi di Notifica

### 7.1 Notifiche Obbligatorie per Legge

| Evento | Autorità | Termine | Responsabile | Riferimento |
|--------|----------|---------|--------------|-------------|
| **Data breach** (dati personali) | Garante Privacy | 72 ore | DPO | GDPR Art. 33 |
| **Data breach** (interessati) | Interessati | "Senza ritardo" | DPO | GDPR Art. 34 |
| **Incidente significativo NIS2** | ACN/CSIRT | 24h alert, 72h report | CISO | NIS2 Art. 23 |
| **Incidente ICT grave DORA** | Autorità vigilanza | 4h alert, 72h report | Compliance | DORA Art. 19 |
| **Incidente sicurezza lavoro** | INAIL/ASL | 48h | HR/HSE | D.Lgs 81/08 |
| **Evento ambientale** | ARPA | Immediato | Facility | TU Ambiente |

### 7.2 Template Notifica Garante Privacy (GDPR Art. 33)

```
NOTIFICA VIOLAZIONE DATI PERSONALI
─────────────────────────────────────────────────────────────────

1. TITOLARE DEL TRATTAMENTO
   Nome: [Organizzazione]
   Contatto: {{dpo_title}}
   Email: [Email DPO]

2. DESCRIZIONE DELLA VIOLAZIONE
   Data/ora scoperta: {{datetime}}
   Natura della violazione: [Descrizione]
   Categorie dati coinvolti: [Elenco]
   Numero interessati (stimato): [Numero]

3. CONSEGUENZE PROBABILI
   [Descrizione rischi per gli interessati]

4. MISURE ADOTTATE
   [Azioni di contenimento]
   [Azioni di mitigazione]

5. NOTIFICA INTERESSATI
   ☐ Effettuata  ☐ Non necessaria  ☐ Pianificata per {{document_date}}

Data notifica: {{document_date}}
Firma DPO: _______________
```

---

## 8. Scenari Specifici

### 8.1 Scenario: Data Breach / Cyber Attack

**Trigger**: Scoperta esfiltrazione dati, ransomware, compromissione sistemi

**Azioni Immediate**:

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Contenimento tecnico (isolamento) | CISO/IT | Immediato |
| 2 | Assessment scope | CISO | 2h |
| 3 | Attivazione CMT | BC Manager | 1h |
| 4 | Valutazione obbligo notifica GDPR | DPO | 4h |
| 5 | Valutazione obbligo notifica NIS2/DORA | Compliance | 4h |
| 6 | Comunicazione dipendenti | HR | 4h |
| 7 | Comunicazione clienti (se dati esposti) | Comms | 24h |
| 8 | Notifica Garante (se necessario) | DPO | 72h |

**Decisioni CMT**:
- Pagare/Non pagare riscatto (Ransomware)
- Coinvolgere forze dell'ordine
- Comunicazione pubblica timing/contenuto
- Notifica interessati

### 8.2 Scenario: Incidente con Vittime/Feriti

**Trigger**: Incidente sul lavoro grave, incidente che coinvolge terzi

**Azioni Immediate**:

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Chiamata emergenza (112) | Chiunque | Immediato |
| 2 | Primo soccorso | Addetti | Immediato |
| 3 | Messa in sicurezza area | HSE | Immediato |
| 4 | Notifica management | Manager area | 15min |
| 5 | Attivazione CMT | CEO | 30min |
| 6 | Contatto familiari vittime | HR/CEO | ASAP |
| 7 | Preservazione scena (per indagini) | HSE/Legal | Immediato |
| 8 | Notifica INAIL/Autorità | HR/HSE | 48h |

**Priorità comunicazione**:
1. Familiari delle vittime (priorità assoluta, di persona se possibile)
2. Dipendenti presenti/testimoni
3. Tutti i dipendenti
4. Autorità
5. Media (se necessario)

### 8.3 Scenario: Crisi Reputazionale

**Trigger**: Articolo stampa negativo, scandal, social media crisis

**Azioni Immediate**:

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Raccolta articoli/post | Comms | 30min |
| 2 | Assessment verità delle accuse | Legal | 1h |
| 3 | Attivazione CMT | Crisis Leader | 1h |
| 4 | Preparazione holding statement | Comms | 2h |
| 5 | Briefing portavoce | Comms | 2h |
| 6 | Risposta coordinata | Comms | 4h |
| 7 | Monitoraggio continuo | Comms | Ongoing |

**Strategia di risposta** (decidere in CMT):
- ☐ Silenzio tattico (monitorare senza rispondere)
- ☐ Risposta fattuale (correggere errori)
- ☐ Scuse (se responsabilità accertata)
- ☐ Azione legale (diffamazione)
- ☐ Proactive outreach a stakeholder chiave

### 8.4 Scenario: Indisponibilità Leadership

**Trigger**: Morte, incapacità, dimissioni improvvise di CEO o figure chiave

**Azioni Immediate**:

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Attivazione successore designato | Board | Immediato |
| 2 | Comunicazione interna | HR + Successore | 2h |
| 3 | Comunicazione Board completo | Chairman | 4h |
| 4 | Comunicazione investitori (se quotata) | CFO/IR | 24h |
| 5 | Comunicazione clienti/partner chiave | Successore | 24h |
| 6 | Comunicazione stampa | Comms | 24h |

**Piano successione** (allegato): vedi documento {{company_name}}-SUC-001

---

## 9. Chiusura della Crisi

### 9.1 Criteri di Chiusura

La crisi può essere dichiarata conclusa quando:

- [ ] Situazione operativa stabilizzata/risolta
- [ ] Comunicazione stakeholder completata
- [ ] Nessuna nuova copertura media negativa da 48h
- [ ] Azioni immediate completate
- [ ] Piano follow-up definito
- [ ] Approvazione Crisis Leader

### 9.2 Processo di Chiusura

| # | Azione | Responsabile |
|---|--------|--------------|
| 1 | Proposta chiusura crisi | BC Manager |
| 2 | Validazione criteri di chiusura | CMT |
| 3 | Approvazione chiusura | Crisis Leader |
| 4 | Comunicazione fine crisi (interna) | HR |
| 5 | Comunicazione fine crisi (esterna se appropriato) | Comms |
| 6 | Stand-down War Room | BC Manager |
| 7 | Avvio Post-Crisis Review | BC Manager |

### 9.3 Post-Crisis Review

Entro 2 settimane dalla chiusura:

#### Partecipanti
Tutti i membri CMT + stakeholder chiave coinvolti

#### Agenda
1. Timeline eventi
2. Cosa ha funzionato bene
3. Cosa non ha funzionato
4. Comunicazione: efficacia e tempestività
5. Decisioni: qualità e velocità
6. Preparazione: gap identificati
7. Azioni di miglioramento

#### Output
- Report Post-Crisis
- Azioni correttive con owner e deadline
- Update a piani e procedure
- Lessons learned per training

---

## 10. Formazione e Esercitazioni

### 10.1 Formazione CMT

| Formazione | Frequenza | Partecipanti |
|------------|-----------|--------------|
| Induction nuovi membri CMT | On boarding | Nuovo membro |
| Refresh ruoli e responsabilità | Annuale | Tutto CMT |
| Media training portavoce | Annuale | CEO, Comms Lead |
| Simulazione crisi completa | Annuale | Tutto CMT |
| Tabletop specifico per scenario | Semestrale | CMT + team rilevanti |

### 10.2 Esercitazioni

Vedi Exercise Programme {{company_name}}-EXP-001 per dettagli.

Esercitazioni specifiche crisis management:
- **Tabletop crisi reputazionale**: Semestrale
- **Tabletop data breach**: Semestrale
- **Simulazione crisi con media**: Annuale
- **Test attivazione CMT**: Trimestrale

---

## 11. Manutenzione del Piano

### 11.1 Review e Aggiornamento

| Elemento | Frequenza | Responsabile |
|----------|-----------|--------------|
| Contact list CMT | Trimestrale | BC Manager |
| Review piano completo | Annuale | BC Manager + CMT |
| Test procedure attivazione | Semestrale | BC Manager |
| Update post-crisi reale | Dopo ogni crisi | BC Manager |

### 11.2 Trigger Revisione Straordinaria

- Cambio CEO o membri chiave CMT
- Acquisizioni/fusioni significative
- Nuovi requisiti normativi
- Lessons learned da crisi reale
- Cambio significativo business model/mercato

---

## 12. Allegati

- **Allegato A**: Contact List CMT (Confidenziale - distribuzione separata)
- **Allegato B**: Template Comunicazioni Pre-Approvati
- **Allegato C**: Checklist per Scenario
- **Allegato D**: Q&A Framework
- **Allegato E**: Media Contact List
- **Allegato F**: Piano Successione Leadership
- **Allegato G**: Accordi con Consulenti Crisis (PR, Legal)

---

## 13. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 14. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{bc_manager}} | | {{document_date}} |
| Verificato da | {{legal_counsel}} | | {{document_date}} |
| Verificato da | {{communications_director}} | | {{document_date}} |
| Approvato da | {{ceo}} | | {{document_date}} |
| Approvato da | {{board_chair}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Business Continuity Policy | {{company_name}}-POL-BCMS-001 | Policy di riferimento |
| Business Continuity Plan | {{company_name}}-BCP-BCMS-001 | Piano attivato dal CMT |
| IT Disaster Recovery Plan | {{company_name}}-DRP-BCMS-001 | Recovery IT durante crisi |
| Recovery Procedure | {{company_name}}-REC-BCMS-001 | Procedure operative |
| Incident Management (ISMS) | {{company_name}}-INC-ISMS-001 | Escalation da incidenti |
| Exercise Programme | {{company_name}}-EXR-BCMS-001 | Test del CMP |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{ceo}}` | Approvazioni — Crisis Leader designato | ☐ |
| 5 | `{{bc_manager}}` | Redatto da | ☐ |
| 6 | Crisis Management Team | Sezione 3 — tutti i membri nominati con contatti | ☐ |
| 7 | Criteri di attivazione | Sezione 2 — soglie specifiche per l'Organizzazione | ☐ |
| 8 | Template comunicazione | Sezione 7 — template adattati al brand aziendale | ☐ |
| 9 | Portavoce designato | Sezione 8 — spokesperson identificato e formato | ☐ |
| 10 | Contatti media e autorita | Sezione 9 — lista aggiornata | ☐ |
| 11 | Test CMP eseguito | Almeno un tabletop con scenario di crisi completato | ☐ |

---

*Template conforme a ISO 22301:2019 Clausola 8.4.2*
*Creato con Kynosure.ai*
