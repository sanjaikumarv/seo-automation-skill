# Standardized SEO Research & Data Gathering Guidelines

This document outlines the protocols for crawling, public data harvesting, search intent classification, and handling missing data across all SEO skills.

---

## 1. Respectful Crawling Protocol

- **User-Agent:** Identify clearly or use standard browser emulation user-agent strings.
- **Request Throttling:** Observe politeness delay (minimum 500ms between requests) to prevent server overload or rate limiting.
- **Respect robots.txt:** Honor crawl-delay and disallow directives unless specifically performing an audit on why assets are blocked.
- **Error Backoff:** On HTTP 429 (Too Many Requests) or 503 (Service Unavailable), implement exponential backoff.

---

## 2. Autonomous Execution & Missing Data Handling

To guarantee autonomous zero-interruption execution across the master pipeline:

1. **Step 0 Intake Boundaries:** Intake variables (`{{WEBSITE_URL}}`, `{{WEBSITE_NAME}}`, `{{SERVICES}}`, etc.) are established at pipeline start.
2. **Never Interrupt for Missing Optional Credentials:** If Search Console, GA4, or third-party paid API tokens are not provided, do not pause or prompt the user.
3. **Explicit Documentation:** Document missing authenticated data using canonical placeholders:
   - `[Public observational search data; requires Google Search Console verification]`
   - `[To be verified in Search Console]`
   - `[GA4 conversion tracking data pending property access]`
4. **Graceful Fallbacks:** Use public HTTP requests, public SERP data, and client-side DOM parsing to proceed autonomously.

---

## 3. Search Intent Taxonomy

Every target query analyzed during keyword research and content planning must be classified into one of the four primary search intent categories:

1. **Informational:** User is researching a topic, definition, guide, or solution (e.g., "what is microservices architecture").
2. **Commercial Investigation:** User is evaluating options, comparisons, or service providers before buying (e.g., "best custom software development companies").
3. **Transactional:** User has high purchase intent and is ready to buy, hire, or contact (e.g., "hire react developer", "enterprise devops consulting pricing").
4. **Navigational:** User is seeking a specific brand, login page, or portal (e.g., "Example Corp customer portal").

---

## 4. Evidence Persistence

All raw search responses, page header traces, and DOM dumps collected during audits must be stored under `outputs/{{CURRENT_DATE}}/{{DOMAIN_NAME}}/audit-report/evidence/` with SHA-256 or timestamp hashes for reproducible audit verification.
