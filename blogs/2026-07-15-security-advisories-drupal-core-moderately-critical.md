---
title: "Security advisories: Drupal core - Moderately critical - Information disclosure - SA-CORE-2026-010"
url: "https://www.drupal.org/sa-core-2026-010"
date: "2026-07-15"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Project: Drupal core Date: 2026-July-15 Security risk: Moderately critical 10 ∕ 25 AC:Complex/A:None/CI:Some/II:None/E:Theoretical/TD:Uncommon Vulnerability: Information disclosure Affected versions: =11.3.0 =11.4.0 CVE IDs: CVE-2026-15916 Description: The Image module allows you to define and configure image fields. The module doesn't sufficiently check access to image style derivatives when those files are served via a file stream other than private:// . This vulnerability is mitigated by the fact that Drupal must be configured to use a contributed (non-core) file scheme to serve private der
