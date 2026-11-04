# Geo Snap — Launch page

A single page for the launch of **Geo Snap - NLR** on Google Play.

Press **Launch now** and the page runs a short sequence — contacting servers,
launching to Google Play, Play accepted the release — then announces
*We are live on Google Play* with sound and confetti.

## How it works

Everything is one file. `index.html` carries its own CSS and JavaScript, and
the only outside request is Google Fonts. There is no build step, no
framework and no server: open the file and it runs.

The launch instant is one line near the top of the script:

```js
var LAUNCH = new Date(2026, 10, 5, 10, 0, 0);   // month is 0-based
```

A tab left open turns itself into the announcement at that moment, so nobody
has to be awake or deploy anything. The button is a way to go early, never
the only way to go at all. After the instant has passed the page opens
already announced.

Sound is synthesised with the Web Audio API rather than loaded from files, so
there is nothing to host and nothing that can fail on the morning itself. It
can be switched off with the control at the bottom left, and every animation
is disabled for anyone whose system asks for reduced motion.

## Deploying

Any static host works — it is one HTML file.

- **Vercel** — import this repository; no framework, no build command.
- **GitHub Pages** — Settings → Pages → deploy from `main`, root.
- **Anywhere else** — copy `index.html` and `favicon.png`.

## Colours

Taken from the main site at [locsnapnlr.vercel.app](https://locsnapnlr.vercel.app):
cream `#F7F5EC`, ink `#1B1E22`, rule `#E7E3D6`, teal `#0E7C91`, gold `#E8B44A`.

---

A product of **NLR Group of Companies**.
