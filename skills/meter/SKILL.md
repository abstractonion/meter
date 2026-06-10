---
name: meter
description: Meter — modern taste and culture for the agentic experience layer. Distills modern visual craft and design traditions into skills agents load mid-session. Routes to visual discipline modules — motion, typography, color, composition. Use for UI polish, design taste, visual hierarchy, animation, type rhythm, color systems, layout craft, or when the user wants interfaces that feel right, not just work.
---

# Meter

**Modern taste and culture** — meter seasons inflight user/AI collaboration with visual craft sensibility. Not workflow (that's Cadence). Meter is the agentic layer where design traditions meet modern product constraints.

## What meter is

| Pillar | What it means here |
| --- | --- |
| **Taste** | Trained discernment — what elevates beyond "good enough" |
| **Culture** | Period craft resonating forward (Swiss grids, Humanist type, Bauhaus color) |
| **Meter** | The skill set agents load to apply both in implementation |

## Route by discipline — load the matching skill

When the task is visual, route to the discipline skill and **read its references before implementing**.

| Discipline | Skill | Triggers |
| --- | --- | --- |
| Motion & interaction | `meter-motion` | animation, easing, springs, gestures, drag, transitions, micro-interactions, UI review |
| Typography | `meter-typography` | type scale, font pairing, kerning, leading, widows, tabular nums, optical rhythm |
| Color | `meter-color` | OKLCH, semantic tokens, tinted neutrals, contrast, dark mode, palette |
| Composition & layout | `meter-composition` | hierarchy, whitespace, grid, scannability, cardlessness, visual anchor |

Each discipline skill lives at `skills/meter-<discipline>/SKILL.md` with depth in `references/`.

## When to use meter vs Cadence

- **Cadence** — how to work: propose-then-implement, verify-with-runtime, clean commits.
- **meter** — how it should *feel*: craft judgment on visual output.

Both can apply in the same session. Cadence wins on process; meter wins on taste.

## Library scope (now)

Visual disciplines only. Motion, typography, color, and composition ship in v0.2. Iconography, imagery, and data-viz are roadmap — see `docs/ARCHITECTURE.md`.
