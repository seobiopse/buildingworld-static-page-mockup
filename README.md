# BuildingWorld static page mockups

HTML mockups and a dev handover for BuildingWorld category and price pages (in-house). One base template. L1 categories stay in the application; L2 and L3 are static pages. Domain: https://www.buildingworld.ai

## Start here
- `index.html` links to everything.
- `handover/release-note.html` a one-page dev note: what to build, H1 formats, breadcrumbs, links, meta and social tags, structured data, publishing rule, open decisions.
- `handover/dev-handover.html` one sheet: the mockup URLs on top, then every page with its URL, H1, breadcrumb (with URLs) and schema types, how the pages link, and the dynamic meta, Open Graph and Twitter tags.
- `handover/content-template.html` Google Docs style content templates with copy buttons.
- `handover/structured-data-reference.html` schema types per page and the Idea page as the reference (a saved copy is in `handover/reference/`).

## Folders
- `mockups/` working HTML pages. Tick the box at the bottom right to show data tokens.
  - Category page: `ac-category-page.html`
  - Price pages: `ac-price-page.html`, `ac-price-range-page.html`, `ac-price-type-page.html`
  - Price hub (one page, three views by toggle): `price-hub-page.html`
- `docs/` URL structure and the Slack message for dev.

## Notes
- AC data was read from the live listing on 2026-11-21.
- The dev toggle panel in each mockup is for review only and is removed before shipping.
