---
name: drupal-tag-content
description: Classify Drupal content with taxonomy terms — discover the vocabulary, find or create the term, and attach it to a node without duplicating terms.
api: drupal:drupal-taxonomy-terms-api
operations: [getTaxonomyVocabulary, listTaxonomyTerms, getTaxonomyTerm, createTaxonomyTerm, updateNodeArticle]
generated: '2026-09-17'
method: generated
source: openapi/drupal-taxonomy-terms-api-openapi.yml, openapi/drupal-taxonomy-vocabularies-api-openapi.yml, data-model/drupal-data-model.yml
---

# Tag Drupal content

Taxonomy on a Drupal site is two entities: a **vocabulary** (the container, a config entity) and
**terms** (the content inside it). A node references terms through a site-defined entity-reference
field — commonly `field_tags` on the default `article` bundle, but never assume it.

## Steps

1. **Confirm the vocabulary exists** — `getTaxonomyVocabulary`
   (`GET /taxonomy/vocabulary/{id}`). Vocabularies are **config entities and read-only over
   JSON:API**. If the vocabulary you need is absent, an administrator must create it; you cannot.

2. **Look for the term before creating one** — `listTaxonomyTerms`
   (`GET /taxonomy_term/{vocabulary}`) with `filter[name]=<term>`.
   Skipping this is how sites end up with three terms called "Food" that are not the same term.

3. **If it is missing, create it** — `createTaxonomyTerm` (`POST /taxonomy/term`) with
   `{"data": {"type": "taxonomy_term--<vocabulary>", "attributes": {"name": "<term>"}}}`.
   No idempotency key exists — if this times out, re-run step 2 rather than retrying the POST.
   For a hierarchical vocabulary set `relationships.parent` to the parent term's UUID.

4. **Read the term back** — `getTaxonomyTerm` — and keep `data.id` (the UUID).

5. **Attach it to the node** — `updateNodeArticle` (`PATCH /node/article/{uuid}`) with a
   relationships block:
   `{"data": {"type": "node--article", "id": "<node-uuid>", "relationships": {"field_tags": {"data": [{"type": "taxonomy_term--tags", "id": "<term-uuid>"}]}}}}`.
   **A relationship PATCH replaces the whole array.** Read the node's current `field_tags` first
   and send the existing terms plus the new one, or you will silently untag the content.

## Verifying

Fetch the node with `include=field_tags` to get the attached terms inline in the `included[]` array
instead of making a second round trip per term.

## Errors

`403` on step 3 usually means the role lacks `administer taxonomy` or `create terms in <vocabulary>`.
`422` on step 5 means the field does not exist on that bundle, or the referenced UUID is not a term
of an allowed vocabulary — read `errors[].source.pointer`.
