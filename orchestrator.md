# Complete SEO Workflow Master Orchestrator

Execute the complete end-to-end SEO automation workflow in **STRICT SEQUENTIAL** order across **ALL 8 specialized SEO skills**.

When this file is called or executed, the AI assistant will:
1. **First, ask or confirm the website's frontend tech stack** (e.g., Next.js App/Pages Router, React/Vite, Astro, Nuxt, HTML, WordPress).
2. Sequentially execute each skill step by step, passing upstream outputs to downstream skills.
3. Generate **`outputs/seo-updates.md`** containing framework-accurate code snippets and an embedded, production-ready developer prompt to apply the changes directly to your codebase.

---

## 1. Target Business & Tech Stack Configuration

- **Target Website:** `https://strawhatdevs.com`
- **Business Name:** `Straw Hat Devs`
- **Target Country:** `India & Global`
- **Target City / Region:** `Coimbatore / Tamil Nadu / Global`
- **Target Audience:** Startups, SMEs, and enterprises seeking custom software, web, and mobile app development
- **Frontend Tech Stack:** `{{frontend_tech_stack}}` *(Confirm with user at start)*
- **Execution Mode:** `STRICT_SEQUENTIAL`

> **IMPORTANT INITIAL STEP (TECH STACK INQUIRY):**
> Before executing the pipeline, the AI must ask or confirm:
> *"What frontend tech stack / framework is your website built with?"*
> *(Options: Next.js App Router, Next.js Pages Router, React + Vite, Astro, Vue/Nuxt, SvelteKit, Static HTML/PHP, WordPress, Shopify, Webflow)*
> 
> *Purpose:* Knowing the tech stack allows Step 9 to generate framework-accurate code (e.g. Next.js `export const metadata: Metadata` vs React Helmet vs HTML `<head>`) and a tailored implementation prompt inside `outputs/seo-updates.md`.

---

## 2. Complete 8-Skill Sequential Execution Pipeline

Execute the following stages strictly one after another:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   COMPLETE 8-SKILL SEO MASTER PIPELINE                 │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                                    ▼
       [0. Confirm Frontend Tech Stack (e.g. Next.js, React, Astro)]
                                    │
                                    ▼
       [1. seo-audit] ───────────────➔ outputs/seo-audit-report.md
              │
              ▼
       [2. technical-seo] ───────────➔ outputs/technical-seo-report.md
              │
              ▼
       [3. keyword-research] ────────➔ outputs/keyword-research-report.md
              │
              ▼
       [4. on-page-seo] ─────────────➔ outputs/on-page-seo-report.md
              │
              ▼
       [5. local-seo] ───────────────➔ outputs/local-seo-report.md
              │
              ▼
       [6. off-page-seo] ────────────➔ outputs/off-page-seo-report.md
              │
              ▼
       [7. content-generation] ──────➔ outputs/generated-content.md
              │
              ▼
       [8. monitoring-and-reporting] ➔ outputs/seo-monitoring-report.md
              │
              ▼
       [9. Compile SEO Updates] ─────➔ outputs/seo-updates.md
              │
              ▼
   PROMPT EMBEDDED IN outputs/seo-updates.md FOR CODE DEPLOYMENT
```

---

### ─── STEP 1: Technical SEO Baseline Audit ───
- **Skill File:** `.agents/skills/seo-audit/SKILL.md`
- **Action:** 
  1. Inspect `https://strawhatdevs.com`.
  2. Audit technical SEO, HTTPS, canonical tags, robots.txt, and sitemap.xml.
  3. Catalog all discovered pages and services (*Discovered Pages Catalog*).
  4. Evaluate Core Web Vitals indicators and mobile responsiveness.
- **Output:** Save complete report to `outputs/seo-audit-report.md`.
- **Validation Gate:** Ensure the *Discovered Pages Catalog* is compiled.

---

### ─── STEP 2: Advanced Technical SEO & Infrastructure Deep-Dive ───
- **Skill File:** `.agents/skills/technical-seo/SKILL.md`
- **Prerequisite Input:** Read `outputs/seo-audit-report.md`.
- **Action:**
  1. Diagnose server response headers (HSTS, CSP, Cache-Control, Brotli/Gzip).
  2. Inspect JavaScript rendering (CSR vs SSR/SSG DOM parity and Googlebot rendering overhead).
  3. Analyze sitemap index protocol validity and URL cleanliness.
  4. Formulate code-level Core Web Vitals fixes (LCP preloads, INP script deferral, CLS aspect-ratio).
- **Output:** Save complete report to `outputs/technical-seo-report.md`.
- **Validation Gate:** Ensure server configuration and Core Web Vitals code fixes are present.

---

### ─── STEP 3: Keyword Research & Search Intent Mapping ───
- **Skill File:** `.agents/skills/keyword-research/SKILL.md`
- **Prerequisite Input:** Read `outputs/seo-audit-report.md`.
- **Action:**
  1. Extract discovered services and URLs from Step 1.
  2. Identify Primary Keywords (core commercial services).
  3. Identify Secondary, Long-Tail, and Local SEO queries.
  4. Classify search intent (Commercial, Transactional, Informational).
  5. Create a **Keyword-to-Page Mapping** assigning target queries to discovered URLs.
- **Output:** Save complete report to `outputs/keyword-research-report.md`.
- **Validation Gate:** Ensure the *Keyword-to-Page Mapping Table* is compiled.

