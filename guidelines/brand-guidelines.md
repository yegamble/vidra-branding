# Vidra brand guidelines

**v1.1 · August 2026.** Vidra is a video platform you install yourself. These are the rules
for how it looks and speaks everywhere **outside the product interface**. (Inside the
product, the [design system](../design-system/README.md) governs.)

*New in v1.1: a Foundation section (§00), Mist `#EEF7FB` in the palette, an explicit
spacing scale in §07, an Accessibility section (§09), and an interactive edition of this
document at [`portal/index.html`](../portal/index.html).*

---

## 00 — Foundation

**Mission.** Video hosting anyone can own. One small server holds the origin; distribution
is offloaded to the people watching, to a CDN, or to IPFS — so the cost of an audience does
not scale with the size of it.

**Personality.** Plain, precise, confident. Vidra says the number, not the adjective, and
uses the real term: ActivityPub, egress, CID, instance.

**Promise.** No vendor between you and your viewers. AGPL v3, federation on by default,
one compose file, and an egress bill that stays flat as the audience grows.

Everything below is a rule; this section is the reason the rules exist.

## 01 — The mark

One otter, four sizes, no variations. The mark is the only drawn asset the brand owns.
It is supplied as vector ([`assets/logo/vidra-icon.svg`](../assets/logo/vidra-icon.svg))
and is **never redrawn, recoloured, outlined, rotated or set inside another shape**.

- **Clear space:** half the mark's height on every side.
- **Minimum sizes:** 16px favicon · 24px minimum in UI · 40px minimum in print ·
  64px comfortable.
- **Approved backgrounds:** Paper `#F5F5F7` (preferred) · Ink `#0C2136` (preferred) ·
  Ice `#CBF2F4` (permitted) · photography/media only behind a 45% Ink scrim.

## 02 — Lockups

**The logotype is drawn** ([`vidra-logotype.svg`](../assets/logo/vidra-logotype.svg),
v1 · 2026-08): "Vidra" as fixed vector outlines derived from Inter Display Bold
(SIL OFL — SF-adjacent proportions, legally redistributable, unlike SF Pro) at the
brand's **−0.045em tracking**, shaped with real kerning. It renders identically on
every platform, in print, and in forced-colour contexts. Use the drawn logotype for
**logo placements** (lockups, banners, headers, decks); inline and UI text still sets
"Vidra" live in the system face at 700 / −0.045em.

- **Horizontal** (default): gap equals a third of the mark's width —
  [`vidra-lockup-horizontal.svg`](../assets/logo/vidra-lockup-horizontal.svg)
- **Stacked**: for square placements and avatars —
  [`vidra-lockup-stacked.svg`](../assets/logo/vidra-lockup-stacked.svg)
- **Mark alone**: only where "Vidra" is already on screen.

**Instance lockup.** Anyone can run Vidra, so most real-world lockups belong to somebody
else. The operator's name leads; Vidra follows in muted type at 13px ("powered by
Vidra"). Never co-size the two — the platform is the smaller signature.

## 03 — Colour

**Cyan outside the product, indigo inside it.** The mark's cyan sits close to both
Bluesky blue and IPFS teal, which the interface reserves for federation identity. Rather
than fight that, the boundary is drawn at the edge of the app: the brand leads everywhere
people read about Vidra; the product keeps the accent it ships and has verified.

| Colour | Hex | Use |
|--------|-----|-----|
| **Vidra Cyan** | `#22BDE3` | The brand colour. Fills, rules, dots, large type on Ink. |
| **Deep Cyan** | `#16A3E2` | Secondary fill. The mark's own shadow tone. |
| **Action Cyan** | `#0B7EA3` | The only cyan that may sit under white text (4.5:1). |
| **Ice** | `#CBF2F4` | Tints, quiet section grounds, chart fills. |
| **Mist** | `#EEF7FB` | Quiet tint surface for cards and section grounds on Paper. |
| **Ink** | `#0C2136` | The dark ground. Headlines, full-bleed sections. |
| **Slate** | `#1D466A` | Dividers and depth on Ink. Never body text on Paper. |
| **Muted** | `#4C6478` | Secondary text on Paper. Clears AA. |
| **Paper** | `#F5F5F7` | Shared with the product canvas — the one continuity. |

Two tints, two jobs: **Ice** is the saturated one (charts, brand moments, type on Ink);
**Mist** is the quiet one (documentation cards, marketing section grounds on Paper, where
Ice would announce itself).

| Surface | Leads with | Accent for actions |
|---------|-----------|--------------------|
| Marketing site | Ink + Vidra Cyan | Action Cyan |
| Docs | Paper + Ink | Action Cyan |
| Social, decks, print | Ink + Vidra Cyan | Vidra Cyan as fill only |
| Transactional email | Paper + Ink | Action Cyan |
| **The product interface** | Canvas + surfaces | **systemIndigo — unchanged** |

