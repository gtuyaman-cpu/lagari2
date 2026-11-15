# Lagari — Martian Map

An interactive Mars surface mission-planning interface focused on Jezero crater. It includes terrain visualization, UAV route planning, EVA planning, and discovery of THEMIS and CRISM orbital products. The map data layers include active DEM elevation, derived slope, and a clearly labeled modeled temperature estimate.

## Files

- index.html — GitHub Pages entry point.
- lagari-martian-9-en.html — the same standalone application under its original filename.
- DEPENDENCIES.md — third-party libraries, data services, and attribution notes.

There are no separate local image files, build steps, or package-manager dependencies. The optional GeoTIFF upload feature loads GeoTIFF.js from a CDN. Live map imagery and NASA PDS product results require an internet connection.

## Run

Open index.html in a modern browser. For reliable access to remote map tiles and product search, publish the repository root with GitHub Pages or serve it from localhost.

No API keys or backend service are required by the app.

## License

This repository does not yet declare a license for the application code. Add a LICENSE file with the license you choose before inviting reuse or contributions. The embedded USGS-derived terrain data is public domain; see DEPENDENCIES.md for its source and requested credit.