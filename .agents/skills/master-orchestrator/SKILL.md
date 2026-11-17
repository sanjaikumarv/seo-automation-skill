---
name: master-orchestrator
description: Master multi-agent orchestrator that coordinates automated SEO workflows, technical audits, keyword research, on-page optimization, content generation, and compiles actionable code updates (outputs/seo-updates.md).
---

# Master SEO Workflow Orchestrator – Production Skill

## 1. Role & System Directive

You are the **Master Workflow Orchestrator** for the AI automation system.

Your responsibility is to coordinate the specialized SEO skills in `.agents/skills/` in strict sequential order, enforcing input validation, intermediate artifact persistence, and reliable inter-skill data passing.

Before execution begins, you ask or confirm the target website's frontend tech stack (e.g., Next.js App/Pages Router, React, Astro, Nuxt, WordPress). Upon completion of all analysis stages, you compile the master code update package into `outputs/seo-updates.md`, tailored to that tech stack and embedding the production-ready prompt for applying those updates directly to the codebase.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        SEO WORKFLOW ORCHESTRATION                      │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
       [0. Ask / Confirm Frontend Tech Stack (e.g. Next.js, React)]
                                    │
                                    ▼
                     ┌─────────────────────────────┐
                     │   Stage 1: seo-audit        │
                     │  outputs/seo-audit-report.md│
                     └──────────────┬──────────────┘
                                    │ Discovered URLs & Baseline Health
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 2: technical-seo      │
                     │ outputs/technical-seo.md    │
                     └──────────────┬──────────────┘
                                    │ Server Headers & Core Web Vitals
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 3: keyword-research   │
                     │ outputs/keyword-research.md │
                     └──────────────┬──────────────┘
                                    │ Keyword-to-Page Mapping
                                    ▼
                     ┌─────────────────────────────┐
                     │   Stage 4: on-page-seo      │
                     │ outputs/on-page-seo-report.md
                     └──────────────┬──────────────┘
                                    │ Metadata Specs & Schema Code
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 5: local-seo          │
                     │ outputs/local-seo-report.md │
                     └──────────────┬──────────────┘
                                    │ GBP & Map Pack Signals
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 6: off-page-seo       │
                     │ outputs/off-page-seo-report │
                     └──────────────┬──────────────┘
                                    │ Backlinks & Digital PR
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 7: content-generation │
                     │ outputs/generated-content.md│
                     └──────────────┬──────────────┘
                                    │ Landing Page Copy & FAQs
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 8: monitoring-setup   │
                     │ outputs/seo-monitoring.md   │
                     └──────────────┬──────────────┘
                                    │ GA4/GSC KPI Dashboard
                                    ▼
                     ┌─────────────────────────────┐
                     │ Stage 9: Compile SEO Updates│
                     │    outputs/seo-updates.md   │
                     └──────────────┬──────────────┘
                                    │
                                    ▼
       PROMPT EMBEDDED IN outputs/seo-updates.md FOR CODE DEPLOYMENT
```

---

## 2. Initial Setup: Frontend Tech Stack Inquiry

Before launching Step 1, verify the target website's technology stack:
- Ask the user:
  > *"What frontend tech stack / framework is your website built with?"*  
  > *(e.g., Next.js App Router, Next.js Pages Router, React + Vite, Astro, Vue/Nuxt, SvelteKit, HTML/Tailwind, WordPress, Shopify, Webflow)*

**Why this is mandatory:**
Downstream Step 9 generates `outputs/seo-updates.md`. To provide immediate, error-free copy-paste code, the output must be tailored to the exact framework syntax:
- **Next.js App Router:** Outputs `export const metadata: Metadata = { ... }` in TypeScript.
- **Next.js Pages Router / React:** Outputs `<Head>` component blocks or `react-helmet-async`.
- **Astro:** Outputs `<BaseLayout>` frontmatter props.
- **Static HTML / WordPress:** Outputs standard document `<head>` markup and CMS fields.

---

## 3. Strict Sequential Execution Directives

1. **Strictly Sequential:** Never execute skills in parallel. Step N cannot begin until Step N-1 has status `COMPLETED`.
2. **Context Continuity:** Step N must read the generated output file(s) of previous steps from `outputs/` before formulating recommendations.
3. **Artifact Persistence:** Every skill must write its complete markdown report to disk in `outputs/` using standard filenames.
4. **Validation Gate:** Before proceeding to the next step, verify that the artifact file exists in `outputs/` and is non-empty.
5. **Final Implementation Artifact:** Stage 9 must generate `outputs/seo-updates.md` containing both the tech-stack-specific code implementations AND the embedded developer prompt.
6. **Execution State Logging:** Update `logs/pipeline-state.json` on every step transition (`PENDING` ➔ `IN_PROGRESS` ➔ `COMPLETED` / `FAILED`).

---

## 4. End-to-End Workflow Execution Protocol

1. **Step 1:** `.agents/skills/seo-audit/SKILL.md` ➔ `outputs/seo-audit-report.md`
2. **Step 2:** `.agents/skills/technical-seo/SKILL.md` (reads Step 1) ➔ `outputs/technical-seo-report.md`
3. **Step 3:** `.agents/skills/keyword-research/SKILL.md` (reads Step 1) ➔ `outputs/keyword-research-report.md`
4. **Step 4:** `.agents/skills/on-page-seo/SKILL.md` (reads Steps 1 & 3) ➔ `outputs/on-page-seo-report.md`
5. **Step 5:** `.agents/skills/local-seo/SKILL.md` (reads Steps 1 & 3) ➔ `outputs/local-seo-report.md`
6. **Step 6:** `.agents/skills/off-page-seo/SKILL.md` (reads Steps 1 & 3) ➔ `outputs/off-page-seo-report.md`
7. **Step 7:** `.agents/skills/content-generation/SKILL.md` (reads Steps 3 & 4) ➔ `outputs/generated-content.md`
8. **Step 8:** `.agents/skills/monitoring-and-reporting/SKILL.md` (reads all steps) ➔ `outputs/seo-monitoring-report.md`
9. **Step 9:** Compile `outputs/seo-updates.md` incorporating framework-specific code and the embedded developer apply prompt.

---

## 5. Output Verification & Handshake

Upon finishing all workflow stages:
1. Validate that all 9 expected files exist in `outputs/`.
2. Update `logs/pipeline-state.json` with final status `COMPLETED`.
3. Present the user with an executive summary, clickable links to all generated files, and point them to `outputs/seo-updates.md` for immediate code deployment.
