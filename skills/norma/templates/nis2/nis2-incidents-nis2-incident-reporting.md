---
title: Procedura di Notifica Incidenti NIS2
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: CISO
approver: Alta Direzione
framework: NIS2
language: IT
documentType: procedure
directive_articles:
  - Art. 23 - Obblighi di notifica
  - Art. 30 - Notifica volontaria
  - Considerando 101-108 - Notifica incidenti
national_transposition: D.Lgs. 138/2024
cross_references:
  - 'ISO 27001:2022 A.5.24-5.28'
  - GDPR Art. 33-34
  - Linee guida ACN per la notifica incidenti
  - D.Lgs. 138/2024 Art. 25 - Obblighi di notifica
related_documents:
  - document: NIS2 Business Continuity Plan
    path: ../continuity/nis2-business-continuity-plan.md
  - document: NIS2 Governance & Accountability
    path: ../governance/nis2-governance-accountability.md
  - document: NIS2 Risk Management Measures
    path: ../risk/nis2-risk-management-measures.md
  - document: NIS2 Compliance Checklist
    path: ../compliance/nis2-compliance-checklist.md
  - document: PIMS Data Breach Notification
    path: ../../pims/procedures/data-breach-notification-procedure.md
status: Bozza
subset: true
---

# NIS2 Incident Reporting Procedure

## 1. Introduzione

### 1.1 Scopo

{{company_name}} riconosce che la tempestiva notifica degli incidenti di sicurezza alle autorità competenti costituisce un obbligo fondamentale ai sensi della Direttiva (UE) 2022/2555 e un elemento essenziale per la protezione collettiva dell'ecosistema digitale europeo. L'Articolo 23 della NIS2 stabilisce una timeline stringente di notifica che richiede la trasmissione di un early warning entro 24 ore dalla rilevazione di un incidente significativo, seguita da una notifica dettagliata entro 72 ore e da un report finale entro un mese.

La presente procedura definisce il processo che {{company_name}} adotta per identificare, classificare e notificare gli incidenti di sicurezza che superano le soglie di significatività stabilite dalla Direttiva. Il documento fornisce criteri chiari per determinare quando un incidente richiede la notifica alle autorità, distinguendo tra eventi che possono essere gestiti internamente e quelli che comportano obblighi di comunicazione verso il CSIRT nazionale e l'Agenzia per la Cybersicurezza Nazionale (ACN).

L'organizzazione integra il processo di notifica NIS2 con le procedure esistenti di incident response e con gli obblighi di comunicazione previsti dal GDPR in caso di data breach, assicurando un coordinamento efficace tra le diverse funzioni coinvolte e il rispetto di tutte le timeline normative applicabili.

### 1.2 Ambito di Applicazione

- Tutti gli incidenti che impattano la fornitura di servizi essenziali/importanti
- Incidenti che potrebbero causare danni operativi, finanziari o reputazionali significativi
- Incidenti con potenziale impatto transfrontaliero

### 1.3 Definizioni

| Termine | Definizione (Art. 6 NIS2) |
|---------|---------------------------|
| **Incidente** | Evento che compromette disponibilità, autenticità, integrità o riservatezza di dati o servizi |
| **Incidente significativo** | Incidente che ha causato o può causare grave perturbazione operativa o perdite finanziarie |
| **Quasi-incidente (Near miss)** | Evento che avrebbe potuto compromettere la sicurezza ma non ha causato danni |
| **Minaccia informatica** | Potenziale circostanza, evento o azione che può danneggiare i sistemi |

---

## 2. Timeline di Notifica NIS2

### 2.1 Fasi Obbligatorie

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    NIS2 INCIDENT REPORTING TIMELINE                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  T0: DETECTION                                                              │
│  ─────────────                                                              │
│       │                                                                     │
│       ▼                                                                     │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ FASE 1: EARLY WARNING (Art. 23.4.a)                                 │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                   │   │
│  │ • Deadline: 24 ORE dalla rilevazione                                │   │
│  │ • Contenuto: Sospetto origine malevola, potenziale transfrontaliero │   │
│  │ • Destinatario: CSIRT nazionale (ACN in Italia)                     │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│       │                                                                     │
│       ▼ (+48h)                                                              │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ FASE 2: INCIDENT NOTIFICATION (Art. 23.4.b)                         │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                           │   │
│  │ • Deadline: 72 ORE dalla rilevazione (aggiorna early warning)       │   │
│  │ • Contenuto: Valutazione iniziale, severità, impatto, IoC           │   │
│  │ • Destinatario: CSIRT nazionale + Autorità competente               │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│       │                                                                     │
│       ▼ (+1 mese)                                                           │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ FASE 3: FINAL REPORT (Art. 23.4.d)                                  │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                                  │   │
│  │ • Deadline: 1 MESE dalla notification (o chiusura incidente)        │   │
│  │ • Contenuto: Descrizione dettagliata, root cause, misure adottate   │   │
│  │ • Destinatario: CSIRT nazionale + Autorità competente               │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│       │                                                                     │
│       ▼ (se ongoing)                                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │ FASE 4: PROGRESS REPORT (Art. 23.4.c)                               │   │
│  │ ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━                               │   │
│  │ • Quando: Se incidente ancora in corso al momento del report        │   │
│  │ • Contenuto: Aggiornamento stato, progress, nuove informazioni      │   │
│  │ • Frequenza: Su richiesta CSIRT o cambiamenti significativi         │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 2.2 Riepilogo Deadline

