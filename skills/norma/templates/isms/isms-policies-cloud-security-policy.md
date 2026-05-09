---
title: Politica di Sicurezza del Cloud
version: '1.0'
date: '{{document_date}}'
classification: Interno
owner: '{{security_officer_title}}'
approver: '{{senior_management}}'
framework: ISO27001
language: IT
documentType: policy
iso_controls:
  - A.5.23 - Sicurezza delle informazioni per l'uso dei servizi cloud
  - A.5.19 - Sicurezza delle informazioni nelle relazioni con i fornitori
  - >-
    A.5.21 - Gestione della sicurezza delle informazioni nella catena di
    fornitura ICT
  - A.8.11 - Mascheramento dei dati
  - A.8.24 - Uso della crittografia
  - A.8.25 - Ciclo di vita dello sviluppo sicuro
cross_references:
  - NIS2 Art. 21(2)(d) - Sicurezza della catena di approvvigionamento
  - 'NIS2 Art. 21(2)(e) - Sicurezza acquisizione, sviluppo e manutenzione'
  - DORA Art. 28-30 - Gestione rischi derivanti da terze parti ICT
  - GDPR Art. 28 - Responsabile del trattamento
  - GDPR Art. 44-49 - Trasferimenti dati extra-UE
status: Da approvare
subset: true
---

# Politica di Sicurezza del Cloud

## 1. Scopo e Obiettivi

### 1.1 Scopo

{{company_name}} adotta servizi cloud per supportare l'operatività aziendale, beneficiando di scalabilità, resilienza e innovazione. L'adozione del cloud introduce tuttavia rischi specifici legati alla condivisione dell'infrastruttura, alla residenza dei dati, alla dipendenza dal provider e alla complessità della gestione degli accessi. La presente Politica stabilisce i principi, i requisiti e i controlli di sicurezza che l'Organizzazione applica all'intero ciclo di vita dei servizi cloud, dall'approvazione iniziale alla dismissione.

La Politica si applica a tutti i modelli di servizio cloud utilizzati dall'Organizzazione, inclusi Infrastructure as a Service (IaaS), Platform as a Service (PaaS), Software as a Service (SaaS) e Function as a Service (FaaS/Serverless). Si applica inoltre ai cloud pubblici, privati e ibridi, indipendentemente dal provider.

### 1.2 Obiettivi

La Politica persegue la protezione dei dati aziendali e personali archiviati, elaborati o trasmessi attraverso servizi cloud. Garantisce la conformità ai requisiti normativi in materia di residenza dei dati e trasferimenti internazionali, con particolare attenzione al GDPR e alla Direttiva NIS2. Definisce il modello di responsabilità condivisa tra l'Organizzazione e i provider cloud. Assicura la disponibilità di strategie di uscita (exit strategy) che prevengano il lock-in tecnologico. Stabilisce requisiti minimi di sicurezza per la selezione, la configurazione e il monitoraggio dei servizi cloud.

---

## 2. Ambito di Applicazione

### 2.1 Soggetti

La presente Politica si applica a tutto il personale che utilizza, configura, amministra o approva servizi cloud per conto dell'Organizzazione, inclusi dipendenti, collaboratori, amministratori IT, sviluppatori e fornitori con accesso agli ambienti cloud aziendali.

### 2.2 Servizi Cloud Coperti

| Modello | Descrizione | Responsabilità Sicurezza (Organizzazione) | Esempi |
|---------|-------------|-------------------------------------------|--------|
| **IaaS** | Infrastruttura virtualizzata | OS, runtime, applicazioni, dati, configurazioni di rete | AWS EC2, Azure VMs, GCP Compute Engine |
| **PaaS** | Piattaforme di sviluppo gestite | Applicazioni, dati, configurazione piattaforma | AWS RDS, Azure App Service, GCP Cloud Run |
| **SaaS** | Applicazioni complete | Configurazione, utenti, dati | Microsoft 365, Salesforce, Google Workspace |
| **FaaS** | Funzioni serverless | Codice, configurazione trigger, secrets | AWS Lambda, Azure Functions, GCP Cloud Functions |

---

## 3. Modello di Responsabilità Condivisa

### 3.1 Principio Fondamentale

La sicurezza nel cloud opera secondo un modello di responsabilità condivisa: il provider è responsabile della sicurezza del cloud (infrastruttura fisica, rete, hypervisor), mentre l'Organizzazione è responsabile della sicurezza nel cloud (dati, configurazioni, identità, applicazioni).

### 3.2 Matrice di Responsabilità

