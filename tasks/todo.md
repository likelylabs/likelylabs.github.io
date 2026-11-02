# likelylabs.com — tasks

## 2026-11-02 — Portfolio facelift (cyber art deco)

Brief: pull every launched project into the portfolio and give the whole page a
cyber art deco facelift matched to the Likely Labs wordmark. Every project gets
a hero image; Cyberoffroading wears an "Acquired" ribbon.

### Design plan

- Palette: ink `#0a0b14`, champagne `#f3efe4`, brass `#d8b45f`, lit gold
  `#ffcf6b`, magenta neon `#ff54a8` (the og-card glow), panel `#10111e`.
- Type: Poiret One for display (the wordmark's thin geometric strokes), Jost
  for everything else. No monospace.
- Layout: centred deco marquee hero with a sunburst and perspective grid floor;
  centred chapter rules for Apps / Web / Tools; every project is a framed
  "poster" — chamfered hero image, title plate, one-line blurb, a single link.
  Ekicho leads as the featured piece.
- Motion: one hero bloom on load; hover lights the frame. Reduced motion
  respected.

### Checklist

- [x] Scout current site, sibling repos, store listings
- [x] Gather facts + hero sources (App Store screenshots, og images, raw captures)
- [x] Compose app heroes on a shared deco backdrop (PIL), draw the Hide
      Unverified X feed illustration, crop the Cyberoffroading dusk photo
- [x] Encode heroes: 1200w + 800w, WebP q80 from source + JPEG q82 fallback,
      verified every WebP is smaller than its JPEG
- [x] Rebuild index.html
- [x] Owner mid-flight: add Claude Switcher under Tools (menu screenshot hero,
      icon from the repo), remove Rivian Essentials (poster + hero files)
- [x] Verify: headless Chrome full page at 1440 and the built-in browser at
      375 (scrollWidth == clientWidth, no console errors), Tab focus rings on
      chips (clip-path cleared on :focus-visible), WebKit via iPhone 17 sim
- [x] Multi-agent review: 22 agents, 12 confirmed findings fixed (Undertone Play
      link, TennisServe video claim, Radio overclaim, Switcher wording, poster
      focus ring, --faint contrast 3.3→5.9:1, h4 product titles, link names,
      copy-button failure state), 7 rejected
- [x] Commit, push (deploys)

### Project facts used

| Project | Status | Link |
|---|---|---|
| Ekicho | launched (invite) | https://ekicho.ai |
| Undertone 2.0 | App Store | id6779034581 |
| TennisServe 2.0 | App Store | id6800581766 |
| PhotoSwipe 1.8 | App Store | id6757325562 |
| Radio Network | App Store + Play | hk / hktw / sg / my |
| Tesla Essentials | live | tesla-essentials.com |
| Cyberoffroading | acquired | cyberoffroading.com |
| Hide Unverified X | open source | github.com/kevinchau/hide-unverified-x |
| Claude Switcher | open source, macOS | github.com/kevinchau/claude-switcher |
