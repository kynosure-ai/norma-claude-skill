---
title: IT Disaster Recovery Plan
version: '2.0'
date: '{{document_date}}'
classification: Riservato
owner: '{{it_manager}}'
approver: '{{senior_management}}'
framework: ISO22301
iso_clauses:
  - Clausola 8.4.4 - Piani di continuità operativa
  - Clausola 8.4.5 - Recupero
cross_references:
  - NIS2 Art. 21(2)(c) - Continuità operativa e gestione delle crisi
  - DORA Art. 11 - Risposta e ripristino
  - DORA Art. 12 - Politiche e procedure di backup
  - DORA Art. 25 - Test dei piani di continuità operativa
  - ISO 27001 A.5.29 - Sicurezza informazioni durante interruzioni
  - ISO 27001 A.5.30 - Prontezza ICT per continuità operativa
  - ISO 27001 A.8.13 - Backup delle informazioni
  - ISO 27001 A.8.14 - Ridondanza delle strutture
status: Da compilare
subset: true
---

# IT Disaster Recovery Plan

## 1. Informazioni Documento

| Campo | Valore |
|-------|--------|
| Codice Documento | {{company_name}}-DRP-001 |
| Versione | 2.0 |
| Data Emissione | {{document_date}} |
| Prossima Revisione | [DATA + 6 mesi] |
| Classificazione | **RISERVATO** |
| Proprietario | [IT Manager] |
| Approvato da | [Direzione Generale] |
| Ultimo Test DR | [Data ultimo test] |

### 1.1 Distribuzione

| # | Ruolo | Nome | Data Consegna |
|---|-------|------|---------------|
| 1 | IT Manager | [Nome] | [Data] |
| 2 | BC Manager | [Nome] | [Data] |
| 3 | CISO | [Nome] | [Data] |
| 4 | Resp. Infrastruttura | [Nome] | [Data] |
| 5 | DBA Lead | [Nome] | [Data] |
| 6 | Network Admin | [Nome] | [Data] |

---

## 2. Introduzione

### 2.1 Scopo

Il presente IT Disaster Recovery Plan definisce le procedure operative e le risorse necessarie per ripristinare i sistemi informativi critici di {{company_name}} a seguito di disastri o interruzioni significative che ne compromettano la disponibilità. In un'era di crescente dipendenza dalla tecnologia, la capacità di ripristinare rapidamente i servizi IT determina la capacità dell'organizzazione di sopravvivere a eventi avversi.

Il piano assicura il ripristino dei sistemi entro i Recovery Time Objectives definiti dalla Business Impact Analysis, riconoscendo che il tempo è il fattore critico nelle situazioni di emergenza e che ogni ora di ritardo genera impatti crescenti sul business. Parallelamente, il piano garantisce che la perdita di dati sia contenuta entro i Recovery Point Objectives definiti, preservando l'integrità delle informazioni aziendali e dei dati dei clienti attraverso strategie di backup e replica adeguate.

L'obiettivo ultimo è garantire la continuità dei processi di business critici, fornendo loro l'infrastruttura tecnologica necessaria per operare, anche se in modalità degradata, durante e dopo un evento di interruzione. Il piano risponde ai requisiti normativi del Regolamento DORA in materia di risposta e ripristino (Art. 11), politiche di backup (Art. 12) e test dei piani di continuità (Art. 25), nonché alle disposizioni della Direttiva NIS2 sulla continuità operativa e alla norma ISO 27001 sulla prontezza ICT per la continuità operativa.

### 2.2 Ambito di Applicazione

| Elemento | Copertura |
|----------|-----------|
| **Data Center Primario** | [Ubicazione] |
| **DR Site** | [Ubicazione] |
| **Cloud Infrastructure** | [Provider - AWS/Azure/GCP] |
| **Sistemi On-Premise** | [Elenco] |
| **Network** | WAN, LAN, Internet |
| **Applicazioni Business-Critical** | [Da inventario Tier 1-2] |

### 2.3 Obiettivi DR

| Metrica | Target | DORA Requirement |
|---------|--------|------------------|
| RTO Globale (Tier 1) | < [4] ore | Art. 11 |
| RPO Globale (Tier 1) | < [1] ora | Art. 12 |
| Disponibilità annua | [99.5]% | Art. 11 |
| Tempo massimo test DR | [8] ore | Art. 25 |
| Frequenza test DR | Semestrale | Art. 25 |

### 2.4 Relazione con Altri Documenti

```
┌─────────────────────────────────────────┐
│     Business Continuity Policy          │
└─────────────────┬───────────────────────┘
                  │
┌─────────────────▼───────────────────────┐
│     Business Continuity Plan            │
└─────────────────┬───────────────────────┘
                  │
┌─────────────────▼───────────────────────┐
│     IT Disaster Recovery Plan           │ ◄── QUESTO DOCUMENTO
└─────────────────┬───────────────────────┘
                  │
        ┌─────────┴─────────┐
        ▼                   ▼
┌───────────────┐    ┌─────────────────┐
│   Runbook     │    │   Procedure     │
│   Applicativi │    │   Operative     │
└───────────────┘    └─────────────────┘
```

---

## 3. Governance DR

### 3.1 Ruoli e Responsabilità

#### DR Manager

| Campo | Valore |
|-------|--------|
| Nome | [Nome Cognome] |
| Cellulare | [Numero] |
| Email | [Email] |
| Backup | [Nome Cognome Backup] |

**Responsabilità**:
- Attivazione e coordinamento del DRP
- Decisione su dichiarazione di disastro IT
- Comunicazione con BC Manager e management
- Supervisione ripristino sistemi
- Autorizzazione failover/failback

#### Team DR

