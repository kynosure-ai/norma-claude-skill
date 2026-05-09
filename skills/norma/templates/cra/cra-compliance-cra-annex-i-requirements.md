---
title: CRA Annex I - Essential Cybersecurity Requirements
version: '1.1'
date: '{{document_date}}'
classification: Interno
owner: Responsabile Product Security
approver: CISO
framework: CRA
language: IT
documentType: checklist
regulation_articles:
  - Regolamento (UE) 2024/2847 - Cyber Resilience Act
  - Annex I Part I - Requisiti sicurezza proprietà dei prodotti
  - Annex I Part II - Requisiti gestione vulnerabilità
cross_references:
  - 'ISO/IEC 27001:2022 - Sistema di gestione sicurezza informazioni'
  - IEC 62443-4-2 - Component security requirements
  - ETSI EN 303 645 - Consumer IoT security
  - OWASP ASVS 4.0 - Application Security Verification Standard
status: Bozza
subset: true
---

# CRA Annex I - Essential Cybersecurity Requirements

## 1. Scopo e Contesto

Il presente documento fornisce una mappatura dettagliata dei requisiti essenziali di cybersecurity definiti nell'Annex I del Cyber Resilience Act, costituendo il riferimento tecnico principale per la valutazione di conformità dei prodotti con elementi digitali dell'Organizzazione. L'Annex I rappresenta il cuore normativo del CRA, definendo sia le proprietà di sicurezza che i prodotti devono possedere sia i processi di gestione delle vulnerabilità che i manufacturer devono implementare.

L'Organizzazione utilizza questa mappatura per due finalità complementari. In primo luogo, essa guida la progettazione e lo sviluppo dei prodotti secondo il principio di security by design, garantendo che i requisiti di sicurezza siano considerati fin dalle prime fasi del ciclo di vita. In secondo luogo, il documento supporta la verifica di conformità pre-rilascio, fornendo checklist operative per ciascuno dei 23 requisiti essenziali.

L'Annex I si articola in due parti distinte ma interconnesse. La Part I definisce 15 requisiti relativi alle proprietà di sicurezza del prodotto, che spaziano dalla progettazione sicura alla protezione dei dati fino ai meccanismi di aggiornamento. La Part II stabilisce 8 requisiti per i processi di vulnerability handling che il manufacturer deve mantenere attivi durante l'intero support period. Entrambe le parti devono essere integralmente soddisfatte per poter procedere con la conformity assessment e l'apposizione del marchio CE.

---

## 2. Part I: Security Requirements - Product Properties

### 2.1 REQ-I.1: Secure by Design

**Requisito CRA**: *Products with digital elements shall be designed, developed and produced in such a way that they ensure an appropriate level of cybersecurity based on the risks.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Sicurezza integrata nel ciclo di sviluppo, non aggiunta dopo |
| **Applicabilità** | Tutti i prodotti |
| **Risk-based** | Livello sicurezza proporzionato ai rischi identificati |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 1.1 | Security requirements definiti in fase di design | ☐ | |
| 1.2 | Threat modeling condotto | ☐ | |
| 1.3 | Security architecture documentata | ☐ | |
| 1.4 | Secure development lifecycle (SDL) implementato | ☐ | |
| 1.5 | Security review in ogni fase di sviluppo | ☐ | |
| 1.6 | Risk assessment cybersecurity condotto | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.25-28 (Secure development lifecycle) |
| IEC 62443-4-1 | SR-1 to SR-7 (Security requirements) |
| OWASP SAMM | Design Security Practices |

---

### 2.2 REQ-I.2: No Known Exploitable Vulnerabilities

