# Website Technical SEO Audit Report

Run: `strawhatdevs-2026-11-18` | Observed: 18 November 2026, IST

Target: https://www.strawhatdevs.com/en | Brand: Straw Hat Devs

## Executive assessment

The site is accessible over HTTPS, renders substantive business content in the initial HTML, and publishes a readable robots file and XML sitemap. The main issue is inconsistent indexation signals: many distinct pages inherit the bare-root canonical, while the preferred serving host is `www.strawhatdevs.com`. Page-level alternate-language links also frequently target language homepages rather than equivalent pages. This can confuse consolidation; actual Google-selected canonicals require Search Console.

**No overall numeric health score assigned:** field performance, rendered mobile behavior, Search Console and complete link coverage are unavailable, so a score would imply unsupported precision. No confirmed sitewide P0 outage was observed.

Business scope supplied by the user includes custom software, web/mobile, websites, AI workflows, SaaS/multi-tenancy, e-commerce, SEO and digital solutions. The live homepage supports custom software, web/mobile, SaaS, cloud and AI/automation positioning. The three dedicated solution pages address manufacturing, dealer orders and workflow automation. Dedicated commercial web development, e-commerce, multi-tenant SaaS and SEO delivery pages were not discovered in this bounded crawl; these are opportunities, not confirmed missing from every possible URL.

## Method, evidence and coverage

Public observational analysis only; Search Console verification required. Audit performed 18 November 2026 IST with ordinary public GET requests and public search inspection. Raw responses, redirect chains, headers and extracted metadata are retained in [crawl.json](evidence/crawl.json) and text snapshots named there. Robots and sitemap were successfully fetched by the local HTTP client even though the web browsing tool could not open those endpoints. Search snippets were sometimes older than current live content; live responses take precedence.

The crawl combines root navigation, two bounded link-expansion passes, every sitemap entry at its preferred-host equivalent, and explicit error/locale probes. It is not an exhaustive crawl of every course lesson, asset or external link. Invalid-locale pages generated during discovery are diagnostic duplicates, not genuine sitemap pages.

Total public requests retained: **68**. Valid English/Tamil 200-page inventory below: **46**. Sitemap entries: **34** across `en` and `ta`; preferred-host equivalents were checked. Of 29 English 200-page samples, **20** declare `https://strawhatdevs.com` as canonical. No JSON-LD script was found in the collected English HTML samples.

## Discovered Pages Catalog

