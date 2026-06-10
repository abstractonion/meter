# Contrast & Dark Mode

Readable in both themes — not inverted light mode.

## Contrast targets

| Content | WCAG AA (minimum product bar) |
| --- | --- |
| Body text | 4.5:1 against background |
| Large text (≥18px regular / 14px bold) | 3:1 |
| UI components & graphics | 3:1 |
| Decorative | No requirement — don't put copy on it |

Test with DevTools contrast panel or APCA for large type — but ship AA at minimum.

## Dark mode is not `filter: invert`

Principles:

1. **Lower peak lightness** — pure white text on `#000` vibrates; use `oklch(93% ...)` for fg
2. **Elevate with lightness, not shadow** — dark UI surfaces: higher L = closer to user (`bg` < `elevated` < `popover`)
3. **Reduce chroma on large fields** — saturated dark blues fatigue; desaturate backgrounds
4. **Borders over shadows** — shadows disappear on dark; 1px `border` with low-contrast token

## Elevation scale (example)

| Level | Light mode | Dark mode |
| --- | --- | --- |
| Base | `gray-1` | `gray-1` (darkest) |
| Subtle | `gray-2` | `gray-2` |
| Card | `gray-2` + shadow | `gray-3` (lighter = elevated) |
| Popover | `gray-1` + shadow | `gray-4` |

Remap semantics in `@media (prefers-color-scheme: dark)` or `[data-theme="dark"]`.

## Focus rings

Focus indicators need 3:1 against **adjacent** colors, not just page bg. Use dedicated `--color-focus-ring` tested on accent, gray, and image backgrounds.

## Reduced transparency trap

`rgba(255,255,255,0.1)` on varied backgrounds fails contrast unpredictably. Prefer opaque semantic tokens.