Two rules keep the boundary clean: cyan never becomes an interactive colour inside the
app, and indigo never appears on a brand surface. The handoff happens at the sign-in
screen.

## 04 — Typography

One face, tighter as it gets bigger. The brand uses the same system stack as the product
(SF Pro on Apple platforms, the native UI face elsewhere, Helvetica Neue fallback), so a
marketing page and the app are set in the same face. Nothing is licensed, nothing
downloads.

Nine levels (extended from five on 2026-08-28, absorbing the ramp vidra-site proved in
production). Sizes are the full-width px; the tokens in
[`brand-tokens.css`](../design-system/brand-tokens.css) set them in **rem, clamped down
on small screens** — never px — so the reader's own font-size setting scales the page.

| Level | Spec |
|-------|------|
| Hero | 64 / 1 · 700 · −0.05em — clamps to 38 on a phone |
| Section head | 44 / 1.09 · 700 · −0.04em |
| Sub | 24 / 1.25 · 700 · −0.025em — a heading inside a section |
| Card title | 20 / 1.4 · 700 · −0.02em |
| Standfirst | 22 / 1.41 · 400 — one or two lines under a headline, never three |
| Body | 17 / 1.53 · 400 — 66-character measure |
| Small | 15 / 1.5 · 400 — captions, dense rows; semibold for labels |
| Mono | 14 / 1.7 — commands, CIDs, stream keys |
| Micro | 11 / 1.4 · 700 · +0.14em, all caps — the only place all caps is allowed |

- **Sentence case, always** — headlines, buttons, nav, section labels. Title Case reads
  like a press release; all caps is reserved for 11px micro-labels.
- **Two weights** — regular for reading, bold for headings. Semibold exists for 13–15px
  labels. Light and black are not part of the brand.

## 05 — Voice

Say the number, not the adjective. Vidra's audience installs software on servers — they
can tell when a claim is measurable and when it is decoration. Write for the person
reading the docs, not the person skimming the homepage.

**Plain** (the shortest true sentence wins) · **Factual** (every claim has a number or a
mechanism) · **Confident** (no hedging, no "simply", no apologising for complexity) ·
**Precise** (use the real term: ActivityPub, egress, CID, instance).

| Write this | Not this |
|------------|----------|
| Serve a million viewers from one small server. | Unleash the power of decentralised video at scale. |
| Egress stays flat because peers carry the bytes. | Revolutionary bandwidth savings you have to see to believe. |
| Federation is on by default. Turn it off per channel. | Seamlessly connect with the wider fediverse ecosystem. |
| Install it yourself. It is AGPL v3. | Join a movement that is putting creators back in control. |
| Upload failed: the file is 4.2 GB and this instance allows 2 GB. | Oops! Something went wrong. Please try again later. |

- **No emoji.** Not in the product (CI-enforced), not in the docs, not on social. Icons
  are drawn glyphs.
- **You, not we.** The reader runs the instance: "you install", "your instance", "your
  viewers". Vidra is the thing, not the protagonist.

## 06 — Messaging

**The line (chosen 2026-08): "Run your own video platform."** It is the shortest true
sentence — the voice's own first principle — and leads on ownership, the reason people
self-host at all. It appears in the banner, site heroes, social bios and meta
descriptions, always with the full stop.

Two supporting lines back it up in longer formats (section heads, decks, docs intros);
they support, they never replace the line:

- **One small server. A million viewers.** — the hardest-to-match technical claim;
  concrete enough to be checked.
- **Video hosting you own, at egress you can afford.** — names the cost problem out
  loud; the most specific about who it is for.

**The paragraph.** Vidra is a federated video platform you install yourself, the way you
would install WordPress. One low-cost server serves thousands or millions of viewers
because egress is distributed rather than paid for. It federates over ActivityPub and
ATProto, stores media on IPFS if you want it to, and it is free software under AGPL v3.

**Three proof points.** Low egress at scale (peers and IPFS carry distribution) ·
Federated by default (ActivityPub and ATProto per channel, not bolted on) · Yours to run
(AGPL v3, one compose file, no vendor between you and your viewers).

**What Vidra is not:** not a hosted service, not a creator monetisation platform, and
not a PeerTube fork — it is a clean-room implementation. Say so plainly when asked.

## 07 — Imagery & layout

Show the product, or show nothing. No photography or illustration library exists; until
it does, the only sanctioned imagery is the interface itself: real screens, real
thumbnails, real terminal output. Stock photography of people at laptops is not part of
this brand.

- **Screens** sit on Ink or Paper with a 16px radius and no drop shadow. Crop to the
  region that proves the point; never show full browser chrome.
- **Video stills** from real videos on real instances, credited. Cool-toned and
  un-graded; no filters, no vignette, no cyan wash.
- **Grid**: 12 columns; 1080px max measure for text, 1280 for media; section padding
  96px desktop / 48 mobile.
- **Spacing**: a 4px base unit. Every gap, pad and offset on a brand surface is a multiple
  of it — 4 · 8 · 12 · 16 · 24 · 32 · 48 · 96 — and card corners take the 16px radius.
