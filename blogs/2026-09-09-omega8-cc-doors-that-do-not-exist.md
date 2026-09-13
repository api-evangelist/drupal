---
title: "Omega8.cc: Doors That Do Not Exist"
url: "https://omega8.cc/blog/doors-that-do-not-exist"
date: "2026-09-09"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Read one night of a Drupal or Backdrop site's log and most of it had no business with that site: WordPress login probes on a site which never ran WordPress, fishing for secret files, a thousand pages nobody ever made, from about as many addresses, one request apiece. On an ordinary server each of them wakes PHP for a not-found page, until no worker is free and your real visitors see an error instead of the site. On a BOA server those shapes are refused inside the web server before PHP or the database are consulted, the connection closed for what is only ever abuse, a cheap static not-found whe
