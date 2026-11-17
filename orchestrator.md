# Complete SEO Workflow Master Orchestrator

Execute the complete end-to-end SEO automation workflow in **STRICT SEQUENTIAL** order across **ALL 8 specialized SEO skills**.

> 🛑 **EXECUTION PROTOCOL: INITIAL INTAKE ➔ ZERO-INTERRUPT RUNTIME**
> 1. **Initial Intake (Step 0):** Upon executing this orchestrator, the AI assistant **MUST prompt the user for the required input fields** listed in Section 1 below (unless the user already provided them in their triggering message). **Do not use hardcoded or prepopulated site values.**
> 2. **Zero Mid-Run Questions:** As soon as the user supplies the initial inputs, execute Step 1 through Step 9 completely autonomously in ONE continuous flow. **DO NOT stop between steps to ask questions.**
> 3. **Context Inheritance:** Downstream skills automatically consume the user's initial inputs and the outputs of completed upstream skills (`outputs/`).
> 4. **Missing Optional Data:** Never interrupt execution to ask for missing credentials (GSC, GA4) or exact phone numbers. Simply record them as documented limitations or placeholders and proceed automatically.
> 5. **Strict Current Output Directory:** All generated reports (Steps 1 through 9) MUST be saved directly into the **CURRENT workspace directory's outputs folder**: `./outputs/` (`c:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs\`). **NEVER** write or redirect outputs to external projects (such as `ai-job-agent`).

---

## 1. Required Input Fields (Initial Intake)

When this orchestrator is executed, prompt the user to provide the following details before starting Step 1:

| # | Field Name | Status | Description & Examples |
| :- | :--- | :--- | :--- |
| **1** | **Target Website URL** | **Required** | The full website URL to audit and optimize (e.g., `https://yourwebsite.com`). |
| **2** | **Business / Brand Name** | **Required** | The legal or trading name of the business (e.g., `Acme Innovations`). |
| **3** | **Frontend Tech Stack** | **Required** | Website framework: `Next.js (App Router)`, `Next.js (Pages Router)`, `React + Vite`, `Astro`, `Vue/Nuxt`, `WordPress`, `Static HTML/Tailwind`. *(Used by Step 9 to generate framework-accurate code).* |
| **4** | **Services Offered to Customers** | **Required** | Core services, solutions, or products delivered to clients (e.g., `Custom Web App Development, Mobile App Engineering, Cloud Solutions, UI/UX Design`). |
| **5** | **Required Keywords for Search Crawl** | **Required** | Specific seed keywords or priority queries to audit and target during search crawl & research (e.g., `custom software development company, react web development services, mobile app developers`). |
| **6** | **Target Geography / Location** | *Recommended* | Target market regions: `Global`, `United States`, `India & Global`, `London, UK`, `Coimbatore, India`, etc. |
| **7** | **Target Audience / Customer Persona** | *Optional* | Client profiles, industries, or demographics (e.g., `Seed/Series-A Startups, Enterprise CTOs, Local SMEs`). |

> **User Prompt Template (The AI must ask this upon initial execution):**
> 
> *"Please provide the following project details to start the complete SEO automation workflow:*
> 1. **Target Website URL:** (e.g., `https://yourwebsite.com`)
> 2. **Business / Brand Name:** (e.g., `Acme Innovations`)
> 3. **Frontend Tech Stack:** (e.g., `Next.js App Router`, `React + Vite`, `Astro`, `WordPress`, etc.)
> 4. **Services Offered to Customers:** (e.g., `Custom Web Development, Mobile Apps, Cloud Engineering`)
> 5. **Required Keywords for Search Crawl:** (e.g., `custom software company, web development services`)
> 6. **Target Geography / City:** (e.g., `Global`, `India & Global`, `Coimbatore`, etc.)
> 7. **Target Audience / Customer Persona:** *(optional, e.g., Startups, SMEs)*
> 
> *Once you reply with these details, I will execute all 8 SEO skills sequentially and compile the code updates without any further interruptions.*"

---

## 2. Autonomous Sequential Execution Pipeline

