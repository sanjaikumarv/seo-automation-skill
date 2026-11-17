# Local SEO and Business Profile Assessment

Run: `strawhatdevs-2026-11-18` | Observed: 18 November 2026, IST

Target: https://www.strawhatdevs.com/en | Brand: Straw Hat Devs

## Local SEO executive assessment

Target: Coimbatore queries plus India/global delivery for startups and SMEs. Read the audit and local keyword mappings. The current [contact page](https://www.strawhatdevs.com/en/contact) explicitly identifies Coimbatore and remote India service coverage. This supports service-area wording but does not establish a customer-facing office, exact address, Google Business Profile eligibility or ownership.

Public brand/Maps/Apple/Bing searches did not identify a verifiable matching map listing during this sample. Apple Maps was inaccessible to the browsing tool. **Not verified is not the same as nonexistent.** No GBP account was connected; profile claim status, categories, reviews, Maps rankings and owner-only fields remain unknown.

## Google Business Profile audit scorecard

| Factor | Current evidence | Recommended action | Priority |
| --- | --- | --- | --- |
| Profile URL / ownership | Not verified | Locate an existing authentic profile first; check duplicates before creating anything | P1 |
| Eligibility | In-person customer contact not established | Owner must confirm actual in-person eligibility; online-only businesses are not automatically eligible | P1 |
| Official name | Straw Hat Devs across live site and LinkedIn | Retain the real business name; do not append keyword/location strings | P1 |
| Primary category | Unknown | If eligible, choose the current available category that matches the primary delivered service; software company is a candidate to verify | P2 |
| Secondary categories | Unknown | Add only actually offered activities supported by current category options | P2 |
| Description / services | No verified GBP fields | Use the draft below after eligibility and scope review | P2 |
| Phone, office, opening hours | Not established on current contact page | Owner verification needed; do not transplant old snippets as current facts | P1 |
| Photos / logo | Site brand assets exist; GBP assets uninspected | Use genuine brand/team/workplace visuals, not AI-generated office evidence | P2 |
| Reviews and reply history | Unknown | Retrieve actual profile evidence before reporting counts or themes | P2 |

Google's [business representation guidelines](https://support.google.com/business/answer/3038177) require a qualifying real-world customer-contact model. Do not claim an office, use a virtual-office address, or expose a home address to satisfy a template. For an eligible service-area business, configure the real service area and address visibility appropriately; no profile edits were made.

## NAP and citation consistency matrix

| Source | Name | Address / locality | Phone / contact | Assessment |
| --- | --- | --- | --- | --- |
| Live contact page | Straw Hat Devs | Serving Coimbatore and remote India; no street address | Project inquiry form; no public business phone in sampled content | Current source of service-area wording |
| Live terms page | Straw Hat Devs | Coimbatore appears in terms; not a business-address record | `support@softwareschooltamil.us` | Legacy-domain support contact is still published; confirm desired contact before change |
| LinkedIn company page | Straw Hat Devs | Coimbatore, postal locality shown; not independently verified office | Website still points to `www.softwareschooltamil.us` | Brand/website mismatch to review with owner |
| Search snippet for contact | Straw Hat Devs | No verified address | Older phone/email/hours shown | Stale relative to current live contact; do not reuse as verified current NAP |
| Google Maps | Not verified | Unknown | Unknown | No claim of absence or consistency |
| Apple Maps | Not verified; tool access blocked | Unknown | Unknown | Owner/manual check needed |
| Bing Places/Maps | Not verified | Unknown | Unknown | Owner/manual check needed |
| Yelp / YellowPages / industry directories | No matching listing validated in this sample | Unknown | Unknown | Select relevant platforms after identity record is approved |

[LinkedIn company evidence](https://in.linkedin.com/company/strawhatdevs) supports a Coimbatore association and still references the earlier website. It does not prove the postal locality is a visitable office. The current live form has changed since the cached search snippet. Use one owner-approved identity sheet (business name, canonical site, contact channels and eligible location details) before changing citations. No BBB relevance is assumed for this India-focused business.

## Draft business description and service inventory

Draft for review, below 750 characters:

> Straw Hat Devs helps startups and small businesses plan and build custom software, websites, web and mobile applications, SaaS products and practical AI workflows. We work through requirements, integrations and delivery scope with businesses in Coimbatore and across India, and welcome international project discussions. Our services combine business-focused software engineering with a practical developer learning platform.

Candidate service entries: custom software development; website and web application development; mobile applications; SaaS and multi-tenant applications; workflow automation and AI integration; e-commerce development; technical SEO optimization. These reflect user-supplied offerings; do not add invented prices, guaranteed outcomes or certifications. Link each listed service to an actual useful page when available.

## Customer review acquisition and response playbook

No verified direct review URL, review count, average rating or review theme was obtained. Use the owner's real profile review link only after verification. Do not invent a place ID.

Unsent review-request draft:

> Thank you for working with Straw Hat Devs. If you would like to share your experience, an honest review helps others understand our work. We welcome your feedback, whether positive or critical. Once our verified review link is available, we can share it with you. Please avoid including confidential project details.

Send neutral requests to eligible customers consistently, without incentives or filtering by satisfaction. Do not solicit only positive reviews or script five-star wording. No emails or requests have been sent.

Positive response template: “Thank you for sharing your experience. We appreciate the opportunity to work with you and your feedback on the project.” Personalize only with public, consented details.

Critical response template: “Thank you for the feedback. We would like to understand what happened and discuss a practical next step. Please contact us through our project inquiry channel so we can review the details privately.” Do not admit unverified events or disclose private client information.

## Conditional LocalBusiness schema — hold for owner verification

The following is a **partial structural draft**, not a deployable LocalBusiness rich-result implementation. It omits an unverified street address, coordinates, telephone, opening hours and review ratings. Deploy the verified Organization/Service graph from Step 4 instead for now. Only consider changing the organization entity's type after actual local-business details and relevance are established. Do not create a second contradictory organization node.

```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "@id": "https://www.strawhatdevs.com/#organization",
  "name": "Straw Hat Devs",
  "url": "https://www.strawhatdevs.com/en",
  "areaServed": [
    {
      "@type": "City",
      "name": "Coimbatore"
    },
    {
      "@type": "Country",
      "name": "India"
    }
  ]
}
```


[Google's LocalBusiness structured-data guidance](https://developers.google.com/search/docs/appearance/structured-data/local-business) includes required/recommended properties and validation considerations. This draft lacks address information needed for that Google implementation. Passing JSON parsing does not establish business eligibility or search-feature eligibility.

## Local landing-page plan

Apply the mapping: home owns software-company/developer/digital-solution Coimbatore variants; the proposed web page owns website-developer intent; the proposed e-commerce page owns store-build intent. Explain actual requirements, discovery, communication and delivery. Do not create city clones, fabricated testimonials or location pages for offices that do not exist. Retain the broader India/global service story.

## Owner implementation checklist (recommendations only)

1. Confirm authentic business identity, customer-contact model and which contact channels may be public.
2. Find/verify the existing GBP if eligible; assess duplicate listings and the actual categories in the account.
3. Reconcile LinkedIn website and legacy email branding after approving the intended destination/contact. Do not remove a functioning channel blindly.
4. Publish useful web/e-commerce service pages before linking new citations to them.
5. Review a small set of relevant citations, not an indiscriminate “top ten” directory submission campaign.
6. If eligible and authorized, maintain genuine photos, accurate hours and a neutral review request process.
7. Validate real schema facts and rendered visibility before replacing the safe Organization graph.

Observed 18 November 2026 IST. Public-only local assessment; no profiles claimed, listings changed, reviews requested or external messages sent.
