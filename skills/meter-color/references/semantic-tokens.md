# Semantic Tokens

Name colors by **job**, not appearance.

## Layer model

```
Primitive → Semantic → Component (optional)
```

**Primitives:** `--gray-1` … `--gray-12`, `--blue-9`, `--red-9`

**Semantics:** what the color *does*

| Token | Role |
| --- | --- |
| `--color-bg` | Page background |
| `--color-bg-subtle` | Recessed panels |
| `--color-bg-elevated` | Cards, popovers |
| `--color-fg` | Primary text |
| `--color-fg-muted` | Secondary text |
| `--color-border` | Default borders |
| `--color-border-strong` | Emphasis dividers |
| `--color-accent` | Primary actions |
| `--color-accent-fg` | Text on accent |
| `--color-danger` | Destructive |
| `--color-success` | Positive state |

Components reference semantics:

```css
.button-primary {
  background: var(--color-accent);
  color: var(--color-accent-fg);
}
```

When dark mode flips, only semantics remap — components stay untouched.

## Pair tokens

Every background token needs a tested foreground:

```
--color-bg-elevated + --color-fg
--color-accent + --color-accent-fg
--color-danger + --color-danger-fg
```

Document pairs in a token table or Storybook swatch page.

## State without new hues

Hover/active often need:

- `--color-accent-hover` (lower L or higher C)
- `--color-bg-hover` (slight L shift on neutral)

Don't invent a new hue per state — shift lightness/chroma on the same hue.

## Cadence alignment

`theme-tokens-only` means no raw hex in components. Meter defines *how* to choose primitive values; Cadence enforces *where* they appear in code.
