UK Canal Navigator V4.0

Changes from V3.9:
- Physical lock deduplication: nearby OSM lock chamber / lock=yes / lock_gate records are clustered into ONE lock marker.
- 55 metre clustering threshold, with same name/ref records always merged.
- Prefers the lock/chamber feature as the representative record instead of a bare gate node.
- Locks inherit the nearest matched CRT waterway status unless the lock record has a stronger explicit status:
    black = normal/unmatched
    yellow ? = restricted/planned passage
    red X = closed
- Generic Grand Union status changed from planned/purple to restricted/yellow in the current snapshot.
- Navigation-critical POIs load first: locks, marinas, boating services.
- Food/shops/laundry/attractions load in a second request so navigation points appear sooner.
- Existing stable queued-refresh model from V3.9 retained.
- Diagnostic now renders the exact deduplicated lock results.

Note:
Lock status is still based on the current matched waterway snapshot + OSM lock tags. Authoritative lock-by-lock CRT notice association remains a future data connector.
