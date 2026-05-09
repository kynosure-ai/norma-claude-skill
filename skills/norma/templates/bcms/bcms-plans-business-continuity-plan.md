---
title: Business Continuity Plan (BCP)
version: '2.0'
date: '{{document_date}}'
classification: Riservato
owner: '{{bc_manager}}'
approver: '{{senior_management}}'
framework: ISO22301
iso_clauses:
  - Clausola 8.4.1 - Generale (pianificazione e controllo operativi)
  - Clausola 8.4.2 - Struttura di risposta agli incidenti
  - Clausola 8.4.4 - Piani di continuità operativa
  - Clausola 8.4.5 - Recupero
cross_references:
  - NIS2 Art. 21(2)(c) - Continuità operativa e gestione delle crisi
  - DORA Art. 11 - Risposta e ripristino
  - DORA Art. 12 - Politiche e procedure di backup
  - ISO 27001 A.5.29 - Sicurezza informazioni durante interruzioni
  - ISO 27001 A.5.30 - Prontezza ICT per continuità operativa
status: Da compilare
subset: true
---

# Business Continuity Plan (BCP)

## 1. Informazioni Documento

| Campo | Valore |
|-------|--------|
| Codice Documento | {{company_name}}-BCP-001 |
| Versione | 2.0 |
| Data Emissione | {{document_date}} |
| Prossima Revisione | [DATA + 6 mesi] |
| Classificazione | **RISERVATO** |
| Proprietario | [BC Manager] |
| Approvato da | [Direzione Generale] |
| Ultimo Test | [Data ultimo test] |

### 1.1 Distribuzione Controllata

| # | Ruolo | Nome | Formato | Data Consegna |
|---|-------|------|---------|---------------|
| 1 | CEO | [Nome] | Digitale + Cartacea | [Data] |
| 2 | BC Manager | [Nome] | Digitale + Cartacea | [Data] |
| 3 | IT Manager | [Nome] | Digitale + Cartacea | [Data] |
| 4 | HR Manager | [Nome] | Digitale | [Data] |
| 5 | Operations Manager | [Nome] | Digitale | [Data] |
| 6 | CFO | [Nome] | Digitale | [Data] |

> **IMPORTANTE**: Questo piano deve essere accessibile anche offline. Mantenere:
> - Copia cartacea in: [UBICAZIONE FISICA]
> - Copia digitale offline su: [USB/DISCO ESTERNO]
> - Copia cloud in: [SHAREPOINT/DRIVE]

---

## 2. Scopo e Ambito

### 2.1 Scopo

Il Business Continuity Plan costituisce il documento operativo principale per la gestione delle interruzioni significative alle attività di {{company_name}}. Questo piano traduce le strategie di continuità definite a livello aziendale in procedure concrete e immediatamente attuabili, fornendo al personale le istruzioni necessarie per rispondere efficacemente alle emergenze.

Il documento definisce la struttura organizzativa di crisi, specificando chi assume la leadership durante le emergenze e come i vari team si coordinano per gestire la risposta e il ripristino. I criteri e le procedure di attivazione assicurano che il piano venga invocato al momento appropriato, evitando sia attivazioni premature sia ritardi nella risposta. Le fasi di risposta, gestione crisi e recovery sono descritte in sequenza logica, permettendo una progressione ordinata dalla prima reazione all'emergenza fino al ritorno alla piena operatività.

La chiara definizione di ruoli, responsabilità e catena di comando elimina ambiguità su chi deve fare cosa e chi ha autorità decisionale nelle diverse fasi della crisi. Le procedure di comunicazione interna ed esterna garantiscono che le informazioni fluiscano correttamente verso dipendenti, clienti, fornitori, media e autorità. L'identificazione delle risorse necessarie per il ripristino supporta una mobilitazione rapida di quanto occorre per riportare i processi critici al livello operativo minimo accettabile.

### 2.2 Ambito di Applicazione

| Elemento | Copertura |
|----------|-----------|
| **Processi** | [Lista processi critici - da BIA] |
| **Sedi** | [Sede principale], [Sedi secondarie] |
| **Sistemi IT** | [Sistemi critici - da BIA] |
| **Personale** | [N] dipendenti nell'ambito |
| **Fornitori** | [Fornitori critici identificati] |

### 2.3 Obiettivi di Recovery (da BIA)

| # | Processo | MTPD | RTO | RPO | MBCO |
|---|----------|------|-----|-----|------|
| 1 | [Processo critico 1] | [X]h | [X]h | [X]h | [X]% |
| 2 | [Processo critico 2] | [X]h | [X]h | [X]h | [X]% |
| 3 | [Processo critico 3] | [X]h | [X]h | [X]h | [X]% |
| 4 | [Processo critico 4] | [X]h | [X]h | [X]h | [X]% |
| 5 | [Processo critico 5] | [X]h | [X]h | [X]h | [X]% |

> **Riferimento**: Business Impact Analysis {{company_name}}-BIA-001

