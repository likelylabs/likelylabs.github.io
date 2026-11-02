# Lessons — likelylabs.com

- **WebKit collapses a stretched grid item that relies on `aspect-ratio`.**
  A `.art` box with `aspect-ratio`, `height:auto`, an absolutely positioned
  image and `align-self:stretch` renders at the right height in Chrome and at
  zero height in Safari (the stretch makes the height definite from a row whose
  height is the item's own content). Give such items `align-self:start` and an
  in-flow image on the breakpoint where they are the only column. Found on the
  iPhone 17 simulator, 2026-11-02; Chrome's mobile emulation did not show it.
- **Headless Chrome will not go narrower than about 500px.** A
  `--window-size=390,…` capture lays the page out at ~500px and crops, which
  looks like horizontal overflow. Verify mobile with the built-in browser's
  mobile preset and a `scrollWidth === clientWidth` probe instead.
- **An element's own `clip-path` beats the global `:focus-visible{clip-path:none}`.**
  Same specificity, later rule wins, so the focus ring on `.btn` / `.chip` was
  clipped. Add `.btn:focus-visible,.chip:focus-visible` to the focus rule.
- **App Store screenshot sources.** `itunes.apple.com/lookup?id=…` returns
  `screenshotUrls`; swap the trailing `320x480bb.jpg` for `1290x2796bb.png` to
  get full-size frames. Marketing frames carry a phone mock, so prefer the raw
  captures in the app repos (`loudplace/design/brand/store-captures`,
  `tennis-serve/outputs/store-shots-build35/raw`) when they exist.
