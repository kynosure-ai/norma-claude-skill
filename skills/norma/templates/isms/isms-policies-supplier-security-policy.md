---
title: Politica di Sicurezza per i Fornitori
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{security_officer_title}}'
approver: '{{senior_management}}'
framework: ISO27001
language: IT
documentType: policy
iso_controls:
  - A.5.19 - Sicurezza delle informazioni nelle relazioni con i fornitori
  - A.5.20 - Gestione della sicurezza nei contratti con i fornitori
  - A.5.21 - Gestione della sicurezza nella catena di fornitura ICT
  - >-
    A.5.22 - Monitoraggio, revisione e gestione delle modifiche dei servizi dei
    fornitori
  - A.5.23 - Sicurezza delle informazioni per l'uso di servizi cloud
cross_references:
  - NIS2 Art. 21(2)(d) - Sicurezza catena approvvigionamento
  - DORA Art. 28-30 - Gestione rischi ICT terze parti
  - GDPR Art. 28 - Responsabile del trattamento
  - GDPR Art. 32 - Sicurezza del trattamento
status: Da approvare
subset: true
---

# Politica di Sicurezza per i Fornitori

## 1. Scopo e Obiettivi

### 1.1 Scopo

{{company_name}} riconosce che la sicurezza delle informazioni non si esaurisce all'interno del perimetro organizzativo, ma si estende a tutti i soggetti che, a vario titolo, accedono alle risorse aziendali o trattano informazioni per conto dell'Organizzazione. La gestione della sicurezza nella catena di fornitura rappresenta pertanto un elemento critico del Sistema di Gestione per la Sicurezza delle Informazioni, particolarmente rilevante nel contesto normativo definito dalla Direttiva NIS2 e dal Regolamento DORA.

La presente Politica di Sicurezza per i Fornitori definisce i requisiti e le procedure per la gestione sicura delle relazioni con terze parti. L'Organizzazione stabilisce criteri per la selezione e valutazione dei fornitori, la definizione contrattuale dei requisiti di sicurezza, la gestione della supply chain ICT con particolare attenzione ai rischi di concentrazione e dipendenza, il monitoraggio continuo delle prestazioni di sicurezza e la gestione dei servizi cloud secondo il modello di responsabilità condivisa.

### 1.2 Obiettivi

La Politica persegue obiettivi di protezione, conformità e resilienza della catena di fornitura. L'Organizzazione garantisce la valutazione della sicurezza di tutti i fornitori critici prima dell'avvio della relazione contrattuale, l'inserimento di clausole di sicurezza appropriate in tutti i contratti ICT, l'assessment periodico dei fornitori di primo livello, la review annuale delle prestazioni di sicurezza per i fornitori critici e la verifica della compliance dei cloud provider ai requisiti di sicurezza applicabili. Questi obiettivi rispondono ai requisiti ISO 27001 Annex A.5.19-5.23, NIS2 Art. 21(2)(d) e DORA Art. 28-30.

---

## 2. Ambito di Applicazione

La presente Politica si applica a tutte le relazioni con fornitori che comportano accesso, diretto o indiretto, alle informazioni o ai sistemi dell'Organizzazione. L'ambito comprende sia i fornitori di servizi ICT, che rappresentano tipicamente le relazioni a maggior rischio, sia i fornitori di servizi generali che possono comunque avere accesso a informazioni riservate o ad aree protette.

### 2.1 Fornitori Coperti

L'Organizzazione classifica i fornitori in base alla criticità della relazione e al livello di rischio associato. I cloud provider (IaaS, PaaS, SaaS), i fornitori di outsourcing IT quali managed service provider e gestori di infrastruttura, e le software house e system integrator rappresentano le categorie a criticità elevata. I servizi professionali di consulenza e audit e i vendor di hardware e software presentano criticità media. I servizi generali quali facility management comportano tipicamente un livello di rischio inferiore, pur richiedendo attenzione quando comportano accesso fisico ad aree sensibili.

