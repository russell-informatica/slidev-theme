# slidev-theme-seconde

A [Slidev](https://sli.dev) theme for the **Informatica 2c** deck: flat,
Zed-inspired surfaces, soft borders and shadowed cards.

It packages everything visual that used to live in the deck repo:

- design tokens (`--c-*`, `--slidev-theme-primary`) for light and dark mode;
- global styles for tables, code blocks, `<kbd>`, callouts/alerts, `.box`,
  `.badge` and `.eyebrow`;
- the persistent `global-top.vue` topic kicker and `global-bottom.vue` footer;
- the bundled fonts (iA Writer Quattro + Fira Code) and their defaults.

## Usage

```md
---
theme: slidev-theme-seconde
addons:
  - slidev-addon-seconde
---
```

The theme can be consumed as a local path (`theme: ./theme`) or, as in the
deck repo, as an npm git dependency:

```json
{
  "dependencies": {
    "slidev-theme-seconde": "github:russell-informatica/slidev-theme-seconde"
  }
}
```

## Development

```bash
npm install
npm run dev        # opens example.md with `theme: ./`
```
