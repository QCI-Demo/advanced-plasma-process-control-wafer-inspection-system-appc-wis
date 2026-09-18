# Typography Scale — Tymeline Customer Experience Platform

| Field | Value |
| --- | --- |
| Document ID | `DS-TYPE-001` |
| Version | `1.0.0` |
| Status | Draft — Design System Foundation |
| Project | Tymeline Customer Experience Platform |
| Story | Establish Design System Foundations |
| Epic | Design System & UI/UX Delivery |
| Related tokens | [`typography.tokens.json`](./typography.tokens.json), [`typography.tokens.css`](./typography.tokens.css) |
| Diagram | [`diagrams/typography-hierarchy.svg`](./diagrams/typography-hierarchy.svg) |
| Brand source | Approved typefaces from [tymeline.app](https://tymeline.app/) brand CSS (`--serif`, `--sans`, `--mono`) |
| Doc convention reference | [OpenTitan documentation style](https://github.com/lowRISC/opentitan) — hierarchical markdown, versioned specs, explicit tables |

This document is the single source of truth for typographic hierarchy used by UI components (dashboard, activity timeline, task management, and related product surfaces).

---

## 1. Approved font families (brand assets)

Extracted from the live brand stylesheet on tymeline.app (Google Fonts load + CSS custom properties).

| Role token | Family | Fallback stack | Brand CSS var | Approved weights |
| --- | --- | --- | --- | --- |
| `font.family.serif` | **Fraunces** | `Georgia, 'Times New Roman', serif` | `--serif` | 400, 500, 600 (+ italic 400/500) |
| `font.family.sans` | **Inter** | `-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` | `--sans` | 400, 500, 600, 700 |
| `font.family.mono` | **JetBrains Mono** | `'SF Mono', Menlo, Consolas, monospace` | `--mono` | 500, 600, 700 |

### Role mapping

| Context | Primary family | Notes |
| --- | --- | --- |
| Marketing / brand display headings | Fraunces | Optical-size aware; italic accents allowed for brand emphasis |
| Product UI headings (dense screens) | Inter | Prefer sans for scannability in dashboards and tables |
| Body, forms, navigation, buttons | Inter | Default UI face |
| Captions, meta, timestamps | Inter or JetBrains Mono | Mono for system/status labels; sans for helper text |
| Overlines, eyebrows, code, IDs | JetBrains Mono | Uppercase + tracking for short labels only |

### Licensing & loading

- Source: Google Fonts CDN (brand site) or self-hosted WOFF2 for production CX apps.
- Prefer `font-display: swap`.
- Subset Latin (+ required app locales) to limit CLS.
- Do **not** introduce alternate display faces without brand approval.

---

## 2. Type scale — size, weight, line-height

Base root size: **16px** (`1rem`). All product tokens are rem-based so users’ browser zoom and OS text scaling apply (WCAG 1.4.4).

### 2.1 Product UI scale (CX platform)

Use this scale for dashboard, timeline, tasks, settings, and dialogs.

| Token | Semantic role | Family | Size | Weight | Line-height | Letter-spacing | Example use |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `text.display.sm` | Soft brand title in-app | Fraunces | 2rem / 32px | 500 | 1.15 (36.8px) | −0.02em | Empty-state headline |
| `text.heading.xl` | Page title (H1) | Inter | 2rem / 32px | 600 | 1.25 (40px) | −0.02em | “Activity timeline” |
| `text.heading.lg` | Section title (H2) | Inter | 1.5rem / 24px | 600 | 1.30 (31.2px) | −0.015em | Panel headers |
| `text.heading.md` | Subsection (H3) | Inter | 1.25rem / 20px | 600 | 1.35 (27px) | −0.01em | Card group titles |
| `text.heading.sm` | Card / list title (H4) | Inter | 1.125rem / 18px | 600 | 1.40 (25.2px) | −0.01em | Task title |
| `text.body.lg` | Emphasized body / lede | Inter | 1.125rem / 18px | 400 | 1.65 (29.7px) | 0 | Intro copy |
| `text.body.md` | Default body | Inter | 1rem / 16px | 400 | 1.50 (24px) | 0 | Descriptions, paragraphs |
| `text.body.sm` | Compact body | Inter | 0.875rem / 14px | 400 | 1.50 (21px) | 0 | Dense tables, secondary |
| `text.label.md` | Control label | Inter | 0.875rem / 14px | 500 | 1.40 (19.6px) | 0.01em | Form labels |
| `text.label.sm` | Chip / tab label | Inter | 0.75rem / 12px | 600 | 1.35 (16.2px) | 0.02em | Tabs, filters |
| `text.caption.md` | Caption / helper | Inter | 0.75rem / 12px | 400 | 1.45 (17.4px) | 0.01em | Field help, footnotes |
| `text.caption.sm` | Micro caption | Inter | 0.6875rem / 11px | 400 | 1.45 (15.95px) | 0.01em | Non-essential meta only |
| `text.overline` | Eyebrow / category | JetBrains Mono | 0.6875rem / 11px | 600 | 1.30 (14.3px) | 0.14em | Section overline (short) |
| `text.code.md` | Inline / block code | JetBrains Mono | 0.875rem / 14px | 500 | 1.50 (21px) | 0 | IDs, snippets |
| `text.code.sm` | Compact mono | JetBrains Mono | 0.75rem / 12px | 500 | 1.45 (17.4px) | 0.02em | Timestamps, hashes |

### 2.2 Marketing / brand display scale

Use on promotional surfaces, onboarding heroes, and stakeholder decks — not inside dense data UI.

| Token | Family | Size | Weight | Line-height | Letter-spacing |
| --- | --- | --- | --- | --- | --- |
| `text.brand.display.xl` | Fraunces | `clamp(2.625rem, 5.4vw, 4.75rem)` (42–76px) | 500 | 1.02 | −0.028em |
| `text.brand.display.lg` | Fraunces | `clamp(2rem, 3.8vw, 3.25rem)` (32–52px) | 500 | 1.08 | −0.024em |
| `text.brand.display.md` | Fraunces | 1.5rem / 24px | 500 | 1.25 | −0.018em |
| `text.brand.display.sm` | Fraunces | 1.375rem / 22px | 500 | 1.25 | −0.015em |
| `text.brand.lede` | Inter | 1.0625rem / 17px | 400 | 1.70 | 0 |

Italic Fraunces (400/500) is reserved for brand emphasis words — never for long paragraphs.

### 2.3 Weight vocabulary

| Token | Numeric | Typical use |
| --- | --- | --- |
| `font.weight.regular` | 400 | Body, captions |
| `font.weight.medium` | 500 | Labels, Fraunces display, mono body |
| `font.weight.semibold` | 600 | UI headings, buttons, overlines |
| `font.weight.bold` | 700 | Rare emphasis; nav wordmarks; avoid for long copy |

### 2.4 Line-height tokens

| Token | Value | Apply to |
| --- | --- | --- |
| `font.lineHeight.tight` | 1.15 | Display / short headings |
| `font.lineHeight.snug` | 1.25–1.35 | UI headings |
| `font.lineHeight.normal` | 1.40–1.45 | Labels, captions |
| `font.lineHeight.relaxed` | 1.50 | Default body (**minimum for paragraphs**) |
| `font.lineHeight.loose` | 1.65–1.70 | Lede / long-form reading |

---

## 3. Accessibility considerations (legibility)

Aligned with **WCAG 2.2 Level AA** (and Text Spacing 1.4.12 where practical).

### 3.1 Minimum sizes

| Content | Minimum | Rationale |
| --- | --- | --- |
| Primary body copy | **16px / 1rem** | Reliable reflow at 200% zoom; matches brand UI body floor |
| Secondary / table body | **14px** | Allowed in dense layouts if contrast ≥ 4.5:1 and line-height ≥ 1.5 |
| Captions / helper | **12px** | Floor for essential UI text |
| Decorative / non-essential chrome | 11px | Must not be the only way to convey information |
| Touch target labels | ≥ 12px inside ≥ 44×44px targets | Pair with spacing tokens |

### 3.2 Contrast (pairs with color palette)

- Normal text (< 18px / < 14px bold): contrast ratio **≥ 4.5:1** against background.
- Large text (≥ 18px regular or ≥ 14px bold): **≥ 3:1**.
- Placeholders and disabled text must not be the sole cue for required fields.
- Do not set body text in low-contrast mute colors (`ink-mute` / equivalent) for primary content.

### 3.3 Spacing & reflow (WCAG 1.4.12 / 1.4.4 / 1.4.10)

When users apply user stylesheets or OS settings, layouts must not clip when:

- Line height ≥ **1.5×** font size (body)
- Paragraph spacing ≥ **2×** font size
- Letter spacing ≥ **0.12×** font size
- Word spacing ≥ **0.16×** font size

Implementation notes:

- Prefer `rem` / `em` over fixed `px` in components.
- Avoid locking line-height in `px`; use unitless multipliers.
- Support **200% zoom** without loss of content or horizontal scrolling of essential text (except data tables with explicit overflow patterns).

### 3.4 Style practices for legibility

1. **Measure**: keep continuous reading width ≈ **45–75 characters** (≈ 60–75ch max for body).
2. **Case**: avoid all-caps for sentences; JetBrains Mono overlines may be uppercase for **≤ ~24 characters**.
3. **Tracking**: negative tracking only on large display sizes; never tighten body/caption.
4. **Italics**: Fraunces italic for short brand emphasis only; Inter body stays roman for readability.
5. **Weight**: do not use ultra-light weights; approved floor is 400.
6. **Icons + text**: do not replace essential labels with icon-only controls unless an accessible name is provided.
7. **Motion**: respect `prefers-reduced-motion` for any typed/animated text reveals.
8. **Language**: set `lang` on pages; use font features (`font-feature-settings: "tnum"` for tabular nums in timelines/tables).

### 3.5 Product-specific guidance

| Surface | Guidance |
| --- | --- |
| Dashboard KPIs | Fraunces or Inter semibold for numbers; mono for units/timestamps |
| Activity timeline | `text.body.sm` + `text.code.sm` for event meta; heading.sm for event titles |
| Task management | Task titles `text.heading.sm`; descriptions `text.body.md`; due dates mono caption |
| Forms | Labels `text.label.md`; errors `text.caption.md` with error color ≥ 4.5:1 |

---

## 4. Token delivery

| Artifact | Purpose |
| --- | --- |
| [`typography.tokens.json`](./typography.tokens.json) | DTCG-style design tokens for Figma / Style Dictionary / codegen |
| [`typography.tokens.css`](./typography.tokens.css) | CSS custom properties for web implementation |
| [`diagrams/typography-hierarchy.svg`](./diagrams/typography-hierarchy.svg) | Visual hierarchy for stakeholder review |

Downstream components must reference these tokens — not hard-coded font sizes — so the CX platform stays consistent with brand and AA requirements.

---

## 5. Change control

| Version | Date | Summary |
| --- | --- | --- |
| 1.0.0 | 2026-09-18 | Initial scale from approved Fraunces / Inter / JetBrains Mono brand assets |

Human design-system owners must approve changes that alter families, drop below the 12px essential-text floor, or weaken contrast pairing rules.
