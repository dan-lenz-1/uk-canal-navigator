UK Canal Navigator V3.7

ROOT CAUSE FIXED
V3.6's generated file referenced progressive POI helper functions that were missing from the final JavaScript.
That meant POI loading could stop before an Overpass request was ever sent.

V3.7:
- Replaces the entire POI loader with a self-contained implementation.
- Adds visible POI diagnostics:
  * current zoom
  * map centre
  * search radius
  * category/group
  * endpoint hostname
  * request time
  * element count
  * HTTP / timeout / network errors
- “Run diagnostic” tests each active category manually.
- Uses POST to Overpass with 3 fallback endpoints.
- Loads navigation POIs from zoom 9.
- Adds food at zoom 11, shops at 12, laundries at 13, attractions at 14.
- Keeps successful/cached groups even if another category fails.
- 60-second per-area/category cache.
- First GPS fix triggers a POI refresh immediately.
- Locks remain permanently visible:
  black = normal/unmatched
  red X = closed
  yellow ? = restricted

DEPLOY
Replace index.html, manifest.webmanifest and sw.js on GitHub Pages.
After deployment, confirm the header says V3.7.
If POIs still fail, expand “POI diagnostics” and tap “Run diagnostic”; the visible log will identify the endpoint/CORS/timeout issue.
