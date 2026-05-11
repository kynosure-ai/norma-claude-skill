# NORMA by Kynosure — Claude Skill

> **Important / Importante:** This skill provides compliance template drafting and gap-analysis support based on public regulations and standards. It is **not legal advice**. Outputs must be reviewed by qualified legal/compliance professionals before use in production. Questo skill non costituisce consulenza legale: le bozze prodotte vanno sempre validate da professionisti qualificati. See [LICENSE](LICENSE) for the full disclaimer.

EU compliance methodology + 32 strategic-subset templates for AI Act, ISO 42001, NIS2, DORA, ISO 27001, ISO 22301, ISO 27701, CRA — adapted from the NORMA corpus by Kynosure.

## Install

In any Claude Code session:

```bash
# 1. Add the marketplace
/plugin marketplace add kynosure-ai/norma-claude-skill

# 2. Install the plugin
/plugin install norma-claude-skill@norma
```

The skill auto-activates on EU-compliance-flavored questions. To invoke it explicitly:

```bash
/norma-claude-skill:norma "Generate a NIS2 Art. 21 risk-analysis policy outline"
```

This plugin is also being submitted to the [Anthropic-official plugin directory](https://github.com/anthropics/claude-plugins-official) — once review completes the install path will additionally be `/plugin install norma-claude-skill@claude-plugins-official`.

## What it does

The skill is a **router**: it identifies the framework + document type from your request, loads the matching framework methodology and template, and composes a draft with specific clause / article citations and a clear caveat. It does NOT replace legal review — it produces serious starting drafts informed by serious framework expertise so you don't start from a blank page.

### Example prompts

**1. Draft a framework-specific policy.**

```
Help me draft an AI Act risk classification policy for our internal HR-screening AI system.
```

Claude loads `frameworks/ai-act.md` (EU AI Act methodology) plus `templates/aims/aims-compliance-eu-ai-act-compliance-checklist.md`. The response includes the Annex III high-risk classification path (HR is Annex III §4(a) — recruitment/selection), the four risk categories, the Art. 14 human oversight design questions, and clarifying questions about deployment scope (provider vs deployer obligations) before producing the draft. Citations point at specific articles, not the regulation generally.

**2. Cross-framework mapping.**

```
Map our ISO 27001 Annex A controls to NIS2 Article 21 risk-management measures.
```

Claude loads both `frameworks/isms.md` and `frameworks/nis2.md` in parallel, then produces a side-by-side table — for example, ISO 27001 A.5.19 (supplier-relationship management) maps to NIS2 Art. 21(2)(d) (supply-chain security); A.5.24 (incident management planning) maps to Art. 21(2)(b) and Art. 23 (incident reporting). The response calls out where ISO conformity is necessary but not sufficient (NIS2 adds the 24h early warning + 72h initial notification timelines that ISO does not prescribe).

**3. Authored from a template.**

```
Generate a Statement of Applicability for ISO 42001 covering 38 Annex A controls.
```

Claude loads `frameworks/aims.md` (which has the 38 controls organised in 9 domains) and the closest matching template structure. The response is a structured SoA with placeholders for each of the 38 controls' applicability decision and rationale, calling out which decisions the user must make based on their AI system inventory (which the skill cannot guess).

## What's inside

- `skills/norma/SKILL.md` — the router (compact, ≤500 lines per Anthropic guidance)
- `skills/norma/INDEX.md` — catalog navigation (framework × document-type for the 32 templates + cross-framework adjacency table)
- `skills/norma/frameworks/{ai-act,aims,isms,bcms,pims,nis2,dora,cra}.md` — 8 framework methodology references
- `skills/norma/templates/{aims,isms,nis2,dora,pims,bcms,cra}/` — 32 strategic-subset templates across 7 framework subdirectories (the `aims/` slice covers both ISO 42001 and EU AI Act use cases)
- `LICENSE` — MIT body + appended not-legal-advice disclaimer
- `PROVENANCE.md` — byte-identical mirror of the NORMA corpus PROVENANCE.md (sources, license posture, audit attestations)
- `.claude-plugin/{plugin.json,marketplace.json}` — plugin manifest and self-distributing marketplace listing

## FAQ

**Is this legal advice?**

No. This skill drafts compliance documents and does gap analysis based on public regulations and standards. Outputs are starting drafts that **must be reviewed by qualified legal / compliance professionals** before any production use. The disclaimer is not boilerplate — regulatory interpretation is jurisdictional, sectoral, and contextual; the skill cannot make those calls for you.

**Where does the corpus come from?**

See [PROVENANCE.md](PROVENANCE.md). The 32 bundled templates are a strategic subset of the broader NORMA corpus (208 templates, IT + EN), selected for breadth-showcase across all 8 frameworks. Sources: EUR-Lex (EU regulations and directives), ISO standards, ENISA guidelines, NIST AI RMF / SP 800-30 / CSF 2.0, and Italian sectoral guidance (ACN, AgID, Garante, Normattiva). Two audits closed PASS pre-release: a stratified-sample provenance audit (47/47 source references resolvable) and a full-corpus employer-cleanliness scan (210 files, 8-pattern hygiene catalogue).

**Can I use this commercially?**

Yes. Code-level artifacts (SKILL.md, manifest files, scripts) are MIT licensed — attribution appreciated but not required. Corpus content (templates, framework references) is CC BY-SA 4.0 — attribution required, derivatives must be shared under the same license. See [LICENSE](LICENSE) for the operative MIT body and [PROVENANCE.md](PROVENANCE.md) for the corpus license posture.

**How do I get the full corpus?**

The full 208-template corpus (104 IT + 104 EN) is Kynosure-private. The 32-template subset bundled here is the public release. To consult against the full corpus programmatically, see the upcoming **NORMA MCP Server** — open code, private data pattern: server is open-source, corpus stays in a Kynosure-managed Cloud Storage bucket.

**Why Italian-first content?**

The framework reference files preserve the original Italian-prose methodology (Kynosure's compliance-corpus voice, EU regulatory context clearest in Italian sources). Section headers and technical terms are English so navigation works for any reader. Templates are Italian-first, matching Kynosure's primary EU audience. English versions of the templates are roadmap for v1.1 if reach signal warrants. If you're drafting in English, ask the skill to draft in English — the structural shape transfers cleanly across languages.

**How do I report an issue?**

Open an issue at https://github.com/kynosure-ai/norma-claude-skill/issues. Particularly welcome: corrections to regulatory references (clause numbers, article numbers, mapping accuracy), missing frameworks within the EU compliance scope, or feedback on template usability in real consulting contexts. Pull requests are welcome under the same license terms (MIT for code, CC BY-SA 4.0 for corpus content).

## Learn more

**Browse other NORMA distribution artifacts, get email updates, or contact Kynosure:**

- [kynosure.ai/it/norma/claude-skill?utm_source=norma-claude-skill-readme&utm_medium=github&utm_campaign=norma-launch](https://kynosure.ai/it/norma/claude-skill?utm_source=norma-claude-skill-readme&utm_medium=github&utm_campaign=norma-launch) (Italian)
- [kynosure.ai/en/norma/claude-skill?utm_source=norma-claude-skill-readme&utm_medium=github&utm_campaign=norma-launch](https://kynosure.ai/en/norma/claude-skill?utm_source=norma-claude-skill-readme&utm_medium=github&utm_campaign=norma-launch) (English)

The Kynosure NORMA catalog page lists this Claude Skill alongside the upcoming **NORMA MCP Server** (programmatic access for any MCP-compatible AI assistant) and the **NORMA Custom GPT** (ChatGPT Custom GPT with embedded subset).

## About Kynosure

This Claude Skill is built and maintained by [Kynosure](https://kynosure.ai), a European compliance platform that produces one assessment covering NIS2, DORA, ISO 27001, ISO 22301, ISO 42001, ISO 27701, CRA, and the EU AI Act. The Skill packages a curated subset of the Kynosure compliance corpus (32 templates across 7 framework families plus 8 framework reference files) so you can route compliance questions through Claude with sector-aware context.

For the full multi-framework assessment, sector-profiled scoring, and methodology-backed PDF reports, see [kynosure.ai](https://kynosure.ai/?utm_source=norma-claude-skill-readme&utm_medium=github&utm_campaign=about-kynosure).

## License + provenance

Released under [MIT License](LICENSE) (code-level artifacts) and CC BY-SA 4.0 (corpus content), with not-legal-advice disclaimer. Provenance, source list, and audit attestations in [PROVENANCE.md](PROVENANCE.md). Maintained by [Kynosure](https://kynosure.ai).