| Ruolo | Nome | Cellulare | Email | Backup |
|-------|------|-----------|-------|--------|
| DR Manager | [Nome] | [Tel] | [Email] | [Nome] |
| Resp. Infrastruttura | [Nome] | [Tel] | [Email] | [Nome] |
| Resp. Network | [Nome] | [Tel] | [Email] | [Nome] |
| DBA Lead | [Nome] | [Tel] | [Email] | [Nome] |
| Resp. Applicazioni | [Nome] | [Tel] | [Email] | [Nome] |
| Security Lead | [Nome] | [Tel] | [Email] | [Nome] |
| Resp. Storage | [Nome] | [Tel] | [Email] | [Nome] |
| Help Desk Lead | [Nome] | [Tel] | [Email] | [Nome] |

### 3.2 Matrice RACI

| Attività | DR Mgr | Infra | Network | DBA | App | Security |
|----------|--------|-------|---------|-----|-----|----------|
| Dichiarazione disastro | A/R | C | C | C | C | C |
| Attivazione DR site | A | R | R | I | I | C |
| Failover network | A | C | R | I | I | C |
| Recovery database | A | C | I | R | C | I |
| Recovery applicazioni | A | C | I | C | R | I |
| Validazione sicurezza | A | I | C | I | I | R |
| Comunicazione utenti | A/R | I | I | I | I | I |
| Dichiarazione normalità | A/R | C | C | C | C | C |

*R=Responsible, A=Accountable, C=Consulted, I=Informed*

### 3.3 Escalation Path

```
LIVELLO 1: Incident (< 1 ora impatto)
    │
    ▼ Se non risolto
LIVELLO 2: Major Incident (1-4 ore impatto)
    │
    ▼ Se non risolto
LIVELLO 3: Disaster Declaration
    │
    ▼
ATTIVAZIONE DRP COMPLETA
```

### 3.4 Criteri Dichiarazione Disastro IT

Un **disastro IT** viene dichiarato quando si verifica **UNO** dei seguenti:

| Criterio | Soglia |
|----------|--------|
| Data center primario inaccessibile | > 4 ore |
| Perdita connettività Internet | > 4 ore |
| Compromissione security critica | Ransomware esteso, breach dati |
| Perdita sistemi Tier 1 | > RTO definito |
| Corruzione dati estesa | > 10% database critici |
| Perdita alimentazione DC | > 4 ore (oltre UPS/generatore) |
| Failure storage primario | Non recuperabile localmente |

---

## 4. Inventario Sistemi e Classificazione

### 4.1 Classificazione Tier

| Tier | Descrizione | RTO | RPO | Strategia DR |
|------|-------------|-----|-----|--------------|
| **Tier 1** | Mission Critical | < 1 ora | < 15 min | Hot standby / Active-Active |
| **Tier 2** | Business Critical | < 4 ore | < 1 ora | Warm standby |
| **Tier 3** | Business Important | < 24 ore | < 4 ore | Cold standby / Backup |
| **Tier 4** | Non Critical | < 72 ore | < 24 ore | Backup only |

### 4.2 Inventario Sistemi per Tier

#### Tier 1 - Mission Critical

| ID | Sistema | Descrizione | RTO | RPO | Strategia DR |
|----|---------|-------------|-----|-----|--------------|
| SYS-001 | [ERP] | Sistema gestionale | 1h | 15min | Active-Passive HA |
| SYS-002 | [Database Core] | Oracle/SQL Server | 1h | 15min | Replica sincrona |
| SYS-003 | [E-commerce/Servizio Core] | Piattaforma vendite | 1h | 15min | Multi-region |
| SYS-004 | [Active Directory] | Identity management | 30min | 15min | Multi-DC replica |
| SYS-005 | [DNS/DHCP] | Network services | 30min | N/A | Multi-site |

#### Tier 2 - Business Critical

| ID | Sistema | Descrizione | RTO | RPO | Strategia DR |
|----|---------|-------------|-----|-----|--------------|
| SYS-101 | [Email] | Microsoft 365/Exchange | 4h | 1h | Cloud native |
| SYS-102 | [CRM] | Customer relationship | 4h | 1h | Cloud native |
| SYS-103 | [HR System] | Gestione HR | 4h | 1h | Warm standby |
| SYS-104 | [VPN/Remote Access] | Accesso remoto | 2h | N/A | Failover config |

#### Tier 3 - Business Important

| ID | Sistema | Descrizione | RTO | RPO | Strategia DR |
|----|---------|-------------|-----|-----|--------------|
| SYS-201 | [File Server] | Storage documenti | 24h | 4h | Backup/Restore |
| SYS-202 | [Intranet] | Portale interno | 24h | 4h | Cold standby |
| SYS-203 | [Wiki/Documentazione] | Knowledge base | 24h | 8h | Cloud backup |

### 4.3 Mappa Dipendenze

```
┌─────────────────────────────────────────────────────────────────┐
│                      LIVELLO APPLICAZIONI                        │
├────────────────┬────────────────┬────────────────┬──────────────┤
│      ERP       │   E-commerce   │      CRM       │    Email     │
└───────┬────────┴───────┬────────┴───────┬────────┴──────┬───────┘
        │                │                │               │
┌───────▼────────────────▼────────────────▼───────────────▼───────┐
│                      LIVELLO DATABASE                            │
├─────────────────────────────────────────────────────────────────┤
│   Oracle DB    │   SQL Server   │  PostgreSQL   │   MongoDB     │
└───────┬────────────────┬────────────────┬───────────────┬───────┘
        │                │                │               │
┌───────▼────────────────▼────────────────▼───────────────▼───────┐
│                   LIVELLO INFRASTRUTTURA                         │
├─────────────────────────────────────────────────────────────────┤
│  VMware/Hyper-V  │  Storage SAN  │   Network   │   Security    │
└───────┬────────────────┬────────────────┬───────────────┬───────┘
        │                │                │               │
┌───────▼────────────────▼────────────────▼───────────────▼───────┐
│                      LIVELLO SERVIZI BASE                        │
├─────────────────────────────────────────────────────────────────┤
│ Active Directory │    DNS    │    DHCP    │   NTP   │   PKI     │
└─────────────────────────────────────────────────────────────────┘
```

