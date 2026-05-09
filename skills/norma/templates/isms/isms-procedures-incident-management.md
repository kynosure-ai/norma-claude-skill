---
title: Procedura di Gestione degli Incidenti di Sicurezza
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{security_officer_title}}'
approver: '{{senior_management}}'
framework: ISO27001
language: IT
documentType: procedure
iso_controls:
  - A.5.24 - Pianificazione e preparazione della gestione incidenti
  - A.5.25 - Valutazione e decisione sugli eventi di sicurezza
  - A.5.26 - Risposta agli incidenti di sicurezza
  - A.5.27 - Apprendimento dagli incidenti
  - A.5.28 - Raccolta delle prove
  - A.6.8 - Segnalazione degli eventi di sicurezza
cross_references:
  - NIS2 Art. 23 - Obblighi di segnalazione
  - DORA Art. 17-19 - Gestione incidenti ICT
  - GDPR Art. 33 - Notifica data breach (72h)
  - GDPR Art. 34 - Comunicazione agli interessati
status: Da approvare
subset: true
---

# Procedura di Gestione degli Incidenti di Sicurezza

## 1. Scopo e Obiettivi

### 1.1 Scopo

{{company_name}} riconosce che gli incidenti di sicurezza delle informazioni rappresentano una minaccia costante per la continuità operativa, la riservatezza dei dati e la reputazione aziendale. La capacità di rilevare tempestivamente gli incidenti, rispondere in modo efficace e apprendere da ogni evento costituisce un elemento fondamentale della resilienza organizzativa. La presente Procedura stabilisce un processo strutturato per la gestione degli incidenti di sicurezza, garantendo risposte coordinate, tempestive e conformi ai requisiti normativi.

La Procedura definisce le modalità operative per il rilevamento e l'identificazione degli eventi e degli incidenti di sicurezza, la classificazione e la prioritizzazione della risposta in base all'impatto e all'urgenza, le attività di contenimento, eradicazione e ripristino dei sistemi, la comunicazione agli stakeholder interni ed esterni incluse le autorità competenti, nonché il processo di apprendimento e miglioramento continuo. L'Organizzazione persegue obiettivi specifici e misurabili in termini di tempi di rilevamento, contenimento e notifica, in conformità ai requisiti della Direttiva NIS2, del Regolamento DORA e del GDPR.

### 1.2 Obiettivi

L'Organizzazione definisce indicatori di prestazione chiave per misurare l'efficacia della risposta agli incidenti. Il tempo medio di rilevamento (MTTD) per incidenti di priorità P1 e P2 non deve superare un'ora, mentre il tempo medio di contenimento (MTTC) per incidenti P1 non deve eccedere le quattro ore. Le notifiche alle autorità competenti devono rispettare le tempistiche normative definite dalla NIS2 e dal GDPR. Ogni incidente di priorità P1 e P2 deve essere oggetto di una post-incident review entro cinque giorni lavorativi, e almeno l'80% delle lesson learned identificate deve essere implementato entro trenta giorni.

---

## 2. Definizioni

### 2.1 Evento vs Incidente

```
┌─────────────────────────────────────────────────────────────┐
│  EVENTO DI SICUREZZA                                       │
│  Occorrenza osservata che potrebbe avere rilevanza         │
│  per la sicurezza delle informazioni                        │
│                         │                                   │
│                         ▼                                   │
│                    TRIAGE                                   │
│                    /     \                                  │
│                   /       \                                 │
│                  ▼         ▼                                │
│          Falso Positivo   INCIDENTE                        │
│          (chiusura)       Compromissione effettiva         │
│                           o potenziale della CIA           │
└─────────────────────────────────────────────────────────────┘
```

