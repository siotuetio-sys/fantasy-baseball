# FeedbackStates

Loading, empty and error states for any card body.

**Markup:** loading `div.loading` > `span.spin` + 「分析中…」; empty `div.empty` > `div.big` (one emoji) + a sentence that says what to do, optionally `div.cta` with a `Button`; error `div.err` with what failed and what to try.

- Spinner 15px ring in `border` with an `accent` head, 0.7s.
- Empty and loading text `muted`, centered. Error `err-text` on `bad-bg` with a `#dc354555` border, `radius-input`.
