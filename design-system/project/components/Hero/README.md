# Hero

The lemon block that opens the dashboard: greeting, the day's question, the H2H score with a quip, actions, and the coach mascot with a speech bubble.

**Markup:** `section.hero` > `.hero-copy` (`p.sticker` greeting, `h2.hero-title` with the key words in `u`, `.hero-score` holding `button.hero-num > span` and `p.hero-quip`, `.pillrow` of buttons and a date `span.pill`) and `.hero-art` (`div.bubble` + `img` of `mascot-coach.svg`).

**Consumer provides:** the greeting for the time of day, the score, a quip that matches the matchup state, the bubble text (live start/sit counts), and handlers.

- `pop` ground, `radius-hero`, no outline. The score is `hero-num`; the title `hero-title` with a paper highlighter stripe under the `u` words.
- One hero per app, on the dashboard only.
- Below 680px: one column, the mascot centred under the copy at 290px.