### 2.2 Esclusioni

Sono esclusi dall'ambito della presente Politica gli acquisti one-shot che non comportano accesso a dati o sistemi, i fornitori privi di qualsiasi accesso fisico o logico alle risorse dell'Organizzazione e le utility standard quali acqua ed energia elettrica prive di componenti ICT rilevanti.

---

## 3. Classificazione Fornitori

### 3.1 Criteri di Criticità

```
┌─────────────────────────────────────────────────────────────┐
│                 MATRICE CRITICITÀ FORNITORI                 │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  Impatto su        CRITICO    ALTO    MEDIO    BASSO       │
│  Business                                                   │
│  ────────────────────────────────────────────────────       │
│  Core business     ●          ●       ○        ○           │
│  Dati sensibili    ●          ●       ●        ○           │
│  Accesso sistemi   ●          ●       ○        ○           │
│  Difficoltà        ●          ○       ○        ○           │
│  sostituzione                                               │
│                                                             │
│  ● = Contribuisce | ○ = Non contribuisce                   │
└─────────────────────────────────────────────────────────────┘
```

### 3.2 Livelli di Criticità

| Livello | Descrizione | Esempi | Requisiti |
|---------|-------------|--------|-----------|
| **Tier 1 - Critico** | Interruzione = Business stop | Cloud core, MSP, ERP vendor | Assessment completo, audit right, SLA stringenti |
| **Tier 2 - Alto** | Interruzione = Degradazione significativa | Software house, security vendor | Assessment, clausole sicurezza, review annuale |
| **Tier 3 - Medio** | Interruzione = Impatto gestibile | Consulenti, fornitori HW | Clausole base, NDA, review biennale |
| **Tier 4 - Basso** | Interruzione = Impatto minimo | Facility, servizi generali | NDA se accesso a informazioni |

### 3.3 Registro Fornitori

| Campo | Descrizione | Obbligatorio |
|-------|-------------|--------------|
| ID Fornitore | Codice univoco | Sì |
| Ragione Sociale | Nome completo | Sì |
| Categoria | Tipo servizio | Sì |
| Tier Criticità | 1-4 | Sì |
| Servizi forniti | Lista servizi | Sì |
| Dati accessibili | Classificazione | Sì |
| Sistemi accessibili | Lista asset | Se applicabile |
| Data inizio contratto | Data | Sì |
| Data scadenza | Data | Sì |
| Owner interno | Responsabile | Sì |
| Ultimo assessment | Data | Se Tier 1-2 |
| Prossima review | Data | Sì |

---

## 4. Processo di Selezione (Due Diligence)

### 4.1 Flusso di Selezione

```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│ IDENTIFICAZIONE│───►│  VALUTAZIONE │───►│ SECURITY     │
│   ESIGENZA    │    │  PRELIMINARE │    │ ASSESSMENT   │
└──────────────┘    └──────────────┘    └──────────────┘
                                               │
┌──────────────┐    ┌──────────────┐    ┌──────┴───────┐
│  ONBOARDING  │◄───│ CONTRATTO    │◄───│  APPROVAZIONE│
│              │    │ NEGOZIAZIONE │    │              │
└──────────────┘    └──────────────┘    └──────────────┘
```

### 4.2 Security Assessment Pre-Contratto

**Per Fornitori Tier 1-2:**

| Area | Requisiti Verificati | Metodo |
|------|---------------------|--------|
| **Certificazioni** | ISO 27001, SOC 2, CSA STAR | Documentale |
| **Sicurezza tecnica** | Vulnerability management, encryption | Questionario |
| **Gestione accessi** | IAM, MFA, privileged access | Questionario |
| **Business continuity** | DR, backup, RTO/RPO | Documentale |
| **Incident response** | Procedure, notifica, SLA | Documentale |
| **Compliance** | GDPR, NIS2, normative settore | Attestazione |
| **Subappaltatori** | Gestione supply chain | Questionario |

