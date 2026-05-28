# Farming the Middle Rio Grande

An oral history project documenting the people growing food along the Middle Rio Grande — their practices, family histories, land relationships, market realities, and visions for more resilient local food systems.

**Live site:** [fwgibbs.github.io/oral-histories](https://fwgibbs.github.io/oral-histories/) *(update with actual URL)*

---

## About the Project

Interviews were conducted by students in **GEOG-589: Qualitative Methods** (Fall 2025). Web profiles were written and published by students in **SUST-364: Local Food Systems Practicum** (Spring 2026). Oral history recordings are archived in the [UNM Digital Repository](https://digitalrepository.unm.edu/).

The site is built on [Xanthan](https://xanthan-web.github.io/xanthan/), a Jekyll-based framework for digital scholarship.

---

## Adding a Farmer Profile

Each farmer gets a folder inside `farmer-profiles/`:

```
farmer-profiles/
  firstname-lastname/
    index.md        ← the profile page
    images/         ← photos for this profile
    audio/          ← audio clips for this profile
```

### Frontmatter fields

Copy this block to the top of a new `index.md` and fill it in:

```yaml
---
title: Farmer Name
farmer-name: Farmer Name
farmer-sort-name: Lastname, Firstname
farm: Farm Name
interviewer: Interviewer Name or Anonymous
webpage-authors:
    - Student One
    - Student Two
interview-date: 2025-11-01
webpage-date: 2026-05-01
repository-link: https://digitalrepository.unm.edu/...
webpage-class: SUST-364, Spring 2026
interview-class: GEOG-589, Fall 2025
layout: scrollstory
thumbnail: images/filename.jpg
thumbnail-position: center center
summary: One or two sentence description shown on the profiles index.
header-image: images/filename.jpg
header-position: center center
geo: [35.68, -106.10]
placename: New Mexico
tags:
    - sustainability
---
```

### Content components

Inside the page body, use these includes to add media and pull quotes:

```liquid
{% include images/figure.html class="right" width="45%"
   image-path="images/photo.jpg" caption="Caption text." %}

{% include typography/aside.html class="right"
   text="A pull quote from the farmer." %}

{% include media/audio.html src="audio/clip.mp3" %}
```

`class` can be `right`, `left`, or `center`. Blockquotes use standard Markdown (`>`).

---

## Site Pages

| File | Purpose |
|------|---------|
| `index.md` | Homepage |
| `oral-histories.md` | List of all farmer profiles |
| `farmer-profiles/index.md` | Full-width card grid of profiles |
| `about.md` | Project description and team |
| `contact.md` | Contact information |
| `map.md` | Geographic map of farm locations |
| `instructions.md` | Student editing guide (not in nav) |

---

## CSS Files

Stylesheets live in `assets/css/`. Every page loads the core set; individual pages can add more via `css: filename.css` in frontmatter.

| File | Purpose |
|------|---------|
| `base.css` | Variables, reset, layout, header images, footer |
| `typography.css` | Headings, body text, blockquotes, pullquotes |
| `nav.css` | Top navigation bar |
| `cards.css` | Farmer record cards, oral history list, contact list |
| `backgrounds.css` | Scrollstory background image components |
| `scrollstory.css` | Farmer profile page layout, figures, metadata card |
| `home.css` | Homepage and about page components, team list |
| `dark-energy.css` | Alternate dark theme (not loaded by default — instructional example) |
| `simple-theme.css` | Minimal theme override starter (instructional example) |

---

## Running Locally

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000/oral-histories/`.

Requires Ruby and Bundler. See the [Xanthan local preview guide](https://xanthan-web.github.io/xanthan/docs/getting-started/previewing-locally) for setup instructions.
