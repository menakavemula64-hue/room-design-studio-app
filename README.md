# Room Design Studio: Website and App

This project has two versions of the room-design preview. They are separate projects with separate links.

## Project links

- **Original website:** [Open Room Design Studio](https://menakavemula64-hue.github.io/room-design-studio/). Use this version in a browser; it is the original website.
- **Installable app:** [Open Room Design Studio App](https://menakavemula64-hue.github.io/room-design-studio-app/). This is the separate PWA version. You can install it from a supported phone browser and reopen its cached app shell offline after the first visit.

## What the app does

- Choose a room type and see its sample photo.
- Apply a visual style filter and accent color.
- Upload a photo for a preview that stays in your browser.
- Install the app on a phone.

## How the app works

The room page, styles, and JavaScript are in `index.html`. `manifest.webmanifest` describes the app name, icons, and standalone display mode. `service-worker.js` caches the app shell for offline use. The page registers it like this:

```js
navigator.serviceWorker.register("./service-worker.js");
```

## Run locally

Service workers require HTTPS or localhost. In this folder, run:

```powershell
python -m http.server 8765
```

Then open `http://localhost:8765/`.

## Install on a phone

- **Android:** open the installable app link in Chrome, then choose **Install app** or **Add to Home screen**.
- **iPhone:** open the installable app link in Safari, tap **Share**, then **Add to Home Screen**.

## Limitations

The app shell works offline after it has been cached, but sample photos are hosted on Unsplash and need internet access. Uploaded photos stay on the user's device; they are not shared. Save and Create currently show confirmation messages but do not store a design. Style options apply photo filters rather than generating or rearranging a room.
