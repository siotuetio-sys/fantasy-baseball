# FeedbackStates

Loading, empty and error states for any card body.

**Markup:** loading `div.loading` > `span.spin` + a playful 「…中…」 line; empty `div.empty` > `img` of `mascot-head.svg` + a sentence that says what to do + optional `div.cta` with a `Button`; error `div.err` with what broke and `button.errretry` 再揮一次.

- The app draws the empty-state head as a background on `.empty .big`; consumers can use the `img`.
- Error: `err-text` on `bad-bg` with a dashed `bad` outline, `radius-tile`.
