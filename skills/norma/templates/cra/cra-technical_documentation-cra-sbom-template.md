---
title: CRA SBOM Requirements & Template
version: '1.1'
date: '{{document_date}}'
classification: Riservato
owner: Product Security / Engineering
approver: CISO
framework: CRA
documentType: procedure
language: IT
regulation_articles:
  - Art. 13.5 - Obligations of manufacturers (vulnerability handling)
  - Art. 13.7 - Information obligations
  - Art. 14 - Reporting obligations
  - Annex I Part II.1 - Vulnerability identification and documentation
  - Annex I Part II.2 - Vulnerability remediation
  - Annex VII - Technical documentation
cross_references:
  - NTIA SBOM Minimum Elements (2021)
  - BSI TR-03183-2 SBOM Requirements
  - 'SPDX 2.3 Specification (ISO/IEC 5962:2021)'
  - CycloneDX 1.4+ Specification (OWASP)
  - CISA SBOM Types Document (2023)
status: Bozza
subset: true
---

# CRA SBOM Requirements & Template

## 1. Scopo e Contesto

Il presente documento definisce i requisiti e fornisce i template per la creazione del Software Bill of Materials (SBOM) in conformità con il Cyber Resilience Act. L'SBOM costituisce un inventario formale di tutti i componenti software che compongono un prodotto con elementi digitali, rappresentando uno strumento essenziale per la gestione delle vulnerabilità e la sicurezza della supply chain.

L'Organizzazione è tenuta a predisporre e mantenere un SBOM per ogni prodotto immesso sul mercato europeo, come richiesto dall'Annex I Part II.1 del CRA. Il documento deve essere in formato machine-readable utilizzando standard riconosciuti quali SPDX o CycloneDX, e deve includere come minimo le dipendenze top-level del prodotto. L'Organizzazione adotta la pratica raccomandata di includere anche le dipendenze transitive per una maggiore trasparenza e capacità di tracciamento delle vulnerabilità.

L'SBOM svolge molteplici funzioni nel contesto della conformità CRA. Esso abilita il monitoraggio continuo delle vulnerabilità nei componenti di terze parti, supporta le attività di incident response permettendo di identificare rapidamente i prodotti impattati da nuove CVE, e facilita la comunicazione con le autorità di sorveglianza del mercato che possono richiedere l'SBOM durante ispezioni o investigazioni. Il documento deve essere mantenuto aggiornato durante l'intero support period del prodotto e conservato secondo i requisiti di retention della documentazione tecnica.

---

## 2. CRA SBOM Requirements

### 1.2 SBOM Lifecycle

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           SBOM LIFECYCLE                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  DEVELOPMENT          BUILD              RELEASE           OPERATIONS       │
│       │                  │                  │                   │           │
│       ▼                  ▼                  ▼                   ▼           │
│  ┌─────────┐        ┌─────────┐        ┌─────────┐        ┌─────────┐      │
│  │ Design  │        │ Generate│        │ Validate│        │ Monitor │      │
│  │ SBOM    │───────►│ SBOM    │───────►│ & Sign  │───────►│ & Update│      │
│  │         │        │         │        │         │        │         │      │
│  └─────────┘        └─────────┘        └─────────┘        └─────────┘      │
│       │                  │                  │                   │           │
│       ▼                  ▼                  ▼                   ▼           │
│  • Identify         • Automated       • CVE scan         • Continuous      │
│    dependencies       generation      • Completeness       monitoring      │
│  • License          • CI/CD             check            • Update on       │
│    analysis           integration     • Digital            changes         │
│  • Risk             • Hash              signature        • Vulnerability   │
│    assessment         generation                           tracking        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 2. Format Requirements

### 2.1 Accepted Formats