| Fase | Deadline | Contenuto Principale | Note |
|------|----------|---------------------|------|
| **Early Warning** | 24 ore | Sospetto incidente significativo | Immediato se ransomware/breach |
| **Incident Notification** | 72 ore | Assessment iniziale, impatto, IoC | Aggiorna early warning |
| **Intermediate Report** | Su richiesta | Status update, progress | Se incidente ongoing |
| **Final Report** | 1 mese | Root cause, remediation completa | Dalla notification |

---

## 3. Criteri per Incidente Significativo

### 3.1 Soglie di Significatività (Art. 23.3)

Un incidente è considerato **significativo** se soddisfa UNO dei seguenti criteri:

| Criterio | Soglia | Esempi |
|----------|--------|--------|
| **Grave perturbazione operativa** | Interruzione > 25% capacità o > 4h servizio critico | Downtime sistema core |
| **Perdite finanziarie** | > €500K dirette o > €2M totali | Ransomware, frode |
| **Impatto su altre entità** | Qualsiasi impatto su terzi | Supply chain, clienti |
| **Compromissione dati** | > 10.000 interessati o dati sensibili | Data breach |
| **Impatto safety** | Qualsiasi rischio per incolumità | Sistemi OT/ICS |
| **Impatto transfrontaliero** | Coinvolge altri Stati Membri | Cross-border service |

### 3.2 Matrice di Classificazione

| Tipo Incidente | Automaticamente Significativo | Valutazione Necessaria |
|----------------|------------------------------|------------------------|
| Ransomware | ✓ Sempre | - |
| Data breach > 1000 record | ✓ Sempre | - |
| Compromissione sistema critico | ✓ Sempre | - |
| DDoS > 4 ore | ✓ | Valutare impatto |
| Phishing con compromissione | - | ✓ Valutare scope |
| Malware isolato | - | ✓ Valutare diffusione |
| Vulnerability sfruttata | - | ✓ Valutare impatto |
| Insider threat | - | ✓ Valutare danni |

### 3.3 Decision Tree

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INCIDENT SIGNIFICATIVITY ASSESSMENT                       │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌────────────────────────────────────┐                                     │
│  │ Incidente rilevato                 │                                     │
│  └─────────────────┬──────────────────┘                                     │
│                    │                                                         │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐      ┌──────────────────────────┐  │
│  │ Ransomware o Data Breach confermato│──YES─▶│ SIGNIFICATIVO            │  │
│  └─────────────────┬──────────────────┘      │ → Early Warning 24h      │  │
│                    │ NO                       └──────────────────────────┘  │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐      ┌──────────────────────────┐  │
│  │ Sistema critico compromesso?       │──YES─▶│ SIGNIFICATIVO            │  │
│  └─────────────────┬──────────────────┘      │ → Early Warning 24h      │  │
│                    │ NO                       └──────────────────────────┘  │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐      ┌──────────────────────────┐  │
│  │ Downtime > 4h o impatto > 25%?     │──YES─▶│ SIGNIFICATIVO            │  │
│  └─────────────────┬──────────────────┘      │ → Early Warning 24h      │  │
│                    │ NO                       └──────────────────────────┘  │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐      ┌──────────────────────────┐  │
│  │ Impatto su terze parti/clienti?    │──YES─▶│ SIGNIFICATIVO            │  │
│  └─────────────────┬──────────────────┘      │ → Early Warning 24h      │  │
│                    │ NO                       └──────────────────────────┘  │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐      ┌──────────────────────────┐  │
│  │ Perdite stimate > €500K?           │──YES─▶│ SIGNIFICATIVO            │  │
│  └─────────────────┬──────────────────┘      │ → Early Warning 24h      │  │
│                    │ NO                       └──────────────────────────┘  │
│                    ▼                                                         │
│  ┌────────────────────────────────────┐                                     │
│  │ NON SIGNIFICATIVO                  │                                     │
│  │ → Gestione interna standard        │                                     │
│  │ → Registrazione incidente          │                                     │
│  │ → Possibile notifica volontaria    │                                     │
│  └────────────────────────────────────┘                                     │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 4. Template Notifiche

### 4.1 Early Warning (24 ore)

