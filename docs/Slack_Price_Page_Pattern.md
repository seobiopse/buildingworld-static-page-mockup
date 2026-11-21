Hi team, price pages should be created from a URL pattern for any category, not from a fixed list. Please build the template once and generate pages from the data:

1. National: `https://www.buildingworld.ai/price/<slug>` e.g. `https://www.buildingworld.ai/price/floor-tile`
2. City: `https://www.buildingworld.ai/price/<state-code>/<city>/<slug>` e.g. `https://www.buildingworld.ai/price/mh/mumbai/floor-tile`
3. Brand: `https://www.buildingworld.ai/price/<brand>/<slug>` e.g. `https://www.buildingworld.ai/price/kag/floor-tile`
4. Brand + city: `https://www.buildingworld.ai/price/<state-code>/<city>/<brand>/<slug>` e.g. `https://www.buildingworld.ai/price/mh/mumbai/kag/floor-tile`

5. Price range (new, not in the 532 list): `https://www.buildingworld.ai/price/<slug>-under-50`, `-50-to-100`, `-100-to-250`, `-above-250` e.g. `https://www.buildingworld.ai/price/floor-tile-under-50`. Real pages, not `#` anchors (Google ignores fragments). Only for categories and ranges with enough products and search demand.

Slug = target keyword without "price". Category pages link to these by pattern (price range chips link to the range pages). Mockups: category page and `price-page.html` (purple tags show what is filled from data).

Please keep an eligibility check so thin combinations are not generated (min products and dealers, per the Dev Handover rules).
