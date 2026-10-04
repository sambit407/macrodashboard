FILES
1. logistics.html
2. logistics-data.json

GITHUB PROCESS
1. In the same repository as index.html, choose Add file > Upload files.
2. Upload logistics.html and logistics-data.json to the repository root.
3. Commit changes.
4. Open https://YOUR-USERNAME.github.io/YOUR-REPO/logistics.html
5. Add a link to logistics.html from index.html if desired.

DATA PROCESS
- Update logistics-data.json without changing its keys.
- Labels are dates/periods/categories.
- series is an array of {"name":"Series name","values":[...]}.
- Keep every values array the same length as labels.
- Use numbers without commas or currency symbols.
- Set lastUpdated to the actual source/date, for example "2026-10-01 | IMF PortWatch and UNCTAD".
- Do not insert estimated or invented values.

SOURCE MAPPING
- freightIndex: Freightos FBX or Drewry WCI published series.
- freightLanes: Freightos route indices.
- portActivity: IMF PortWatch exported port calls and trade-volume estimates.
- portCongestion: OECD AIS dashboard or licensed port-intelligence export.
- routeShare: IMF PortWatch chokepoint data or Drewry Red Sea Diversion Tracker.
- carrierCapacity: licensed carrier-capacity source or an authorized internal report.
- portConnectivity: UNCTAD Port Liner Shipping Connectivity Index.
- dwellDistribution: your internal container-event dataset.

EXAMPLE STRUCTURE ONLY (do not copy as market data)
"portCongestion": {
  "ports": ["Port A", "Port B"],
  "waitingHours": [12.5, 8.2]
}
