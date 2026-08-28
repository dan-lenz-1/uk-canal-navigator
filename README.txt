UK Canal Navigator V4.6

Route-planner corrections:
- Route overlay now follows a graph built from the CRT canal geometry already downloaded by the app.
- Start and end locations snap to the nearest CRT network node.
- Dijkstra shortest-path routing is used across canal linework.
- No 'as-the-crow-flies' fallback is drawn if the network cannot connect the selected locations.

Restriction scheduling:
- Restricted passages are time-window events along the route, not whole-day route cut-offs.
- Arrive before opening: wait until opening, then continue.
- Arrive during the allowed window: pass and continue cruising afterward if daily hours remain.
- Arrive too late to clear the restriction: moor before it and attempt passage on the next cruising day.
- Only a complete closure causes the through-route to be abandoned.
- If the selected number of days is insufficient, the planner reports remaining canal miles instead of treating a restriction as a closure.

V4.5 POI/winding-hole/rich-detail functionality is retained.
