---
title: Questionario di Sicurezza Fornitori NIS2
version: '1.0'
date: '{{document_date}}'
classification: Riservato
owner: '{{security_manager}}'
approver: '{{ciso_name}}'
framework: NIS2
nis2_articles:
  - Art. 21(2)(d) - Sicurezza della catena di approvvigionamento
  - >-
    Art. 21(2)(a) - Politiche di analisi dei rischi e sicurezza dei sistemi
    informatici
  - >-
    Art. 21(2)(e) - Sicurezza nell'acquisizione, sviluppo e manutenzione dei
    sistemi
dlgs_138_articles:
  - Art. 24 - Obblighi degli organi di amministrazione e direttivi
  - >-
    Art. 25 - Obblighi in materia di misure di gestione dei rischi per la
    sicurezza informatica
cross_references:
  - document: NIS2 Supply Chain Security
    path: ../supply-chain/nis2-supply-chain-security.md
  - document: NIS2 Risk Management Measures
    path: ../risk/nis2-risk-management-measures.md
  - document: NIS2 Incident Reporting
    path: ../incidents/nis2-incident-reporting.md
  - document: NIS2 Business Continuity Plan
    path: ../continuity/nis2-business-continuity-plan.md
related_documents:
  - nis2-supply-chain-security
  - nis2-risk-management-measures
  - nis2-incident-reporting
  - nis2-business-continuity-plan
  - nis2-governance-accountability
  - nis2-scope-applicability
status: draft
review_frequency: annual
last_review: '{{last_review_date}}'
next_review: '{{next_review_date}}'
subset: true
---

# Questionario di Sicurezza Fornitori NIS2

## 1. Introduzione

### 1.1 Scopo

Questo questionario e lo strumento standard utilizzato da {{organization_name}} per valutare la postura di sicurezza dei fornitori e dei partner della catena di approvvigionamento ai sensi dell'Art. 21(2)(d) della Direttiva (UE) 2022/2555 (NIS2) e dell'Art. 25 del D.Lgs. 138/2024. La compilazione e obbligatoria per tutti i fornitori classificati come Tier 1 o Tier 2 secondo la metodologia di classificazione della supply chain dell'Organizzazione.

### 1.2 Istruzioni per il Fornitore

- Compilare tutti i campi applicabili con risposte dettagliate
- Allegare evidenze documentali ove richiesto
- Se un requisito non e applicabile, indicare "N/A" con motivazione
- Il questionario deve essere compilato dal responsabile sicurezza o equivalente
- Tempo stimato per la compilazione: 2-4 ore
- Restituire entro **15 giorni lavorativi** dalla ricezione

### 1.3 Informazioni Fornitore

| Campo | Valore |
|-------|--------|
| **Ragione sociale** | {{vendor_name}} |
| **Sede legale** | {{vendor_address}} |
| **Paese** | {{vendor_country}} |
| **Partita IVA** | {{vendor_vat}} |
| **Settore** | {{vendor_sector}} |
| **N. dipendenti** | {{vendor_employees}} |
| **Fatturato annuo** | {{vendor_revenue}} |
| **Referente sicurezza** | {{vendor_security_contact}} |
| **Email referente** | {{vendor_security_email}} |
| **Data compilazione** | {{questionnaire_date}} |
| **Compilato da** | {{vendor_respondent}} |
| **Ruolo compilatore** | {{vendor_respondent_role}} |

### 1.4 Servizio/Fornitura

| Campo | Valore |
|-------|--------|
| **Descrizione servizio** | {{service_description}} |
| **Contratto n.** | {{contract_number}} |
| **Classificazione Tier** | [ ] Tier 1 (Critico) [ ] Tier 2 (Importante) [ ] Tier 3 (Standard) |
| **Accesso a sistemi** | [ ] Si — Quali: __________ [ ] No |
| **Accesso a dati** | [ ] Si — Categorie: __________ [ ] No |
| **Connessione rete** | [ ] Si — Tipo: __________ [ ] No |

---

