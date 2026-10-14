Perfect Draft is the look and voice of **The Perfect Fantasy Baseball Draft**, a live MLB decision desk for a Yahoo H2H fantasy manager. It reads like a well-made Japanese stationery notebook that an American cartoonist doodled in: paper, black ink lines, one pop of lemon, and a baseball mascot who talks to you. Keep it calm and tidy; let the jokes live in the words and the drawings, never in extra colour.

## Content fundamentals

- **Language.** The UI is Traditional Chinese (`lang="zh-Hant"`). Player names, team abbreviations and stat names stay in English: `Aaron Judge`, `NYY`, `OPS`, `ERA`. Recommendation labels stay in caps: `START`, `SIT`, `STREAM`, `GRAB`.
- **Voice: a dugout coach who likes you.** Talk to the manager as 你, short sentences, a little teasing, never mean. Every joke still says what is true.
  - Hero quips follow the matchup: 「別鬆懈，對手正在偷看你的陣容。」 (leading), 「暫時落後，但棒球是圓的。」 (trailing), 「可以準備香檳了（先別開）。」 (clinched).
  - Loading: 「教練翻筆記中…」「偷聽休息室八卦中…」「在自由市場翻箱倒櫃…」
  - Empty: 「板凳空空的。先把你的 Yahoo 陣容叫進來，之後每天幫你排好先發。」「今天沒有比賽。球員們應該在打電動。」
  - Errors say what broke and what to do: 「球被接殺了：連不上資料來源，檢查一下網路。」 with a 「再揮一次」 button.
- **Page names are plain questions or nicknames**, followed by a handwritten English aside: 今天誰跟誰打 *tonight's games* · 本週對決 *head to head* · 球員顯微鏡 *under the microscope* · 自由市場撿寶 *waiver wire gems* · 誰上誰下 *who's in, who's out* · 我的球隊 *your dugout* · 教練錦囊 *game plan*.
- **Greeting by the clock** above the hero: *Morning, Skipper!* / *Afternoon, Skipper!* / *Evening, Skipper!* / *Still up, Skipper?*
- **No emoji in headings.** Drawings do that job.

## Visual foundations

### Colour
- Three things only: `bg` paper, `line`/`text` ink, and `pop` lemon. Everything else is a quiet helper (`panel`, `chip`, `border`, `muted`) or a state colour.
- `pop` is spent on purpose: the dashboard hero block, the active bottom tab, the refresh button, the START label's letters, the selected search result, the focus glow. Never put lemon text on paper.
- Primary actions and the active state are **ink**: black pill with paper text (`button.btn`, `nav.tabs button.active`, `.seg button.on`).
- Hover is `pop-soft`, never a darker shade.
- State colours `good`, `warn`, `bad` are for text and small marks; pair each with a word. `bad` on `bad-bg` is 4.34:1, so keep it bold there.
- Charts: series A in `text`, series B in `series-b`. No blue and orange pairs.

### Type
- `display` (Anton) for numbers, the wordmark and START/SIT labels. Numbers are the loudest thing on any screen: `hero-num` 88px, `kpi-num` 44px, `stat-num` 26px.
- `head` (Noto Serif TC 900) for Chinese headings: `hero-title` 44px, `page-title` 28px, `card-title` 19px.
- `body` (Noto Sans TC) for everything else at 14px / 1.55.
- `hand` (Caveat 700) only for short English asides and the greeting, at 1.25em of the heading beside it, in `muted`. Never set Chinese in `hand`.
- Fonts load from Google Fonts; `bundle.css` imports them.

### Lines, shapes and spacing
- Shapes are drawn, not shaded: every card, control, pill and bubble has a `line-width` (1.5px) `line` outline. Hairlines between table rows use `border`. There are no drop shadows; the only glow is `shadow-focus`.
- Corners are round and generous: `radius-card` 24 for cards, `radius-kpi` 22 for KPI cards and bubbles, `radius-hero` 28 for the hero, `radius-pill` for anything you press.
- Content column max 1100px; cards stack `space-16` apart; card padding 20/22 (16 on phone).
- Breakpoint 680px: the tab bar moves to the bottom (active tab gets a lemon tile), KPI cards stack, the hero mascot drops under the copy.

### Motion
- Small and physical: cards and game rows lift 2px on hover; buttons press to 0.97–0.98. Views fade up 12px. `prefers-reduced-motion` turns it all off.

## Illustration

- **The mascot** is a baseball with a black cap, two dot eyes and stubby legs, drawn in `line` at `line-art` weight with `bg` fill and `pop` details. Five drawings live in `assets/Illustrations/`:
  - `mascot-coach.svg` holds a clipboard and points up. Dashboard hero only, with a speech bubble.
  - `mascot-pitch.svg` mid leg-kick. Schedule page.
  - `mascot-bat.svg` bat on the shoulder. H2H page.
  - `mascot-ice.svg` ice bag on the cap, plaster, sweat drops. Transactions and injuries page.
  - `mascot-head.svg` the head alone on a lemon ball. Every empty state.
- Page mascots sit at the right of the page title and peek over the first card's top edge (`PageMascot`). One drawing per screen, plus the empty-state head where needed.
- Speech bubbles carry live facts in the mascot's voice: 「9 人先發、3 人坐板凳。我已經幫你排好了！」
- Draw new poses from the same parts: 46-unit ball, seams with tick stitches, cap with brim, ellipse eyes, 2.6 stroke, round caps and joins. Add only `pop` and `bg` as fills.

## Iconography

- UI icons are 24px line icons, 1.8 stroke, `currentColor`, round caps: grid (總覽), calendar (賽程), swap arrows (對戰), bars (球員), target (市場), pulse (異動), baseball (陣容), circular arrow (refresh). Show them at 18px, 21px in the bottom bar.
- The **brandmark** (`assets/Logos/brandmark.svg`) is a lemon baseball with ink seams. Show it at 40px beside the PERFECT DRAFT wordmark and as the favicon.

## Using the components

Components are plain CSS classes in `components/bundle.css`; there is no JavaScript bundle. Load `tokens.css`, then `bundle.css`, and copy the markup in each component's card. Class names match the app's `index.html`, except the app bar (`header.appbar`), tabs (`nav.tabs`, `nav.tabs.bottom`), toast (`.toast`), hero quip (`.hero-quip`) and page title (`h2.sec.page`), which the app writes as bare `header`, `nav`, `#toast`, `#heroQuip` and `.view>h2.sec`.
