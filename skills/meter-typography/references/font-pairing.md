# Font Pairing

Pair families that share intent — not just contrast for its own sake.

## The two-family rule

Most products need exactly two families:

1. **UI / body** — highly legible at small sizes, full character set, variable weight axis preferred
2. **Display (optional)** — personality for heroes and marketing; can be serif or geometric display

Adding a third family needs justification (monospace for code is the usual exception).

## Pairing strategies

| Strategy | Body | Display | Vibe |
| --- | --- | --- | --- |
| Grotesk + Grotesk | Inter, Geist | Söhne, Helvetica Now Display | Neutral product |
| Humanist + Serif display | Source Sans 3 | Fraunces, Newsreader | Warm editorial |
| Geometric + Mono accent | DM Sans | — | Technical, dev tools |
| System stack | `system-ui` | — | Maximum performance |

## Variable fonts

Prefer variable fonts when available:

- One file, many weights — fewer FOUT/FOIT issues
- Fine-tune `font-weight: 550` for "between medium and semibold"
- `font-variation-settings` for optical size on display cuts

## Loading discipline

```html
<link rel="preload" href="/fonts/inter-var.woff2" as="font" type="font/woff2" crossorigin>
```

- Subset to Latin + required scripts
- `font-display: swap` for body; `optional` only if system fallback is acceptable
- Never load 6 weights of 6 families — users pay the latency tax

## Anti-patterns

- Display face in 12px table cells
- Two grotesks that look identical (Inter + Roboto)
- Script or blackletter anywhere near forms
- faux bold (`font-weight: 700` when only 400 is loaded)