### 2.4 Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| BC Policy | {{company_name}}-POL-BC-001 | Governance |
| Business Impact Analysis | {{company_name}}-BIA-001 | Input MTPD/RTO |
| BC Risk Assessment | {{company_name}}-RA-BC-001 | Scenari rischio |
| BC Strategy | {{company_name}}-STR-BC-001 | Strategie recovery |
| IT Disaster Recovery Plan | {{company_name}}-DRP-001 | Recovery IT |
| Crisis Management Plan | {{company_name}}-CMP-001 | Gestione crisi |

---

## 3. Struttura Organizzativa di Crisi

### 3.1 Organigramma di Emergenza

```
                         ┌─────────────────────────┐
                         │   CRISIS MANAGEMENT     │
                         │        TEAM (CMT)       │
                         │   Leader: {{name_role}}  │
                         └───────────┬─────────────┘
                                     │
        ┌────────────────────────────┼────────────────────────────┐
        │                            │                            │
        ▼                            ▼                            ▼
┌───────────────────┐    ┌───────────────────┐    ┌───────────────────┐
│ EMERGENCY         │    │ BUSINESS          │    │ COMMUNICATIONS    │
│ RESPONSE TEAM     │    │ RECOVERY TEAM     │    │ TEAM              │
│                   │    │                   │    │                   │
│ • Sicurezza       │    │ • Process Owner   │    │ • Comunicazione   │
│ • Primo soccorso  │    │ • Operations      │    │ • HR              │
│ • Evacuazione     │    │ • Finance         │    │ • Legal           │
└─────────┬─────────┘    └─────────┬─────────┘    └───────────────────┘
          │                        │
          ▼                        ▼
┌───────────────────┐    ┌───────────────────┐
│ IT RECOVERY       │    │ LOGISTICS         │
│ TEAM              │    │ TEAM              │
│                   │    │                   │
│ • Infrastruttura  │    │ • Facility        │
│ • Applicazioni    │    │ • Procurement     │
│ • Network         │    │ • Trasporti       │
└───────────────────┘    └───────────────────┘
```

### 3.2 Crisis Management Team (CMT)

| Ruolo | Titolare | Backup | Cellulare | Email |
|-------|----------|--------|-----------|-------|
| **CMT Leader** | [Nome] | [Nome] | [Num] | [Email] |
| **Deputy Leader** | [Nome] | [Nome] | [Num] | [Email] |
| **BC Manager** | [Nome] | [Nome] | [Num] | [Email] |
| **IT Manager** | [Nome] | [Nome] | [Num] | [Email] |
| **HR Manager** | [Nome] | [Nome] | [Num] | [Email] |
| **Comunicazione** | [Nome] | [Nome] | [Num] | [Email] |
| **Legal** | [Nome] | [Nome] | [Num] | [Email] |
| **Finance** | [Nome] | [Nome] | [Num] | [Email] |
| **Operations** | [Nome] | [Nome] | [Num] | [Email] |

**Responsabilità CMT**:
- Valutazione situazione e dichiarazione stato emergenza/crisi
- Decisioni strategiche di risposta
- Allocazione e prioritizzazione risorse
- Comunicazione verso stakeholder esterni
- Approvazione comunicati stampa
- Dichiarazione ritorno alla normalità

### 3.3 Team di Recovery

#### Emergency Response Team (ERT)

| Ruolo | Nome | Backup | Contatto |
|-------|------|--------|----------|
| ERT Leader | [Nome] | [Nome] | [Num] |
| Responsabile Sicurezza | [Nome] | [Nome] | [Num] |
| Addetto Primo Soccorso | [Nome] | [Nome] | [Num] |
| Addetto Antincendio | [Nome] | [Nome] | [Num] |

**Responsabilità**: Risposta immediata, sicurezza personale, evacuazione, primo contenimento

#### IT Recovery Team

| Ruolo | Nome | Backup | Contatto |
|-------|------|--------|----------|
| IT Recovery Leader | [Nome] | [Nome] | [Num] |
| DBA | [Nome] | [Nome] | [Num] |
| Network Admin | [Nome] | [Nome] | [Num] |
| System Admin | [Nome] | [Nome] | [Num] |
| Security | [Nome] | [Nome] | [Num] |

**Responsabilità**: Ripristino sistemi IT, attivazione DR, supporto tecnico

#### Business Recovery Team

| Ruolo | Nome | Backup | Contatto |
|-------|------|--------|----------|
| BR Leader | [Nome] | [Nome] | [Num] |
| Process Owner - [Processo 1] | [Nome] | [Nome] | [Num] |
| Process Owner - [Processo 2] | [Nome] | [Nome] | [Num] |
| Process Owner - [Processo 3] | [Nome] | [Nome] | [Num] |

**Responsabilità**: Ripristino processi business, workaround operativi, ritorno normalità

---

## 4. Autorità ed Escalation

### 4.1 Livelli di Emergenza

