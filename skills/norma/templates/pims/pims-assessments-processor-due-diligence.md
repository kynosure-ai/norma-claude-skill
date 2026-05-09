---
title: Valutazione Due Diligence Responsabili del Trattamento
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: '{{privacy_manager}}'
approver: '{{dpo_title}}'
framework: 'ISO 27701:2019'
iso_clauses:
  - 7.2.6 - Contracts with PII processors
  - 7.5.1 - Identify basis for PII transfer between jurisdictions
  - 8.2.1 - Customer agreement
annex_controls:
  - A.7.2.6 - Contracts with PII processors
  - B.8.2.1 - Customer agreement
gdpr_articles:
  - Art. 28 - Responsabile del trattamento
  - Art. 28(1) - Garanzie sufficienti
  - Art. 28(3) - Contenuto contratto
  - Art. 32 - Sicurezza del trattamento
  - Art. 44-49 - Trasferimenti internazionali
role: controller
cross_references:
  - document: Privacy Policy
    path: ../policies/privacy-policy.md
  - document: RoPA
    path: ../registers/record-of-processing-activities.md
  - document: International Transfer Assessment
    path: ../procedures/international-data-transfer-assessment.md
  - document: Privacy Risk Assessment
    path: ../risk-assessment/privacy-risk-assessment.md
related_documents:
  - privacy-policy
  - record-of-processing-activities
  - international-data-transfer-assessment
  - privacy-risk-assessment
  - pims-internal-audit-programme
  - data-breach-notification-procedure
status: draft
review_frequency: per_engagement
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# Valutazione Due Diligence Responsabili del Trattamento

## 1. Informazioni Generali

### 1.1 Scopo

Questa valutazione verifica che il Responsabile del trattamento (Processor) offra "garanzie sufficienti per mettere in atto misure tecniche e organizzative adeguate" ai sensi dell'Art. 28(1) GDPR e della clausola 7.2.6 ISO 27701. La due diligence deve essere completata **prima** dell'affidamento del trattamento e ripetuta periodicamente in base alla classificazione di rischio del fornitore.

### 1.2 Informazioni Fornitore

| Campo | Valore |
|-------|--------|
| **Ragione sociale** | {{processor_name}} |
| **Sede legale** | {{processor_address}} |
| **Paese** | {{processor_country}} |
| **Partita IVA** | {{processor_vat}} |
| **Referente privacy** | {{processor_privacy_contact}} |
| **Email referente** | {{processor_privacy_email}} |
| **Sito web** | {{processor_website}} |
| **Data valutazione** | {{assessment_date}} |
| **Valutatore** | {{assessor_name}} |

### 1.3 Informazioni sul Trattamento

| Campo | Valore |
|-------|--------|
| **Servizio/Contratto** | {{service_description}} |
| **Categorie di dati** | {{data_categories}} |
| **Categorie di interessati** | {{data_subject_categories}} |
| **Dati particolari (Art. 9)** | [ ] Si — Categorie: __________ [ ] No |
| **Volume stimato interessati** | {{data_volume}} |
| **Durata trattamento** | {{processing_duration}} |
| **Trasferimento extra-UE** | [ ] Si — Paese: __________ [ ] No |

---

## 2. Classificazione Rischio Fornitore

### 2.1 Criteri di Classificazione

| Criterio | Peso | Punteggio (1-5) | Ponderato |
|----------|:----:|:---------------:|:---------:|
| Volume dati trattati | 20% | | |
| Categorie dati (ordinari vs particolari) | 25% | | |
| Criticita per il business | 15% | | |
| Paese del trattamento (adeguatezza) | 15% | | |
| Sub-processor coinvolti | 10% | | |
| Storico incidenti/breach | 15% | | |
| **TOTALE PONDERATO** | 100% | | |

**Scala punteggio**:
- 1 = Rischio minimo (es. pochi dati, solo UE, no dati particolari)
- 2 = Rischio basso
- 3 = Rischio medio
- 4 = Rischio alto
- 5 = Rischio critico (es. dati sanitari, volume elevato, paese terzo senza adeguatezza)

### 2.2 Classificazione e Frequenza Review

