---
title: "Stuart Clark (Deciphered): JSON:API Views 8.x-1.2"
url: "https://stuar.tc/writing/jsonapi-views-120-20260812"
date: "2026-08-12"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
JSON:API on its own gets you decoupled entities: fetch a node, fetch a set of IDs, done. It doesn't get you the filtering, sorting and pagination that most real content listings actually need - a list of articles by tag, a paginated product catalogue, an events calendar with a date filter. You either reimplement that logic on the frontend, or Drupal ships a hand-written custom resource for every list on the site.