#### Modulo Early Warning

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    EARLY WARNING - NIS2 Art. 23.4.a                         │
│                    Da inviare entro 24 ORE dalla rilevazione                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ SEZIONE A: DATI ENTITÀ                                                      │
│ ─────────────────────                                                       │
│ Ragione Sociale: _________________________________________________________  │
│ P.IVA/CF: ________________________________________________________________  │
│ Settore NIS2: ☐ Annex I (Essential) ☐ Annex II (Important)                 │
│ Sottosettore: ____________________________________________________________  │
│ Referente Notifica: ______________________________________________________  │
│ Email: ______________________________ Tel: _______________________________  │
│                                                                             │
│ SEZIONE B: INFORMAZIONI INCIDENTE                                           │
│ ─────────────────────────────────                                           │
│ ID Incidente interno: ____________________________________________________  │
│ Data/ora rilevazione: ____________________________________________________  │
│ Data/ora stimata inizio: _________________________________________________  │
│                                                                             │
│ Tipo incidente:                                                             │
│ ☐ Ransomware/Malware    ☐ Data breach           ☐ DDoS                     │
│ ☐ Compromissione sistema ☐ Phishing/Social eng.  ☐ Insider threat          │
│ ☐ Supply chain attack    ☐ Vulnerabilità sfruttata ☐ Altro: _____________  │
│                                                                             │
│ SEZIONE C: VALUTAZIONE PRELIMINARE                                          │
│ ──────────────────────────────────                                          │
│ Sospetto origine malevola: ☐ Sì ☐ No ☐ In valutazione                      │
│                                                                             │
│ Se sì, tipo di threat actor sospetto:                                       │
│ ☐ Cybercrime    ☐ State-sponsored    ☐ Hacktivism                          │
│ ☐ Insider       ☐ Sconosciuto                                              │
│                                                                             │
│ Potenziale impatto transfrontaliero: ☐ Sì ☐ No ☐ In valutazione            │
│ Se sì, Stati Membri coinvolti: __________________________________________   │
│                                                                             │
│ Impatto stimato sui servizi:                                                │
│ ☐ Servizi completamente non disponibili                                     │
│ ☐ Servizi parzialmente degradati                                            │
│ ☐ Servizi operativi con limitazioni                                         │
│ ☐ Ancora in valutazione                                                     │
│                                                                             │
│ SEZIONE D: AZIONI IMMEDIATE                                                 │
│ ───────────────────────────                                                 │
│ Azioni di contenimento avviate: ☐ Sì ☐ No                                  │
│ Descrizione: _____________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ SEZIONE E: DICHIARAZIONI                                                    │
│ ─────────────────────────                                                   │
│ ☐ Confermo che questo early warning viene inviato entro 24 ore             │
│   dalla rilevazione dell'incidente                                          │
│ ☐ Mi impegno a fornire incident notification entro 72 ore                  │
│                                                                             │
│ Nome: __________________________ Ruolo: _________________________________   │
│ Data: __________________________ Ora: ___________________________________   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.2 Incident Notification (72 ore)

#### Modulo Incident Notification

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                 INCIDENT NOTIFICATION - NIS2 Art. 23.4.b                    │
│                 Da inviare entro 72 ORE dalla rilevazione                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ SEZIONE A: RIFERIMENTI                                                      │
│ ──────────────────────                                                      │
│ Riferimento Early Warning: ______________________________________________   │
│ Data Early Warning: _____________________________________________________   │
│ ID Incidente interno: ___________________________________________________   │
│                                                                             │
│ SEZIONE B: DATI ENTITÀ (come Early Warning)                                 │
│ ──────────────────────────────────────────                                  │
│ [Compilare se diversi da Early Warning]                                     │
│                                                                             │
│ SEZIONE C: DESCRIZIONE INCIDENTE                                            │
│ ────────────────────────────────                                            │
│ Descrizione dettagliata dell'incidente:                                     │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ Vettore di attacco identificato:                                            │
│ ☐ Email (phishing/malware)     ☐ Web application vulnerability             │
│ ☐ Remote access vulnerability  ☐ Supply chain compromise                   │
│ ☐ Physical access              ☐ Social engineering                        │
│ ☐ Insider                      ☐ Non ancora identificato                   │
│ ☐ Altro: _______________________________________________________________   │
│                                                                             │
│ SEZIONE D: VALUTAZIONE IMPATTO                                              │
│ ──────────────────────────────                                              │
│                                                                             │
│ Severità incidente: ☐ Critica ☐ Alta ☐ Media ☐ Bassa                       │
│                                                                             │
│ Sistemi/servizi impattati:                                                  │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ Numero utenti/clienti impattati: ________________________________________   │
│ Area geografica impattata: ______________________________________________   │
│ Durata interruzione (se applicabile): ___________________________________   │
│                                                                             │
│ Impatto operativo:                                                          │
│ ☐ Interruzione totale servizio critico                                      │
│ ☐ Degradazione significativa (>25% capacità)                                │
│ ☐ Degradazione limitata                                                     │
│ ☐ Nessun impatto operativo diretto                                          │
│                                                                             │
│ Impatto finanziario stimato: €__________________________________________    │
│                                                                             │
│ Dati compromessi:                                                           │
│ ☐ Nessun dato compromesso                                                   │
│ ☐ Dati operativi/tecnici                                                    │
│ ☐ Dati personali (specificare): ________________________________________   │
│ ☐ Dati finanziari                                                           │
│ ☐ Proprietà intellettuale                                                   │
│ ☐ Altro: _______________________________________________________________   │
│                                                                             │
│ SEZIONE E: INDICATORS OF COMPROMISE (IoC)                                   │
│ ─────────────────────────────────────────                                   │
│                                                                             │
│ IP Address malevoli: ____________________________________________________   │
│ Domini malevoli: ________________________________________________________   │
│ Hash file (MD5/SHA256): _________________________________________________   │
│ Email mittente: _________________________________________________________   │
│ TTP identificate (MITRE ATT&CK): ________________________________________   │
│ Altri IoC: ______________________________________________________________   │
│                                                                             │
│ SEZIONE F: AZIONI INTRAPRESE                                                │
│ ────────────────────────────                                                │
│                                                                             │
│ Misure di contenimento:                                                     │
│ ☐ Isolamento sistemi compromessi                                            │
│ ☐ Blocco account compromessi                                                │
│ ☐ Blocco IP/domini malevoli                                                 │
│ ☐ Attivazione incident response team                                        │
│ ☐ Coinvolgimento forze dell'ordine                                          │
│ ☐ Altro: _______________________________________________________________   │
│                                                                             │
│ Dettaglio azioni:                                                           │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ SEZIONE G: IMPATTO TRANSFRONTALIERO                                         │
│ ───────────────────────────────────                                         │
│                                                                             │
│ L'incidente ha impatto su altri Stati Membri: ☐ Sì ☐ No                    │
│ Se sì:                                                                      │
│ Stati Membri coinvolti: _________________________________________________   │
│ Tipo di impatto: ________________________________________________________   │
│ Entità potenzialmente impattate: ________________________________________   │
│                                                                             │
│ SEZIONE H: DICHIARAZIONI                                                    │
│ ─────────────────────────                                                   │
│ ☐ Confermo accuratezza delle informazioni fornite                          │
│ ☐ Mi impegno a fornire aggiornamenti significativi                         │
│ ☐ Mi impegno a fornire report finale entro 1 mese                          │
│                                                                             │
│ Nome: __________________________ Ruolo: _________________________________   │
│ Data: __________________________ Ora: ___________________________________   │
│ Firma: __________________________________________________________________   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 4.3 Final Report (1 mese)

