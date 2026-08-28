# Vidra design system — the implementation layer

The reusable layer for the **product UI**: Apple HIG foundations, one accent, semantic
colour, and a navigation-layer glass material.

## Where it lives

| Artifact | Location | Role |
|----------|----------|------|
| **Browsable system** | [Claude Design](https://claude.ai/design) project **"Vidra Design System"** | Rendered cards for every token group and primitive — generate new designs against it so they stay consistent |
| **Source of truth** | [`vidra-user/app/globals.css`](https://github.com/yegamble/vidra-user) | The tokens the product actually ships |
| **Spec** | `vidra-user` `.ralph/specs/design-system.md` | The written contract |
| **Reference copy** | [`tokens.css`](tokens.css) | Snapshot of the semantic token sheet, kept in this repo for brand work |
| **Brand token sheet** | [`brand-tokens.css`](brand-tokens.css) | The other side of the boundary — brand surfaces only |

Where any two disagree, **the repo wins**.

## Two sheets, one boundary

[`tokens.css`](tokens.css) is the **product**: systemIndigo accent, `light-dark()` values,
glass material, the component contract. [`brand-tokens.css`](brand-tokens.css) is
**everything outside the product** — marketing, docs, decks, README art, email — and
carries the cyan palette, the brand type ramp, the 4px spacing scale and the 96/48 section
rhythm from the [brand guidelines](../guidelines/brand-guidelines.md). A surface imports
one or the other, never both: cyan never becomes an interactive colour in the app, and
indigo never appears on a brand surface. The seam is the sign-in screen.

## Principles

**Clarity** (type and spacing carry the hierarchy) · **Deference** (neutral chrome
defers to video — restraint, not absence) · **Depth** (hairline borders, quiet
elevation, a floating functional layer) · **Harmony** (radii nest concentrically).

## Hard rules

- **Mobile first** — 390px designed first; no horizontal overflow at 390 or 768.
- **Targets** — 44×44pt minimum on anything interactive.
- **Navigation** — no hamburger menus; tab bar below `sm`, sidebar above, one in the
  accessibility tree at a time.
- **Tokens only** — no hardcoded hex in components, no `dark:` variants; every value is
  defined once with `light-dark()` and switches on `color-scheme`.
- **Contrast** — WCAG 2.2 AA minimum; axe serious/critical is a hard CI gate and the
  authority on any token change.

## The material split

Two layers, two material families. **Glass** (translucent, blur 24 / saturate 1.35
regular, blur 12 / 16% fill clear) is the functional layer: header, sidebar, tab bar,
player chrome, floating pills. **Standard** (opaque surfaces, hairline borders) is the
content layer: cards, panels, grouped rows, sheet bodies. Glass in the content layer is
a review defect, glass always degrades to solid under Reduce Transparency / Increase
Contrast / forced colours.

## Component inventory

Button · IconButton · Chips (filter + navigation, never mixed) · Segmented control ·
Toggle · Checkbox · Radio · Field · Textarea · Badge · Avatar · Skeleton · VideoCard ·
Grouped rows · Empty state · IconTile · Modal (dialog + sheet) · Dropdown (portal +
fixed) · Tabs · Toast · Card · Spinner · ErrorState · LoadMoreButton · ProtocolRibbon.

Every primitive is bespoke, token-driven, and carries its own accessibility contract —
do not fork these patterns locally.

## Accessibility contract

One focus-ring recipe (2px surface gap + 2px accent ring, keyboard-only) · the subtle
foreground token carries no meaning · glass degrades to solid · icons are SVG from the
41-glyph set, never emoji (CI-enforced) · one `main` landmark and one primary nav in
the tree per page · accessible names are asserted in tests and never change in a
restyle.
