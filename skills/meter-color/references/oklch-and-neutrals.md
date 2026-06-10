# OKLCH & Tinted Neutrals

Build palettes humans perceive as even steps — not hex lottery.

## Why OKLCH

OKLCH separates **lightness (L)**, **chroma (C)**, and **hue (H)** in perceptual space. Interpolating `oklch(60% 0.1 250)` → `oklch(90% 0.1 250)` keeps hue stable; hex `#666` → `#eee` drifts muddy.

```css
--gray-9: oklch(35% 0.02 260);
--gray-1: oklch(97% 0.01 260);
```

Same hue (260 = cool blue-gray) across the ramp — **tinted neutrals**.

## Building a neutral ramp

1. Pick a hue for your brand temperature (warm: 60–80, cool: 250–270, neutral: 0.01 chroma)
2. Hold chroma low (0.01–0.03) for grays; raise chroma only for accents
3. Step lightness in ~8–12% jumps for 9–11 steps
4. Name `1` lightest (background) → `12` darkest (text on light bg) — match your token convention

## Accent from the same hue family

Accent that shares neutral hue feels cohesive:

```
Neutrals: oklch(... 0.02 260)
Primary:  oklch(55% 0.18 260)  /* same hue, higher chroma */
```

Complementary accents (orange + blue) are loud — reserve for marketing, not chrome.

## Migration from hex

1. Convert existing brand hex → OKLCH (oklch.com or `color-mix`)
2. Rebuild ramp in OKLCH native
3. Snapshot critical pairs for regression (text on surface contrast)

## Anti-patterns

- `#808080` center of ramp — no tint, no character
- Identical L steps with wildly different chroma — uneven perceived weight
- 20-step gray scale nobody can distinguish — 9–11 steps is enough