| Livello | Nome | Chi Dichiara | Criteri |
|---------|------|--------------|---------|
| **0** | Normale | - | Operatività standard |
| **1** | Incidente | Manager Area | Interruzione contenuta < 2h |
| **2** | Emergenza | BC Manager | Interruzione 2-4h, rischio escalation |
| **3** | Crisi | CMT Leader | Interruzione > 4h, impatto significativo |
| **4** | Disastro | CEO | Impatto catastrofico, DR completo |

### 4.2 Matrice di Escalation

```
TIMELINE ESCALATION
═══════════════════════════════════════════════════════════════════

T+0 min     RILEVAMENTO
            ├── Identificazione evento
            ├── Primo assessment
            └── Se urgente: primo intervento
                    │
T+15 min    NOTIFICA INIZIALE
            ├── Manager di area informato
            ├── Valutazione impatto preliminare
            └── Decisione: gestione locale o escalation
                    │
T+30 min    ESCALATION LIVELLO 2
            ├── BC Manager notificato
            ├── Assessment dettagliato
            └── Convocazione team se necessario
                    │
T+1-2 ore   ESCALATION LIVELLO 3
            ├── CMT convocato
            ├── Dichiarazione formale crisi
            └── Attivazione BCP
                    │
T+2+ ore    GESTIONE CRISI STRUTTURATA
            ├── Implementazione procedure
            ├── Comunicazione stakeholder
            └── Recovery operations
```

### 4.3 Criteri di Attivazione BCP

Il BCP viene **attivato** quando si verifica **UNO** dei seguenti:

| Criterio | Soglia |
|----------|--------|
| ☐ | Interruzione processo critico > MTPD |
| ☐ | Sede principale inaccessibile > 4 ore |
| ☐ | Failure sistema IT critico senza recovery entro RTO |
| ☐ | Indisponibilità > 30% personale chiave |
| ☐ | Evento che richiede attivazione sito alternativo |
| ☐ | Incidente con impatto su stakeholder esterni |
| ☐ | Richiesta da autorità competenti |
| ☐ | Incidente di sicurezza informatica significativo |
| ☐ | Evento mediatico che richiede crisis communication |

---

## 5. Fasi di Risposta

### Fase 0: Rilevamento e Allarme (0-30 minuti)

**Obiettivi**: Identificare l'evento, garantire sicurezza immediata, iniziare assessment

#### Checklist Fase 0

| # | Azione | Responsabile | Tempo | ✓ |
|---|--------|--------------|-------|---|
| 0.1 | Rilevare l'evento | Chiunque | T+0 | ☐ |
| 0.2 | Valutare sicurezza immediata personale | Manager presente | T+5min | ☐ |
| 0.3 | Se pericolo: attivare piano evacuazione | ERT Leader | Immediato | ☐ |
| 0.4 | Notificare BC Manager (cell: [NUM]) | Primo rilevatore | T+10min | ☐ |
| 0.5 | Raccogliere informazioni iniziali | BC Manager | T+20min | ☐ |
| 0.6 | Compilare Modulo Segnalazione Iniziale | Primo rilevatore | T+30min | ☐ |
| 0.7 | Valutare necessità escalation | BC Manager | T+30min | ☐ |

#### Modulo Segnalazione Iniziale

```
╔════════════════════════════════════════════════════════════════╗
║              MODULO SEGNALAZIONE EVENTO/INCIDENTE              ║
╠════════════════════════════════════════════════════════════════╣
║                                                                ║
║  DATA/ORA RILEVAMENTO: ____/____/______  ____:____            ║
║  SEGNALATO DA: ___________________ Tel: _______________       ║
║  UBICAZIONE EVENTO: ______________________________________    ║
║                                                                ║
║  TIPO EVENTO:                                                  ║
║  ☐ Incendio/Allagamento    ☐ Guasto infrastruttura           ║
║  ☐ Failure IT              ☐ Cyber incident                  ║
║  ☐ Indisponibilità sede    ☐ Indisponibilità personale       ║
║  ☐ Failure fornitore       ☐ Altro: _______________          ║
║                                                                ║
║  DESCRIZIONE EVENTO:                                          ║
║  ___________________________________________________________  ║
║  ___________________________________________________________  ║
║                                                                ║
║  IMPATTO IMMEDIATO RILEVATO:                                  ║
║  ☐ Personale a rischio (N. persone: ___)                     ║
║  ☐ Sede inaccessibile                                        ║
║  ☐ Sistemi IT non disponibili: _________________________     ║
║  ☐ Processo interrotto: _______________________________      ║
║  ☐ Dati potenzialmente persi/compromessi                     ║
║                                                                ║
║  AZIONI GIÀ INTRAPRESE:                                       ║
║  ___________________________________________________________  ║
║                                                                ║
║  RISORSE/SUPPORTO NECESSARIO:                                 ║
║  ___________________________________________________________  ║
║                                                                ║
║  INVIATO A: ☐ BC Manager  ☐ IT Manager  ☐ HR  ☐ Altro       ║
╚════════════════════════════════════════════════════════════════╝
```

---

### Fase 1: Risposta Immediata (30 min - 4 ore)

