# drupal (drupal)

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

Drupal is an open-source content management system written in PHP and used to build websites, applications, and digital experiences for individuals, organizations, and enterprises worldwide.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/drupal/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/drupal/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-05-19

## APIs

### Drupal REST API

The Drupal RESTful Web Services API is a core module that exposes Drupal entities and data as REST resources over HTTP. It supports multiple serialization formats and HTTP methods including GET, POST, PATCH, and DELETE, and is highly configurable in terms of which resources, formats, and authentication methods are enabled. Unlike the JSON:API module, it allows developers to define custom REST endpoints for non-entity data and complex business logic operations.

- **Human URL:** [https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module](https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module)
- **Base URL:** `https://example.com`

#### Tags

- CMS
- Content Management
- REST
- Web Services

#### Properties

- [Documentation](https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module)
- [OpenAPI](openapi/drupal-rest-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/drupal-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/drupal-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Drupal JSON:API

The Drupal JSON:API module is a core component that exposes all Drupal entity types and bundles as a standards-compliant JSON:API interface, requiring no configuration to enable. Each entity bundle receives a unique URL path following the pattern /jsonapi/{entity_type}/{bundle}, and the module supports GET, POST, PATCH, and DELETE operations for full CRUD access.

- **Human URL:** [https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview)
- **Base URL:** `https://example.com/jsonapi`

#### Tags

- CMS
- Content Management
- Headless
- JSON:API
- REST

#### Properties

- [Documentation](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview)
- [OpenAPI](openapi/drupal-jsonapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/drupal-jsonapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/drupal-jsonapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/drupal-jsonapi-resource-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Drupal GraphQL API

The Drupal GraphQL module is a contributed module that enables developers to craft and expose a GraphQL schema for Drupal 10 and 11, allowing client applications to query Drupal content and entities using GraphQL syntax. It supports both queries and mutations for reading and writing data, and includes a built-in GraphiQL Explorer interface at /graphql/explorer for interactive schema browsing and query development.

- **Human URL:** [https://www.drupal.org/docs/contributed-modules/graphql](https://www.drupal.org/docs/contributed-modules/graphql)
- **Base URL:** `https://example.com/graphql`

#### Tags

- CMS
- Content Management
- GraphQL
- Headless
- Query Language

#### Properties

- [Documentation](https://www.drupal.org/docs/contributed-modules/graphql)
- [Documentation](https://drupal-graphql.gitbook.io/graphql/)
- [Postman Collection](collections/drupal-jsonapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/drupal-jsonapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/drupal-rest-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/drupal-rest-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/drupal)
- [LinkedIn](https://www.linkedin.com/company/drupal-project)
- [JSON-LD](json-ld/drupal-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [JSON Schema](json-schema/drupal-node-schema.json) — [JSON Schema](https://json-schema.org/specification)