| Ambito | IaaS | PaaS | SaaS | FaaS |
|--------|------|------|------|------|
| Infrastruttura fisica | Provider | Provider | Provider | Provider |
| Rete fisica | Provider | Provider | Provider | Provider |
| Hypervisor | Provider | Provider | Provider | Provider |
| Sistema operativo | **Organizzazione** | Provider | Provider | Provider |
| Runtime e middleware | **Organizzazione** | Condivisa | Provider | Provider |
| Applicazione | **Organizzazione** | **Organizzazione** | Provider | **Organizzazione** |
| Dati | **Organizzazione** | **Organizzazione** | **Organizzazione** | **Organizzazione** |
| Identity & Access | **Organizzazione** | **Organizzazione** | **Organizzazione** | **Organizzazione** |
| Configurazione sicurezza | **Organizzazione** | **Organizzazione** | **Organizzazione** | **Organizzazione** |
| Cifratura dati | **Organizzazione** | Condivisa | Condivisa | **Organizzazione** |

---

## 4. Approvazione e Governance dei Servizi Cloud

### 4.1 Processo di Approvazione

Nessun servizio cloud può essere utilizzato per dati o processi aziendali senza approvazione formale. Il processo di approvazione segue gli step definiti nella Politica di Uso Accettabile (Sezione 7.2 — Shadow IT e Approvazione SaaS) e include una valutazione specifica per i rischi cloud.

### 4.2 Valutazione Rischi Cloud

Prima dell'approvazione, ogni servizio cloud deve essere sottoposto a una valutazione che copra i seguenti aspetti:

| Area di Valutazione | Criteri | Evidenza Richiesta |
|---------------------|---------|--------------------|
| Certificazioni provider | ISO 27001, SOC 2 Type II, C5 (per Germania), CSA STAR | Certificato valido |
| Residenza dati | Data center nell'Unione Europea | Documentazione provider |
| Cifratura | At-rest AES-256, in-transit TLS 1.3, opzione CMEK | Documentazione tecnica |
| Accesso e autenticazione | SSO/SAML, MFA, RBAC | Documentazione tecnica |
| Logging e audit | Log di accesso, log di amministrazione, retention >= 90 giorni | Documentazione tecnica |
| Portabilità dati | API per export, formati standard, nessun lock-in proprietario | Documentazione API |
| SLA disponibilità | >= 99.9% per servizi critici, >= 99.5% per non critici | Contratto SLA |
| Incident notification | Notifica breach entro 72 ore, comunicazione outage proattiva | Clausola contrattuale |
| Sub-processori | Lista pubblica e aggiornata, notifica cambio sub-processori | DPA e lista sub-processori |
| Exit strategy | Periodo transizione >= 90 giorni, assistenza migrazione, cancellazione certificata | Clausola contrattuale |

### 4.3 Classificazione dei Servizi Cloud

| Classe | Dati Trattati | Requisiti Aggiuntivi |
|--------|---------------|----------------------|
| **Cloud Tier 1 — Critico** | C3/C4, dati personali sensibili, processi core business | ISO 27001 obbligatoria, CMEK, audit diritto annuale, DR multi-region |
| **Cloud Tier 2 — Importante** | C2, dati personali ordinari, processi di supporto | SOC 2 obbligatoria, SSO, backup verificati |
| **Cloud Tier 3 — Standard** | C1, dati non sensibili, strumenti interni | Cifratura in transit, autenticazione sicura |

---

## 5. Requisiti di Sicurezza

### 5.1 Identity and Access Management

L'Organizzazione implementa i seguenti requisiti per la gestione delle identità e degli accessi negli ambienti cloud:

| Requisito | Dettaglio |
|-----------|-----------|
| Single Sign-On (SSO) | Obbligatorio per tutti i servizi Cloud Tier 1 e Tier 2; l'identity provider aziendale è la fonte autoritativa |
| Multi-Factor Authentication (MFA) | Obbligatorio per tutti gli accessi amministrativi e per gli accessi a dati C3/C4; MFA resistente a phishing (FIDO2/WebAuthn) per account privilegiati |
| Principio del minimo privilegio | Ogni account riceve esclusivamente i permessi necessari per la propria funzione; nessun account con privilegi amministrativi per uso quotidiano |
| Account di servizio | Nessun account di servizio con credenziali statiche a lunga durata; preferire identity federation, workload identity o chiavi a rotazione automatica |
| Review accessi | Review trimestrale degli accessi per servizi Tier 1, semestrale per Tier 2 |
| Account break-glass | Account di emergenza con MFA hardware, monitorato, utilizzabile solo in caso di indisponibilità del sistema IAM primario |

