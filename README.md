<h1 align="center">Bioq. Aldo J. Cáceres Ruiz Díaz</h1>

<p align="center">
  <strong>I build AI agent systems that run in production — with method, evidence and human control.</strong>
</p>

<p align="center">
  Biochemist &amp; virologist at ANLIS Malbrán — CBRN (QBRN), disarmament &amp; AI<br>
  Biosafety &amp; CBRN scientist adding AI and bioinformatics
</p>

<p align="center">
  Scientific Advisor (Asesor científico), UOCCB, ANLIS "Dr. Carlos G. Malbrán"<br>
  Ministry of Health, Argentina
</p>

<p align="center">
  <a href="https://github.com/bioqruizdiazaldo-cmd/praxia-ops">PraxIA Ops</a> ·
  Microbiology, biosafety and CBRN (QBRN) governance ·
  Argentina
</p>

---

## What I do

I come from science: microbiology, infectious disease, biosafety, and CBRN (QBRN) governance. In July 2026 I started building **PraxIA Ops**, an operational AI-agent platform. In 22 days it went from a first workflow to a 24/7 system with an orchestrator, 15 subagents, persistent memory in PostgreSQL, human approval on consequential actions, and deployment with rollback.

I do not write the application line by line. **I design the architecture, write the contracts, define the invariants in the database, and direct coding agents that implement under supervision.** That is the discipline: the model proposes, evidence decides, the person approves.

What I bring from biosafety applies here in the same way: traceability, access control, containment, written procedures, and the habit of assuming that things will fail.

---

## Scientific practice and direction

**Current position.** Scientific Advisor (Asesor científico), UOCCB, ANLIS "Dr. Carlos G. Malbrán" (Ministry of Health, Argentina). The work is virology, biosafety, biosecurity, biological containment, and CBRN (QBRN: chemical, biological, radiological, and nuclear).

**CBRN, disarmament, and international security.** This pillar sits alongside the AI and bioinformatics work: CBRN defense, non-proliferation of biological weapons under the Biological Weapons Convention (BWC), disarmament, arms control, and international security. I am aiming at organizations in that field, including the Organisation for the Prohibition of Chemical Weapons (OPCW) and the Stockholm International Peace Research Institute (SIPRI). Current affiliation remains the post above.

**Artificial intelligence and bioinformatics.** I am pursuing a Master’s in Artificial Intelligence at UTAMED and a Master’s in Bioinformatics at the Universidad Internacional de Valencia (VIU). Both are in progress. The applied focus is machine learning for genomics and biosecurity, bioinformatics pipelines, and viral genomic surveillance.

---

## Principal project

### [praxia-ops](https://github.com/bioqruizdiazaldo-cmd/praxia-ops) — production AI-agent platform

Complete, sanitised, verifiable documentation of a real system.

| | |
|---|---|
| Agents in production | 1 orchestrator + 15 subagents |
| n8n workflows registered / active | 217 / 25 |
| Versioned SQL migrations | 40+ |
| Automated test cases | 606 |
| API endpoints | 60+, none `DELETE` |
| MCP tools | 22, in 4 OAuth scopes |

These figures describe the private system. The public repository is the sanitised record.

**Inside you will find:**

- A [user manual](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/00-manual-de-usuario) in 10 chapters, including the chapter on the fiscal agent.
- A [breakdown of decision criteria](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/02-desglose-tecnico): when it belongs in SQL, when in n8n, when it warrants a subagent, when an MCP, when a purpose-built API, when a screen.
- [13 ADRs](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/04-decisiones), including the one for a search tool that was **not** published because it scored 2 of 7 tests.
- A [fiscal agent](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/systems/praxia-agente-fiscal) that proposes and never applies: not because it behaves, but because its credential receives 403 when it tries to approve.
- [Runbooks and real incidents](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/06-runbooks): a 21.9 MB PDF that broke the pipeline, and five days of drift between repository and server.
- A [method for working with AI agents](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/05-gobernanza) — SDLC, templates, and checklists — reusable by any team. Also [in English](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/05-gobernanza/en).

### AI-driven viral genomic surveillance pipeline — coming soon

Placeholder. No repository yet. The intended work is a pipeline that applies machine learning to viral genome data for surveillance.

### Biosecurity risk-assessment tool — coming soon

Placeholder. No repository yet. The intended work is a tool for structured biosecurity risk assessment.

---

## Stack

**Orchestration** n8n self-hosted · Model Context Protocol (MCP) · OpenAI (chat, Whisper, TTS)
**Data** PostgreSQL 16 · SQL as contract: triggers, functions, views, roles without `DELETE`
**Runtime** Docker · Traefik + TLS · own VPS · backups with verification and rollback
**Backend** Node.js ESM · OpenAPI 3.1 · OAuth 2.0 + PKCE
**Interfaces** Telegram (text, voice, image, PDF) · web dashboard · MCP for external agents
**Integrations** Gmail · Google Calendar, Drive, and Sheets · Tavily · Europe PMC · OpenAlex · RSS
**Method** ADRs · workflow manifests · canary · blameless post-mortems · `node --test` + PGlite

**Scientific computing, alongside the master’s work** Python · Bash · machine-learning libraries · bioinformatics tools

---

## How I work

> **Without order there is no system, only experiments.**

1. **Planning before implementation.** Always. The expensive error is almost never technical: it is one of sequence.
2. **Inspection is not authorisation to change.** An agent may read everything; writing needs explicit permission.
3. **The absence of data does not become an invented datum.** If there is no evidence, the gap is declared.
4. **Human approval is not a formality.** Sending mail, spending, deleting, or publishing goes through a person.
5. **Every deployment has a verified rollback.** If it cannot be undone, it does not ship.

---

## On publishing failures

In [praxia-ops](https://github.com/bioqruizdiazaldo-cmd/praxia-ops) the incidents are documented, as are the drift, the 73 laboratory workflows that remained living alongside production, and the search tool that did not pass validation.

They are there on purpose. A system that only shows its successes is not documented: it is advertised.

---

## Education

- Master’s in Artificial Intelligence, UTAMED — in progress
- Master’s in Bioinformatics, Universidad Internacional de Valencia (VIU) — in progress
- Biochemist (Bioquímico)

Virology, biosafety, biosecurity, biological containment, and CBRN (QBRN) are my practice as Scientific Advisor (Asesor científico) at UOCCB, ANLIS "Dr. Carlos G. Malbrán".

---

## Contact

- LinkedIn: [https://www.linkedin.com/in/PLACEHOLDER](https://www.linkedin.com/in/PLACEHOLDER) — replace `PLACEHOLDER` with the public profile URL
- GitHub: [github.com/bioqruizdiazaldo-cmd](https://github.com/bioqruizdiazaldo-cmd)

---

<p align="center">
  <sub>All public documentation is sanitised. The runtime, the credentials, and the real data live on private infrastructure.</sub>
</p>
