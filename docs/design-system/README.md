# Design System Foundations

Single source of truth for Tymeline Customer Experience Platform design tokens.

Documentation structure follows hierarchical, versioned specs inspired by mature open hardware documentation practices such as [OpenTitan](https://github.com/lowRISC/opentitan) — clear IDs, tables, and change history — adapted here for UI design tokens rather than silicon IP.

## Token domains

| Domain | Status | Spec |
| --- | --- | --- |
| Color palette | Planned | — |
| **Typography** | **Draft v1.0.0** | [`typography/TYPOGRAPHY-SCALE.md`](./typography/TYPOGRAPHY-SCALE.md) |
| Spacing | Planned | — |
| Icons | Planned | — |

## Typography package

| Artifact | Description |
| --- | --- |
| [`typography/TYPOGRAPHY-SCALE.md`](./typography/TYPOGRAPHY-SCALE.md) | Hierarchy, sizes, weights, line-heights, accessibility |
| [`typography/typography.tokens.json`](./typography/typography.tokens.json) | Machine-readable tokens |
| [`typography/typography.tokens.css`](./typography/typography.tokens.css) | CSS custom properties + utilities |
| [`typography/diagrams/typography-hierarchy.svg`](./typography/diagrams/typography-hierarchy.svg) | Visual scale diagram |
| [`typography/preview.html`](./typography/preview.html) | Interactive specimen for review |

### Approved families (brand assets)

- **Fraunces** — brand / display (`--serif`)
- **Inter** — product UI / body (`--sans`)
- **JetBrains Mono** — overlines, code, meta (`--mono`)

Source: live brand CSS on [tymeline.app](https://tymeline.app/).
