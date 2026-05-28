---
title: Contact Us
homepage: TRUE
layout: base
position: 1
summary: ""
thumbnail: assets/images/Plants.jpg
date: 2026-01-20
header-image: assets/images/Plants.jpg
header-title: Contact Us
header-subtitle: Questions about the project, interviews, archives, or student work.
header-height: 45vh
header-position: center center
header-zoom: cover
header-tier: section
---

<h1 class="sr-only">Contact Us</h1>

For questions about the project, interviews, archives, or student work, contact a member of the project team.


{% assign about_page = site.pages | where: "path", "about.md" | first %}
{% assign contacts = about_page.team-members | where: "contact", true %}

{% include nav/contact-list.html contacts=contacts %}