### 2.2 Tipologie di Incidente
| Categoria | Codice | Esempi |
|-----------|--------|--------|
| Malware | MAL | Ransomware, virus, trojan |
| Accesso non autorizzato | ACC | Intrusione, privilege escalation |
| Data breach | DBR | Esfiltrazione, esposizione dati |
| DDoS/Availability | DOS | Attacco volumetrico, service disruption |
| Phishing/Social Engineering | PHI | Spear phishing, BEC |
| Insider threat | INS | Sabotaggio, data theft interno |
| Vulnerability exploitation | VUL | Zero-day, exploit noti |
| Physical security | PHY | Furto dispositivi, accesso non autorizzato |
| Third-party | TPR | Breach fornitore, supply chain |

---

## 3. Classificazione e Priorità

### 3.1 Matrice di Severità

| Impatto ↓ / Urgenza → | Bassa | Media | Alta | Critica |
|------------------------|-------|-------|------|---------|
| **Critico** | P2 | P1 | P1 | P1 |
| **Alto** | P3 | P2 | P1 | P1 |
| **Medio** | P4 | P3 | P2 | P2 |
| **Basso** | P4 | P4 | P3 | P3 |

### 3.2 Criteri di Impatto
| Livello | Descrizione | Esempi |
|---------|-------------|--------|
| **Critico** | Business interruption totale, data breach massivo, impatto reputazionale grave | Ransomware su sistemi core, breach dati PII >10k, compromissione infrastruttura critica |
| **Alto** | Servizi critici degradati, data breach significativo, potenziale danno reputazionale | Sistemi critici offline >4h, breach dati PII <10k, accesso admin compromesso |
| **Medio** | Servizi non-critici impattati, dati interni esposti | Applicazioni secondarie down, malware contenuto, phishing riuscito |
| **Basso** | Impatto minimo, nessun dato sensibile coinvolto | Tentativo bloccato, spam, false positive |

### 3.3 Criteri di Urgenza
| Livello | Descrizione |
|---------|-------------|
| **Critica** | Attacco in corso, esfiltrazione attiva |
| **Alta** | Compromissione confermata, propagazione possibile |
| **Media** | Attività sospetta, richiede investigazione |
| **Bassa** | Evento storico, già contenuto |

### 3.4 SLA per Priorità

| Priorità | Risposta Iniziale | Contenimento | Risoluzione | Escalation |
|----------|-------------------|--------------|-------------|------------|
| **P1** | 15 minuti | 4 ore | 24 ore | Immediata a CISO |
| **P2** | 1 ora | 8 ore | 48 ore | 2 ore a CISO |
| **P3** | 4 ore | 24 ore | 5 giorni | Fine giornata |
| **P4** | 8 ore | 48 ore | 10 giorni | Weekly report |

---

## 4. Processo di Gestione Incidenti

### 4.1 Flusso Principale

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│  1. DETECT   │───►│  2. TRIAGE   │───►│  3. CONTAIN  │
│  Rilevamento │    │  Classifica  │    │  Isolamento  │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│  6. CLOSE    │◄───│  5. RECOVER  │◄───│ 4. ERADICATE │
│  Chiusura    │    │  Ripristino  │    │  Rimozione   │
└──────────────┘    └──────────────┘    └──────────────┘
        │
        ▼
