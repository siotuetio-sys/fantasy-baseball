# GameRow

A tappable line for one game: time or score, the teams, and state.

**Markup:** `button.gamerow` > `span.gtime` (or `span.gscore`), `span.gteams` (away, `span.at` @, home) and `span.gstate` (`.live` while in progress).

- `panel`, ink outline, `radius-row`; hover lifts 2px onto `pop-soft`. Score in `display`. Live state is bold `good` with words (7局上).
