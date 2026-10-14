# StatTile

A number with its label; the clickable `.kpi-link` variant jumps to the view that explains it.

**Markup:** `div.stat` > `div.v` (the value) + `div.k` (the label). Lay several in `.statbox` or a `.grid` with `minmax(150px,1fr)`. Add `.kpi-link` and `span.arrow` (›) for a shortcut tile; tint the value with `.tag-good` / `.tag-warn` / `.tag-bad`.

- `panel2`, 1px `border`, `radius-tile`, padding 10px 12px.
- Value `stat-value` with tabular numerals; label `caption` in `muted`.
- KPI tiles rise 2px with `shadow-lift` and an `accent2` border on hover.