**Obiettivi**: Garantire sicurezza, contenere evento, valutare impatto, attivare team

#### Checklist Fase 1

| # | Azione | Responsabile | Entro | ✓ |
|---|--------|--------------|-------|---|
| 1.1 | Confermare sicurezza tutto il personale | HR / ERT | T+30min | ☐ |
| 1.2 | Attivare call tree se necessario | BC Manager | T+30min | ☐ |
| 1.3 | Convocare CMT (fisico o virtuale) | CMT Leader | T+1h | ☐ |
| 1.4 | Briefing situazione al CMT | BC Manager | T+1h | ☐ |
| 1.5 | Valutare impatto su processi critici | Process Owner | T+2h | ☐ |
| 1.6 | **DECISIONE**: dichiarazione crisi SI/NO | CMT Leader | T+2h | ☐ |
| 1.7 | Se crisi: attivare procedure Fase 2 | CMT | T+2h | ☐ |
| 1.8 | Prima comunicazione interna | HR/Comunicazione | T+2h | ☐ |
| 1.9 | Attivare workaround immediati | Process Owner | T+4h | ☐ |
| 1.10 | Notifica autorità se richiesto (GDPR, NIS2) | Legal/DPO | T+4h | ☐ |

#### Modulo Decisione CMT

```
╔════════════════════════════════════════════════════════════════╗
║                  CMT MEETING - DECISIONE CRISI                 ║
╠════════════════════════════════════════════════════════════════╣
║                                                                ║
║  DATA/ORA: ____/____/______  ____:____                        ║
║  LUOGO: ☐ Sala crisi  ☐ Virtuale (link: _____________)       ║
║                                                                ║
║  PARTECIPANTI:                                                 ║
║  ☐ CMT Leader: ____________  ☐ BC Manager: ____________       ║
║  ☐ IT Manager: ____________  ☐ HR Manager: ____________       ║
║  ☐ Finance: _______________  ☐ Legal: _________________       ║
║  ☐ Comunicazione: _________  ☐ Operations: ____________       ║
║                                                                ║
║  SITUAZIONE ATTUALE:                                          ║
║  ___________________________________________________________  ║
║  ___________________________________________________________  ║
║                                                                ║
║  IMPATTO VALUTATO: ☐ Basso  ☐ Medio  ☐ Alto  ☐ Critico      ║
║                                                                ║
║  PROCESSI IMPATTATI:                                          ║
║  ☐ [Processo 1]  ☐ [Processo 2]  ☐ [Processo 3]              ║
║  ☐ [Processo 4]  ☐ [Processo 5]  ☐ Tutti                     ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║                        DECISIONE                               ║
║  ═══════════════════════════════════════════════════════════  ║
║                                                                ║
║  ☐ Gestione locale - NO attivazione BCP                      ║
║  ☐ Attivazione PARZIALE BCP (specificare: _____________)     ║
║  ☐ Attivazione COMPLETA BCP                                  ║
║  ☐ Attivazione DR (sito alternativo IT)                      ║
║  ☐ Attivazione Crisis Management Plan                        ║
║                                                                ║
║  MOTIVAZIONE DECISIONE:                                       ║
║  ___________________________________________________________  ║
║                                                                ║
║  PROSSIMO BRIEFING: ____/____/______ ore ____:____           ║
║                                                                ║
║  FIRMA CMT Leader: ___________________ Data: _____________    ║
╚════════════════════════════════════════════════════════════════╝
```

---

### Fase 2: Gestione Crisi (4-72 ore)

**Obiettivi**: Stabilizzare, implementare soluzioni temporanee, mantenere MBCO, comunicare

#### Checklist Fase 2

| # | Azione | Responsabile | Entro | ✓ |
|---|--------|--------------|-------|---|
| 2.1 | Attivare sito alternativo (se necessario) | BC Manager | T+6h | ☐ |
| 2.2 | Implementare workaround per processi critici | Process Owner | T+8h | ☐ |
| 2.3 | Attivare DR IT (se necessario) | IT Manager | T+4h | ☐ |
| 2.4 | Briefing CMT ogni 4 ore | CMT Leader | Continuo | ☐ |
| 2.5 | Aggiornamento dipendenti | HR | Ogni 8h | ☐ |
| 2.6 | Comunicazione clienti chiave | Account Manager | T+24h | ☐ |
| 2.7 | Gestione media (se necessario) | CEO/Comunicazione | Continuo | ☐ |
| 2.8 | Supporto welfare personale | HR | Continuo | ☐ |
| 2.9 | Documentazione continua eventi (log) | BC Manager | Continuo | ☐ |
| 2.10 | Valutazione risorse/budget aggiuntivi | Finance | T+24h | ☐ |
| 2.11 | Pianificazione recovery | Recovery Team | T+48h | ☐ |
| 2.12 | Notifica assicurazione | Finance/Legal | T+24h | ☐ |

#### Frequenza Briefing CMT