**Requisito CRA**: *Products shall be made available on the market without any known exploitable vulnerabilities.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Zero vulnerabilità sfruttabili note al rilascio |
| **Applicabilità** | Tutti i prodotti |
| **Continuous** | Verificato ad ogni release |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 2.1 | Vulnerability scanning pre-release condotto | ☐ | |
| 2.2 | Penetration testing condotto | ☐ | |
| 2.3 | SBOM analizzato per CVE note | ☐ | |
| 2.4 | Tutte vulnerabilità High/Critical rimediate | ☐ | |
| 2.5 | Sign-off security prima del rilascio | ☐ | |
| 2.6 | Processo per bloccare release se vuln critiche | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.8 (Vulnerability management) |
| IEC 62443-4-1 | SVV (Security verification and validation) |
| OWASP ASVS | V14 (Configuration verification) |

---

### 2.3 REQ-I.3: Secure by Default

**Requisito CRA**: *Products shall be made available on the market with a secure by default configuration, including the possibility to reset the product to its original state.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Configurazione sicura out-of-the-box |
| **Applicabilità** | Tutti i prodotti |
| **Reset** | Possibilità di ripristino configurazione originale |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 3.1 | Default password non usate o uniche per dispositivo | ☐ | |
| 3.2 | Servizi non necessari disabilitati di default | ☐ | |
| 3.3 | Porte non necessarie chiuse di default | ☐ | |
| 3.4 | Crittografia abilitata di default dove applicabile | ☐ | |
| 3.5 | Logging sicurezza abilitato di default | ☐ | |
| 3.6 | Factory reset function disponibile | ☐ | |
| 3.7 | Secure defaults documentati | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ETSI EN 303 645 | 5.1 (No universal default passwords) |
| CIS Benchmarks | Secure configuration baselines |
| NIST SP 800-123 | Server security guidelines |

---

### 2.4 REQ-I.4: Protection from Unauthorized Access

**Requisito CRA**: *Products shall ensure protection from unauthorised access by appropriate control mechanisms, including but not limited to authentication, identity or access management systems.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Controllo accessi robusto |
| **Applicabilità** | Tutti i prodotti con funzionalità di accesso |
| **Meccanismi** | Autenticazione, IAM, access control |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 4.1 | Autenticazione richiesta per accesso | ☐ | |
| 4.2 | Password policy robusta (complessità, lunghezza) | ☐ | |
| 4.3 | Multi-factor authentication supportata (se applicable) | ☐ | |
| 4.4 | Account lockout dopo tentativi falliti | ☐ | |
| 4.5 | Session timeout implementato | ☐ | |
| 4.6 | Role-based access control (RBAC) | ☐ | |
| 4.7 | Principle of least privilege applicato | ☐ | |
| 4.8 | Credential storage sicuro (hashing, no plaintext) | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.5.15-18, A.8.2-5 (Access control) |
| IEC 62443-4-2 | CR 1.1-1.14 (Identification and authentication) |
| OWASP ASVS | V2-V4 (Authentication, Session, Access) |

---

### 2.5 REQ-I.5: Confidentiality Protection

**Requisito CRA**: *Products shall protect the confidentiality of stored, transmitted or otherwise processed data, personal or other, such as by encrypting relevant data at rest or in transit by state of the art mechanisms.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Protezione riservatezza dati |
| **Scope** | Dati at rest e in transit |
| **Mechanism** | Crittografia state-of-the-art |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 5.1 | Dati sensibili identificati e classificati | ☐ | |
| 5.2 | Crittografia at rest per dati sensibili (AES-256+) | ☐ | |
| 5.3 | TLS 1.2+ per comunicazioni in transit | ☐ | |
| 5.4 | Cipher suite sicure configurate | ☐ | |
| 5.5 | Certificate validation implementata | ☐ | |
| 5.6 | Key management sicuro | ☐ | |
| 5.7 | No dati sensibili in log o error messages | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.24 (Use of cryptography) |
| IEC 62443-4-2 | CR 4.1-4.3 (Data confidentiality) |
| NIST SP 800-175B | Cryptographic standards |

---

### 2.6 REQ-I.6: Data Integrity Protection

