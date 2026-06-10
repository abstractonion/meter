# Type Scale & Rhythm

Build scales that read consistently across breakpoints — not arbitrary pixel picks.

## Modular scale basics

A modular scale multiplies a base size by a ratio. Common ratios:

| Ratio | Character | Typical use |
| --- | --- | --- |
| 1.125 (Major second) | Tight, dense UI | Tables, admin |
| 1.2 (Minor third) | Balanced | General product UI |
| 1.25 (Major third) | Airy marketing | Landing pages |
| 1.333 (Perfect fourth) | Strong contrast | Editorial hero |

Pick **one ratio** for the product. Mixing ratios across pages breaks rhythm.

## Step naming (semantic, not `text-lg`)

Name steps by role, not Tailwind defaults:

```
--font-size-caption
--font-size-body
--font-size-body-emphasis
--font-size-subheading
--font-size-heading
--font-size-display
```

Map components to roles. When design changes, retoken — don't hunt 47 `text-sm` call sites.

## Vertical rhythm

Line-height should relate to the scale:

| Role | Line-height guidance |
| --- | --- |
| Body (14–16px) | 1.5–1.6 for paragraphs |
| UI labels (12–13px) | 1.4–1.5; single line often OK |
| Headings | 1.1–1.25; tighten as size grows |
| Display | 1.0–1.1; may need negative tracking |

**Baseline grid (optional):** Set `line-height` in px multiples of 4 (or 8) so stacked text aligns across columns. Worth it for marketing; often overkill for dense app chrome.

## Fluid type

For marketing, clamp between min and max:

```css
font-size: clamp(1.125rem, 0.9rem + 1vw, 1.5rem);
```

App UI rarely needs fluid body text — fixed steps reduce QA surface.

## Audit checklist

- [ ] No more than 6–7 distinct sizes in production UI
- [ ] Adjacent steps are visually distinguishable (≥1.125 ratio)
- [ ] Body line-length 45–75 characters for prose; narrower for sidebars
- [ ] Heading levels map 1:1 to semantic HTML (`h1`–`h6`)
