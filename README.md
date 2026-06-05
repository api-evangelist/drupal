# drupal (drupal)

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