┌──────────────┐
│ 7. LESSONS   │
│  LEARNED     │
└──────────────┘
```

### 4.2 Fase 1: Rilevamento (Detection)

**Fonti di Rilevamento:**
| Fonte | Tipo | Responsabile |
|-------|------|--------------|
| SIEM/SOC | Automatico | Security Team |
| EDR/XDR | Automatico | Security Team |
| IDS/IPS | Automatico | Network Team |
| Segnalazione utente | Manuale | Tutti |
| Threat intelligence | Proattivo | Security Team |
| Audit/Assessment | Periodico | Audit Team |
| Terze parti | Esterno | CERT/Autorità |

**Canali di Segnalazione:**
| Canale | Utilizzo | SLA Risposta |
|--------|----------|--------------|
| Email security@[azienda].it | Non urgente | 4 ore |
| Telefono SOC | Urgente | 15 minuti |
| Ticketing system | Standard | 1 ora |
| Chat sicuro | Real-time | 5 minuti |

### 4.3 Fase 2: Triage e Classificazione

**Checklist Triage Iniziale:**
- [ ] Identificare tipo di evento
- [ ] Verificare se è falso positivo
- [ ] Determinare scope (sistemi, utenti, dati)
- [ ] Classificare impatto e urgenza
- [ ] Assegnare priorità
- [ ] Aprire ticket incidente
- [ ] Notificare team appropriato

**Informazioni da Raccogliere:**
| Campo | Descrizione | Obbligatorio |
|-------|-------------|--------------|
| Timestamp | Data/ora rilevamento | Sì |
| Reporter | Chi ha segnalato | Sì |
| Sistemi coinvolti | Asset impattati | Sì |
| Descrizione | Cosa è successo | Sì |
| IOC iniziali | IP, hash, URL, etc. | Se disponibili |
| Azioni già intraprese | Cosa è stato fatto | Se applicabile |

### 4.4 Fase 3: Contenimento

**Strategie di Contenimento:**
| Tipo | Azione | Quando Usare |
|------|--------|--------------|
| **Short-term** | Isolamento rete, disable account | Immediatamente |
| **Long-term** | Patch, config change | Dopo analisi |

**Playbook Contenimento per Tipo:**

**Malware/Ransomware:**
1. Isolare sistema dalla rete (non spegnere)
2. Bloccare C2 su firewall
3. Disable account compromesso
4. Preservare memoria/disco per forensics
5. Identificare altri sistemi infetti

**Data Breach:**
1. Identificare flusso dati
2. Revocare accessi coinvolti
3. Bloccare endpoint esfiltrazione
4. Preservare log
5. Attivare procedura GDPR se PII

**Account Compromesso:**
1. Disable/reset password account
2. Revocare token/sessioni
3. Verificare attività recente
4. Controllare altri account dell'utente
5. Analizzare vettore compromissione

### 4.5 Fase 4: Eradicazione

**Attività di Eradicazione:**
- [ ] Rimuovere malware/tool attaccante
- [ ] Applicare patch/fix
- [ ] Rimuovere account/accessi non autorizzati
- [ ] Bonificare sistemi compromessi
- [ ] Eliminare persistenza
- [ ] Verificare completezza rimozione

**Validazione Eradicazione:**
| Check | Metodo | Responsabile |
|-------|--------|--------------|
| Scan malware | EDR/AV full scan | Security |
| Verifica IOC | Threat hunting | Security |
| Log review | SIEM analysis | SOC |
| Vulnerability scan | Scanner | Security |

### 4.6 Fase 5: Recovery

**Piano di Recovery:**
| Attività | Responsabile | Priorità |
|----------|--------------|----------|
| Restore da backup verificato | IT Ops | 1 |
| Rebuild sistema se necessario | IT Ops | 2 |
| Re-enable servizi gradualmente | IT Ops | 3 |
| Reset credenziali utenti | IT Security | 4 |
| Verifica funzionalità | Business Owner | 5 |
| Monitoraggio intensivo | SOC | Continuo |

**Criteri Return-to-Normal:**
- [ ] Tutti i sistemi operativi
- [ ] Nessun IOC rilevato in 24h
- [ ] Vulnerabilità sfruttata corretta
- [ ] Utenti ri-abilitati con nuove credenziali
- [ ] Business Owner conferma operatività
- [ ] CISO autorizza chiusura contenimento

### 4.7 Fase 6: Chiusura

**Documentazione Finale:**
| Documento | Contenuto | Retention |
|-----------|-----------|-----------|
| Incident Report | Timeline, azioni, impact | 5 anni |
| Forensic Report | Analisi tecnica dettagliata | 5 anni |
| Evidence | Log, immagini, artefatti | 5 anni |
| Communication Log | Tutte le comunicazioni | 5 anni |

### 4.8 Fase 7: Lessons Learned

**Post-Incident Review (PIR):**
| Domanda | Obiettivo |
|---------|-----------|
| Cosa è successo esattamente? | Root cause |
| Come è stato rilevato? | Detection capability |
| Quanto tempo ha richiesto ogni fase? | SLA analysis |
| Cosa ha funzionato bene? | Best practice |
| Cosa poteva essere fatto meglio? | Improvement |
| Quali controlli hanno fallito? | Gap analysis |
| Quali azioni correttive servono? | Remediation plan |

**Template PIR Meeting:**
- Partecipanti: IRT, CISO, Business Owner, IT
- Timing: Entro 5 giorni lavorativi da chiusura
- Output: PIR Report + Action Items

---

## 5. Obblighi di Notifica

### 5.1 Timeline Notifiche Regolatorie

```
       T+0              T+24h             T+72h            T+30gg
        │                 │                 │                 │
        ▼                 ▼                 ▼                 ▼
   ┌─────────┐      ┌─────────┐      ┌─────────┐      ┌─────────┐
   │Incidente│      │NIS2     │      │GDPR     │      │Report   │
   │Rilevato │      │Early    │      │Notifica │      │Finale   │
   │         │      │Warning  │      │Garante  │      │NIS2     │
   └─────────┘      └─────────┘      └─────────┘      └─────────┘
