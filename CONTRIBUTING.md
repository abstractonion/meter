# Contributing to Meter

Meter is a growing library of visual craft skills for agents. Contributions add disciplines or deepen references — not workflow rules (that's [Cadence](https://github.com/abstractonion/cadence)).

## Adding a visual discipline

### 1. Create the skill directory

```
skills/meter-<discipline>/
├── SKILL.md
└── references/
    ├── <topic-1>.md
    ├── <topic-2>.md
    └── ...
```

### 2. Parent `SKILL.md` (~50–80 lines)

Include:

- YAML frontmatter: `name: meter-<discipline>` and a `description` with modern taste and culture framing + trigger terms
- 3–5 philosophy principles (taste angle)
- Routing table: task → `references/<file>.md`
- Brief culture note (historical tradition → modern UI)
- **"Read the reference BEFORE implementing"** — mandatory

### 3. References (2–4 for v1)

- Substantive craft content — original synthesis in meter's voice
- Do **not** paste third-party material verbatim; distill ideas into your own reference prose

### 4. Register the discipline

- Add row to routing table in `skills/meter/SKILL.md`
- Add row to discipline index in `README.md`
- Add to roadmap table in `docs/ARCHITECTURE.md` (move from "later" to "now")

### 5. Verify

```bash
npx skills add . -g --agent cursor -y
# Confirm new skill appears in agent skill list
```

## Naming

- Library router: `meter`
- Disciplines: `meter-<noun>` (e.g. `meter-typography`, not `meter-type`)
- Reference files: `kebab-case.md`, topic-named

## PR checklist

- [ ] Parent skill under ~80 lines
- [ ] References loaded on demand, not inlined in parent
- [ ] No broken relative paths
- [ ] README + library router updated
- [ ] Original writing in new references