| Score Ponderato | Classificazione | Frequenza Due Diligence | Audit On-site |
|:---------------:|:---------------:|:-----------------------:|:-------------:|
| 1.0 - 2.0 | Basso | Ogni 36 mesi | No |
| 2.1 - 3.0 | Medio | Ogni 24 mesi | Facoltativo |
| 3.1 - 4.0 | Alto | Ogni 12 mesi | Si (remoto o on-site) |
| 4.1 - 5.0 | Critico | Ogni 6 mesi | Si (on-site obbligatorio) |

**Classificazione risultante**: [ ] Basso [ ] Medio [ ] Alto [ ] Critico

---

## 3. Valutazione Organizzativa

### 3.1 Governance Privacy

| # | Requisito | Evidenza | Conforme | Note |
|---|-----------|----------|:--------:|------|
| 3.1.1 | DPO o referente privacy nominato | [ ] Nomina [ ] Contatto | [ ] Si [ ] No [ ] Parziale | |
| 3.1.2 | Policy privacy documentata | [ ] Documento [ ] Link | [ ] Si [ ] No [ ] Parziale | |
| 3.1.3 | Registro trattamenti (Art. 30(2)) | [ ] Estratto | [ ] Si [ ] No [ ] Parziale | |
| 3.1.4 | Formazione privacy al personale | [ ] Piano [ ] Attestati | [ ] Si [ ] No [ ] Parziale | |
| 3.1.5 | Procedura data breach | [ ] Documento | [ ] Si [ ] No [ ] Parziale | |
| 3.1.6 | Procedura gestione diritti interessati | [ ] Documento | [ ] Si [ ] No [ ] Parziale | |

### 3.2 Certificazioni e Attestazioni

| Certificazione | Posseduta | Organismo | Scadenza | Evidenza |
|----------------|:---------:|-----------|----------|----------|
| ISO 27001 | [ ] Si [ ] No | | | |
| ISO 27701 | [ ] Si [ ] No | | | |
| SOC 2 Type II | [ ] Si [ ] No | | | |
| CSA STAR | [ ] Si [ ] No | | | |
| ISAE 3402 | [ ] Si [ ] No | | | |
| Altre: _________ | [ ] Si [ ] No | | | |

### 3.3 Assicurazione

| Tipo | Massimale | Compagnia | Scadenza |
|------|-----------|-----------|----------|
| Cyber Insurance | {{cyber_insurance_amount}} | | |
| RC Professionale | {{professional_liability_amount}} | | |

---

## 4. Valutazione Tecnica (Art. 32 GDPR)

### 4.1 Misure di Sicurezza

| # | Misura (Art. 32) | Implementata | Dettaglio |
|---|------------------|:------------:|-----------|
| **Cifratura** | | | |
| 4.1.1 | Cifratura dati at-rest | [ ] Si [ ] No | Algoritmo: _________ |
| 4.1.2 | Cifratura dati in-transit (TLS 1.2+) | [ ] Si [ ] No | Protocollo: _________ |
| 4.1.3 | Gestione chiavi crittografiche | [ ] Si [ ] No | HSM: [ ] Si [ ] No |
| **Controllo Accessi** | | | |
| 4.1.4 | Autenticazione multi-fattore | [ ] Si [ ] No | Tipo: _________ |
| 4.1.5 | Principio least privilege | [ ] Si [ ] No | |
| 4.1.6 | Review accessi periodica | [ ] Si [ ] No | Frequenza: _________ |
| 4.1.7 | Segregazione ambienti (prod/test) | [ ] Si [ ] No | |
| **Logging e Monitoraggio** | | | |
| 4.1.8 | Log accessi ai dati | [ ] Si [ ] No | Retention: _________ |
| 4.1.9 | Monitoraggio anomalie | [ ] Si [ ] No | SIEM: [ ] Si [ ] No |
| 4.1.10 | Alerting automatico | [ ] Si [ ] No | |
| **Continuita** | | | |
| 4.1.11 | Backup regolari | [ ] Si [ ] No | Frequenza: _________ |
| 4.1.12 | Test restore | [ ] Si [ ] No | Frequenza: _________ |
| 4.1.13 | Piano disaster recovery | [ ] Si [ ] No | RTO: _____ RPO: _____ |
| **Sicurezza Applicativa** | | | |
| 4.1.14 | Vulnerability assessment periodico | [ ] Si [ ] No | Frequenza: _________ |
| 4.1.15 | Penetration test | [ ] Si [ ] No | Ultimo: _________ |
| 4.1.16 | Patch management | [ ] Si [ ] No | SLA critico: _________ |