| Format | Version | Specification | Recommended |
|--------|---------|---------------|-------------|
| **SPDX** | 2.3+ | [spdx.dev](https://spdx.dev) | ☐ |
| **CycloneDX** | 1.4+ | [cyclonedx.org](https://cyclonedx.org) | ☐ |

### 2.2 Output Formats

| Output | SPDX | CycloneDX | Use Case |
|--------|------|-----------|----------|
| JSON | ✓ | ✓ | Primary exchange format |
| XML | ✓ | ✓ | Enterprise integration |
| Tag-Value | ✓ | - | Legacy compatibility |
| RDF | ✓ | - | Semantic web |

### 2.3 Format Selection Criteria

| Criterio | SPDX | CycloneDX |
|----------|------|-----------|
| License compliance focus | ★★★★★ | ★★★ |
| Security focus | ★★★ | ★★★★★ |
| Vulnerability linking | ★★★ | ★★★★★ |
| Tool ecosystem | ★★★★ | ★★★★★ |
| BSI TR-03183-2 compliance | ✓ | ✓ |

**Recommendation**: CycloneDX for security-focused SBOM, SPDX for license compliance focus

---

## 3. Minimum Required Elements

### 3.1 CRA Minimum (Top-Level Dependencies)

| Element | Required | Description |
|---------|----------|-------------|
| Component Name | ✓ | Nome univoco del componente |
| Component Version | ✓ | Versione specifica |
| Supplier | ✓ | Fornitore/maintainer |
| Relationship | ✓ | Tipo di dipendenza |

### 3.2 BSI TR-03183-2 Extended Elements

| Element | Required | Recommended | Description |
|---------|----------|-------------|-------------|
| Component Name | ✓ | | Nome componente |
| Component Version | ✓ | | Versione |
| Supplier/Author | ✓ | | Fonte componente |
| Unique Identifier | ✓ | | PURL, CPE, SWID |
| Dependency Relationship | ✓ | | contains, depends-on |
| Hash/Checksum | | ✓ | Verifica integrità |
| License | | ✓ | Identificativo licenza |
| Source Location | | ✓ | Repository URL |
| Download Location | | ✓ | URL download |
| Copyright | | ✓ | Holder copyright |

### 3.3 Recommended Additional Elements

| Element | Purpose | Format |
|---------|---------|--------|
| PURL | Universal package identifier | pkg:type/namespace/name@version |
| CPE | Vulnerability matching | cpe:2.3:a:vendor:product:version |
| SWID | Software identification | ISO/IEC 19770-2 |
| VEX | Vulnerability exploitability | CSAF VEX or CycloneDX VEX |

---

## 4. SBOM Metadata Template

### 4.1 Document Information

```json
{
  "bomFormat": "CycloneDX",
  "specVersion": "1.5",
  "serialNumber": "urn:uuid:[GENERATE-UUID]",
  "version": 1,
  "metadata": {
    "timestamp": "[YYYY-MM-DDTHH:MM:SSZ]",
    "tools": [
      {
        "vendor": "[Tool Vendor]",
        "name": "[SBOM Generation Tool]",
        "version": "[Tool Version]"
      }
    ],
    "authors": [
      {
        "name": "[Author Name]",
        "email": "[author@company.com]"
      }
    ],
    "component": {
      "type": "application",
      "name": "[Product Name]",
      "version": "[Product Version]",
      "description": "[Product Description]",
      "licenses": [
        {
          "license": {
            "id": "[SPDX-License-ID]"
          }
        }
      ],
      "supplier": {
        "name": "[Manufacturer Name]",
        "url": ["https://manufacturer.com"],
        "contact": [
          {
            "email": "security@manufacturer.com"
          }
        ]
      }
    },
    "manufacture": {
      "name": "[Manufacturer Name]",
      "url": ["https://manufacturer.com"]
    }
  }
}
```

### 4.2 Component Entry Template

```json
{
  "components": [
    {
      "type": "library",
      "bom-ref": "[unique-reference]",
      "name": "[Component Name]",
      "version": "[X.Y.Z]",
      "description": "[Component Description]",
      "purl": "pkg:npm/component-name@1.2.3",
      "cpe": "cpe:2.3:a:vendor:component:1.2.3:*:*:*:*:*:*:*",
      "licenses": [
        {
          "license": {
            "id": "MIT"
          }
        }
      ],
      "supplier": {
        "name": "[Supplier Name]",
        "url": ["https://supplier.com"]
      },
      "hashes": [
        {
          "alg": "SHA-256",
          "content": "[hash-value]"
        }
      ],
      "externalReferences": [
        {
          "type": "website",
          "url": "https://component-website.com"
        },
        {
          "type": "vcs",
          "url": "https://github.com/org/component"
        }
      ]
    }
  ]
}
```

### 4.3 Dependency Relationship Template

```json
{
  "dependencies": [
    {
      "ref": "[main-product-bom-ref]",
      "dependsOn": [
        "[component-1-bom-ref]",
        "[component-2-bom-ref]",
        "[component-3-bom-ref]"
      ]
    },
    {
      "ref": "[component-1-bom-ref]",
      "dependsOn": [
        "[transitive-dep-1-bom-ref]",
        "[transitive-dep-2-bom-ref]"
      ]
    }
  ]
}
```

---

## 5. SBOM Information Sheet

### 5.1 Product SBOM Summary

| Campo | Valore |
|-------|--------|
| **Product Name** | [________________________________] |
| **Product Version** | [________________________________] |
| **SBOM Generation Date** | [________________________________] |
| **SBOM Format** | ☐ SPDX 2.3 ☐ CycloneDX 1.5 |
| **SBOM File Name** | [________________________________] |
| **SBOM Serial Number** | [________________________________] |

### 5.2 Component Statistics

| Metric | Count |
|--------|-------|
| Total Components | [___] |
| Direct Dependencies | [___] |
| Transitive Dependencies | [___] |
| Open Source Components | [___] |
| Commercial/Proprietary | [___] |
| Unique Licenses | [___] |

### 5.3 License Distribution

| License | Count | Risk Level |
|---------|-------|------------|
| MIT | [___] | Low |
| Apache-2.0 | [___] | Low |
| GPL-3.0 | [___] | High (copyleft) |
| BSD-3-Clause | [___] | Low |
| Proprietary | [___] | Review required |
| [Other] | [___] | [___] |

### 5.4 Vulnerability Summary (at time of SBOM generation)

| Severity | Count | Status |
|----------|-------|--------|
| Critical | [___] | ☐ All mitigated |
| High | [___] | ☐ All mitigated |
| Medium | [___] | ☐ All mitigated |
| Low | [___] | ☐ Accepted risk |

---

## 6. SBOM Generation Process

### 6.1 Generation Workflow

| Step | Action | Tool | Output |
|------|--------|------|--------|
| 1 | Identify all dependencies | Package manager, build system | Dependency list |
| 2 | Generate SBOM | SBOM tool | Raw SBOM file |
| 3 | Enrich with metadata | SBOM tool + manual | Complete SBOM |
| 4 | Validate format | SBOM validator | Validation report |
| 5 | Scan for vulnerabilities | VA tool | CVE report |
| 6 | Sign SBOM | Signing tool | Signed SBOM |
| 7 | Archive | Document system | Stored SBOM |

### 6.2 Recommended Tools

| Tool | Type | License | Formats |
|------|------|---------|---------|
| Syft | SBOM generation | Apache 2.0 | SPDX, CycloneDX |
| CycloneDX CLI | SBOM generation | Apache 2.0 | CycloneDX |
| SPDX Tools | SBOM generation | Apache 2.0 | SPDX |
| Dependency-Track | SBOM management | Apache 2.0 | CycloneDX |
| Grype | Vulnerability scan | Apache 2.0 | Multiple |
| Trivy | Vulnerability scan | Apache 2.0 | Multiple |

### 6.3 CI/CD Integration Example

```yaml
# Example GitHub Actions workflow
name: SBOM Generation

on:
  release:
    types: [created]

jobs:
  sbom:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Generate SBOM
        uses: anchore/sbom-action@v0
        with:
          format: cyclonedx-json
          output-file: sbom.json

      - name: Scan for vulnerabilities
        uses: anchore/scan-action@v3
        with:
          sbom: sbom.json
          fail-build: true
          severity-cutoff: high

      - name: Upload SBOM
        uses: actions/upload-artifact@v3
        with:
          name: sbom
          path: sbom.json
```

---

## 7. SBOM Validation Checklist

### 7.1 Format Validation

| Check | Status | Notes |
|-------|--------|-------|
| Valid JSON/XML structure | ☐ Pass ☐ Fail | |
| Correct schema version | ☐ Pass ☐ Fail | |
| All required fields present | ☐ Pass ☐ Fail | |
| Valid SPDX license identifiers | ☐ Pass ☐ Fail | |
| Valid PURL format | ☐ Pass ☐ Fail | |

### 7.2 Completeness Validation

| Check | Status | Notes |
|-------|--------|-------|
| All direct dependencies included | ☐ Pass ☐ Fail | |
| Transitive dependencies included | ☐ Pass ☐ Fail | |
| Version information for all components | ☐ Pass ☐ Fail | |
| Supplier information for all components | ☐ Pass ☐ Fail | |
| License information for all components | ☐ Pass ☐ Fail | |

### 7.3 Security Validation

| Check | Status | Notes |
|-------|--------|-------|
| Hashes present for verification | ☐ Pass ☐ Fail | |
| No known critical CVEs unaddressed | ☐ Pass ☐ Fail | |
| VEX document for known vulnerabilities | ☐ Pass ☐ Fail | |
| SBOM digitally signed | ☐ Pass ☐ Fail | |

---

## 8. SBOM Maintenance

### 8.1 Update Triggers

| Trigger | Action | Timeline |
|---------|--------|----------|
| New product release | Generate new SBOM | Before release |
| Security patch release | Update SBOM | With patch |
| Component update | Regenerate SBOM | With update |
| New CVE affecting component | Update VEX | Within 72h |
| Quarterly review | Validate current SBOM | Quarterly |

### 8.2 Version Control

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| SBOM-v1.0 | {{document_date}} | Initial release | [Name] |
| SBOM-v1.1 | {{document_date}} | Security patch X | [Name] |
| SBOM-v2.0 | {{document_date}} | Major version update | [Name] |

### 8.3 Retention

| Requirement | Period |
|-------------|--------|
| CRA requirement | 10 years from market placement |
| During support period | Continuously maintained |
| After support period | Archived for reference |

---

## 9. VEX (Vulnerability Exploitability eXchange)

### 9.1 VEX Purpose

```
VEX documents allow manufacturers to communicate:
• Which CVEs affect their product
• Whether vulnerabilities are actually exploitable in context
• What actions (if any) customers should take

This reduces "alert fatigue" from SBOM vulnerability scanning
```

### 9.2 VEX Status Values

| Status | Meaning | Action Required |
|--------|---------|-----------------|
| Not Affected | Vulnerability not exploitable in this product | None |
| Affected | Vulnerability is exploitable | Apply mitigation |
| Fixed | Vulnerability was present but fixed | Update to fixed version |
| Under Investigation | Still assessing impact | Monitor for updates |

### 9.3 VEX Template (CycloneDX)

```json
{
  "vulnerabilities": [
    {
      "id": "CVE-2024-XXXXX",
      "source": {
        "name": "NVD",
        "url": "https://nvd.nist.gov/vuln/detail/CVE-2024-XXXXX"
      },
      "ratings": [
        {
          "source": {
            "name": "NVD"
          },
          "score": 7.5,
          "severity": "high",
          "method": "CVSSv31",
          "vector": "CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N"
        }
      ],
      "analysis": {
        "state": "not_affected",
        "justification": "code_not_reachable",
        "detail": "The vulnerable code path is not used in our implementation"
      },
      "affects": [
        {
          "ref": "[component-bom-ref]"
        }
      ]
    }
  ]
}
```

---

## 10. SBOM for Authorities

### 10.1 Information for Market Surveillance

| Element | Included | Format |
|---------|----------|--------|
| Product identification | ✓ | In metadata |
| All components | ✓ | Component list |
| Known vulnerabilities | ✓ | VEX or separate |
| Supplier information | ✓ | Per component |
| Contact information | ✓ | In metadata |

### 10.2 Request Response Process

```
MARKET SURVEILLANCE AUTHORITY REQUEST:

1. Request received from authority
2. Validate requestor identity
3. Prepare SBOM package:
   • Current SBOM (machine-readable)
   • VEX document
   • Summary report (human-readable)
4. Transmit via secure channel
5. Document request and response
6. Retain records
```

---

## 11. Sign-Off

| Role | Name | Signature | Date |
|------|------|-----------|------|
| SBOM Author | | | |
| Security Reviewer | | | |
| Product Owner | | | |

---

## 12. Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | {{document_date}} | {{document_author}} | Initial release |

---

*This SBOM documentation must be maintained throughout the product support period and updated with each release affecting the software composition.*

---

## Documenti Correlati

| Documento | Descrizione |
|-----------|-------------|
| cra-vulnerability-handling.md | Processo gestione vulnerabilità (usa SBOM per triage) |
| cra-annex-i-requirements.md | Requisiti essenziali (Annex I Part II.1) |
| cra-risk-assessment.md | Risk assessment (SBOM input per vulnerability scan) |
| cra-technical-documentation.md | Documentazione tecnica (SBOM come allegato) |
| cra-security-update-process.md | Security update (SBOM per impatto componenti) |
| cra-incident-reporting.md | Incident reporting (SBOM per impatto analisi) |
| cra-compliance-checklist.md | Checklist conformità CRA completa |

---

## Checklist di Compilazione

Campi da completare per rendere operativo questo documento:

| Campo | Sezione | Descrizione |
|-------|---------|-------------|
| `{{document_date}}` | Frontmatter, Sez. 12 | Data del documento |
| `{{document_author}}` | Sez. 12 | Autore del documento |
| Product metadata | Sez. 2 | Informazioni prodotto per SBOM header |
| Format selection | Sez. 3 | Selezionare CycloneDX o SPDX |
| Component inventory | Sez. 4 | Elenco completo componenti (top-level + transitivi) |
| License data | Sez. 5 | Licenze per ogni componente |
| Vulnerability tracking | Sez. 6 | Configurare monitoraggio CVE continuo |
| VEX integration | Sez. 9 | Configurare Vulnerability Exploitability eXchange |
| Authority response | Sez. 10 | Processo risposta richieste authority |
| SBOM tooling | Sez. 7-8 | Configurare generazione e verifica automatica |
| Sign-off | Sez. 11 | Firme SBOM author, security reviewer, product owner |
