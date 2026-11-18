# Straw Hat Devs SEO audit · Executive summary

**18 November 2026, IST**  
**Website** [Straw Hat Devs](https://www.strawhatdevs.com/en)  
**Coverage** 123 URL strings evaluated and 86 distinct HTML destinations inspected across English and Tamil.

The audit confirmed **18 issues**, with 0 critical, 4 high, 10 medium, 4 low. Canonical and sitemap inconsistencies are the most important risk to search discovery. Google index status requires Search Console verification.

- **Search discovery.** All 34 sitemap entries redirect. Several distinct commercial and editorial pages declare the homepage as canonical, and multiple interior pages advertise the locale homepages as alternates.
- **Mobile performance.** The homepage scored 58/100 in the mobile Lighthouse run and recorded 8.09 s lab LCP. The 896 kB hero PNG was the measured LCP element. PageSpeed Insights returned 429, leaving field data unverified.
- **Course discovery.** Catalog buttons exposed 12 course URLs missing from the source-link crawl and sitemap. Course overviews also depend on JavaScript to show their main content.
- **Maintenance.** Two public product repository links returned 404. Several Tamil pages repeat English content. The public privacy notice location needs confirmation.

Prioritize the canonical, locale and sitemap fixes, followed by homepage image delivery and crawlable course navigation. The issue register names the affected URLs, fix effort and validation criteria.

[Full audit report](SEO_Audit_Report.md) · [Issue register](SEO_Issue_Register.csv) · [Page inventory](SEO_Page_Inventory.csv) · [Performance results](SEO_Performance_Report.csv)
