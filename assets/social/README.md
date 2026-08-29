# Social cards

One template, every surface. [`og-card.mjs`](og-card.mjs) is the canonical
1200×630 OG/social card: the README banner centred on a fixed Ink `#0C2136`
ground, artwork inside a centred ~1120×550 safe area for crop tolerance.

Crawlers that matter (X, Slack, older LinkedIn) drop SVG cards, so consuming
repos commit the rendered PNG and regenerate it here whenever the banner
changes — vidra-site's `public/brand/og-card.png` and the docs' social card
both regenerate from this script, never from per-repo exports.

## Usage

The script renders with Playwright Chromium and nothing else. This repo does
not ship one; run it from a checkout that does (vidra-site does):

```
node ../vidra-branding/assets/social/og-card.mjs public/brand/og-card.png
```

Arguments: output path first (default `./og-card.png`), then an optional
banner path (default [`../readme/banner.svg`](../readme/banner.svg)).

## The one check

The banner must not carry a `prefers-color-scheme` switch — an asset that
flips with the OS mode renders Ink-on-Ink when rasterised onto the card's
fixed Ink ground. The script checks for the switch mechanically and refuses
to render; if the artwork ever needs one, rasterise a fixed-ground variant
instead. Never let the rasteriser pick a mode.
