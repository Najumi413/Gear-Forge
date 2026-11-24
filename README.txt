# Gear Forge

A small installable PWA for desktop and mobile.

## What it does
- Three lines with 100%, 50%, and 30% activation chances.
- Stat weights: 10%, 12%, 12%, 10%, 12%, 12%, 12%, 10%, 10%.
- Target stats are Stat 1, Stat 4, and Stat 8.
- A stat cannot appear more than once in the same roll.
- You manually lock only target stats; any target line can be locked first.
- Each locked line increases the next roll cost by one module (1, 2, or 3).
- Tracks rolls, modules spent, and roll history.
- Saves session locally on the device and works offline after first load.

## Probability implementation assumption
When a stat is already used in a roll or held by a locked line, the remaining available stat weights are renormalized proportionally before the next line draws. Lines are processed in order: Line 1, then Line 2, then Line 3. Activation probabilities stay unchanged.

## Install on Windows / desktop
1. Host this folder on an HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages, etc.), or run it locally on `http://localhost`.
2. Open the site in Chrome or Edge.
3. Use the install icon in the address bar, or browser menu > Install Gear Forge.

## Install on Android
1. Open the HTTPS site in Chrome.
2. Browser menu > Install app / Add to Home screen.

## Install on iPhone
1. Open the HTTPS site in Safari.
2. Tap Share > Add to Home Screen.

## Important
A PWA must be served from HTTPS (or localhost) to install and use offline features. Opening `index.html` directly as a file will run the simulator, but will not enable PWA installation/service-worker caching.