**Checklist Assessment:**
- [ ] Certificazioni verificate (copia certificati)
- [ ] Questionario sicurezza completato
- [ ] Penetration test report (ultimi 12 mesi)
- [ ] SOC 2 Type II o equivalente
- [ ] Polizza cyber risk verificata
- [ ] Referenze clienti verificate
- [ ] Verifica reputazionale completata

### 4.3 Questionario Sicurezza Fornitori

| Sezione | Domande Chiave | Peso |
|---------|----------------|------|
| **Governance** | Policy sicurezza, ruoli, awareness | 15% |
| **Controllo accessi** | IAM, MFA, PAM, logging | 20% |
| **Protezione dati** | Encryption, DLP, classificazione | 20% |
| **Sicurezza infrastruttura** | Network, endpoint, cloud | 15% |
| **Gestione vulnerabilità** | Patch, scan, pen test | 10% |
| **Business continuity** | DR, backup, test | 10% |
| **Incident management** | Detection, response, notifica | 10% |

**Scoring:**
| Punteggio | Valutazione | Azione |
|-----------|-------------|--------|
| 80-100% | Eccellente | Approvato |
| 60-79% | Adeguato | Approvato con remediation plan |
| 40-59% | Insufficiente | Richiesto miglioramento |
| <40% | Inaccettabile | Non approvato |

### 4.4 Valutazione Rischio Fornitore

| Fattore | Peso | Criteri |
|---------|------|---------|
| Accesso dati sensibili | 25% | C1-C4 |
| Accesso sistemi critici | 20% | Tier asset |
| Dependency operativa | 20% | Impatto business |
| Localizzazione | 15% | Giurisdizione dati |
| Storia/Reputazione | 10% | Track record |
| Postura sicurezza | 10% | Assessment score |

---

## 5. Requisiti Contrattuali (A.5.20)

### 5.1 Clausole Obbligatorie

**Per tutti i fornitori con accesso a informazioni:**
| Clausola | Contenuto |
|----------|-----------|
| **NDA** | Non divulgazione informazioni |
| **Compliance normativa** | Rispetto GDPR, normative applicabili |
| **Notifica incidenti** | Obbligo segnalazione breach |
| **Diritto di audit** | Accesso per verifica compliance |
| **Exit strategy** | Restituzione/cancellazione dati |

**Clausole aggiuntive per Tier 1-2:**
| Clausola | Contenuto |
|----------|-----------|
| **SLA sicurezza** | Metriche, penali, reporting |
| **Certificazioni** | Mantenimento ISO 27001/SOC 2 |
| **Subappalto** | Approvazione preventiva |
| **Penetration test** | Obbligo test periodici |
| **Background check** | Verifica personale assegnato |
| **Formazione** | Security awareness |
| **Cyber insurance** | Copertura minima richiesta |

### 5.2 Allegato Sicurezza Tipo

```
ALLEGATO SICUREZZA - REQUISITI TECNICI E ORGANIZZATIVI
======================================================

1. CONTROLLO ACCESSI
   - Implementare MFA per accessi privilegiati
   - Principio del minimo privilegio
   - Review trimestrale degli accessi
   - Logging di tutti gli accessi

2. PROTEZIONE DATI
   - Crittografia dati at rest (AES-256)
   - Crittografia dati in transit (TLS 1.2+)
   - Backup giornaliero con test mensile
   - Retention secondo accordi contrattuali

3. GESTIONE VULNERABILITÀ
   - Patching entro 30 giorni (critiche entro 7)
   - Scan vulnerabilità mensile
   - Penetration test annuale

4. INCIDENT RESPONSE
   - Notifica incidenti entro 24 ore
   - Cooperazione in caso di indagine
   - Report post-incidente entro 5 giorni

5. BUSINESS CONTINUITY
   - RTO: {{supplier_rto}} ore
   - RPO: {{supplier_rpo}} ore
   - Test DR annuale con report

6. AUDIT E COMPLIANCE
   - Audit annuale con accesso a documentazione
   - Right-to-audit con preavviso 10 giorni
   - Attestazione compliance annuale
```

