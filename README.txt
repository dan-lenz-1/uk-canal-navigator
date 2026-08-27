UK Canal Navigator V4.2

POI reliability fix:
- Food, shops, laundry and attractions are no longer bundled into one large amenity query.
- Each category is requested and rendered independently.
- A pub query failure cannot remove shops, locks or marinas.
- Existing cached category markers are used if a refresh fails.
- Food and shops now load from zoom 10.
- Laundry loads from zoom 11.
- Attractions load from zoom 12 when enabled.
- Navigation-critical POIs still load first.
- V4.1 emoji markers and V4.0 lock deduplication/status behaviour are retained.
- Diagnostics now test/render each amenity category separately.