| Fase | Frequenza Briefing | Durata |
|------|-------------------|--------|
| Prime 24 ore | Ogni 4 ore | 30 min |
| Giorno 2-3 | Ogni 8 ore | 30 min |
| Giorno 4+ | Giornaliero | 45 min |
| Fase recovery | Giornaliero | 30 min |

#### Template Situation Report (SITREP)

```
╔════════════════════════════════════════════════════════════════╗
║             SITUATION REPORT (SITREP) #____                    ║
╠════════════════════════════════════════════════════════════════╣
║                                                                ║
║  DATA/ORA: ____/____/______  ____:____                        ║
║  REDATTO DA: ____________________                              ║
║  PERIODO COPERTURA: Da ____:____ a ____:____                  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  1. SITUAZIONE ATTUALE                                        ║
║  ═══════════════════════════════════════════════════════════  ║
║  ___________________________________________________________  ║
║  ___________________________________________________________  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  2. AZIONI COMPLETATE DALL'ULTIMO SITREP                      ║
║  ═══════════════════════════════════════════════════════════  ║
║  • _________________________________________________________  ║
║  • _________________________________________________________  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  3. AZIONI IN CORSO                                           ║
║  ═══════════════════════════════════════════════════════════  ║
║  • _________________________________________________________  ║
║  • _________________________________________________________  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  4. PROBLEMI/OSTACOLI                                         ║
║  ═══════════════════════════════════════════════════════════  ║
║  • _________________________________________________________  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  5. DECISIONI RICHIESTE                                       ║
║  ═══════════════════════════════════════════════════════════  ║
║  • _________________________________________________________  ║
║                                                                ║
║  ═══════════════════════════════════════════════════════════  ║
║  6. PROSSIMI PASSI                                            ║
║  ═══════════════════════════════════════════════════════════  ║
║  • _________________________________________________________  ║
║                                                                ║
║  PROSSIMO SITREP: ____/____/______ ore ____:____             ║
╚════════════════════════════════════════════════════════════════╝
```

---

### Fase 3: Recovery (72 ore - 2 settimane)

**Obiettivi**: Ripristinare operatività normale, recuperare arretrato, verificare integrità

#### Checklist Fase 3

| # | Azione | Responsabile | ✓ |
|---|--------|--------------|---|
| 3.1 | Confermare risoluzione causa root | Team tecnico | ☐ |
| 3.2 | Verificare sicurezza sede/sistemi | IT/Facility | ☐ |
| 3.3 | Ripristino sistemi IT (priorità da BIA) | IT Recovery | ☐ |
| 3.4 | Test funzionamento sistemi | IT + Business | ☐ |
| 3.5 | Rientro personale (se evacuato) | HR/Facility | ☐ |
| 3.6 | Ripristino processi per priorità | Process Owner | ☐ |
| 3.7 | Recupero lavoro arretrato (WRT) | Business Team | ☐ |
| 3.8 | Comunicazione ripresa ai clienti | Comunicazione | ☐ |
| 3.9 | Verifica completezza/integrità dati | Process Owner + IT | ☐ |
| 3.10 | Disattivazione sito alternativo | BC Manager | ☐ |
| 3.11 | Verifica capacità normale | Operations | ☐ |

#### Priorità di Ripristino (da BIA)

| Priorità | Processo | RTO | Verifiche Pre-Ripristino |
|----------|----------|-----|--------------------------|
| 1 | [Processo critico 1] | [X]h | [Checklist specifica] |
| 2 | [Processo critico 2] | [X]h | [Checklist specifica] |
| 3 | [Processo critico 3] | [X]h | [Checklist specifica] |
| 4 | [Processo critico 4] | [X]h | [Checklist specifica] |
| 5 | [Altri processi] | [X]h | [Checklist specifica] |

---

### Fase 4: Ritorno alla Normalità

**Obiettivi**: Confermare operatività completa, chiudere crisi, lessons learned

#### Checklist Fase 4

| # | Azione | Responsabile | ✓ |
|---|--------|--------------|---|
| 4.1 | Verifica tutti i processi operativi al 100% | Process Owner | ☐ |
| 4.2 | Sign-off business owner per ogni processo | Business Owner | ☐ |
| 4.3 | Conferma formale chiusura crisi | CMT Leader | ☐ |
| 4.4 | Comunicazione fine crisi (interna) | HR/Comunicazione | ☐ |
| 4.5 | Comunicazione fine crisi (esterna) | Comunicazione | ☐ |
| 4.6 | Raccolta lessons learned | BC Manager | ☐ |
| 4.7 | Post-Incident Review meeting | CMT | ☐ |
| 4.8 | Report finale incidente | BC Manager | ☐ |
| 4.9 | Aggiornamento BCP se necessario | BC Manager | ☐ |
| 4.10 | Gestione pratiche assicurazione | Finance | ☐ |
| 4.11 | Riconoscimento team | HR/CEO | ☐ |
| 4.12 | Archiviazione documentazione | BC Manager | ☐ |

---

## 6. Procedure per Scenario

### 6.1 Scenario: Indisponibilità Sede

