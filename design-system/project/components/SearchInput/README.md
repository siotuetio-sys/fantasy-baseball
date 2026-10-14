# SearchInput

Pill-shaped player search with a dropdown of matches.

**Markup:** `div.pos-rel` > `input.search` + `div.resultlist` of `div` rows; the keyboard-selected row gets `.hi`.

- Input: `panel`, ink outline, `radius-pill`; focus adds `shadow-focus`. Placeholder names the language: （英文，如 Aaron Judge）.
- Results float on `panel` with an ink outline, `radius-tile`; the hovered row turns `pop`.
