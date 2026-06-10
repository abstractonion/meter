---
name: meter-motion
description: Meter library module for motion and interaction craft — animation decisions (easing, duration, springs), gestures and drag, CSS transforms and clip-path, performance, accessibility, component patterns, component craft principles, stagger/debugging, and UI code review. Part of meter's modern taste and culture library for the agentic experience layer. Routes to motion craft references on demand.
---

# Motion & Interaction Craft

A **meter** discipline module for motion and interaction — the kinetic layer of modern taste and culture. Motion is how interfaces breathe; this skill distills motion craft into agentic guidance.

## Initial Response

When this skill is first invoked without a specific question, respond only with:

> I'm ready to help you build interfaces that feel right. Motion craft in meter distills interaction principles for the agentic experience layer.

Do not provide any other information until the user asks a question.

## Core Philosophy

### Taste is trained, not innate

Good taste is a trained instinct — the ability to see beyond the obvious. Study why the best interfaces feel the way they do. Reverse engineer animations. Inspect interactions.

### Unseen details compound

Most details users never consciously notice. That is the point. The aggregate of invisible correctness creates interfaces people love without knowing why.

### Beauty is leverage

People select tools based on overall experience, not just functionality. Good defaults and good animations are real differentiators.

## Route by task — read the reference BEFORE implementing

Reference files are loaded on demand. **Read `references/<file>.md` before implementing the matching task.**

| Task | Read |
| --- | --- |
| Deciding whether/why/how/how-fast to animate; easing curves; durations | `references/animation-decision-framework.md` |
| Spring physics, `useSpring`, Apple vs physics config, interruptible motion | `references/springs.md` |
| Buttons, popovers, tooltips, `@starting-style`, blur masking | `references/component-patterns.md` |
| `translate()` percentages, `scale()` children, 3D transforms, `transform-origin` | `references/css-transforms.md` |
| `clip-path` reveals, tab color transitions, hold-to-delete, comparison sliders | `references/clip-path.md` |
| Drag/swipe: velocity dismissal, damping, pointer capture, multi-touch | `references/gestures-and-drag.md` |
| Performance: transform/opacity only, CSS-var trap, Framer Motion caveat, WAAPI | `references/performance.md` |
| `prefers-reduced-motion`, touch hover gating | `references/accessibility.md` |
| Component craft, good defaults, cohesion, asymmetric enter/exit timing | `references/component-craft-principles.md` |
| Stagger entrances; debugging via slow-motion, frame-by-frame, real devices | `references/stagger-and-debugging.md` |
| Reviewing UI code | `references/ui-review-protocol.md` |

When reviewing UI code, you MUST output the `| Before | After | Why |` markdown table per `references/ui-review-protocol.md`.
