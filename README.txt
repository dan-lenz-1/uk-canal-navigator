UK Canal Navigator V3.5

Changes from V3.4
- Fixed POI regression: locks no longer depend on a removed locksToggle.
- POIs load from zoom level 9 rather than 13.
- Search radius scales with zoom:
  z9  ~12 km
  z10 ~9.5 km
  z11 ~7.5 km
  z12 ~6 km
  z13 ~4.5 km
  z14 ~3.2 km
  z15 ~2.4 km
  z16+ ~1.6 km
- POI refresh debounce reduced from 800 ms to 250 ms.
- POI responses cached for 45 seconds by map area/layer selection.
- Existing POIs remain visible if a refresh fails.
- GPS requests an immediate fix, then starts a high-accuracy watch.
- Locks are a permanent layer:
  black = normal/unmatched
  red X = closed
  yellow ? = restricted
- Lock status is currently inferred from the waterway-level notice snapshot. Exact CRT lock/notice matching is still required for authoritative lock-by-lock status.
- New service worker version forces quicker update from V3.4.

Deploy all three web files (index.html, manifest.webmanifest, sw.js) over the V3.4 GitHub Pages version.
