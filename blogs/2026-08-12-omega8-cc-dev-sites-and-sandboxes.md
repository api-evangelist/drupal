---
title: "Omega8.cc: Dev Sites and Sandboxes"
url: "https://omega8.cc/blog/dev-sites-and-sandboxes"
date: "2026-08-12"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Every Drupal or Backdrop site sooner or later needs a safe copy to experiment on – plenty of us still build one by hand and live with the quiet fear that the copy touches production, and plenty more click a dev-environment button inside somebody else's walled garden. On a BOA server the whole workflow is delegated: one Ægir task clones the site from a fresh backup, and the copy arrives with the handbrake pulled – cron off, HTTPS off, files in its own store – then dev-prefixed names mark the copies as dev sites with their own larger limits, a dev alias flips PHP errors and caching into dev mode
