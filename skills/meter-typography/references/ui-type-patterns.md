# UI Type Patterns

Recurring product UI situations — set them once, reuse everywhere.

## Labels & metadata

| Element | Size | Weight | Case |
| --- | --- | --- | --- |
| Form label | `body` or `caption` | 500 | Sentence |
| Helper text | `caption` | 400 | Sentence |
| Section label | `caption` | 600 | ALL CAPS + tracking |
| Timestamp | `caption` | 400 | Tabular nums, muted color |

**Avoid:** ALL CAPS body copy. **Avoid:** labels smaller than 11px effective (zoom users).

## Tables

- Header row: `caption` or `body`, weight 600, not larger than cell text
- Numeric columns: right-align + tabular nums
- Truncation: `text-overflow: ellipsis` with `title` tooltip or expand on click — never truncate without affordance

## Buttons

- One size step above adjacent body when button is primary action
- Don't shrink button text below 14px
- Icon + label: icon optically aligned (often 1px nudge up)

## Dense vs marketing

| Surface | Strategy |
| --- | --- |
| App shell | Fewer sizes, tighter leading |
| Marketing | Display family, fluid hero, generous leading |
| Empty states | One heading step + one body step — resist the third size |

## Accessibility

- User font scaling must not break layout — use `rem`, test at 200% zoom
- `line-height` ≥ 1.5 for paragraphs (WCAG advisory)
- Don't convey state by color alone — pair with weight or icon
