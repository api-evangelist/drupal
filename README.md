# Drupal (drupal)
Drupal is an open-source content management system and web application framework used by millions of websites and applications worldwide. It provides a robust developer platform through multiple API layers including REST, JSON:API, and GraphQL, enabling headless and decoupled architectures for building flexible content-driven applications.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/drupal/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Content Management, CMS, REST, JSON:API, GraphQL, Headless, Web Services

## Timestamps

- **Created:** 2026-03-21
- **Modified:** 2026-03-21

## APIs

### Drupal REST API
The Drupal RESTful Web Services API is a core module that exposes Drupal entities and data as REST resources over HTTP. It supports multiple serialization formats and HTTP methods including GET, POST, PATCH, and DELETE, and is highly configurable in terms of which resources, formats, and authentication methods are enabled. Unlike the JSON:API module, it allows developers to define custom REST endpoints for non-entity data and complex business logic operations. Authentication can be handled via basic auth, cookie-based sessions, or OAuth2, and responses can be serialized as JSON, HAL+JSON, or XML depending on configuration.

**Human URL:** [https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module](https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module)


#### Tags:

 - REST, Content Management, CMS, Web Services

#### Properties

- [Documentation](https://www.drupal.org/docs/core-modules-and-themes/core-modules/restful-web-services-module)
- [OpenAPI](openapi/drupal-rest-api-openapi.yml)

### Drupal JSON:API
The Drupal JSON:API module is a core component that exposes all Drupal entity types and bundles as a standards-compliant JSON:API interface, requiring no configuration to enable. Each entity bundle receives a unique URL path following the pattern /jsonapi/{entity_type}/{bundle}, and the module supports GET, POST, PATCH, and DELETE operations for full CRUD access. It supports filtering, sorting, pagination, sparse fieldsets, includes for relationship resolution, translations, revisions, and file uploads out of the box. The JSON:API module is the recommended approach for most decoupled and headless Drupal applications due to its adherence to the open JSON:API specification and its compatibility with the broader JSON:API client ecosystem.

**Human URL:** [https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview)


#### Tags:

 - JSON:API, Content Management, CMS, REST, Headless

#### Properties

- [Documentation](https://www.drupal.org/docs/core-modules-and-themes/core-modules/jsonapi-module/api-overview)
- [OpenAPI](openapi/drupal-jsonapi-openapi.yml)
- [JSONSchema](json-schema/drupal-jsonapi-resource-schema.json)

### Drupal GraphQL API
The Drupal GraphQL module is a contributed module that enables developers to craft and expose a GraphQL schema for Drupal 10 and 11, allowing client applications to query Drupal content and entities using GraphQL syntax. It supports both queries and mutations for reading and writing data, and includes a built-in GraphiQL Explorer interface at /graphql/explorer for interactive schema browsing and query development. The schema is developer-defined and must be explicitly built, providing fine-grained control over what data is exposed and how it is shaped. It is commonly used in headless and decoupled Drupal architectures where frontend applications require flexible, efficient data access with minimal over-fetching.

**Human URL:** [https://www.drupal.org/docs/contributed-modules/graphql](https://www.drupal.org/docs/contributed-modules/graphql)


#### Tags:

 - GraphQL, Content Management, CMS, Headless, Query Language

#### Properties

- [Documentation](https://www.drupal.org/docs/contributed-modules/graphql)
- [Documentation](https://drupal-graphql.gitbook.io/graphql/)

## Common Properties

- [Portal](https://www.drupal.org/docs/develop)
- [Documentation](https://www.drupal.org/docs)
- [Website](https://www.drupal.org/)
- [PrivacyPolicy](https://www.drupal.org/privacy)
- [TermsOfService](https://www.drupal.org/terms)
- [Support](https://www.drupal.org/support)
- [Blog](https://www.drupal.org/planet)
- [Login](https://www.drupal.org/user/login)

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