```

### 5.2 NIS2 - Obblighi di Segnalazione (Art. 23)

| Fase | Timing | Contenuto | Destinatario |
|------|--------|-----------|--------------|
| Early Warning | 24h | Sospetto incidente significativo | CSIRT/ACN |
| Notifica Incidente | 72h | Valutazione iniziale, gravità, impatto | CSIRT/ACN |
| Report Intermedio | Su richiesta | Aggiornamenti significativi | CSIRT/ACN |
| Report Finale | 1 mese | Analisi completa, root cause, misure | CSIRT/ACN |

**Criteri Incidente Significativo NIS2:**
- Grave perturbazione operativa dei servizi
- Perdite finanziarie significative per l'entità
- Danni considerevoli a persone fisiche o giuridiche

### 5.3 GDPR - Data Breach Notification

**Art. 33 - Notifica Garante:**
| Requisito | Dettaglio |
|-----------|-----------|
| Timing | Senza ingiustificato ritardo, max 72h |
| Condizione | Rischio per diritti e libertà interessati |
| Contenuto | Natura breach, categorie dati, n. interessati, conseguenze, misure |
| Canale | Portale Garante Privacy |

**Art. 34 - Comunicazione Interessati:**
| Requisito | Dettaglio |
|-----------|-----------|
| Timing | Senza ingiustificato ritardo |
| Condizione | Rischio elevato per diritti e libertà |
| Esenzioni | Dati cifrati, misure che eliminano rischio, sforzo sproporzionato |
| Contenuto | Linguaggio chiaro, natura breach, conseguenze, misure, contatti DPO |

### 5.4 DORA - Incidenti ICT Rilevanti (Art. 19)

| Criterio | Soglia |
|----------|--------|
| Clienti impattati | >10% clientela o >100.000 |
| Durata | >2 ore per servizi critici |
| Impatto geografico | >2 Stati Membri |
| Perdita dati | Integrità dati critici |
| Perdita economica | Criteri ente vigilanza |

### 5.5 Matrice Notifiche

| Tipo Incidente | NIS2 | GDPR | DORA | Clienti | Forze Ordine |
|----------------|------|------|------|---------|--------------|
| Ransomware con esfiltrazione | ✓ | ✓ | ✓ | Valutare | Valutare |
| Data breach PII | ○ | ✓ | ○ | ✓ | Valutare |
| DDoS prolungato | ✓ | ○ | ✓ | ✓ | ○ |
| Compromissione fornitore | ✓ | Valutare | ✓ | Valutare | ○ |
| Insider theft | ○ | ✓ | ○ | Valutare | ✓ |

✓ = Obbligatorio | ○ = Se applicabile | Valutare = Case-by-case

---

## 6. Ruoli e Responsabilità

### 6.1 Incident Response Team (IRT)

| Ruolo | Responsabilità | Contatto |
|-------|----------------|----------|
| **Incident Manager** | Coordinamento, decisioni, comunicazione | [NOME/TEL] |
| **Security Analyst** | Investigazione, contenimento, eradicazione | [NOME/TEL] |
| **IT Operations** | Azioni tecniche, recovery | [NOME/TEL] |
| **Communications** | Comunicazione interna/esterna | [NOME/TEL] |
| **Legal/Compliance** | Aspetti legali, notifiche | [NOME/TEL] |
| **Business Owner** | Decisioni impatto business | [VARIABILE] |

### 6.2 RACI Matrix

| Attività | CISO | Inc. Manager | Security | IT Ops | Legal | Business |
|----------|------|--------------|----------|--------|-------|----------|
| Dichiarare incidente | A | R | C | I | I | I |
| Contenimento | A | R | R | R | I | C |
| Notifica autorità | A | C | I | I | R | I |
| Comunicazione clienti | A | R | I | I | C | C |
| Recovery | I | A | C | R | I | C |
| Post-incident review | A | R | R | C | C | C |

### 6.3 Escalation Path

```
Level 1: SOC/Help Desk
    │
    ▼ (P3-P4)
