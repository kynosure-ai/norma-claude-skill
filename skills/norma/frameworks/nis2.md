---
framework: nis2
display_name: "NIS2 Directive — Directive (EU) 2022/2555"
canonical_ref: "Directive (EU) 2022/2555"
language: it
---

The NIS2 Directive (EU) 2022/2555 raises the baseline of cybersecurity for essential and important entities across 18 sectors in the EU; this reference covers scope, the 10 mandatory risk-management measures of Article 21, the 24h/72h/30-day incident reporting timeline (Article 23), governance accountability (Article 20) and the Italian implementation context (D.Lgs. 138/2024 + ACN).

## Scope

NIS2 sostituisce la prima Direttiva NIS (2016/1148) ampliando l'ambito a 18 settori critici, suddivisi fra Allegato I (settori ad alta criticità — entità essenziali) e Allegato II (altri settori critici — entità importanti).

### Allegato I — settori essenziali

```
Alta criticità:
├── Energia (elettricità, teleriscaldamento, petrolio, gas, idrogeno)
├── Trasporti (aereo, ferroviario, marittimo, stradale)
├── Bancario (enti creditizi)
├── Infrastrutture mercati finanziari (sedi negoziazione, controparti centrali)
├── Sanità (assistenza sanitaria, laboratori UE, fabbricanti dispositivi medici critici)
├── Acqua potabile
├── Acque reflue
├── Infrastrutture digitali (IXP, DNS, TLD, cloud, data center, CDN, eIDAS, reti)
├── Gestione servizi ICT B2B (MSP, MSSP)
├── Spazio (operatori infrastrutture terrestri)
└── Pubblica amministrazione (centrale)
```

### Allegato II — settori importanti

```
Altri settori critici:
├── Servizi postali
├── Gestione rifiuti
├── Sostanze chimiche (fabbricazione/distribuzione)
├── Alimenti (produzione/trasformazione/distribuzione)
├── Fabbricazione (dispositivi medici, computer/elettronica, apparecchiature elettriche, macchinari, autoveicoli, altri mezzi di trasporto)
├── Fornitori servizi digitali (marketplace online, motori di ricerca, social network)
└── Ricerca (escluse istituzioni educative)
```

### Soglie dimensionali

| Tipo entità | Criteri |
|-------------|---------|
| Essenziale | Settore Allegato I + media o grande impresa |
| Importante | Settore Allegato II + media o grande impresa |
| Micro / piccola | Generalmente esclusa (salvo eccezioni — enti critici, fornitori unici) |

```
Media impresa:   50-249 dipendenti  o  €10-50M fatturato
Grande impresa:  ≥ 250 dipendenti   o  > €50M fatturato
```

## Implementation Timeline (Italia)

| Data | Milestone |
|------|-----------|
| 16 gennaio 2023 | NIS2 in vigore (Direttiva UE) |
| 17 ottobre 2024 | Recepimento nazionale Italia (D.Lgs. 138/2024) |
| 1 dicembre 2024 - 28 febbraio 2025 | Finestra di registrazione presso ACN |
| 17 aprile 2025 | Piena applicabilità delle misure Art. 21 |
| Continuativamente | Notifica incidenti significativi (24h / 72h / 30 gg) |

## Article 20 — Governance Accountability

NIS2 introduce responsabilità diretta dell'**organo di gestione** (management body): approvazione delle misure, supervisione dell'implementazione, formazione cyber per i dirigenti, possibile responsabilità personale. È il salto qualitativo più rilevante rispetto a NIS1.

## Article 21 — 10 Mandatory Risk-Management Measures

