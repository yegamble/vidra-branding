# Brand governance

How the Vidra brand stays coherent: who owns what, how changes land, and what is still
undecided.

## Ownership

| Surface | Authority | Enforced by |
|---------|-----------|-------------|
| Brand assets & guidelines (this repo) | Project maintainer (@yegamble) | PR review in `vidra-branding` |
| Product UI tokens & components | `vidra-user` design system | axe CI gate + e2e accessible-name assertions |
| Repo READMEs | Each repo, using [`readme-snippets.md`](../readme-snippets.md) | Hot-linked assets from this repo |
| Instance operators' theming | The operator | Design-system semantic tokens (supported surface) |

## Change process

1. **Propose** — open a PR against this repo. One decision per PR; say what breaks or
   changes downstream.
2. **Check the boundary** — any colour change is tested against the two boundary rules
   (cyan never interactive in-app; indigo never on a brand surface). Any in-product
   token change belongs in `vidra-user`, not here, and axe is the authority there.
3. **Version** — guidelines carry a version and date (currently **v1.1 · August 2026**).
   Breaking visual changes (mark, palette, lockups) bump the version; copy edits do not.
4. **Propagate** — assets are hot-linked from `main`, so merging is shipping. Renaming
   or moving an asset file is a breaking change: grep the org's READMEs first.

## Decision log

| Date | Decision | Status |
|------|----------|--------|
| 2026-08 | **Cyan outside the product, indigo inside it** — brand leads with the mark's cyan; the app keeps verified systemIndigo. Handoff at the sign-in screen. | **Decided** |
| 2026-08 | Tri-protocol ribbon: exactly three placements, product-owned | **Decided** |
| 2026-08 | **Logotype v1 drawn** — "Vidra" as fixed outlines from Inter Display Bold (SIL OFL) at −0.045em, kerned. Drawn form for logo placements; live system-face text remains for UI/inline use. | **Decided** |
| 2026-08 | **Positioning line: "Run your own video platform."** — shortest true sentence, leads on ownership. The other two drafts become supporting lines ([guidelines §06](../guidelines/brand-guidelines.md#06--messaging)). | **Decided** |
| 2026-08 | **Guidelines ship as an interactive document** — `portal/index.html` becomes the rendered edition of the guidelines (sticky contents, specimens, do/don't tiles, downloads) and replaces the static Brand Center. Markdown stays canonical; the page must stay build-free, system-stack and request-free. | **Decided** |
| 2026-08 | **Mist `#EEF7FB` added** as the quiet tint surface for cards and section grounds on Paper. Ice stays, as the saturated tint ([guidelines §03](../guidelines/brand-guidelines.md#03--colour)). | **Decided** |
| 2026-08 | **Accessibility section added** ([§09](../guidelines/brand-guidelines.md#09--accessibility)) — AA 4.5:1, Action Cyan the only cyan under white text, visible 2px focus ring, motion ≤300ms with `prefers-reduced-motion`, never colour alone. Matches the product's axe CI gate. | **Decided** |
| 2026-08 | **Figma Make proposals reviewed; format adopted, content rejections logged** — adopted: the single-page interactive format, a Foundation section, first-class accessibility rules, a documented spacing/radius rhythm, Mist. Rejected: Archivo / Inter / JetBrains Mono webfonts (the stack stays system, the logotype stays drawn); a lowercase live-text "vidra" wordmark; metaphor voice ("calm currents", otter mascot copy); water/stock photography; Deep Cyan `#16A3E2` as the interactive colour (Action Cyan `#0B7EA3` remains the only cyan under white text); the Abyss/Current/Splash/Foam palette rename (assets are hot-linked and names are shipped); Harbor `#18314F` (Slate and Ink already cover that range). See [guidelines v1.1](../guidelines/brand-guidelines.md). | **Decided** |
| 2026-08-28 | **Navigation-layer glass admitted on brand surfaces** — identity §7's "never appears on brand surfaces" is overturned in place (struck, with reasons) for the navigation layer only: sticky header and sticky bottom bar, under vidra-site's shipped conditions — unconditional solid Ink fallback, translucent ground only inside `@supports (backdrop-filter: …)`, `prefers-reduced-transparency` / `prefers-contrast: more` force solid, Ink alpha ≥ 0.92 (header) / 0.94 (bar) as a contrast floor, never in content. Why: sticky chrome over alternating grounds reads as a seam when opaque; HIG puts materials on the navigation layer and nowhere else; the product's own `.glass-chrome` rule draws the same line. From the 2026-08-28 vidra-site design audit. | **Decided** |
| — | Single-colour / reversed **mark** for engraving, embroidery, forced-colour contexts (the logotype is already single-colour) | Open |
| — | Photography / illustration library (interim rule: real product imagery only) | Open |

## Using the marks

The Vidra name and the otter mark identify the Vidra project. The software is AGPL v3;
the marks are not part of that grant.

- **Instances**: use the instance lockup ("powered by Vidra") to credit the platform.
  Your name leads; don't co-size. Don't imply your instance is officially operated by
  the Vidra project.
- **Forks**: ship under your own name and mark. Keep "compatible with Vidra" phrasing
  factual.
- **Press / community**: use the supplied assets unmodified; follow
  [guidelines §08 — Misuse](../guidelines/brand-guidelines.md#08--misuse).

## Review checklist (any brand artifact)

- [ ] Mark unmodified, clear space respected, approved background
- [ ] Cyan/indigo boundary intact
- [ ] Sentence case; two weights; no emoji; numbers over adjectives
- [ ] Text contrast clears WCAG AA (Action Cyan — never Vidra Cyan — under white text)
- [ ] No gradients; no stock photography; screens shown honestly
