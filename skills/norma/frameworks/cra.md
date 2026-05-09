---
framework: cra
display_name: "Cyber Resilience Act — Regulation (EU) 2024/2847"
canonical_ref: "Regulation (EU) 2024/2847"
language: it
---

The EU Cyber Resilience Act (Regulation 2024/2847) imposes cybersecurity requirements on products with digital elements placed on the EU market; this reference covers product classification (Default / Important Class I-II / Critical), the Annex I essential cybersecurity requirements (15 product properties + 8 vulnerability handling), conformity assessment modules (A / B+C / H), the 24h/72h/14-day vulnerability reporting flow, SBOM requirements, and CE marking obligations.

## Architecture

Il CRA è un Regolamento UE direttamente applicabile, in vigore dal 10 dicembre 2024 con piena applicazione dall'**11 dicembre 2027**. Si applica a manufacturer, importatori e distributori di prodotti con elementi digitali (hardware, software, combinazioni).

```
REGOLAMENTO (UE) 2024/2847 - CYBER RESILIENCE ACT

CHAPTER I:    GENERAL PROVISIONS (Art. 1-4)
CHAPTER II:   OBLIGATIONS OF ECONOMIC OPERATORS (Art. 5-22)
              ├── Art. 5   Placing on the market
              ├── Art. 6   General obligations of manufacturers
              ├── Art. 7   Reporting obligations (vulnerabilities/incidents)
              ├── Art. 8   SBOM obligations
              ├── Art. 9   Authorised representatives
              ├── Art. 10  Importers
              ├── Art. 11  Distributors
              └── Art. 12-22 Altre obbligazioni
CHAPTER III:  CONFORMITY OF PRODUCTS (Art. 23-36)
              ├── Art. 23  Presumption of conformity
              ├── Art. 25  EU declaration of conformity
              ├── Art. 26-27 CE marking
              ├── Art. 28  Technical documentation
              └── Art. 29-33 Conformity assessment (Default / Important / Critical)
CHAPTER IV:   NOTIFICATION OF CONFORMITY ASSESSMENT BODIES (Art. 37-51)
CHAPTER V:    MARKET SURVEILLANCE AND ENFORCEMENT (Art. 52-58)
CHAPTER VI:   DELEGATED AND IMPLEMENTING ACTS (Art. 59-61)
CHAPTER VII:  CONFIDENTIALITY AND PENALTIES (Art. 62-64)
CHAPTER VIII: TRANSITIONAL AND FINAL PROVISIONS (Art. 65-71)

ANNEXES:
├── ANNEX I    Essential Cybersecurity Requirements (Part I + Part II)
├── ANNEX II   Information and Instructions to Users
├── ANNEX III  Important Products (Class I & II)
├── ANNEX IV   Critical Products
├── ANNEX V    EU Declaration of Conformity (template)
├── ANNEX VI   Simplified Declaration
├── ANNEX VII  Technical Documentation
└── ANNEX VIII Conformity Assessment Procedures (Modules A / B / C / H)
```

## Product Classification

L'albero decisionale CRA è il primo step: senza una classificazione corretta, le obbligazioni e il modulo di conformity assessment sono indeterminati.

```
                    PRODOTTO CON ELEMENTI DIGITALI?
                    (Connettività diretta o indiretta a un altro device o network)
                              │
                              ▼
                    Esclusioni Art. 2.2-2.5
                    (es. dispositivi medici già in MDR, automotive in UNECE,
                     prodotti coperti da regolamenti settoriali specifici)
                              │
        NO ◄──────────────────┴──────────────────► SI
        │                                          │
   Fuori scope                                     ▼
                              È in Annex III (Important) o Annex IV (Critical)?
                                            │
              ┌─────────────────────────────┼─────────────────────────────┐
              │                             │                             │
              ▼                             ▼                             ▼
    DEFAULT (~90% prodotti)        IMPORTANT (Annex III)         CRITICAL (Annex IV)
    Self-assessment                Class I o Class II            Mandatory third-party
    Module A                                                     + EUCC certification
```

### Annex III — Important Products

#### Class I (third-party richiesto se non si applicano harmonised standards)

| Categoria | Esempi |
|-----------|--------|
| Identity management systems | Authentication, access control, biometric readers |
| Password managers | Consumer ed enterprise |
| Browsers | Standalone ed embedded |
| VPN products | Consumer ed enterprise VPN |
| Network management systems | Tool di configurazione, SIEM |
| Routers / modem / switch | Connessi a Internet (non Class II) |
| Operating systems | Consumer OS (non Class II) |
| Firewall / IDS / IPS | Non-industrial |
| Microprocessori / MCU | Con funzionalità di sicurezza |
| Smart home security | Door locks, cameras, alarms, baby monitors |
| Wearables | Health monitoring |
| Smart toys | Con funzionalità social/location |