```
Art. 21(2) Misure di gestione del rischio:

(a) Politiche di analisi dei rischi e sicurezza dei sistemi informativi
    ├── Risk assessment methodology
    ├── Information security policy
    └── Gestione rischi supply chain

(b) Gestione degli incidenti
    ├── Procedura rilevamento
    ├── Procedura risposta
    ├── Procedura notifica
    └── Lessons learned

(c) Continuità operativa e gestione delle crisi
    ├── Business continuity plan
    ├── Disaster recovery plan
    ├── Backup management
    └── Crisis management

(d) Sicurezza della catena di approvvigionamento
    ├── Valutazione fornitori
    ├── Requisiti contrattuali
    ├── Monitoraggio continuo
    └── Sub-fornitori

(e) Sicurezza nell'acquisizione, sviluppo e manutenzione di sistemi
    ├── Secure SDLC
    ├── Vulnerability management
    ├── Patch management
    └── Security testing

(f) Politiche e procedure per valutare l'efficacia
    ├── Audit interni
    ├── Penetration testing
    ├── Vulnerability assessment
    └── Metriche di sicurezza

(g) Pratiche di igiene informatica di base e formazione
    ├── Security awareness
    ├── Training periodico
    ├── Phishing simulation
    └── Acceptable use policy

(h) Politiche e procedure di crittografia
    ├── Encryption policy
    ├── Key management
    ├── Crittografia at-rest
    └── Crittografia in-transit

(i) Sicurezza delle risorse umane e controllo accessi
    ├── Access control policy
    ├── Identity management (IAM)
    ├── Privileged access management (PAM)
    └── HR security (screening, cessazione)

(j) Autenticazione multi-fattore o continua
    ├── MFA policy
    ├── SSO sicuro
    ├── Comunicazioni sicure
    └── Sistemi di emergenza
```

## Article 23 — Incident Reporting Timeline

```
T+0     Incidente significativo rilevato

T+24h   Preallarme (early warning)
        ├── Sospetto attacco?
        ├── Impatto transfrontaliero?
        └── Informazioni preliminari

T+72h   Notifica incidente
        ├── Aggiornamento del preallarme
        ├── Valutazione iniziale
        ├── Gravità e impatto
        ├── IoC (se disponibili)
        └── Misure adottate

T+30gg  Relazione finale
        ├── Descrizione dettagliata
        ├── Causa probabile / root cause
        ├── Misure di attenuazione
        ├── Impatto transfrontaliero
        └── Lessons learned

Su richiesta: relazione intermedia con aggiornamenti situazione
```

### Criteri per incidente significativo

| Criterio | Soglia |
|----------|--------|
| Grave perturbazione operativa | Servizio essenziale interrotto |
| Perdite finanziarie | Significative per l'entità |
| Danni a persone (fisiche o giuridiche) | Materiali o non materiali considerevoli |
| Impatto transfrontaliero | Effetti in altri Stati membri |

## Documentary Requirements

### Tier 1 — documenti core

| ID | Documento | Misura Art. 21 | Priorità |
|----|-----------|----------------|----------|
| D01 | NIS2 Scope & Applicability | — | Critica |
| D02 | Risk Management Policy | (a) | Critica |
| D03 | Information Security Policy | (a) | Critica |
| D04 | Incident Response Procedure | (b) | Critica |
| D05 | Business Continuity Plan | (c) | Critica |
| D06 | Supply Chain Security Policy | (d) | Critica |

### Tier 2 — procedure e controlli

| ID | Documento | Misura Art. 21 | Priorità |
|----|-----------|----------------|----------|
| P01 | Vulnerability Management Procedure | (e) | Alta |
| P02 | Security Testing Programme | (f) | Alta |
| P03 | Security Awareness Programme | (g) | Alta |
| P04 | Encryption Policy | (h) | Alta |
| P05 | Access Control Policy | (i) | Alta |
| P06 | MFA Implementation Guide | (j) | Alta |
| P07 | Backup & Recovery Procedure | (c) | Alta |

### Tier 3 — registri e template

| ID | Documento | Riferimento | Priorità |
|----|-----------|-------------|----------|
| R01 | Risk Register | Art. 21(a) | Alta |
| R02 | Incident Log | Art. 23 | Alta |
| R03 | Supplier Register | Art. 21(d) | Media |
| T01 | Incident Notification Template | Art. 23 | Alta |
| T02 | Authority Registration Form | Recepimento nazionale | Critica |

## Mapping NIS2 ↔ ISO/IEC 27001:2022

