# 🌰 Chestnut Stand

A cozy street-stand game: roast chestnuts and corn on your stove, serve the customers
before they lose patience, collect coins and upgrade to a bigger stove.
12 days across two seasons (Autumn / Winter and Spring / Summer), plus a gift waiting at the end of the Train Station day.

> **Built with vibe coding by Me, myself and I.** 🎨🤖


---

## How to play

- **Tap the grill** to start roasting.
- **Tap the glowing chestnuts/corn** when they are ready to pick them up (leave them too long and they burn!).
- **Tap a customer** to serve their order. Quick service earns tips.
- Save coins and tap **Bigger stove** for more slots.
- Reach the day's coin goal for ⭐ stars and to unlock the next day.

## Playing on a phone

Play **sideways (landscape)**. If you hold the phone upright, the game pauses and asks you to rotate.
Use the ⛶ button in the top bar for full screen (browsers only — the installed app is already full screen).

## Install as an app (PWA)

The game is a Progressive Web App: it installs to the home screen and works **offline**.
It must be served over **HTTPS** (or `localhost`) — opening `index.html` straight from disk works for playing,
but does not install or cache.

- **Android / Chrome:** open the page → ⋮ menu → *Install app* / *Add to Home screen*.
- **iPhone / iPad (Safari):** Share → *Add to Home Screen*.
- **Desktop Chrome / Edge:** install icon in the address bar.

## Run locally

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Publish (free)

Upload the whole folder to any static host — GitHub Pages, Netlify, Cloudflare Pages, etc.
All paths are relative, so it also works from a sub-folder (e.g. `https://you.github.io/chestnut-stand/`).

## The gift video

The "A gift for you" button (unlocked after passing the Train Station day) plays `kastanas-gift.mp4`,
which is included next to `index.html` (about 10 MB, 59 s, 720p H.264/AAC). It streams from the network,
so the gift needs an internet connection; everything else works offline.
The game tells the player this too: on the Train Station results screen, on the gift tile in the menu, and under the video.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The game (canvas, ~55 KB of code) |
| `kastanas-gift.mp4` | The gift video |
| `assets/` | Images and music extracted from the original single-file build |
| `manifest.webmanifest` | PWA manifest (name, icons, landscape, full screen) |
| `sw.js` | Service worker — caches everything for offline play |
| `icons/`, `favicon.ico` | Favicon, app icons, maskable icons, Apple touch icon |

When you change any file, bump `VERSION` in `sw.js` so installed copies update.

Progress (coins, stars, upgrades) is saved in your browser's local storage on that device.

---

© Built with vibe coding by **Me, myself and I**.
