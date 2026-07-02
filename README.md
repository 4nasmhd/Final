# ProLedge — Launching Soon

A standalone "coming soon" landing page for **ProLedge**.

> **Learn What Matters.** — practical CMA® & FMAA™ preparation, built by CMA-qualified professionals.

## Features

- **ProLedge brand theme** — deep navy & sky blue, matched to the logo
- CFA-style hero: full-bleed real photography slideshow (Ken-Burns crossfade) with 3D mouse/touch parallax
- Animated rotating headline word (**Matters / Moves You / Lasts / Counts**)
- **Who We Are** mission statement (italic, CFA-style)
- **Programs** section — CMA® and FMAA™ tiles with photo headers and syllabus highlights
- **Why ProLedge** feature grid ("We build leaders, not just certificate holders.")
- Signup section with Warren Buffett quote + waitlist form ("Reserve Your Spot")
- Waitlist capture → **Google Sheet** (name, email, country code, mobile, education); also mirrored to `localStorage`
- Footer with logo, office address (Kakkanad, Ernakulam), LinkedIn & Instagram links, and IMA® trademark note
- Interactive blue dot-grid pointer effect
- Fully responsive + reduced-motion friendly

## Folder structure

All assets live **flat in the repo root** (matches the GitHub Pages deployment):

```
launching-soon/
├── index.html              # the landing page (entry point)
├── 404.html                # branded not-found page
├── favicon.svg             # brand favicon (chart mark)
├── hero-1.jpg              # NYC skyline — signup background + hero slide
├── hero-2.jpg              # professionals collaborating — hero slide + FMAA card
├── hero-3.jpg              # skyscrapers — hero slide + CMA card
├── hero-4.jpg              # unused (CGI render — kept for reference only)
├── proledge_converted.svg  # footer logo (REQUIRED)
├── site.webmanifest        # PWA manifest
├── robots.txt              # crawler directives
├── sitemap.xml             # sitemap
├── serve.ps1               # local static dev server (port 5501)
├── google-apps-script.gs   # Apps Script for the waitlist → Google Sheet (reference; not served)
└── README.md
```

## Run locally

```powershell
powershell -ExecutionPolicy Bypass -File serve.ps1
```

Then open <http://localhost:5501/>.

## Deploy (GitHub Pages)

1. Push/upload the contents of this folder to the repo root.
2. Repo **Settings ▸ Pages ▸ Deploy from a branch** → `main` / `/ (root)`.
3. The site goes live at `https://<username>.github.io/<repo>/`.

Any other static host works too — just upload the folder contents as-is.

## Customizing

- **Photos:** replace `hero-1/2/3.jpg` (use real photography only — no AI/CGI imagery).
- **Headline / copy:** edit the `<h1>`, `.hero-sub`, and section text in `index.html`.
- **Brand colors:** defined as CSS variables in the `:root` block of `index.html`.
- **Waitlist → Google Sheet:** set `const SHEET_ENDPOINT` in `index.html` to your deployed Apps Script `/exec` URL (see `google-apps-script.gs`).
- **Social links:** LinkedIn & Instagram are wired in the footer; the X icon is still a placeholder.

## License

© ProLedge. All rights reserved.
