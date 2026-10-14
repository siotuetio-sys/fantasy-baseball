Perfect Draft is the interface language of **The Perfect Fantasy Baseball Draft**, a live MLB decision desk for a Yahoo H2H fantasy manager. It is a dense, glanceable tool: navy chrome, a cool grey-blue page, white cards, one hot orange for the brand and the primary action, and a blue for everything you can click. Build every screen so the answer (start him, sit him, grab him) reads before the numbers do.

## Content fundamentals

- **Language.** The UI is Traditional Chinese (`lang="zh-Hant"`). Player names, team abbreviations and stat names stay in English: `Aaron Judge`, `NYY`, `OPS`, `xwOBA`, `ERA`. Never translate a stat abbreviation.
- **Fantasy vernacular is kept in English** where managers say it that way: `Stream`, `START` / `SIT` / `STREAM` / `GRAB`, `H2H`, `IL`, `DFA`. Write the recommendation words in caps inside a `RecBadge`.
- **Voice.** Short, direct, second person (你 / 你的球員). Headings name the job, often with a `·` subtitle: 「⭐ 我的球員 · 今日先發建議」, 「🔥 話題球員 · 大家在討論誰」.
- **Helper text** sits under a card's controls in `small` + `muted`, one sentence that says what the tool finds: 「找出今天對到弱打線、最適合 stream 的先發投手。」
- **Loading copy** is a verb + 中…: 「分析中…」, 「載入賽程中…」, 「掃描中…」. Always behind a `Spinner`.
- **Empty states** say what to do next: 「搜尋任一球員，檢視完整進階數據…」.
- **Source credit** is plain and specific: 「即時資料 © MLB Advanced Media (statsapi.mlb.com) · 進階數據參考 Baseball Savant」.
- **Emoji are the icon system** (see Iconography) — one leading emoji per nav tab and per card heading, never more than one, never mid-sentence.

## Visual foundations

### Color
- Page ground is `bg`; content sits on `panel` cards; anything recessed inside a card (stat tiles, player rows, inputs, segmented control) is `panel2`. Separate with the `border` hairline, never with a second shadow.
- Text is `text` (the brand navy) on all three surfaces; secondary text is `muted`.
- Chrome — the app bar, the tab bar and the toast — is `navbg` with `on-dark` titles and `navmut` labels.
- `accent` orange is scarce: the primary `Button`, the active tab, the active segment, the spinner head, and the word **Fantasy** in the title. One orange button per card.
- `accent2` blue means *interactive*: links, focus outlines (2px solid, 1px offset), and the hover border on cards and rows. In charts it is series A; `series-b` amber is series B.
- State colors come in text + tint pairs: `good`/`good-bg`, `warn`/`warn-bg`, `bad`/`bad-bg`. Their contrast on their tints is below AA (2.98, 3.17, 3.94:1) — keep them bold and **always** pair the color with a word (先發, 觀望, 板凳; 領先 / 平 / 落後). Green and red are never the only signal.
- Percentile bars step `good` (80+) → `pct-fair` (60–79) → `warn` (40–59) → `bad` (<40). The `Meter` uses a `bad → warn → good` gradient.
- The user's own players get a `mine` row tint in tables and a ⭐.
- White label on `accent` is 3.12:1 — this is the source's value and is kept; set button labels at 13px **bold** and never use `accent` behind body-size regular text.

### Type
- One family: the platform sans stack in `sans` (`-apple-system`, Segoe UI, Roboto, Noto Sans TC). No web fonts; Noto Sans TC carries the Chinese on Android and Linux.
- Base is `body` at 13.5px / 1.5. The scale is small and tight: `section` 15/700 for headings, `table` 13 for cells, `th` 11.5/600 uppercase for column heads, `caption` 11 for meta.
- Numbers are the heroes and the heaviest weight: `stat-value` 19/800, `score` 22/800, `score-hero` 34/800. Every number in a column or a score uses `font-variant-numeric: tabular-nums`.
- `app-title` 18/800 with −0.3px tracking is the only negatively tracked style; uppercase labels (`th`, `eyebrow`) get +0.4–0.5px.

### Spacing and layout
- Content column `max-width: 1100px`, padding `space-22` top, `space-16` sides (12px on phone), 60px bottom (86px on phone to clear the tab bar).
- Cards pad `space-14` (13px on phone) and stack `space-14`–`space-16` apart. Rows of controls gap `space-10`; chips gap `space-8`; list rows gap `space-6`.
- Grids are `auto-fit`/`auto-fill` with a min track: KPI tiles 150px, stat tiles 95px (two columns on phone), schedule cards 240px.
- Breakpoint is **680px**. Below it the top tabs become a fixed bottom tab bar, `.rtable` tables turn into one card per row (accordion for secondary cells), and other wide tables scroll horizontally with a 520px min width.

### Shape, borders and elevation
- Radii grow with the surface: `radius-xs` 5 badge → `radius-sm` 6 badge/meter → `radius-btn` 8 controls → `radius-input` 9 inputs → `radius-tile` 10 tiles and rows → `radius-card` 15 cards; `radius-pill` 20 for chips. Keep these exact (9 is not 8).
- Every surface has a 1px `border`. Cards add `shadow-card`; hoverable tiles and game rows rise 2px with `shadow-lift` and a `accent2` border. Floating layers use `shadow-dropdown`, `shadow-toast`, `shadow-modal`.

### Motion
- Views fade up 12px over 0.26s `cubic-bezier(.2,.7,.3,1)`, cards staggered by 0.04s. Game rows pop in from 96% scale.
- Press feedback: buttons scale to 0.97, chips and category buttons to 0.95–0.96.
- Hover: `filter: brightness(1.08)` on filled buttons; border to `accent2` on outlined things.
- `prefers-reduced-motion: reduce` turns all animation and transition off.

## Iconography

- **Emoji are the icons**, rendered by the platform: nav 📋 總覽 · 📅 賽程 · 🥊 對戰 · 🔬 球員 · 📡 市場 · 🔁 異動 · ⭐ 陣容; card headings ⭐ 📰 🔥 🔎 🏆 🎯 👁 🗓; actions 🔄 refresh, 🔍 search, ⇄ compare, ☆/⭐ watch, 🩹 injury, × remove, › go.
- Inside the nav an emoji sits in `.ic` at 15px (19px in the bottom bar) above or beside a `.lb` label.
- Team logos and player headshots come from MLB's image CDN at runtime (`.tlogo`, `.phead`); they are content, not part of this system.
- The **brandmark** (`assets/Logos/brandmark.svg`) is the only drawn mark: an orange `radius-logo` square, a white baseball with orange seams and a navy **P**. Show it at 38px in the app bar and as the favicon. Do not redraw or recolor it.

## Using the components

Components are plain CSS classes in `components/bundle.css`; there is no JavaScript bundle. Load `tokens.css` then `bundle.css`, write the markup shown in each component's card, and wire behavior yourself. Class names match the app's `index.html`, except the app bar (`header.appbar`), tab nav (`nav.tabs`, `nav.tabs.bottom`) and toast (`.toast`), which are bare `header`, `nav` and `#toast` in the app.