| NIS2 Art. 21 | Misura | ISO 27001 (clausola/controllo) | Note |
|--------------|--------|--------------------------------|------|
| (a) | Risk analysis | 6.1.2, A.5.1 | Risk-based |
| (b) | Incident handling | A.5.24-28 | Notifica 24h |
| (c) | Business continuity | A.5.29-30 | Crisis management |
| (d) | Supply chain | A.5.19-23 | Esteso ai sub-fornitori |
| (e) | Acquisition security | A.8.25-31 | Vulnerability management |
| (f) | Effectiveness | 9.1, 9.2 | Testing programme |
| (g) | Cyber hygiene | A.6.3 | Basic practices |
| (h) | Cryptography | A.8.24 | Policy required |
| (i) | HR & access | A.5.15-18, A.6.x | IAM focus |
| (j) | MFA | A.8.5 | Mandatory MFA |

Un'organizzazione che gestisce un ISMS 27001 maturo copre la maggior parte dei requisiti Art. 21 a livello di controllo; i delta tipici riguardano: timeline incidenti più stretta (24h vs nessun obbligo specifico), governance dell'organo di gestione (Art. 20 NIS2 più prescrittivo), supply chain sub-fornitori, MFA obbligatoria.

## Sanctions

Le sanzioni NIS2 sono esecutive a livello UE e implementate dagli Stati membri.

### Entità essenziali
- Fino a **€10.000.000** o **2% del fatturato mondiale** annuo (il maggiore dei due)
- Sanzioni accessorie: sospensione, divieto di esercizio per i dirigenti

### Entità importanti
- Fino a **€7.000.000** o **1.4% del fatturato mondiale** annuo (il maggiore dei due)

### Fattori aggravanti
- Recidiva
- Mancata notifica di incidenti
- Mancata cooperazione con l'autorità competente
- Danno significativo a terzi

## National Implementation Notes (Italia)

In Italia il recepimento è il D.Lgs. 138/2024. L'autorità competente è **ACN** (Agenzia per la Cybersicurezza Nazionale). Le entità soggette devono:

- Registrarsi sul portale ACN entro il 28 febbraio 2025
- Designare un referente NIS2 (responsabilità formalizzata)
- Predisporre la documentazione richiesta dall'Art. 21
- Notificare gli incidenti significativi via piattaforma dedicata ACN
- Comunicare i dati di inventario e i servizi essenziali/importanti

Dati richiesti per la registrazione: ragione sociale e P.IVA, settore e sottosettore NIS2, categoria (essenziale/importante), dati di contatto (referente NIS2, PEC, telefono), elenco servizi essenziali/importanti, Stati membri in cui l'entità opera, range IP (se applicabile), data ultima valutazione rischi.

Implementazioni nazionali analoghe in altri Stati membri (BSI in Germania, ANSSI in Francia, NCSC nei Paesi Bassi, ecc.). Le timelines e i dettagli di registrazione variano per Stato membro.

## Implementation Notes

- L'organo di gestione (Art. 20) è il vero perno di NIS2: senza un commitment formalizzato e senza la formazione cyber dei dirigenti, le misure di Art. 21 rimangono carte non operative. Il primo audit ACN tipico include verifiche sulla governance prima ancora che sui controlli tecnici.
- La supply chain (Art. 21.d) è uno dei punti più sottovalutati. NIS2 richiede non solo di valutare i fornitori diretti ma di considerare le vulnerabilità lungo la catena (sub-fornitori inclusi). Per le PMI in scope è spesso il gap più costoso da chiudere.
- La timeline di notifica è stringente. Il preallarme entro 24 ore richiede un processo di intake operativo h24 — procedure cartacee non bastano, servono runbook concreti, contact list testate, accesso al portale ACN in tempo reale.
- L'integrazione con un ISMS ISO 27001 esistente accorcia drasticamente il path: la maggior parte delle 10 misure ha mapping diretto su Annex A. La documentazione 27001 può essere riusata, integrata da delta NIS2-specifici (governance Art. 20, timeline Art. 23, registrazione presso autorità).

## References

- Direttiva (UE) 2022/2555 (NIS2)
- D.Lgs. 138/2024 — Recepimento Italia
- Linee guida ACN
- ENISA — NIS2 Implementation Guidance
- ENISA — Mapping NIS2-ISO/IEC 27001
- Atti di esecuzione e atti delegati della Commissione UE pertinenti
