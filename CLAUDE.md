# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static GitHub Pages website for Likely Labs, a company that makes mobile radio apps. The site is hosted at likelylabs.com via the CNAME file.

## Structure

- `index.html` - Main landing page (based on a Coming Soon page template)
- `*-privacy.html` / `*-terms.html` - Privacy policy and terms of service pages for mobile apps:
  - hkradio (Hong Kong Radio)
  - vnradio (Vietnam Radio)
  - hktwradio (Hong Kong/Taiwan Radio)
  - sgradio (Singapore Radio)
  - myradio (Malaysia Radio)
- `app-ads.txt` - App-ads.txt for ad network verification
- `logo.jpg` - Company logo

## Development

No build process required. This is a static HTML site:
- Edit HTML files directly
- Push to master branch to deploy via GitHub Pages
- Test locally by opening HTML files in a browser
