# DataTable

Stat table for leaderboards, transactions and H2H categories.

**Markup:** `table` with `th` heads; numeric columns get `.num`; a section break is `tr.grouprow`; the user's own players are `tr.mine`. Wrap in a scroll container (`.tscroll`) or, for a phone card layout, add `.rtable` and a `data-l` label on each `td`.

- 13px cells, padding 9px 10px, 1px `border` rules; heads `th` style in `muted`; row hover `hover`.
- Numbers right-aligned with tabular numerals. Better-than-opponent values can be tinted `good`, worse `bad`.
- Below 680px a plain table keeps a 520px min width and scrolls; `.rtable` becomes one `panel2` card per row with secondary cells (`td.det`) behind an accordion.
