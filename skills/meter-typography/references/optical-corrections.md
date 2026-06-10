# Optical Corrections

Mathematical equality ≠ visual equality. Adjust tracking, leading, and figures for the eye.

## Tracking (letter-spacing)

| Context | Tracking |
| --- | --- |
| Body text | `0` or `0.01em` — don't track body by default |
| ALL CAPS labels | `+0.04em` to `+0.08em` — caps need air |
| Small caps | `+0.06em` |
| Large display (48px+) | `-0.02em` to `-0.04em` — tighten |
| Dense tables | `0` on numbers; avoid tracking numerals |

## Leading (line-height)

Widows and orphans: single lines stranded at column top/bottom. Fixes:

- `text-wrap: balance` on headings (progressive enhancement)
- `hyphens: auto` for long prose (with `lang` attribute)
- Slightly increase `max-width` or reduce font size — don't solve with `&nbsp;` hacks in CMS content

## Tabular figures

Financial data, timers, and tables need **tabular nums** so columns align:

```css
font-variant-numeric: tabular-nums;
/* or */
font-feature-settings: "tnum";
```

Proportional figures in a price column cause jitter on update — a motion problem disguised as typography.

## Kerning in UI

Browser kerning is usually sufficient. Manual kerning matters for:

- Logotypes
- Hero display lines in Figma → export as SVG for lockups only

Don't kern individual UI strings in code.

## Weight illusion

At equal pixel size, **Geist looks lighter than Inter**. When switching families, re-audit the weight scale — don't assume `font-weight: 500` maps 1:1.
