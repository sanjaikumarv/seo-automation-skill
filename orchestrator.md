# SEO Workflow Master Orchestrator

Execute the complete end-to-end SEO automation workflow in **STRICT SEQUENTIAL** order.

When this file is called or executed, the AI assistant will automatically run each step one by one without stopping, passing the outputs from each completed step into the next.

---

## 1. Target Business Configuration

- **Target Website:** `https://strawhatdevs.com`
- **Business Name:** `Straw Hat Devs`
- **Target Country:** `India & Global`
- **Target Audience:** Startups, SMEs, and enterprises seeking custom software, web, and mobile app development
- **Execution Mode:** `STRICT_SEQUENTIAL`

---

## 2. Sequential Execution Pipeline

Execute the following stages strictly one after another:

### ─── STEP 1: Technical SEO Audit ───

- **Skill:** `.agents/skills/seo-audit/SKILL.md`
- **Action:**
  1. Inspect `https://strawhatdevs.com`.
  2. Audit technical SEO, HTTPS, canonical tags, robots.txt, and sitemap.xml.
  3. Catalog all discovered pages and services.
  4. Evaluate Core Web Vitals indicators and mobile responsiveness.
- **Output:** Save complete report to `outputs/seo-audit-report.md`.
- **Validation:** Ensure the _Discovered Pages Catalog_ is created.

---

### ─── STEP 2: Keyword Research & Intent Mapping ───

- **Skill:** `.agents/skills/keyword-research/SKILL.md`
- **Prerequisite Input:** Read `outputs/seo-audit-report.md`.
- **Action:**
  1. Extract discovered services and URLs from Step 1.
  2. Identify Primary Keywords (core commercial services).
  3. Identify Secondary, Long-Tail, and Local SEO queries.
  4. Classify search intent (Commercial, Transactional, Informational).
  5. Create a **Keyword-to-Page Mapping** assigning target queries to discovered URLs.
- **Output:** Save complete report to `outputs/keyword-research-report.md`.
- **Validation:** Ensure the _Keyword-to-Page Mapping Table_ is created.

---

### ─── STEP 3: SEO Content & Schema Generation ───

- **Skill:** `.agents/skills/content-generation/SKILL.md`
- **Prerequisite Inputs:** Read `outputs/seo-audit-report.md` and `outputs/keyword-research-report.md`.
- **Action:**
  1. Use mapped keywords from Step 2 to generate optimized Title tags (50-60 chars) and Meta descriptions (140-160 chars).
  2. Generate single H1 and H2-H3 heading hierarchies for primary service offerings.
  3. Draft high-ranking, reader-first body content addressing search intent.
  4. Generate copy-pasteable JSON-LD structured data (`Organization`, `Service`, `FAQPage`).
- **Output:** Save complete content package to `outputs/generated-content.md`.
- **Validation:** Ensure valid JSON-LD schema blocks are present.

---

## 3. Final Verification & Completion

1. Verify all three deliverables exist in `outputs/`:
   - `outputs/seo-audit-report.md`
   - `outputs/keyword-research-report.md`
   - `outputs/generated-content.md`
2. Update status in `logs/pipeline-state.json` to `COMPLETED`.
3. Present an executive summary with clickable links to all generated reports.
