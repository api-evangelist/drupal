---
title: "HOOK_DEV_ALTER(): PHP Structured Concurrency and Beyond (2): ownership, and why its absence breaks persistent servers"
url: "https://www.hook-dev-alter.com/en/articles/php-structured-concurrency-and-beyond-2-ownership-and-why-its-absence-breaks-persistent"
date: "2026-09-25"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
A coroutine nobody owns is a leak. Under one process per request you never see it. Persistent servers take that away.
