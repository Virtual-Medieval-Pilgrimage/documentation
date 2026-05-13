---
title: Editing a pilgrimage
layout: default
nav_order: 5
parent: Publishing Your Site
has_children: false
---
# Front Matter Fields
## Required fields
{: .subheadline}
Each entry in the collection requires the following fields in its YAML front matter:

- **layout** — The Jekyll layout template to use for this page. For pilgrimage entries, this should always be `pilgrimage`.
- **title** — The display title of the entry, in quotes. For example: `"Travel a Forested Path"`.
- **categories** — A list of descriptive tags for the entry. The first item is typically a geographic region and the second a time period: `[ East Asia, 9th century ]`.
- **mapurl** — A full Google Maps URL pointing to the modern location associated with the entry.
- **clue** — A short hint describing the physical location of the entry in the real world, in quotes.
- **shortdesc** — A short paragraph summary of the entry. Use the `>` block scalar so that line breaks in the file are treated as spaces.
- **lat** and **long** — The latitude and longitude of the modern location, in quotes, matching the coordinates in `mapurl`.
- **creationdate** — The date the entry was created, in `YYYY-MM-DD` format.

## Medieval parallel fields
{: .subheadline}
These fields describe the historical parallel that the entry draws on:

- **medievalparalleltitle** — The name of the medieval pilgrimage or parallel being described. For example: `"Shikoku Henro"`.
- **medievalmapurl** — A full Google Maps URL pointing to a key location associated with the medieval parallel.
- **medievalparallel** — A multi-paragraph description of the medieval parallel. Use the `|` block scalar to preserve line breaks. Markdown formatting (links, italics, lists) is supported.
- **learnmore** — A list of further reading suggestions or course recommendations related to the entry, using the `|` block scalar. Markdown list formatting is supported.
- **medievallat** and **medievallong** — The latitude and longitude of the primary medieval location. These are unquoted decimal values, unlike `lat` and `long`.

## Attribution fields
{: .subheadline}
These fields credit the people and images associated with the entry:

- **entryauthor** — A nested field with two subfields:
  - **name** — The full name of the entry's author, in quotes.
  - **affiliation** — The author's department and institution, in quotes.
- **img** — A nested field with three subfields:
  - **file** — The filename of the entry's primary image, located in the site's images folder. No quotes required.
  - **credit** — A full image credit, using the `|` block scalar. May include a source URL.
  - **source** — A direct URL to the image's source page, used to link the credit.