---

### ─── STEP 4: Page-by-Page On-Page SEO Optimization ───
- **Skill File:** `.agents/skills/on-page-seo/SKILL.md`
- **Prerequisite Inputs:** Read `outputs/seo-audit-report.md` and `outputs/keyword-research-report.md`.
- **Action:**
  1. Use mapped keywords from Step 3 to generate optimized Title tags (50-60 chars) and Meta descriptions (140-160 chars) for each page.
  2. Formulate H1-H3 heading hierarchies for critical pages.
  3. Design contextual internal linking graph connecting discovered pages.
  4. Generate copy-pasteable JSON-LD structured data (`Organization`, `Service`, `FAQPage`).
- **Output:** Save complete on-page specifications to `outputs/on-page-seo-report.md`.
- **Validation Gate:** Ensure valid metadata and JSON-LD schema blocks are present.

---

### ─── STEP 5: Local SEO & Google Business Profile (Map Pack) ───
- **Skill File:** `.agents/skills/local-seo/SKILL.md`
- **Prerequisite Inputs:** Read `outputs/seo-audit-report.md` and `outputs/keyword-research-report.md`.
- **Action:**
  1. Audit Google Business Profile categories, description, visual assets, and services list.
  2. Audit Name, Address, Phone (NAP) citation consistency across major directories.
  3. Formulate customer review generation campaign and response protocols.
  4. Generate `LocalBusiness` / `ProfessionalService` JSON-LD schema snippet.
- **Output:** Save complete report to `outputs/local-seo-report.md`.
- **Validation Gate:** Ensure LocalBusiness schema and NAP consistency matrix are present.

---

### ─── STEP 6: Off-Page Authority, Link Gaps & Digital PR ───
- **Skill File:** `.agents/skills/off-page-seo/SKILL.md`
- **Prerequisite Inputs:** Read `outputs/seo-audit-report.md` and `outputs/keyword-research-report.md`.
- **Action:**
  1. Audit backlink profile health and anchor text diversity.
  2. Identify competitor backlink gap opportunities (referring domains linking to competitors).
  3. Formulate unlinked brand mention reclamation outreach playbook.
  4. Develop 2-3 data-driven digital PR campaign concepts.
- **Output:** Save complete report to `outputs/off-page-seo-report.md`.
- **Validation Gate:** Ensure competitor link gap and digital PR sections are present.

---

### ─── STEP 7: Production Content & Landing Page Generation ───
- **Skill File:** `.agents/skills/content-generation/SKILL.md`
- **Prerequisite Inputs:** Read `outputs/keyword-research-report.md` and `outputs/on-page-seo-report.md`.
- **Action:**
  1. Draft publication-ready copy for the primary service landing page.
  2. Integrate semantic keywords naturally and address user search intent.
  3. Format with finalized H1-H3 headings, FAQ sections, and schema blocks.
- **Output:** Save complete content package to `outputs/generated-content.md`.
- **Validation Gate:** Verify that complete body content is present.

---

### ─── STEP 8: Ongoing Analytics & Performance Monitoring Baseline ───
- **Skill File:** `.agents/skills/monitoring-and-reporting/SKILL.md`
- **Prerequisite Inputs:** Read all upstream deliverables.
- **Action:**
  1. Establish GA4 organic traffic and conversion tracking framework.
  2. Configure GSC striking distance query analysis framework (queries in positions 4-10).
  3. Set up monthly KPI dashboard template (sessions, CTR, average position, conversions).
  4. Formulate the ongoing optimization roadmap for the next reporting period.
- **Output:** Save complete report to `outputs/seo-monitoring-report.md`.
- **Validation Gate:** Ensure KPI scorecard and striking distance query framework are present.

---

### ─── STEP 9: Compile Master Actionable SEO Updates Package (outputs/seo-updates.md) ───
- **Action:**
  1. Consolidate every code-ready change from all 8 upstream reports into `outputs/seo-updates.md`.
  2. **Tailor code to the confirmed frontend tech stack:**
     - Next.js App Router: `export const metadata: Metadata = { ... }` and React component code.
     - Next.js Pages Router: `<Head>` with Next.js imports.
     - React / Vite: `react-helmet-async` tags and JSX.
     - Astro: `<BaseLayout>` frontmatter props.
     - HTML/PHP: Clean standard markup.
  3. **Include the Production-Ready Developer Apply Prompt directly at the top of `outputs/seo-updates.md`** so anyone opening the file can copy-paste it immediately into their coding agent (Antigravity, Cursor, Claude Code, Copilot) or assign it to a developer.
- **Output:** Save the complete package to `outputs/seo-updates.md`.

---

## 3. Final Deliverables Register & Embedded Apply Prompt

Verify all 9 deliverables exist in `outputs/`:
1. `outputs/seo-audit-report.md`
2. `outputs/technical-seo-report.md`
3. `outputs/keyword-research-report.md`
4. `outputs/on-page-seo-report.md`
5. `outputs/local-seo-report.md`
6. `outputs/off-page-seo-report.md`
7. `outputs/generated-content.md`
8. `outputs/seo-monitoring-report.md`
9. **`outputs/seo-updates.md` (Contains full code diffs AND the embedded AI developer implementation prompt)**

Update status in `logs/pipeline-state.json` to `COMPLETED`.