### 5.3 Data Processing Agreement (DPA)

**Requisiti GDPR Art. 28:**
| Elemento | Contenuto |
|----------|-----------|
| Oggetto trattamento | Finalità, durata, tipo dati |
| Categorie interessati | Dipendenti, clienti, etc. |
| Obblighi responsabile | Istruzioni scritte, sicurezza |
| Sub-responsabili | Lista e procedura approvazione |
| Trasferimenti extra-UE | Base giuridica, garanzie |
| Diritti interessati | Supporto nell'esercizio |
| Cancellazione | Obbligo a fine contratto |
| Audit | Diritto di verifica |

---

## 6. Gestione Supply Chain ICT (A.5.21)

### 6.1 Requisiti NIS2 Art. 21(2)(d)

```
┌─────────────────────────────────────────────────────────────┐
│              CATENA DI FORNITURA SICURA                     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  {{company_name}}                                           │
│        │                                                    │
│        ▼                                                    │
│  ┌─────────────┐                                           │
│  │ FORNITORE   │◄── Contratto, assessment, monitoring      │
│  │  TIER 1     │                                           │
│  └──────┬──────┘                                           │
│         │                                                   │
│         ▼                                                   │
│  ┌─────────────┐                                           │
│  │ FORNITORE   │◄── Visibilità, requisiti flow-down       │
│  │  TIER 2     │                                           │
│  └──────┬──────┘                                           │
│         │                                                   │
│         ▼                                                   │
│  ┌─────────────┐                                           │
│  │ FORNITORE   │◄── Risk awareness                        │
│  │  TIER N     │                                           │
│  └─────────────┘                                           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 6.2 Controlli Supply Chain

| Controllo | Descrizione | Tier Applicabile |
|-----------|-------------|------------------|
| **Software Bill of Materials** | Lista componenti software | 1-2 |
| **Integrity verification** | Hash, firma digitale | 1-2 |
| **Secure development** | SDLC sicuro attestato | 1-2 |
| **Vulnerability disclosure** | Processo coordinato | 1-2 |
| **Update mechanism** | Aggiornamenti sicuri | 1-3 |
| **Subcontractor visibility** | Mappa sub-fornitori | 1 |

### 6.3 Requisiti DORA per ICT Third Parties

**Art. 28 - Principi generali:**
| Requisito | Implementazione |
|-----------|-----------------|
| Strategia rischio ICT terze parti | Politica documentata |
| Registro accordi contrattuali | Database aggiornato |
| Valutazione proporzionata | Risk-based approach |
| Due diligence pre-contratto | Assessment strutturato |

**Art. 30 - Disposizioni contrattuali chiave:**
- Descrizione completa servizi
- Localizzazione dati e processing
- SLA e metriche
- Obblighi di reporting
- Diritti di accesso, ispezione, audit
- Cooperazione con autorità
- Exit e trasferibilità

---

## 7. Servizi Cloud (A.5.23)

### 7.1 Valutazione Cloud Provider

| Criterio | Requisito Minimo | Verifiche |
|----------|------------------|-----------|
| **Certificazioni** | ISO 27001 + SOC 2 Type II | Certificati validi |
| **Data residency** | UE/EEA (primario) | Contratto + verifica tecnica |
| **Encryption** | At rest + in transit | Documentazione tecnica |
| **Access control** | MFA, IAM, audit log | Demo/POC |
| **SLA availability** | 99.9% minimo | Contratto |
| **Incident notification** | 24h max | Contratto |
| **Portabilità dati** | Standard formats | Contratto + test |
| **Exit assistance** | Supporto migrazione | Contratto |

### 7.2 Modello di Responsabilità Cloud

```
                    On-Prem    IaaS      PaaS      SaaS
                    ────────────────────────────────────
