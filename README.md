# Meter

**Modern taste and culture** for the agentic experience layer.

Meter distills modern visual craft and design traditions into skills agents load mid-session — seasoning inflight user/AI collaboration so interfaces don't just work, they *feel* right.

Where [Cadence](https://github.com/abstractonion/cadence) governs *how* you work, meter governs *how it should look and move*.

## What meter is

| Pillar | What it is |
| --- | --- |
| **Taste** | Trained discernment — what elevates beyond "good enough" |
| **Culture** | Period craft resonating forward (Swiss grids, Humanist type, Bauhaus color) |
| **Meter** | The skill library agents load to apply both in implementation |

## What's in it

Visual discipline skills — each a thin router (`SKILL.md`) with depth in `references/`:

| Discipline | Skill | Focus |
| --- | --- | --- |
| Library router | `meter` | Routes to the right discipline |
| Motion & interaction | `meter-motion` | Animation, springs, gestures, UI review |
| Typography | `meter-typography` | Scale, rhythm, pairing, optical corrections |
| Color | `meter-color` | OKLCH, semantic tokens, contrast, dark mode |
| Composition | `meter-composition` | Hierarchy, whitespace, grid, scannability |

See `docs/ARCHITECTURE.md` for roadmap (iconography, imagery, data-viz) and design decisions.

## Install

```bash
npx skills add abstractonion/meter
```

Local development:

```bash
npx skills add /path/to/meter -g --agent cursor -y
```

### Cursor

Install via the skills CLI above, or point Cursor's plugin flow at this repo if using `.cursor-plugin/plugin.json`.

Each `skills/<name>/SKILL.md` is discovered independently. The `meter` router loads on broad taste/polish requests; discipline skills load on specific triggers (animation, typography, color, layout).

## Relationship to Cadence

| Project | Layer |
| --- | --- |
| **Cadence** | Workflow — propose, verify, ship, reflect |
| **meter** | Visual craft — taste and culture in the agentic layer |

Meter complements Cadence rules like `theme-tokens-only` and `react-compiler` without replacing them.

## Contributing

Add a visual discipline: see `CONTRIBUTING.md`.

## License

MIT — see repository root for license terms.
