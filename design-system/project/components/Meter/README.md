# Meter

A thin bar for a 0–100 score such as a Statcast percentile or matchup rating.

**Markup:** `div.meter` > `span` with `style="width:NN%"`. Put the number beside it; the bar alone is not the value.

- 7px tall, `panel2` track, `radius-sm`; fill is a `bad → warn → good` gradient so the bar's end color reads as the grade.
- For a single-color percentile bar use `good` (80+), `pct-fair` (60–79), `warn` (40–59), `bad` (<40).
