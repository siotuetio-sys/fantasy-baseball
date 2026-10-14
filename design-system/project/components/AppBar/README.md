# AppBar

The navy app bar that opens every screen: brandmark, title, live-update time, a date picker and a refresh button.

**Markup:** `header.appbar` > `.brandmark` (the brandmark SVG at 38px), a block with `h1` (wrap the word Fantasy in `span.baseball`) and `span.sub` tagline, `span.spacer`, `span.updated`, a `label` wrapping `input.datepick[type=date]`, and an `.iconbtn`.

**Consumer provides:** title text, the tagline, the last-updated string, the date value and the refresh handler.

- Ground is `navbg`; title `on-dark` in `app-title`; captions `navmut`.
- Inside the bar, `.datepick` and `.iconbtn` switch to a translucent white fill (12%) with a 22% white border.
- Below 680px: padding 11px 14px, title 15px, hide `.sub`.
- Don't put a second orange element in the bar; the brandmark and the word Fantasy carry it.