Data                Cliente    Cliente   Cliente   Cliente
Applications        Cliente    Cliente   Cliente   Provider
Runtime             Cliente    Cliente   Provider  Provider
Middleware          Cliente    Cliente   Provider  Provider
Operating System    Cliente    Cliente   Provider  Provider
Virtualization      Cliente    Provider  Provider  Provider
Servers             Cliente    Provider  Provider  Provider
Storage             Cliente    Provider  Provider  Provider
Networking          Cliente    Provider  Provider  Provider
Data Center         Cliente    Provider  Provider  Provider
```

### 7.3 Controlli per Servizi Cloud

| Area | Controllo | Responsabile |
|------|-----------|--------------|
| **Identity** | Federation/SSO con IdP aziendale | Cliente |
| **Access** | RBAC, least privilege, MFA | Condiviso |
| **Data** | Classificazione, encryption keys | Cliente |
| **Network** | VPC, security groups, firewall | Condiviso |
| **Monitoring** | Log collection, SIEM integration | Condiviso |
| **Compliance** | Configuration audit | Cliente |
| **Backup** | Strategia, test restore | Condiviso |

### 7.4 Cloud Exit Strategy

| Fase | Attività | Timeline |
|------|----------|----------|
| 1. Pianificazione | Inventario dati, mappatura dipendenze | -90 giorni |
| 2. Preparazione | Setup ambiente destinazione | -60 giorni |
| 3. Migrazione | Export dati, trasferimento, validazione | -30 giorni |
| 4. Validazione | Test funzionali, performance | -14 giorni |
| 5. Cutover | Switch traffico, monitoring | D-Day |
| 6. Cleanup | Verifica cancellazione dati origine | +30 giorni |

---

## 8. Monitoraggio e Review (A.5.22)

### 8.1 Attività di Monitoraggio Continuo

| Attività | Frequenza | Responsabile | Output |
|----------|-----------|--------------|--------|
| Review SLA performance | Mensile | Contract Owner | Report KPI |
| Security scorecard | Trimestrale | Security | Risk score |
| Incident review | Continuo | Security | Trend analysis |
| Compliance check | Semestrale | Compliance | Attestation |
| Full assessment | Annuale (Tier 1-2) | Security | Assessment report |

### 8.2 KPI Fornitori

| KPI | Target | Tier |
|-----|--------|------|
| Uptime servizio | >99.9% | 1 |
| Tempo risposta incidenti | <4h | 1-2 |
| Patch critiche applicate | <7 giorni | 1-2 |
| Security incidents | 0 gravi | All |
| Compliance status | 100% | 1-2 |
| Audit findings aperti | 0 critici | 1-2 |

### 8.3 Supplier Scorecard

| Categoria | Peso | Score | Note |
|-----------|------|-------|------|
| Performance SLA | 30% | /10 | |
| Sicurezza | 25% | /10 | |
| Compliance | 20% | /10 | |
| Comunicazione | 15% | /10 | |
| Innovation | 10% | /10 | |
| **TOTALE** | 100% | **/10** | |

### 8.4 Trigger Review Straordinaria

| Evento | Azione |
|--------|--------|
| Security incident presso fornitore | Assessment immediato |
| Cambio proprietà/management | Due diligence |
| Modifiche significative servizio | Review impatto |
| Breach di terze parti collegato | Assessment catena |
| Nuova normativa applicabile | Gap analysis |
| Downgrade rating fornitore | Risk assessment |

---

## 9. Gestione Modifiche e Cambiamenti

### 9.1 Notifica Modifiche

**Modifiche che richiedono approvazione preventiva:**
- Cambio subappaltatori per servizi critici
- Modifica location processing dati
- Cambio significativo architettura sicurezza
- Modifica personale chiave assegnato
- Variazione scope certificazioni

**Processo approvazione:**
```
┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│  NOTIFICA    │───►│  VALUTAZIONE │───►│ APPROVAZIONE │
│  Fornitore   │    │  Security    │    │ o RIGETTO    │
└──────────────┘    └──────────────┘    └──────────────┘
```

### 9.2 Gestione Subappaltatori

| Requisito | Descrizione |
|-----------|-------------|
| Approvazione | Lista subappaltatori approvata |
| Flow-down | Requisiti sicurezza trasferiti |
| Audit right | Esteso a sub-contractor |
| Responsabilità | Fornitore principale responsabile |
| Notifica | Preavviso cambio subappaltatori |

---

## 10. Incidenti Fornitori

### 10.1 Processo di Notifica

```
┌─────────────────────────────────────────────────────────────┐
│            INCIDENT NOTIFICATION CHAIN                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  FORNITORE ──[24h max]──► ORGANIZZAZIONE                   │
│                                │                            │
│                                ▼                            │
│                          TRIAGE/VALUTAZIONE                │
│                                │                            │
│                    ┌───────────┼───────────┐               │
│                    ▼           ▼           ▼               │
│               Impatto       Impatto     Nessun            │
│               Grave         Limitato    Impatto           │
│                    │           │           │               │
│                    ▼           ▼           ▼               │
│              NIS2/GDPR    Monitoring   Chiusura           │
│              Notifica                                       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### 10.2 Informazioni Richieste dal Fornitore

