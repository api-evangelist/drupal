---
title: "Penyaskito: Canvas Tips&Tricks: Declaring images in SDCs"
url: "http://penyaskito.com/articles/2026/07/18/canvas-tipstricks-declaring-images-sdcs"
date: "2026-07-18"
feed_url: "https://www.drupal.org/planet/rss.xml"
---
Canvas Tips&Tricks: Declaring images in SDCs I've read recently about making SDCs dependent on Drupal Canvas because of needing to reference Canvas in the definition of your prop, so the right media widget is used inside Canvas: image: $ref: json-schema-definitions://canvas.module/image type: object title: Image description: > Image of the singer examples: - src: 'micro.webp' alt: 'Nice picture of the singer' width: 200 height: 300 That was the case during the alphas. But was fixed long ago, even before the 1.0.0 release. See canvas#3515074 .
