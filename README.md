# Backlog: standalone app

A game backlog tracker you can install on your phone's Home Screen. It starts with an empty
library, saves everything on the device, and works offline.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole app: layout, styles and code in one file |
| `manifest.webmanifest` | Tells the phone the app's name, icon and that it opens full screen |
| `sw.js` | The service worker: saves a copy of the app so it opens without internet |
| `icons/` | Home Screen and browser icons |

## Put it online (free, with GitHub Pages)

An app installed from Safari has to come from a real web address (https), so host the folder once:

1. Sign in at github.com and create a new **public** repository, for example `backlog`.
2. On the repository page choose **Add file → Upload files**, drag in everything in this folder
   (including the `icons` folder), and press **Commit changes**.
3. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**,
   pick the `main` branch and the `/ (root)` folder, and press **Save**.
4. After a minute the page shows your address, like `https://yourname.github.io/backlog/`.

## Install it on your iPhone

1. Open that address in **Safari**.
2. Tap **Share → Add to Home Screen**, then **Add**.
3. Open Backlog from the Home Screen. It runs full screen, like an app.

## Your data

- Games, journal entries, rankings and settings are saved on the phone, inside the app.
- Photos and videos you add to entries are stored on the phone too.
- Nothing is sent anywhere. Removing the app from the Home Screen can delete its data, so use
  **Export backup** (at the bottom of the Backlog page) now and then. **Restore from backup**
  loads a backup file back in. Backups hold everything except photos and videos.

## Updating the app later

Replace `index.html` in the repository with the new version, and change `VERSION` at the top of
`sw.js` (for example `backlog-v2`) so phones fetch the new copy. Opening the app twice picks it up.
