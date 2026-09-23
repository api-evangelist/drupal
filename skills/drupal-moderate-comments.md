---
name: drupal-moderate-comments
description: Review, unpublish and remove comments on a Drupal site, with the permission and reversibility rules that decide which of those you should actually do.
api: drupal:drupal-comments-api
operations: [createComment, getComment, updateComment, deleteComment]
generated: '2026-09-17'
method: generated
source: openapi/drupal-comments-api-openapi.yml, conventions/drupal-conventions.yml, errors/drupal-problem-types.yml
---

# Moderate comments on a Drupal site

Comments in Drupal are entities in their own right, attached polymorphically to a host entity
(usually a node) through `entity_id`. They carry their own published status and their own
permissions, separate from the content they hang off.

## Reading a comment

`getComment` (`GET /comment/{id}`). The response carries `attributes.status` (published or not),
`attributes.subject`, `attributes.comment_body`, and relationships to `uid` (the author) and the
host entity.

## Unpublishing — the default moderation action

`updateComment` (`PATCH /comment/{id}`) with `attributes.status = false`.

This is the action to reach for. It removes the comment from public view, is fully reversible by
PATCHing `status` back to `true`, and preserves the author attribution and the thread structure so
replies underneath it do not become orphans.

## Deleting — only on explicit instruction

`deleteComment` (`DELETE /comment/{id}`) is permanent. Drupal core has no comment trash and no
restore operation. Deleting a comment in the middle of a thread also affects the replies beneath it.
Do not use deletion as a moderation reflex; unpublish instead, and escalate to a human for anything
that genuinely needs to be destroyed.

## Posting a comment

`createComment` (`POST /comment`) needs `relationships.entity_id` pointing at the host entity,
`relationships.field_name` naming the comment field on it, and `attributes.comment_body`.
Depending on the site's settings the comment may land unpublished pending approval — read
`attributes.status` on the response rather than assuming it went live.

There is no idempotency key on this endpoint. A retried POST posts the comment twice.

## Errors

| Status | Cause |
|---|---|
| 401 | Missing or expired credentials |
| 403 | The role lacks `administer comments` (for status changes) or `post comments` |
| 404 | The comment id does not exist, or comments are disabled on this site |
| 422 | Validation failed — a missing host entity, a disallowed text format, or spam filtering |