#### Class II (sempre third-party)

| Categoria | Esempi |
|-----------|--------|
| Hypervisor | Container runtime, virtualizzazione |
| Industrial firewalls | ICS/SCADA IDS/IPS |
| Tamper-resistant MPU | Hardware security modules |
| Tamper-resistant MCU | Secure elements |

### Annex IV — Critical Products

| Categoria | Requisiti |
|-----------|-----------|
| Hardware security boxes | Third-party + EUCC |
| Smart meter gateway | Third-party + EUCC |
| Smartcards | Third-party + EUCC |
| Secure elements | Third-party + EUCC |

## Annex I — Essential Cybersecurity Requirements

### Part I — Product Properties (15 requisiti)

| ID | Requisito | Descrizione |
|----|-----------|-------------|
| I.1 | Secure by design | Livello appropriato di sicurezza basato su risk assessment |
| I.2 | No known vulnerabilities | Nessuna vulnerabilità nota sfruttabile al rilascio |
| I.3 | Secure by default | Configurazione sicura di default; possibilità di reset |
| I.4 | Protezione da accesso non autorizzato | Autenticazione, IAM, access control |
| I.5 | Protezione confidentiality | Crittografia at-rest e in-transit (state-of-the-art) |
| I.6 | Data integrity | Protezione da manipolazione, segnalazione di corruzioni |
| I.7 | Data minimization | Solo dati necessari per scopo previsto |
| I.8 | Availability protection | Resilienza a DoS, mitigazione impatti |
| I.9 | Minimize negative impact | Non impattare disponibilità di altri device/reti |
| I.10 | Attack surface limitation | Ridurre interfacce esterne, design sicuro |
| I.11 | Incident impact reduction | Meccanismi di mitigation in caso di exploitation |
| I.12 | Monitoring / Logging | Logging delle attività interne con opt-out |
| I.13 | Data removal | Capacità di rimozione sicura dei dati utente |
| I.14 | Data portability | Trasferimento sicuro ad altri sistemi |
| I.15 | Security updates | Meccanismo di update sicuro, notifiche utenti |

### Part II — Vulnerability Handling (8 requisiti)

| ID | Requisito | Descrizione |
|----|-----------|-------------|
| II.1 | Identify / document vulnerabilities | Inclusione di SBOM machine-readable |
| II.2 | Address vulnerabilities | Remediation senza ritardi |
| II.3 | Security testing | Test regolari ed efficaci |
| II.4 | Disclose fixed vulnerabilities | Pubblicazione delle informazioni dopo il fix |
| II.5 | CVD policy | Coordinated Vulnerability Disclosure |
| II.6 | Reporting contact | Canale per segnalazioni |
| II.7 | Update distribution | Distribuzione sicura delle patch |
| II.8 | Free security updates | Gratuiti durante il support period |

## Conformity Assessment Modules

```
Module A — Internal Control (self-assessment)
└── Default products + Important Class I quando si applicano harmonised standards
    1. Prepare technical documentation (Annex VII)
    2. Conduct internal assessment (verify design conformity, test security controls,
       validate vulnerability handling)
    3. Finalize conformity (EU Declaration, CE marking, mantenere documentazione 10
       anni o per support period)

Module B + C — EU-Type Examination + Conformity to Type
└── Important Class I (no h.std), Class II, Critical
    Module B: notified body esamina design + tech docs + emette certificato EU-Type
    Module C: manufacturer mantiene QMS production con ongoing surveillance
              da parte del notified body

Module H — Full Quality Assurance
└── Alternativa a B+C
    QMS comprehensive che copre design, sviluppo, produzione, vulnerability handling,
    post-market monitoring (analogo a ISO 9001 + cybersecurity)
    Notified body: full QMS assessment + design examination + production audit +
                   ongoing surveillance
    Vantaggi: copre intero portfolio prodotti, integra con ISO 9001
    Svantaggi: più complesso, costi maggiori
```

## Mandatory Documentation

### Tier 1 — Technical Documentation (Annex VII)

