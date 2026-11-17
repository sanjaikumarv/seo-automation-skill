# Workspace Guidelines for AI Agents: Multi-Workflow SEO Automation

## Operational Directives

### 1. Workflow Execution & Orchestration
All workflows must be coordinated using [.agents/skills/master-orchestrator/SKILL.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/.agents/skills/master-orchestrator/SKILL.md) or triggered via [orchestrator.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/orchestrator.md).

#### Mandatory Initial Setup (Tech Stack Inquiry)
Before executing Step 1, the AI agent MUST ask or confirm:
> *"What frontend tech stack / framework is your website built with?"*  
> *(Options: Next.js App Router, Next.js Pages Router, React + Vite, Astro, Vue/Nuxt, SvelteKit, Static HTML/PHP, WordPress, Shopify, Webflow)*

*Purpose:* This enables Step 9 to tailor code blocks (e.g. Next.js `generateMetadata` / `export const metadata: Metadata` vs React Helmet vs HTML `<head>`) and embed an exact, framework-native developer implementation prompt inside `outputs/seo-updates.md`.

#### Complete 8-Skill Master SEO Workflow (`workflows/seo-workflow.json` / `orchestrator.md`)
Execute in strict chronological order:
1. **`.agents/skills/seo-audit/SKILL.md`** ➔ writes `outputs/seo-audit-report.md`
2. **`.agents/skills/technical-seo/SKILL.md`** (reads Step 1) ➔ writes `outputs/technical-seo-report.md`
3. **`.agents/skills/keyword-research/SKILL.md`** (reads Step 1) ➔ writes `outputs/keyword-research-report.md`
4. **`.agents/skills/on-page-seo/SKILL.md`** (reads Steps 1 & 3) ➔ writes `outputs/on-page-seo-report.md`
5. **`.agents/skills/local-seo/SKILL.md`** (reads Steps 1 & 3) ➔ writes `outputs/local-seo-report.md`
6. **`.agents/skills/off-page-seo/SKILL.md`** (reads Steps 1 & 3) ➔ writes `outputs/off-page-seo-report.md`
7. **`.agents/skills/content-generation/SKILL.md`** (reads Steps 3 & 4) ➔ writes `outputs/generated-content.md`
8. **`.agents/skills/monitoring-and-reporting/SKILL.md`** (reads all steps) ➔ writes `outputs/seo-monitoring-report.md`
9. **Compile Master SEO Updates Package (`outputs/seo-updates.md`):** Consolidates all code, technical, metadata, heading, internal link, and schema changes into **`outputs/seo-updates.md`**, embedding the production-ready developer apply prompt directly at the top.

---

### 2. Inter-Skill Data Dependencies & Context Ingestion
- **Strict Sequential Order:** Never execute skills in parallel. A skill cannot start until all preceding prerequisite steps have finished with status `COMPLETED`.
- **Mandatory File Reading:** Before formulating recommendations, the running skill MUST read the output markdown files of prior steps from `outputs/`.
- **Grounded Recommendations:**
  - `technical-seo` must inspect the crawl issues identified in `outputs/seo-audit-report.md`.
  - `keyword-research` must map queries directly to the *Discovered Pages Catalog* from `outputs/seo-audit-report.md`.
  - `on-page-seo` must build metadata and heading hierarchies around the queries mapped in `outputs/keyword-research-report.md`.
  - `local-seo` must optimize for the geographic queries discovered in `outputs/keyword-research-report.md`.
  - `off-page-seo` must build link acquisition around core business services.
  - `content-generation` must incorporate verified keywords, headings, and schema blueprints.
  - Final Step must compile all concrete code modifications into `outputs/seo-updates.md`.

---

### 3. Artifact Persistence & State Logging
- **Deterministic File Naming:** Save all reports to `outputs/` using exact predetermined filenames.
- **State Audit Trail:** Log state transitions (`PENDING` ➔ `IN_PROGRESS` ➔ `COMPLETED` / `FAILED`) in [logs/pipeline-state.json](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/logs/pipeline-state.json).

---

### 4. Data Integrity & Google Search Essentials Compliance
- **No Fabricated Data:** Never invent search volumes, keyword difficulty numbers, PageSpeed scores, ranking positions, or backlink counts.
- **Document Limitations:** When authenticated access (Google Search Console, Google Analytics 4) is unavailable, explicitly label findings as *"Public observational search data; requires Google Search Console verification."*
- **White-Hat Only:** Strictly follow Google Search Essentials (Spam Policies). Never recommend PBNs, link schemes, cloaking, or keyword stuffing.
