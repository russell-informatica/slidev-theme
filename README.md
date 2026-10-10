# slidev-theme-russell

A [Slidev](https://sli.dev) theme for the decks in the
[`russell-informatica`](https://github.com/russell-informatica) organization:
flat, Zed-inspired surfaces, soft borders and shadowed cards.

It packages everything visual that used to live in the deck repos:

- design tokens (`--c-*`, `--slidev-theme-primary`) for light and dark mode;
- a single-direction vertical rhythm: every block carries `--flow` of space
  *above* it only (`--flow-tight` binds a heading to its content,
  `--flow-loose` before a section heading). Nothing carries a bottom margin,
  so the first/last block of any container is flush and grid/flex/centred
  layouts need no per-layout fixes;
- global styles for tables, code blocks, `<kbd>`, callouts/alerts, `.box`
  and `.eyebrow`;
- component theme tokens for the [`slidev-addons-russell`](../addons) components;
- the persistent `global-top.vue` topic kicker and `global-bottom.vue` footer;
- the bundled fonts (iA Writer Quattro + Fira Code) and their defaults.

## Usage

```md
---
theme: slidev-theme-russell
addons:
  - slidev-addons-russell
---
```

The theme can be consumed as a local path (`theme: ./theme`) or, as in the
deck repos, as an npm git dependency:

```json
{
  "dependencies": {
    "slidev-theme-russell": "github:russell-informatica/slidev-theme"
  }
}
```

## Development

```bash
npm install
npm run dev        # opens example.md with `theme: ./`
```