**Trigger**: Edificio inaccessibile (incendio, allagamento, ordine autorità, evento sismico)

#### Azioni Immediate

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Evacuazione secondo piano emergenza | ERT Leader | Immediato |
| 2 | Verifica sicurezza personale (appello) | HR | T+30min |
| 3 | Comunicazione a tutti i dipendenti | HR | T+1h |
| 4 | Valutazione danni/accessibilità | Facility | T+2h |
| 5 | Attivazione smart working | IT/HR | T+4h |
| 6 | Attivazione sito alternativo (se necessario) | BC Manager | T+8h |

#### Opzioni Sito Alternativo

| Opzione | Ubicazione | Capacità | Tempo Attivazione | Costo/Giorno |
|---------|------------|----------|-------------------|--------------|
| **Smart Working** | Casa dipendenti | 100% | 2-4 ore | Minimo |
| **Sito alternativo 1** | [Indirizzo] | [N] postazioni | [X] ore | €[Y] |
| **Sito alternativo 2** | [Indirizzo] | [N] postazioni | [X] ore | €[Y] |
| **Coworking** | [Provider/Indirizzo] | [N] postazioni | [X] ore | €[Y] |

#### Risorse Smart Working

- [ ] VPN capacity per [N] utenti simultanei
- [ ] Laptop/dispositivi disponibili: [N]
- [ ] Licenze software remote: [N]
- [ ] Linee telefoniche alternative: [Dettagli]
- [ ] Accesso sistemi cloud: [Provider]

---

### 6.2 Scenario: Failure Sistemi IT Critici

**Trigger**: Sistema critico non disponibile, cyber attack, ransomware

#### Azioni Immediate

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Valutazione impatto e causa | IT Manager | T+30min |
| 2 | Contenimento (isolamento se cyber) | IT Security | T+1h |
| 3 | Decisione: fix locale vs DR | IT Manager + CMT | T+2h |
| 4 | Se DR: attivare IT-DRP | IT Recovery Team | T+4h |
| 5 | Attivare workaround business | Process Owner | T+4h |
| 6 | Comunicazione a utenti | IT/Comunicazione | T+2h |

#### Workaround per Sistema

| Sistema | Workaround Manuale | Capacità | Durata Max |
|---------|-------------------|----------|------------|
| ERP | Ordini via email + Excel | 30% | 24h |
| Email | WhatsApp aziendale, telefono | 50% | 8h |
| CRM | Schede cliente offline | 40% | 24h |
| [Sistema X] | [Workaround] | [%] | [Durata] |

> **Riferimento**: IT Disaster Recovery Plan {{company_name}}-DRP-001

---

### 6.3 Scenario: Indisponibilità Personale Critico

**Trigger**: Pandemia, sciopero, indisponibilità multipla personale chiave

#### Azioni

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Assessment personale disponibile | HR | T+4h |
| 2 | Attivazione backup per ruoli critici | Manager linea | T+8h |
| 3 | Cross-training accelerato se necessario | HR | T+24h |
| 4 | Attivazione risorse esterne/temporanee | HR/Procurement | T+48h |
| 5 | Pianificazione riduzione capacità | CMT | T+24h |

#### Backup Ruoli Critici

| Ruolo Critico | Titolare | Backup 1 | Backup 2 | Cross-Training |
|---------------|----------|----------|----------|----------------|
| [Ruolo 1] | [Nome] | [Nome] | [Nome] | ☐ Completato |
| [Ruolo 2] | [Nome] | [Nome] | [Nome] | ☐ Completato |
| [Ruolo 3] | [Nome] | [Nome] | [Nome] | ☐ Completato |
| [Ruolo 4] | [Nome] | [Nome] | [Nome] | ☐ Completato |

---

### 6.4 Scenario: Failure Fornitore Critico

**Trigger**: Fornitore non disponibile, fallimento, interruzione supply chain

#### Azioni

| # | Azione | Responsabile | Entro |
|---|--------|--------------|-------|
| 1 | Contattare fornitore per assessment | Procurement | T+2h |
| 2 | Valutare impatto su processi | Process Owner | T+4h |
| 3 | Verificare scorte disponibili | Operations | Immediato |
| 4 | Attivare fornitore alternativo | Procurement | T+24h |
| 5 | Comunicazione a clienti se impattati | Account Manager | T+24h |

#### Fornitori Alternativi Pre-Qualificati

| Fornitore Primario | Servizio | Alternativo | Contratto Attivo | Lead Time |
|--------------------|----------|-------------|------------------|-----------|
| [Nome] | [Servizio] | [Nome alt.] | ☐ Sì / ☐ No | [X] giorni |
| [Nome] | [Servizio] | [Nome alt.] | ☐ Sì / ☐ No | [X] giorni |

---

## 7. Piano di Comunicazione

### 7.1 Principi di Comunicazione di Crisi

- **Tempestività**: Prima comunicazione entro 2 ore dall'evento
- **Accuratezza**: Solo informazioni verificate
- **Coerenza**: Messaggi allineati tra tutti i canali
- **Empatia**: Tono appropriato alla situazione
- **Single Voice**: Portavoce unico designato per comunicazioni esterne

