---
name: meter-color
description: Meter library module for color craft — OKLCH palettes, tinted neutrals, semantic design tokens, contrast, dark mode. Modern taste and culture — period palettes and color symbolism distilled into modern product systems. Part of meter's agentic experience layer.
---

# Color Craft

A **meter** discipline module — the spectral layer. Color carries meaning before copy loads; historical palettes (Bauhaus primaries, Japanese iki, Art Deco metallics) inform how we build token systems without nostalgia cosplay.

## Core Philosophy

### Neutrals carry the product

Most surfaces are gray. Tinted neutrals (hue in the gray, not pure `#888`) make light and dark themes feel intentional. Pure gray feels like a wireframe that shipped.

### Semantics before decoration

`--color-danger` must work on every surface it touches. Decorative accent colors are the reward layer on top of a coherent semantic base.

### Perceptual uniformity wins

OKLCH (or LCH) keeps steps visually even. Hex interpolation lies; users feel the lie as "muddy mid-tones."

## Route by task — read the reference BEFORE implementing

| Task | Read |
| --- | --- |
| Building palettes; OKLCH steps; tinted neutrals | `references/oklch-and-neutrals.md` |
| Semantic tokens; surface/foreground/border roles | `references/semantic-tokens.md` |
| Contrast, WCAG, dark mode elevation | `references/contrast-and-dark-mode.md` |
| Culture-informed accent discipline; period → product | `references/culture-palettes.md` |

## Cadence overlap

When the project has `theme-tokens-only` (Cadence), meter color craft applies to *how* you choose token values — not whether you hardcode hex in components.
