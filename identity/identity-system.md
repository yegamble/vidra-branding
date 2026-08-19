# Vidra brand identity system

The complete visual and verbal language — the small set of elements that makes a landing
page, a README, a deck and the product itself recognisably belong to the same project.

## The recognisable elements

1. **The otter mark.** The only drawn asset. Six fixed colours, its own silhouette,
   never modified. If one thing identifies Vidra, it is this.
2. **The cyan family on Ink.** Vidra Cyan `#22BDE3` on Ink `#0C2136` is the brand's
   signature pairing — used for rules, dots, fills and large display type on every
   brand surface.
3. **The drawn logotype.** "Vidra" as fixed vector outlines (v1, from Inter Display
   Bold at 700 / −0.045em, kerned) for logo placements — identical on every platform
   and in print. Inline and UI text still sets "Vidra" live in the system face at the
   same weight and tracking, so the two forms read as one voice: native, unthemed,
   installed — like the software.
4. **The colour boundary.** Cyan outside the product, systemIndigo inside it. The
   sign-in screen is the seam. Seeing indigo tells you that you are *in* the product;
   seeing cyan tells you that you are *reading about* it.
5. **Paper `#F5F5F7`.** The one colour shared across the boundary — the brand's light
   ground is the product's canvas, which makes the handoff feel continuous rather than
   jarring.
6. **The tri-protocol ribbon** (`#6364FF → #0085FF → #65C2CB`). Product-owned, exactly
   three placements (header wordmark, Network hero divider, federated badge top edge).
   It is the only gradient in the whole identity, which is what keeps it legible as
   "federation" rather than decoration.
7. **The glass material.** Inside the product, navigation and player chrome float on a
   translucent glass layer above opaque content. It is the product's depth signature and
   never appears on brand surfaces.
8. **The voice.** Plain, factual, confident, precise. Numbers over adjectives, "you"
   over "we", no emoji anywhere.

## How the layers fit

| Layer | Governed by | Accent | Face |
|-------|------------|--------|------|
| Marketing, docs, social, print | [Brand guidelines](../guidelines/brand-guidelines.md) | Vidra Cyan / Action Cyan | System stack, brand ramp (64/44/22/17) |
| Product interface | [Design system](../design-system/README.md) | systemIndigo | System stack, HIG ramp (34…12) |
| Operator instances | Instance lockup rules | The operator's own | The operator's own |

## The federated identity problem

Vidra is software other people run. The identity system is designed so that an
operator's brand can lead without Vidra disappearing:

- The **instance lockup** ("powered by Vidra", mark at 14px, muted 13px type) is the
  sanctioned way an instance credits the platform. The operator's name always leads.
- Operators may theme their instance; the design system's semantic tokens are the
  supported surface for that. The otter mark and the Vidra name stay as shipped.
- Federation identity (ActivityPub / Bluesky / IPFS) is expressed through the
  protocol dot-badges and the ribbon — *inside the product only* — so protocol colour
  never competes with either the operator's brand or Vidra's.

## Asset index

| Asset | File | Use |
|-------|------|-----|
| Mark | [`assets/logo/vidra-icon.svg`](../assets/logo/vidra-icon.svg) | Favicon, app icon, avatars, anywhere |
| Logotype (drawn, v1) | [`assets/logo/vidra-logotype.svg`](../assets/logo/vidra-logotype.svg) | Logo placements — banners, headers, decks, print |
| Horizontal lockup | [`assets/logo/vidra-lockup-horizontal.svg`](../assets/logo/vidra-lockup-horizontal.svg) | Headers, docs, decks |
| Stacked lockup | [`assets/logo/vidra-lockup-stacked.svg`](../assets/logo/vidra-lockup-stacked.svg) | Square placements, avatars |
| README banner | [`assets/readme/banner.svg`](../assets/readme/banner.svg) | Repo README heroes |
| Powered-by badge | [`assets/readme/powered-by-vidra.svg`](../assets/readme/powered-by-vidra.svg) | Instance credits, README footers |
