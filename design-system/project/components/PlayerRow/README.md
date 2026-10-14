# PlayerRow

One player in a roster or watch list: name, meta, verdict and actions. `PlayerChip` (`.pchip`) is the compact removable form.

**Markup:** `div.plist` > `div.prow` holding `div` (`.nm` name + `.meta` line), then `div.rt` with a `RecBadge`, `button.act` and/or `button.rm` (×). Chips: `div.rosterbar` > `span.pchip` with the name and a `button` ×.

**Consumer provides:** the player, the meta line (team · position · key stat) and handlers.

- Row `panel2`, 1px `border`, `radius-tile`, padding 8px 11px, gap `space-10`; rows stack `space-6` apart.
- Name `player-name`; meta `caption` `muted`. Remove × is `bad`.
