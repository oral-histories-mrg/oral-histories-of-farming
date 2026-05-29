---
title: Oral Histories
layout: base
date: 2025-09-30
homepage: TRUE
position: 1
summary: ""
thumbnail: assets/images/Goat.jpg
header-image: assets/images/students-chispas.jpg
header-title: Oral Histories
header-subtitle: Oral history transcripts and audio are permanently preserved in the <a href = "https://digitalrepository.unm.edu/oralhistoriesoffarming/">Oral Histories of Farming along the Middle Rio Grande Collection</a> in the UNM Digital Repository.
header-height: 45vh
header-position: center center
header-zoom: cover
header-tier: section
---

<h1 class="sr-only">Oral Histories</h1>

{% assign farmer_pages = site.pages | where_exp: "p", "p.path contains 'farmer-profiles/'" | where_exp: "p", "p.path != 'farmer-profiles/index.md'" %}

{% include nav/oral-history-list.html histories=farmer_pages %}
