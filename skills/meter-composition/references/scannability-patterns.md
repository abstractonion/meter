# Scannability Patterns

Users scan, they don't read. Design for the glance, then the deep read.

## Cardlessness

Cards bundle padding + border + shadow. Ask: would a **section heading + spacing** suffice?

| Use cards | Skip cards |
| --- | --- |
| Draggable/reorderable items | Static settings groups |
| Distinct clickable destinations | Sequential form sections |
| Heterogeneous content types | Homogeneous lists |

Card soup — 12 identical boxes on a dashboard — hides hierarchy. Try one list with row dividers.

## List row anatomy

```
[Leading icon/avatar] [Primary label + secondary line] [Trailing meta/action]
```

- Primary: one line, weight 500
- Secondary: caption, muted, one line max
- Trailing: align right; tabular nums for numbers

## Dashboard hierarchy

1. **Hero metric** — one number, large, top-left or center
2. **Supporting KPIs** — 3–4 max in a row
3. **Detail tables/charts** — below fold

Ten equal KPI cards = no story.

## Tables vs cards on mobile

Wide tables → horizontal scroll with sticky first column, or card-per-row transformation. Don't squeeze 8 columns into 320px.

## Visual anchors

Repeat one anchor element per section:

- Icon in consistent slot
- Colored left border on active nav item
- Avatar column in team lists

Anchors speed re-orientation when scrolling back up.

## Progressive disclosure

Show scan layer first; detail on expand. Accordion, "Show more", side panel — match complexity to frequency of need.
