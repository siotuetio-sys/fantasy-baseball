# TabNav

Primary navigation between the seven views; a sticky top tab strip on desktop and a fixed bottom tab bar under 680px.

**Markup:** `nav.tabs` > `button[data-v]` each holding `span.ic` (one emoji) and `span.lb` (label). Mark the current view `.active`. Add `.bottom` for the phone bar (the app switches it with a media query).

**Consumer provides:** the views, their emoji and labels, and the click handler.

- Inactive `navmut`, hover `on-dark`, active `accent` with a 2px `accent` underline (top line in the bottom bar).
- The bottom bar's tabs are equal width, 54px tall, label 10px; it carries `shadow-tabbar` and needs `padding-bottom` for the safe area.
- Keep labels to two Chinese characters: 總覽 賽程 對戰 球員 市場 異動 陣容.
