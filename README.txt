UK Canal Navigator V3.6

Fixes the V3.5 POI refresh failures by replacing one large Overpass request with progressive category requests.

POI loading by zoom:
- Zoom 9-10: locks + marinas + navigation services only
- Zoom 11: adds pubs/restaurants/cafes
- Zoom 12: adds shops/supermarkets
- Zoom 13: adds laundries
- Zoom 14+: adds attractions when enabled

Other changes:
- Uses POST requests to Overpass instead of long GET URLs.
- Three Overpass endpoints used as fallbacks.
- Each query has a smaller output cap and shorter timeout.
- Individual category failures no longer kill the whole POI refresh.
- Existing/cached category markers remain if one service call fails.
- POI status pills show which categories loaded/failed.
- 60-second category cache reduces repeated calls while panning.
- Locks remain a permanent layer:
  black = normal/unmatched
  red X = closed
  yellow ? = restricted
- GPS fast-fix behavior from V3.5 retained.

Deploy index.html, manifest.webmanifest and sw.js over V3.5 on GitHub Pages.
