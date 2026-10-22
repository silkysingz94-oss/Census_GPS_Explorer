# GBoS GEOAI | Advanced Census & GPS Explorer

Interactive web dashboard for The Gambia featuring enumeration-area mapping, cascading LGA/district/ward filters, population and household indicators, settlement/district sex-ratio analysis, comparative charts, descriptive statistics, table search, exports, and optional browser GPS.

## Open the dashboard

- **GitHub repository:** https://github.com/silkysingz94-oss/Census_GPS_Explorer
- **Dashboard source:** https://github.com/silkysingz94-oss/Census_GPS_Explorer/blob/main/index.html
- **GitHub Pages (after enabling Pages):** https://silkysingz94-oss.github.io/Census_GPS_Explorer/

## Automatic data loading

The dashboard looks for these files in the repository root (same folder as `index.html`):

| File | Status | Purpose |
|---|---|---|
| `Settlement_Sex_Ratio.csv` | Included | Settlement-level male/female counts and sex-ratio analysis |
| `District_Sex_Ratio.csv` | Included | District-level male/female counts and sex-ratio analysis |
| `Census_EAs_Geo.json` | **Not yet published** | EA polygon map and EA-level population/household indicators |

The enumeration-area GeoJSON is a large file (about 15 MB) and has not been committed in this update. To enable automatic EA mapping, upload the authorised `Census_EAs_Geo.json` to the repository root. Keep the exact filename, including capitalization. Once it is added, the page's existing auto-loader will load it on refresh.

**Important:** only publish census/GPS/geospatial data that you are authorised to make public. Enumeration-area boundaries and attached attributes may be sensitive. If the dataset is not approved for public release, keep it private and use the dashboard's manual file-upload controls instead.

## Enable GitHub Pages

1. Open the repository's **Settings**.
2. Select **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Choose branch `main` and folder `/ (root)`, then save.
5. Wait for deployment and open the Pages URL above.

## Local use

Open `index.html` in a browser. For automatic relative-file loading, use GitHub Pages or a local web server (browsers may block `fetch()` from `file://`). Manual file upload is available in the dashboard. GPS requires a secure context (HTTPS or localhost) and explicit browser permission.

## Libraries and map sources

- [Leaflet](https://leafletjs.com/) for interactive mapping
- [Chart.js](https://www.chartjs.org/) for charts
- [PapaParse](https://www.papaparse.com/) for CSV parsing
- Basemap tiles from OpenStreetMap, CARTO, Esri, and OpenTopoMap, subject to their terms and attribution

## Credits

Produced by Ansu Singhateh — GIS Analyst | GIS / Cartography Unit | Gambia Bureau of Statistics (GBoS).

Research and educational use. Statistics are only as reliable as their source data, definitions, coverage, and reference dates. Do not compare totals across geographic levels without confirming that their coverage and definitions are compatible.
