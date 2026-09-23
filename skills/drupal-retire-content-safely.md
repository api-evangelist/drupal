---
name: drupal-retire-content-safely
description: Take Drupal content out of circulation without destroying it — the unpublish-first pattern, and what deletion actually costs on a Drupal site.
api: drupal:drupal-nodes-api
operations: [getNode, updateNode, deleteNode]
generated: '2026-09-17'
method: generated
source: openapi/drupal-nodes-api-openapi.yml, conventions/drupal-conventions.yml
---

# Retire Drupal content safely

This skill exists because of one property of the contract: **Drupal core ships no undo.**
`deleteNode` is immediate and permanent. There is no trash, no restore, no grace window, and no
reversal operationId anywhere in the spec. An agent that deletes on a Drupal site has destroyed
the content.

## The safe sequence

1. **Read the current state** — `getNode` (`GET /node/{id}`).
   Record `attributes.status` and `attributes.changed` so you can describe what you changed.

2. **Unpublish** — `updateNode` (`PATCH /node/{id}`) with `attributes.status = false`.
   The content disappears from anonymous view but every field, revision and relationship survives.
   This is reversible: PATCH `status` back to `true`.

3. **Stop.** Report the unpublish and let a human decide about deletion.

## Only if a human has explicitly asked for destruction

4. `deleteNode` (`DELETE /node/{id}`). Before calling it:
   - Confirm the UUID against step 1 — a wrong UUID deletes the wrong content, irrecoverably.
   - Confirm the site actually has revisions or backups. Neither is guaranteed and neither is
     exposed over this API.
   - Say plainly, in your own output, that the action cannot be reversed through the API.

## Why not rely on revisions

Drupal's revision system is real, but it is not an API reversal path. JSON:API can *read* a prior
revision through the `resourceVersion` query parameter; it cannot revert to one. Whether revisions
are created at all is a per-content-type setting an operator controls, so you cannot assume them.
Revisions also do not survive a node deletion.

## Related operations on other entity types

The same rule holds across the surface: `deleteNodeArticle`, `deleteComment`, `deleteFile`,
`deleteTaxonomyTerm` and `deleteUser` are all irreversible in core. Only nodes have a
publish/unpublish status field to fall back on; for comments, use `updateComment` to set the
comment unpublished rather than deleting it.
