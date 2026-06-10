# Grid & Alignment

Invisible structure users feel as "professional" without naming it.

## Column grid

| Context | Columns | Gutter |
| --- | --- | --- |
| Marketing | 12 | 24–32px |
| App content | 12 or 8 | 16–24px |
| Dense admin | 8 | 12–16px |
| Sidebar layout | Main 8–9 + rail 3–4 | Fixed sidebar width |

Use CSS Grid or framework grid — **same grid** across pages in a section.

## Alignment discipline

Pick edges and stick to them:

- **Left edge** of text blocks aligns across sections
- **Baselines** align in horizontal toolbars (icon + label)
- **Right edge** for numeric columns and trailing actions

Misalignment by 4–8px reads as "bug" not "quirky."

## Breakpoints change structure, not just scale

| Breakpoint | Composition shift |
| --- | --- |
| Mobile | Single column; stack sidebar below or drawer |
| Tablet | 2-column where desktop has 3 |
| Desktop | Full grid; optional max-width container (`1200–1280px`) |

Don't only shrink font — reflow the story.

## Container max-width

Long line lengths kill prose readability. Cap content:

```css
.content { max-width: 65ch; } /* prose */
.page { max-width: 1280px; margin-inline: auto; } /* app shell */
```

Full-bleed hero + constrained body is a valid editorial pattern.

## Optical alignment

Icons in buttons: often need 1px vertical nudge. Carets in selects: align to cap height, not box center. Trust screenshot review.
