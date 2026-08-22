# Podia (podia)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Podia is an all-in-one creator platform for selling online courses, digital downloads, coaching, webinars, and memberships, paired with a website builder, blog, communities, and built-in email marketing. As of June 2026, Podia rebuilt itself around community as the core experience, and reports 15,000+ creators on the platform.

## Access Model: No Public API

**Podia does not offer a public or partner developer API, and it does not expose webhooks.** This is stated plainly in Podia's own help center: *"Podia does not offer a public API or webhooks."* The help center recommends [Zapier](https://zapier.com/apps/podia/integrations) as the only supported way to integrate Podia with other tools, noting that *"while we don't have a public API at the moment, Zapier can often provide a workaround."*

Because there is no first-party API, this catalog entry contains **no OpenAPI, AsyncAPI, rate-limit, or FinOps artifacts** - there is no published base URL, authentication scheme, or API reference to describe. The APIs listed below are **modeled** (`endpointsModeled: true`): they represent the logical resources and events Podia surfaces through its Zapier app, not real REST endpoints.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/podia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/podia/refs/heads/main/apis.yml)

## Tags

- Creator Economy
- Online Courses
- Digital Products
- Memberships
- Email Marketing
- No Public API
- Zapier Only

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## Modeled APIs

These are logical surfaces derived from Podia's Zapier integration, not documented endpoints.

### Podia Products API (modeled)

Online courses, digital downloads, coaching, and webinars. Enrollment can be automated only through the Zapier "Sign Someone Up for a Product" action and the "Product Signed Up For" trigger (write actions require the Shaker plan).

### Podia Customers and Audience API (modeled)

Customers, email audience, and tags. Via Zapier, Podia can add someone to your audience and subscribe them for email, react to tag events, and add people to a product waitlist.

### Podia Community API (modeled)

Communities and membership plans. Zapier exposes "Someone Joins Community" and "Someone Leaves Community" triggers, plus actions to add or remove a community member.

### Podia Sales API (modeled)

Sales and orders. Zapier surfaces a "New Sale" trigger that fires when someone purchases a free or paid course or digital download - the only supported way to react to a transaction programmatically.

## Zapier Triggers and Actions

**Triggers:** New Sale, Someone Joins Community, Someone Leaves Community, Someone Gets Tagged, Someone Waitlists, Published Blog Post, Product Signed Up For.

**Actions (Shaker plan and above):** Sign someone up for a product, add a community member, remove a community member, subscribe someone to your audience, add someone to a product waitlist.

## Pricing

Podia removed its free plan and offers three paid tiers, each with a 30-day free trial. The monthly rate is lower when billed annually (shown first) and higher when billed month-to-month.

| Plan | Annual (per mo.) | Monthly | Transaction fee |
|------|------------------|---------|-----------------|
| Mover | $42 | $49 | 5% |
| Shaker | $84 | $99 | 0% |
| Earthquaker | $150 | $179 | 0% |

Podia has no API pricing, usage plans, or metering, because it does not sell or expose API access. See [plans/podia-plans-pricing.yml](plans/podia-plans-pricing.yml).

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/podiadotcom)
- [Website](https://www.podia.com)
- [Documentation - Does Podia have a public API or webhooks?](https://help.podia.com/en/articles/11371075-does-podia-have-a-public-api-or-webhooks)
- [Integrations (Zapier)](https://zapier.com/apps/podia/integrations)
- [Plans](plans/podia-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
