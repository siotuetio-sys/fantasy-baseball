# AppBar

The paper app bar: brandmark, PERFECT DRAFT wordmark with its tagline, update time, date field and a lemon refresh button.

**Markup:** `header.appbar` > `.brandmark` (`assets/Logos/brandmark.svg` at 40px), `.wordmark` (`h1` + `span.sub`), `span.spacer`, `span.updated`, `input.datepick.pill-field[type=date]`, `button.iconbtn.pop` with the refresh icon.

**Consumer provides:** the update time, date value and refresh handler.

- `bg` ground with a `line` bottom rule. Wordmark in `wordmark`; tagline 你的夢幻棒球軍師 in `muted`.
- The refresh button is the bar's only lemon.
- Below 680px: 34px mark, 21px wordmark, hide the tagline, update time and date label.
