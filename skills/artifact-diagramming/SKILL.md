---
name: artifact-diagramming
description: Clear, editable technical diagrams for real mechanisms and decisions.
license: MIT
---

# Artifact diagramming

Create a diagram only when it lets a reader understand a mechanism or decision more quickly than prose. If a sentence or small table is clearer, use that instead.

## Decide what to show

Start with the one question the diagram should answer: where data goes, how a request changes state, which boundary is crossed, or what differs between options. Use verified or supplied facts; do not invent components or relationships to make a diagram look complete.

Draw the mechanism, not a labeled inventory. Show the paths, reads, writes, invalidations, retries, branches, queues, ownership, and failures that matter. Label arrows with the actual action. For a comparison, keep the shared context aligned and make the meaningful difference visually explicit.

Match scope to the decision. Prefer one figure with one claim; split an overview from a detailed flow rather than cramming both into one drawing. Keep labels short and put explanatory sentences in the caption or surrounding prose.

## Build the diagram

Use Mermaid by default for flowcharts, architecture and infrastructure diagrams, request lifecycles, sequence diagrams, state diagrams, ER diagrams, and similar technical visuals. Use another tool only when it clearly communicates the particular idea better.

- Write clean Mermaid source with short labels, explicit arrow actions, and a simple hierarchy. Prefer clear structure over encoding every detail; split a complex system into multiple focused diagrams when it improves comprehension.
- Render the Mermaid with available tooling, preferably to SVG (or PNG when appropriate), and keep the `.mmd` source beside the rendered file so it remains editable. Use responsive output and make the essential meaning available in nearby prose or a caption.
- Visually inspect the rendered diagram. Revise its layout, direction, grouping, labels, or scope if it is cluttered, ambiguous, or poorly arranged.

When the host supports it, provide a meaningful accessible label and caption. Ensure the surrounding text still communicates the essential conclusion.

## Check before delivery

Confirm that the diagram has one main idea, every arrow describes a real operation, all relevant success/failure or state paths are visible, and no box, label, boundary, or accent exists merely as decoration. Simplify until the mechanism reads at a glance.
