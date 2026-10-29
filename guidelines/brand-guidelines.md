# Vidra brand and marketing guidelines

Version 2.1 · 29 October 2026

The reference approved on 29 October 2026 establishes Vidra’s new marketing identity: warm paper, deep navy, a black V/play mark, and a quiet launch page. This replaces the cyan/otter marketing identity and its long technical homepage. The product interface remains governed by `design-system/tokens.css`; this change does not recolor the application.

[Editable Figma guidelines](https://www.figma.com/design/3UVHlVHh4MXHoBUdufD2n7)

## 1. Position and launch message

Vidra is a streaming platform for videos, creators, and viewers. At this launch stage, say what is being built and invite interest. Do not imply that a hosted service is already open.

- Status: **Coming soon**. Keep the visible words with the square status mark.
- Eyebrow: **Vidra Beta**.
- Headline: **A new home for streaming is taking shape.**
- Supporting copy: **We’re building Vidra — a streaming platform for videos, creators, and viewers. A place to discover, watch, and share what moves you.**
- Primary action: **Join waitlist**.
- Contact: **support@vidra.media**.

The current action opens an email request to support; it does not store an address or confirm registration. Any future form must name its collection behavior and show confirmation only after successful submission. No invented audience counts, launch dates, testimonials, speed claims, or “premium” quality claims. Technical claims need a mechanism or measurement verified in source code. Derive release counts with the site’s envelope script; never copy a README count.

## 2. Logo

The mark combines a descending V stroke with a separate right-facing play triangle. Use the canonical vectors in `assets/logo/`. The horizontal lockup is the default; the icon is for compact placements, and the stacked lockup is for square formats. The wordmark is outlined so it cannot change with installed fonts.

Use black on Paper. For repository READMEs, use `assets/readme/logo.svg`: its fixed Paper tile stays readable in either viewer theme. A reversed mark on Navy may use Paper, but never let the asset switch with the operating system. Keep at least half the mark’s width clear on every side. Render a standalone mark at least 1.5rem high and a marketing lockup at least 2.75rem high. Do not stretch, rotate, tint, add a badge, or combine the retired otter with the new mark.

## 3. Marketing palette

| Token | Value | Role |
| --- | --- | --- |
| `--brand-paper` | `#F1E8DF` | Main page ground |
| `--brand-ink` | `#0D1B3B` | Headline, primary action, status, focus |
| `--brand-black` | `#080808` | Logo and action hover |
| `--brand-muted` | `#666361` | Body and footer text |
| `--brand-white` | `#FFFAF4` | Text on Navy and illustration highlights |
| `--brand-line` | `#B9B3AF` | Decorative construction lines only |
| `--brand-surface` | `#E5D9CE` | Illustration surfaces |
| `--brand-slate` | `#747E90` | Illustration mountain layers |
| `--brand-signal` | `#F4B942` | Decorative data wires, packets, node edges and player receipt |

Use `design-system/brand-tokens.css`; the marketing site copies it into `app/brand.css`. Component colors reference tokens. Navy is a dark neutral, not the product’s indigo accent. Cyan is retired from marketing. Do not add indigo, bright accent gradients, or automatic dark-mode recoloring. Decorative low-contrast lines must never carry essential information.

## 4. Typography

Use the native system sans stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Arial, sans-serif`. No webfonts. The fixed vector wordmark is an asset, not a typeface for page text. Figma specimens use Inter only as a preview fallback when system fonts are unavailable.

| Role | Size | Weight / leading |
| --- | --- | --- |
| Hero | `clamp(3rem, 5.4vw, 4.6rem)` | 800 / 1.025, tracking −0.055em |
| Mobile hero | `clamp(2.75rem, 10.8vw, 4rem)` | 800 / 1.025 |
| Supporting copy | 1.1875rem desktop, 1.0625rem mobile | 400 / 1.6 |
| Eyebrow | 0.9375rem | 700 / 1.5 |
| Action / footer | 0.875rem | 700 action, 400 footer |
| Status micro-label | 0.6875rem | 750 / 1.4, tracking 0.14em |

Sentence case throughout. Uppercase is reserved for the status micro-label. Use rem for visible sizing; preserve reader font scaling and readable wrapping. Never shrink text to force a reference-image line break.

## 5. Layout and imagery

A single launch composition: header with logo at left and status at right; headline and action at left; one isometric streaming illustration at right; legal/contact footer. Use generous empty space and a continuous Paper ground. No feature grids, comparison tables, install commands, architecture explorers, demo gallery, extra marketing navigation, or sticky install bar in this launch treatment.

At narrow widths, stack copy, action, then artwork. Let the page scroll naturally. The illustration must not force horizontal scrolling. Footer items stack on phones. Keep header logo and status visible without a menu.

Signal Yellow is a decorative illustration accent only; it does not become a button, body-text or status color. The maintainer’s 29 October animation amendment allows gentle floating and glowing packets moving along wires toward the player. Reduced motion leaves the wires and tag visible but still. The atproto tag uses the current official `at://` header mark with an adjacent lowercase protocol label; it does not claim that video bytes travel over AT Protocol.

The illustration is conceptual artwork: translucent cream planes, navy player, quiet mountain thumbnails, and sparse dashed construction lines. It is not evidence of a shipping interface. Mark it decorative in HTML; do not expose fictional playback controls as buttons. Real product captures, if added later, need source and capture date. No stock photography, emoji, mascot, or unrelated ornamental scene.

## 6. Voice and accessibility

Write plainly and invite participation. “We’re building” is appropriate to the launch page; technical documentation may address the operator as “you.” Avoid unsupported superlatives, urgency, performance promises, competitor claims, and claims of security audits. A concise promise of intent is distinct from an assertion of delivered functionality.

Body text must meet 4.5:1 contrast; large text and functional boundaries 3:1. The approved Navy/Paper, Muted/Paper, and White/Navy pairs meet those thresholds. Every action has a 2.75rem minimum target. Show a visible Navy focus outline with spacing from the control. Keep semantic header/main/footer, one H1, a keyboard skip link, meaningful image alternatives for logos, and hidden decorative artwork. Respect reduced motion. No webfonts, UI kit, tracking, or dependencies for cosmetic effects.

## 7. Distribution and governance

Canonical vectors, README banner, README logo tile, and powered-by badge live in this repository. Consumers should reference the shared `main` assets or copy them verbatim. The README banner doubles as the source of the raster 1200×630 social card. Regenerate PNGs after any banner change.

This version supersedes v1.x marketing color, logo, hero copy, imagery restrictions, and multi-section rhythm. Historical Git revisions preserve the former system. Product tokens and operator configuration are not part of this marketing migration. Future decisions update these guidelines, Figma, the identity index, the brand token copy, and affected assets together.
