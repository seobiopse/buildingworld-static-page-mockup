# BuildingWorld static page mockups

HTML mockups and a dev handover for BuildingWorld category and price pages (in-house). One base template, two page types.

## Start here
- `index.html` links to everything.
- `handover/release-note.html` a one-page dev note: what to build, the mockups, the rules, the open decisions.
- `handover/dev-handover.html` one sheet: the mockup URLs on top, then every page from the top-level category pages to the price pages and how they link.
- `handover/content-template.html` Google Docs style content templates with copy buttons.

## Folders
- `mockups/` working HTML pages. Tick the box at the bottom right to show data tokens.
  - Category page: `ac-category-page.html`
  - Price page: `ac-price-page.html`
  - Price range page: `ac-price-range-page.html`
  - Price capacity page: `ac-price-capacity-page.html`
  - Price type page: `ac-price-type-page.html`
  - Price hub, one switcher on all three: `price-hub-page.html` (Pan-India Prices), `price-hub-city-page.html` (In My City), `price-hub-brand-page.html` (Brand Prices)
- `docs/` URL structure and the Slack message for dev.

## Notes
- AC data was read from the live listing on 2026-11-21.
- The dev toggle panel in each mockup is for review only and is removed before shipping.
