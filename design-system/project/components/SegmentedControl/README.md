# SegmentedControl

A row of mutually exclusive options: date ranges, hitter/pitcher, day windows.

**Markup:** `div.seg` > `button` per option; the chosen one gets `.on`.

- `panel2` track with 1px `border`, `radius-btn`, clipped corners.
- Options 12.5px/600 `muted`, min height 38px; the selected option is `accent` with `on-dark` text.
- Keep options short and parallel: 整季 / 近 30 天 / 近 14 天 / 近 7 天.
