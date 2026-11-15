# Dependencies and data sources

## Browser libraries

- **GeoTIFF.js 2.1.3** — imported dynamically from `https://cdn.jsdelivr.net/npm/geotiff@2.1.3/dist-module/geotiff.js` only when a user uploads a GeoTIFF DEM. It is not vendored in this repository; the optional import needs an internet connection.
- **No CSS framework or other third-party JavaScript library** is loaded. The interface uses browser-native HTML, CSS, Canvas 2D, Fetch, File, and Blob APIs.

## Online data services

- **NASA Mars Trek tiles** — CTX, HiRISE, and THEMIS daytime IR map imagery. Tile base URL: `https://trek.nasa.gov/tiles/Mars/EQ/`. The app requests imagery dynamically; these tiles are not stored in the repository.
- **NASA PDS Orbital Data Explorer (ODE) REST API** — `https://oderest.rsl.wustl.edu/live2/`. Used to search for THEMIS IRPBT and CRISM MTRDR/MRDR4 products and retrieve product thumbnails. Search results need an internet connection.
- **USGS Astrogeology / Fred Calef (2021), Mars 2020 Science Investigation CTX DEM Mosaic** — Jezero terrain values are embedded in the HTML as a 1,485 × 1,689-cell grid at 60 m spacing. The app also links to the original 20 m/pixel GeoTIFF (about 87 MB), which is not bundled separately:
  - Product metadata: `https://astrogeology.usgs.gov/search/map/mars_2020_science_investigation_ctx_dem_mosaic`
  - Source GeoTIFF: `https://planetarymaps.usgs.gov/mosaic/mars2020_trn/CTX/ScienceInvestigationMaps_JPL/M20_JezeroCrater_CTXDEM_20m.tif`

The app's route calculations use the CTX elevation and derived slope. THEMIS and CRISM products are shown for archive discovery and are not inputs to route computation. The source HTML includes additional CRS, resolution, and attribution details.

## Secrets and licensing

No API key or secret is embedded. The HTML does not declare a license for the application code. The embedded USGS-derived data is public domain; credit Fred Calef and the product authors. Keep attribution and the service providers' terms when redistributing or publishing.