| Observed URL | Classification | Current title / function | HTTP | Declared canonical |
| --- | --- | --- | --- | --- |
| [/en](https://www.strawhatdevs.com/en) | Company/commercial | Software Engineering & Developer Education \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/vr](https://www.strawhatdevs.com/en/vr) | Utility/auth | Virtual Reality World \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/schedule](https://www.strawhatdevs.com/en/schedule) | Company/commercial | Schedule a Free Consultation \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/auth/sign-in](https://www.strawhatdevs.com/en/auth/sign-in) | Utility/auth | Sign In \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/auth/sign-up](https://www.strawhatdevs.com/en/auth/sign-up) | Utility/auth | Sign Up \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/courses](https://www.strawhatdevs.com/en/courses) | Learning | Programming Courses in Tamil \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/solutions/manufacturing-software](https://www.strawhatdevs.com/en/solutions/manufacturing-software) | Service/solution | Custom manufacturing software for clearer operations. \| StrawHatDevs | 200 | https://strawhatdevs.com/en/solutions/manufacturing-software |
| [/en/solutions/dealer-order-management](https://www.strawhatdevs.com/en/solutions/dealer-order-management) | Service/solution | Make dealer ordering easier to manage. \| StrawHatDevs | 200 | https://strawhatdevs.com/en/solutions/dealer-order-management |
| [/en/solutions/workflow-automation](https://www.strawhatdevs.com/en/solutions/workflow-automation) | Service/solution | Spend less time on repetitive business workflows. \| StrawHatDevs | 200 | https://strawhatdevs.com/en/solutions/workflow-automation |
| [/en/courses/nextjs-cartcraft](https://www.strawhatdevs.com/en/courses/nextjs-cartcraft) | Learning | CartCraft: Build an E-commerce App with React and Next.js | 200 | https://strawhatdevs.com |
| [/en/courses/sql](https://www.strawhatdevs.com/en/courses/sql) | Learning | SQL & PostgreSQL Database Modeling Crash Course | 200 | https://strawhatdevs.com |
| [/en/courses/docker](https://www.strawhatdevs.com/en/courses/docker) | Learning | Docker Crash Course: Beginner to Builder | 200 | https://strawhatdevs.com |
| [/en/blogs](https://www.strawhatdevs.com/en/blogs) | Article | Software Engineering Blogs in Tamil \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/insights](https://www.strawhatdevs.com/en/insights) | Business insight | Business Insights \| Software, SaaS & Industry Workflows \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights |
| [/en/tools](https://www.strawhatdevs.com/en/tools) | Company/commercial | Our Products \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/consulting](https://www.strawhatdevs.com/en/consulting) | Company/commercial | Software Consulting Services in Tamil \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/contact](https://www.strawhatdevs.com/en/contact) | Company/commercial | Straw Hat Devs \| Software Engineering, Cloud & AI | 200 | https://strawhatdevs.com |
| [/en/terms](https://www.strawhatdevs.com/en/terms) | Company/commercial | Terms of Service \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/auth/forgot-password](https://www.strawhatdevs.com/en/auth/forgot-password) | Utility/auth | Forgot Password \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/en/blogs/learn-programming-in-tamil-without-getting-stuck](https://www.strawhatdevs.com/en/blogs/learn-programming-in-tamil-without-getting-stuck) | Article | How to Learn Programming in Tamil Without Getting Stuck | 200 | https://strawhatdevs.com |
| [/en/blogs/system-design-basics-scaling-simple-app](https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app) | Article | System Design Basics: Scaling a Simple App | 200 | https://strawhatdevs.com |
| [/en/blogs/clean-code-habits-junior-developers](https://www.strawhatdevs.com/en/blogs/clean-code-habits-junior-developers) | Article | Clean Code Habits Every Junior Developer Should Practice | 200 | https://strawhatdevs.com |
| [/en/insights/manufacturing-order-workflow](https://www.strawhatdevs.com/en/insights/manufacturing-order-workflow) | Business insight | Orders without the chase \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/manufacturing-order-workflow |
| [/en/insights/healthcare-front-desk-workflows](https://www.strawhatdevs.com/en/insights/healthcare-front-desk-workflows) | Business insight | A calmer clinic front desk \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/healthcare-front-desk-workflows |
| [/en/insights/retail-mart-inventory-visibility](https://www.strawhatdevs.com/en/insights/retail-mart-inventory-visibility) | Business insight | Stock your team can trust \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/retail-mart-inventory-visibility |
| [/en/insights/shopping-mall-iot-pilot](https://www.strawhatdevs.com/en/insights/shopping-mall-iot-pilot) | Business insight | Smarter shared spaces \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/shopping-mall-iot-pilot |
| [/en/insights/saas-first-useful-release](https://www.strawhatdevs.com/en/insights/saas-first-useful-release) | Business insight | Start SaaS with one job \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/saas-first-useful-release |
| [/en/about](https://www.strawhatdevs.com/en/about) | Company/commercial | Straw Hat Devs \| Software Engineering, Cloud & AI | 200 | https://strawhatdevs.com |
| [/en/work](https://www.strawhatdevs.com/en/work) | Company/commercial | Straw Hat Devs \| Software Engineering, Cloud & AI | 200 | https://strawhatdevs.com |
| [/ta/insights](https://www.strawhatdevs.com/ta/insights) | Business insight | Business Insights \| Software, SaaS & Industry Workflows \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights |
| [/ta/insights/manufacturing-order-workflow](https://www.strawhatdevs.com/ta/insights/manufacturing-order-workflow) | Business insight | Orders without the chase \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/manufacturing-order-workflow |
| [/ta/insights/healthcare-front-desk-workflows](https://www.strawhatdevs.com/ta/insights/healthcare-front-desk-workflows) | Business insight | A calmer clinic front desk \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/healthcare-front-desk-workflows |
| [/ta/insights/retail-mart-inventory-visibility](https://www.strawhatdevs.com/ta/insights/retail-mart-inventory-visibility) | Business insight | Stock your team can trust \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/retail-mart-inventory-visibility |
| [/ta/insights/shopping-mall-iot-pilot](https://www.strawhatdevs.com/ta/insights/shopping-mall-iot-pilot) | Business insight | Smarter shared spaces \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/shopping-mall-iot-pilot |
| [/ta/insights/saas-first-useful-release](https://www.strawhatdevs.com/ta/insights/saas-first-useful-release) | Business insight | Start SaaS with one job \| Business Insights \| Straw Hat Devs | 200 | https://strawhatdevs.com/en/insights/saas-first-useful-release |
| [/ta](https://www.strawhatdevs.com/ta) | Company/commercial | Software Engineering & Developer Education \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/ta/blogs](https://www.strawhatdevs.com/ta/blogs) | Article | தமிழில் மென்பொருள் கட்டுரைகள் \| ஸ்ட்ரா ஹாட் டெவ்ஸ் | 200 | https://strawhatdevs.com |
| [/ta/courses](https://www.strawhatdevs.com/ta/courses) | Learning | தமிழில் நிரலாக்கப் பயிற்சிகள் \| ஸ்ட்ரா ஹாட் டெவ்ஸ் | 200 | https://strawhatdevs.com |
| [/ta/tools](https://www.strawhatdevs.com/ta/tools) | Company/commercial | எங்கள் தயாரிப்புகள் \| Straw Hat Devs | 200 | https://strawhatdevs.com |
| [/ta/consulting](https://www.strawhatdevs.com/ta/consulting) | Company/commercial | தமிழில் மென்பொருள் ஆலோசனை சேவைகள் \| ஸ்ட்ரா ஹாட் டெவ்ஸ் | 200 | https://strawhatdevs.com |
| [/ta/solutions/manufacturing-software](https://www.strawhatdevs.com/ta/solutions/manufacturing-software) | Service/solution | Custom manufacturing software for clearer operations. \| StrawHatDevs | 200 | https://strawhatdevs.com/ta/solutions/manufacturing-software |
| [/ta/solutions/dealer-order-management](https://www.strawhatdevs.com/ta/solutions/dealer-order-management) | Service/solution | Make dealer ordering easier to manage. \| StrawHatDevs | 200 | https://strawhatdevs.com/ta/solutions/dealer-order-management |
| [/ta/solutions/workflow-automation](https://www.strawhatdevs.com/ta/solutions/workflow-automation) | Service/solution | Spend less time on repetitive business workflows. \| StrawHatDevs | 200 | https://strawhatdevs.com/ta/solutions/workflow-automation |
| [/ta/about](https://www.strawhatdevs.com/ta/about) | Company/commercial | ஸ்ட்ரா ஹாட் டெவ்ஸ் \| மென்பொருள் பொறியியல், கிளவுட் & AI | 200 | https://strawhatdevs.com |
| [/ta/work](https://www.strawhatdevs.com/ta/work) | Company/commercial | ஸ்ட்ரா ஹாட் டெவ்ஸ் \| மென்பொருள் பொறியியல், கிளவுட் & AI | 200 | https://strawhatdevs.com |
| [/ta/contact](https://www.strawhatdevs.com/ta/contact) | Company/commercial | ஸ்ட்ரா ஹாட் டெவ்ஸ் \| மென்பொருள் பொறியியல், கிளவுட் & AI | 200 | https://strawhatdevs.com |

The inventory retains learning, auth and VR pages for completeness. Auth and VR pages are not commercial landing-page opportunities. The `about` and `work` pages were discovered in the sitemap even though not linked from the sampled footer; that alone does not prove they are orphaned.

## Technical infrastructure findings

| Finding | Observed evidence | Priority / implication |
| --- | --- | --- |
| Host and path canonical inconsistency | `/en`, `/en/consulting`, `/en/contact`, courses and blog samples point to the bare apex root; solution/insight pages use their own paths but apex hostname | P1: publish absolute self-canonicals at the serving host for every indexable page |
| Alternate-language links inherited from root | For example `/en/consulting` advertises apex `/en` and `/ta` rather than corresponding consulting routes | P1: reciprocal page-equivalent hreflang; verify translations before linking |
| Locale matcher accepts an invalid first segment | `/sitemap_index.xml` returns homepage HTML with 200; `/sitemap_index.xml/courses` serves course-list content with 200 | P1: reject invalid locales, ensure XML-like nonexistent resources return 404 |
| Robots and sitemap use apex | Robots points to `https://strawhatdevs.com/sitemap.xml`; all 34 sitemap locations use apex, which redirects to www | P1: align sitemap, robots and internal canonical host |
| Repeated commercial metadata | Contact, about and work use the inherited software-engineering/cloud/AI title and education description | P1/P2: distinct metadata and commercial intent |
| Missing raw-HTML H1 on sampled learning pages | `/en/courses`, `/en/blogs`, course-detail and auth/VR samples lack an extracted H1 | P2: inspect rendered client content before changing; keep useful heading in server-rendered HTML |
| Auth pages inherit index,follow and homepage canonical | Sign-in/sign-up/forgot-password are 200 public utility pages | P2: set deliberate noindex,follow; do not use the homepage canonical as a substitute |

Robots: `User-Agent: *`, `Allow: /`, `Disallow: /private/`, `Disallow: /admin/`. Locale-prefixed admin/private paths were not accessed; exclusion scope should be reviewed. Robots exclusions are not authentication controls. No global noindex was found in sampled public HTML. HTTPS certificate validation succeeded in the requests client; a full TLS configuration test was not run. No obvious HTTP image source was present in sampled home image URLs; complete browser mixed-content validation remains unperformed.

## Broken links, redirects and error handling

| Source / probe | Target | Observed result | Interpretation |
| --- | --- | --- | --- |
| User target | `https://strawhatdevs.com/` | 308 to www root, 307 to `/en/`, 308 to `/en`, then 200 | Three redirects; reduce the avoidable trailing-slash hop |
| HTTP variant | `http://strawhatdevs.com/` | Ends at HTTPS www `/en`, 200 | HTTPS redirect works; exact chain retained in crawl evidence |
| Sitemap | 34 apex locale URLs | Preferred-host equivalents 200 | XML host still induces avoidable redirects for crawlers |
| Deliberate negative probes | `/en/seo-audit-nonexistent-20261118`, `/en/not-a-real-page` | 404 | Correct real missing-page behavior in valid locale |
| Invalid-locale/XML probe | `/sitemap_index.xml` | HTML homepage, 200 | Duplicate/soft-routing anomaly, not a valid sitemap index |
| Invalid-locale nested probe | `/sitemap_index.xml/solutions/workflow-automation` | HTML solution content, 200 | Route validation defect confirmed |

No 4xx/5xx was found among the sampled linked/sitemap commercial pages. Probe 404s are intentional, not broken site links. External links were inventoried but not exhaustively status-checked; social/login bot restrictions can look like failures and are not treated as broken links without browser confirmation.

## Performance and Core Web Vitals baseline

| Metric | Mobile | Desktop | Evidence |
| --- | --- | --- | --- |
| PageSpeed performance score; LCP; INP; CLS; FCP | Unavailable | Unavailable | Public PageSpeed API returned 429 quota exceeded for both requests; [mobile response](evidence/psi-mobile.json), [desktop response](evidence/psi-desktop.json) |
| Browser navigation TTFB | Not measured | Not measured | HTTP request wall times in crawl.json include network/redirect work and are not browser TTFB |
| Field percentile / pass status | Unknown | Unknown | No CrUX/GSC authenticated dataset retrieved |

The homepage PNG `/coding-on-laptop.png` is served at **895,857 bytes** (Content-Length observed); it is a plausible image optimization candidate, not a measured LCP element. Home HTML preloads it and two logo variants; multiple image/font preloads should be checked against actual viewport demand. Sampled images have explicit width/height and lower cards use lazy loading, which are positive structural indicators. Gzip is present in HTML responses. Source dimensions do not establish the real CLS score.

## Mobile usability

Viewport is `width=device-width, initial-scale=1`. Responsive class names and image dimensions exist, but tap-target sizes, overflow, font readability and interaction behavior have not been verified in a rendered mobile browser. No browser automation package was available locally; no pass claim is made. Check 360, 390 and 768 CSS-pixel widths before deploying changes.

## Search presence and service-keyword crawl coverage

Public `site:strawhatdevs.com` queries returned the English homepage, courses, consulting, contact, schedule, blogs and terms. This establishes public discoverability of some URLs, not a complete indexed count or target-query ranking. Search results still described an older education-first homepage while current live content is broader business software; this may reflect crawl lag. The live contact page explicitly states service to Coimbatore and remote clients across India. User-targeted web-development/e-commerce queries need focused buying pages; an e-commerce **course** is a different intent from an e-commerce build service.

## Prioritized issues and acceptance criteria

- **P0:** None verified during this public sample.
- **P1:** Correct self-canonicals and page-equivalent hreflang; validate locale routing; align canonical host everywhere. Accept when all sampled indexable paths return one page-specific canonical, alternate links return equivalent 200 pages, and invalid locale/resource probes return 404.
- **P1:** Give homepage/consulting/contact a clear division between business-service and learning intent. Accept when their titles/descriptions/H1s match mapped page purpose.
- **P2:** Optimize the large hero asset after measuring its role; verify server-rendered headings and utility-page noindex. Accept with before/after mobile/desktop lab runs and HTML assertions.
- **P2:** Add truthful organization/service structured data where useful; absence alone is not an indexing blocker or a guaranteed ranking lever.
- **P3:** Remove the literal placeholder `yandex-verification-code` unless a real verification value exists; keep existing valid ownership verifications intact.

Primary evidence: [live home](https://www.strawhatdevs.com/en), [consulting](https://www.strawhatdevs.com/en/consulting), [contact](https://www.strawhatdevs.com/en/contact), [robots](https://www.strawhatdevs.com/robots.txt), [sitemap](https://www.strawhatdevs.com/sitemap.xml), and the timestamped local crawl evidence. No website changes or form submissions were made.
