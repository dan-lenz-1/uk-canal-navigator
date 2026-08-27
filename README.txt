UK Canal Navigator V3.9

Rebased on V3.3 single-layer POI renderer.
Fixes the V3.7/V3.8 stuck poiBusy race condition.
- single persistent poiLayer
- queued refresh rather than request cancellation
- fast overpass-api.de first
- dynamic radius from zoom 9
- permanent black locks, red X closed, yellow ? restricted when OSM status tags support it
- rich POI details and marina amenity icons
- fast GPS
- route planner and marine services retained from V3.4
- manual diagnostic now renders the same returned POIs onto the map
