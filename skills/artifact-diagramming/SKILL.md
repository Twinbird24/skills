---
name: artifact-diagramming
description: Focused, accessible SVG diagrams for real technical mechanisms and decisions.
license: MIT
---

# Artifact diagramming

Create a diagram only when it lets a reader understand a mechanism or decision more quickly than prose. If a sentence or small table is clearer, use that instead.

## Decide what to show

Start with the one question the diagram should answer: where data goes, how a request changes state, which boundary is crossed, or what differs between options. Use verified or supplied facts; do not invent components or relationships to make a diagram look complete.

Draw the mechanism, not a labeled inventory. Show the paths, reads, writes, invalidations, retries, branches, queues, ownership, and failures that matter. Label arrows with the actual action. For a comparison, keep the shared context aligned and make the meaningful difference visually explicit.

Match scope to the decision. Prefer one figure with one claim; split an overview from a detailed flow rather than cramming both into one drawing. Keep labels short and put explanatory sentences in the caption or surrounding prose.

## Build the diagram

Prefer a clean, hand-authored inline SVG when the destination supports it. Use native SVG shapes, text, paths, and markers—never Mermaid, external images, JavaScript, runtime libraries, or decorative complexity.

- Set a content-sized `viewBox` and let the SVG scale responsively (for example, `max-width: 100%; height: auto`). Use left-to-right layouts for flows and top-to-bottom layouts for layers or branching.
- Use `currentColor` for strokes, text, and arrowheads so the diagram works in light and dark themes. Reserve accent color for a meaningful distinction, and never make color the only carrier of meaning.
- Use `defs` and a diagram-specific marker id for arrowheads. Keep all references within the SVG fragment.
- Align nodes to a simple grid with even gaps and shared baselines. Use clear hierarchy, not ornament, to emphasize the path or difference that matters.
- Keep text legible at the rendered size and labels to a few words. Avoid `foreignObject`, embedded styles or scripts, and long decorative path data.

Wrap standalone SVGs in a `figure` when the host permits it. Give the SVG `role="img"` and a meaningful `aria-label`; add a `figcaption` when it helps state the diagram's claim. Ensure the surrounding text still communicates the essential conclusion.

## Check before delivery

Confirm that the diagram has one main idea, every arrow describes a real operation, all relevant success/failure or state paths are visible, and no box, label, boundary, or accent exists merely as decoration. Render or preview it when possible; simplify until the mechanism reads at a glance.