## 2. Governance e Organizzazione (Art. 21(2)(a) NIS2)

| # | Domanda | Risposta | Evidenza |
|---|---------|----------|----------|
| 2.1 | L'organizzazione dispone di un CISO o equivalente? | [ ] Si [ ] No | [ ] Organigramma |
| 2.2 | Esiste una policy di sicurezza delle informazioni approvata dalla direzione? | [ ] Si [ ] No | [ ] Policy |
| 2.3 | La policy e rivista almeno annualmente? | [ ] Si [ ] No | Data ultimo review: _____ |
| 2.4 | L'organizzazione e certificata ISO 27001? | [ ] Si [ ] No | Certificato n.: _____ Scadenza: _____ |
| 2.5 | Il top management e coinvolto nelle decisioni di cybersecurity? | [ ] Si [ ] No | [ ] Verbali |
| 2.6 | Esiste un budget dedicato alla cybersecurity? | [ ] Si [ ] No | % fatturato: _____% |
| 2.7 | L'organizzazione e soggetta alla NIS2? | [ ] Si — Categoria: _____ [ ] No [ ] In valutazione | |
| 2.8 | L'organizzazione ha un programma di compliance normativa per la cybersecurity? | [ ] Si [ ] No | [ ] Piano |

---

## 3. Gestione del Rischio (Art. 21(2)(a) NIS2)

| # | Domanda | Risposta | Evidenza |
|---|---------|----------|----------|
| 3.1 | Viene effettuata una valutazione dei rischi cyber almeno annualmente? | [ ] Si [ ] No | Data ultimo assessment: _____ |
| 3.2 | Quale metodologia di risk assessment viene utilizzata? | [ ] ISO 27005 [ ] NIST [ ] FAIR [ ] Altra: _____ | [ ] Metodologia |
| 3.3 | I rischi sono classificati per probabilita e impatto? | [ ] Si [ ] No | [ ] Risk register |
| 3.4 | Esiste un piano di trattamento dei rischi con owner e scadenze? | [ ] Si [ ] No | [ ] Piano |
| 3.5 | Il risk register include rischi relativi alla supply chain? | [ ] Si [ ] No | |
| 3.6 | I rischi sono rivisti dopo incidenti significativi? | [ ] Si [ ] No | |

---

## 4. Sicurezza Tecnica (Art. 21(2)(a)(e) NIS2)

### 4.1 Controllo Accessi

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 4.1.1 | Autenticazione multi-fattore implementata? | [ ] Si, per tutti [ ] Si, parziale [ ] No | Sistemi coperti: _____ |
| 4.1.2 | Principio least privilege applicato? | [ ] Si [ ] No | |
| 4.1.3 | Review accessi periodica? | [ ] Si [ ] No | Frequenza: _____ |
| 4.1.4 | Gestione utenze privilegiate (PAM)? | [ ] Si [ ] No | Soluzione: _____ |
| 4.1.5 | Processo off-boarding per revoca accessi? | [ ] Si [ ] No | SLA revoca: _____ |

### 4.2 Sicurezza Rete

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 4.2.1 | Segmentazione rete implementata? | [ ] Si [ ] No | |
| 4.2.2 | Firewall con regole documentate? | [ ] Si [ ] No | |
| 4.2.3 | IDS/IPS in produzione? | [ ] Si [ ] No | Soluzione: _____ |
| 4.2.4 | VPN per accesso remoto? | [ ] Si [ ] No | Protocollo: _____ |
| 4.2.5 | Monitoraggio traffico anomalo? | [ ] Si [ ] No | |

### 4.3 Protezione Dati

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 4.3.1 | Cifratura dati at-rest? | [ ] Si [ ] No | Algoritmo: _____ |
| 4.3.2 | Cifratura dati in-transit (TLS 1.2+)? | [ ] Si [ ] No | Protocollo min: _____ |
| 4.3.3 | Classificazione dati implementata? | [ ] Si [ ] No | Livelli: _____ |
| 4.3.4 | DLP (Data Loss Prevention)? | [ ] Si [ ] No | Soluzione: _____ |
| 4.3.5 | Gestione chiavi crittografiche? | [ ] Si [ ] No | HSM: [ ] Si [ ] No |

