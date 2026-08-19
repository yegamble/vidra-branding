<p align="center">
  <img src="assets/readme/banner.svg" alt="Vidra — run your own video platform" width="100%">
</p>

# vidra-branding

The brand home for [Vidra](https://github.com/yegamble/vidra) — a clean-room, federated
video platform anyone can self-host. Everything that makes something *look and sound like
Vidra* lives here: the rules, the reusable pieces, and the approved assets.

| Pillar | Where | What it covers |
|--------|-------|----------------|
| **Brand guidelines** | [`guidelines/brand-guidelines.md`](guidelines/brand-guidelines.md) | The rules: the mark, lockups, colour, typography, voice, messaging, imagery, do/don't |
| **Design system** | [`design-system/`](design-system/README.md) | The reusable implementation layer for the product UI: tokens, components, accessibility contract |
| **Brand identity system** | [`identity/identity-system.md`](identity/identity-system.md) | The complete visual language — what makes everything recognisably Vidra |
| **Brand governance** | [`governance/governance.md`](governance/governance.md) | How changes are proposed, reviewed and approved; the decision log; usage by instance operators |
| **Brand portal** | [`portal/index.html`](portal/index.html) | One page to grab approved logos, colours, snippets and guidelines |

## The one rule to know

**Cyan outside the product, indigo inside it.** The otter mark's cyan (`#22BDE3`) leads
everywhere people *read about* Vidra — marketing, docs, decks, social, this repo. The
product interface keeps its verified systemIndigo accent. Cyan never becomes an
interactive colour inside the app; indigo never appears on a brand surface. The handoff
happens at the sign-in screen.

## Using the brand in repo READMEs

Ready-to-paste blocks for every Vidra repo are in
[`readme-snippets.md`](readme-snippets.md). Assets are hot-linked from this repo, so a
banner fix here propagates everywhere:

```html
<p align="center">
  <img src="https://raw.githubusercontent.com/yegamble/vidra-branding/main/assets/readme/banner.svg"
       alt="Vidra — run your own video platform" width="100%">
</p>
```

## Where the design system is authored

The living, browsable design system is a [Claude Design](https://claude.ai/design)
project (**"Vidra Design System"**) — token sheets, materials, type ramp and every
component primitive as rendered cards, so new designs can be generated consistently
against it. The in-product source of truth is
[`vidra-user/app/globals.css`](https://github.com/yegamble/vidra-user); this repo carries
a reference copy in [`design-system/tokens.css`](design-system/tokens.css).

## Layout

```
assets/       logo/ (icon, lockups) · readme/ (banner, powered-by badge)
guidelines/   brand-guidelines.md
design-system/  README.md · tokens.css
identity/     identity-system.md
governance/   governance.md
portal/       index.html
readme-snippets.md
```

## License

Documentation and templates: [CC BY-SA 4.0](LICENSE). The Vidra name and the otter mark
identify the Vidra project and are excluded — see
[`governance/governance.md`](governance/governance.md#using-the-marks) for usage rules.
