# Workspace Guidelines for AI Agents: Multi-Workflow SEO Automation

## Operational Directives

### 1. Workflow Execution & Orchestration
All workflows must be coordinated using [.agents/skills/master-orchestrator/SKILL.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/.agents/skills/master-orchestrator/SKILL.md) or triggered via [orchestrator.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/orchestrator.md).

#### Initial Intake & Autonomous Zero-Interruption Rule
- **Step 0 Initial Intake:** When triggered via [orchestrator.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/orchestrator.md) or the orchestrator skill, the AI agent **MUST prompt the user for the required input fields** (Target Website URL, Business Name, Frontend Tech Stack, Services Offered to Customers, Required Keywords for Search Crawl, and Target Geography) if not already provided in the opening prompt. **Do not assume or use hardcoded/prepopulated site values.**
- **Zero Mid-Run Questions:** Once the user provides the initial intake parameters, execute Step 1 through Step 9 in strict sequential order without asking any intermediate questions.
- **Input Ingestion Hierarchy:**
  1. **User Intake Inputs (Step 0):** Used by Step 1 (`seo-audit` - URL, crawl verification for required keywords & services), Step 3 (`keyword-research` - seed queries & services mapping), Step 5 (`local-seo`), Step 6 (`off-page-seo`), and Step 9 (`seo-updates.md`).
  2. **Previous Skill Responses:** Downstream skills must automatically read the output markdown files (`outputs/`) of upstream completed skills.
  3. **Missing Optional Data:** Never interrupt execution to ask for missing credentials (GSC, GA4) or exact phone numbers. Record them as documented limitations or placeholders (e.g., `[To be verified in Search Console]`) and proceed immediately.
- **Frontend Tech Stack Handling:** Apply the tech stack specified by the user in Step 0. If the user leaves it blank or unspecified, default to **Next.js (App Router) / React / Tailwind CSS** automatically. This ensures Step 9 generates framework-native code blocks and embeds the tailored developer prompt directly into `outputs/seo-updates.md`.

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

### 3. Artifact Persistence & Current Workspace Directory Guardrail
- **MANDATORY CURRENT DIRECTORY PATH:** All output markdown files MUST be written directly to the `outputs/` folder of the **CURRENT active workspace directory** (`./outputs/` or `c:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs\`).
- **PROHIBITION:** NEVER write, redirect, or copy output files to external directories (such as `ai-job-agent` or any parent/sibling folders).
- **Deterministic File Naming:** Save all reports to `./outputs/` using exact predetermined filenames.
- **State Audit Trail:** Log state transitions (`PENDING` ➔ `IN_PROGRESS` ➔ `COMPLETED` / `FAILED`) in [logs/pipeline-state.json](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/logs/pipeline-state.json).

---

### 4. Data Integrity & Google Search Essentials Compliance
- **No Fabricated Data:** Never invent search volumes, keyword difficulty numbers, PageSpeed scores, ranking positions, or backlink counts.
- **Document Limitations:** When authenticated access (Google Search Console, Google Analytics 4) is unavailable, explicitly label findings as *"Public observational search data; requires Google Search Console verification."*
- **White-Hat Only:** Strictly follow Google Search Essentials (Spam Policies). Never recommend PBNs, link schemes, cloaking, or keyword stuffing.
