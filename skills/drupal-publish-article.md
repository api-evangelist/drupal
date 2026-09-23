---
name: drupal-publish-article
description: Create, review and publish an article node on a Drupal site over JSON:API, including the UUID and media-type rules that trip up most first integrations.
api: drupal:drupal-node-articles-api
operations: [listNodeArticles, createNodeArticle, getNodeArticle, updateNodeArticle]
generated: '2026-09-17'
method: generated
source: openapi/drupal-node-articles-api-openapi.yml, conventions/drupal-conventions.yml
---

# Publish an article on a Drupal site

Drupal is self-hosted. Everything below runs against `https://{site}/jsonapi` — the operator's own
domain. There is no shared host.

## Before you start

- Send **and** accept `application/vnd.api+json`. A plain `application/json` request is rejected.
- Authenticate with an OAuth 2.0 Bearer token (`simple_oauth`), HTTP Basic, or a session cookie.
  See `authentication/drupal-authentication.yml`.
- The account needs `create article content` and, to publish, `administer nodes` or the matching
  content-moderation permission.

## Steps

1. **Check what already exists** — `listNodeArticles` (`GET /node/article`).
   Filter rather than paging through everything: `filter[title]=<title>`.
   Reduce the payload with `fields[node--article]=title,status,created`.

2. **Create the article** — `createNodeArticle` (`POST /node/article`).
   The body is a JSON:API document: `{"data": {"type": "node--article", "attributes": {"title": ..., "body": {"value": ..., "format": "basic_html"}}}}`.
   `format` must be a text format the authenticated user is allowed to use; `basic_html` and
   `full_html` are the core defaults and `full_html` is usually restricted.
   **There is no idempotency key.** If this call times out, do NOT blindly retry — run step 1 first
   and check whether the node was created, or you will publish it twice.

3. **Read it back** — `getNodeArticle` (`GET /node/article/{uuid}`).
   Use the `data.id` UUID returned by step 2. Do **not** use `drupal_internal__nid`; that integer
   belongs to the legacy REST surface, not to JSON:API paths.

4. **Publish or unpublish** — `updateNodeArticle` (`PATCH /node/article/{uuid}`).
   Set `attributes.status` to `true` to publish, `false` to unpublish. The PATCH body must repeat
   `"type": "node--article"` and `"id": "<uuid>"` alongside the changed attributes.

## Errors

| Status | What it means here | What to do |
|---|---|---|
| 401 | No or expired token | Re-issue the Bearer token and retry |
| 403 | The role lacks the content permission, or the text format is not permitted | Fix the permission or use `basic_html`; do not retry unchanged |
| 404 | The `article` bundle does not exist on this site, or the UUID is wrong | Confirm the bundle name — it is site-defined |
| 422 | Entity validation failed | Read `errors[].source.pointer`; it is a JSON Pointer to the offending attribute |

Errors arrive as a JSON:API `errors[]` array, not RFC 9457 Problem Details.
See `errors/drupal-problem-types.yml`.

## Do not

- Do not `deleteNodeArticle` to undo a mistaken publish. Deletion is permanent in Drupal core and
  there is no restore operation. Unpublish with step 4 instead.
