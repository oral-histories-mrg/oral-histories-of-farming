---
title: Farmer Profiles
layout: base
date: 2025-09-30
homepage: TRUE
position: 2
summary: ""
thumbnail: assets/images/casa-fresco-tomatoes.jpeg
---

<h1 class="sr-only">Farmer Profiles</h1>


{% assign cards = site.pages | where_exp: "p", "p.path contains 'farmer-profiles/'" | where_exp: "p", "p.path != 'farmer-profiles/index.md'" %}

{% include nav/farmer-records.html records=cards %}
