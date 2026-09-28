# Room Design Studio App

An installable Progressive Web App (PWA) based on the Room Design Studio project.

**Live app:** [Open Room Design Studio](https://menakavemula64-hue.github.io/room-design-studio-app/)

## Features

- Choose a room type, photo style, and accent color.
- Upload a photo for a local room preview.
- Install the app from a supported mobile browser.
- Reopen the cached app shell offline after the first visit.

## How it works

- `index.html` contains the page, styles, room controls, and install button.
- `manifest.webmanifest` defines the app name, display mode, and icons.
- `service-worker.js` caches the main app files for offline use.
- `icon-192.png` and `icon-512.png` provide app icons.

The service worker is registered by the page with:

```js
navigator.serviceWorker.register("./service-worker.js");
```

## Run locally

Service workers need HTTPS or localhost. From this folder, run:

```powershell
python -m http.server 8765
```

Then open `http://localhost:8765/`.

## Install on a phone

- Android: open the live HTTPS link in Chrome and select **Install app** or **Add to Home screen**.
- iPhone: open the live HTTPS link in Safari, tap **Share**, then **Add to Home Screen**.

## Offline and privacy notes

The app shell is cached after the first visit. Sample Unsplash photos need an internet connection. Uploaded photos stay in the browser and are not shared. The Save and Create buttons currently show confirmation messages but do not store designs. Style options apply photo filters; they do not generate a 3D room.