**Requisito CRA**: *Products shall protect the integrity of stored, transmitted or otherwise processed data, personal or other, against any unlawful processing, modification, or deliberate manipulation, and shall report corruptions.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Protezione integrità dati |
| **Scope** | Stored, transmitted, processed data |
| **Reporting** | Segnalazione corruzioni |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 6.1 | Integrity checks per dati critici (hash, checksum) | ☐ | |
| 6.2 | Digital signatures per firmware/software | ☐ | |
| 6.3 | Input validation implementata | ☐ | |
| 6.4 | Output encoding applicato | ☐ | |
| 6.5 | Database integrity constraints | ☐ | |
| 6.6 | Audit trail per modifiche dati critici | ☐ | |
| 6.7 | Corruption detection e alerting | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.24 (Cryptography for integrity) |
| IEC 62443-4-2 | CR 3.1-3.9 (System integrity) |
| OWASP ASVS | V5 (Validation, Sanitization, Encoding) |

---

### 2.7 REQ-I.7: Data Minimization

**Requisito CRA**: *Products shall process only data, personal or other, that are adequate, relevant and limited to what is necessary in relation to the intended use of the product (data minimisation).*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Minimizzazione raccolta/elaborazione dati |
| **Principio** | Solo dati necessari per scopo previsto |
| **Link GDPR** | Allineato con principi GDPR |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 7.1 | Data inventory condotto | ☐ | |
| 7.2 | Justification per ogni tipo dato raccolto | ☐ | |
| 7.3 | No raccolta dati oltre intended purpose | ☐ | |
| 7.4 | Data retention policy definita | ☐ | |
| 7.5 | Automatic data deletion implementata | ☐ | |
| 7.6 | Privacy by design applicato | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| GDPR | Art. 5.1(c) (Data minimisation) |
| ISO 27701 | 7.4 (Data minimization) |
| ETSI EN 303 645 | 5.8 (Personal data protection) |

---

### 2.8 REQ-I.8: Availability Protection

**Requisito CRA**: *Products shall protect the availability of essential and basic functions, including through resilience against and mitigation of denial of service attacks.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Garantire disponibilità funzioni essenziali |
| **Focus** | Resilienza contro DoS |
| **Scope** | Funzioni essential e basic |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 8.1 | Essential functions identificate | ☐ | |
| 8.2 | Rate limiting implementato | ☐ | |
| 8.3 | Input size limits definiti | ☐ | |
| 8.4 | Connection limits configurati | ☐ | |
| 8.5 | Resource exhaustion protection | ☐ | |
| 8.6 | Graceful degradation under load | ☐ | |
| 8.7 | Watchdog/self-recovery mechanisms | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.5.29-30 (Business continuity) |
| IEC 62443-4-2 | CR 7.1-7.8 (Resource availability) |
| OWASP ASVS | V11 (Business logic) |

---

### 2.9 REQ-I.9: Minimize Negative Impact on Other Systems

**Requisito CRA**: *Products shall minimise their own negative impact on the availability of services provided by other devices or networks.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Non impattare altri sistemi/reti |
| **Scope** | Comportamento prodotto in rete |
| **Prevenzione** | Evitare che prodotto diventi vettore |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 9.1 | Network traffic normale e prevedibile | ☐ | |
| 9.2 | No broadcast storms o flooding | ☐ | |
| 9.3 | Comportamento in caso di errore controllato | ☐ | |
| 9.4 | No exploitation come botnet/amplifier | ☐ | |
| 9.5 | Quarantine capability se compromesso | ☐ | |

---

### 2.10 REQ-I.10: Attack Surface Limitation

**Requisito CRA**: *Products shall be designed, developed and produced to limit attack surfaces, including external interfaces.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Ridurre superficie di attacco |
| **Focus** | Interfacce esterne, servizi esposti |
| **Principio** | Minimum necessary exposure |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 10.1 | External interfaces inventariate | ☐ | |
| 10.2 | Solo porte/servizi necessari aperti | ☐ | |
| 10.3 | Admin interfaces non esposte pubblicamente | ☐ | |
| 10.4 | Debug interfaces disabilitate in production | ☐ | |
| 10.5 | Unused code/features rimossi | ☐ | |
| 10.6 | API attack surface review condotto | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.20-22 (Network security) |
| IEC 62443-4-2 | CR 2 (Use control) |
| CIS Controls | Control 4 (Secure configuration) |