### 7.2 Stakeholder e Responsabilità

| Stakeholder | Priorità | Canale | Responsabile | Entro |
|-------------|----------|--------|--------------|-------|
| CMT | 1 | Call/SMS | BC Manager | 30 min |
| Dipendenti | 1 | Email, SMS, Intranet | HR | 2h |
| Clienti chiave | 2 | Telefono, Email | Account Manager | 4h |
| Fornitori critici | 2 | Telefono | Procurement | 4h |
| Autorità (GDPR, NIS2) | 2 | Canali ufficiali | Legal/DPO | Da norma |
| Banche/Assicurazioni | 2 | Email/Telefono | CFO | 24h |
| Media | 3 | Comunicato stampa | CEO/Comunicazione | 24h |
| Social media | 3 | Post pianificati | Comunicazione | 24h |

### 7.3 Template Comunicazioni

#### Comunicazione Dipendenti - Iniziale

```
OGGETTO: [URGENTE] Comunicazione aziendale - [Tipo evento]

Cari colleghi,

Vi informiamo che [breve descrizione evento senza dettagli sensibili]
sta impattando [sede/sistema/servizio].

SITUAZIONE ATTUALE
[Descrizione situazione - cosa sappiamo]

COSA FARE ORA
1. [Istruzione specifica 1]
2. [Istruzione specifica 2]
3. [Istruzione specifica 3]

PROSSIMI AGGIORNAMENTI
Riceverete un aggiornamento entro [tempo].

Per urgenze operative contattare:
- [Nome/Ruolo]: [Telefono]
- [Nome/Ruolo]: [Telefono]

Grazie per la collaborazione.

[Nome]
[Ruolo]
[Data/Ora]
```

#### Comunicazione Clienti

```
Gentile [Cliente / Sig./Sig.ra Nome],

La informiamo che stiamo gestendo una situazione che potrebbe
causare [impatto specifico sul servizio].

COSA ASPETTARSI
[Descrizione impatto pratico]

TEMPO STIMATO RIPRISTINO
[Stima realistica]

COSA FACCIAMO
I nostri team stanno lavorando per ripristinare la piena
operatività nel più breve tempo possibile.

ALTERNATIVE DISPONIBILI
[Canali/servizi alternativi se disponibili]

Per aggiornamenti: [contatto/pagina status]

Ci scusiamo per il disagio.

Cordiali saluti,
[Nome]
[Nome Organizzazione]
Tel: [Numero]
```

### 7.4 Bridge di Emergenza

| Tipo | Numero/Link | PIN | Note |
|------|-------------|-----|------|
| Conference call | [Numero] | [PIN] | Disponibile H24 |
| Video call | [Link Teams/Zoom] | - | Sala "Crisis Room" |
| Chat emergenza | [Link canale] | - | Gruppo "Emergency" |

---

## 8. Contact List di Emergenza

### 8.1 Contatti Interni Critici

| Ruolo | Nome | Cellulare | Alternativo | Email |
|-------|------|-----------|-------------|-------|
| CEO | [Nome] | [Num] | [Num] | [Email] |
| BC Manager | [Nome] | [Num] | [Num] | [Email] |
| IT Manager | [Nome] | [Num] | [Num] | [Email] |
| HR Manager | [Nome] | [Num] | [Num] | [Email] |
| CFO | [Nome] | [Num] | [Num] | [Email] |
| DPO | [Nome] | [Num] | [Num] | [Email] |
| Facility Manager | [Nome] | [Num] | [Num] | [Email] |
| Security Manager | [Nome] | [Num] | [Num] | [Email] |

### 8.2 Contatti Esterni

| Servizio | Numero | Note |
|----------|--------|------|
| Emergenze generali | 112 | |
| Vigili del Fuoco | 115 | |
| Ambulanza | 118 | |
| Polizia | 113 | |
| Fornitore IT [Nome] | [Num] | Support H24, contratto [N.] |
| Cloud Provider | [Num] | Support H24 |
| ISP | [Num] | Support H24 |
| Assicurazione | [Num] | Polizza [N.], broker: [Nome] |
| Studio legale | [Num] | [Nome referente] |
| Agenzia PR | [Num] | Per crisis communication |

> **NOTA**: Lista completa in Allegato A - Verificare aggiornamento trimestrale

---

## 9. Risorse di Recovery

### 9.1 Sito Alternativo

| Elemento | Dettaglio |
|----------|-----------|
| Indirizzo | [Indirizzo completo] |
| Contatto sito | [Nome, telefono] |
| Codice accesso / Badge | [Procedura accesso] |
| Postazioni disponibili | [N] |
| Infrastruttura IT | [Descrizione] |
| Tempo attivazione | [X ore] |
| Contratto/Provider | [Riferimento] |

### 9.2 Risorse IT per DR

