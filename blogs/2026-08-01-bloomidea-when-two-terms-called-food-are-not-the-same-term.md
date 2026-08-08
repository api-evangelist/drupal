---
title: "BloomIdea: When two terms called Food are not the same term"
url: "https://bloomidea.com/en/blog/when-two-terms-called-food-are-not-same-term"
date: "2026-08-01"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
You have a supplier spreadsheet with a category column that reads Animals > Dogs > Food , and you want Drupal to end up with a real taxonomy tree: Animals , with a child Dogs , with a child Food , each level created only if it does not exist yet, and every product referencing the leaf of its own path. Neither Drupal core nor Feeds does that on its own. Feeds Tamper Term Hierarchy does: it reads the path out of the column, creates the taxonomy terms that do not already exist, and respects the hierarchy between them.
