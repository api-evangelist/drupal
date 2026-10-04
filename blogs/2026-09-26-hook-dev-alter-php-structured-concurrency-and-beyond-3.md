---
title: "HOOK_DEV_ALTER(): PHP Structured Concurrency and Beyond (3): structured state, and why its absence breaks concurrency"
url: "https://www.hook-dev-alter.com/en/articles/php-structured-concurrency-and-beyond-3-structured-state-and-why-its-absence-breaks"
date: "2026-09-26"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Every framework service that holds state is a bug under fibers. The current fix is to switch concurrency off. There is a third option.