### 5.2 Protezione dei Dati

| Requisito | Dettaglio |
|-----------|-----------|
| Cifratura at-rest | AES-256 minimo; CMEK (Customer-Managed Encryption Keys) obbligatoria per dati C3/C4 |
| Cifratura in-transit | TLS 1.3 (o TLS 1.2 con cipher suite sicure) per tutte le comunicazioni |
| Residenza dati | I dati di {{company_name}} devono risiedere esclusivamente in data center nell'Unione Europea, salvo adeguatezza riconosciuta dalla Commissione Europea |
| Classificazione | I dati archiviati nel cloud mantengono la classificazione definita nella Policy di Classificazione Dati (C1–C4) |
| Backup | Backup dei dati critici gestiti dall'Organizzazione, indipendenti dal backup nativo del provider, con test di restore semestrali |
| Data Loss Prevention | DLP attivo per servizi che trattano dati C3/C4, con policy di blocco per trasferimenti non autorizzati |

### 5.3 Configurazione Sicura

L'Organizzazione adotta il principio di secure-by-default per tutte le configurazioni cloud:

| Area | Requisito |
|------|-----------|
| Rete | Nessuna risorsa esposta pubblicamente salvo esplicita approvazione; default deny per firewall e security group; VPC/VNet isolate per ambiente (prod/staging/dev) |
| Storage | Nessun bucket/blob accessibile pubblicamente per dati aziendali; versioning abilitato per dati critici; lifecycle policy per archiviazione e cancellazione |
| Logging | Cloud Audit Logs abilitati su tutti i servizi; log centralizzati e inoltrati al SIEM aziendale; retention minima 90 giorni operativi, 1 anno archivio |
| Secrets | Nessun secret nel codice sorgente; utilizzo obbligatorio di Secret Manager o Vault; rotazione automatica per chiavi API e service account |
| Infrastructure as Code | Tutte le configurazioni cloud gestite tramite IaC (Terraform, Pulumi, CloudFormation); nessuna modifica manuale in produzione |
| Scansione | Scansione vulnerabilità automatica per container e immagini VM; policy di non-deploy per vulnerabilità critiche |

### 5.4 Monitoraggio e Incident Response

| Attività | Frequenza | Responsabile |
|----------|-----------|--------------|
| Review alert di sicurezza cloud | Giornaliera | IT Security |
| Scansione posture management (CSPM) | Settimanale | IT Security |
| Verifica compliance configurazioni | Mensile | IT Security |
| Review accessi privilegiati | Trimestrale | IT Security + IT Manager |
| Incident response cloud | On demand | IRT + provider (se necessario) |

---

## 6. Gestione dei Fornitori Cloud

### 6.1 Due Diligence

Prima della contrattualizzazione, il provider cloud deve essere sottoposto a una due diligence che includa la verifica delle certificazioni di sicurezza, la revisione del DPA (Data Processing Agreement), l'analisi della catena di sub-processori e la valutazione della stabilità finanziaria del provider.

### 6.2 Clausole Contrattuali Obbligatorie

| Clausola | Requisito |
|----------|-----------|
| DPA conforme GDPR Art. 28 | Firmato prima del trasferimento dati |
| SLA disponibilità | >= 99.9% per servizi critici, penali in caso di mancato rispetto |
| Notifica breach | Entro 72 ore, con dettaglio su dati coinvolti e azioni intraprese |
| Diritto di audit | Possibilità di audit diretto o tramite terza parte indipendente |
| Portabilità dati | Export completo in formato standard entro 30 giorni dalla richiesta |
| Cancellazione dati | Cancellazione certificata entro 90 giorni dalla cessazione contratto |
| Periodo di transizione | Minimo 90 giorni di assistenza alla migrazione |
| Sub-processori | Notifica preventiva di 30 giorni per cambio sub-processori, diritto di opposizione |

### 6.3 Monitoraggio Continuo Provider

| Attività | Frequenza | Responsabile |
|----------|-----------|--------------|
| Verifica stato certificazioni | Annuale | IT Security |
| Review performance SLA | Mensile | IT Manager |
| Review sicurezza e incidenti provider | Trimestrale | IT Security |
| Assessment completo fornitore | Annuale | Procurement + IT Security |

---

## 7. Exit Strategy

### 7.1 Principio

L'Organizzazione mantiene una exit strategy documentata e testata per ogni servizio cloud Tier 1 e Tier 2, al fine di prevenire il vendor lock-in e garantire la continuità operativa in caso di cessazione del rapporto con il provider.

