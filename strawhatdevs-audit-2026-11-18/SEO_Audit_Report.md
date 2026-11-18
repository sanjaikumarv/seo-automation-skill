# Straw Hat Devs SEO Audit

## 1. Executive summary

**Audit date** 18 November 2026 (IST)  
**Website** [Straw Hat Devs](https://www.strawhatdevs.com/en)  
**Technology** Next.js, indicated by `/_next/` bundles and App Router flight data in the delivered HTML.  
**Scope** Public www/apex website, English and Tamil, including browser-accessible course overviews. The site offers software engineering, consulting and developer education. Audience and intent observations draw on visible copy.  
**Coverage** 123 discovered website URL strings, 86 distinct 200 HTML destinations audited, 70 final paths without query parameters.  
**Findings** 18 confirmed issues (0 critical, 4 high, 10 medium, 4 low) plus 2 informational items. No composite SEO score was assigned.

The biggest technical priority is to align canonical tags, locale alternates and sitemap URLs with the URLs that actually serve content. The homepage mobile lab performance score was 58/100 with 8.09 s LCP on the recorded run. The course catalog also requires interaction to expose part of its public inventory.

## 2. Website crawl summary

On the first pass, the crawler requested 107 entry URLs from the homepage variants, sitemap and public source anchors. The browser follow-up added 12 course destinations, each fetched and inspected in source. The inventory also includes 4 final destinations observed at the end of redirect chains. Initial responses to the 119 entry requests were 82 direct 200s, 36 first-hop 308s and 1 first-hop 307. All 119 ended at 200 HTML. Zero crawl-entry requests ended in HTTP error or remained inaccessible. Diagnostic missing-route probes and external statuses are tracked separately.

There are 37 redirect aliases in the inventory and 16 contact-prefill variants. Exact main-text matches are recorded in the content evidence, including client shells with empty main text. 16 final URLs were unreachable by following source-level hrefs from the two locale homepages in the captured graph. Some paths were available through sitemap entries or client interaction.

`robots.txt` disallows `/private/` and `/admin/` and lists the apex sitemap. The XML parsed as a URL set with 34 entries, covering English and Tamil. All entries redirect to www. The retained XML shows a shared lastmod value across all entries. Actual content update history would be needed to validate that value.

[Complete page inventory](SEO_Page_Inventory.csv) · [Robots responses](SEO_Evidence/01-robots.json) · [Sitemap discovery](SEO_Evidence/01-sitemaps.json) · [Additional course responses](SEO_Evidence/07-course-followup-http.json)

| Stage | Objective | Outcome and evidence |
| --- | --- | --- |
| 1. Discovery | Map public URLs and first responses | 107 entry URLs from seeds, sitemap and source links. [Evidence](SEO_Evidence/01-crawl.json) |
| 2. HTML | Review metadata and document structure | 86 unique final HTML responses after catalog follow-up. [Evidence](SEO_Evidence/02-html.json) |
| 3. Images | Check markup, assets and file metadata | 43/43 observed source URLs returned 200. [First-party](SEO_Evidence/03-images.json) · [Sanity CDN](SEO_Evidence/03-cdn-images.json) |
| 4. Links | Verify source anchors and destination responses | 16 external HTTPS destinations. Two public GitHub 404s. [Evidence](SEO_Evidence/04-links.json) |
| 5. Technical | Inspect preferred URLs, robots and indexability signals | 34 redirecting sitemap loc values. Six additional route probes. [Evidence](SEO_Evidence/05-route-probes.json) |
| 6. Performance | Measure representative mobile and desktop loads | 10 Lighthouse lab runs. PSI status counts {429: 10}. |
| 7. Mobile | Check viewports, navigation and hydration | 30 viewport navigations and 12 additional public course routes discovered. [Evidence](SEO_Evidence/07-browser.json) · [Catalog](SEO_Evidence/07-course-navigation.json) |
| 8. Content | Assess distinct purpose and localized content | 13 clean Tamil routes repeat English main copy. [Evidence](SEO_Evidence/08-content.json) |
| 9. Structured data | Inspect public structured markup | No source markup in the three surveyed formats. [Evidence](SEO_Evidence/09-structured-data.json) |
| 10. Trust | Check HTTPS and visible business disclosures | About, contact and terms verified. Privacy URL unresolved. [Evidence](SEO_Evidence/10-trust.json) |
| 11. Prioritization | Assign IDs, severity and validation steps | 18 confirmed issues. [Issue register](SEO_Issue_Register.csv) |

## 3. Detailed SEO findings

### HTML and on-page SEO

Reviewed titles, descriptions, robots, canonical tags, headings, language, viewport, semantic landmarks, Open Graph and Twitter metadata. All documents include a title, description, declared language and viewport. There were no source documents with multiple H1s. Account and VR heading omissions are lower-confidence SEO concerns on utility pages. Course-detail heading absence is captured under source rendering. Nu validation sampled the homepage and consulting. Both flag the framework-generated next-size-adjust meta element; no SEO impact was demonstrated for that notice. See each source response referenced in the HTML evidence for full markup. [Evidence](SEO_Evidence/02-html.json)

#### SEO-07 · About, work and contact reuse generic titles and descriptions · MEDIUM

**URL examples** [/en/about](https://www.strawhatdevs.com/en/about), [/en/contact](https://www.strawhatdevs.com/en/contact), [/en/work](https://www.strawhatdevs.com/en/work), [/ta/about](https://www.strawhatdevs.com/ta/about). See the issue register for all 6 URLs.  
**Element** title, meta[name=description]  
**Observed** Each group of three localized pages shares the same title and description. English title is “Straw Hat Devs | Software Engineering, Cloud & AI” even on the contact and portfolio routes.  
**Expected** Use a unique title and description that represent the actual purpose and language of each page.  
**Impact** Generic labels reduce differentiation in search results and social previews.  
**Recommendation** Add route-specific metadata to the about, contact and work page modules in both locales.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json)

#### SEO-08 · Blog and course listings lack an H1 · LOW

**URL examples** [/en/blogs](https://www.strawhatdevs.com/en/blogs), [/en/courses](https://www.strawhatdevs.com/en/courses), [/ta/blogs](https://www.strawhatdevs.com/ta/blogs), [/ta/courses](https://www.strawhatdevs.com/ta/courses).  
**Element** Listing title hierarchy  
**Observed** The first prominent listing heading is H2. Examples include “Software Engineering Blogs” and “Our Courses”.  
**Expected** Represent the visible main page heading as H1 and keep listing card headings subordinate.  
**Impact** Improves document structure and helps assistive technology users identify the page topic.  
**Recommendation** Change the primary heading element in the shared listing templates and adjust child heading levels as needed.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [07-browser.json](SEO_Evidence/07-browser.json)

#### SEO-09 · Open Graph URL points to the homepage on interior pages · LOW

**URL examples** [/en/about](https://www.strawhatdevs.com/en/about), [/en/auth/forgot-password](https://www.strawhatdevs.com/en/auth/forgot-password), [/en/auth/sign-in](https://www.strawhatdevs.com/en/auth/sign-in), [/en/auth/sign-up](https://www.strawhatdevs.com/en/auth/sign-up). See the issue register for all 23 URLs.  
**Element** meta[property=og:url]  
**Observed** 23 clean, non-default-home URLs emit https://strawhatdevs.com as og:url.  
**Expected** Social metadata uses the intended share URL for the individual page.  
**Impact** Social platforms may consolidate previews or engagement on the homepage.  
**Recommendation** Set page-aware Open Graph URLs and verify relevant title, description and image values.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json)

#### SEO-20 · Navigation nests buttons inside links · LOW

**URL examples** [/en](https://www.strawhatdevs.com/en), [/en/about](https://www.strawhatdevs.com/en/about), [/en/auth/forgot-password](https://www.strawhatdevs.com/en/auth/forgot-password), [/en/auth/sign-in](https://www.strawhatdevs.com/en/auth/sign-in). See the issue register for all 84 URLs.  
**Element** Shared public navigation markup  
**Observed** 84 captured pages include at least one `<a><button>…</button></a>` pattern. W3C Nu independently flags four nested buttons on both the homepage and consulting page.  
**Expected** Each navigation action uses one interactive anchor with a descriptive accessible name.  
**Impact** Nested interactive elements can create ambiguous semantics for keyboard and assistive technology users.  
**Recommendation** Render the navigational control as a styled link via the shared navigation component.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-nu-home.json](SEO_Evidence/02-nu-home.json) · [02-nu-consulting.json](SEO_Evidence/02-nu-consulting.json) · [02-html.json](SEO_Evidence/02-html.json)

| URL | HTML element | Actual value or snippet | Expected value | Issue | Recommendation |
| --- | --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/en/contact | title / description | `<title>Straw Hat Devs &#124; Software Engineering, Cloud & AI</title>` and a shared education-oriented description | Contact-specific metadata | SEO-07 | Set contact-specific title and description |
| https://www.strawhatdevs.com/en/blogs | Page heading | `<h2>Software Engineering Blogs</h2>` (class attribute omitted) | Main heading uses H1 | SEO-08 | Promote the existing listing heading |
| https://www.strawhatdevs.com/en/blogs | og:url | `<meta property="og:url" content="https://strawhatdevs.com"/>` | https://www.strawhatdevs.com/en/blogs | SEO-09 | Emit the intended final page URL |

### Image SEO

Inspected source img attributes and fetched 43 unique source image URLs. All initial img tags carried an alt attribute. Empty alt values appear on repeated decorations and secondary linked article images. Those values were reviewed in page context. Modern WebP and SVG images are already used throughout shared components. Some CMS images lack intrinsic width/height attributes. The captured mobile and desktop lab samples show CLS 0. Dimension attributes or a verified aspect-ratio container can reserve space, especially where crops differ. Mobile display measurements below are reported only when captured. [Image metadata](SEO_Evidence/03-images.json)

#### SEO-11 · Large fixed-source PNGs increase transfer across solution and editorial templates · MEDIUM

**URL examples** [/en/blogs](https://www.strawhatdevs.com/en/blogs), [/en/blogs/clean-code-habits-junior-developers](https://www.strawhatdevs.com/en/blogs/clean-code-habits-junior-developers), [/en/blogs/learn-programming-in-tamil-without-getting-stuck](https://www.strawhatdevs.com/en/blogs/learn-programming-in-tamil-without-getting-stuck), [/en/blogs/system-design-basics-scaling-simple-app](https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app). See the issue register for all 16 URLs.  
**Element** Solution illustrations and Sanity raster media  
**Observed** 9 observed PNG sources exceed the audit’s 300 kB triage cutoff. Examples include the 1,050,342-byte database illustration and a 1,851,132-byte article graphic. Image elements use one src and omit srcset/sizes.  
**Expected** Supply variants for real display widths and DPRs while preserving crops, diagram readability and acceptable quality.  
**Impact** Extra bytes use bandwidth needed for other resources and add image decoding cost.  
**Recommendation** Use Sanity size/format variants for editorial media and responsive exports for the solution illustrations. Preserve appropriate lazy loading for below-fold media.  
**Effort and status** Medium. Confirmed.  
**Evidence** [03-images.json](SEO_Evidence/03-images.json) · [03-cdn-images.json](SEO_Evidence/03-cdn-images.json) · [02-html.json](SEO_Evidence/02-html.json) · [manufacturing-mobile.json](SEO_Evidence/lighthouse/manufacturing-mobile.json)

| Page URL | Image URL | Bytes | Intrinsic and displayed dimensions | Alt attribute | Issue | Recommendation |
| --- | --- | --- | --- | --- | --- | --- |
| [/en/blogs](https://www.strawhatdevs.com/en/blogs) | [27e6d805c2c0cdbc2b0f2710f6b206f184791254-1672x941.png](https://cdn.sanity.io/images/o9bmr6k7/production/27e6d805c2c0cdbc2b0f2710f6b206f184791254-1672x941.png) | 1,851,132 | 1672×941 PNG; 356×200 CSS px at 390 px | 'Clean code represented as organized modules and a code review workflow' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/blogs](https://www.strawhatdevs.com/en/blogs) | [44a25dc07f376baa32fcc57aff45cbcaae4097cc-1672x941.png](https://cdn.sanity.io/images/o9bmr6k7/production/44a25dc07f376baa32fcc57aff45cbcaae4097cc-1672x941.png) | 1,761,472 | 1672×941 PNG; 356×200 CSS px at 390 px | 'A learner working through a programming roadmap with orange and green progress markers' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/blogs](https://www.strawhatdevs.com/en/blogs) | [c4436e9890b59bf34b3c3127719ab3c9975cd516-1672x941.png](https://cdn.sanity.io/images/o9bmr6k7/production/c4436e9890b59bf34b3c3127719ab3c9975cd516-1672x941.png) | 1,519,023 | 1672×941 PNG; 356×200 CSS px at 390 px | 'A scalable app architecture with server, database, cache, queue, monitoring, and users' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/solutions/manufacturing-software](https://www.strawhatdevs.com/en/solutions/manufacturing-software) | [database-design-concept.png](https://www.strawhatdevs.com/database-design-concept.png) | 1,050,342 | 1024×680 PNG; 358×239 CSS px at 390 px | 'Illustration: Limited visibility into production and dispatch' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en](https://www.strawhatdevs.com/en) | [coding-on-laptop.png](https://www.strawhatdevs.com/coding-on-laptop.png) | 895,857 | 1024×680 PNG; 358×179 CSS px at 390 px | 'Software engineering illustration' | SEO-10 | Match crop and intrinsic variants to slot width and DPR |
| [/en/courses](https://www.strawhatdevs.com/en/courses) | [8f7ba719e33e3b9aa50007c4ff08bc8623b4d0f3-1920x1080.png](https://cdn.sanity.io/images/o9bmr6k7/production/8f7ba719e33e3b9aa50007c4ff08bc8623b4d0f3-1920x1080.png) | 464,327 | 1920×1080 PNG; 356×200 CSS px at 390 px | 'Git Essentials: Version Control Made Simple' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/courses](https://www.strawhatdevs.com/en/courses) | [cd6f1f5c4cde0e8bbbeb678b8840727ee02499ae-1280x720.png](https://cdn.sanity.io/images/o9bmr6k7/production/cd6f1f5c4cde0e8bbbeb678b8840727ee02499ae-1280x720.png) | 437,350 | 1280×720 PNG; 356×200 CSS px at 390 px | 'CartCraft: Build an E-commerce App with React and Next.js' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/solutions/manufacturing-software](https://www.strawhatdevs.com/en/solutions/manufacturing-software) | [devops-cloud-integration.png](https://www.strawhatdevs.com/devops-cloud-integration.png) | 432,204 | 1024×530 PNG; 318×239 CSS px at 390 px | 'Illustration: Integrations with existing systems, subject to API access' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/solutions/manufacturing-software](https://www.strawhatdevs.com/en/solutions/manufacturing-software) | [api-design.png](https://www.strawhatdevs.com/api-design.png) | 346,581 | 1024×409 PNG; 358×239 CSS px at 390 px | 'Illustration: Manual status updates between teams' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |
| [/en/courses](https://www.strawhatdevs.com/en/courses) | [5e5ff03d98f1c0d77b3c29f5985a9107b3d79d2c-1280x720.png](https://cdn.sanity.io/images/o9bmr6k7/production/5e5ff03d98f1c0d77b3c29f5985a9107b3d79d2c-1280x720.png) | 316,394 | 1280×720 PNG; 356×200 CSS px at 390 px | 'SQL & PostgreSQL Database Modeling Crash Course' | SEO-11 | Match crop and intrinsic variants to slot width and DPR |

### Internal and external links

Source-level internal targets all resolved to 200 within the checked graph. No redirect loop was observed. Ten image-only article links are marked aria-hidden and tabindex=-1 and have a separate named text link to the same destination. Contact query variants serve a prefill purpose. Three external destinations (Instagram, LinkedIn, npm) were excluded by the robots/scope checks and require browser-side verification. A 200 from a public social landing page does not verify invite or account validity. [Evidence](SEO_Evidence/04-links.json)

#### SEO-05 · Two product repository links returned 404 · MEDIUM

**URL examples** [/en/tools](https://www.strawhatdevs.com/en/tools), [/ta/tools](https://www.strawhatdevs.com/ta/tools).  
**Element** Product-card links  
**Observed** https://github.com/Santheepkumar/clean-note returned HTTP 404; https://github.com/Santheepkumar/dimensions-visualization returned HTTP 404  
**Expected** Each linked repository is publicly accessible or the card provides an appropriate substitute.  
**Impact** Visitors following these cards cannot reach the promised resource.  
**Recommendation** Confirm whether the repositories were moved, made private, or removed, then update or remove each public link.  
**Effort and status** Small. Confirmed.  
**Evidence** [04-links.json](SEO_Evidence/04-links.json) · [02-html.json](SEO_Evidence/02-html.json)

#### SEO-17 · Catalog course cards use JavaScript-only navigation · MEDIUM

**URL examples** [/en/courses](https://www.strawhatdevs.com/en/courses), [/ta/courses](https://www.strawhatdevs.com/ta/courses).  
**Element** Course card navigation and pagination  
**Observed** The catalog’s View Course controls are buttons. The interactive pass surfaced 12 routes absent from the source-anchor crawl and sitemap. Page 2 is reached via another button.  
**Expected** Each public course is reachable through a standard link. Stable paginated URLs expose the catalog’s remaining public cards.  
**Impact** Crawlers that extract hrefs may miss course pages reachable only by user actions.  
**Recommendation** Use locale-aware anchor links for course destinations and linkable pagination. Keep the cards as client components where needed.  
**Effort and status** Medium. Confirmed.  
**Evidence** [07-course-navigation.json](SEO_Evidence/07-course-navigation.json) · [07-course-followup-http.json](SEO_Evidence/07-course-followup-http.json) · [02-html.json](SEO_Evidence/02-html.json) · [01-sitemaps.json](SEO_Evidence/01-sitemaps.json)

| Source URL | Destination URL | HTTP status | Anchor text | Issue | Recommendation |
| --- | --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/en/tools | https://github.com/Santheepkumar/clean-note | 404 | GitHub — Clean Note | SEO-05 | Update or remove the repository link |
| https://www.strawhatdevs.com/ta/tools | https://github.com/Santheepkumar/clean-note | 404 | GitHub — Clean Note | SEO-05 | Update or remove the repository link |
| https://www.strawhatdevs.com/en/tools | https://github.com/Santheepkumar/dimensions-visualization | 404 | GitHub — Dimensions Visual Lab | SEO-05 | Update or remove the repository link |
| https://www.strawhatdevs.com/ta/tools | https://github.com/Santheepkumar/dimensions-visualization | 404 | GitHub — Dimensions Visual Lab | SEO-05 | Update or remove the repository link |
| https://www.strawhatdevs.com/en/courses | https://www.strawhatdevs.com/en/courses/git | 200 | View Course button | SEO-17 | Use an anchor with a normal href |

### Technical SEO

Crawl access was tested with HTTP responses and robots rules. Index eligibility was assessed using directives and canonical signals. All final captured pages returned 200 HTML. Each declares an alternate canonical and none carried a noindex directive in the inspected fields. The sampled English and no-locale nonexistent URLs return 404 after any locale redirect. Trailing-slash probes resolve to clean locale paths. Homepage hreflang targets point to the apex host, which redirects. Account and VR utility routes return 200 and advertise index, follow. Confirm intended index treatment before changing those routes. Catalog pagination is covered in SEO-17. Public search returned several English routes, including the homepage, courses, consulting and blogs. Some snippets reflect older site content. Actual indexed status and Google-selected canonicals remain unverified. [Public search spot check](SEO_Evidence/05-public-search.md)

#### SEO-01 · Distinct public routes declare the apex homepage as canonical · HIGH

**URL examples** [/en](https://www.strawhatdevs.com/en), [/en/about](https://www.strawhatdevs.com/en/about), [/en/blogs](https://www.strawhatdevs.com/en/blogs), [/en/blogs/clean-code-habits-junior-developers](https://www.strawhatdevs.com/en/blogs/clean-code-habits-junior-developers). See the issue register for all 44 URLs.  
**Element** link[rel=canonical]  
**Observed** 44 non-parameter content and landing URLs declare `<link rel="canonical" href="https://strawhatdevs.com"/>`. The declared URL redirects to https://www.strawhatdevs.com/en. The set includes pages with distinct headings and intent.  
**Expected** Each index-targeted route declares its preferred absolute HTTPS final URL.  
**Impact** Conflicting signals can consolidate distinct landing pages and articles under the homepage.  
**Recommendation** Move default canonical generation into the locale-aware Next.js metadata layer. Set route canonicals for each independently indexable page.  
**Effort and status** Medium. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [01-crawl.json](SEO_Evidence/01-crawl.json)

#### SEO-02 · Route-specific canonicals point to a redirecting host · MEDIUM

**URL examples** [/en/insights](https://www.strawhatdevs.com/en/insights), [/en/insights/healthcare-front-desk-workflows](https://www.strawhatdevs.com/en/insights/healthcare-front-desk-workflows), [/en/insights/manufacturing-order-workflow](https://www.strawhatdevs.com/en/insights/manufacturing-order-workflow), [/en/insights/retail-mart-inventory-visibility](https://www.strawhatdevs.com/en/insights/retail-mart-inventory-visibility). See the issue register for all 12 URLs.  
**Element** link[rel=canonical]  
**Observed** 12 locale routes declare the equivalent path on the apex host, which redirects to www. For example, `<link rel="canonical" href="https://strawhatdevs.com/en/insights"/>`.  
**Expected** The canonical destination responds directly with 200.  
**Impact** Canonical and redirect signals differ on the host and require an extra retrieval.  
**Recommendation** Set the preferred origin in the Next.js metadata base/config and keep the resolved path.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [01-crawl.json](SEO_Evidence/01-crawl.json)

#### SEO-03 · Sitemap lists redirect sources · HIGH

**URL examples** [https://strawhatdevs.com/en](https://strawhatdevs.com/en), [https://strawhatdevs.com/en/about](https://strawhatdevs.com/en/about), [https://strawhatdevs.com/en/blogs](https://strawhatdevs.com/en/blogs), [https://strawhatdevs.com/en/consulting](https://strawhatdevs.com/en/consulting). See the issue register for all 34 URLs.  
**Element** XML sitemap and robots.txt directive  
**Observed** All 34 XML entries use https://strawhatdevs.com. Each first hop returned 308 to www. The robots directive also advertises the redirected sitemap URL.  
**Expected** The sitemap advertises preferred, indexable, direct-200 URLs; robots.txt points directly to the sitemap.  
**Impact** Sitemap signals disagree with the preferred serving host across the entire submitted URL set.  
**Recommendation** Generate XML from the preferred URL registry after the canonical and locale decisions. Update robots.txt to the served sitemap URL.  
**Effort and status** Small. Confirmed.  
**Evidence** [01-sitemaps.json](SEO_Evidence/01-sitemaps.json) · [01-crawl.json](SEO_Evidence/01-crawl.json) · [01-robots.json](SEO_Evidence/01-robots.json)

#### SEO-04 · Non-home pages advertise locale homepages as alternates · HIGH

**URL examples** [/en/about](https://www.strawhatdevs.com/en/about), [/en/auth/forgot-password](https://www.strawhatdevs.com/en/auth/forgot-password), [/en/auth/sign-in](https://www.strawhatdevs.com/en/auth/sign-in), [/en/auth/sign-up](https://www.strawhatdevs.com/en/auth/sign-up). See the issue register for all 50 URLs.  
**Element** link[hreflang]  
**Observed** 50 non-home base routes advertise https://strawhatdevs.com/en and https://strawhatdevs.com/ta. Neither URL is a localized counterpart for an individual service, article, or utility page.  
**Expected** Equivalent, index-targeted locale pages use reciprocal links to their final locale URLs, including self references.  
**Impact** Search engines can disregard inconsistent language annotations.  
**Recommendation** Generate locale alternates per route. Publish them only when equivalent localized content exists.  
**Effort and status** Medium. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json)

#### SEO-06 · Contact prefill variants declare the homepage as canonical · MEDIUM

**URL examples** [/en/contact?service=AI%20%26%20automation](https://www.strawhatdevs.com/en/contact?service=AI%20%26%20automation), [/en/contact?service=APIs%20%26%20integrations](https://www.strawhatdevs.com/en/contact?service=APIs%20%26%20integrations), [/en/contact?service=Cloud%20%26%20DevOps](https://www.strawhatdevs.com/en/contact?service=Cloud%20%26%20DevOps), [/en/contact?service=Custom%20software](https://www.strawhatdevs.com/en/contact?service=Custom%20software). See the issue register for all 16 URLs.  
**Element** Contact route metadata and service query  
**Observed** 16 query variants returned 200 and declare the apex homepage. 16 appear in an exact main-text match group.  
**Expected** Prefill variants consolidate to the corresponding clean locale contact URL while preserving useful form context.  
**Impact** Duplicate URLs can dilute contact-page discovery and give search engines a conflicting canonical target.  
**Recommendation** Preserve service selection while generating canonical URLs from the stable contact route in each locale.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [08-content.json](SEO_Evidence/08-content.json) · [01-crawl.json](SEO_Evidence/01-crawl.json)

#### SEO-15 · Course detail content absent from initial HTML · MEDIUM

**URL examples** [/en/courses/docker](https://www.strawhatdevs.com/en/courses/docker), [/en/courses/engineering-fundamentals](https://www.strawhatdevs.com/en/courses/engineering-fundamentals), [/en/courses/git](https://www.strawhatdevs.com/en/courses/git), [/en/courses/go](https://www.strawhatdevs.com/en/courses/go). See the issue register for all 18 URLs.  
**Element** Course detail rendering  
**Observed** 18 course detail URLs returned 200 with course-specific metadata but no main text or H1 in source HTML. The browser found a course H1 after JavaScript on 18 catalog destinations.  
**Expected** Public course overviews expose the course title, essential details and useful navigation in initial HTML.  
**Impact** Discovery and content interpretation depend on client execution and successful data loading.  
**Recommendation** Server-render the course overview and public navigation. Retain interactive enrollment or lesson features as client components.  
**Effort and status** Medium. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [07-browser.json](SEO_Evidence/07-browser.json) · [07-course-navigation.json](SEO_Evidence/07-course-navigation.json)

#### SEO-18 · Tamil insight routes declare English canonicals and appear in the sitemap · MEDIUM

**URL examples** [/ta/insights](https://www.strawhatdevs.com/ta/insights), [/ta/insights/healthcare-front-desk-workflows](https://www.strawhatdevs.com/ta/insights/healthcare-front-desk-workflows), [/ta/insights/manufacturing-order-workflow](https://www.strawhatdevs.com/ta/insights/manufacturing-order-workflow), [/ta/insights/retail-mart-inventory-visibility](https://www.strawhatdevs.com/ta/insights/retail-mart-inventory-visibility). See the issue register for all 6 URLs.  
**Element** Tamil insights canonical and sitemap loc  
**Observed** Tamil insight URLs return the same English main copy, declare English canonicals and appear as separate Tamil sitemap entries.  
**Expected** Only the preferred English page is listed for an untranslated item; each published translation can have its own aligned canonical.  
**Impact** The sitemap and canonical tags recommend different URLs for the same main content.  
**Recommendation** While insight pages share English copy, list only the preferred English URLs. Add Tamil sitemap entries when localized pages are ready.  
**Effort and status** Small. Confirmed.  
**Evidence** [02-html.json](SEO_Evidence/02-html.json) · [01-sitemaps.json](SEO_Evidence/01-sitemaps.json) · [08-content.json](SEO_Evidence/08-content.json)

#### SEO-19 · Apex homepage takes three redirects to the final page · LOW

**URL examples** [http://strawhatdevs.com/](http://strawhatdevs.com/), [https://strawhatdevs.com/](https://strawhatdevs.com/), [/](https://www.strawhatdevs.com/).  
**Element** Host, locale and trailing slash redirects  
**Observed** HTTPS apex root returns 308 to www root, 307 to /en/, then 308 to /en. The HTTP apex adds an HTTP-to-HTTPS hop.  
**Expected** Reach the preferred URL with the fewest hops consistent with the locale selection policy.  
**Impact** Extra hops add request latency for visitors or crawlers starting at the root.  
**Recommendation** Coordinate hosting redirects and Next.js locale handling so the generated locale URL already uses the preferred slash form.  
**Effort and status** Small. Confirmed.  
**Evidence** [01-crawl.json](SEO_Evidence/01-crawl.json)

| URL or resource | Technical check | Actual result | Expected result | Severity | Recommendation |
| --- | --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/en/consulting | Canonical | https://strawhatdevs.com | https://www.strawhatdevs.com/en/consulting | HIGH | SEO-01 |
| https://www.strawhatdevs.com/sitemap.xml | Sitemap loc validity | 34 entries redirect | Direct 200 URLs | HIGH | SEO-03 |
| https://www.strawhatdevs.com/en/blogs | Language alternates | Locale homepages | Equivalent article listings | HIGH | SEO-04 |
| https://www.strawhatdevs.com/ta/insights | Locale canonical | https://strawhatdevs.com/en/insights | Align sitemap with chosen preferred locale | MEDIUM | SEO-18 |
| https://www.strawhatdevs.com/robots.txt | Crawl policy | 200; disallows /private/ and /admin/ | Rules match intended public access | INFO | Recheck after URL policy changes |
| https://www.strawhatdevs.com/en/seo-audit-public-not-found | Missing path | 404 | 404 | INFO | Observe after routing changes |

### Website performance

The lab sample covers the homepage, consulting, manufacturing solution, consultation landing page and an engineering blog article. See Section 4 for full mobile and desktop results.

#### SEO-10 · Homepage hero drives slow mobile LCP in the lab · HIGH

**URL examples** [/en](https://www.strawhatdevs.com/en).  
**Element** Homepage hero image and request priority  
**Observed** Mobile Lighthouse LCP was 8.09 s. Its LCP node uses /coding-on-laptop.png (895,857 bytes, PNG, 1024×680); the markup sends a single source and the asset is preloaded.  
**Expected** Aim for LCP at or below 2.5 s; validate separately with field p75 when available.  
**Impact** A slow hero delays the largest visible homepage element on constrained connections.  
**Recommendation** Serve quality-checked responsive WebP or AVIF variants, align preload with the chosen candidate, and prioritize only the hero request.  
**Effort and status** Medium. Confirmed.  
**Evidence** [home-mobile.json](SEO_Evidence/lighthouse/home-mobile.json) · [03-images.json](SEO_Evidence/03-images.json) · [07-browser.json](SEO_Evidence/07-browser.json)

#### SEO-16 · Mobile lab runs exceeded the TBT target on sampled templates · MEDIUM

**URL examples** [/en](https://www.strawhatdevs.com/en), [/en/blogs/system-design-basics-scaling-simple-app](https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app), [/en/consulting](https://www.strawhatdevs.com/en/consulting), [/en/schedule](https://www.strawhatdevs.com/en/schedule). See the issue register for all 5 URLs.  
**Element** Main-thread long tasks and startup bundles  
**Observed** Single-run mobile TBT above the 200 ms Lighthouse reference on home (256 ms), consulting (694 ms), manufacturing (598 ms), schedule (551 ms), blog (492 ms).  
**Expected** Aim for mobile Lighthouse TBT at or below 200 ms and measure INP separately in field data.  
**Impact** Long tasks may delay interactive readiness during page load.  
**Recommendation** Use the bootup-time and network sections to attribute work to shared Next.js chunks, component hydration and third-party tags. Defer client code unrelated to initial use.  
**Effort and status** Medium. Confirmed.  
**Evidence** [home-mobile.json](SEO_Evidence/lighthouse/home-mobile.json) · [consulting-mobile.json](SEO_Evidence/lighthouse/consulting-mobile.json) · [manufacturing-mobile.json](SEO_Evidence/lighthouse/manufacturing-mobile.json) · [schedule-mobile.json](SEO_Evidence/lighthouse/schedule-mobile.json) · [blog-mobile.json](SEO_Evidence/lighthouse/blog-mobile.json)

### Mobile SEO

Chromium sampled 10 templates/routes at 360 px, 390 px and 1,365 px. The mobile drawer opened and its Learn group exposed courses and articles after expansion. The sampled layouts showed no viewport-level horizontal overflow. Core marketing copy and headings were present across devices. The course overview loaded its H1 and content after client rendering. Narrow inline or isolated links flagged by geometry need spacing and exception review before classifying a target-size issue. [Evidence](SEO_Evidence/07-browser.json) · [Expanded mobile menu](SEO_Evidence/browser/home-390-menu-expanded.png)

| URL | Device | Issue | Evidence | Impact | Recommendation |
| --- | --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/en | 390 px touch | No overflow or nav blocker observed | 390 px document; Learn expanded | Navigation can expose course and blog links | Recheck after header changes |
| https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app | 390 px touch | 20 px link height; manual review | Back to Blogs bounding box 148×20 CSS px | Spacing/inline-context exceptions require review | Review tap spacing on device |
| https://www.strawhatdevs.com/en/courses/docker | 360/390 px touch | Course content depends on JavaScript | Rendered course H1 compared with empty source main | Public course overview requires successful hydration | SEO-15 |

### Content SEO

Compared extracted main content, headings, routes and page purpose across both locales. The site covers business software services, consultation, educational articles and learning paths. The work page says permissioned case studies are being prepared. First-hand proof is an opportunity when publishable evidence exists. The short work/contact content serves transactional or trust intent. Market-wide keyword gaps, rankings and search volume were outside the observable evidence. [Evidence](SEO_Evidence/08-content.json)

#### SEO-12 · Tamil routes show the same English main content as English routes · MEDIUM

**URL examples** [/ta](https://www.strawhatdevs.com/ta), [/ta/about](https://www.strawhatdevs.com/ta/about), [/ta/contact](https://www.strawhatdevs.com/ta/contact), [/ta/insights](https://www.strawhatdevs.com/ta/insights). See the issue register for all 13 URLs.  
**Element** Localized body content and locale signals  
**Observed** 13 Tamil routes declare lang="ta" while their extracted main text matches the English route and contains zero Tamil-script characters. Compare the paired English/Tamil excerpts. Tamil insight canonicals point to their English routes.  
**Expected** A Tamil-targeted URL delivers an equivalent Tamil page or the locale selector transparently leads to the English original.  
**Impact** Users choosing Tamil can land on English copy. Separate English copies may be crawled and consolidated.  
**Recommendation** Translate the pages prioritized for Tamil users. Until translations are ready, align locale availability, navigation, sitemap membership and canonical decisions with the actual content.  
**Effort and status** Large. Confirmed.  
**Evidence** [08-content.json](SEO_Evidence/08-content.json) · [02-html.json](SEO_Evidence/02-html.json)

| URL | Content issue | Evidence | Search intent | Recommendation |
| --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/ta | SEO-12 | Main copy exactly matches English homepage | Business and learning discovery | Translate homepage and then apply locale-specific signals |
| https://www.strawhatdevs.com/ta/solutions/manufacturing-software | SEO-12 | English-only solution body with lang=ta | Evaluate manufacturing software | Translate for Tamil buyers if that is the intended market |
| https://www.strawhatdevs.com/en/work | Opportunity | Work copy describes case studies as in preparation | Evaluate delivery capability | Publish permissioned case studies when supporting evidence is available |

### Structured data

Source inspection found no JSON-LD blocks or sampled Microdata or RDFa markers. There were no source entities to validate for syntax, vocabulary, duplicates or visible-content consistency. Google feature eligibility was not tested. Organization and Article are relevant candidates. BreadcrumbList depends on a real site hierarchy. A Service type may describe a real service in Schema.org, while Google search features have separate documented requirements. [Google structured data feature gallery](https://developers.google.com/search/docs/appearance/structured-data/search-gallery)

#### SEO-13 · Article and organization markup opportunities · INFO

**URL examples** [/en](https://www.strawhatdevs.com/en), [/en/blogs/clean-code-habits-junior-developers](https://www.strawhatdevs.com/en/blogs/clean-code-habits-junior-developers), [/en/blogs/learn-programming-in-tamil-without-getting-stuck](https://www.strawhatdevs.com/en/blogs/learn-programming-in-tamil-without-getting-stuck), [/en/blogs/system-design-basics-scaling-simple-app](https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app). See the issue register for all 17 URLs.  
**Element** JSON-LD, Microdata and RDFa  
**Observed** No JSON-LD blocks or sampled Microdata/RDFa markers in 86 source HTML documents.  
**Expected** Optional Organization and Article markup accurately mirrors visible business and editorial information when added.  
**Impact** Potential enhancement to entity and article understanding. Rich presentation is subject to Google’s eligibility rules.  
**Recommendation** Consider Organization on the homepage and Article/BlogPosting where the visible author, date, title and image support it.  
**Effort and status** Medium. Opportunity.  
**Evidence** [09-structured-data.json](SEO_Evidence/09-structured-data.json) · [02-html.json](SEO_Evidence/02-html.json)

| URL | Schema type | Validation result | Issue | Recommendation |
| --- | --- | --- | --- | --- |
| https://www.strawhatdevs.com/en | Organization | Absent in tested source markup | SEO-13 opportunity | Add factual organization identity if desired |
| https://www.strawhatdevs.com/en/blogs/system-design-basics-scaling-simple-app | Article | Absent in tested source markup | SEO-13 opportunity | Use visible author/date/title/image information |
| https://www.strawhatdevs.com/en/consulting | Service | Absent in tested source markup | Optional vocabulary | Use only if it accurately describes the service |

### Security and trust signals

The main host served HTTPS with successful browser loads, and the HTTP apex redirects to HTTPS. Sampled browser navigations showed no HTTP subresource requests or mixed-content console errors. Both locale routes for About, Contact and Terms resolved. The two guessed privacy paths returned 404. A public policy may exist elsewhere. Checkout, authentication and form submission were outside the public read-only checks.

#### SEO-14 · Public privacy notice path needs confirmation · INFO

**URL examples** [/en/auth/sign-up](https://www.strawhatdevs.com/en/auth/sign-up), [/en/contact](https://www.strawhatdevs.com/en/contact), [/en/schedule](https://www.strawhatdevs.com/en/schedule), [/ta/contact](https://www.strawhatdevs.com/ta/contact).  
**Element** Privacy navigation and form-adjacent disclosures  
**Observed** The checked /en/privacy and /en/privacy-policy routes returned 404 and no privacy route was discovered in crawled anchors.  
**Expected** Visitors can reach the applicable privacy notice from public contact and account forms.  
**Impact** A visible notice helps visitors understand how submitted information is used.  
**Recommendation** Verify whether a notice exists under another route or within the relevant form or terms. Surface its public destination if needed.  
**Effort and status** Small. NEEDS MANUAL VERIFICATION.  
**Evidence** [10-trust.json](SEO_Evidence/10-trust.json) · [05-route-probes.json](SEO_Evidence/05-route-probes.json) · [02-html.json](SEO_Evidence/02-html.json)

## 4. Performance report

Lighthouse 13.6.0 was run once for each page/device pair. Results are cold-navigation lab snapshots and vary with route, server, network and host conditions. The mobile and desktop presets have different throttling and scoring. LCP, FCP, Speed Index and TBT below are in milliseconds. CLS is unitless and transfer uses bytes. PageSpeed returned HTTP 429 for all ten requests, so page and origin field p75 values for LCP, INP and CLS remain unmeasured.

| Template | Device | Score | LCP (ms) | CLS | FCP (ms) | Speed Index (ms) | TBT (ms) | Transfer (bytes) | Evidence |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| home | mobile | 58 | 8086.8 | 0 | 3306.7 | 6424.9 | 256.5 | 1598608 | [JSON](SEO_Evidence/lighthouse/home-mobile.json) |
| home | desktop | 92 | 1803.4 | 0 | 521.0 | 1188.5 | 69 | 1709322 | [JSON](SEO_Evidence/lighthouse/home-desktop.json) |
| consulting | mobile | 82 | 1344.9 | 0 | 1344.9 | 2763.0 | 693.5 | 540739 | [JSON](SEO_Evidence/lighthouse/consulting-mobile.json) |
| consulting | desktop | 85 | 307.1 | 0 | 307.1 | 1281.5 | 327.0 | 678628 | [JSON](SEO_Evidence/lighthouse/consulting-desktop.json) |
| manufacturing | mobile | 85 | 1193.7 | 0 | 1193.7 | 2341.0 | 598.0 | 3472707 | [JSON](SEO_Evidence/lighthouse/manufacturing-mobile.json) |
| manufacturing | desktop | 100 | 357.0 | 0 | 357.0 | 985.7 | 30.5 | 3594584 | [JSON](SEO_Evidence/lighthouse/manufacturing-desktop.json) |
| schedule | mobile | 82 | 1962.0 | 0.067 | 1962.0 | 3012.1 | 551 | 2246786 | [JSON](SEO_Evidence/lighthouse/schedule-mobile.json) |
| schedule | desktop | 98 | 391.5 | 0.069 | 391.5 | 1256.4 | 19.5 | 2338453 | [JSON](SEO_Evidence/lighthouse/schedule-desktop.json) |
| blog | mobile | 62 | 11689.8 | 0 | 1037.1 | 2715.6 | 492 | 2108169 | [JSON](SEO_Evidence/lighthouse/blog-mobile.json) |
| blog | desktop | 87 | 2359.0 | 0 | 565.3 | 1171.5 | 0 | 2109060 | [JSON](SEO_Evidence/lighthouse/blog-desktop.json) |

[Metric-level performance CSV](SEO_Performance_Report.csv) · [Sample PSI error](SEO_Evidence/pagespeed/home-mobile.json) · [Google PageSpeed field and lab methodology](https://developers.google.com/speed/docs/insights/v5/about)

| Template | Device | Requests | Image kB | Script kB | CSS kB | Font kB | Third-party kB | JS execution |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| home | mobile | 46 | 1,014.9 | 407.2 | 20.5 | 111.9 | 119.2 | 1.2 s |
| home | desktop | 51 | 1,125.1 | 407.1 | 20.5 | 111.9 | 119.2 | 0.3 s |
| consulting | mobile | 36 | 6.2 | 361.2 | 20.5 | 111.9 | 119.2 | 1.3 s |
| consulting | desktop | 48 | 127.5 | 363.3 | 20.5 | 111.9 | 119.2 | 0.3 s |
| manufacturing | mobile | 42 | 2,854.2 | 359.3 | 20.5 | 197.4 | 119.2 | 1.4 s |
| manufacturing | desktop | 50 | 2,975.5 | 359.3 | 20.5 | 197.5 | 119.2 | 0.2 s |
| schedule | mobile | 121 | 12.5 | 1,718.3 | 118.5 | 310.3 | 1,827.0 | 1.2 s |
| schedule | desktop | 124 | 14.6 | 1,718.2 | 118.2 | 310.5 | 1,918.2 | 0.2 s |
| blog | mobile | 40 | 1,526.7 | 406.9 | 20.5 | 111.8 | 1,639.7 | 1.1 s |
| blog | desktop | 42 | 1,526.7 | 407.3 | 20.5 | 111.9 | 1,640.0 | 0.1 s |

The homepage hero was the measured mobile LCP element. The manufacturing template transferred roughly 2.85 MB of images in the mobile sample even though its LCP element was text. Lighthouse identified shared Next.js chunks and Google Tag Manager in JavaScript execution. The reports retain the render-blocking stylesheet list, font waterfall, request priorities, cache checks and script timings. Compare these details with repeated runs when testing a fix.

## 5. Issue summary

| Category | Critical | High | Medium | Low | Info |
| --- | --- | --- | --- | --- | --- |
| HTML and on-page SEO | 0 | 0 | 1 | 3 | 0 |
| Image SEO | 0 | 0 | 1 | 0 | 0 |
| Internal and external links | 0 | 0 | 2 | 0 | 0 |
| Technical SEO | 0 | 3 | 4 | 1 | 0 |
| Website performance | 0 | 1 | 1 | 0 | 0 |
| Mobile SEO | 0 | 0 | 0 | 0 | 0 |
| Content SEO | 0 | 0 | 1 | 0 | 0 |
| Structured data | 0 | 0 | 0 | 0 | 1 |
| Security and trust signals | 0 | 0 | 0 | 0 | 1 |

| ID | Category | Issue | Affected URLs | Severity | Evidence | Recommended fix | Effort | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| SEO-01 | Technical SEO | Distinct public routes declare the apex homepage as canonical | 44 | HIGH | [Evidence](SEO_Evidence/02-html.json) | Move default canonical generation into the locale-aware Next.js metadata layer. Set route canonicals for each independently indexable page. | Medium | Confirmed |
| SEO-02 | Technical SEO | Route-specific canonicals point to a redirecting host | 12 | MEDIUM | [Evidence](SEO_Evidence/02-html.json) | Set the preferred origin in the Next.js metadata base/config and keep the resolved path. | Small | Confirmed |
| SEO-03 | Technical SEO | Sitemap lists redirect sources | 34 | HIGH | [Evidence](SEO_Evidence/01-sitemaps.json) | Generate XML from the preferred URL registry after the canonical and locale decisions. Update robots.txt to the served sitemap URL. | Small | Confirmed |
| SEO-04 | Technical SEO | Non-home pages advertise locale homepages as alternates | 50 | HIGH | [Evidence](SEO_Evidence/02-html.json) | Generate locale alternates per route. Publish them only when equivalent localized content exists. | Medium | Confirmed |
| SEO-05 | Internal and external links | Two product repository links returned 404 | 2 | MEDIUM | [Evidence](SEO_Evidence/04-links.json) | Confirm whether the repositories were moved, made private, or removed, then update or remove each public link. | Small | Confirmed |
| SEO-06 | Technical SEO | Contact prefill variants declare the homepage as canonical | 16 | MEDIUM | [Evidence](SEO_Evidence/02-html.json) | Preserve service selection while generating canonical URLs from the stable contact route in each locale. | Small | Confirmed |
| SEO-07 | HTML and on-page SEO | About, work and contact reuse generic titles and descriptions | 6 | MEDIUM | [Evidence](SEO_Evidence/02-html.json) | Add route-specific metadata to the about, contact and work page modules in both locales. | Small | Confirmed |
| SEO-08 | HTML and on-page SEO | Blog and course listings lack an H1 | 4 | LOW | [Evidence](SEO_Evidence/02-html.json) | Change the primary heading element in the shared listing templates and adjust child heading levels as needed. | Small | Confirmed |
| SEO-09 | HTML and on-page SEO | Open Graph URL points to the homepage on interior pages | 23 | LOW | [Evidence](SEO_Evidence/02-html.json) | Set page-aware Open Graph URLs and verify relevant title, description and image values. | Small | Confirmed |
| SEO-10 | Website performance | Homepage hero drives slow mobile LCP in the lab | 1 | HIGH | [Evidence](SEO_Evidence/lighthouse/home-mobile.json) | Serve quality-checked responsive WebP or AVIF variants, align preload with the chosen candidate, and prioritize only the hero request. | Medium | Confirmed |
| SEO-11 | Image SEO | Large fixed-source PNGs increase transfer across solution and editorial templates | 16 | MEDIUM | [Evidence](SEO_Evidence/03-images.json) | Use Sanity size/format variants for editorial media and responsive exports for the solution illustrations. Preserve appropriate lazy loading for below-fold media. | Medium | Confirmed |
| SEO-12 | Content SEO | Tamil routes show the same English main content as English routes | 13 | MEDIUM | [Evidence](SEO_Evidence/08-content.json) | Translate the pages prioritized for Tamil users. Until translations are ready, align locale availability, navigation, sitemap membership and canonical decisions with the actual content. | Large | Confirmed |
| SEO-13 | Structured data | Article and organization markup opportunities | 17 | INFO | [Evidence](SEO_Evidence/09-structured-data.json) | Consider Organization on the homepage and Article/BlogPosting where the visible author, date, title and image support it. | Medium | Opportunity |
| SEO-14 | Security and trust signals | Public privacy notice path needs confirmation | 4 | INFO | [Evidence](SEO_Evidence/10-trust.json) | Verify whether a notice exists under another route or within the relevant form or terms. Surface its public destination if needed. | Small | NEEDS MANUAL VERIFICATION |
| SEO-15 | Technical SEO | Course detail content absent from initial HTML | 18 | MEDIUM | [Evidence](SEO_Evidence/02-html.json) | Server-render the course overview and public navigation. Retain interactive enrollment or lesson features as client components. | Medium | Confirmed |
| SEO-16 | Website performance | Mobile lab runs exceeded the TBT target on sampled templates | 5 | MEDIUM | [Evidence](SEO_Evidence/lighthouse/home-mobile.json) | Use the bootup-time and network sections to attribute work to shared Next.js chunks, component hydration and third-party tags. Defer client code unrelated to initial use. | Medium | Confirmed |
| SEO-17 | Internal and external links | Catalog course cards use JavaScript-only navigation | 2 | MEDIUM | [Evidence](SEO_Evidence/07-course-navigation.json) | Use locale-aware anchor links for course destinations and linkable pagination. Keep the cards as client components where needed. | Medium | Confirmed |
| SEO-18 | Technical SEO | Tamil insight routes declare English canonicals and appear in the sitemap | 6 | MEDIUM | [Evidence](SEO_Evidence/02-html.json) | While insight pages share English copy, list only the preferred English URLs. Add Tamil sitemap entries when localized pages are ready. | Small | Confirmed |
| SEO-19 | Technical SEO | Apex homepage takes three redirects to the final page | 3 | LOW | [Evidence](SEO_Evidence/01-crawl.json) | Coordinate hosting redirects and Next.js locale handling so the generated locale URL already uses the preferred slash form. | Small | Confirmed |
| SEO-20 | HTML and on-page SEO | Navigation nests buttons inside links | 84 | LOW | [Evidence](SEO_Evidence/02-nu-home.json) | Render the navigational control as a styled link via the shared navigation component. | Small | Confirmed |

## 6. Developer action plan

### Immediate triage

No critical issue was confirmed. Agree on the preferred origin and which locale variants should appear in search before changing shared metadata.

### High-priority fixes

| ID | Component | Change | Validation |
| --- | --- | --- | --- |
| SEO-01 | link[rel=canonical] | Move default canonical generation into the locale-aware Next.js metadata layer. Set route canonicals for each independently indexable page. | Extract canonical tags from HTML for each affected route and confirm the exact target returns 200. Verify Google-selected canonical in Search Console when available. |
| SEO-03 | XML sitemap and robots.txt directive | Generate XML from the preferred URL registry after the canonical and locale decisions. Update robots.txt to the served sitemap URL. | Parse the sitemap and check every loc with redirects disabled. Verify indexability signals after the template update. |
| SEO-04 | link[hreflang] | Generate locale alternates per route. Publish them only when equivalent localized content exists. | Verify self references, reciprocal references, direct 200 targets and canonical alignment for representative route pairs. |
| SEO-10 | Homepage hero image and request priority | Serve quality-checked responsive WebP or AVIF variants, align preload with the chosen candidate, and prioritize only the hero request. | Check the selected candidate at multiple DPRs and compare repeated cold mobile Lighthouse runs. Review CrUX p75 when available. |

### Medium-priority improvements

| ID | Component | Change | Validation |
| --- | --- | --- | --- |
| SEO-02 | link[rel=canonical] | Set the preferred origin in the Next.js metadata base/config and keep the resolved path. | Fetch each declared canonical without redirect following and confirm a direct 200. |
| SEO-05 | Product-card links | Confirm whether the repositories were moved, made private, or removed, then update or remove each public link. | Follow each corrected link in a signed-out session and confirm the expected project is visible. |
| SEO-06 | Contact route metadata and service query | Preserve service selection while generating canonical URLs from the stable contact route in each locale. | Check canonical output with and without query parameters and verify the service still prefills. |
| SEO-07 | title, meta[name=description] | Add route-specific metadata to the about, contact and work page modules in both locales. | Compare titles and descriptions within each language after deployment. |
| SEO-11 | Solution illustrations and Sanity raster media | Use Sanity size/format variants for editorial media and responsive exports for the solution illustrations. Preserve appropriate lazy loading for below-fold media. | Compare visual quality and transfer sizes at mobile and desktop widths. Inspect currentSrc and the network waterfall. |
| SEO-12 | Localized body content and locale signals | Translate the pages prioritized for Tamil users. Until translations are ready, align locale availability, navigation, sitemap membership and canonical decisions with the actual content. | Review visible language manually, then verify sitemap, canonicals and hreflang for each published translation. |
| SEO-15 | Course detail rendering | Server-render the course overview and public navigation. Retain interactive enrollment or lesson features as client components. | Compare the initial response with the hydrated page and verify the main course content appears in both. |
| SEO-16 | Main-thread long tasks and startup bundles | Use the bootup-time and network sections to attribute work to shared Next.js chunks, component hydration and third-party tags. Defer client code unrelated to initial use. | Repeat Lighthouse under identical settings and inspect long tasks in the Chrome Performance panel. |
| SEO-17 | Course card navigation and pagination | Use locale-aware anchor links for course destinations and linkable pagination. Keep the cards as client components where needed. | Disable JavaScript, follow course and pagination links, then crawl from each locale catalog to confirm public course coverage. |
| SEO-18 | Tamil insights canonical and sitemap loc | While insight pages share English copy, list only the preferred English URLs. Add Tamil sitemap entries when localized pages are ready. | Compare canonical and XML membership for every insight pair and confirm the chosen targets return a direct 200. |

### Low-priority enhancements

| ID | Component | Change | Validation |
| --- | --- | --- | --- |
| SEO-08 | Listing title hierarchy | Change the primary heading element in the shared listing templates and adjust child heading levels as needed. | Inspect both locales in initial HTML and rendered DOM for one meaningful leading H1. |
| SEO-09 | meta[property=og:url] | Set page-aware Open Graph URLs and verify relevant title, description and image values. | Read the final HTML and test representative social previews. |
| SEO-19 | Host, locale and trailing slash redirects | Coordinate hosting redirects and Next.js locale handling so the generated locale URL already uses the preferred slash form. | Run a header-only or GET redirect trace in a clean session for HTTP/HTTPS and www/apex. |
| SEO-20 | Shared public navigation markup | Render the navigational control as a styled link via the shared navigation component. | Run Nu again on both templates and keyboard-test each navigation action. |

### Manual investigation and optional work

| ID | Check | Validation |
| --- | --- | --- |
| SEO-13 | Article and organization markup opportunities | Validate vocabulary with Schema.org Validator and Google-supported features with the Rich Results Test. |
| SEO-14 | Public privacy notice path needs confirmation | Check the form, terms and public navigation in both languages. |

## 7. Untested items and limitations

- Public observational analysis. Search Console and analytics exports were unavailable. Google index coverage, Google-selected canonicals, rankings, traffic and conversions are **NOT TESTED**.
- Screaming Frog was unavailable on PATH. The fallback used Python requests, Beautiful Soup, Pillow and Playwright with Chrome.
- W3C/Nu validation covered the homepage and English consulting page. Other URLs received local source inspection. External schema validators and the Rich Results Test were **NOT TESTED**.
- PageSpeed Insights returned **429**. Field CrUX LCP, INP and CLS are **NOT TESTED** for both page and origin levels.
- Authenticated content, course enrollment, private lessons, form submission and authenticated analytics were **NOT TESTED**. There may be public URLs outside sources discoverable from seeds, sitemap, HTML anchors and the exercised catalog flows. Separately hosted product subdomains were treated as linked destinations where discovered within scope.
- Device testing used Chromium emulation and selected public interactions. Other browsers, assistive technologies, every breakpoint, and complete per-image display dimensions were **NOT TESTED**.
- The external checks followed observed robots and host rules. LinkedIn, Instagram and npm target availability remain **UNVERIFIED**.
- This audit observed HTTPS and trust signals through ordinary public requests and rendered samples. Security testing was outside scope.

## 8. Final recommendations

1. Fix the canonical and locale metadata rules together, then regenerate the sitemap with direct 200 destinations. Verify canonical alignment across page templates before checking Google’s selection with Search Console. [Google canonical guidance](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) · [Google localized-version guidance](https://developers.google.com/search/docs/specialty/international/localized-versions)
2. Reduce the homepage hero transfer and verify request priority in mobile traces. Apply responsive media delivery to the heaviest solution and editorial images and profile shared JavaScript.
3. Make every public course overview reachable through an HTML link and expose core course content in the initial response.
4. Review language availability for duplicate English/Tamil routes, repair product links, write unique commercial metadata and confirm the privacy notice location before adding optional structured data.
