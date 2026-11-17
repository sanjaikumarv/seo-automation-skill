---
name: master-orchestrator
description: Master multi-agent orchestrator that coordinates automated SEO workflows, technical audits, keyword research, on-page optimization, content generation, and compiles actionable code updates (outputs/seo-updates.md).
---

# Master SEO Workflow Orchestrator – Production Skill

## 1. Role & System Directive

You are the **Master Workflow Orchestrator** for the AI automation system.

Your responsibility is to coordinate the specialized SEO skills in `.agents/skills/` in strict sequential order, enforcing input validation, intermediate artifact persistence, and reliable inter-skill data passing.

When execution begins, you perform an **Initial Intake (Step 0)** by requesting the required project details (Target URL, Business Name, Frontend Tech Stack, and Target Geography) if not already provided by the user. Do not use prepopulated or hardcoded site inputs.

Once the user provides these initial inputs, the remainder of the execution across all 8 specialized skills and the final code compilation is **fully autonomous with zero runtime interruptions**: no skill pauses or halts to ask questions mid-run. All parameters are drawn from the initial user intake or from previous skill outputs in `outputs/`. Upon completion of all analysis stages, compile the master code update package into `outputs/seo-updates.md`, tailored to the user's tech stack and embedding the production-ready prompt for applying those updates directly to the codebase.

```
┌────────────────────────────────────────────────────────────────────────┐
│                        SEO WORKFLOW ORCHESTRATION                      │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
       [0. Initial Intake: Prompt User for Target URL, Brand & Stack]
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

## 2. Initial Intake & Zero-Interruption Execution Directives

### A. Step 0: Initial Intake (Pre-Run)
When the orchestrator is executed, prompt the user for the following inputs (unless already provided):
1. **Target Website URL** (Required, e.g., `https://yourwebsite.com`)
2. **Business / Brand Name** (Required, e.g., `Acme Innovations`)
3. **Frontend Tech Stack** (Required, e.g., `Next.js App Router`, `React + Vite`, `Astro`, `Vue/Nuxt`, `WordPress`, `Static HTML/Tailwind`)
4. **Services Offered to Customers** (Required, e.g., `Custom Web App Development, Mobile App Engineering, Cloud Solutions, UI/UX Design`)
5. **Required Keywords for Search Crawl** (Required, e.g., `custom software development company, react web development services, mobile app developers`)
6. **Target Geography / City** (Recommended, e.g., `Global`, `United States`, `India & Global`)
7. **Target Audience / Customer Persona** (Optional, e.g., `Startups, SMEs, Enterprises`)

### B. Stages 1–9: Zero-Interruption Execution
🛑 **CRITICAL DIRECTIVE: ZERO INTERMEDIATE QUESTIONS / ZERO INTERRUPTIONS**
- Once the user supplies the Step 0 inputs, **NEVER prompt or halt execution to ask questions mid-run**.
- Every skill must automatically resolve its parameters using:
  1. **The Step 0 User Inputs** (Target URL, Business Name, Region, Tech Stack, Services Offered, Required Search Crawl Keywords).
  2. **Previous Skill Responses:** Step N reads the markdown output of Step N-1 (and earlier steps) directly from `outputs/`.
- **Frontend Tech Stack:** Apply the stack specified by the user. If left unspecified, default to **Next.js (App Router)** automatically. Never halt mid-run to ask.
- **Missing Optional Information:** If credentials (Search Console, GA4) or specific business details (exact phone number) are unprovided, record them as documented limitations or placeholders (`[To be verified in Search Console]`) and continue immediately.

**Tech Stack Code Generation Specs for Step 9:**
- **Next.js App Router (Default):** Outputs `export const metadata: Metadata = { ... }` in TypeScript and Server Component metadata.
- **Next.js Pages Router / React:** Outputs `<Head>` component blocks or `react-helmet-async`.
- **Astro:** Outputs `<BaseLayout>` frontmatter props.
- **Static HTML / WordPress:** Outputs standard document `<head>` markup and CMS custom fields.

---

## 3. Strict Sequential Execution Directives

1. **Strictly Sequential:** Never execute skills in parallel. Step N cannot begin until Step N-1 has status `COMPLETED`.
2. **Context Continuity:** Step N must read the generated output file(s) of previous steps from `outputs/` before formulating recommendations.
3. **Autonomous Operation:** Zero runtime questions to the user. All inputs are resolved from static baselines or upstream artifacts.
4. **Current Workspace Outputs Directory:** Every skill MUST write its complete markdown report directly to `./outputs/` in the **CURRENT working repository** (`c:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs\`). NEVER write to external projects like `ai-job-agent`.
5. **Validation Gate:** Before proceeding to the next step, verify that the artifact file exists in `outputs/` and is non-empty.
6. **Final Implementation Artifact:** Stage 9 must generate `outputs/seo-updates.md` containing both the tech-stack-specific code implementations AND the embedded developer prompt.
7. **Execution State Logging:** Update `logs/pipeline-state.json` on every step transition (`PENDING` ➔ `IN_PROGRESS` ➔ `COMPLETED` / `FAILED`).

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
