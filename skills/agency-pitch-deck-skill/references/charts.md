# Charts

Every chart in a Milkyano deck answers one question, uses colour by meaning, and is labelled so it can be read without a legend. Charts are built from shapes (or a simple SVG), not embedded images, so they stay crisp and editable after export.

## 1. Pick the chart from the question

| Question | Chart | Rules |
|---|---|---|
| Where does the money go? | **Split bar** (one pill bar cut into parts) | Max 4 parts; merge the rest into "Other". Biggest part first. Part labels: % inside the bar, name + Rp value under it. |
| What wins? | **Sorted bar list** (horizontal) | Largest first, always. Name left (fixed 360px column), bar, value at the bar end. Max 7 bars. |
| What changed? | **Before → after** (two numbers with an arrow) or **paired bars** | Before in `context`, after in `focus` (or `risk` if worse). Always show both values. |
| Where is it heading? | **Line + benchmark** | One line in `focus`, one dashed benchmark in `risk`, last point marked with a dot and its value. Max 12 points. |
| Who is right? | **Twin windows** (platform view vs business view) | Same size, same structure, side by side. Status badge top-right of each. |
| How much? | **Big number + delta badge** | One hero number per slide, or a stat row of max 4. |
| Is this normal? | **Bar vs benchmark** | Bars plus one dashed `risk` line labelled with its value ("Target 4.0×"). |
| What's the split by segment? | **Grid of tiles** (stat strip) | Max 7 tiles; the exception tile (e.g. "Unallocated") in `risk`. |
| When? | **Timeline / Gantt** | 3–6 columns; see Content blocks. |

**Never:** pie or donut, 3D, shadows on bars, two y-axes, stacked bars with more than 4 parts, legends, gridlines, chart junk (icons inside bars, gradients on bars).

## 2. Colour roles inside a chart

- `focus` — the one series or bar the headline is about. One per chart.
- `focus-soft` — a second series worth noticing (rank 2).
- `context` — everything else.
- `gain` — only for a real business gain (revenue, profit, real traffic up). Never for a platform metric looking good.
- `risk` — decline, missing data, a target/benchmark line, the exception tile.
- `client` — replaces `focus` in co-branded decks. Nothing else.

Categories and channels **never** get their own colours. Tell them apart by label and position. If a chart needs 5 different colours to be read, it is the wrong chart.

Colour never carries meaning alone: a gain also shows ▲ or a word, a risk shows ▼, a dashed line, or a word ("Missing").

## 3. Anatomy (every chart)

1. **Title = takeaway** — card-title style above the chart: "Shopee returns 3× more per rupiah", not "ROAS by channel".
2. **Direct labels** — values at the bar end (24–30px, 700), names on the left. No legend.
3. **One benchmark max** — dashed `risk`, 3px, labelled.
4. **Source** — in the slide's speaker notes, not under the chart: "Source: Shopee Seller Centre · Mar 2026". On the slide, keep only a caveat the chart would mislead without (estimate, small sample, unmappable share). Illustrative data says "Illustrative" on the slide.
5. **Geometry** — bars `radius-bar` 12px, 36–56px thick, 16–22px apart; bar length is proportional to the value (check it: a 44% bar is never shorter than a 39% bar).
6. **Frame** — chart sits in a `panel` card (`radius-card`, `pad-card`).

## 4. Tables

Use a table only when the reader must look up exact values across more than 3 columns. Otherwise use a chart or cards. Tables look like every other card in the deck: quiet, rounded, no heavy bars.

- The table sits inside a `panel` card (`radius-card`, 16px/28px padding, `shadow-card` in light mode).
- Header row: no fill. Label style, 700, caps, `muted`. Hairline `line` rules between rows. No zebra bands, no vertical rules, no black or navy bars.
- First column: bold names, optional muted descriptor on a second line.
- Numbers right-aligned, tabular figures. Context columns (before, prior) in `muted`.
- Change column: ▲ `gain`, ▼ `risk`, → `muted`, ● New `focus`. Always with a word ("Reduced", "New, test").
- Total row: `ground` tint, bold label, the key total in `focus`.
- Cells are plain text: style a whole cell (its colour), never bold or coloured words inside a cell — the slide editor and Google Slides strip them.
- Highlight: see §5. Max 8 rows on a slide; split or move the rest to an appendix.

## 5. Highlighting data

The consulting standard, kept classy: the eye should land on one thing, read why it matters, then see the context. Everything on a data slide either supports the highlight or steps back.

**Six rules**

