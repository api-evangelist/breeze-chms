# Breeze ChMS (breeze-chms)

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

Breeze ChMS is church management software ([breezechms.com](https://www.breezechms.com)) for small and mid-sized churches, covering people and membership, tags and groups, events and calendars, check-ins and attendance, online and text giving, funds, pledge campaigns, custom forms, and volunteer scheduling. Breeze publishes a documented REST API scoped to each church subdomain (`https://{subdomain}.breezechms.com/api`), authenticated with an account API key sent in the `Api-Key` HTTP header. Every API operation is an HTTP `GET` request with query-string parameters, and the API is rate limited to roughly 20 requests per minute (wait about 3.5 seconds between calls). The API key is generated by the Account Owner under **Manage Account > API Key**.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/breeze-chms/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/breeze-chms/refs/heads/main/apis.yml)

## Tags

- Church Management
- ChMS
- Nonprofit
- Giving
- Membership
- Events
- Faith

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Authentication

- **Header:** `Api-Key: {your_api_key}`
- **Base URL:** `https://{subdomain}.breezechms.com/api`
- **Key location:** Manage Account > API Key (Account Owner)
- **Rate limit:** ~20 requests/minute; wait ~3.5s between calls

## APIs

### Breeze People API

List, retrieve, add, update, and delete people (members and contacts), read and write custom profile fields, and manage families. Supports paging, detailed field expansion, and filtering via `filter_json`.

- **Human URL:** [https://app.breezechms.com/api#people](https://app.breezechms.com/api#people)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- People
- Members
- Contacts

#### Properties

- [Documentation](https://support.breezechms.com/hc/en-us/articles/360001324153-API-Advanced-Custom-Development)
- [API Reference](https://app.breezechms.com/api#people)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Tags API

List tags and tag folders, create and delete tags and folders, and assign or unassign tags to people to build groups and segments.

- **Human URL:** [https://app.breezechms.com/api#tags](https://app.breezechms.com/api#tags)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Tags
- Groups
- Segmentation

#### Properties

- [API Reference](https://app.breezechms.com/api#tags)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Events API

List events within a date range, retrieve a single event instance (with schedule expansion), list calendars and locations, and add or delete events on the church calendar.

- **Human URL:** [https://app.breezechms.com/api#events](https://app.breezechms.com/api#events)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Events
- Calendars
- Scheduling

#### Properties

- [API Reference](https://app.breezechms.com/api#events)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Check-Ins and Attendance API

Record check-in / check-out attendance for people against an event instance, delete attendance, list who attended, and list who is eligible to check in to a given event.

- **Human URL:** [https://app.breezechms.com/api#attendance](https://app.breezechms.com/api#attendance)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Check-Ins
- Attendance
- Eligibility

#### Properties

- [API Reference](https://app.breezechms.com/api#attendance)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Giving and Contributions API

List, add, edit, and delete contributions (giving records), including splitting a single contribution across multiple funds, associating a payment, and matching gifts to a person and payment method.

- **Human URL:** [https://app.breezechms.com/api#giving](https://app.breezechms.com/api#giving)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Giving
- Contributions
- Donations

#### Properties

- [API Reference](https://app.breezechms.com/api#giving)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Funds API

List the contribution funds configured for the church, used to designate and report on giving (for example General Fund, Missions, Building).

- **Human URL:** [https://app.breezechms.com/api#funds](https://app.breezechms.com/api#funds)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Funds
- Giving
- Accounting

#### Properties

- [API Reference](https://app.breezechms.com/api#funds)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Pledges API

List pledge campaigns and the individual pledges within a campaign, which record who committed to give what over a date range against specified funds.

- **Human URL:** [https://app.breezechms.com/api#pledges](https://app.breezechms.com/api#pledges)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Pledges
- Campaigns
- Giving

#### Properties

- [API Reference](https://app.breezechms.com/api#pledges)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Forms API

List forms, list a form's fields, list submitted form entries (with detail expansion), and remove a form entry.

- **Human URL:** [https://app.breezechms.com/api#forms](https://app.breezechms.com/api#forms)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Forms
- Submissions
- Data Capture

#### Properties

- [API Reference](https://app.breezechms.com/api#forms)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Volunteers API

List, add, remove, and update volunteers on an event instance, and manage the volunteer roles (list, add, remove) available for scheduling.

- **Human URL:** [https://app.breezechms.com/api#volunteers](https://app.breezechms.com/api#volunteers)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Volunteers
- Roles
- Serving

#### Properties

- [API Reference](https://app.breezechms.com/api#volunteers)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Breeze Account API

Retrieve an account summary and read the account activity log, filtered by action, user, and date range, for auditing and administration.

- **Human URL:** [https://app.breezechms.com/api#account](https://app.breezechms.com/api#account)
- **Base URL:** `https://{subdomain}.breezechms.com/api`

#### Tags

- Account
- Audit Log
- Administration

#### Properties

- [API Reference](https://app.breezechms.com/api#account)
- [OpenAPI](openapi/breeze-chms-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/breeze-chms.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/breeze-chms.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/breeze-chms)
- [Website](https://www.breezechms.com)
- [Documentation](https://app.breezechms.com/api)
- [Plans](plans/breeze-chms-plans-pricing.yml)
- [Rate Limits](rate-limits/breeze-chms-rate-limits.yml)
- [Fin Ops](finops/breeze-chms-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