### 4.2 Localizzazione Dati

| Tipo di Dato | Data Center | Paese | Provider Infra | Adeguatezza |
|--------------|-------------|-------|----------------|:-----------:|
| Dati in produzione | | | | [ ] Si [ ] No |
| Backup | | | | [ ] Si [ ] No |
| Log | | | | [ ] Si [ ] No |
| Dati di test | | | | [ ] Si [ ] No |

---

## 5. Valutazione Contrattuale (Art. 28(3) GDPR)

### 5.1 Clausole DPA Obbligatorie

| # | Requisito Art. 28(3) | Presente nel DPA | Conforme | Note |
|---|---------------------|:----------------:|:--------:|------|
| 5.1.1 | Oggetto e durata del trattamento | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.2 | Natura e finalita del trattamento | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.3 | Tipo di dati personali | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.4 | Categorie di interessati | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.5 | Trattamento solo su istruzioni documentate (Art. 28(3)(a)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.6 | Obbligo riservatezza personale (Art. 28(3)(b)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.7 | Misure sicurezza Art. 32 (Art. 28(3)(c)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.8 | Condizioni sub-processor (Art. 28(3)(d)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.9 | Assistenza diritti interessati (Art. 28(3)(e)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.10 | Assistenza obblighi Art. 32-36 (Art. 28(3)(f)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.11 | Cancellazione/restituzione dati a fine contratto (Art. 28(3)(g)) | [ ] Si [ ] No | [ ] Si [ ] No | |
| 5.1.12 | Audit e ispezioni (Art. 28(3)(h)) | [ ] Si [ ] No | [ ] Si [ ] No | |

### 5.2 Sub-Processor

| Sub-Processor | Servizio | Paese | DPA in essere | Autorizzazione |
|---------------|----------|-------|:-------------:|:--------------:|
| {{sub_processor_1}} | | | [ ] Si [ ] No | Generale / Specifica |
| {{sub_processor_2}} | | | [ ] Si [ ] No | Generale / Specifica |

**Procedura notifica nuovi sub-processor**: [ ] Prevista nel DPA [ ] Non prevista

**Diritto di opposizione**: [ ] Previsto [ ] Non previsto

---

## 6. Valutazione Trasferimenti Internazionali

*Compilare solo se il Processor trasferisce dati fuori dallo Spazio Economico Europeo.*

### 6.1 Meccanismo di Trasferimento

| Paese Destinazione | Base Giuridica | Evidenza |
|--------------------|----------------|----------|
| {{transfer_country}} | [ ] Adeguatezza (Art. 45) [ ] SCC (Art. 46) [ ] BCR [ ] Deroghe (Art. 49) | |

### 6.2 Transfer Impact Assessment (TIA)

| Aspetto | Valutazione |
|---------|-------------|
| Legislazione paese terzo (accesso governativo) | {{tia_legislation}} |
| Misure supplementari implementate | {{tia_supplementary_measures}} |
| Valutazione rischio residuo | [ ] Accettabile [ ] Non accettabile |

---

## 7. Riepilogo Valutazione

### 7.1 Score per Area

| Area | Score (1-5) | Peso | Ponderato |
|------|:-----------:|:----:|:---------:|
| Governance Privacy (Sez. 3) | | 25% | |
| Sicurezza Tecnica (Sez. 4) | | 30% | |
| Conformita Contrattuale (Sez. 5) | | 25% | |
| Trasferimenti (Sez. 6) | | 20% | |
| **TOTALE** | | 100% | |

### 7.2 Scala di Valutazione

| Score | Valutazione | Azione |
|:-----:|:----------:|--------|
| >= 4.0 | Eccellente | Approvazione immediata |
| 3.0 - 3.9 | Buono | Approvazione con monitoraggio |
| 2.0 - 2.9 | Sufficiente | Approvazione condizionata a piano miglioramento |
| 1.0 - 1.9 | Insufficiente | Non approvare, richiedere remediation prima dell'ingaggio |

### 7.3 Non Conformita Identificate

| # | Area | NC | Severita | Azione Richiesta | Scadenza |
|---|------|----|:--------:|------------------|----------|
| 1 | | | [ ] Critica [ ] Maggiore [ ] Minore | | |
| 2 | | | [ ] Critica [ ] Maggiore [ ] Minore | | |
| 3 | | | [ ] Critica [ ] Maggiore [ ] Minore | | |

### 7.4 Decisione

```
ESITO VALUTAZIONE DUE DILIGENCE

Fornitore: {{processor_name}}
Servizio: {{service_description}}
Score: _____/5.0

[ ] APPROVATO — Il Processor soddisfa i requisiti Art. 28(1) GDPR
[ ] APPROVATO CON CONDIZIONI — Piano miglioramento richiesto (allegato)
[ ] NON APPROVATO — Garanzie insufficienti, engagement non autorizzato
[ ] IN ATTESA — Informazioni aggiuntive richieste al Processor

Motivazione: ____________________________________________

Prossima revisione: {{next_review_date}}

Valutatore: _________________________  Data: _____________
DPO: _________________________  Data: _____________
Privacy Manager: _________________________  Data: _____________
```

---

## 8. Piano di Monitoraggio

### 8.1 Monitoraggio Continuativo

| Attivita | Frequenza | Responsabile |
|----------|-----------|--------------|
| Verifica certificazioni attive | Annuale | Privacy Team |
| Review report SOC2/audit | Alla ricezione | Privacy Manager |
| Verifica sub-processor | Ad ogni notifica + semestrale | Privacy Team |
| Verifica data breach processor | Trimestrale | Privacy Manager |
| Review SLA sicurezza | Semestrale | IT Security |
| Audit on-site (se classificazione Alta/Critica) | Annuale | Internal Audit |

### 8.2 Trigger per Revisione Straordinaria

La due diligence deve essere ripetuta immediatamente in caso di:
- Data breach che coinvolge dati del Titolare
- Cambio significativo nel servizio o nel trattamento
- Cambio sede/paese del trattamento
- Acquisizione o cambio di proprieta del Processor
- Perdita di certificazioni (es. ISO 27001, SOC2)
- Reclamo da parte di interessati verso il Processor
- Modifica normativa significativa nel paese del Processor

---

## 9. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{contact_name}} | Prima emissione |

---

## 10. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Valutato da | {{assessor_name}} | | {{assessment_date}} |
| Verificato da | {{privacy_manager}} | | {{document_date}} |
| Approvato da | {{dpo_title}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Riferimento | Relazione |
|-----------|-------------|-----------|
| Privacy Policy | `../policies/privacy-policy.md` | Informativa sui destinatari dei dati |
| RoPA | `../registers/record-of-processing-activities.md` | Registro trattamenti affidati a processor |
| International Transfer Assessment | `../procedures/international-data-transfer-assessment.md` | TIA per trasferimenti extra-UE |
| Privacy Risk Assessment | `../risk-assessment/privacy-risk-assessment.md` | Rischi derivanti da affidamento a terzi |
| PIMS Internal Audit Programme | `../audit/pims-internal-audit-programme.md` | Piano audit fornitori |
| Data Breach Notification | `../procedures/data-breach-notification-procedure.md` | Procedura notifica breach da processor |

---

## Checklist di Compilazione

Prima di considerare questa valutazione completa, verificare di aver compilato:

- [ ] {{processor_name}} — Ragione sociale completa del Processor
- [ ] {{processor_country}} — Paese sede legale
- [ ] {{service_description}} — Descrizione servizio affidato
- [ ] {{data_categories}} — Categorie dati trattati (ordinari/particolari)
- [ ] {{data_volume}} — Volume stimato interessati coinvolti
- [ ] Sezione 2 — Classificazione rischio con score ponderato
- [ ] Sezione 3 — Valutazione organizzativa: governance, certificazioni, assicurazione
- [ ] Sezione 4 — Valutazione tecnica: cifratura, accessi, logging, continuita, VA/PT
- [ ] Sezione 5 — Verifica tutte le 12 clausole obbligatorie Art. 28(3) nel DPA
- [ ] Sezione 5.2 — Lista sub-processor completa con DPA e autorizzazione
- [ ] Sezione 6 — TIA se trasferimento extra-UE (legislazione, misure supplementari)
- [ ] Sezione 7 — Score finale per area e decisione motivata
- [ ] Sezione 8 — Piano monitoraggio con frequenza basata su classificazione rischio
- [ ] Firme — Valutatore, Privacy Manager e DPO

---

*Template conforme a ISO/IEC 27701:2019 (7.2.6, 7.5.1, 8.2.1), GDPR Art. 28*
