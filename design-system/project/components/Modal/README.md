# Modal

A centered sheet for a detailed breakdown, such as a matchup's factor list.

**Markup:** a fixed backdrop (`scrim`, 16px padding) containing `div.modal` > `div.mhead` (title + `button.mclose` ×) and `div.mbody`. Factor lines are `div.frow` with `.fl` (label, `small` note) and `.fdelta` (signed number tinted `good`/`bad`).

**Consumer provides:** open/close state, Escape and backdrop-click to close, focus management.

- `panel`, 1px `border`, `radius-modal`, `shadow-modal`, max 580px wide and 88vh tall; the head stays sticky while the body scrolls.