### 4.4 Matrice Dipendenze Critiche

| Sistema | Dipende da | Necessario per |
|---------|------------|----------------|
| ERP | AD, DNS, Database, Storage | Tutti i processi business |
| Database | Storage, Network, AD | ERP, BI, Reporting |
| Active Directory | DNS, Network | Tutti i sistemi |
| Email | AD, DNS, Network | Comunicazioni |
| Network | Power, ISP | Tutti i sistemi |

---

## 5. Infrastruttura DR

### 5.1 Architettura DR

```
┌─────────────────────────────────────────────────────────────────────┐
│                        SITO PRIMARIO                                 │
│                     [Ubicazione Primaria]                            │
├─────────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐                  │
│  │   Compute   │  │   Storage   │  │   Network   │                  │
│  │   Cluster   │  │    SAN      │  │   Core      │                  │
│  │  [X] Host   │  │  [X] TB     │  │  [X] Gbps   │                  │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘                  │
│         │                │                │                          │
│         └────────────────┼────────────────┘                          │
│                          │                                           │
│                    ┌─────▼─────┐                                     │
│                    │  REPLICA  │                                     │
│                    │  ENGINE   │                                     │
│                    └─────┬─────┘                                     │
└──────────────────────────┼──────────────────────────────────────────┘
                           │
                    ═══════╪═══════  WAN Link
                    [X] Gbps / [X]ms latency
                           │
┌──────────────────────────┼──────────────────────────────────────────┐
│                          │                                           │
│                    ┌─────▼─────┐                                     │
│                    │  REPLICA  │                                     │
│                    │  TARGET   │                                     │
│                    └─────┬─────┘                                     │
│         ┌────────────────┼────────────────┐                          │
│         │                │                │                          │
│  ┌──────▼──────┐  ┌──────▼──────┐  ┌──────▼──────┐                  │
│  │   Compute   │  │   Storage   │  │   Network   │                  │
│  │   Cluster   │  │    SAN      │  │   Core      │                  │
│  │  [X] Host   │  │  [X] TB     │  │  [X] Gbps   │                  │
│  └─────────────┘  └─────────────┘  └─────────────┘                  │
├─────────────────────────────────────────────────────────────────────┤
│                          DR SITE                                     │
│                      [Ubicazione DR]                                 │
│                    Distanza: [X] km                                  │
└─────────────────────────────────────────────────────────────────────┘
```

### 5.2 Specifiche Siti

| Componente | Sito Primario | Sito DR | Note |
|------------|---------------|---------|------|
| **Ubicazione** | [Indirizzo] | [Indirizzo] | Distanza: [X] km |
| **Compute** | [X] server / [Y] vCPU | [X] server / [Y] vCPU | [Z]% capacità |
| **Storage** | [X] TB SAN | [X] TB SAN | Replica sinc/asinc |
| **Network** | [X] Gbps | [X] Gbps | Dual ISP |
| **Power** | UPS [X]h + Generator | UPS [X]h + Generator | N+1 |
| **Cooling** | [X] kW N+1 | [X] kW N+1 | Ridondato |

### 5.3 Connettività

| Connessione | Tipo | Bandwidth | Latenza | Utilizzo |
|-------------|------|-----------|---------|----------|
| WAN Primaria | MPLS/Dedicata | [X] Gbps | < [X] ms | Replica dati |
| WAN Backup | Internet VPN | [X] Mbps | < [X] ms | Failover |
| ISP DR #1 | [Provider] | [X] Gbps | - | Accesso utenti |
| ISP DR #2 | [Provider] | [X] Mbps | - | Backup |

### 5.4 Strategia di Replica

| Tipo Dato | Metodo | Frequenza | RPO Effettivo |
|-----------|--------|-----------|---------------|
| Database Tier 1 | Replica sincrona | Real-time | ~0 |
| Database Tier 2 | Replica asincrona | 15 min | 15 min |
| File System | Rsync/DFS-R | Oraria | 1 ora |
| VM/Container | Snapshot replica | 4 ore | 4 ore |
| Configuration | Git/Ansible | On change | Immediato |
| Backup | [Tool] | Giornaliero | 24 ore |

---

## 6. Procedure di Backup (DORA Art. 12)

### 6.1 Strategia Backup 3-2-1-1

