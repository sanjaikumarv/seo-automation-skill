# Workspace Guidelines for AI Agents

Use [seo-orchestrator.md](seo-orchestrator.md) or the [SEO Orchestrator skill](.agents/skills/seo-orchestrator/SKILL.md) for the full SEO workflow. The skill defines the stage order, handoffs, and deliverables for the nine SEO skills in this workspace.

See [workspace maintenance](docs/workspace-maintenance.md) for the folder conventions and cleanup process.

- Complete Step 0 before starting the audit. Use the current user's website URL, business name, services, seed queries, and target geography. Use their frontend stack when supplied, otherwise default the developer handoff to Next.js (App Router) / React / Tailwind CSS and flag the assumption for repository verification.
- Run one stage at a time, read its required upstream outputs from this run, and verify its artifacts before starting the next stage. Record missing optional data as limitations and continue without mid-run questions.
- Keep all generated reports within the active workspace's `outputs/` directory governed by `OUT_PUT_ROOT_FOLDER` (defaulting to `C:\Users\Sanjaikumar\Desktop\straw-hat-devs\seo-orchestration-flow\outputs`). Structure run artifacts under `{OUT_PUT_ROOT_FOLDER}/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/{{STAGE_FOLDER}}/` (`00-orchestration/` through `09-final-seo-report/`).
- Every stage must generate two core deliverables: `<skill-name>-overall-report.md` (strategic analysis) and `<skill-name>-website-changes.md` (page-by-page register of concrete website modifications).
- Report verifiable SEO evidence only and follow Google Search Essentials. When authenticated search or analytics data is unavailable, label applicable findings “Public observational search data; requires Google Search Console verification.”