### 4.4 Sicurezza Applicativa (Art. 21(2)(e))

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 4.4.1 | Secure SDLC implementato? | [ ] Si [ ] No | Framework: _____ |
| 4.4.2 | Code review/SAST? | [ ] Si [ ] No | Tool: _____ |
| 4.4.3 | DAST/penetration test periodici? | [ ] Si [ ] No | Frequenza: _____ Ultimo: _____ |
| 4.4.4 | Gestione vulnerabilita con SLA? | [ ] Si [ ] No | SLA critico: _____ |
| 4.4.5 | SBOM (Software Bill of Materials) disponibile? | [ ] Si [ ] No | Formato: _____ |
| 4.4.6 | Dependency scanning automatico? | [ ] Si [ ] No | |

---

## 5. Gestione Incidenti (Art. 21(2)(b) NIS2)

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 5.1 | Piano di risposta incidenti documentato? | [ ] Si [ ] No | [ ] Piano |
| 5.2 | Team di incident response dedicato (o CSIRT esterno)? | [ ] Si [ ] No | Contatto H24: _____ |
| 5.3 | SLA notifica incidenti al committente? | [ ] Si [ ] No | Ore: _____ |
| 5.4 | Esercitazioni incident response almeno annuali? | [ ] Si [ ] No | Ultima: _____ |
| 5.5 | Capacita di forensic analysis? | [ ] Si, interna [ ] Si, esterna [ ] No | |
| 5.6 | N. incidenti significativi ultimi 12 mesi? | _____ | Descrizione: _____ |
| 5.7 | Notifiche autorita effettuate negli ultimi 24 mesi? | [ ] Si — N.: _____ [ ] No | |

---

## 6. Continuita Operativa (Art. 21(2)(c) NIS2)

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 6.1 | Piano di continuita operativa (BCP)? | [ ] Si [ ] No | [ ] Piano |
| 6.2 | Disaster recovery plan? | [ ] Si [ ] No | [ ] DRP |
| 6.3 | RTO definito per servizi critici? | [ ] Si [ ] No | RTO: _____ |
| 6.4 | RPO definito? | [ ] Si [ ] No | RPO: _____ |
| 6.5 | Backup regolari con test restore? | [ ] Si [ ] No | Frequenza backup: _____ Test: _____ |
| 6.6 | Georidondanza infrastruttura? | [ ] Si [ ] No | Siti: _____ |
| 6.7 | Test BCP/DR almeno annuale? | [ ] Si [ ] No | Ultimo: _____ Risultato: _____ |

---

## 7. Supply Chain del Fornitore (Art. 21(2)(d) NIS2)

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 7.1 | Il fornitore utilizza sub-fornitori per il servizio? | [ ] Si [ ] No | Lista: _____ |
| 7.2 | I sub-fornitori sono valutati per la sicurezza? | [ ] Si [ ] No | Frequenza: _____ |
| 7.3 | Esistono clausole di sicurezza nei contratti con sub-fornitori? | [ ] Si [ ] No | |
| 7.4 | Procedura di notifica per cambio sub-fornitori? | [ ] Si [ ] No | |
| 7.5 | Software supply chain security (SBOM, signing)? | [ ] Si [ ] No | |

---

## 8. Formazione e Awareness (Art. 21(2)(g) NIS2)

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 8.1 | Programma formazione cybersecurity per tutto il personale? | [ ] Si [ ] No | Frequenza: _____ |
| 8.2 | Formazione specifica per ruoli tecnici? | [ ] Si [ ] No | |
| 8.3 | Simulazioni phishing? | [ ] Si [ ] No | Frequenza: _____ Click rate: _____% |
| 8.4 | % personale formato nell'ultimo anno? | _____% | |

---

## 9. Conformita Normativa

