# Sea Cadets — UK Units Map (GitHub Pages)

This one-page site builds an up-to-date map of **all UK Sea Cadet units** directly in the browser and lets you export a **PNG** image and a **CSV** dataset.

- **Live directory**: [Sea Cadets Unit Finder](https://www.sea-cadets.org/units)
- **Geocoding**: [Postcodes.io (bulk geocoding, no API key)](https://postcodes.io/docs/overview/)

## Data modes
1. **Live Fetch** (default): Pulls the Unit Finder page as plain text and parses units.
2. **Paste Mode**: Paste the Unit Finder page content (Ctrl+A, Ctrl+C → Ctrl+V), then Build.
3. **Local Fallback**: Small embedded sample so the page always renders something even without network access.

> Overseas entries (e.g., Bermuda) are excluded after geocoding by country.

## Usage
1. Open the GitHub Pages URL of this repo.
2. Choose the data mode (Live / Paste / Fallback).
3. Click **Build map** and wait for “Plotted N UK units”.
4. Click **Export PNG** (map with OpenStreetMap basemap) or **Download CSV**.
5. **Zoom UK** recentres the British Isles; **Clear** removes markers.

## GitHub Pages
- Enable in **Settings → Pages** → “Deploy from a branch”, Branch: `main`, Folder: `/root`.
- After ~1–3 minutes, your site will be live at `https://<user>.github.io/<repo>/`.

## Notes
- This page uses Leaflet + MarkerCluster and `leaflet-image` for PNG export.
- Bulk geocoding is performed in chunks to be polite to Postcodes.io.
