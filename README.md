# Complete 8-Skill Master SEO Automation System

An enterprise-grade, sequential multi-agent SEO automation system featuring nine standardized, non-overlapping production skills and automated workflow pipelines.

---

## 1. Directory Structure

```
seo-orchestration-flow/
│
├── .agents/
│   └── skills/
│       ├── master-orchestrator/
│       │   └── SKILL.md             # ⭐ Master Workflow Engine & Pipeline Controller
│       ├── seo-audit/
│       │   └── SKILL.md             # Baseline site crawl, health scorecard & URL catalog
│       ├── technical-seo/
│       │   └── SKILL.md             # GSC index coverage, server headers & Core Web Vitals
│       ├── keyword-research/
│       │   └── SKILL.md             # Query discovery, search intent & page-to-keyword mapping
│       ├── on-page-seo/
│       │   └── SKILL.md             # Page-by-page metadata, headings, internal links & schema
│       ├── local-seo/
│       │   └── SKILL.md             # Google Business Profile, map pack & LocalBusiness schema
│       ├── off-page-seo/
│       │   └── SKILL.md             # Backlink profile health, unlinked brand mentions & PR
│       ├── content-generation/
│       │   └── SKILL.md             # Production-ready landing page copy, articles & schema
│       └── monitoring-and-reporting/
│           └── SKILL.md             # Ongoing GA4/GSC tracking, striking distance & KPI reports
│
├── workflows/
│   ├── seo-workflow.json            # Complete 8-skill master automated execution pipeline
│   ├── resume-workflow.json         # Resume ATS analysis & tailored rewrite pipeline
│   └── content-workflow.json        # Keyword research to reader-first content pipeline
│
├── outputs/                         # Destination directory for all generated deliverables
│   ├── .gitkeep
│   ├── seo-audit-report.md          # (Step 1 deliverable)
│   ├── technical-seo-report.md      # (Step 2 deliverable)
│   ├── keyword-research-report.md   # (Step 3 deliverable)
│   ├── on-page-seo-report.md        # (Step 4 deliverable)
│   ├── local-seo-report.md          # (Step 5 deliverable)
│   ├── off-page-seo-report.md       # (Step 6 deliverable)
│   ├── generated-content.md         # (Step 7 deliverable)
│   ├── seo-monitoring-report.md     # (Step 8 deliverable)
│   └── seo-updates.md               # 🚀 (Step 9 actionable code updates + embedded AI prompt)
│
├── prompts/
│   └── apply-seo-updates.md         # Dedicated production prompt to apply updates to website
│
├── logs/                            # Real-time state tracking & execution audit trail
│   ├── .gitkeep
│   └── pipeline-state.json
│
├── orchestrator.md                  # Single-command trigger file for instant 8-skill execution
├── AGENTS.md                        # Project-level agent operational directives & guardrails
└── README.md                        # Complete system architecture documentation
```

---

## 2. Complete 8-Skill Master Sequential Flowchart

The master SEO workflow begins with confirming the website's frontend tech stack, then executes in strict chronological order across all 8 specialized skills, culminating in **`outputs/seo-updates.md`** (which houses the developer apply prompt and code snippets):

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

## 3. Complete Skill Catalog & Deliverables Matrix

| Step | Skill Name | Operational Domain | Upstream Prerequisite | Generated Deliverable |
| :--- | :--- | :--- | :--- | :--- |
| **00** | *Tech Stack Inquiry* | Asks user what frontend stack the site uses (Next.js, React, Astro, WordPress, HTML). | User Input | Context for Step 9 |
| **01** | `seo-audit` | Baseline site crawl, health scorecard, broken links, mobile usability, and URL catalog. | Initial User Inputs | `outputs/seo-audit-report.md` |
| **02** | `technical-seo` | Server response headers, HSTS, JS rendering, GSC crawl errors, Core Web Vitals remediation. | `outputs/seo-audit-report.md` | `outputs/technical-seo-report.md` |
| **03** | `keyword-research` | Primary/secondary/long-tail keyword discovery, search intent, and Keyword-to-Page mapping. | `outputs/seo-audit-report.md` | `outputs/keyword-research-report.md` |
| **04** | `on-page-seo` | Title tags, meta descriptions, H1-H3 hierarchy, image alt text, internal links, JSON-LD schema. | `outputs/seo-audit-report.md` + `outputs/keyword-research-report.md` | `outputs/on-page-seo-report.md` |
| **05** | `local-seo` | Google Business Profile (GBP), local 3-pack, NAP consistency, reviews, LocalBusiness schema. | `outputs/keyword-research-report.md` | `outputs/local-seo-report.md` |
| **06** | `off-page-seo` | Backlink profile audit, competitor link gaps, unlinked brand reclamation, white-hat digital PR. | `outputs/keyword-research-report.md` | `outputs/off-page-seo-report.md` |
| **07** | `content-generation`| Publication-ready landing page copy, FAQs, and rich snippet structured data code. | `outputs/keyword-research-report.md` + `outputs/on-page-seo-report.md` | `outputs/generated-content.md` |
| **08** | `monitoring-and-reporting`| GA4/GSC tracking baseline, striking distance query dashboard, and monthly KPI report. | All Upstream Reports | `outputs/seo-monitoring-report.md` |
| **09** | `compile-seo-updates`| Consolidates all code updates tailored to the frontend stack, embedding the developer apply prompt. | All 8 Upstream Deliverables | **`outputs/seo-updates.md`** |

---

## 4. Applying SEO Updates to Your Website

Once all skills complete, open [outputs/seo-updates.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/outputs/seo-updates.md).

Right at the top of the file is the **Production-Ready Developer Prompt**, tailored to your frontend framework. You can copy and paste it into any AI coding agent (Antigravity, Cursor, Claude Code, Copilot, ChatGPT) or assign it to a frontend developer to apply the changes directly to your website codebase.

---

## 5. How to Run

### Method A: Single-Command File Execution (Antigravity IDE)
Simply send this command in the chat:
```markdown
Run orchestrator.md
```
*(or type `@orchestrator.md execute`)*

The agent will ask for your frontend tech stack (if not already specified), then automatically execute all 8 stages + compilation in sequential order without stopping.

---

### Method B: Native Skill Invocation
```markdown
$master-orchestrator

Execute workflows/seo-workflow.json for:
- Website URL: https://strawhatdevs.com
- Business Name: Straw Hat Devs
- Frontend Tech Stack: Next.js (App Router)
- Target Country: India & Global Markets
```

---

### Method C: Running in ChatGPT
1. Copy or upload [orchestrator.md](file:///c:/Users/Sanjaikumar/Desktop/straw-hat-devs/seo-orchestration-flow/orchestrator.md) into ChatGPT.
2. Prompt: *"Execute this `orchestrator.md` sequentially step by step. Ask for my frontend tech stack first."*
3. ChatGPT will ask for your stack, run all 8 stages, and generate `outputs/seo-updates.md` with the embedded code prompt.