#### Modulo Final Report

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    FINAL REPORT - NIS2 Art. 23.4.d                          │
│                    Da inviare entro 1 MESE dalla notification               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│ SEZIONE A: RIFERIMENTI                                                      │
│ ──────────────────────                                                      │
│ Riferimento Incident Notification: ______________________________________   │
│ ID Incidente interno: ___________________________________________________   │
│ Data incident notification: _____________________________________________   │
│                                                                             │
│ SEZIONE B: CRONOLOGIA COMPLETA                                              │
│ ──────────────────────────────                                              │
│                                                                             │
│ | Data/Ora | Evento | Azione |                                              │
│ |----------|--------|--------|                                              │
│ | | | |                                                                     │
│ | | | |                                                                     │
│ | | | |                                                                     │
│                                                                             │
│ SEZIONE C: DESCRIZIONE DETTAGLIATA                                          │
│ ──────────────────────────────────                                          │
│                                                                             │
│ C.1 Descrizione completa dell'incidente:                                    │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ C.2 Tipo di minaccia/attacco (classificazione finale):                      │
│ ___________________________________________________________________________  │
│                                                                             │
│ C.3 Probabile origine (se determinata):                                     │
│ ☐ Cybercriminale       ☐ State-sponsored                                   │
│ ☐ Hacktivista          ☐ Insider                                           │
│ ☐ Accidentale          ☐ Non determinabile                                 │
│                                                                             │
│ SEZIONE D: ROOT CAUSE ANALYSIS                                              │
│ ──────────────────────────────                                              │
│                                                                             │
│ D.1 Causa radice identificata:                                              │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ D.2 Fattori contribuenti:                                                   │
│ ☐ Vulnerabilità software non patchata                                       │
│ ☐ Configurazione errata                                                     │
│ ☐ Errore umano                                                              │
│ ☐ Mancanza di controlli adeguati                                            │
│ ☐ Processo inadeguato                                                       │
│ ☐ Altro: _______________________________________________________________   │
│                                                                             │
│ D.3 Dettaglio vulnerabilità sfruttate (se applicabile):                     │
│ CVE: _____________________________________________________________________   │
│ Descrizione: _____________________________________________________________  │
│                                                                             │
│ SEZIONE E: IMPATTO FINALE                                                   │
│ ─────────────────────────                                                   │
│                                                                             │
│ E.1 Impatto operativo totale:                                               │
│ Durata totale interruzione: ______________________________________________  │
│ Servizi impattati: ______________________________________________________   │
│ Percentuale capacità persa: _____________________________________________   │
│                                                                             │
│ E.2 Impatto su utenti/clienti:                                              │
│ Numero totale impattati: ________________________________________________   │
│ Tipo di impatto: ________________________________________________________   │
│                                                                             │
│ E.3 Impatto finanziario (valori finali):                                    │
│ Costi diretti: €________________________________________________________    │
│ Costi indiretti stimati: €______________________________________________    │
│ Costi di remediation: €_________________________________________________    │
│                                                                             │
│ E.4 Dati compromessi (conferma finale):                                     │
│ Tipo dati: ______________________________________________________________   │
│ Volume: _________________________________________________________________   │
│ Esfiltrazione confermata: ☐ Sì ☐ No ☐ Non determinabile                    │
│                                                                             │
│ SEZIONE F: MISURE ADOTTATE                                                  │
│ ──────────────────────────                                                  │
│                                                                             │
│ F.1 Azioni di contenimento:                                                 │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ F.2 Azioni di eradicazione:                                                 │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ F.3 Azioni di recovery:                                                     │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ F.4 Misure di mitigazione implementate:                                     │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ SEZIONE G: LESSONS LEARNED E MIGLIORAMENTI                                  │
│ ──────────────────────────────────────────                                  │
│                                                                             │
│ G.1 Lessons learned:                                                        │
│ ___________________________________________________________________________  │
│ ___________________________________________________________________________  │
│                                                                             │
│ G.2 Miglioramenti pianificati:                                              │
│ | Azione | Responsabile | Deadline | Stato |                                │
│ |--------|--------------|----------|-------|                                │
│ | | | | |                                                                   │
│ | | | | |                                                                   │
│                                                                             │
│ SEZIONE H: COMUNICAZIONI EFFETTUATE                                         │
│ ───────────────────────────────────                                         │
│                                                                             │
│ ☐ Notifica GDPR Art. 33 al Garante Privacy                                 │
│ ☐ Notifica GDPR Art. 34 agli interessati                                   │
│ ☐ Comunicazione a forze dell'ordine                                         │
│ ☐ Comunicazione ad assicurazione cyber                                      │
│ ☐ Comunicazione pubblica/media                                              │
│ ☐ Altro: _______________________________________________________________   │
│                                                                             │
│ SEZIONE I: ALLEGATI                                                         │
│ ───────────────────                                                         │
│ ☐ Timeline dettagliata                                                      │
│ ☐ Log rilevanti (sanitizzati)                                               │
│ ☐ Report forensic                                                           │
│ ☐ IoC completi                                                              │
│ ☐ Piano di remediation                                                      │
│                                                                             │
│ SEZIONE J: DICHIARAZIONI FINALI                                             │
│ ───────────────────────────────                                             │
│ ☐ Confermo che l'incidente è stato completamente risolto                   │
│   Data risoluzione: _____________________________________________________   │
│ ☐ Confermo accuratezza e completezza delle informazioni                    │
│                                                                             │
│ Nome: __________________________ Ruolo: _________________________________   │
│ Data: __________________________ Firma: _________________________________   │
│                                                                             │
│ Approvato da (Management):                                                  │
│ Nome: __________________________ Ruolo: _________________________________   │
│ Data: __________________________ Firma: _________________________________   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 5. Processo Operativo

