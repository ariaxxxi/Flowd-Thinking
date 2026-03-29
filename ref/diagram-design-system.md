# Flowd Diagram Design System

Source of truth: Figma file `80HD`, node `1154:1799`
Reference: https://www.figma.com/design/UfVYVYDJetggVnGNcKt9zx/80HD?node-id=1154-1799&t=r8n8YDXbQY5tgW9m-11

This spec is the house style for every diagram used in `flowd-case-study.html`. Future diagram SVGs should preserve this language unless a section explicitly needs a different visual system.

## 1. Visual Intent

These diagrams should feel calm, exact, and lightweight.

- White pill containers floating on a quiet field.
- Small, warm-gray section labels that feel editorial, not dashboard-like.
- Dotted connectors that suggest relation, sequence, and drift without becoming heavy arrows.
- One acid-lime accent used sparingly to mark the important node or shift in state.
- Layouts centered on the x-axis with generous breathing room and no decorative framing.

## 2. Core Tokens

### Color

- Pill fill: `#FFFFFF`
- Primary text and connector color: `#171613`
- Section label color: `#979186`
- Caption / secondary annotation color: `#7C766C`
- Neutral badge fill: `#E8E6DC`
- Accent badge fill: `#DFFF37`

### Shadow

- Pill shadow: `0 10px 20px 5px rgba(33, 33, 50, 0.05)`

### Typography

- Font family: `DM Sans`
- Pill label: `14px`, regular, color `#171613`
- Number inside badge: `12px`, regular, color `#171613`
- Section label: `12px`, regular, uppercase, color `#979186`
- Footer caption / diagram note: `12.5px`, regular, color `#7C766C`
- Minimum type size in final exported diagrams: `12px`. If a layout only works below `12px`, the layout must change.

## 3. Components

### Pill shell

- Height: `44px`
- Radius: `60px` pill radius
- Fill: white
- Shadow: use the standard pill shadow
- Default structure: left badge + text block

### Badge

- Size: `36px x 36px`
- Shape: circle
- Placement: inset `4px` from top and bottom, and `4px` from the left edge
- Variants:
  - Neutral numbered badge: warm-gray fill `#E8E6DC`
  - Neutral icon badge: warm-gray fill `#E8E6DC`
  - Accent icon badge: lime fill `#DFFF37`

### Inner icon

- Size: `19.4px x 19.4px`
- Fill: `#171613`
- Form: 9-dot cluster / spark mark
- Center the icon optically inside the badge, not mathematically low or high

### Connector

- Stroke: `#171613`
- Style: dotted
- Dash pattern: `1 3`
- Cap: round
- Weight: `1px`
- Use straight connectors by default; curved dotted connectors only when the diagram is explicitly about detour, loop, or seam

## 4. Layout Rules

### Horizontal rhythm

- Badge left inset must match the top inset. The left gap is not allowed to drift larger.
- Keep the gap from badge edge to text start at about `14px`.
- Keep right-side text padding optically balanced with the left-side inner spacing.

### Content-fit width

The Figma reference uses `130px` pills in the base example, but for this site the more important rule is content fit.

- Pill width must respond to its text content.
- A pill may expand or shrink to fit the label cleanly.
- Do not leave a conspicuously empty tail on the right just to preserve a uniform width.
- Do not let text approach the right edge or run outside the pill.
- Use `130px` as a reference rhythm, not a hard lock.

Practical formula:

- `pill width = 4 + 36 + 14 + text block width + 20`
- Increase the right padding when the pill is visually important or carries two lines.

### Diagram centering

- The whole graphic must be centered on the x-axis.
- Left and right whitespace should feel optically balanced.
- Do not let the diagram drift right because one label is longer.
- If a row has asymmetric content, recenter the full composition, not just the first row.

### Canvas bounds

- The SVG `viewBox` must include the full graphic, including shadows, captions, and curved connectors.
- Keep at least `16px` safe padding on every side.
- No outer frame should crop the right-most pill or the bottom-most dotted line.
- Diagrams should export on a transparent background unless the section explicitly calls for a filled field.

## 5. Variants

### A. Numbered process chain

Use for linear models, steps, or inherited tool flows.

- Neutral numbered badges
- One-line labels
- Dotted connectors between pills
- Section label aligned to the row, set in small uppercase

### B. Non-linear / generative chain

Use for bursts, fragments, connections, inspiration, or emergent relationships.

- Spark icon inside badge instead of a number
- Start with neutral badges
- Use lime on the key node, outcome, or new-state node
- Keep the connector language the same so the row still belongs to the same system

### C. Emphasis / outcome pill

This is a derived extension for the case study, based on the same Figma language.

- Same pill shell, shadow, and badge logic
- May grow wider than the base pills
- May carry a second line if needed
- If a second line is used:
  - Primary line remains `14px`
  - Secondary line should feel lighter and quieter
  - Keep the text block vertically centered
  - Increase pill height only as much as needed

## 6. Composition Rules

- Use at most one visual accent color per diagram.
- Prefer 1 to 2 rows. More rows usually weaken the calm editorial feel.
- Keep connector paths simple and legible.
- When showing failure or seam, use the dotted line as the storytelling device rather than adding arrows, boxes, or extra decoration.
- If a footer note exists, keep it light, centered, and separated from the main row by clear vertical space.

## 7. Implementation Rules For This Page

These rules are not optional. They address layout problems already seen in the case study.

- No text may overflow a pill.
- No pill should have meaningless extra width on the right.
- The graphic must never be cut off by the SVG bounds.
- The HTML wrapper must not crop the SVG with a forced placeholder ratio or `overflow: hidden`.
- The diagram image should render at intrinsic aspect ratio with `height: auto`.
- The final composition must be visually centered before export.
- No final exported diagram may use type smaller than `12px`.

## 8. QA Checklist

Before shipping any new diagram, check all of these:

- Text is fully inside every pill.
- Badge left inset matches the top inset.
- Right padding feels intentional, not arbitrary.
- The overall graphic is centered.
- The right edge is not clipped.
- The viewBox includes shadows and dotted endpoints.
- DM Sans is used consistently.
- No text falls below `12px`.
- Connector dot spacing is consistent.
- Only the intended node is accented lime.

## 9. What To Reuse Going Forward

Every future diagram for the case study should reuse this stack:

- White pill shell
- `44px` pill height
- `36px` badge
- DM Sans typography scale
- `#171613` dotted connector
- `#E8E6DC` neutral badge
- `#DFFF37` accent badge
- Soft floating shadow

If a new diagram needs a more complex layout, extend the composition, not the visual language.