---

### 2.11 REQ-I.11: Incident Impact Reduction

**Requisito CRA**: *Products shall be designed, developed and produced to reduce the impact of a security incident using appropriate exploitation mitigation mechanisms and techniques.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Limitare impatto di exploitation |
| **Meccanismi** | ASLR, DEP, sandboxing, etc. |
| **Defense in depth** | Multiple layers of protection |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 11.1 | ASLR abilitato | ☐ | |
| 11.2 | DEP/NX abilitato | ☐ | |
| 11.3 | Stack canaries/protection | ☐ | |
| 11.4 | Sandboxing per componenti critici | ☐ | |
| 11.5 | Privilege separation implementata | ☐ | |
| 11.6 | Memory-safe coding practices | ☐ | |
| 11.7 | Secure boot chain | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| IEC 62443-4-2 | CR 3.4 (Software and information integrity) |
| OWASP ASVS | V14 (Configuration) |
| NIST SP 800-53 | SI-16 (Memory protection) |

---

### 2.12 REQ-I.12: Security Logging & Monitoring

**Requisito CRA**: *Products shall provide security-related information by recording and/or monitoring relevant internal activity, including the access to or modification of data, services or functions, with an opt-out mechanism for the user.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Visibilità attività security-relevant |
| **Scope** | Access, modification di dati/servizi/funzioni |
| **Privacy** | Opt-out per utente |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 12.1 | Security events logged (auth, access, changes) | ☐ | |
| 12.2 | Log format strutturato e consistente | ☐ | |
| 12.3 | Timestamp accurati (NTP sync) | ☐ | |
| 12.4 | Log integrity protected | ☐ | |
| 12.5 | Log retention appropriata | ☐ | |
| 12.6 | Opt-out mechanism per utente | ☐ | |
| 12.7 | Privacy considerations per logging | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.15-16 (Logging, monitoring) |
| IEC 62443-4-2 | CR 6.1-6.2 (Audit/accountability) |
| OWASP ASVS | V7 (Error handling and logging) |

---

### 2.13 REQ-I.13: Secure Data Removal

**Requisito CRA**: *Products shall provide for the possibility for the user to securely and easily remove all data and settings on a permanent basis, and, where data can be transferred to other products or systems, ensure that this is done in a secure manner.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Rimozione sicura dati utente |
| **Scope** | Tutti i dati e settings |
| **Method** | Secure, permanent deletion |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 13.1 | Factory reset elimina tutti i dati utente | ☐ | |
| 13.2 | Secure erase (non solo delete) | ☐ | |
| 13.3 | Procedura semplice per utente | ☐ | |
| 13.4 | Conferma eliminazione completata | ☐ | |
| 13.5 | Documentazione procedura decommissioning | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.10 (Information deletion) |
| NIST SP 800-88 | Media sanitization |
| GDPR | Art. 17 (Right to erasure) |

---

### 2.14 REQ-I.14: Secure Data Transfer

**Requisito CRA**: *Where data can be transferred to other products or systems, ensure that this is done in a secure manner.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Trasferimento sicuro dati |
| **Scope** | Export/import dati |
| **Security** | Crittografia, integrity |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 14.1 | Data export in formato standard sicuro | ☐ | |
| 14.2 | Crittografia export opzionale/obbligatoria | ☐ | |
| 14.3 | Integrity verification per data import | ☐ | |
| 14.4 | Authentication per data transfer | ☐ | |

---

### 2.15 REQ-I.15: Security Updates

