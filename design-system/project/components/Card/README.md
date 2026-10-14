# Card

The white container every tool lives in.

**Markup:** `div.card`. For a full-bleed table use `style="padding:0;overflow:hidden"`.

**Consumer provides:** a `SectionHeading`, controls, and content.

- `panel`, 1px `border`, `radius-card`, `shadow-card`, padding `space-14`.
- A heading row is `.row` with `justify-content:space-between; flex-wrap:wrap` — heading left, action or `Legend` right.
- Don't nest cards; recess inner groups with `panel2` tiles or rows instead.
