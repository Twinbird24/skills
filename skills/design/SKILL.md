---
name: design
description: "Intentional, production-ready UI design: explore distinct directions, then implement, inspect, refine, and simplify."
license: MIT
---

# Design

Build an intentional product experience, not a generic AI-styled interface. For substantial or open-ended work, use: **understand → diverge → present 3+ directions → user chooses → develop → implement → render → critique → refine → simplify**. Treat the user's taste feedback as a durable constraint.

Skip presenting directions only for a small local change, when the user has already supplied a clear direction, or when they explicitly ask you to choose and proceed autonomously.

## Understand and diverge

Before code, understand the product, audience, primary task, content, constraints, and intended feeling. Inspect an existing product's design system first; preserve its patterns, tokens, and interaction conventions unless the request calls for a redesign.

For work that needs exploration, create at least three directions with short memorable names and concise descriptions. Each needs a recognizable design thesis and must differ in several meaningful choices: composition, typography, density, hierarchy, visual language, imagery, interaction, motion, or tone. A palette swap, font swap, radius tweak, hero reversal, or superficial theme variation is not a separate direction.

Push past the first familiar ideas. Deliberately explore contrasts appropriate to the product—such as editorial versus utilitarian versus expressive, dense versus spacious, or ordered versus asymmetric. Include one bolder, non-obvious option when appropriate, without making every option experimental. Draw conceptual inspiration from beyond SaaS interfaces: print, architecture, industrial design, fashion, games, physical products, photography, art, signage, or packaging. Adapt principles, never copy an example. If the options still feel predictable, introduce an external or random creative seed to widen the search, then judge the result on its merits.

## Present, choose, and develop

Proactively present the directions before implementing and ask the user which to pursue. If the user explicitly delegates the choice, select the strongest direction and state why.

After selection, write a short internal brief covering the intended feeling and decisive choices—layout, hierarchy, type, materials, imagery or motion, and interaction character. Stop blending unrelated ideas from the discarded directions; optimize the chosen thesis for coherence and execution quality.

## Implement, inspect, and refine

Implement with real content, clear hierarchy, semantic structure, responsive behavior, accessible interaction, and maintainable components. Use imagery, custom assets, image generation, or motion when they materially strengthen the chosen concept; do not substitute easy CSS decoration for a visual idea. Keep assets performant and respect reduced-motion preferences.

For substantial visual work, render and inspect representative viewports and states; do not judge from code alone. When useful, run a bounded critic loop: give a fresh reviewer the screenshot, intended direction, and relevant references—not implementation rationale—then address only the highest-impact gaps. Render again and stop after one or two loops unless the work is clearly converging.

## Simplify and polish

Remove anything that does not clarify content, support interaction, establish hierarchy, or reinforce the chosen direction. Be skeptical of excessive gradients or glows, nested cards, pills everywhere, decorative graphics without a job, redundant labels, filler copy, and needless effects. These are not forbidden; they must earn their place.

Keep the final result usable, accessible, responsive, performant, and coherent. A smaller number of decisive elements is usually stronger than a screen full of decoration.
