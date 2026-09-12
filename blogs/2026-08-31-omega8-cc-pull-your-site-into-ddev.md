---
title: "Omega8.cc: Pull Your Site into DDEV"
url: "https://omega8.cc/blog/pull-your-site-into-ddev"
date: "2026-08-31"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Reproducing a bug that only happens on the live Drupal site used to mean a hand-made dump, the uploads copied across one rsync at a time, and an hour of persuading the copy it is not production. On a BOA-hosted site it is one pull into the DDEV project you already have: a small add-on reads what the site reports about itself, sets the local project to the same PHP and Drupal version and the same docroot, then brings the database and the uploads down through the ordinary limited shell account you already use for SFTP, with the key you already have, and nothing new switched on server-side. It sy
