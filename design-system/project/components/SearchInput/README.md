# SearchInput

Full-width player search with a dropdown of matches.

**Markup:** `div.pos-rel` > `input.search` (placeholder starts with 🔍 and names what to type) + `div.resultlist` of `div` rows. Highlight the keyboard-selected row with `.hi`.

**Consumer provides:** the query handler, the results and selection.

- Input `panel2`, 1px `border`, `radius-input`, 14px text, padding 11px 13px; focus border `accent2`.
- Results float on `panel2` with `shadow-dropdown`, max 300px tall; hovered row fills `accent2` with `on-dark` text.
- Placeholder says the language to search in: （英文，如 Aaron Judge）.