**Requisito CRA**: *Products shall ensure that vulnerabilities can be addressed through security updates, including, where applicable, through automatic updates and the notification of available updates to users.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Capacità di aggiornamento sicuro |
| **Scope** | Security updates durante support period |
| **Features** | Automatic updates, notifications |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 15.1 | Update mechanism implementato | ☐ | |
| 15.2 | Updates firmati digitalmente | ☐ | |
| 15.3 | Secure download channel (HTTPS) | ☐ | |
| 15.4 | Rollback capability | ☐ | |
| 15.5 | Automatic update option | ☐ | |
| 15.6 | User notification per updates disponibili | ☐ | |
| 15.7 | Update non richiede technical expertise | ☐ | |

#### Standards Reference

| Standard | Controlli Correlati |
|----------|---------------------|
| ISO 27001 | A.8.32 (Change management) |
| ETSI EN 303 645 | 5.3 (Keep software updated) |
| IEC 62443-4-2 | CR 7.6 (Patch management) |

---

## 3. Part II: Vulnerability Handling Requirements

### 3.1 REQ-II.1: Vulnerability Identification & SBOM

**Requisito CRA**: *Manufacturers shall identify and document vulnerabilities and components contained in products with digital elements, including by drawing up a software bill of materials in a commonly used and machine-readable format covering at the very least the top-level dependencies of the products.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Visibilità completa componenti e vulnerabilità |
| **SBOM** | Machine-readable, min top-level dependencies |
| **Format** | SPDX 2.3+, CycloneDX 1.4+ |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 1.1 | SBOM tool integrato in build pipeline | ☐ | |
| 1.2 | SBOM generato automaticamente | ☐ | |
| 1.3 | SBOM in formato standard (SPDX/CycloneDX) | ☐ | |
| 1.4 | Top-level dependencies incluse | ☐ | |
| 1.5 | Transitive dependencies incluse (recommended) | ☐ | |
| 1.6 | SBOM versionato con ogni release | ☐ | |
| 1.7 | Vulnerability scanning basato su SBOM | ☐ | |

---

### 3.2 REQ-II.2: Vulnerability Remediation

**Requisito CRA**: *Manufacturers shall address and remediate vulnerabilities without delay, including by providing security updates.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Remediation tempestiva vulnerabilità |
| **Timeline** | "Without delay" - proporzionato a severità |
| **Delivery** | Security updates |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 2.1 | Vulnerability triage process definito | ☐ | |
| 2.2 | SLA per remediation basato su severità | ☐ | |
| 2.3 | Processo sviluppo patch | ☐ | |
| 2.4 | Testing patch pre-release | ☐ | |
| 2.5 | Processo distribuzione patch | ☐ | |
| 2.6 | Tracking remediation status | ☐ | |

#### Suggested SLAs

| Severità (CVSS) | Target Remediation |
|-----------------|-------------------|
| Critical (9.0+) | 7-14 giorni |
| High (7.0-8.9) | 30 giorni |
| Medium (4.0-6.9) | 90 giorni |
| Low (0.1-3.9) | Next release |

---

### 3.3 REQ-II.3: Security Testing

**Requisito CRA**: *Manufacturers shall apply effective and regular tests and reviews of the security of the product with digital elements.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Validazione continua sicurezza |
| **Scope** | Test regolari ed efficaci |
| **Types** | Pentest, VA, code review, etc. |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 3.1 | Security testing programme definito | ☐ | |
| 3.2 | Static code analysis (SAST) | ☐ | |
| 3.3 | Dynamic testing (DAST) | ☐ | |
| 3.4 | Penetration testing periodico | ☐ | |
| 3.5 | Vulnerability assessment periodico | ☐ | |
| 3.6 | Fuzz testing (se applicable) | ☐ | |
| 3.7 | Test results documentati | ☐ | |
| 3.8 | Findings tracked to remediation | ☐ | |

---

### 3.4 REQ-II.4: Vulnerability Disclosure