### 7.2 Requisiti Exit Strategy

| Elemento | Requisito |
|----------|-----------|
| Backup indipendente | Copia dei dati critici su infrastruttura non dipendente dal provider |
| Formato dati | Dati esportabili in formato standard e documentato |
| Test portabilità | Test annuale di export/import dei dati su piattaforma alternativa |
| Alternativa identificata | Per ogni servizio Tier 1, identificato almeno un provider alternativo |
| Piano di migrazione | Runbook di migrazione documentato con tempi stimati |
| Competenze | Personale formato sulla piattaforma alternativa (almeno a livello base) |

---

## 8. Conformità Normativa

### 8.1 GDPR

Il trasferimento di dati personali verso servizi cloud richiede la verifica della base legale per il trasferimento (decisione di adeguatezza, Standard Contractual Clauses, o deroga specifica), la stipula di un DPA conforme all'Art. 28, l'aggiornamento del Registro dei Trattamenti (RoPA) e l'esecuzione di una DPIA per trattamenti ad alto rischio.

### 8.2 NIS2

Per le entità soggette alla Direttiva NIS2, l'utilizzo di servizi cloud deve rispettare i requisiti di sicurezza della catena di approvvigionamento (Art. 21.2.d) e le misure di gestione dei rischi (Art. 21.2.e). L'Organizzazione documenta la dipendenza da provider cloud nel proprio assessment dei rischi e include i servizi cloud nei test di resilienza operativa.

### 8.3 DORA (se applicabile)

Per le entità finanziarie soggette al Regolamento DORA, i provider cloud che forniscono funzioni critiche o importanti sono soggetti ai requisiti degli Articoli 28-30, inclusi il registro delle informazioni, la valutazione dei rischi di concentrazione e la segnalazione degli accordi contrattuali alle autorità di vigilanza.

---

## 9. Aggiornamenti e Deroghe

La presente Politica è soggetta a revisione annuale o in caso di cambiamenti significativi nell'utilizzo dei servizi cloud, nella normativa applicabile o nel panorama delle minacce. Le richieste di deroga seguono il processo definito nella Politica di Sicurezza delle Informazioni e devono essere approvate dal {{security_officer_title}} con documentazione del rischio residuo accettato.

---

## 10. Storico Revisioni

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

## 11. Approvazioni

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
| Politica di Uso Accettabile | {{company_name}}-AUP-ISMS-001 | Approvazione SaaS e Shadow IT |
| Inventario degli Asset | {{company_name}}-INV-ISMS-001 | Asset cloud (SRV-001a/b/c/d) |
| Risk Register | {{company_name}}-REG-ISMS-001 | R-009 Cloud Outage, R-015 Supply Chain |
| Politica Controllo Accessi | {{company_name}}-ACC-ISMS-001 | IAM e MFA |
| Procedura Backup e Recovery | {{company_name}}-BKP-ISMS-001 | Backup dati cloud |
| Politica Gestione Fornitori | {{company_name}}-SUP-ISMS-001 | Due diligence fornitori |

---

## Checklist di Compilazione

| # | Placeholder | Sezione | Stato |
|---|-------------|---------|-------|
| 1 | `{{company_name}}` | Globale — denominazione Organizzazione | ☐ |
| 2 | `{{document_date}}` | Globale — data emissione | ☐ |
| 3 | `{{document_author}}` | Storico revisioni | ☐ |
| 4 | `{{senior_management}}` | Approvazioni | ☐ |
| 5 | `{{security_officer_title}}` | Owner e Approvazioni | ☐ |
| 6 | `{{contact_name}}` | Approvazioni — Redatto da | ☐ |
| 7 | Inventario servizi cloud | Sezione 4.3 — tutti i servizi cloud in uso classificati per Tier | ☐ |
| 8 | Valutazione rischi per servizio | Sezione 4.2 — una valutazione per ciascun servizio Tier 1/2 | ☐ |
| 9 | DPA firmato per ogni provider | Sezione 6.2 — DPA in archivio | ☐ |
| 10 | Exit strategy per Tier 1/2 | Sezione 7 — piano documentato per ogni servizio critico | ☐ |
| 11 | Alternativa identificata | Sezione 7.2 — provider alternativo per ogni Tier 1 | ☐ |
| 12 | Identity provider configurato | Sezione 5.1 — SSO attivo per Tier 1 e 2 | ☐ |

---

*Template conforme a ISO/IEC 27001:2022 Controllo A.5.23*
*Creato con Kynosure.ai*
