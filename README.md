# NAVKIN — site copy

A static copy of **navkin.com** ("NAVKIN – Kompletta Säkerhetslösningar, för alla
branscher."), reconstructed from the Wayback Machine snapshot dated
`20250329130924` (29 Mar 2025).

## What's here

- **`index.html`** — the home page, fully de-archived:
  - All Internet Archive injection removed (Wayback toolbar, `wombat.js`,
    `bundle-playback.js`, `ruffle.js`, `__wm` rewrite hooks, archive analytics).
  - Every `web.archive.org/web/…/` URL unwrapped back to its original target.
  - All localized asset references repointed from the saved `…_files/` folder
    to a local **`assets/`** folder.
  - All inline theme CSS (WordPress global styles + Salient dynamic styles +
    WooCommerce) is preserved in the document, so structure and most styling are
    intact.
- **`assets/`** — target folder for the page's external assets (see below).

Page content (Swedish): a security-solutions company site built on the Salient
WordPress theme — hero "Ett säkerhetsbolag att lita på.", sections for
Företag & Organisationer / Myndigheter / Privatpersoner, branschlösningar,
produkter, kundcase, and contact (info@navkin.com · +46 (0) 8 551 135 99).

## Completing the copy (the 86 external assets)

The uploaded source was a single saved `.html` file **without** its companion
`…_files/` asset folder, and this environment has no network access to
`web.archive.org`, so the external stylesheets, scripts, and a few images
could not be downloaded here. Images that use the Jetpack CDN
(`i0.wp.com/…`) load directly over the web with no extra files needed; the
remaining assets are referenced under `assets/`.

To make the copy fully self-contained, drop the contents of the original
`NAVKIN … _files/` folder (the one your browser created next to the saved
`.html`) into **`assets/`**. The page expects these 86 files:

- 37 CSS, 32 JS, 12 images, plus a few misc files
  (full list in `assets/MANIFEST.txt`).

Alternatively, re-run this task in an environment whose network policy allows
`web.archive.org`, and the assets can be fetched automatically with:

```
wget -mkEpnp "https://web.archive.org/web/20250329130924/https://navkin.com/"
```

## Viewing

Open `index.html` in a browser. With internet access the CDN-hosted images
render immediately; once `assets/` is populated the page matches the archived
snapshot.
