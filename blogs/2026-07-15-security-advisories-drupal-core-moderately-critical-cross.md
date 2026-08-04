---
title: "Security advisories: Drupal core - Moderately critical - Cross-site scripting - SA-CORE-2026-012"
url: "https://www.drupal.org/sa-core-2026-012"
date: "2026-07-15"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Project: Drupal core Date: 2026-July-15 Security risk: Moderately critical 13 ∕ 25 AC:Basic/A:User/CI:Some/II:Some/E:Theoretical/TD:Default Vulnerability: Cross-site scripting Affected versions: =11.3.0 =11.4.0 CVE IDs: CVE-2026-55805 Description: The Layout Builder module doesn't sufficiently sanitize block labels in certain scenarios, which can lead to a cross-site scripting (XSS) vulnerability. This is mitigated by the fact that both the attacker and the targeted user need to be using the Layout Builder editing interface. Solution: Install the latest version: Drupal 11 If you use Drupal 11.
