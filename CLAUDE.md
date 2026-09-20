# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Internal guidance

This repository is PUBLIC. Never commit internal strategy, analytics,
credentials, or business notes here. The operating tenets and cross-repo
guidance live in the private coordination repo
(`~/localdev/radioapp-hq/CLAUDE.md`) — read that before making changes.

## Project Overview

This is a static GitHub Pages website for Likely Labs, a company that makes mobile radio apps. The site is hosted at likelylabs.com via the CNAME file.

## Structure

- `index.html` - Main landing page
- `*-privacy.html` / `*-terms.html` - Privacy policy and terms of service pages,
  one pair per app. Store listings link these, so treat every URL as load-bearing:
  - hkradio (Hong Kong Radio)
  - hktwradio (Hong Kong/Taiwan Radio)
  - sgradio (Singapore Radio)
  - myradio (Malaysia Radio)
  - vnradio (Vietnam Radio) - legacy market, no current app, pages still served.
    Do not remove them without first confirming no published listing links them.
  - photoswipe (PhotoSwipe)
  - tennisserve (TennisServe)
  - undertone - `undertone-privacy.html` only (no terms page)
- `hkradio/`, `hktwradio/`, `sgradio/`, `myradio/` - one-link landing pages
  (`index.html` + `icon.png`) that route a visitor to the right app store
- `assets/` + `assets/large/` - station logos and artwork served at
  `likelylabs.com/assets/...`; the station backup feeds reference these URLs,
  so renaming or deleting a file here breaks live feeds
- `app-ads.txt`, `sellers.json` - advertising authorization files
- `robots.txt`, `sitemap.xml` - crawler files (`robots.txt` is `Allow: /`)
- `googlebe222f8132685055.html` - Google site verification
- `.well-known/appspecific/com.tesla.3p.public-key.pem` - PUBLIC key that the
  Tesla Fleet API requires a registered third-party application to publish.
  Unrelated to the radio apps; publishing it is intended, it is not a secret.
- `CNAME` - likelylabs.com
- `.nojekyll` - serve files verbatim, no Jekyll build (this is also why `.md`
  files in this repo are served raw at the apex domain)
- `og-card.png`, `logo.jpg` / `logo.png` / `logo.webp`, `*-icon.png` / `.webp`

## Development

No build process required. This is a static HTML site:
- Edit HTML files directly
- Push to master branch to deploy via GitHub Pages
- Test locally by opening HTML files in a browser
