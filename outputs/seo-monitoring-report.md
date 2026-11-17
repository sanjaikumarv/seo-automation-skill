# SEO Monitoring Baseline and KPI Framework

Run: `strawhatdevs-2026-11-18` | Observed: 18 November 2026, IST

Target: https://www.strawhatdevs.com/en | Brand: Straw Hat Devs

## Executive baseline

All seven preceding reports were read. This is a **public technical baseline and monitoring design**, not an authenticated historical performance report. Requires Google Analytics 4 and Google Search Console account authentication. A GTM container reference was observed in HTML, but account access, GA4 property configuration, consent settings, event delivery and data quality were not verified. No analytics account was created, connected or changed.

Baseline date: 18 November 2026 IST. Recommended complete-month comparison when data is available: **1-31 October 2026 vs 1-30 September 2026**, with per-day rates noted for unequal periods. November is incomplete; compare matched elapsed-day windows only when appropriate and label data lag. Use the properties' actual reporting timezones and document differences; project follow-up dates use IST. Suggested monthly reporting is a plan, not a created recurring automation.

## Core SEO KPI scorecard

| Metric | October 2026 | September 2026 | Change | Status / data source |
| --- | --- | --- | --- | --- |
| Organic sessions / active users | Unavailable | Unavailable | N/A | GA4, session channel Organic Search |
| Engaged sessions / engagement rate | Unavailable | Unavailable | N/A | GA4; no universal engagement target imposed |
| Search clicks / impressions | Unavailable | Unavailable | N/A | Search Console Web Search |
| Search CTR | Unavailable | Unavailable | N/A | Clicks / impressions, weighted totals |
| Average search position | Unavailable | Unavailable | N/A | GSC query/page/device/country segmentation |
| Confirmed project inquiries | Unavailable | Unavailable | N/A | Valid successful lead event; exclude test/spam submissions |
| Organic session key-event rate | Unavailable | Unavailable | N/A | Sessions with qualifying lead / organic sessions |
| Qualified leads / opportunities | Unavailable | Unavailable | N/A | Owner-approved CRM categorization; separate from all inquiries |
| Local map-pack visibility | Unavailable | Unavailable | N/A | Verified eligible GBP + repeatable location/device setup |

Unavailable is not zero. Do not infer improvement, decline or stability before obtaining a real comparison. Average position is not a fixed rank; report query/page mix changes rather than presenting a single number as market share. Use business-fit inquiries as the primary decision signal for this startup/SME service strategy.

## Public technical baseline retained from Steps 1-7

- 34 XML sitemap locations across English/Tamil; declared URLs use the apex host while served pages use www.
- 46 unique 200 English/Tamil page samples recorded; bounded coverage, not a complete site-size or indexed-page count.
- 20 of 29 English 200-page samples declare the apex root canonical; other solution/insight self-path canonicals still use the apex host.
- `/sitemap_index.xml` is a 200 HTML invalid-locale route; genuine invalid pages under `/en` return 404.
- Home image `/coding-on-laptop.png` Content-Length: 895,857 bytes; not a measured LCP.
- Mobile and desktop public PSI API calls returned 429; CWV and browser TTFB unavailable.
- Current business identity/contact details differ from some older snippets and profile website fields.

These are implementation baselines, not traffic metrics. Keep their raw evidence with this run and rerun the same checks after authorized changes.

## GSC query analysis framework

Export query, page, country, device, clicks, impressions, CTR and average position for the same period and search type. Segment branded queries separately from nonbrand buying queries, and separate course/learning pages from business services. Check data privacy thresholds and omitted queries; query totals may not match all chart totals.

| Candidate segment | Actual query metrics now | Future selection rule | Action after validation |
| --- | --- | --- | --- |
| Software development company / Coimbatore variants | Unavailable | Real mapped page impressions and relevant intent | Fix home canonical and assess snippet fit |
| Web development / website developer variants | Unavailable | Buyer-intent queries on the dedicated page after launch | Improve content around actual impressions and lead fit |
| E-commerce website builder/developer variants | Unavailable | Separate DIY/course queries from implementation buyers | Keep the service page and CartCraft learning intent distinct |
| AI/workflow and SaaS queries | Unavailable | Map real query intent to existing workflow or launched SaaS page | Fill demonstrated content gaps |

