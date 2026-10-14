# Modal

A centred sheet for a detailed breakdown, like a matchup's factor list.

**Markup:** a fixed `scrim` backdrop holding `div.modal` > `.mhead` (title + round `button.mclose`) and `.mbody`; factor lines `div.frow` with `.fl` (label + `small`) and `.fdelta`.

**Consumer provides:** open/close state, Escape and backdrop click, focus management.

- `panel`, ink outline, `radius-card`, max 580px; ink rule under the head; deltas in `display`, tinted `good`/`bad`.