Execute the following stages strictly one after another without stopping:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   AUTONOMOUS 8-SKILL SEO MASTER PIPELINE               │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
       [0. Initial Intake: Gather Target URL, Business Name & Tech Stack]
                                    │
                                    ▼
       [1. seo-audit] ───────────────➔ outputs/seo-audit-report.md
              │ (Passes: Discovered Pages Catalog & Site Baseline)
              ▼
       [2. technical-seo] ───────────➔ outputs/technical-seo-report.md
              │ (Passes: Server Headers & Core Web Vitals Fixes)
              ▼
       [3. keyword-research] ────────➔ outputs/keyword-research-report.md
              │ (Passes: Keyword-to-Page Mapping & Intent Data)
              ▼
       [4. on-page-seo] ─────────────➔ outputs/on-page-seo-report.md
              │ (Passes: Metadata Specifications & JSON-LD Schemas)
              ▼
       [5. local-seo] ───────────────➔ outputs/local-seo-report.md
              │ (Passes: Local Map Pack & LocalBusiness Schema)
              ▼
       [6. off-page-seo] ────────────➔ outputs/off-page-seo-report.md
              │ (Passes: Competitor Link Gaps & PR Strategy)
              ▼
       [7. content-generation] ──────➔ outputs/generated-content.md
              │ (Passes: Production Copy & FAQ Snippets)
              ▼
       [8. monitoring-and-reporting] ➔ outputs/seo-monitoring-report.md
              │ (Passes: GA4/GSC KPI Dashboard & Trajectory)
              ▼
       [9. Compile SEO Updates] ─────➔ outputs/seo-updates.md
              │
              ▼
   ALL OUTPUTS PERSISTED & DEPLOYMENT PROMPT DISPLAYED
