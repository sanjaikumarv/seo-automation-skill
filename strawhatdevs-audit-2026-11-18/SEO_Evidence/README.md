# Straw Hat Devs audit evidence

Captured 18 November 2026 (IST). URLs in these files are public audit inputs. Each issue links to the relevant capture in the [main report](../SEO_Audit_Report.md) and [issue register](../SEO_Issue_Register.csv).

| Evidence | Contents |
| --- | --- |
| [Crawl responses](01-crawl.json) | Requested URLs, timestamped HTTP hops, headers, final URL, discovery sources and pointers to preserved HTML in `responses/` |
| [Robots](01-robots.json) and [sitemaps](01-sitemaps.json) | Robots responses, XML parse results and sitemap URL membership |
| [HTML extraction](02-html.json) | Titles, headings, canonical tags, locale and social metadata, source anchors and other markup from each captured final page |
| [W3C Nu homepage](02-nu-home.json) and [consulting](02-nu-consulting.json) | Raw external validator responses for the two templates |
| [First-party images](03-images.json) and [Sanity CDN images](03-cdn-images.json) | HTTP status, image format, decoded file size and intrinsic dimensions |
| [Link verification](04-links.json) | External destinations, source pages, response status, redirect and robots observations |
| [Route probes](05-route-probes.json) and [search spot check](05-public-search.md) | Public missing-route, slash and privacy checks, plus sampled public search visibility |
| [Performance sample](06-sample.json) | Exact URLs sent to PageSpeed Insights and Lighthouse; device-specific JSON in `pagespeed/` and `lighthouse/` |
| [Browser measurements](07-browser.json) | Viewport dimensions, visible DOM, small-target candidates, image layout, network and console observations, and screenshot pointers |
| [Mobile navigation](07-menu-navigation.json) | Settled mobile navigation states and labels; screenshot in [browser/home-390-menu-expanded.png](browser/home-390-menu-expanded.png) |
| [Course navigation](07-course-navigation.json) and [course HTTP follow-up](07-course-followup-http.json) | Browser-exposed catalog destinations, rendered headings and the corresponding source HTTP evidence for newly surfaced routes |
| [Content comparison](08-content.json) | Exact main-text matches, language checks and paired excerpts |
| [Structured data](09-structured-data.json) and [trust checks](10-trust.json) | Source-markup inspection and public legal/contact navigation evidence |

HTML and XML snapshots preserve downloaded response bodies. Lighthouse JSON includes diagnostic estimates. Browser screenshots show the sampled viewports at capture time.
