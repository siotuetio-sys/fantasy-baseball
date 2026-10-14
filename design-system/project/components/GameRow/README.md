# GameRow

A tappable line for one game in the schedule: time, the two teams, and state.

**Markup:** `button.gamerow` > `span.gtime`, `span.gteams` (away, `span.at` @, home — with team logos when available), and `span.gstate`; add `.live` while in progress. Show `span.gscore` in place of the time once a game has a score.

- `panel`, 1px `border`, `radius-tile`, grid `50px 1fr auto`; hover rises 2px with `shadow-lift` and an `accent2` border.
- Live state is `good` and bold, with a word (LIVE / 7局上).