### 5.1 Workflow di Notifica

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    INCIDENT REPORTING WORKFLOW                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────────┐                                                       │
│  │ DETECTION        │  Security tools, SOC, employee report                │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ TRIAGE           │  Initial classification, severity assessment         │
│  │ (30 min)         │  Incident Manager on-call                            │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐     ┌────────────────────────────────────┐           │
│  │ SIGNIFICATIVITY  │────▶│ NON SIGNIFICATIVO                  │           │
│  │ ASSESSMENT       │ NO  │ → Standard incident management     │           │
│  │ (2 ore max)      │     │ → Internal logging                 │           │
│  └────────┬─────────┘     │ → Optional voluntary notification  │           │
│           │ YES           └────────────────────────────────────┘           │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ ESCALATION       │  Notify CISO, Legal, Management                      │
│  │ (immediate)      │  Activate IR team                                    │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ EARLY WARNING    │  Submit to CSIRT/ACN via portal                      │
│  │ (< 24h)          │  Document submission timestamp                       │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ INVESTIGATION    │  Forensics, impact assessment                        │
│  │ & CONTAINMENT    │  Evidence preservation                               │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ NOTIFICATION     │  Detailed notification to CSIRT/ACN                  │
│  │ (< 72h)          │  Include IoC, impact assessment                      │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ ERADICATION &    │  Remove threat, restore services                     │
│  │ RECOVERY         │  Update authorities as needed                        │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ FINAL REPORT     │  Complete root cause analysis                        │
│  │ (< 1 month)      │  Lessons learned, remediation plan                   │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌──────────────────┐                                                       │
│  │ CLOSE-OUT        │  Archive, update procedures                          │
│  │                  │  Implement improvements                              │
│  └──────────────────┘                                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### 5.2 Contatti per Notifica

| Autorità | Contatto | Canale | Note |
|----------|----------|--------|------|
| **CSIRT Italia (ACN)** | csirt@acn.gov.it | Portale ACN | Principale |
| **ACN** | [Portale NIS] | Portale dedicato | Per registrazione |
| **Garante Privacy** | protocollo@gpdp.it | Portale telematico | Se data breach GDPR |
| **Polizia Postale** | [Questura competente] | Denuncia | Se reato |

### 5.3 RACI Matrix

| Attività | CISO | IR Team | Legal | CEO | IT Ops | Comms |
|----------|------|---------|-------|-----|--------|-------|
| Detection & Triage | C | R | I | I | A | I |
| Significativity Assessment | A | R | C | I | C | I |
| Early Warning | A | R | C | I | C | I |
| Incident Investigation | A | R | C | I | C | I |
| 72h Notification | A | R | C | I | C | I |
| User Notification | C | I | C | A | I | R |
| Final Report | A | R | C | I | C | I |
| Lessons Learned | A | R | C | I | C | I |