1. **The title says what to see.** The headline names the highlighted thing ("Shopee returns 3× more per rupiah"). If you can't write that title, the chart is wrong.
2. **One highlight, the rest grey.** One bar, line, row or cell in `focus` (or `risk` if the point is a problem, `gain` if it's a real win). Everything else `context`. Two highlights max, never three.
3. **Annotate the highlight.** A short note next to it: the number and why it matters ("3× Google, on 26.7% of the budget"). Use a 2px `focus` rule or a thin leader line — no boxes, bubbles or big arrows.
4. **Sort to tell the story.** Largest first, or the order that puts the highlight first or last, where it's read.
5. **Give it one context.** A target, average or last year: dashed `risk` 3px line, or a `context` ghost series, labelled at its end. Never louder than the data.
6. **Build in steps.** For live presenting, show context first, then the same chart with the highlight.

**By chart type**

| Chart | Highlight | Annotation |
|---|---|---|
| Bar list | Focus bar in `focus`; others `context`; value labels on the focus bar in `focus`, others `muted` | Note to the right of the bars with a 2px `focus` rule |
| Line | Focus series `focus` 6–7px; comparison series `context` 4–5px | **Band**: `focus-wash` rectangle behind a period, label on top. **Event**: dot + thin `muted` leader + number and meaning. Series labelled at their end, no legend. |
| Split bar | The part the headline is about in `focus`/`risk`; others `context` shades | Name + value under the highlighted part |
| Table | **Row tint**: `focus-wash` fill + bold label on one row. **Key cell**: value in `focus` 700. **Verdict column**: empty except the highlighted row (▲ 33% YoY) | Never colour a whole column; never more than one tinted row |
| Big number | Number in `focus`/`gain`/`risk` | Delta badge + one line of meaning |
| Stat strip | Exception tile with dashed `risk` border | "of <total>" under it |

**Axes (line, column and time charts)**

- **Y axis:** 4–5 round values on the left (30 / 40 / 50 / 60), label style, `muted`, right-aligned to the plot. Hairline gridlines in `line` at each value; no vertical axis line. Name the unit once, above the top value ("Daily store visits", "Rp M").
- **Bars start at zero, always.** Lines may start above zero, but the lowest value must be labelled.
- **X axis:** a 2px `line-strong` baseline; labels under it, 8px below, every period or every other one, always the last one (W1, W3 … W12). Never rotate labels — abbreviate instead.
- Horizontal bar lists don't need a value axis when every bar is labelled at its end; overlapping (bullet) bars do (0 / 20M / 40M / 60M under the plot).

**Overlapping and grouped bars**

| Need | Pattern | Rules |
|---|---|---|
| Actual vs target / budget / last period | **Overlap (bullet)** | Target: wide (56px) `context` bar behind. Actual: thin (24px) bar in front, `focus`, or `risk` when over/under the limit. Note at the end: "105%, over budget". |
| Two periods or two segments per category | **Side by side** | Max 2 series, 8px apart, context series first, focus second. Labels on the focus bar only. |
| Parts of a whole per category | **Stacked** | Only if the parts add up to the whole. Max 3 parts, the focus part at the base. |
| Three or more series | **Don't** — split into small multiples. |

**Three datasets on one slide (small multiples)**

When a story needs several metrics (spend, visits, ROAS), stack them as separate panels on one shared timeline instead of one chart with two y-axes:
- Same x-axis and widths for every panel; x labels once, under the last panel.
- Each panel: name and unit at top-left, 2–3 y values, own scale.
- The same highlight band runs through every panel, so the eye reads cause and effect top to bottom.
- Max 3 panels per slide; one headline that links them ("Spend up in W6–W8; visits and ROAS both fell").

**Pie and donut charts:** don't. People can't compare angles accurately. Use instead:
- share of a total → **split bar** (max 4 parts, highlight one);
- a single percentage → **waffle** (10×10 squares, filled count = the %);
- the share is the whole message → **big number in words** ("6 in 10 rupiah go to Google").

**Before / after a highlight** — a default chart has a topic title, many colours and random order; the Milkyano chart has a takeaway title, sorted bars, one colour of focus and one note. If a chart still needs a legend after this, split it into two charts.

## 6. Placeholders

A chart that has no data yet is a dashed `line-strong` frame with the chart title and "Data pending: [source]". Never ship a client deck with a placeholder.

## 7. Export safety

Bars, pills and frames are shapes. Lines and dashed benchmarks can be SVG. No repeating gradients or patterns (Google Slides turns them into solid blocks); the corner grid texture is SVG line art.
