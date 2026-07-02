# ProLedge — Launching Soon

A standalone "coming soon" landing page for **ProLedge**.

> **Beyond Average. Built Better.** — world-class finance & accounting education, launching soon.

## Features

- Cinematic **black & white "Skyfall"** theme
- Poster-style landing screen: giant **LEARN** type with a walking figure composited in (`mix-blend-mode: multiply`) and mouse/touch/tilt **3D parallax**
- Animated rotating word (**Matters / Moves You / Lasts / Counts**)
- Hero with Warren Buffett quote + waitlist signup
- Waitlist capture → **Google Sheet** (name, email, country code, mobile, education); also mirrored to `localStorage`
- Fully responsive + reduced-motion friendly

## Folder structure

```
launching-soon/
├── index.html            # the landing page (entry point)
├── 404.html              # branded not-found page
├── site.webmanifest      # PWA manifest
├── robots.txt            # crawler directives
├── sitemap.xml           # sitemap
├── serve.ps1             # local static dev server (port 5501)
├── google-apps-script.gs # Apps Script for the waitlist → Google Sheet (reference; not served)
├── README.md
└── assets/
    ├── favicon.svg        # brand favicon (chart mark)
    └── images/
        ├── walk.png       # poster figure — the walking gentleman (REQUIRED)
        ├── proledge_converted.svg   # footer logo (REQUIRED)
        ├── hero-1.jpg     # legacy / unused (old slideshow)
        ├── hero-2.jpg     # legacy / unused
        ├── hero-3.jpg     # legacy / unused
        └── hero-4.jpg     # legacy / unused
```

## Run locally

```powershell
powershell -ExecutionPolicy Bypass -File serve.ps1
```

Then open <http://localhost:5501/>.

Any static host works too — just upload the contents of this folder.

## Customizing

- **Poster figure:** replace `assets/images/walk.png` (a light-grey-background photo blends best with the `multiply` composite).
- **Headline / copy:** edit the poster text and the `<h1>` / `.hero-sub` in `index.html`.
- **Brand colors:** defined as CSS variables in the `:root` block of `index.html`.
- **Waitlist → Google Sheet:** set `const SHEET_ENDPOINT` in `index.html` to your deployed Apps Script `/exec` URL (see `google-apps-script.gs`).
- **Canonical URL / social meta:** update the domain references in the `<head>` to your real domain.

## License

© ProLedge. All rights reserved.
