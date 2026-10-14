# H2HInput

Number box for a category total in the H2H table; it turns green when you are winning that category.

**Markup:** `input.h2hin[inputmode=decimal]` inside a `td.num`; the app toggles `.tag-good` on the cell when you lead.

- 38px tall (40 on phone), `panel`, ink outline, `radius-input-sm`, value in `display` at 17px, right-aligned. Winning: `good` on `good-bg` with a `good` outline.