**Requisito CRA**: *Once a security update is available, manufacturers shall make publicly available information about fixed vulnerabilities, including a description of the vulnerabilities, information allowing users to identify the affected product, the impacts of the vulnerabilities, their severity and information helping users to remediate the vulnerabilities.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Trasparenza su vulnerabilità corrette |
| **Timing** | Dopo disponibilità fix |
| **Content** | Description, affected products, impact, severity, remediation |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 4.1 | Security advisory template definito | ☐ | |
| 4.2 | Security advisory page pubblica | ☐ | |
| 4.3 | CVE assigned (se applicable) | ☐ | |
| 4.4 | Affected versions chiaramente indicate | ☐ | |
| 4.5 | CVSS score incluso | ☐ | |
| 4.6 | Remediation steps inclusi | ☐ | |
| 4.7 | Distribution list per notifiche | ☐ | |

---

### 3.5 REQ-II.5: Coordinated Vulnerability Disclosure Policy

**Requisito CRA**: *Manufacturers shall put in place and enforce a policy on coordinated vulnerability disclosure.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Processo per ricevere segnalazioni esterne |
| **Scope** | Policy CVD pubblica e applicata |
| **Standard** | ISO 29147, ISO 30111 |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 5.1 | CVD policy documentata | ☐ | |
| 5.2 | Policy pubblicata su website | ☐ | |
| 5.3 | Canale segnalazione sicuro (es. security.txt) | ☐ | |
| 5.4 | Timeline di risposta definite | ☐ | |
| 5.5 | Safe harbor per ricercatori | ☐ | |
| 5.6 | Acknowledgment process | ☐ | |
| 5.7 | Coordinamento con reporter | ☐ | |

---

### 3.6 REQ-II.6: Vulnerability Reporting Contact

**Requisito CRA**: *Manufacturers shall provide a contact address for the reporting of vulnerabilities discovered in the product with digital elements.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Canale chiaro per segnalazioni |
| **Visibility** | Facilmente trovabile |
| **Format** | security.txt, dedicated email, form |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 6.1 | Security contact pubblicato | ☐ | |
| 6.2 | security.txt implementato | ☐ | |
| 6.3 | Encryption key per comunicazioni (PGP) | ☐ | |
| 6.4 | Acknowledgment automatico | ☐ | |
| 6.5 | Processo interno per gestione segnalazioni | ☐ | |

---

### 3.7 REQ-II.7: Secure Update Distribution

**Requisito CRA**: *Manufacturers shall provide for mechanisms to securely distribute updates for products with digital elements to ensure that exploitable vulnerabilities are fixed or mitigated in a timely manner.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Distribuzione sicura aggiornamenti |
| **Security** | Integrità, autenticità updates |
| **Timeliness** | Tempestivo in base a severità |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 7.1 | Update server sicuro (HTTPS, CDN) | ☐ | |
| 7.2 | Code signing per tutti updates | ☐ | |
| 7.3 | Signature verification sul dispositivo | ☐ | |
| 7.4 | Rollback protection | ☐ | |
| 7.5 | Multiple distribution channels | ☐ | |
| 7.6 | Update status tracking | ☐ | |

---

### 3.8 REQ-II.8: Free Security Updates

**Requisito CRA**: *Manufacturers shall ensure that, where technically feasible, security updates are disseminated free of charge, are accompanied by advisory messages providing users with the relevant information including on the potential impact of the installed update, and are provided in a timely manner.*

| Elemento | Descrizione |
|----------|-------------|
| **Obiettivo** | Security updates gratuiti durante support period |
| **Separation** | Separati da functionality updates dove possibile |
| **Information** | Advisory con informazioni rilevanti |

#### Implementation Checklist

| # | Controllo | Status | Evidenza |
|---|-----------|--------|----------|
| 8.1 | Security updates gratuiti | ☐ | |
| 8.2 | Security updates separati da feature updates (dove possibile) | ☐ | |
| 8.3 | Release notes con security info | ☐ | |
| 8.4 | Impact assessment comunicato | ☐ | |
| 8.5 | User notification per critical updates | ☐ | |
| 8.6 | Support period rispettato | ☐ | |