| ID | Documento | Articolo | Contenuto |
|----|-----------|----------|-----------|
| D01 | Product Description | Art. 28 | Purpose, versions, connectivity, dependencies |
| D02 | System Architecture | Art. 28 | Component integration, data flows |
| D03 | Cybersecurity Risk Assessment | Art. 28 | Threats, vulnerabilities, risks, treatments |
| D04 | SBOM | Art. 8 | Machine-readable; top-level dependencies minimo |
| D05 | Annex I Mapping | Art. 28 | Come ogni requisito è soddisfatto |
| D06 | Test Reports | Art. 28 | Penetration test, code analysis, vulnerability assessment |
| D07 | Support Period | Art. 28 | Durata, giustificazione |

### Tier 2 — Conformity Documentation

| ID | Documento | Articolo |
|----|-----------|----------|
| D08 | EU Declaration of Conformity | Art. 25, Annex V |
| D09 | Module Selection Justification | Art. 29-33 |
| D10 | Harmonized Standards Reference | Art. 23 |
| D11 | Notified Body Certificate | Art. 32-33 (se applicabile) |

### Tier 3 — Vulnerability Management

| ID | Documento | Articolo |
|----|-----------|----------|
| D12 | Vulnerability Handling Process | Art. 7, Annex I |
| D13 | CVD Policy | Annex I.II.5 |
| D14 | Incident Response Plan | Art. 7 |
| D15 | Vulnerability Register | Art. 7 |
| D16 | Security Update Policy | Annex I.II.7-8 |

### Tier 4 — Reporting Templates

| ID | Documento | Articolo | Timeline |
|----|-----------|----------|----------|
| D17 | Early Warning Notification | Art. 14 | Entro 24h |
| D18 | Vulnerability Notification | Art. 14 | Entro 72h |
| D19 | Final Vulnerability Report | Art. 14 | Entro 14 giorni dal fix |
| D20 | Incident Final Report | Art. 14 | Entro 1 mese |

## Vulnerability Reporting Flow (Art. 14)

```
ACTIVELY EXPLOITED VULNERABILITY DISCOVERED

T+0       Discovery / awareness

T+24h     EARLY WARNING NOTIFICATION
          To: CSIRT + ENISA
          ├── Product identification
          ├── Suspected malicious act? (Y/N)
          └── EU countries where available

T+72h     DETAILED VULNERABILITY NOTIFICATION
          To: CSIRT + ENISA
          ├── General product info
          ├── Nature of exploit/vulnerability
          ├── Corrective/mitigating measures taken
          └── Measures users can implement

T+14gg    FINAL VULNERABILITY REPORT (dopo che il fix è disponibile)
          ├── Vulnerability description
          ├── Severity and impact analysis
          ├── Malicious actors info (se nota)
          └── Detailed mitigation information

SEVERE SECURITY INCIDENT (track separato)
T+24h     Early warning
T+72h     Detailed notification
T+1mese   Final report (incident description, severity, root cause)

Platform: ENISA Single Reporting Platform
```

## Implementation Timeline

```
10 DEC 2024  Entry into force
              │
              │  Iniziare subito:
              │  • Product categorization
              │  • Gap analysis vs Annex I
              │  • SBOM implementation
              │  • Vulnerability handling process
              ▼
11 JUN 2026  Notified Bodies operational
              │  Stati membri designano notifying authorities
              ▼
11 SEP 2026  Vulnerability Reporting MANDATORY
              │  • 24h early warning (actively exploited vuln)
              │  • 72h detailed notification
              │  • 14 days final report (post-fix)
              │  • 1 month final report (severe incidents)
              │  Anche per prodotti già sul mercato
              ▼
11 DEC 2027  FULL COMPLIANCE REQUIRED
              │  Per nuovi prodotti immessi sul mercato:
              │  • Full Annex I compliance
              │  • Technical documentation completa
              │  • Conformity assessment completato
              │  • CE marking apposto
              │  • EU Declaration of Conformity
              │  Prodotti esistenti: grandfathered ma reporting attivo
```

## Support Period

| Fattore | Considerazione |
|---------|----------------|
| Minimum | 5 anni (o expected use time se inferiore) |
| Expected lifetime | Quanto durerà il prodotto in uso? |
| User expectations | Cosa si aspettano ragionevolmente gli utenti? |
| Product nature | IoT consumer vs industrial equipment |
| Competitor practices | Cosa offrono i competitor? |

Obblighi durante il support period: monitoraggio vulnerabilità (incluse componenti terze), security updates gratuiti, manutenzione SBOM aggiornata, incident response attivo, comunicazione di end-of-support (dove tecnicamente possibile).

## SBOM Requirements