Level 2: Security Team
    │
    ▼ (P2)
Level 3: Incident Manager + IRT
    │
    ▼ (P1)
Level 4: CISO + Crisis Team
    │
    ▼ (Business Critical)
Level 5: Executive/Board
```

---

## 7. Comunicazione

### 7.1 Template Comunicazione Interna

**Oggetto:** [CONFIDENTIAL] Security Incident - [CODICE] - [STATUS]

```
INCIDENT BRIEFING
-----------------
Incident ID: [INC-YYYY-NNNN]
Severity: [P1/P2/P3/P4]
Status: [Investigating/Containing/Recovering/Closed]

SUMMARY:
[Breve descrizione dell'incidente]

IMPACTED SYSTEMS:
- [Lista sistemi]

CURRENT ACTIONS:
- [Azioni in corso]

REQUIRED ACTIONS:
- [Azioni richieste al destinatario]

NEXT UPDATE: [Data/ora]

Contact: [Incident Manager] - [Tel]
```

### 7.2 Template Comunicazione Clienti

**Oggetto:** Notifica di Sicurezza - {{company_name}}

```
Gentile Cliente,

La informiamo che in data {{document_date}} abbiamo rilevato un incidente
di sicurezza che potrebbe aver coinvolto i seguenti dati:
- [Categoria dati]

COSA È SUCCESSO:
[Descrizione non tecnica]

QUALI DATI SONO COINVOLTI:
[Lista categorie]

COSA STIAMO FACENDO:
[Azioni intraprese]

COSA PUÒ FARE LEI:
[Raccomandazioni per il cliente]

Per qualsiasi domanda, contatti: {{email_phone}}

Ci scusiamo per l'inconveniente.
```

### 7.3 Notifica Data Breach al Garante Privacy (GDPR Art. 33)

La notifica al Garante per la Protezione dei Dati Personali deve essere effettuata entro 72 ore dal momento in cui l'Organizzazione viene a conoscenza della violazione. Se la notifica avviene oltre le 72 ore, deve essere corredata da una motivazione del ritardo.

```
NOTIFICA DATA BREACH AL GARANTE PRIVACY
========================================
(Modello per compilazione sul portale del Garante)

1. TITOLARE DEL TRATTAMENTO
   Denominazione: {{company_name}}
   Indirizzo: {{company_address}}
   Referente: {{dpo_name}} (DPO)
   Email: {{dpo_email}}
   Telefono: {{dpo_phone}}

2. VIOLAZIONE
   Data/Ora scoperta: [GG/MM/AAAA HH:MM]
   Data/Ora presunta violazione: [GG/MM/AAAA HH:MM]
   Natura della violazione:
   [ ] Violazione della riservatezza (accesso/divulgazione non autorizzata)
   [ ] Violazione dell'integrità (alterazione non autorizzata)
   [ ] Violazione della disponibilità (perdita/distruzione)

3. CATEGORIE DI DATI COINVOLTI
   [ ] Dati identificativi (nome, cognome, CF)
   [ ] Dati di contatto (email, telefono, indirizzo)
   [ ] Dati finanziari (IBAN, carte di credito)
   [ ] Dati sanitari
   [ ] Dati biometrici
   [ ] Credenziali di accesso
   [ ] Altro: [specificare]

4. NUMERO APPROSSIMATIVO DI INTERESSATI: [N]
   NUMERO APPROSSIMATIVO DI RECORD: [N]

5. DESCRIZIONE DELLA VIOLAZIONE
   [Descrizione dettagliata di cosa è accaduto, come è stata
    scoperta e quali sistemi sono coinvolti]

6. CONSEGUENZE PROBABILI
   [Descrizione dei possibili effetti sugli interessati:
    furto identità, perdita finanziaria, discriminazione, ecc.]

7. MISURE ADOTTATE O PROPOSTE
   [Elenco delle misure di contenimento e mitigazione:
    es. reset password, notifica interessati, isolamento sistemi]

8. COMUNICAZIONE AGLI INTERESSATI
   [ ] Effettuata in data [GG/MM/AAAA]
   [ ] Non necessaria (motivazione: cifratura, rischio non elevato)
   [ ] Prevista entro [data]

Note: Compilato da [Nome] - Data: [GG/MM/AAAA]
```

### 7.4 Notifica Incidente Significativo al CSIRT Italia (NIS2 Art. 23)

Per le entità soggette alla Direttiva NIS2, la notifica al CSIRT Italia (presso l'Agenzia per la Cybersicurezza Nazionale — ACN) segue tempistiche stringenti e progressive.

| Fase | Tempistica | Contenuto | Canale |
|------|------------|-----------|--------|
| **Early warning** | Entro 24 ore dalla conoscenza | Sospetto incidente significativo, possibile causa dolosa, possibile impatto transfrontaliero | PEC al CSIRT / Portale ACN |
| **Notifica formale** | Entro 72 ore dalla conoscenza | Valutazione iniziale: gravità, impatto, IoC (Indicatori di Compromissione) | Portale ACN |
| **Report intermedio** | Su richiesta CSIRT | Aggiornamenti sullo stato di gestione, azioni di contenimento | Portale ACN |
| **Report finale** | Entro 1 mese dalla notifica formale | Descrizione dettagliata, root cause, misure adottate, impatto transfrontaliero | Portale ACN |

**Criteri per incidente "significativo" (NIS2 Art. 23.3):**
- Ha causato o è in grado di causare grave perturbazione operativa dei servizi o perdite finanziarie per l'entità
- Ha interessato o è in grado di interessare altre persone fisiche o giuridiche causando perdite materiali o immateriali considerevoli

### 7.5 SLA di Escalation

Per garantire tempi di risposta adeguati, l'Organizzazione definisce i seguenti SLA di escalation automatica:

| Priorità | Tempo senza aggiornamento | Escalation automatica a | Azione |
|-----------|---------------------------|------------------------|--------|
| **P1** | 30 minuti | IT Manager | Conferma presa in carico |
| **P1** | 2 ore | CISO | Status update e conferma contenimento |
| **P1** | 4 ore | Direzione Generale | Briefing e decisioni strategiche |
| **P2** | 1 ora | IT Manager | Conferma presa in carico |
| **P2** | 4 ore | CISO | Status update |
| **P2** | 8 ore | Direzione | Briefing se necessario |
| **P3** | 4 ore | IT Manager | Status update |
| **P3** | 24 ore | CISO | Review se non risolto |
| **P4** | 8 ore | IT Ops Lead | Status update |

### 7.6 Comunicazione con Autorità — Riferimenti

| Autorità | Canale | Formato | Tempistica |
|----------|--------|---------|------------|
| Garante Privacy | Portale online garante.it | Modulistica standard (vedi 7.3) | 72 ore (GDPR Art. 33) |
| ACN / CSIRT Italia | PEC / Portale ACN | Formato NIS2 (vedi 7.4) | 24h early warning / 72h notifica |
| Polizia Postale | Denuncia / PEC | Denuncia formale | Tempestiva per reati informatici |
| Ente Vigilanza (DORA) | Canale dedicato regolatore | Formato regolatore settoriale | 4h classificazione iniziale |

---

## 8. Strumenti e Risorse

### 8.1 Toolkit Incident Response

| Strumento | Utilizzo | Responsabile |
|-----------|----------|--------------|
| SIEM | Detection, correlation, alerting | SOC |
| EDR | Endpoint detection and response | Security |
| Forensic toolkit | Acquisizione e analisi prove | Security |
| Ticketing | Tracking incidenti | IRT |
| Secure comms | Comunicazione team | IRT |
| Threat intel | IOC, TTP | Security |

### 8.2 Documentazione di Supporto

| Documento | Ubicazione |
|-----------|------------|
| Playbook per tipo incidente | {{url}} |
| Contatti emergenza | {{url}} |
| Inventario asset critici | {{url}} |
| Procedure di backup/restore | {{url}} |
| Template notifiche | {{url}} |

---

## 9. Test e Esercitazioni

### 9.1 Piano di Test

| Tipo | Frequenza | Partecipanti | Obiettivo |
|------|-----------|--------------|-----------|
| Tabletop | Semestrale | IRT + Management | Validare procedure |
| Drill tecnico | Trimestrale | Security + IT | Testare capability |
| Red Team | Annuale | Esterni | Test realistico |
| Full simulation | Annuale | Intera organizzazione | Business continuity |

### 9.2 Scenari di Test
1. Ransomware su file server critico
2. Data breach cliente via phishing
3. Compromissione account privilegiato
4. DDoS su servizi pubblici
5. Insider data theft
6. Supply chain attack

---

## 10. Metriche e KPI

### 10.1 Metriche Operative

| Metrica | Formula | Target |
|---------|---------|--------|
| MTTD (Mean Time to Detect) | Σ(tempo rilevamento)/n | < 1 ora |
| MTTC (Mean Time to Contain) | Σ(tempo contenimento)/n | < 4 ore |
| MTTR (Mean Time to Resolve) | Σ(tempo risoluzione)/n | < 24 ore (P1) |
| Incident Rate | Incidenti/mese | Trend ↓ |
| False Positive Rate | FP/Total alerts | < 20% |

### 10.2 Dashboard Incidenti

| Indicatore | Q1 | Q2 | Q3 | Q4 | YTD |
|------------|----|----|----|----|-----|
| Totale incidenti | | | | | |
| Di cui P1 | | | | | |
| Di cui P2 | | | | | |
| MTTD medio | | | | | |
| MTTC medio | | | | | |
| % SLA rispettati | | | | | |
| Notifiche autorità | | | | | |

---

## 11. Allegati

### Allegato A - Incident Report Template

```
INCIDENT REPORT
===============

SEZIONE 1: INFORMAZIONI GENERALI
--------------------------------
Incident ID: INC-{{document_year}}-[NNNN]
Data/Ora Rilevamento: {{timestamp}}
Data/Ora Chiusura: {{timestamp}}
Durata Totale: [HH:MM]
Classificazione: [CATEGORIA]
Priorità: [P1/P2/P3/P4]
Incident Manager: {{contact_name}}

SEZIONE 2: DESCRIZIONE
----------------------
Descrizione evento:
[Descrizione dettagliata]

Sistemi impattati:
- [Sistema 1]
- [Sistema 2]

Dati coinvolti:
- [Categoria dati]

SEZIONE 3: TIMELINE
-------------------
{{timestamp}} - Evento
{{timestamp}} - Rilevamento
{{timestamp}} - Triage completato
{{timestamp}} - Contenimento iniziato
{{timestamp}} - Contenimento completato
{{timestamp}} - Eradicazione completata
{{timestamp}} - Recovery completato
{{timestamp}} - Incidente chiuso

SEZIONE 4: IMPATTO
------------------
Impatto business: {{description}}
Impatto dati: {{description}}
Impatto reputazionale: {{description}}
Costo stimato: [€]

SEZIONE 5: ROOT CAUSE
---------------------
Causa principale: {{description}}
Vettore di attacco: {{description}}
Vulnerabilità sfruttata: [CVE/DESCRIZIONE]

SEZIONE 6: AZIONI INTRAPRESE
----------------------------
Contenimento:
- [Azione 1]

Eradicazione:
- [Azione 1]

Recovery:
- [Azione 1]

SEZIONE 7: NOTIFICHE
--------------------
| Destinatario | Data | Esito |
|--------------|------|-------|
| [DEST] | {{document_date}} | [ESITO] |

SEZIONE 8: LESSON LEARNED
-------------------------
Cosa ha funzionato:
- [Punto 1]

Cosa migliorare:
- [Punto 1]

SEZIONE 9: ACTION ITEMS
-----------------------
| Azione | Owner | Scadenza | Status |
|--------|-------|----------|--------|
| {{action}} | [OWNER] | {{document_date}} | [STATUS] |

APPROVAZIONI
------------
Incident Manager: _______________ Data: ___
CISO: _______________ Data: ___
```

### Allegato B - Contatti Emergenza

| Ruolo | Nome | Tel Ufficio | Tel Mobile | Email |
|-------|------|-------------|------------|-------|
| CISO | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| Incident Manager On-Call | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| IT Manager | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| DPO | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| Legal | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| CEO | {{contact_name}} | {{contact_phone}} | {{contact_phone}} | {{contact_email}} |
| SOC (24/7) | - | {{contact_phone}} | - | {{contact_email}} |

**Contatti Esterni:**
| Organizzazione | Telefono | Email/PEC |
|----------------|----------|-----------|
| ACN - CSIRT Italia | {{contact_phone}} | {{contact_email}} |
| Garante Privacy | {{contact_phone}} | {{pec_email}} |
| Polizia Postale | {{contact_phone}} | {{contact_email}} |
| Fornitore IR | {{contact_phone}} | {{contact_email}} |
| Cyber Insurance | {{contact_phone}} | {{contact_email}} |

---

## 12. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 13. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{security_officer_title}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Politica di Sicurezza delle Informazioni | {{company_name}}-POL-ISMS-001 | Policy madre |
| Risk Register | {{company_name}}-REG-ISMS-001 | Rischi R-001 a R-015 — alimentati da lesson learned |
| Procedura di Backup e Recovery | {{company_name}}-BKP-ISMS-001 | Recovery post-incidente |
| Piano di Continuità Operativa | {{company_name}}-BCP-BCMS-001 | Attivazione BCP per incidenti maggiori |
| Inventario degli Asset | {{company_name}}-INV-ISMS-001 | Identificazione asset impattati |
| Politica Uso Accettabile | {{company_name}}-AUP-ISMS-001 | Violazioni che generano incidenti |
| Informativa Privacy Dipendenti | — | Monitoraggio e raccolta prove |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{security_officer_title}}` | Owner e Approvazioni | ☐ |
| 6 | `{{contact_name}}` | Allegato B — contatti emergenza e Approvazioni | ☐ |
| 7 | `{{contact_phone}}` | Allegato B — numeri telefono | ☐ |
| 8 | `{{contact_email}}` | Allegato B — indirizzi email | ☐ |
| 9 | `{{dpo_name}}` | Sezione 7.3 — notifica GDPR | ☐ |
| 10 | `{{dpo_email}}` | Sezione 7.3 — contatto DPO | ☐ |
| 11 | `{{dpo_phone}}` | Sezione 7.3 — telefono DPO | ☐ |
| 12 | `{{company_address}}` | Sezione 7.3 — sede legale | ☐ |
| 13 | `{{email_phone}}` | Sezione 7.2 — contatto per clienti | ☐ |
| 14 | IRT membri nominati | Sezione 4 — tutti i ruoli assegnati | ☐ |
| 15 | Contatti esterni compilati | Allegato B — ACN, Garante, Polizia Postale, assicurazione | ☐ |
| 16 | Playbook per tipo incidente | Sezione 8.2 — URL o riferimento documenti | ☐ |
