# Universal Dynamic Input Variables Reference

This document defines the standardized universal dynamic variables used across the complete SEO skills ecosystem. Every skill within `.agents/skills/` must ingest and resolve these dynamic variables without hardcoding project, domain, or company details.

---

## 1. Universal Variable Schema

| Variable Name | Description | Example Value | Required / Optional |
|---|---|---|---|
| `{{WEBSITE_URL}}` | Complete target website root URL with protocol and no trailing slash | `https://example.com` | **Required** |
| `{{DOMAIN_NAME}}` | Host domain name without protocol, www, or trailing slash | `example.com` | **Required** |
| `{{WEBSITE_NAME}}` | Human-readable name of the website or business entity | `Example Corp` | **Required** |
| `{{BRAND_NAME}}` | Official brand or company name for entity SEO and schema | `Example` | **Required** |
| `{{TARGET_COUNTRY}}` | Primary country targeted for organic search rankings (ISO-3166 alpha-2 or full name) | `United States` (`US`) | **Required** |
| `{{TARGET_GEOGRAPHY}}` | Regional, metropolitan, or localized search scope | `Global`, `National`, or `Austin, TX` | **Required** |
| `{{TARGET_AUDIENCE}}` | Target buyer persona, industry vertical, or customer segment | `B2B Enterprise CTOs & VP Engineering` | Optional |
| `{{BUSINESS_TYPE}}` | Business model category (SaaS, Agency, E-commerce, Local Business, Healthcare, etc.) | `Digital Engineering Consultancy` | **Required** |
| `{{SERVICES}}` | Comma-delimited list of core services or product lines offered to customers | `Custom Software Development, Cloud Architecture, DevOps` | **Required** |
| `{{SEED_KEYWORDS}}` | Comma-delimited initial seed keywords for crawl and discovery | `software development services, cloud migration agency` | **Required** |
| `{{COMPETITORS}}` | Comma-delimited list of primary organic search competitors | `competitor-a.com, competitor-b.com` | Optional |
| `{{SEO_OBJECTIVE}}` | Primary objective for this SEO optimization campaign | `Increase qualified B2B organic demo bookings by 40%` | Optional |
| `{{BRAND_VOICE}}` | Tone and style guidelines for content generation | `Authoritative, technical, concise, developer-centric` | Optional |
| `{{CURRENT_DATE}}` | Dynamic execution date formatted strictly as `YYYY-MM-DD` | `2025-01-15` | **Required** |
| `{{PROJECT_ID}}` | Unique alphanumeric identifier for project tracking | `proj-example-001` | Optional |

---

## 2. Ingestion Hierarchy

All skills must resolve input variables in the following priority order:

1. **Step 0 Intake / Orchestrator Context:** Variables passed directly from `seo-orchestrator` or the user's initial intake prompt.
2. **Upstream Skill Deliverables:** Upstream completed markdown reports (e.g. `SEO_Audit_Report.md`, `Keyword_Research_Report.md`).
3. **Canonical Placeholders:** If an optional variable is absent, fall back to safe defaults or record a placeholder (e.g., `[Not Specified; defaults to Global]`). **Never halt autonomous execution or fabricate unverified values.**

---

## 3. Variable Replacement Rules

- **Domain Isolation:** Never write hardcoded domain names into reusable skill logic. Use `{{DOMAIN_NAME}}`.
- **URL Isolation:** Always use `{{WEBSITE_URL}}` for root crawl targets.
- **Entity Isolation:** Always use `{{WEBSITE_NAME}}` or `{{BRAND_NAME}}` instead of hardcoded company names.
- **Date Isolation:** Never hardcode calendar dates. Always compute and use `{{CURRENT_DATE}}` formatted as `YYYY-MM-DD`.
