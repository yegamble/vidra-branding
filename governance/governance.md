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
3. **Version** — guidelines carry a version and date (currently **v1 · August 2026**).
   Breaking visual changes (mark, palette, lockups) bump the version; copy edits do not.
4. **Propagate** — assets are hot-linked from `main`, so merging is shipping. Renaming
   or moving an asset file is a breaking change: grep the org's READMEs first.

## Decision log

| Date | Decision | Status |
|------|----------|--------|
| 2026-08 | **Cyan outside the product, indigo inside it** — brand leads with the mark's cyan; the app keeps verified systemIndigo. Handoff at the sign-in screen. | **Decided** |
| 2026-08 | Tri-protocol ribbon: exactly three placements, product-owned | **Decided** |
| — | Drawn logotype (wordmark is currently system type) | Open |
| — | Single-colour / reversed mark for engraving, embroidery, forced-colour contexts | Open |
| — | Positioning line (three drafts in [guidelines §06](../guidelines/brand-guidelines.md#06--messaging)) | Open |
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