- **Rhythm**: long scroll, alternating Ink and Paper sections — never two Ink sections
  in a row.
- **Whitespace**: if a section feels empty, cut a sentence rather than adding a card.
- **Materials** (2026-08-28): brand surfaces are flat, with one exception — sticky
  navigation chrome may be glass (blurred, translucent Ink) under the conditions in
  [identity §7](../identity/identity-system.md#the-recognisable-elements): unconditional
  solid Ink fallback, translucency only inside `@supports (backdrop-filter: …)`,
  `prefers-reduced-transparency` and `prefers-contrast: more` force solid, Ink at
  ≥ 0.92 alpha (≥ 0.94 for a bottom bar). Glass in a content section is a defect.

## 08 — Misuse

- Don't recolour the mark. It has six colours and they are all fixed; no single-colour
  version exists yet.
- Don't put the mark in a circle, rounded square or badge — it has its own silhouette.
- Don't set cyan type on Paper below 20px. Use Action Cyan, or Ink.
- Don't gradient anything. The tri-protocol ribbon is the only gradient the brand owns,
  and it belongs to the product.
- Don't add an otter illustration, mascot pose or animal metaphor to the copy. The mark
  carries it; the words do not need to.
- Don't use indigo on a brand surface, or cyan as a button colour inside the app. That
  boundary is the whole colour system.

## 09 — Accessibility

Brand surfaces are held to the product's bar. Inside the product, WCAG 2.2 AA is enforced
in CI — axe serious and critical findings block the build — and everything outside the
product is checked against the same numbers at review.

- **Contrast.** Body text clears 4.5:1; large type and UI edges clear 3:1. Action Cyan
  `#0B7EA3` is the only cyan permitted under white text; Vidra Cyan and Deep Cyan are
  fills and large type only. Small cyan type on Paper darkens to `#0A6B8C`.
- **Focus.** Every interactive element shows a visible 2px focus ring with a 2px offset:
  Action Cyan on Paper, Ice on Ink. Removing the ring, or replacing it with a colour
  change alone, is a defect.
- **Motion.** Transitions run 150ms for fills and 200ms for lifts and never exceed 300ms.
  Everything honours `prefers-reduced-motion`, including scroll behaviour.

  **The ambient exception (2026-08-28).** An infinite ambient animation may ship only
  with a written argument — recorded where the animation lives — for why a ≤ 300ms
  one-shot cannot say the same thing. Two exist, both on vidra-site: `vd-pulse`, a 2.4s
  opacity loop on the hero version dot (its whole message is "this release is current"),
  and `vd-dash`, a 1.1s travelling dash on the federation figure's live wires (direction
  of flow, which a static dashed line cannot express). Both are ambient, carry no
  information that is not also in adjacent text, and **stop dead under
  `prefers-reduced-motion`** — as must any successor. A third instance needs its
  paragraph written first.
- **Never colour alone.** A state carries a glyph or a word as well as a colour. The
  do/don't badges in the interactive edition are drawn check and cross vectors, not
  colour swaps and not dingbat characters.

## 10 — Comparison surfaces

Vidra positions itself against alternatives, so comparisons will keep being made — in
tables, decks, READMEs. This is how the brand makes one (pattern codified 2026-08-28
from the site's shipped `Comparison` component, its reference implementation). The test
it must survive: being read by someone who works at the thing in column one.

- **Columns of checkable prose.** Every cell is a sentence the reader can verify or an
  admission that it varies ("Varies by project. Check the one you are comparing.").
  **No ticks, no crosses, no scores, no ratings** — the reader can do the arithmetic,
  and a checkmark grid is the competitor-page cliché this brand does not make.
- **Admissions of parity and concessions stay in.** Where Vidra matches the other
  self-hosted options, the table says so rather than inventing a difference; where an
  alternative is ahead, the cell says that too. The concessions are what make the rest
  of the table believable.
- **Emphasis, never colour alone.** The Vidra column is marked three ways at once:
  heading in Vidra Cyan, a quiet fill behind the column, and last position. The other
  columns are not marked down — secondary text, not strikeouts.
- **Competitor columns carry a visible verification date**, in the surface itself, not
  a footnote page: "PeerTube column checked against PeerTube's own documentation,
  v8.2.4, August 2026." A comparison without a date is a claim about the past wearing
  present tense.
- Voice rules apply with no discount: say the number, use the real term, and every
  competitor cell is sourced from their documentation, not from memory.

## Known gaps

No single-colour or reversed **mark** (the logotype is single-colour by nature; the
otter is not), and no photography library. Each is a decision waiting to be made, not
an oversight — tracked in the
[governance decision log](../governance/governance.md#decision-log).

These guidelines now also ship as an interactive document —
[`portal/index.html`](../portal/index.html), which replaced the old download portal in
v1.1. The markdown here stays canonical; the page renders it.