**Legenda:** R = Responsible, A = Accountable, C = Consulted, I = Informed

---

## 6. Notifica agli Utenti (Art. 23.7)

### 6.1 Quando Notificare

La notifica agli utenti/destinatari dei servizi è richiesta quando:

- L'incidente può pregiudicare la fornitura del servizio
- Ci sono azioni che gli utenti possono intraprendere per mitigare l'impatto
- È necessario per trasparenza o obblighi contrattuali

### 6.2 Template Comunicazione Utenti

```
OGGETTO: Informativa su incidente di sicurezza - [Nome Servizio]

Gentile Cliente/Utente,

La informiamo che in data {{document_date}} abbiamo rilevato un incidente di sicurezza
che ha interessato [DESCRIZIONE GENERALE SERVIZIO/SISTEMA].

COSA È SUCCESSO
[Descrizione sintetica e comprensibile dell'incidente]

QUALI DATI/SERVIZI SONO STATI INTERESSATI
[Elenco servizi impattati, eventuali dati coinvolti]

COSA STIAMO FACENDO
[Azioni intraprese per risolvere l'incidente]

COSA PUÒ FARE LEI
[Azioni consigliate all'utente, es. cambio password, monitoraggio]

PROSSIMI PASSI
[Tempistiche previste per risoluzione, ulteriori comunicazioni]

Per qualsiasi informazione può contattare:
{{dedicated_contact}}

Ci scusiamo per il disagio.

Cordiali saluti,
[FIRMA]
```

---

## 7. Notifica Volontaria (Art. 30)

### 7.1 Quando Considerare

Anche se l'incidente non è "significativo", considerare notifica volontaria per:

- Near-miss che avrebbero potuto essere significativi
- Nuove minacce/vulnerabilità scoperte
- Incidenti che potrebbero interessare il settore
- Information sharing con ISAC di settore

### 7.2 Benefici

- Contributo alla sicurezza collettiva
- Accesso a threat intelligence dal CSIRT
- Dimostrazione di maturità security
- Possibili attenuanti in caso di future violazioni

---

## 8. Integrazione GDPR

### 8.1 Dual Notification

| Scenario | NIS2 | GDPR Art. 33 | GDPR Art. 34 |
|----------|------|--------------|--------------|
| Incidente IT senza dati personali | ✓ | ✗ | ✗ |
| Breach dati personali significativo | ✓ (24h) | ✓ (72h) | ✓ (se alto rischio) |
| Breach dati personali non significativo | ✗ | ✓ (72h) | ✓ (se alto rischio) |

### 8.2 Coordinamento Notifiche

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    DUAL NOTIFICATION WORKFLOW                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────────────┐                                                       │
│  │ INCIDENTE CON    │                                                       │
│  │ DATI PERSONALI   │                                                       │
│  └────────┬─────────┘                                                       │
│           │                                                                 │
│           ▼                                                                 │
│  ┌────────────────────────────────────────────────────────────────────┐    │
│  │                    PARALLEL ASSESSMENT                              │    │
│  │  ┌────────────────────┐      ┌────────────────────┐                │    │
│  │  │ NIS2 Assessment    │      │ GDPR Assessment    │                │    │
│  │  │ • Significativo?   │      │ • Rischio diritti? │                │    │
│  │  │ • Impatto servizi? │      │ • Alto rischio?    │                │    │
│  │  └─────────┬──────────┘      └─────────┬──────────┘                │    │
│  └────────────┼─────────────────────────────┼─────────────────────────┘    │
│               │                             │                               │
│               ▼                             ▼                               │
│  ┌────────────────────┐      ┌────────────────────┐                        │
│  │ NIS2 REPORTING     │      │ GDPR REPORTING     │                        │
│  │ • Early Warning 24h│      │ • Garante 72h      │                        │
│  │ • Notification 72h │      │ • Interessati      │                        │
│  │ • Final 1 month    │      │   (se alto rischio)│                        │
│  │ → ACN/CSIRT        │      │ → Garante Privacy  │                        │
│  └────────────────────┘      └────────────────────┘                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 9. Registro Incidenti

### 9.1 Template Registro

| ID | Data Rilev. | Tipo | Significativo | Early Warning | Notification | Final Report | Status |
|----|-------------|------|---------------|---------------|--------------|--------------|--------|
| INC-2025-001 | | | ☐ Sì ☐ No | Data: | Data: | Data: | |
| INC-2025-002 | | | ☐ Sì ☐ No | Data: | Data: | Data: | |

---

## 10. Documentazione Correlata

| Documento | Riferimento |
|-----------|-------------|
| Incident Response Plan | PLA-INC-001 |
| Crisis Communication Plan | PLA-CRI-001 |
| Business Continuity Plan | PLA-BC-001 |
| Data Breach Procedure (GDPR) | PRO-GDPR-001 |
| Contatti Emergenza | DOC-CONT-001 |

---

