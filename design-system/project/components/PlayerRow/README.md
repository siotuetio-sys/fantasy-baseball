# PlayerRow

One player in a roster or watch list; `PlayerChip` (`.pchip`) is the removable pill form.

**Markup:** `div.plist` > `div.prow` with `div` (`.nm` + `.meta`) and `div.rt` (a `RecBadge`, `button.act`, `button.rm` ×). Chips: `div.rosterbar` > `span.pchip` with the name and a `button` ×.

- Row: `panel`, `border` hairline, `radius-tile`. Name `player-name`; meta `caption` `muted`; × in `bad` with a 32px target.
- Chip: ink-outlined pill.