| Elemento | Requisito |
|----------|-----------|
| Formato | Machine-readable (SPDX 2.3+, CycloneDX 1.4+) |
| Scope minimo | Top-level dependencies |
| Raccomandato | Transitive dependencies |
| Update | Continuo durante support period |
| Disponibilità | Market surveillance su richiesta |

Campi consigliati (BSI TR-03183-2): component name (required), version (required), supplier (required), relationship (required, depends on / contains), license (recommended), hash (recommended), vulnerabilities con CVE link (recommended), purl (recommended).

## Cross-Framework Mapping

### CRA → ISO/IEC 27001:2022

| CRA Requirement | ISO 27001 Control |
|-----------------|-------------------|
| Secure by design | A.8.25-28 (secure development lifecycle) |
| Access control | A.5.15-18, A.8.2-5 |
| Encryption | A.8.24 |
| Logging / monitoring | A.8.15-16 |
| Vulnerability handling | A.8.8 |
| Incident response | A.5.24-27 |
| SBOM / supply chain | A.5.19-23 |
| Security testing | A.8.29 |
| Change management | A.8.32 |

### CRA → IEC 62443 (Industrial)

| CRA Requirement | IEC 62443 Reference |
|-----------------|---------------------|
| Risk assessment | IEC 62443-3-2 |
| Secure development | IEC 62443-4-1 |
| Product security | IEC 62443-4-2 |
| System security | IEC 62443-3-3 |

### CRA → ETSI EN 303 645 (Consumer IoT)

| CRA Requirement | ETSI Provision |
|-----------------|----------------|
| No default passwords | Provision 5.1 |
| Vulnerability disclosure | Provision 5.2 |
| Software updates | Provision 5.3 |
| Secure storage | Provision 5.4 |
| Secure communication | Provision 5.5 |

### CRA ↔ NIS2

| Aspetto | CRA | NIS2 |
|---------|-----|------|
| Focus | Prodotti | Entità (essential / important) |
| Applicabilità | Manufacturers | Operators |
| Incident reporting | A ENISA / CSIRT | A CSIRT nazionale |
| Timeline | 24h / 72h / 14gg | 24h / 72h / 30gg |

CRA e NIS2 sono complementari: prodotti sicuri (CRA) usati da entità in scope NIS2, con catene di fornitura e incidenti che fluiscono da entrambe le cornici.

## Penalties (Art. 64)

| Violazione | Sanzione massima |
|------------|------------------|
| Non conformità ai requisiti essenziali | €15M o 2.5% turnover |
| Violazioni di documentazione / conformity | €10M o 2% turnover |
| Informazioni errate alle autorità | €5M o 1% turnover |

Esenzioni: microimprese e PMI hanno esenzione dalla deadline 24h reporting; gli open-source software stewards hanno esenzione generale dalle penalty (definizione e perimetro precisati negli atti delegati).

## Implementation Notes

- La product categorization è il gate decisionale: senza una mappatura chiara fra il prodotto e Annex III/IV (e le esclusioni di Art. 2), tutta la pianificazione downstream è speculativa.
- L'SBOM machine-readable è il cambio operativo più impattante per molti manufacturer: integrarlo nella pipeline di build (SPDX o CycloneDX) e mantenerlo vivo durante il support period richiede processi di software composition analysis e vulnerability monitoring già in atto.
- Il vulnerability handling process (Annex I Part II) richiede un canale di reporting pubblico, una CVD policy formalizzata, e un'organizzazione capace di processare segnalazioni esterne in modo strutturato. Per molte PMI è una capability nuova.
- Il support period va dichiarato e giustificato: troppo breve espone a contestazioni di consumer protection; troppo lungo crea costi di mantenimento elevati. La pratica emergente suggerisce 5-7 anni come baseline per consumer IoT, più lunghi per industrial equipment.
- Per organizzazioni che già operano un ISMS ISO 27001 e un secure-development lifecycle (es. ISO/IEC 27034), il path CRA è più breve: gran parte dei requisiti Annex I Part I trova mapping diretto, e il delta è soprattutto nella formalizzazione di SBOM, technical documentation Annex VII e conformity assessment.

## References

- Regolamento (UE) 2024/2847 — Cyber Resilience Act
- BSI TR-03183-2 — SBOM Requirements
- ETSI EN 303 645 — Consumer IoT cybersecurity
- IEC 62443 — Industrial cybersecurity
- ISO/IEC 27001:2022 + ISO/IEC 27034 — Application security
- ENISA — CRA Implementation Guidance
- JRC / ENISA — CRA Requirements Standards Mapping
