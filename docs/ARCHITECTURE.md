# Meter Library Architecture

## What meter is

**Meter** distills **modern taste and culture** into the **agentic experience layer** — craft sensibility, design traditions, and contemporary product constraints that agents apply in inflight user/AI collaboration.

Where **Cadence** governs *how* you work (investigate → propose → implement → review → test → ship → reflect), **meter** governs *how it should feel* when the work is visual — motion, type, color, composition, and future visual disciplines.

| Pillar | Role in meter |
| --- | --- |
| **Taste** | Trained instinct for what elevates — not personal whim, but practiced discernment |
| **Culture** | Design traditions (Swiss grids, Bauhaus color, Humanist type) resonating into modern UI |
| **Meter** | The agentic layer — skills an agent loads mid-session to season implementation with craft |

## Repository layout

```
meter/
├── docs/
│   └── ARCHITECTURE.md          # This file — library design & roadmap
├── skills/
│   ├── meter/                   # Library entry router (thin index)
│   ├── meter-motion/            # Motion & interaction craft
│   ├── meter-typography/        # Type rhythm, scale, pairing
│   ├── meter-color/             # Color systems, contrast, dark mode
│   ├── meter-composition/       # Layout hierarchy, whitespace, scannability
│   └── meter-<discipline>/      # Future visual modules
├── README.md
├── CONTRIBUTING.md
└── .cursor-plugin/
    └── plugin.json              # Optional Cursor manifest (skills-only)
```

## Skill naming convention

| Pattern | Purpose |
| --- | --- |
| `meter` | Library router — routes to the right discipline skill |
| `meter-<discipline>` | One visual craft domain per directory |
| `references/<topic>.md` | Depth lives here; parent SKILL.md stays ~50–80 lines |

**Frontmatter:** Each skill has `name` matching the directory and a `description` with modern taste and culture branding plus natural-language trigger terms agents match against.

## Parent router vs references

Follow the Cadence router + references split pattern:

1. **Parent `SKILL.md`** — philosophy (3–5 principles), discipline positioning within meter, routing table ("read reference BEFORE implementing"), no deep tutorials.
2. **`references/`** — substantive craft content loaded on demand. Agent MUST read the matching reference before implementing.
3. **Cross-skill routing** — `skills/meter/SKILL.md` lists all disciplines; discipline skills do not duplicate each other's references.

## Visual disciplines roadmap

### Now (v0.2 library)

| Skill | Scope |
| --- | --- |
| `meter` | Library index router |
| `meter-motion` | Animation, springs, gestures, performance, UI review |
| `meter-typography` | Scale, rhythm, pairing, optical corrections |
| `meter-color` | OKLCH tokens, tinted neutrals, contrast, dark mode |
| `meter-composition` | Hierarchy, whitespace, editorial grids → app UI |

### Later (scaffold only — not in repo yet)

| Skill | Scope |
| --- | --- |
| `meter-iconography` | Stroke weight, optical sizing, metaphor discipline |
| `meter-imagery` | Photography tone, illustration cohesion, empty states |
| `meter-data-viz` | Chart craft, label density, color semantics in graphs |
| `meter-accessibility-visual` | Beyond motion a11y — focus, contrast, cognitive load |

Non-visual disciplines (copy voice, sound, haptics) are out of scope until the visual library is stable.

## Relationship to Cadence

| Project | Layer | Analogy |
| --- | --- | --- |
| **Cadence** | Workflow & stack conventions | The kitchen pass — order, timing, hygiene |
| **meter** | Taste & visual craft | The seasoning — what makes the plate memorable |

Meter skills complement Cadence rules (`theme-tokens-only`, `react-compiler`) without replacing them. When both apply, Cadence wins on workflow; meter wins on craft judgment within visual work.

## Install & discovery

```bash
npx skills add abstractonion/meter
# or local dev:
npx skills add /path/to/meter -g --agent cursor -y
```

Each `skills/<name>/SKILL.md` is discovered independently. The `meter` router skill loads when users ask for taste, polish, or visual craft broadly; discipline skills load on specific triggers (animation, typography, color, layout).

## Adding a new discipline

See `CONTRIBUTING.md`. Summary: create `skills/meter-<discipline>/` with parent router + 2–4 reference files, register in `skills/meter/SKILL.md` and `README.md`, keep parent under ~80 lines.