---

## 4. Compliance Summary

### 4.1 Part I Status

| Req ID | Requirement | Status | Owner | Notes |
|--------|-------------|--------|-------|-------|
| I.1 | Secure by design | ☐ C ☐ P ☐ NC | | |
| I.2 | No known vulnerabilities | ☐ C ☐ P ☐ NC | | |
| I.3 | Secure by default | ☐ C ☐ P ☐ NC | | |
| I.4 | Access control | ☐ C ☐ P ☐ NC | | |
| I.5 | Confidentiality | ☐ C ☐ P ☐ NC | | |
| I.6 | Integrity | ☐ C ☐ P ☐ NC | | |
| I.7 | Data minimization | ☐ C ☐ P ☐ NC | | |
| I.8 | Availability | ☐ C ☐ P ☐ NC | | |
| I.9 | Minimize negative impact | ☐ C ☐ P ☐ NC | | |
| I.10 | Attack surface | ☐ C ☐ P ☐ NC | | |
| I.11 | Incident impact reduction | ☐ C ☐ P ☐ NC | | |
| I.12 | Logging/monitoring | ☐ C ☐ P ☐ NC | | |
| I.13 | Data removal | ☐ C ☐ P ☐ NC | | |
| I.14 | Data transfer | ☐ C ☐ P ☐ NC | | |
| I.15 | Security updates | ☐ C ☐ P ☐ NC | | |

### 4.2 Part II Status

| Req ID | Requirement | Status | Owner | Notes |
|--------|-------------|--------|-------|-------|
| II.1 | SBOM & vuln identification | ☐ C ☐ P ☐ NC | | |
| II.2 | Vulnerability remediation | ☐ C ☐ P ☐ NC | | |
| II.3 | Security testing | ☐ C ☐ P ☐ NC | | |
| II.4 | Vulnerability disclosure | ☐ C ☐ P ☐ NC | | |
| II.5 | CVD policy | ☐ C ☐ P ☐ NC | | |
| II.6 | Reporting contact | ☐ C ☐ P ☐ NC | | |
| II.7 | Secure update distribution | ☐ C ☐ P ☐ NC | | |
| II.8 | Free security updates | ☐ C ☐ P ☐ NC | | |

---

## 5. Revision History

| Versione | Data | Autore | Modifiche |
|----------|------|--------|-----------|
| 1.0 | {{document_date}} | {{document_author}} | Prima emissione |

---

*Questo documento deve essere aggiornato ad ogni release del prodotto e riesaminato annualmente o in caso di modifiche normative.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| cra-compliance-checklist.md | Checklist conformità CRA completa con rubric |
| cra-risk-assessment.md | Risk assessment prodotto (per req. I.2, I.9) |
| cra-sbom-template.md | SBOM prodotto (per req. II.1) |
| cra-vulnerability-handling.md | Processo gestione vulnerabilità (Part II) |
| cra-cvd-policy.md | CVD policy (per req. II.5) |
| cra-security-update-process.md | Processo security update (per req. I.15, II.7-8) |
| cra-technical-documentation.md | Documentazione tecnica Annex VII |
| cra-module-a-checklist.md | Self-assessment Module A |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter, Sez. 5 | Data del documento |
| `{{document_author}}` | Sez. 5 | Autore del documento |
| Part I assessment | Sez. 2 | Valutare conformità per ognuno dei 15 requisiti |
| Part II assessment | Sez. 3 | Valutare conformità per ognuno degli 8 requisiti |
| Evidence per requirement | Sez. 2-3 | Documentare evidenze per ogni requisito |
| Compliance status | Sez. 4 | Compilare summary status (C/P/NC per requisito) |
| Owner per requirement | Sez. 4 | Assegnare owner per ogni requisito |
| Approval signatures | Sez. 5 | Firme approvazione |
