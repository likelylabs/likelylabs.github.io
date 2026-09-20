# likelylabs.com

The Likely Labs website. A static site served by GitHub Pages from the
`master` branch of this repository, published at **https://likelylabs.com**
(see `CNAME`). `.nojekyll` is present, so files are served exactly as they
are committed — there is no build step and no Jekyll processing.

## What is here

- `index.html` — the landing page.
- `*-privacy.html` / `*-terms.html` — the legal pages the app store listings
  link to, one pair per app (hkradio, hktwradio, sgradio, myradio, vnradio,
  photoswipe, tennisserve), plus `undertone-privacy.html`.
- `hkradio/`, `hktwradio/`, `sgradio/`, `myradio/` — one-link landing pages
  that send a visitor to the right store for their device.
- `assets/` (with `assets/large/`) — station logos and artwork served at
  `likelylabs.com/assets/…` and referenced by the station backup feeds.
- `app-ads.txt`, `sellers.json` — advertising authorization files.
- `robots.txt`, `sitemap.xml`, `og-card.png`, `googlebe222f8132685055.html` —
  crawler, sitemap, social-card and site-verification files.
- `.well-known/appspecific/com.tesla.3p.public-key.pem` — the public key a
  Tesla Fleet API third-party application is required to publish.
- `logo.jpg` / `logo.png` / `logo.webp` and the `*-icon` images.

## Editing and deploying

Edit the HTML directly and open it in a browser to check it. **Pushing to
`master` deploys the live site** — there is no staging step, so review the
diff before pushing.

Everything in this repository is public and crawlable, Markdown files
included: they are served raw at the apex domain.

## Station backup feeds

Moved to the `likelylabs-feeds` repo, served at `https://feeds.likelylabs.com/`
(dedicated subdomain so the backing host can be re-pointed via DNS without
shipping new app binaries). See that repo's README for the update rules.
