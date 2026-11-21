# BuildingWorld static page URL structure

Domain: `https://www.buildingworld.ai` (all URLs below are paths on it).
Source: live site (Chrome check, 2026-11-21) and `Brand & Price Finalized Version .xlsx`, `Static Price Pages - Review for Approval.xlsx`, `25 Product Static Pages.txt`.

## 1. Patterns

| Page type | Pattern | Status | Example |
|---|---|---|---|
| Home | `/` | live | |
| L1 category (app page) | `/products/categories/<l1-slug>` | live | `/products/categories/floors-and-walls` |
| L2 / L3 static category page | `/product/<l1-slug>/<category-slug>.html` | live for 25 pages, proposed for the rest | `/product/floors-and-walls/wall-tiles.html` |
| Product detail | `/products/<id>-<product-slug>` | live | `/products/lzko9l-thetileshouse-coventry-kitkat-brown-tile-12-x-24-inch` |
| Brand page | `/brands/<id>-<brand-slug>` | live | `/brands/f5atu4-kag` |
| National price page (76) | `/price/<slug>` | final, Dev Handover 2026-11-19 | `/price/floor-tile` |
| City price page (197) | `/price/<state-code>/<city>/<slug>` | final | `/price/mh/mumbai/cooler` |
| Brand price page (215) | `/price/<brand>/<slug>` | final | `/price/lg/ac` |
| Price range page (proposed) | `/price/<slug>-under-50`, `-50-to-100`, `-100-to-250`, `-above-250` | proposed; not in the 532 | `/price/floor-tile-under-50` |
| Brand + city price page (44) | `/price/<state-code>/<city>/<brand>/<slug>` | final | `/price/wb/kolkata/kutchina/chimney` |
| City + category page | `/<city>/<l1-slug>/<category-slug>.html` | proposed (used in mockup) | `/bangalore/floors-and-walls/wooden-floor-tiles.html` |
| Ideas | `/ideas/categories/<slug>`, `/ideas/iconic-projects` | live | `/ideas/categories/residential` |

Ideas categories live: residential, landscape, commercial, hospitality, educational, healthcare, sports-fitness, culture-and-entertainment, industrial, transport.

## 2. Slug rules

- Lowercase, hyphens, no stop words removed, no trailing slash.
- Static category page: plural of the category name (`Wall Tile` -> `wall-tiles`). The 25 live pages use this.
- Price page slug = the target keyword without "price" (`floor tile price` -> `floor-tile`), as in the Dev Handover.
- One canonical URL per page. Self-referencing canonical on every static page. Filtered app URLs (`?l3_category_ids=...`) canonicalize to the clean static URL or are not linked.

## 3. Floors and Walls (L1) -> L2 -> L3 (from the live site)

L2 list (live sidebar): Floor Tile, Wall Tile, Floor and Wall Tile, Natural Stone, Wall Panel, Wall Cladding, Vinyl Flooring, Wooden Flooring, Internal Partition, Louver, Wall Accessories, Wall Protection, Deck Tiles, Floor Finishes, Gym and Sports Flooring, Floor and Deck Accessories, Wall Finishes, Secondary Floor System.

| Level | Name | Proposed static URL | Price page (finalized) |
|---|---|---|---|
| L2 | Floor Tile (2,369) | `/product/floors-and-walls/floor-tiles.html` | `/price/floor-tile` (PP-0057) |
| L3 | Wooden Floor Tile (442) | `/product/floors-and-walls/wooden-floor-tiles.html` | none yet |
| L3 | Vitrified Floor Tile (704) | `/product/floors-and-walls/vitrified-floor-tiles.html` | `/price/vitrified-tile` (PP-0056, workbook names it "Vitrified Tile") |
| L3 | Ceramic Floor Tile (392) | `/product/floors-and-walls/ceramic-floor-tiles.html` | `/price/tiles-per-square-feet` (PP-0052, "Ceramic Tile") |
| L3 | Outdoor Floor Tile (337) | `/product/floors-and-walls/outdoor-floor-tiles.html` | none yet |
| L3 | Marble Floor Tile (191) | `/product/floors-and-walls/marble-floor-tiles.html` | `/price/marble` (PP-0049) |
| L3 | Porcelain Floor Tile (159) | `/product/floors-and-walls/porcelain-floor-tiles.html` | none yet |
| L3 | Carpet / Terrazzo / Cement / Industrial Floor Tile (67 / 44 / 29 / 4) | `/product/floors-and-walls/<name>-floor-tiles.html` | none yet |
| L2 | Wall Tile | `/product/floors-and-walls/wall-tiles.html` (live) | `/price/wall-tiles` (PP-0083) |
| L2 | Wooden Flooring | `/product/floors-and-walls/wooden-flooring.html` | `/price/wooden-flooring` (PP-0088) |

## 4. Open items

- The 25 live static pages use names such as `vitrified-tiles.html` (no "floor"). Confirm whether the Floor Tile L3 pages follow `vitrified-floor-tiles.html` or the shorter live names, so two pages do not compete for the same keyword.
- Pages with 4 to 30 products (Industrial, Cement) need a minimum-product rule before they get a static page or `index`.
- Price pages: 532 in `Dev Handover - Price Pages-2026-11-19.xlsx` (76 national, 197 city, 215 brand, 44 brand + city), confirmed 2026-11-21. 13 slugs are marked "confirm".
