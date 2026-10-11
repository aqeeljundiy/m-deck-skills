# Client co-branding and export

## Co-branding a deck

Milkyano owns the system; the client brings one colour and their logo.

1. Set the `client` token to the client's main brand colour (fills: bars, the focus bar, the client chip, header accents).
2. Set `client-ink` to a shade of that colour that reaches 4.5:1 on the slide ground; use it for the headline's blue line and small text. Example — Coca-Cola: `client` #F40009, `client-ink` #B30008 on light.
3. `client` replaces `focus` everywhere. Nothing else changes: `gain`, `risk`, `ink`, `muted`, grounds, type and layout stay Milkyano.
4. If the client colour is green or orange (clashes with gain/risk), use it only for the logo chip and keep `focus` blue.
5. The client logo sits in the cover chip or footer right, never larger than 48px tall. Their typeface appears only inside their logo.
6. Footer reads "<Client> × Milkyano · <page>".

## Building

- Build decks as Claude Slides artifacts at 1920 × 1080 using this system. Do not build through a Google Slides connector: layout is not one-to-one.
- Start every deck from the Content blocks; keep the headline position fixed.
- Before handing over: every number has a source, no placeholders, page numbers in order, bar lengths proportional, nothing overflows its card.

## Exporting to Google Slides

1. In the deck: Share › Export › PowerPoint (.pptx).
2. Google Drive › New › File upload, then right-click › Open with › Google Slides.
3. Expect: text, tables, shapes stay editable; Plus Jakarta Sans matches; radial glows may flatten (set background to `ground`); SVG lines (grids, sparklines, benchmarks) arrive as pictures.
4. After import, edit text and numbers only. Layout changes happen in the source deck, then re-export.
