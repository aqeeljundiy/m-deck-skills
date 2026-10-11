---
name: agency-pitch-deck-skill
description: Agency pitch deck skill. Builds marketing-agency decks — pitches, marketing audits, performance reports, social/creative reports, growth strategies, client co-branded decks — following the Milkyano design system (navy/blue, Plus Jakarta Sans, light and dark mode) and its chart, highlighting and data-display rules. Use whenever the user asks for a Milkyano deck, slides or report for a client, a marketing/performance report deck, or to check or fix a deck against the Milkyano guidelines, even if they don't say "skill".
---

# Milkyano decks

Every Milkyano deck shows the client the numbers that matter and what to do about them. This skill makes every deck look and read the same: same tokens, same blocks, same chart rules, same checks.

## Sources (read before building)

1. **The design system** (the live source of truth): https://claude.ai/artifact/8oWSmBBjonkyPqAEjtnqQE — read its `project/README.md`, then `charts.md`, `content-blocks.md`, `numbers-and-words.md`, `client-and-export.md` and `tokens.json` with the Artifact tool (`action: "read"`, `path`).
2. **Offline copies** in `references/` (same files, may be older). Use them if the artifact can't be read, and say so.
3. **The visual guide deck** (37 example slides): https://claude.ai/artifact/RwJCbbt84axyk6VvbZ2veU — read a slide file from it when you need markup to copy a pattern exactly (e.g. `project/slides/h-line.html` for a line chart with axes).

## Workflow

1. **Brief.** Get: client, period, deck type (pitch / audit / performance / social / creative / strategy), mode (dark for pitches, light for reports), currency, client brand colour if co-branded, and the data. Never invent numbers: use `[Rp__M]` placeholders and list them in the reply.
2. **Outline** from `content-blocks.md` → Deck order. Pick one block per slide; each slide = chip, two-line headline (fact / turn in blue), one block, source line, footer.
3. **Create the deck** as a Claude Slides artifact (Artifact `quickstart` with intent `slides`, then the Slides type). Install the Milkyano design system in it when the type allows; otherwise use the hex values from `tokens.json`. One Google Fonts face: Plus Jakarta Sans.
4. **Build charts** with `charts.md`: pick the chart from the question, one highlight, rest grey, annotate, axes on time/column charts, small multiples for 3 datasets, never pies.
5. **Co-brand** with `client-and-export.md`: client colour replaces `focus` only; darker shade for text.
6. **QA** (below), then give the link and the Google Slides export steps.

## Hard rules (the ones that get broken)

- Headline = takeaway, two lines, never a topic label.
- Colour by meaning only: focus = the point, context grey = everything else, gain green = real gains, risk orange = problems/targets. Categories never get their own colours.
- One highlight per chart (two max). Direct labels, no legends. Sorted bars. One dashed benchmark.
- Bars start at zero. Y axis 4–5 values + hairlines; X labels under the baseline, never rotated.
- No pies/donuts, 3D, dual y-axes, legends, repeating gradients/patterns (Google Slides turns them into blocks — draw grids as SVG line art).
- **Table cells are plain text**: style whole cells; never `<b>`/`<span>` inside `<td>` (stripped by the editor and Google Slides). Tables sit in a white rounded card, no black/navy header bars.
- Only three callouts: Do line, takeaway card, note bar.
- Numbers: Rp389.9M, 4.1×, 59.5%, ▲ 33% YoY, −17%, 62–78%, ~ only for estimates. One currency per deck.
- Every chart has a source line; illustrative data says so. Page numbers on every slide, in order.

## QA before handing over

- Render the slides (local preview of the slide HTML at 1920×1080) and check: nothing overflows its card or the slide; body content ends ≥16px above the footer; no word breaks mid-word.
- Look at every chart slide: bar lengths proportional to values, labels not on top of lines, highlight obvious at a glance.
- Every number has a label and a source; no placeholders left in a client deck (or they're listed).
- Score honestly against this checklist; fix before saying it's done.

## Exporting to Google Slides

Share › Export › PowerPoint (.pptx) → Google Drive › New › File upload → Open with Google Slides. Edit only text and numbers there; layout changes happen in the source deck. Do not rebuild decks through a Google Slides connector — it isn't one-to-one.
