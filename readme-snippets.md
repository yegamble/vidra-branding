# README snippets

Copy-paste blocks that put the brand on every Vidra repo. Assets are hot-linked from
this repo's `main`, so fixes here propagate everywhere without touching the other repos
again.

> Raw base URL: `https://raw.githubusercontent.com/yegamble/vidra-branding/main/`

## Meta repo (`vidra`) — hero banner

```html
<p align="center">
  <img src="https://raw.githubusercontent.com/yegamble/vidra-branding/main/assets/readme/banner.svg"
       alt="Vidra — run your own video platform" width="100%">
</p>
```

## Component repos (`vidra-core`, `vidra-user`, `vidra-search`) — header

Mark above the title; the repo name stays the `<h1>` so GitHub search/SEO is unaffected:

```html
<p align="center">
  <a href="https://github.com/yegamble/vidra">
    <img src="https://raw.githubusercontent.com/yegamble/vidra-branding/main/assets/logo/vidra-icon.svg"
         width="72" alt="Vidra">
  </a>
</p>
```

For example, `vidra-core`'s README would begin:

```markdown
<p align="center">
  <a href="https://github.com/yegamble/vidra">
    <img src="https://raw.githubusercontent.com/yegamble/vidra-branding/main/assets/logo/vidra-icon.svg" width="72" alt="Vidra">
  </a>
</p>

# vidra-core

Backend / HTTP API for [Vidra](https://github.com/yegamble/vidra), a federated video
platform you install yourself.
```

## Any repo — footer credit

```html
<p align="center">
  <a href="https://github.com/yegamble/vidra">
    <img src="https://raw.githubusercontent.com/yegamble/vidra-branding/main/assets/readme/powered-by-vidra.svg"
         height="28" alt="powered by Vidra">
  </a>
</p>
```

## Rules

- The banner belongs on the **meta repo and brand surfaces**; component repos get the
  mark, not the full hero — the repo's own name leads (instance-lockup logic).
- Don't inline copies of the SVGs into other repos; hot-link so governance stays here.
- Alt text is required and factual (see
  [voice rules](guidelines/brand-guidelines.md#05--voice)).
- No shields.io colour badges in Vidra colours — status badges stay their default
  colours; the brand doesn't tint third-party UI.
