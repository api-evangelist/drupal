---
title: "Stuart Clark (Deciphered): Druxt Auth 0.5.0; two ways to sign in without leaving your site"
url: "https://stuar.tc/writing/druxt-auth-050-two-ways-to-sign-in-20260926?utm_source=planet-drupal&utm_medium=rss&utm_campaign=syndication"
date: "2026-09-26"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Every Druxt site I have built signs people in by sending them somewhere else to do it: out to Drupal's login page, on to a consent screen, and eventually back. With Druxt Auth 0.5.0 the username and password can now be handled entirely in the frontend instead, either through the authorization code grant or through the password grant. If you have not used it, Druxt Auth wires Nuxt's auth module to Simple OAuth on the Drupal side.
