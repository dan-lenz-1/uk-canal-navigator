UK CANAL NAVIGATOR V3.3

WHY V3.2 GPS/POIs FAILED ON ANDROID
The screenshot shows the app being opened from:
  content://com.google.android.apps.nbu.files.provider/...
That is Android's Files content provider, not a normal HTTPS web origin.

The CRT ArcGIS endpoint happens to load from that environment, but browser geolocation
permission and cross-origin POI queries are not reliable from a content:// page.

V3.3 IS BUILT FOR HTTPS / PWA USE
Files:
  index.html
  manifest.webmanifest
  sw.js

Once hosted on HTTPS:
- Live GPS can request normal site location permission.
- OpenStreetMap/Overpass POIs can be queried normally.
- Chrome can install the site to the Android home screen as a PWA.
- Pinch/pan map behavior remains unchanged.

QUICK TEST
Deploy this folder to any static HTTPS host:
- GitHub Pages
- Cloudflare Pages
- Netlify
- Vercel

No build process is required.

POI TEST
1. Open the HTTPS site.
2. Use Jump to test location -> Braunston.
3. Zoom 13+.
4. POIs should load automatically.
5. Tap Refresh nearby POIs if needed.

GPS TEST
1. Tap Start live GPS.
2. Allow location permission.
3. A blue position marker + accuracy circle should appear.
4. Keep "follow my location" enabled to centre while moving.

OTHER V3.3 CHANGES
- Checkbox controls are now left-aligned, full-width touch rows.
- POI radius adapts to zoom.
- POIs auto-load from zoom 13.
- Local-file/content:// mode is explicitly detected and explained.