“Striking distance” rule: select actual GSC average-position 4-10 query/page combinations with meaningful impressions and relevant business intent; compare CTR within device/country and position context. No current query is claimed to be in that range. Review high-impression/low-CTR items only after canonical/indexation issues and page intent are understood. Do not claim top-three or top-ten counts, ranking gains/drops or local ranking trajectories from today's search sample.

## GA4 and successful-lead instrumentation plan

1. Verify the intended GA4 property, stream, timezone, consent implementation and existing GTM deployment before adding any tags. Keep one page-view owner; check App Router client navigation for missing or duplicate pageviews.
2. Fire a `generate_lead` event only after the project inquiry backend confirms successful acceptance. Clicking Submit, failing validation or merely loading Contact is not a lead. Do not infer appointment completion from the schedule-page click.
3. Use a stable non-personal `form_id` and page path. Never send name, email, phone, company text, free-form project details or sensitive query strings to ordinary analytics event parameters. Do not fabricate conversion values.
4. Configure the business-selected event as a key event only when the owner authorizes account changes; confirm one fire per successful submission and keep test traffic separate.
5. Track CTA or schedule clicks as separate engagement events if useful. If an actual external booking success event becomes available, define it separately rather than counting the click twice as an inquiry.

Integration fragment, **not installed or sent**:

```ts
// Inside the existing form success branch, after a confirmed successful API result.
// Respect the existing consent/tag manager implementation. Do not add a second GTM.
const trackingWindow = window as Window & {
  dataLayer?: Record<string, unknown>[];
};
trackingWindow.dataLayer = trackingWindow.dataLayer || [];
trackingWindow.dataLayer.push({
  event: 'generate_lead',
  form_id: 'project_inquiry',
  page_path: window.location.pathname,
});
```

The application must call this branch once, not on every re-render. A dataLayer push alone does not prove GA4 receives the event; a corresponding approved GTM trigger/tag and validation are required. If a property already tracks leads by another path, reconcile it before adding this fragment.

## Metric formulas and QA

- CTR = clicks / impressions; if impressions = 0, display N/A rather than divide by zero.
- Event lead rate = confirmed lead events / organic sessions; it can differ from the session key-event rate when one session has multiple events. Prefer the session definition for a conversion-propensity comparison.
- Period change = (current - previous) / previous when previous > 0; otherwise report raw values and N/A/new baseline, not infinite growth.
- Segment qualified business leads without exporting personal identifiers into analytics. Keep any CRM linkage local/owner-approved and governed by the actual account setup.
- Validate a successful submission, a server failure, client validation failure, double click, back navigation, and consent-denied case. Do not submit production test forms without authorization; use a development/staging flow or designated test endpoint.

## Technical stability and next-period roadmap

| Timing after implementation authorization | Check | Acceptance |
| --- | --- | --- |
| Release day | Canonicals, hreflang, sitemap, invalid locale and real 404 routes | One correct canonical per indexable page; correct host and actual locale equivalents; invalid-locale route no longer serves content |
| First week | Inquiry success tracking and actual page navigation | No PII; no duplicate leads or pageviews; owner-verified event delivery |
| First month | Business landing impressions, qualified inquiries, crawl/indexing changes | Compare real data with the recorded baseline and publish date; avoid attributing all movement to one edit |
| Following month | Matched reporting period and content opportunities | Real demand and lead quality guide next pages; retain useful learning content |

Algorithm updates, seasonality and query mix require evidence before explaining a change; no performance movement was measured here. GBP and backlink dashboards stay unavailable until actual sources are provided.

Implementation references consulted 18 November 2026: [GA4 recommended lead event](https://developers.google.com/analytics/devguides/collection/ga4/reference/events#generate_lead), [Analytics PII prevention](https://support.google.com/analytics/answer/6366371/), [GSC performance report](https://support.google.com/webmasters/answer/7576553), and [Google Search updates](https://developers.google.com/search/updates). Current Search documentation says FAQ rich results were retired in May 2026; optional FAQPage semantic markup must not be sold as a Google rich-result benefit.
