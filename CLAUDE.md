# CLAUDE.md

Guidance for working in this repository.

## Project

This is a [Hugo](https://gohugo.io/) static site for a hiking-guide business. The
active theme is `deliberate-pace` (under `themes/`). Build with `hugo` (output goes
to `public/`); preview with `hugo server`.

- Site content lives in `content/`.
- Field notes (trail reports) live in `content/field-notes/`, one Markdown file per
  hike, with front matter for `title`, `date`, `description`, `location`, `region`,
  `image`, `imageAlt`, and an optional `gallery` list (`src`, `caption`, `alt`).
- Images live in `themes/deliberate-pace/static/img/` and are referenced as `/img/...`.

## Field notes

- **Link trails to AllTrails.** When a field note names a specific trail, link it to
  that trail's page on [AllTrails](https://www.alltrails.com/).
- **Link parks and locations to their official websites.** When a field note names a
  park, forest, preserve, or similar location, link it to its official site (e.g. the
  NPS, US Forest Service, or state park page).
- **Links open in new tabs automatically.** Just write normal Markdown links. The
  `render-link.html` render hook adds `target="_blank" rel="noopener noreferrer"` to
  all external links, so you do not need to add this by hand.

## Images

- **Always remove location (GPS) and timestamps from images used on the site.** Before
  adding any photo, strip its EXIF metadata — at minimum GPS coordinates and date/time
  fields, and preferably all metadata. Resize large photos to a reasonable web size
  (long edge around 1600px) as well. Verify the saved image carries no EXIF afterward.