```
┌─────────────────────────────────────────────────────────────────┐
│                    REGOLA 3-2-1-1 (DORA)                        │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  3 = TRE copie dei dati                                         │
│      ├── Produzione                                             │
│      ├── Backup locale (NAS/Tape)                               │
│      └── Backup off-site (Cloud/DR)                             │
│                                                                  │
│  2 = DUE tipi di media diversi                                  │
│      ├── Disco (SAN/NAS)                                        │
│      └── Cloud/Tape/Object Storage                              │
│                                                                  │
│  1 = UNA copia off-site                                         │
│      └── Geograficamente separata (> 100 km)                    │
│                                                                  │
│  1 = UNA copia immutabile (DORA Art.12)                         │
│      └── WORM / Immutable backup / Air-gapped                   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### 6.2 Schedule Backup

| Tipo | Frequenza | Retention | Window | Target |
|------|-----------|-----------|--------|--------|
| **Full** | Domenica | 4 settimane | 00:00-06:00 | Cloud/Tape |
| **Differential** | Lun-Sab | 1 settimana | 00:00-04:00 | Disco locale |
| **Incremental** | Ogni 4 ore | 48 ore | Continuo | Disco locale |
| **Transaction Log** | Ogni 15 min | 7 giorni | Continuo | Disco + DR |
| **Archive** | Mensile | 7 anni | Weekend | Tape/Cold storage |

### 6.3 Backup per Sistema

| Sistema | Tipo Backup | Tool | Schedule | Retention | Target |
|---------|-------------|------|----------|-----------|--------|
| Oracle DB | RMAN + DataGuard | Native | Continuo | 30 giorni | DR Site |
| SQL Server | Full + Log | [Tool] | Full: Dom, Log: 15min | 30 giorni | DR Site |
| File Server | Full + Incr | [Tool] | Giornaliero | 60 giorni | Cloud |
| VM Infrastructure | Snapshot | [Tool] | Giornaliero | 14 giorni | DR Site |
| Microsoft 365 | Cloud-to-cloud | [Tool] | Continuo | 90 giorni | Cloud |
| Active Directory | System State | Native | Giornaliero | 30 giorni | DR Site |

### 6.4 Monitoraggio Backup

**Dashboard Monitoraggio**: {{url}}

| Metrica | Soglia Warning | Soglia Critical | Azione |
|---------|----------------|-----------------|--------|
| Backup fallito | 1 consecutivo | 2 consecutivi | Ticket P2 → P1 |
| Backup incompleto | > 5% file | > 10% file | Investigare |
| Durata backup | > 150% media | > 200% media | Analisi |
| Spazio disponibile | < 20% | < 10% | Espansione |
| Replica lag | > 30 min | > 1 ora | Escalation |

### 6.5 Test Restore

| Frequenza | Tipo Test | Scope | Responsabile |
|-----------|-----------|-------|--------------|
| Settimanale | File random | File Server | Backup Admin |
| Mensile | Database completo | DB non-prod | DBA |
| Trimestrale | VM completa | Sistema Tier 2 | Infra Team |
| Semestrale | Full DR test | Tutti Tier 1 | DR Manager |

---

## 7. Procedure di Recovery

### 7.1 Workflow Recovery Completo

```
═══════════════════════════════════════════════════════════════════
                    IT DISASTER RECOVERY WORKFLOW
═══════════════════════════════════════════════════════════════════

FASE 0: RILEVAMENTO (0-30 min)
├── Allarme ricevuto (monitoring/utenti)
├── Valutazione iniziale impatto
├── Escalation se necessario
└── Decisione: Incident vs Disaster
                │
                ▼
FASE 1: DICHIARAZIONE (30-60 min)
├── DR Manager convoca emergency call
├── Assessment dettagliato impatto
├── Dichiarazione formale disastro IT
├── Notifica stakeholder (BC Manager, Management)
└── Attivazione Team DR
                │
                ▼
FASE 2: ATTIVAZIONE DR SITE (1-2 ore)
├── Team DR connesso/presente al DR site
├── Verifica infrastruttura DR
├── Attivazione servizi base (AD, DNS, Network)
├── Verifica connettività
└── Conferma readiness infrastruttura
                │
                ▼
FASE 3: RECOVERY SISTEMI (2-8 ore)
├── Recovery Tier 1 (priorità massima)
├── Recovery Tier 2 (seconda priorità)
├── Recovery Tier 3 (se tempo permette)
├── Validazione funzionale per sistema
└── Verifica integrità dati
                │
                ▼
FASE 4: VALIDAZIONE (1-2 ore)
├── Test applicazioni critiche end-to-end
├── Test integrazioni
├── Test accesso utenti
├── Performance check
└── Business sign-off
                │
                ▼
FASE 5: OPERAZIONI SU DR (ongoing)
├── Monitoraggio intensivo
├── Supporto utenti
├── Comunicazioni periodiche
├── Documentazione
└── Pianificazione failback
                │
                ▼
FASE 6: FAILBACK (quando sito primario pronto)
├── Assessment sito primario
├── Sincronizzazione dati reverse
├── Failback pianificato
├── Validazione post-failback
└── Ritorno alla normalità
```

### 7.2 Sequenza di Recovery Dettagliata

```
ORDINE DI RECOVERY - ESECUZIONE SEQUENZIALE

[STEP 1] INFRASTRUCTURE FOUNDATION          Target: 30 min
    ├── 1.1 Verifica Power & Cooling
    ├── 1.2 Network core activation
    ├── 1.3 Storage SAN online
    └── 1.4 Compute cluster ready
                │
                ▼
[STEP 2] BASE SERVICES                      Target: 1 ora
    ├── 2.1 Active Directory / LDAP
    ├── 2.2 DNS primario e secondario
    ├── 2.3 DHCP (se necessario)
    ├── 2.4 NTP
    └── 2.5 Certificate Authority (PKI)
                │
                ▼
[STEP 3] SECURITY SERVICES                  Target: 1.5 ore
    ├── 3.1 Firewall
    ├── 3.2 VPN Gateway
    ├── 3.3 PAM/Identity management
    └── 3.4 SIEM/Log collection
                │
                ▼
[STEP 4] DATABASE LAYER                     Target: 2 ore
    ├── 4.1 Database Tier 1 (failover)
    ├── 4.2 Database Tier 2
    ├── 4.3 Verifica integrità dati
    └── 4.4 Test connessione applicazioni
                │
                ▼
[STEP 5] APPLICATION LAYER                  Target: 4 ore
    ├── 5.1 Applicazioni Tier 1
    ├── 5.2 Applicazioni Tier 2
    ├── 5.3 Middleware/Integration
    └── 5.4 Web servers/Load balancers
                │
                ▼
[STEP 6] VALIDATION                         Target: 1 ora
    ├── 6.1 Test funzionali applicazioni
    ├── 6.2 Test performance baseline
    ├── 6.3 Test sicurezza
    └── 6.4 User acceptance testing