| Informazione | Timing |
|--------------|--------|
| Descrizione incidente | Immediata |
| Scope e impatto | Entro 24h |
| Root cause | Entro 72h |
| Remediation actions | Entro 72h |
| Timeline completa | Entro 5 giorni |
| Lesson learned | Entro 30 giorni |

### 10.3 Azioni Post-Incidente Fornitore

| Severità Impatto | Azione | Owner |
|------------------|--------|-------|
| Critico | Review contratto, valutare exit | Legal + Security |
| Alto | Assessment straordinario | Security |
| Medio | Remediation plan con follow-up | Contract Owner |
| Basso | Documentare e monitorare | Contract Owner |

---

## 11. Exit Strategy

### 11.1 Scenari di Exit

| Scenario | Trigger | Timeline Target |
|----------|---------|-----------------|
| Fine contratto pianificata | Naturale scadenza | 6-12 mesi |
| Terminazione per causa | Breach, performance | 30-90 giorni |
| Exit strategico | Insourcing, cambio vendor | 6-12 mesi |
| Exit emergenza | Incident grave, compliance | Immediato |

### 11.2 Checklist Exit

- [ ] Inventario completo dati presso fornitore
- [ ] Piano migrazione dati e servizi
- [ ] Test ambiente destinazione
- [ ] Comunicazione stakeholder
- [ ] Esecuzione migrazione
- [ ] Verifica completezza trasferimento
- [ ] Richiesta certificazione cancellazione dati
- [ ] Revoca accessi fornitore
- [ ] Archiviazione documentazione
- [ ] Lesson learned

### 11.3 Certificazione Cancellazione Dati

| Requisito | Descrizione |
|-----------|-------------|
| Standard | NIST SP 800-88 o equivalente |
| Scope | Tutti i supporti (HDD, SSD, backup, cloud) |
| Evidenza | Certificato firmato con seriali |
| Verifica | Attestazione del metodo utilizzato |
| Retention certificato | 10 anni |

---

## 12. Ruoli e Responsabilità

### 12.1 RACI Matrix

| Attività | Business Owner | Security | Legal | Procurement | IT |
|----------|---------------|----------|-------|-------------|-----|
| Identificare esigenza | R | C | I | C | C |
| Valutazione sicurezza | C | R | C | I | C |
| Negoziazione contratto | C | C | R | R | C |
| Approvazione fornitore | A | R | C | C | I |
| Onboarding tecnico | C | R | I | I | R |
| Monitoring continuo | C | R | I | I | C |
| Review periodica | A | R | C | C | C |
| Gestione incidenti | C | R | R | I | C |
| Exit management | A | R | R | C | R |

### 12.2 Responsabilità Specifiche