| Elemento | Ubicazione | Accesso |
|----------|------------|---------|
| DR Site IT | [Cloud/Location] | [Credenziali in password manager] |
| Backup dati | [Location] | [Procedura restore] |
| Documentazione DR | [Path] | [Accesso] |
| Immagini VM | [Location] | [Procedura deploy] |

### 9.3 Scorte di Emergenza

| Elemento | Quantità | Ubicazione | Responsabile Verifica |
|----------|----------|------------|----------------------|
| Laptop di riserva | [N] | [Ubicazione] | IT |
| Smartphone di riserva | [N] | [Ubicazione] | IT |
| Power bank | [N] | [Ubicazione] | IT |
| Router 4G/5G | [N] | [Ubicazione] | IT |
| Cassetta pronto soccorso | [N] | [Ubicazione] | HR/HSE |
| Torce elettriche | [N] | [Ubicazione] | Facility |

---

## 10. Manutenzione del Piano

### 10.1 Frequenza Aggiornamenti

| Elemento | Frequenza | Responsabile |
|----------|-----------|--------------|
| Contact list | Trimestrale | HR/BC Manager |
| Test call tree | Trimestrale | BC Manager |
| Review piano completo | Semestrale | BC Manager |
| Esercitazione tabletop | Semestrale | BC Manager |
| Test DR IT | Semestrale | IT Manager |
| Review post-incidente | Dopo ogni evento | BC Manager |

### 10.2 Trigger Revisione Straordinaria

Il piano deve essere rivisto immediatamente quando:
- Cambiamento organizzativo significativo (fusioni, acquisizioni, riorganizzazioni)
- Nuovo processo critico aggiunto
- Incidente/esercitazione con lessons learned significative
- Cambio sede o infrastruttura IT importante
- Cambio normativo rilevante (es. nuovi requisiti NIS2/DORA)
- Cambio fornitore critico

---

## 11. Conformità Normativa

### 11.1 Requisiti e Riferimenti

| Normativa | Requisito | Sezione BCP |
|-----------|-----------|-------------|
| **ISO 22301** | Piani di continuità documentati | Tutto il documento |
| **ISO 22301 8.4.4** | Procedure di risposta | Sezioni 5, 6 |
| **NIS2 Art. 21(2)(c)** | Continuità operativa e gestione crisi | Sezioni 3, 5, 6, 7 |
| **DORA Art. 11** | Risposta e ripristino | Sezioni 5, 6 |
| **GDPR Art. 32** | Capacità di ripristino | Sezione 5.3, 6.2 |

### 11.2 Notifiche Obbligatorie

| Evento | Autorità | Termine | Responsabile |
|--------|----------|---------|--------------|
| Data breach | Garante Privacy | 72 ore | DPO |
| Incidente significativo NIS2 | ACN/CSIRT | 24-72 ore | CISO |
| Incidente ICT grave (DORA) | Autorità vigilanza | 24-72 ore | Compliance |

---

## 12. Allegati

- **Allegato A**: Contact List Completa
- **Allegato B**: Checklist Attivazione per Scenario
- **Allegato C**: Template Report Incidente
- **Allegato D**: Mappe Sedi ed Evacuazione
- **Allegato E**: Inventario Risorse Emergenza
- **Allegato F**: Procedure Specifiche di Processo
- **Allegato G**: Moduli e Template Compilabili

---

## 13. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |
| 2.0 | {{document_date}} | {{document_author}} | Nuovo formato, allineamento NIS2/DORA |

---

## 14. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{bc_manager}} | | {{document_date}} |
| Verificato da | {{quality_manager}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Business Continuity Policy | {{company_name}}-POL-BCMS-001 | Policy di riferimento |
| Business Impact Analysis | {{company_name}}-BIA-BCMS-001 | RTO/RPO/MBCO dei processi |
| Crisis Management Plan | {{company_name}}-CMP-BCMS-001 | Escalation e gestione crisi |
| IT Disaster Recovery Plan | {{company_name}}-DRP-BCMS-001 | Recovery tecnico IT |
| Recovery Procedure | {{company_name}}-REC-BCMS-001 | Procedure operative di recovery |
| BC Risk Assessment | {{company_name}}-BRA-BCMS-001 | Rischi che attivano il BCP |
| Exercise Programme | {{company_name}}-EXR-BCMS-001 | Test del BCP |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{bc_manager}}` | Redatto da | ☐ |
| 6 | Processi critici con RTO/RPO | Sezione 4 — allineati alla BIA | ☐ |
| 7 | Team recovery nominati | Sezione 5 — tutti i ruoli assegnati | ☐ |
| 8 | Contatti emergenza | Allegato — lista completa e aggiornata | ☐ |
| 9 | Sedi alternative | Sezione 6 — accordi formalizzati | ☐ |
| 10 | Workaround documentati | Sezione 7 — per ogni processo critico | ☐ |
| 11 | Test BCP eseguito | Almeno un tabletop o walkthrough completato | ☐ |

---

*Template conforme a ISO 22301:2019 Clausole 8.4.1-8.4.5*
*Creato con Kynosure.ai*