```

### 7.3 Runbook per Sistema

#### Active Directory Recovery

| Sistema | Active Directory |
|---------|------------------|
| **RTO** | 30 min |
| **Responsabile** | [Nome] |
| **Prerequisiti** | Network, DNS (temporaneo) |

| Step | Azione | Comando/Procedura | Verifica |
|------|--------|-------------------|----------|
| 1 | Avvia DC DR | Power on VM/Server | Ping OK |
| 2 | Verifica replica | `repadmin /showrepl` | No errori |
| 3 | Verifica FSMO roles | `netdom query fsmo` | Ruoli assegnati |
| 4 | Seize FSMO se necessario | `ntdsutil` seize | Ruoli trasferiti |
| 5 | Test autenticazione | Login test user | Login OK |
| 6 | Verifica DNS integrato | `nslookup domain.local` | Risoluzione OK |

#### Database Oracle Recovery

| Sistema | Oracle Database |
|---------|------------------|
| **RTO** | 1 ora |
| **Responsabile** | [Nome DBA] |
| **Prerequisiti** | AD, Network, Storage |

| Step | Azione | Comando/Procedura | Verifica |
|------|--------|-------------------|----------|
| 1 | Verifica DataGuard status | `dgmgrl> show configuration` | Primary/Standby OK |
| 2 | Failover a standby | `dgmgrl> failover to 'standby_db'` | Success |
| 3 | Verifica open mode | `SELECT OPEN_MODE FROM V$DATABASE` | READ WRITE |
| 4 | Verifica redo apply | `SELECT * FROM V$ARCHIVE_GAP` | No gaps |
| 5 | Test connessione | TNS test da app server | Connection OK |
| 6 | Check performance | AWR baseline comparison | Accettabile |

#### SQL Server Recovery

| Sistema | SQL Server |
|---------|------------------|
| **RTO** | 2 ore |
| **Responsabile** | [Nome DBA] |
| **Prerequisiti** | AD, Network, Storage |

| Step | Azione | Comando/Procedura | Verifica |
|------|--------|-------------------|----------|
| 1 | Verifica AlwaysOn | SSMS > Availability Groups | Synchronized |
| 2 | Failover manuale | `ALTER AVAILABILITY GROUP [AG] FAILOVER` | New primary |
| 3 | Verifica database | `SELECT state_desc FROM sys.databases` | ONLINE |
| 4 | Update connessioni | DNS/Load balancer update | Redirect OK |
| 5 | Test applicazione | Query test | Response OK |

### 7.4 Checklist Recovery Tier 1

```
╔════════════════════════════════════════════════════════════════╗
║              TIER 1 RECOVERY CHECKLIST                          ║
╠════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  PRE-RECOVERY                                                    ║
║  ☐ DR site accessibile (fisico/remoto)                          ║
║  ☐ Team DR presente/connesso                                    ║
║  ☐ Comunicazione bridge attivo                                   ║
║  ☐ Autorizzazione DR Manager ricevuta                           ║
║                                                                  ║
║  INFRASTRUCTURE                                                  ║
║  ☐ Network core operativo                                       ║
║  ☐ Storage SAN disponibile                                      ║
║  ☐ Compute risorse allocate                                     ║
║  ☐ Power stabile                                                 ║
║                                                                  ║
║  BASE SERVICES                                                   ║
║  ☐ Active Directory operativo          Ora: ____:____           ║
║  ☐ DNS funzionante                     Ora: ____:____           ║
║  ☐ DHCP (se necessario)                Ora: ____:____           ║
║  ☐ NTP sincronizzato                   Ora: ____:____           ║
║                                                                  ║
║  DATABASE                                                        ║
║  ☐ Oracle failover completato          Ora: ____:____           ║
║  ☐ SQL Server failover completato      Ora: ____:____           ║
║  ☐ Integrità dati verificata                                    ║
║  ☐ Performance accettabile                                       ║
║                                                                  ║
║  APPLICATIONS                                                    ║
║  ☐ [App Tier 1 #1] operativa          Ora: ____:____           ║
║  ☐ [App Tier 1 #2] operativa          Ora: ____:____           ║
║  ☐ [App Tier 1 #3] operativa          Ora: ____:____           ║
║  ☐ Integrazioni funzionanti                                     ║
║                                                                  ║
║  VALIDATION                                                      ║
║  ☐ Test transazione end-to-end                                  ║
║  ☐ Test accesso utenti                                          ║
║  ☐ Sign-off business owner                                      ║
║  ☐ Documentazione completata                                    ║
║                                                                  ║
║  RTO ACHIEVEMENT                                                 ║
║  Tempo totale recovery: ____h ____min                           ║
║  RTO Target: [X] ore                                            ║
║  Status: ☐ Met  ☐ Not Met                                       ║
║                                                                  ║
║  FIRMA DR Manager: _________________ Data: __/__/____           ║
╚════════════════════════════════════════════════════════════════╝
```

---

## 8. Scenari di Disastro

### 8.1 Scenario: Perdita Data Center

**Trigger**: Incendio, allagamento, terremoto, evacuazione forzata

**Azioni Immediate**:
1. Evacuazione personale (se presente)
2. Valutazione danni da remoto (se possibile)
3. Dichiarazione disastro IT
4. Attivazione full DR site

**Recovery**:
- Failover completo al DR site
- Tutti i sistemi Tier 1-3
- RTO Target: 4 ore

**Checklist Specifica**:
- [ ] Personale in sicurezza
- [ ] Connettività al DR site verificata
- [ ] Failover network completato
- [ ] Failover storage completato
- [ ] VM/Server avviati al DR site
- [ ] Database failover completato
- [ ] Applicazioni validate
- [ ] Utenti reindirizzati (DNS/Load balancer)

### 8.2 Scenario: Attacco Ransomware

**Trigger**: Rilevamento encryption, richiesta riscatto, alert security

**Azioni Immediate** (CRITICO - ordine specifico):
1. **ISOLAMENTO IMMEDIATO**: Disconnettere sistemi infetti dalla rete
2. **PRESERVAZIONE**: NON spegnere - preservare evidence forensic
3. **ASSESSMENT**: Determinare scope dell'infezione
4. **ESCALATION**: Security team + Management + Legal + Cyber Insurance

**Recovery**:
- Restore da backup pre-infezione (verificare integrità)
- Clean room environment per validazione
- Rebuild se necessario

**Checklist Specifica**:
- [ ] Sistemi infetti isolati (network disconnect)
- [ ] Evidence forensic preservata
- [ ] Punto di infezione identificato (Patient Zero)
- [ ] Backup verificati NON compromessi
- [ ] Ambiente clean room preparato
- [ ] Restore in ambiente isolato
- [ ] Validazione integrità post-restore
- [ ] Hardening pre-reconnection
- [ ] Monitoring aumentato post-recovery
- [ ] Incident report completato
- [ ] Notifica autorità se data breach (GDPR/NIS2)

### 8.3 Scenario: Failure Storage

**Trigger**: Perdita array primario, corruzione dati estesa

**Azioni Immediate**:
1. Verifica failure mode (hardware/software/corruzione)
2. Tentativo recovery locale (se possibile)
3. Se impossibile, failover a DR storage

**Recovery**:
- Replica storage al DR site
- Restore da snapshot/backup

**Checklist Specifica**:
- [ ] Tipo failure identificato
- [ ] Vendor storage contattato
- [ ] Failover LUN attivato
- [ ] Database re-puntati a nuovo storage
- [ ] Performance verificata
- [ ] Data integrity check completato

### 8.4 Scenario: Perdita Connettività

**Trigger**: Failure ISP, DDoS, cable cut fisico

**Azioni Immediate**:
1. Verificare punto di failure (interno/esterno)
2. Attivare connessione backup
3. Se totale, valutare attivazione DR site

**Recovery**:
- Failover a ISP secondario
- BGP rerouting (se applicabile)
- Attivazione VPN backup

**Checklist Specifica**:
- [ ] Causa failure identificata
- [ ] ISP primario contattato (ticket aperto)
- [ ] Link backup attivato
- [ ] BGP convergenza completata (se applicabile)
- [ ] Servizi esterni raggiungibili
- [ ] VPN utenti remote funzionante

---

## 9. Procedura Failback

### 9.1 Prerequisiti Failback

Prima di iniziare il failback, verificare:

- [ ] Sito primario completamente ripristinato
- [ ] Root cause identificata ed eliminata
- [ ] Infrastruttura testata e certificata
- [ ] Capacità adeguata confermata
- [ ] Change window approvata
- [ ] Team completo disponibile
- [ ] Piano comunicazione pronto
- [ ] Rollback plan definito

### 9.2 Procedura Failback

```
FASE 1: PREPARAZIONE (1-2 giorni prima)
├── Verifica completa infrastruttura sito primario
├── Test connettività WAN tra siti
├── Avvio sincronizzazione dati reverse
├── Validazione backup correnti
└── Comunicazione stakeholder su piano

FASE 2: SINCRONIZZAZIONE (4-8 ore)
├── Final sync database
├── Final sync file system
├── Verifica consistenza dati
└── Point-in-time recovery test

FASE 3: CUTOVER (2-4 ore)
├── Stop servizi su DR site (maintenance mode)
├── Final data sync (delta)
├── Switch DNS/Load balancer
├── Start servizi su primario
└── Validazione immediata

FASE 4: VALIDAZIONE (2 ore)
├── Test applicazioni critiche
├── Test integrazioni
├── Test accesso utenti
└── Business sign-off

FASE 5: NORMALIZZAZIONE (24-48 ore)
├── Monitoraggio intensivo
├── Ripristino replica verso DR
├── Documentazione lessons learned
└── Update procedure se necessario
```

### 9.3 Checklist Failback

```
╔════════════════════════════════════════════════════════════════╗
║                    FAILBACK CHECKLIST                           ║
╠════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  PRE-FAILBACK                                                    ║
║  ☐ Root cause risolto e documentato                             ║
║  ☐ Sito primario certificato (test completati)                  ║
║  ☐ Change request approvato                                     ║
║  ☐ Team DR completo disponibile                                 ║
║  ☐ Rollback plan documentato                                    ║
║                                                                  ║
║  SYNC                                                            ║
║  ☐ Database sync completato (delta < RPO)                       ║
║  ☐ File system sync completato                                  ║
║  ☐ Consistency check passed                                     ║
║                                                                  ║
║  CUTOVER                                                         ║
║  ☐ Servizi DR in maintenance mode                               ║
║  ☐ Final sync eseguito                                          ║
║  ☐ DNS/LB aggiornato                                            ║
║  ☐ Servizi primario avviati                                     ║
║                                                                  ║
║  VALIDATION                                                      ║
║  ☐ Applicazioni funzionanti                                     ║
║  ☐ Performance nella norma                                       ║
║  ☐ Utenti operativi                                             ║
║  ☐ Business sign-off ricevuto                                   ║
║                                                                  ║
║  POST-FAILBACK                                                   ║
║  ☐ Replica DR riattivata                                        ║
║  ☐ Backup schedule normale                                      ║
║  ☐ Monitoraggio normale                                         ║
║  ☐ Documentazione aggiornata                                    ║
║  ☐ Lessons learned documentate                                  ║
║                                                                  ║
║  FIRMA DR Manager: _________________ Data: __/__/____           ║
╚════════════════════════════════════════════════════════════════╝
```

---

## 10. Test e Manutenzione (DORA Art. 25)

### 10.1 Programma Test DR Annuale

| Tipo Test | Frequenza | Durata | Scope | Owner |
|-----------|-----------|--------|-------|-------|
| **Tabletop** | Trimestrale | 2 ore | Procedure review | DR Manager |
| **Component** | Mensile | 2-4 ore | Singolo sistema | System Owner |
| **Partial** | Semestrale | 4-8 ore | Sistemi Tier 1 | DR Manager |
| **Full** | Annuale | 8-24 ore | Tutti i Tier | IT Manager |

### 10.2 Calendario Test Annuale

| Mese | Tipo Test | Focus |
|------|-----------|-------|
| Gennaio | Component | Database failover |
| Febbraio | Component | Network failover |
| Marzo | Tabletop | Scenario ransomware |
| Aprile | **Partial** | Tier 1 applications |
| Maggio | Component | Storage failover |
| Giugno | Tabletop | Scenario data center loss |
| Luglio | Component | AD/DNS failover |
| Agosto | Component | Backup restore |
| Settembre | Tabletop | Scenario cyber attack |
| Ottobre | **Partial** | Tier 1+2 applications |
| Novembre | Component | Communication systems |
| Dicembre | **FULL DR TEST** | Complete failover |

### 10.3 Template Report Test DR

```
═══════════════════════════════════════════════════════════════
              IT DISASTER RECOVERY TEST REPORT
═══════════════════════════════════════════════════════════════

Test ID: DR-TEST-{{document_year}}-[NN]
Data: {{document_date}}
Tipo: [Tabletop/Component/Partial/Full]
Durata Pianificata: [X] ore
Durata Effettiva: [Y] ore

OBIETTIVI
─────────────────────────────────────────────────────────────────
1. [Obiettivo 1]
2. [Obiettivo 2]
3. [Obiettivo 3]

SISTEMI TESTATI
─────────────────────────────────────────────────────────────────
| Sistema | RTO Target | RTO Actual | RPO Target | RPO Actual | Status |
|---------|------------|------------|------------|------------|--------|
| [Sys 1] | [X]h       | [Y]h       | [X]h       | [Y]h       | ✓/✗   |
| [Sys 2] | [X]h       | [Y]h       | [X]h       | [Y]h       | ✓/✗   |

RISULTATI
─────────────────────────────────────────────────────────────────
Obiettivi raggiunti: [X]/[Y]
RTO compliance: [X]%
RPO compliance: [X]%
Overall status: ☐ PASS  ☐ PARTIAL  ☐ FAIL

ISSUES RILEVATE
─────────────────────────────────────────────────────────────────
| # | Issue | Severità | Azione Correttiva | Owner | Deadline |
|---|-------|----------|-------------------|-------|----------|
| 1 | [Issue] | High/Med/Low | [Azione] | [Nome] | [Data] |

LESSONS LEARNED
─────────────────────────────────────────────────────────────────
Cosa ha funzionato bene:
• [Item 1]
• [Item 2]

Cosa migliorare:
• [Item 1]
• [Item 2]

APPROVAZIONI
─────────────────────────────────────────────────────────────────
DR Manager: _________________ Data: _______
IT Manager: _________________ Data: _______
```

### 10.4 Manutenzione DRP

| Attività | Frequenza | Responsabile |
|----------|-----------|--------------|
| Review contact list | Mensile | DR Manager |
| Update inventario sistemi | Trimestrale | IT Asset Mgmt |
| Review procedure | Semestrale | DR Manager |
| Update RTO/RPO (da BIA) | Annuale | BC Manager + IT |
| Review contratti DR | Annuale | Procurement |
| Audit compliance | Annuale | Internal Audit |

---

## 11. Comunicazioni

### 11.1 Matrice Comunicazioni DR

| Stakeholder | Quando | Chi Comunica | Canale | Template |
|-------------|--------|--------------|--------|----------|
| IT Team | Immediato | DR Manager | Call/Chat | COM-DR-001 |
| BC Manager | 15 min | DR Manager | Call | COM-DR-002 |
| IT Management | 30 min | DR Manager | Call | COM-DR-003 |
| Executive (CIO/CEO) | 1 ora | IT Manager | Call | COM-DR-004 |
| Utenti interni | 2 ore | Help Desk | Email/Intranet | COM-DR-005 |
| Fornitori IT critici | 1 ora | DR Manager | Call | COM-DR-006 |

### 11.2 Bridge Permanente DR

| Tipo | Dettaglio |
|------|-----------|
| Conference Call | [Numero] - PIN: [PIN] |
| Video Conference | [Link Teams/Zoom] |
| Chat DR | [Link canale - es. Teams/Slack] |

---

## 12. Vendor e Supporto

### 12.1 Contatti Vendor Critici

| Vendor | Servizio | N. Contratto | SLA | Contatto H24 |
|--------|----------|--------------|-----|--------------|
| [HW Vendor] | Server/Storage | [Num] | 4h onsite | [Tel] |
| [DB Vendor] | Database support | [Num] | 2h response | [Tel] |
| [Cloud Provider] | IaaS/PaaS | [Num] | 99.95% | [Portal/Tel] |
| [ISP Primary] | Connettività | [Num] | 99.9% | [Tel] |
| [DR Site Provider] | Colocation/DRaaS | [Num] | 99.99% | [Tel] |
| [Backup SW] | Backup/Recovery | [Num] | NBD | [Tel] |

### 12.2 Escalation Vendor

| Livello | Tempo | Azione |
|---------|-------|--------|
| 1 | 0-30 min | Apertura ticket/call standard |
| 2 | 30-60 min | Escalation a team lead vendor |
| 3 | 1-2 ore | Escalation a management vendor |
| 4 | 2+ ore | Account manager + nostro management |

---

## 13. Conformità e Audit

### 13.1 Requisiti Normativi

| Normativa | Requisito | Riferimento | Copertura DRP |
|-----------|-----------|-------------|---------------|
| **ISO 22301** | Piani BC documentati | Clausola 8.4.4 | Tutto il documento |
| **ISO 27001** | Continuità ICT | A.5.30 | Sezioni 5-9 |
| **NIS2** | Backup e recovery | Art. 21(2)(c) | Sezioni 6, 7 |
| **DORA** | Digital resilience | Art. 11, 12, 25 | Tutto il documento |
| **GDPR** | Disponibilità dati | Art. 32.1(c) | Sezioni 6, 7 |

### 13.2 KPI e Metriche

| KPI | Target | Misurazione | Owner |
|-----|--------|-------------|-------|
| RTO compliance (test) | 100% | Test DR | DR Manager |
| RPO compliance (test) | 100% | Test DR | DR Manager |
| Backup success rate | > 99% | Daily monitoring | Backup Admin |
| DR test completion | 100% schedule | Annuale | DR Manager |
| DRP currency | < 6 mesi | Review date | DR Manager |
| Team DR training | 100% annuale | Training records | HR/IT |

---

## 14. Allegati

### Allegato A: Contact List Emergency (STAMPA E CONSERVA)

```
╔════════════════════════════════════════════════════════════════╗
║               CONTATTI EMERGENZA DR - CONFIDENZIALE             ║
╠════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  DR TEAM                                                         ║
║  ─────────────────────────────────────────────────────────────  ║
║  DR Manager:        [Nome]        [Mobile]                      ║
║  Backup DR Manager: [Nome]        [Mobile]                      ║
║  Resp. Infra:       [Nome]        [Mobile]                      ║
║  DBA Lead:          [Nome]        [Mobile]                      ║
║  Network Lead:      [Nome]        [Mobile]                      ║
║  Security Lead:     [Nome]        [Mobile]                      ║
║                                                                  ║
║  MANAGEMENT                                                      ║
║  ─────────────────────────────────────────────────────────────  ║
║  CIO:               [Nome]        [Mobile]                      ║
║  CISO:              [Nome]        [Mobile]                      ║
║  BC Manager:        [Nome]        [Mobile]                      ║
║  CEO:               [Nome]        [Mobile]                      ║
║                                                                  ║
║  VENDOR CRITICI                                                  ║
║  ─────────────────────────────────────────────────────────────  ║
║  [HW Vendor] H24:   [Numero]                                    ║
║  [Cloud] Support:   [Numero]                                    ║
║  [ISP] NOC:         [Numero]                                    ║
║  [DR Site]:         [Numero]                                    ║
║                                                                  ║
║  BRIDGE DR:         [Numero]      PIN: [PIN]                    ║
║                                                                  ║
╚════════════════════════════════════════════════════════════════╝
```

### Allegato B: Quick Reference Card

```
╔════════════════════════════════════════════════════════════════╗
║           QUICK REFERENCE - IT DISASTER RECOVERY                ║
╠════════════════════════════════════════════════════════════════╣
║                                                                  ║
║  1. ASSESS    Cosa è successo? Scope? Impatto?                  ║
║                                                                  ║
║  2. NOTIFY    DR Manager → IT Mgmt → BC Manager → Executive    ║
║                                                                  ║
║  3. DECLARE   Se criteri met → Dichiarare disastro IT          ║
║                                                                  ║
║  4. ACTIVATE  Team al DR site / connesso remoto                 ║
║                                                                  ║
║  5. RECOVER   Infrastructure → Services → Database → Apps       ║
║                                                                  ║
║  6. VALIDATE  Test end-to-end, business sign-off               ║
║                                                                  ║
║  7. COMMUNICATE  Update ogni 30-60 min                         ║
║                                                                  ║
║  ═══════════════════════════════════════════════════════════   ║
║  BRIDGE DR: [NUMERO] - PIN: [PIN]                               ║
║  DR Manager: {{contact_name}} - {{mobile}}                                  ║
║  ═══════════════════════════════════════════════════════════   ║
║                                                                  ║
╚════════════════════════════════════════════════════════════════╝
```

---

## 15. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |
| 2.0 | {{document_date}} | {{document_author}} | Nuovo formato, allineamento DORA/NIS2 |

---

## 16. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{it_manager}} | | {{document_date}} |
| Verificato da | {{ciso}} | | {{document_date}} |
| Verificato da | {{bc_manager}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Business Continuity Plan | {{company_name}}-BCP-BCMS-001 | BCP che attiva il DRP |
| Business Impact Analysis | {{company_name}}-BIA-BCMS-001 | RTO/RPO per sistemi IT |
| Recovery Procedure | {{company_name}}-REC-BCMS-001 | Procedure operative recovery |
| Backup and Recovery (ISMS) | {{company_name}}-BKP-ISMS-001 | Procedura backup e restore |
| Asset Inventory (ISMS) | {{company_name}}-INV-ISMS-001 | Inventario sistemi IT |
| Incident Management (ISMS) | {{company_name}}-INC-ISMS-001 | Incidenti che attivano DRP |
| Exercise Programme | {{company_name}}-EXR-BCMS-001 | Test del DRP |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{it_manager}}` | Redatto da | ☐ |
| 6 | `{{bc_manager}}` | Verificato da | ☐ |
| 7 | Inventario sistemi critici | Sezione 3 — tutti i sistemi con RTO/RPO | ☐ |
| 8 | Procedure recovery per sistema | Sezione 5 — runbook per ogni sistema critico | ☐ |
| 9 | Sito DR configurato | Sezione 4 — infrastruttura DR operativa | ☐ |
| 10 | Contatti team DR | Sezione 6 — lista completa e aggiornata | ☐ |
| 11 | Test DR eseguito | Almeno un test tecnico con verifica RTO/RPO | ☐ |
| 12 | Backup verificati | Sezione 7 — ultimo test restore riuscito | ☐ |

---

*Template conforme a ISO 22301:2019 Clausole 8.4.4, 8.4.5 e DORA Art. 11-12*
*Creato con Kynosure.ai*
