# Sea Cadets — UK Units Map (GitHub Pages)

This site builds an up-to-date map of **all UK Sea Cadet units** directly in your browser and lets you export a **PNG** image and a **CSV** dataset.

- **Live directory**: [Sea Cadets Unit Finder](https://www.sea-cadets.org/units)  
- **Geocoding**: [Postcodes.io bulk geocoding (no key)](https://postcodes.io/docs/overview/)

## How to use
1. Open the site.
2. Click **Build map** (1–2 minutes, uses bulk geocoding).
3. Click **Export PNG** (map with OpenStreetMap basemap) or **Download CSV**.

> Overseas entries (e.g., Bermuda) are excluded after geocoding by country.

## How it works
- Fetches the Unit Finder page as plain text via a CORS-permissive proxy (r.jina.ai).
- Parses units & UK postcodes with regex.
- Bulk-geocodes postcodes via `POST /postcodes`.
- Plots markers with Leaflet + MarkerCluster; exports the map with leaflet-image.