## 11. Revisione e Approvazione

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | | | |
| Verificato da (Legal) | | | |
| Approvato da (CISO) | | | |
| Approvato da (CEO) | | | |

---

*Questa procedura deve essere testata almeno 2 volte l'anno tramite esercitazioni tabletop e almeno 1 volta l'anno con simulazione operativa completa. Deve essere revisionata in caso di modifiche normative, organizzative o a seguito di incidenti reali.*

---

## 12. Requisiti Settoriali per la Notifica

### 12.1 Energia (Allegato I, Settore 1)

| Sottosettore | Autorità Aggiuntiva | Soglie Specifiche | Riferimento |
|-------------|--------------------|--------------------|-------------|
| Elettricità | ARERA + ENTSO-E | Interruzione > 50 MW o > 50.000 utenti | Reg. UE 2019/943 |
| Gas | ARERA | Interruzione fornitura > 10.000 utenti | D.Lgs. 164/2000 |
| Petrolio | MiSE | Impatto su approvvigionamento nazionale | D.Lgs. 249/2012 |

**Nota settoriale**: Per il settore energia, la notifica NIS2 deve essere coordinata con il reporting ACER ai sensi del Regolamento UE 2019/941 sulla preparazione ai rischi nel settore dell'energia elettrica. Il CISO deve informare il responsabile della sicurezza fisica degli impianti entro 1 ora dalla classificazione come incidente significativo.

### 12.2 Settore Bancario e Finanziario (Allegato I, Settore 4)

| Sottosettore | Autorità Aggiuntiva | Soglie Specifiche | Riferimento |
|-------------|--------------------|--------------------|-------------|
| Enti creditizi | Banca d'Italia + BCE | Interruzione servizi bancari > 2h | DORA Art. 19 |
| Infrastrutture mercato | CONSOB | Impatto su negoziazione/regolamento | Reg. UE 2022/2554 |
| Servizi di pagamento | Banca d'Italia | Transazioni impattate > 10.000 | PSD2 Art. 96 |

**Nota settoriale**: Obbligo di doppia notifica NIS2 + DORA. La notifica DORA all'autorità finanziaria competente segue la timeline NIS2 ma con format specifico. Verificare requisiti aggiuntivi BCE per enti significativi. Tempo massimo per attivazione del team di incident response: 30 minuti.

### 12.3 Sanitario (Allegato I, Settore 5)

| Sottosettore | Autorità Aggiuntiva | Soglie Specifiche | Riferimento |
|-------------|--------------------|--------------------|-------------|
| Prestatori sanitari | ASL + Regione | Impatto su pazienti in cura | D.Lgs. 502/1992 |
| Laboratori | ISS | Compromissione dati referti | Reg. UE 2017/746 |
| Dispositivi medici | Min. Salute | Malfunzionamento device connessi | Reg. UE 2017/745 |

**Nota settoriale**: In ambito sanitario, un incidente che compromette sistemi di supporto vitale o cartelle cliniche elettroniche è automaticamente classificato come significativo indipendentemente dalle soglie generali. Priorità assoluta al patient safety. Notifica aggiuntiva alla Regione competente entro 12 ore.

### 12.4 Infrastrutture Digitali (Allegato I, Settore 8)

| Sottosettore | Autorità Aggiuntiva | Soglie Specifiche | Riferimento |
|-------------|--------------------|--------------------|-------------|
| IXP | AGCOM | Impatto su peering > 100 Gbps | Codice Comunicazioni Elettroniche |
| DNS | AGCOM + ENISA | Impatto risoluzione > 1M query/h | Reg. UE 2022/2555 Art. 28 |
| Cloud computing | ACN | SLA breach > 99.9% per > 4h | Qualificazione ACN |
| Data center | ACN | Indisponibilità > 4h Tier III+ | Qualificazione ACN |

**Nota settoriale**: I fornitori di servizi DNS, registri TLD, servizi cloud, data center e CDN hanno obblighi rafforzati di notifica. La notifica deve includere l'impatto stimato sui clienti downstream. Per i cloud provider: notifica parallela a tutti i clienti NIS2 impattati entro 24 ore.

### 12.5 Gestione Servizi ICT B2B (Allegato I, Settore 10)

| Sottosettore | Autorità Aggiuntiva | Soglie Specifiche | Riferimento |
|-------------|--------------------|--------------------|-------------|
| MSP/MSSP | ACN | Impatto su > 5 clienti NIS2 | Art. 21.2(d) NIS2 |
| System integrator | ACN | Compromissione supply chain | Art. 21.2(d) NIS2 |

**Nota settoriale**: MSP e MSSP hanno obbligo di notifica sia al CSIRT nazionale sia a tutti i clienti potenzialmente impattati. La notifica ai clienti deve avvenire entro 24 ore dalla rilevazione, in parallelo con l'early warning al CSIRT. Documentare la catena di impatto supply chain.

---

## 13. Responsabilità dell'Organo Direttivo (Art. 20 NIS2)

### 13.1 Obblighi dell'Alta Direzione nella Gestione Incidenti

