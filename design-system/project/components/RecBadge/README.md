# RecBadge

The app's verdict on a player for today: START, SIT, STREAM or GRAB.

**Markup:** `span.rec.START` / `.SIT` / `.STREAM` / `.GRAB` with the word in caps as its text.

- 13px/800, `radius-sm`, padding 3px 9px. START `good` on `good-bg`; SIT `bad` on `bad-bg`; STREAM and GRAB `warn` on `warn-bg`.
- These pairs are 2.98–3.94:1; the word itself carries the meaning, so never show the tint without the word.