```

---

### ─── STEP 1: Technical SEO Baseline Audit ───
- **Skill File:** `.agents/skills/seo-audit/SKILL.md`
- **Input Source:** User inputs collected in Step 0 Intake (Target URL, Services Offered, Required Keywords). *(Do not prompt user again).*
- **Action:** 
  1. Inspect the target website URL provided by the user.
  2. Audit technical SEO, HTTPS, canonical tags, robots.txt, and sitemap.xml.
  3. Catalog all discovered pages and services (*Discovered Pages Catalog*), cross-referencing user services.
  4. Evaluate crawl presence for pages targeting the user's required keywords.
  5. Evaluate Core Web Vitals indicators and mobile responsiveness.
- **Output:** Save complete report to `outputs/seo-audit-report.md`.
- **Handoff:** Automatically pass the *Discovered Pages Catalog* to Step 2 & 3.

---

### ─── STEP 2: Advanced Technical SEO & Infrastructure Deep-Dive ───
- **Skill File:** `.agents/skills/technical-seo/SKILL.md`
- **Input Source:** Step 1 Output (`outputs/seo-audit-report.md`). *(Do not prompt user).*
- **Action:**
  1. Diagnose server response headers (HSTS, CSP, Cache-Control, Brotli/Gzip).
  2. Inspect JavaScript rendering (CSR vs SSR/SSG DOM parity and Googlebot rendering overhead).
  3. Analyze sitemap index protocol validity and URL cleanliness.
  4. Formulate code-level Core Web Vitals fixes (LCP preloads, INP script deferral, CLS aspect-ratio).
- **Output:** Save complete report to `outputs/technical-seo-report.md`.
- **Handoff:** Automatically pass server & technical fixes to Step 9.

---

### ─── STEP 3: Keyword Research & Search Intent Mapping ───
- **Skill File:** `.agents/skills/keyword-research/SKILL.md`
- **Input Source:** Step 0 User Inputs (Services Offered & Required Keywords for Crawl) + Step 1 Discovered Pages Catalog. *(Do not prompt user).*
- **Action:**
  1. Ingest the user's required search crawl keywords and customer services as primary seed queries.
  2. Expand into Primary, Secondary, Long-Tail, and Local SEO queries across target geography.
  3. Classify search intent (Commercial, Transactional, Informational).
  4. Create a **Keyword-to-Page Mapping** assigning target queries directly to discovered URLs and services.
- **Output:** Save complete report to `outputs/keyword-research-report.md`.
- **Handoff:** Automatically pass the *Keyword-to-Page Mapping Table* to Steps 4, 5, and 7.

---

### ─── STEP 4: Page-by-Page On-Page SEO Optimization ───
- **Skill File:** `.agents/skills/on-page-seo/SKILL.md`
- **Input Source:** Step 1 Pages Catalog + Step 3 Keyword Mappings. *(Do not prompt user).*
- **Action:**
  1. Use mapped keywords from Step 3 to generate optimized Title tags (50-60 chars) and Meta descriptions (140-160 chars) for each page.
  2. Formulate H1-H3 heading hierarchies for critical pages.
  3. Design contextual internal linking graph connecting discovered pages.
  4. Generate copy-pasteable JSON-LD structured data (`Organization`, `Service`, `FAQPage`).
- **Output:** Save complete on-page specifications to `outputs/on-page-seo-report.md`.
- **Handoff:** Automatically pass metadata specs, internal links, and schemas to Steps 7 and 9.

---

### ─── STEP 5: Local SEO & Google Business Profile (Map Pack) ───
- **Skill File:** `.agents/skills/local-seo/SKILL.md`
- **Input Source:** Step 0 Target Geography + Step 3 Local Keywords. *(Do not prompt user).*
- **Action:**
  1. Audit Google Business Profile categories, description, visual assets, and services list.
  2. Audit Name, Address, Phone (NAP) citation consistency across major directories.
  3. Formulate customer review generation campaign and response protocols.
  4. Generate `LocalBusiness` / `ProfessionalService` JSON-LD schema snippet.
- **Output:** Save complete report to `outputs/local-seo-report.md`.
- **Handoff:** Automatically pass LocalBusiness schema to Step 9.

---

### ─── STEP 6: Off-Page Authority, Link Gaps & Digital PR ───
- **Skill File:** `.agents/skills/off-page-seo/SKILL.md`
- **Input Source:** Step 0 User Inputs + Step 3 Service Topics. *(Do not prompt user).*
- **Action:**
  1. Audit backlink profile health and anchor text diversity.
  2. Identify competitor backlink gap opportunities (referring domains linking to competitors).
  3. Formulate unlinked brand mention reclamation outreach playbook.
  4. Develop 2-3 data-driven digital PR campaign concepts.
- **Output:** Save complete report to `outputs/off-page-seo-report.md`.

---

### ─── STEP 7: Production Content & Landing Page Generation ───
- **Skill File:** `.agents/skills/content-generation/SKILL.md`
- **Input Source:** Step 3 Target Keywords + Step 4 Heading Structures. *(Do not prompt user).*
- **Action:**
  1. Draft publication-ready copy for the primary service landing page.
  2. Integrate semantic keywords naturally and address user search intent.
  3. Format with finalized H1-H3 headings, FAQ sections, and schema blocks.
- **Output:** Save complete content package to `outputs/generated-content.md`.

---

### ─── STEP 8: Ongoing Analytics & Performance Monitoring Baseline ───
- **Skill File:** `.agents/skills/monitoring-and-reporting/SKILL.md`
- **Input Source:** Ingests all previous reports (Steps 1–7). *(Do not prompt user).*
- **Action:**
  1. Establish GA4 organic traffic and conversion tracking framework.
  2. Configure GSC striking distance query analysis framework (queries in positions 4-10).
  3. Set up monthly KPI dashboard template (sessions, CTR, average position, conversions).
  4. Formulate the ongoing optimization roadmap for the next reporting period.
- **Output:** Save complete report to `outputs/seo-monitoring-report.md`.

---

### ─── STEP 9: Compile Master Actionable SEO Updates Package (outputs/seo-updates.md) ───
- **Input Source:** Ingests all completed responses from Steps 1 through 8. *(Do not prompt user).*
- **Action:**
  1. Consolidate every code-ready change from all 8 upstream reports into `outputs/seo-updates.md`.
  2. Format code specifically for the **Frontend Tech Stack** confirmed in Step 0 (e.g. Next.js App Router TypeScript metadata, React components, Astro props, or HTML head tags).
  3. **Include the Production-Ready Developer Apply Prompt directly at the top of `outputs/seo-updates.md`** for immediate copy-pasting into an AI coding agent or developer handoff.
- **Output:** Save the complete package to `outputs/seo-updates.md`.

---

## 3. Final Verification & Completion

1. Verify all 9 deliverables exist in `outputs/`:
   - `outputs/seo-audit-report.md`
   - `outputs/technical-seo-report.md`
   - `outputs/keyword-research-report.md`
   - `outputs/on-page-seo-report.md`
   - `outputs/local-seo-report.md`
   - `outputs/off-page-seo-report.md`
   - `outputs/generated-content.md`
   - `outputs/seo-monitoring-report.md`
   - `outputs/seo-updates.md`
2. Update status in `logs/pipeline-state.json` to `COMPLETED`.
3. Display the final completion summary and direct the user to `outputs/seo-updates.md`.
