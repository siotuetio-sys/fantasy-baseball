# PageMascot

A mascot pose at the right of a page title, standing on the first card's top edge.

**Markup:** give the page wrapper `.doodled`, then after its `h2.sec.page` add `div.page-doodle > img` of the pose: `mascot-pitch.svg` on the schedule, `mascot-bat.svg` on H2H, `mascot-ice.svg` on injuries and transactions.

- 120px wide, 40px above the title's top, `z-index` over the card; the title gets 130px right padding. On phone: 84px wide, 22px up, 88px padding.
- One pose per page; decorative, so `alt=""`.
