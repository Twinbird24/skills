---
name: design
description: Design and implement distinctive, production-ready user interfaces. Use for new screens, flows, or material UI redesigns; not for narrow mechanical UI fixes with no visual-direction work.
license: MIT
---

# Design

Build an intentional product experience, not a generic AI-styled interface. Work in this order: **understand → explore → choose → implement → render → critique → refine → simplify**. Treat the user's taste feedback as a durable design constraint.

## Discover

Before implementation, understand the product, audience, primary task, content, technical constraints, and the feeling the interface should create. Inspect the existing product and its design system first; preserve its patterns, tokens, and interaction conventions unless the request calls for a redesign.

For substantial new UI, explore two or three genuinely different directions before converging. Vary composition, hierarchy, density, typography, imagery, material, and interaction—not merely colors. If the brief is vague, use an unexpected but relevant source of inspiration or a constrained creative prompt to escape familiar defaults. Use visual references to identify principles worth adapting, never to copy an interface.

## Define

Choose the direction that best serves the product and the user's stated or demonstrated taste. State a short internal brief covering the intended feeling and the decisive visual choices: layout, hierarchy, type, palette/materials, imagery or motion, and interaction character. Commit to that direction and make the details reinforce it.

## Deliver

Implement the direction with real content, clear hierarchy, semantic structure, responsive behavior, accessible interaction, and maintainable components. Use imagery, custom assets, image generation, or motion when they materially strengthen the concept; do not replace a missing visual idea with easy CSS decoration. Keep assets performant, provide appropriate fallbacks, and respect reduced-motion preferences.

For substantial visual work, run the UI and inspect rendered screenshots at representative viewports and states. Do not judge the result from code alone.

When useful, use a bounded critic loop:

1. Capture the current UI and give a fresh reviewer the screenshot, the intended direction, and relevant visual references—not the implementation rationale.
2. Ask for the few highest-impact gaps in composition, hierarchy, character, and polish, plus concrete improvements.
3. Implement the worthwhile feedback, render again, and stop after one or two loops unless evidence shows further iteration is converging.

Prefer a separate agent or fresh context for criticism when available; it should evaluate the outcome, not defend earlier choices.

## Simplify and polish

Before finishing, remove anything that does not clarify content, support interaction, establish hierarchy, or reinforce the chosen direction. Be especially skeptical of excessive gradients or glows, nested cards, pills everywhere, decorative graphics without a job, redundant labels, filler copy, and needless visual effects. These patterns are not forbidden—they must earn their place.

Keep the final result usable, accessible, responsive, performant, and coherent with the product. A smaller number of decisive elements is usually stronger than a screen full of decoration.