| # | Domanda | Risposta | Dettaglio |
|---|---------|----------|-----------|
| 9.1 | Conformita GDPR/privacy? | [ ] Si [ ] No [ ] In corso | DPO nominato: [ ] Si [ ] No |
| 9.2 | Soggetto a regolamentazioni settoriali? | [ ] Si — Quali: _____ [ ] No | |
| 9.3 | Audit di terza parte negli ultimi 24 mesi? | [ ] Si [ ] No | Tipo: _____ Esito: _____ |
| 9.4 | Sanzioni o provvedimenti ricevuti? | [ ] Si — Dettaglio: _____ [ ] No | |
| 9.5 | Assicurazione cyber? | [ ] Si [ ] No | Massimale: _____ |

---

## 10. Requisiti Settoriali Aggiuntivi

### 10.1 Energia (ARERA, IEC 62443)

*Compilare solo se il fornitore opera nel settore energetico o fornisce servizi a entita del settore.*

| # | Domanda | Risposta |
|---|---------|----------|
| 10.1.1 | Conformita IEC 62443 per sistemi OT? | [ ] Si [ ] No [ ] N/A |
| 10.1.2 | Separazione reti IT/OT? | [ ] Si [ ] No [ ] N/A |
| 10.1.3 | Conformita requisiti ARERA? | [ ] Si [ ] No [ ] N/A |

### 10.2 Bancario/Finanziario (DORA, EBA)

*Compilare solo se il fornitore opera nel settore finanziario o e ICT third-party provider.*

| # | Domanda | Risposta |
|---|---------|----------|
| 10.2.1 | Conformita DORA (Reg. 2022/2554)? | [ ] Si [ ] No [ ] In corso [ ] N/A |
| 10.2.2 | TLPT (Threat-Led Penetration Testing) eseguito? | [ ] Si [ ] No [ ] N/A |
| 10.2.3 | Exit strategy documentata per servizi critici? | [ ] Si [ ] No [ ] N/A |
| 10.2.4 | Classificazione come fornitore ICT critico? | [ ] Si [ ] No [ ] In valutazione |

### 10.3 Sanitario (NIS2, MDR)

*Compilare solo se il fornitore opera nel settore sanitario o fornisce dispositivi medici.*

| # | Domanda | Risposta |
|---|---------|----------|
| 10.3.1 | Conformita MDR (Reg. 2017/745) per dispositivi medici? | [ ] Si [ ] No [ ] N/A |
| 10.3.2 | Gestione dati sanitari con misure rafforzate? | [ ] Si [ ] No [ ] N/A |
| 10.3.3 | Conformita standard IHE per interoperabilita? | [ ] Si [ ] No [ ] N/A |

### 10.4 Infrastruttura Digitale (AGCOM)

*Compilare solo se il fornitore fornisce servizi di cloud, DNS, TLD, data center, CDN.*

| # | Domanda | Risposta |
|---|---------|----------|
| 10.4.1 | SLA uptime >= 99.99%? | [ ] Si [ ] No [ ] N/A |
| 10.4.2 | Protezione DDoS? | [ ] Si [ ] No [ ] N/A |
| 10.4.3 | Localizzazione dati UE garantita? | [ ] Si [ ] No [ ] N/A |

---

## 11. Scoring e Valutazione

### 11.1 Metodologia di Scoring

Ogni sezione riceve un punteggio da 1 a 5 in base alla completezza e maturita delle risposte:

| Score | Livello | Descrizione |
|:-----:|:-------:|-------------|
| 5 | Ottimizzato | Processi maturi, miglioramento continuo, certificazioni |
| 4 | Gestito | Processi documentati e misurati, review periodiche |
| 3 | Definito | Processi documentati ma non completamente implementati |
| 2 | Iniziale | Alcuni processi informali, non documentati |
| 1 | Inesistente | Nessun processo o misura in atto |

### 11.2 Score per Area

