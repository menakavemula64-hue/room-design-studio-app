# Room Design Studio App

An installable web app for previewing room photos, styles, and accent colors. It is a separate copy of the Room Design Studio website.

## Features

- Choose a room type and preview its sample photo.
- Apply a visual filter and accent color.
- Upload a photo for a local preview.
- Install the app from a supported browser.
- Open the cached app shell while offline.

## How it works

The page markup, styles, and interaction code are in `index.html`. `manifest.webmanifest` provides the app name, display mode, and icons. `service-worker.js` caches the app shell so it can open without a network connection after the first visit.

## Run locally

Service workers need HTTPS or localhost. From this folder, run:

```powershell
python -m http.server 8765
```

Then open `http://localhost:8765/` in your browser.

## Install on a phone

- Android: open the published HTTPS site in Chrome, then use **Install app** or **Add to Home screen**.
- iPhone: open the published HTTPS site in Safari, tap **Share**, then **Add to Home Screen**.

## Offline and privacy

The app shell is cached after the first visit. Sample room photos are hosted on Unsplash and require internet access. Uploaded photos are previewed in the browser and are not uploaded or shared. The current Save and Create buttons display messages but do not store designs.

Style options apply photo filters; they do not generate a 3D room or rearrange furniture.