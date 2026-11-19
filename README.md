# Wellsy65

Astro music website for https://wellsy65.com. GitHub `main` deploys through Cloudflare Pages (`npm run build`, output `dist`).

## Development

Install with `npm ci`. Use `npm run dev -- --background` for a local server and `npm run astro -- dev stop` to stop it. `npm run build` builds production files.

## Updating music

Edit `src/data/releases.json` to change the featured tracks. Each entry has a title, unique slug, public listening URL and local artwork path. Artwork lives in `public/artwork`. Use square images. Track links open the artist's SoundCloud releases; no autoplay or embedded third-party player is loaded.

The mixes section links to the artist's SoundCloud playlists. Replace that link with a specific DJ-mix collection when selected. All section copy is in `src/pages/index.astro`; styling and responsive layouts are in `src/styles/global.css`.

The vinyl and waveform visuals are CSS, with no external image or animation dependency. Typography uses Google Fonts with system fallbacks. No analytics or contact-form backend is configured.

## Domain

`astro.config.mjs` sets the canonical origin. `public/_redirects` redirects www to the apex. `public/robots.txt` and `public/sitemap.xml` support search indexing.