| Area | Sezione | Peso | Score (1-5) | Ponderato |
|------|---------|:----:|:-----------:|:---------:|
| Governance | 2 | 15% | | |
| Risk Management | 3 | 15% | | |
| Sicurezza Tecnica | 4 | 25% | | |
| Gestione Incidenti | 5 | 15% | | |
| Continuita Operativa | 6 | 10% | | |
| Supply Chain | 7 | 10% | | |
| Formazione | 8 | 5% | | |
| Conformita | 9 | 5% | | |
| **TOTALE** | | 100% | | |

### 11.3 Soglie di Accettazione

| Score | Classificazione | Azione |
|:-----:|:---------------:|--------|
| >= 4.0 | Approvato | Onboarding autorizzato |
| 3.0 - 3.9 | Approvato condizionato | Piano miglioramento entro 90 giorni |
| 2.0 - 2.9 | Non approvato | Remediation richiesta, rivalutazione dopo completamento |
| < 2.0 | Rifiutato | Fornitore non idoneo, cercare alternativa |

### 11.4 Decisione Finale

```
ESITO VALUTAZIONE FORNITORE NIS2

Fornitore: {{vendor_name}}
Classificazione Tier: _____
Score complessivo: _____/5.0

[ ] APPROVATO
[ ] APPROVATO CON CONDIZIONI (vedi piano miglioramento)
[ ] NON APPROVATO — Remediation richiesta
[ ] RIFIUTATO

Condizioni/Note: ____________________________________________

Prossima valutazione: {{next_review_date}}

Valutato da: _________________________  Data: _____________
Approvato da (CISO): _________________________  Data: _____________
```

---

## 12. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{contact_name}} | Prima emissione |

---

## 13. Approvazione

| Ruolo | Nome | Firma | Data |
|-------|------|-------|------|
| Redatto da | {{contact_name}} | | {{document_date}} |
| Verificato da | {{security_manager}} | | {{document_date}} |
| Approvato da | {{ciso_name}} | | {{document_date}} |

---

## Documenti Correlati

| Documento | Riferimento | Relazione |
|-----------|-------------|-----------|
| NIS2 Supply Chain Security | `../supply-chain/nis2-supply-chain-security.md` | Framework supply chain e classificazione tier |
| NIS2 Risk Management Measures | `../risk/nis2-risk-management-measures.md` | Misure di sicurezza Art. 21(2) |
| NIS2 Incident Reporting | `../incidents/nis2-incident-reporting.md` | Requisiti notifica incidenti fornitori |
| NIS2 Business Continuity Plan | `../continuity/nis2-business-continuity-plan.md` | Requisiti continuita supply chain |
| NIS2 Governance | `../governance/nis2-governance-accountability.md` | Responsabilita direzionale supply chain |
| NIS2 Scope | `../context/nis2-scope-applicability.md` | Ambito di applicazione NIS2 |

---

## Checklist di Compilazione

Prima di considerare questo questionario completo, verificare:

- [ ] {{vendor_name}} — Ragione sociale completa del fornitore
- [ ] {{service_description}} — Descrizione del servizio/fornitura
- [ ] {{contract_number}} — Riferimento contrattuale
- [ ] Classificazione Tier assegnata in base a criteri supply chain
- [ ] Sezione 2 — Governance: almeno 8 domande con risposta e evidenze
- [ ] Sezione 3 — Risk management: metodologia e risk register verificati
- [ ] Sezione 4 — Sicurezza tecnica: tutte le sottosezioni compilate (accessi, rete, dati, applicativa)
- [ ] Sezione 5 — Gestione incidenti: SLA notifica definito, storico incidenti dichiarato
- [ ] Sezione 6 — Continuita: RTO/RPO dichiarati, test annuali verificati
- [ ] Sezione 7 — Sub-fornitori identificati e valutati
- [ ] Sezione 8 — % formazione personale dichiarata
- [ ] Sezione 9 — Conformita normativa e storico sanzioni verificato
- [ ] Sezione 10 — Requisiti settoriali compilati (se applicabili)
- [ ] Sezione 11 — Score calcolato, decisione motivata e firmata da CISO

---

*Template conforme a Direttiva (UE) 2022/2555 Art. 21(2)(d), D.Lgs. 138/2024 Art. 25*