| Ruolo | Responsabilità |
|-------|----------------|
| **Business Owner** | Sponsor, esigenze business, approvazione finale |
| **Security** | Assessment, requisiti, monitoring, incident |
| **Legal** | Contratti, DPA, compliance normativa |
| **Procurement** | Processo acquisto, negoziazione commerciale |
| **IT** | Integrazione tecnica, supporto operativo |
| **DPO** | Verifica GDPR, DPA review |

---

## 13. Metriche e Reporting

### 13.1 KPI del Programma

| Metrica | Target | Frequenza |
|---------|--------|-----------|
| % fornitori Tier 1-2 con assessment | 100% | Trimestrale |
| % contratti con clausole sicurezza | 100% | Trimestrale |
| Tempo medio onboarding | <30 giorni | Mensile |
| Incident fornitori | 0 gravi | Mensile |
| % review completate on-time | >95% | Trimestrale |
| Fornitori con finding critici aperti | 0 | Mensile |

### 13.2 Dashboard Fornitori

| Fornitore | Tier | Assessment Score | SLA Status | Risk Level | Next Review |
|-----------|------|------------------|------------|------------|-------------|
| {{supplier_name}} | {{supplier_tier}} | {{assessment_score}} | {{sla_status}} | {{risk_level}} | {{next_review_date}} |

---

## 14. Allegati

### Allegato A - Questionario Sicurezza Fornitori

Vedi documento {{company_name}}-QSF-ISMS-001 — Questionario Sicurezza Fornitori

### Allegato B - Template Clausole Contrattuali

Vedi documento {{company_name}}-CLS-ISMS-001 — Template Clausole Contrattuali Sicurezza

### Allegato C - Registro Fornitori

| ID | Fornitore | Categoria | Tier | Owner | Contratto | Assessment | Review |
|----|-----------|-----------|------|-------|-----------|------------|--------|
| | | | | | | | |

### Allegato D - Contatti

| Ruolo | Nome | Email | Telefono |
|-------|------|-------|----------|
| Security Manager | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| Procurement Manager | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| Legal Counsel | {{contact_name}} | {{contact_email}} | {{contact_phone}} |
| DPO | {{contact_name}} | {{contact_email}} | {{contact_phone}} |

---

## 15. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 16. Approvazioni

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{security_officer_title}} | | {{document_date}} |
| Approvato da | {{senior_management}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Codice | Relazione |
|-----------|--------|-----------|
| Politica di Sicurezza delle Informazioni | {{company_name}}-POL-ISMS-001 | Policy madre ISMS |
| Politica di Sicurezza Cloud | {{company_name}}-CLD-ISMS-001 | Fornitori cloud |
| Risk Register | {{company_name}}-REG-ISMS-001 | R-015 Supply Chain Risk |
| Politica Controllo Accessi | {{company_name}}-ACC-ISMS-001 | Accessi fornitori ai sistemi |
| Procedura Gestione Incidenti | {{company_name}}-INC-ISMS-001 | Incidenti coinvolgenti fornitori |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{security_officer_title}}` | Owner e Approvazioni | ☐ |
| 6 | `{{contact_name}}` | Approvazioni e Allegato D — contatti per ruolo | ☐ |
| 7 | Registro Fornitori | Allegato C — tutti i fornitori attivi censiti | ☐ |
| 8 | Tier assegnato | Sezione 3 — ogni fornitore classificato per Tier (1-4) | ☐ |
| 9 | DPA firmato | Sezione 5 — DPA GDPR Art. 28 in archivio per ogni fornitore con dati personali | ☐ |
| 10 | Assessment completato | Sezione 4 — due diligence per ogni Tier 1-2 | ☐ |
| 11 | Clausole contrattuali | Sezione 5 — clausole sicurezza in tutti i contratti attivi | ☐ |

---

*Template conforme a ISO/IEC 27001:2022 Controlli A.5.19-A.5.23*
*Creato con Kynosure.ai*
