# Whitespace & Density

Space is a design material — allocate it like color or type.

## Spacing scale

Use a modular spacing scale (4px base common):

```
4, 8, 12, 16, 24, 32, 48, 64, 96
```

**Rule:** Adjacent sections differ by ≥1 scale step. `16px` gap between cards + `16px` section margin = flat rhythm.

## Density modes

Products serving power users may offer density toggle:

| Mode | Padding | Type | Use |
| --- | --- | --- | --- |
| Comfortable | 16–24px | body | Default |
| Compact | 8–12px | caption/body | Tables, IDEs |

Implement via data attribute on root — remap spacing tokens, don't fork components.

## Ma (間) — intentional void

Japanese concept of meaningful emptiness. Between major sections, **one generous gap** (48–64px) beats many hairline dividers. The void says "new thought starts here."

## When to add a divider

Try in order:

1. More space between groups
2. Background color shift (`bg` → `bg-subtle`)
3. 1px border
4. Card wrapper

Most UIs stop at step 2.

## Vertical rhythm in sections

Standard section anatomy:

```
[Section label / eyebrow]  — caption, muted
[Heading]                  — 8px below label
[Body or content]          — 16px below heading
[Actions]                  — 24px below content
```

Consistent section anatomy across pages trains scan patterns.