L'Articolo 20 della NIS2, trasposto nell'Art. 23 del D.Lgs. 138/2024, stabilisce che gli organi di gestione delle entità essenziali e importanti sono **personalmente responsabili** dell'approvazione delle misure di gestione del rischio e della supervisione della loro attuazione. In materia di incident reporting, ciò comporta:

| Obbligo | Azione Richiesta | Frequenza | Evidenza |
|---------|------------------|-----------|----------|
| Approvazione procedura | Firma formale procedura di notifica | Annuale e ad ogni revisione | Verbale CdA/delibera |
| Supervisione notifiche | Review di ogni incidente significativo | Per evento | Report al CdA |
| Formazione | Partecipazione a training su incident handling | Minimo annuale, >= 4 ore | Attestato frequenza |
| Esercitazioni | Partecipazione ad almeno 1 tabletop exercise/anno | Annuale | Verbale esercitazione |
| Risorse | Allocazione budget dedicato IR | Annuale | Budget approvato |

### 13.2 Sanzioni per Inadempimento

| Violazione | Sanzione Entità Essenziali | Sanzione Entità Importanti |
|------------|---------------------------|---------------------------|
| Mancata notifica early warning (24h) | Fino a €10.000.000 o 2% fatturato mondiale | Fino a €7.000.000 o 1,4% fatturato mondiale |
| Mancata notifica 72h | Fino a €10.000.000 o 2% fatturato mondiale | Fino a €7.000.000 o 1,4% fatturato mondiale |
| Mancato report finale | Fino a €10.000.000 o 2% fatturato mondiale | Fino a €7.000.000 o 1,4% fatturato mondiale |
| Mancata formazione management | Sanzioni accessorie, sospensione funzioni dirigenziali | Sanzioni accessorie |

**Nota**: Le sanzioni si applicano al valore più elevato tra importo fisso e percentuale di fatturato. L'organo direttivo può essere ritenuto personalmente responsabile in caso di grave negligenza (Art. 20.1 NIS2).

---

## 14. KPI e Metriche di Efficacia

| KPI | Target | Formula | Frequenza Monitoraggio |
|-----|--------|---------|----------------------|
| Tempo medio di rilevazione (MTTD) | <= 24 ore | Media tempo tra inizio incidente e rilevazione | Trimestrale |
| Tempo medio di risposta (MTTR) | <= 4 ore | Media tempo tra rilevazione e primo contenimento | Trimestrale |
| Compliance early warning 24h | 100% | Early warning inviati entro 24h / Totale incidenti significativi | Per evento |
| Compliance notification 72h | 100% | Notification inviate entro 72h / Totale incidenti significativi | Per evento |
| Compliance final report 1 mese | 100% | Report finali entro 1 mese / Totale incidenti significativi | Per evento |
| Completezza notifiche | >= 95% | Campi compilati / Campi totali per notifica | Per evento |
| Esercitazioni completate | >= 2/anno | N. esercitazioni completate nell'anno | Annuale |
| Partecipazione management esercitazioni | 100% | Membri CdA partecipanti / Totale membri CdA | Annuale |
| Incidenti ripetuti (stessa root cause) | 0 | N. incidenti con root cause già identificata in precedenza | Trimestrale |

---

## 15. Documenti Correlati

| Documento | Tipo | Percorso |
|-----------|------|----------|
| NIS2 Business Continuity Plan | Piano | `../continuity/nis2-business-continuity-plan.md` |
| NIS2 Governance & Accountability | Policy | `../governance/nis2-governance-accountability.md` |
| NIS2 Risk Management Measures | Policy | `../risk/nis2-risk-management-measures.md` |
| NIS2 Supply Chain Security | Policy | `../supply-chain/nis2-supply-chain-security.md` |
| NIS2 Compliance Checklist | Checklist | `../compliance/nis2-compliance-checklist.md` |
| NIS2 ISMS Integration Guide | Guida | `../context/nis2-isms-integration-guide.md` |
| PIMS Data Breach Notification | Procedura | `../../pims/procedures/data-breach-notification-procedure.md` |

---

## 16. Checklist di Compilazione

Prima di considerare questo documento completo, verificare che tutti i campi siano stati personalizzati:

| # | Placeholder | Sezione | Descrizione |
|---|-------------|---------|-------------|
| 1 | `{{company_name}}` | 1.1 | Ragione sociale dell'organizzazione |
| 2 | `{{document_date}}` | Frontmatter, 6.2, 11 | Data emissione documento |
| 3 | `{{document_author}}` | 11 | Autore della procedura |
| 4 | `{{dedicated_contact}}` | 6.2 | Contatto dedicato per comunicazione utenti |
| 5 | Tabella Sezione 5.2 | 5.2 | Completare contatti specifici ACN e autorità |
| 6 | Tabella RACI | 5.3 | Inserire nomi specifici per ogni ruolo |
| 7 | Soglie significatività | 3.1 | Confermare o adattare le soglie alla propria organizzazione |
| 8 | Registro Incidenti | 9.1 | Predisporre il registro nel sistema documentale |
| 9 | Sezione 11 | 11 | Completare nomi e firme nella tabella di approvazione |
| 10 | Sezione 12 | 12 | Selezionare il proprio settore e completare i riferimenti settoriali |
