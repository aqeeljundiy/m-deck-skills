# Milkyano

Milkyano Digital is a Melbourne growth and performance agency that sells "marketing systems that actually make profit". Its decks (pitches, audits, performance reports, growth strategies) have one job: show the client the numbers that matter, and what to do about them. This system is the rulebook every Milkyano deck follows, so a deck made by anyone, in any Claude chat, looks and reads the same.

The look blends three sites: **milkyano.com** (midnight navy, a blue glow at the top, fine grid lines in the corners, white pill buttons), **Pixel & Profits** (pill chips with a dot, headlines whose second line turns colour, "platform vs reality" dashboard windows) and **Elkiya Group** (a soft light mode: pale blue wash, rounded white cards, blue gradient buttons). One typeface: **Plus Jakarta Sans**.

Read this file first, then the sections: **Charts** (which chart, colour roles, anatomy, tables), **Content blocks** (every slide type and its layout), **Numbers and words** (formats, glossary, headline formula) and **Client co-branding and export**.

## How to make a Milkyano deck

1. Build it as a Claude Slides artifact (1920 × 1080), using these tokens. Never build directly in Google Slides through a connector: layout will not match.
2. Pick the mode: **dark** for pitches, covers, statements; **light** for reports and audits. One main mode per deck; the other only for section openers or a contrast slide.
3. Assemble the deck from the **content blocks** (section "Content blocks"), in the order of the client's question.
4. Every chart follows the **Charts** section. No exceptions.
5. Export: Share › Export › PowerPoint (.pptx) → Google Drive › New › File upload › Open with Google Slides. After import, only edit text and numbers in Google Slides; change layout here and re-export.

## Content fundamentals

- **Headlines are takeaways.** Line 1 (ink) states the fact. Line 2 (focus blue) gives the turn. *"Google says it's working. / Store traffic says otherwise."* Never a topic label like "Channel Performance".
- **One idea per slide.** One headline, one block, one takeaway.
- **Plain words, real numbers.** Every figure has a label and a source. No "$0K" placeholders in client decks; in templates use bracketed placeholders like `[Rp__M]`.
- **Profit over platform.** Where a platform metric (ROAS, reported visits) and a business metric (margin, real traffic, GMV) disagree, show both, side by side.
- **Recommend, don't just report.** Every analysis slide ends in an action: a "Do:" line, a verdict, or a tag (Scale / Expand / Keep / Test / Cut).
- **Voice:** direct, confident, a little sceptical of platform numbers. Short sentences. No hype words ("revolutionary", "synergy"), no exclamation marks, no emoji.

## Visual foundations

**Colour.** Each colour has a meaning, so the deck reads at a glance:

| Token | Means | Never |
|---|---|---|
| `focus` | Us, the client, the thing this slide is about. Headline turn. | More than one focus per chart |
| `context` | Everything else | Used for the key bar |
| `gain` | Real gain (revenue/profit up), Scale | Decoration, or "good" platform metrics |
| `risk` | Risk, gap, missing data, decline, targets/benchmarks | Errors in the client's work as blame |
| `client` | Replaces `focus` in co-branded decks | Replacing gain/risk/ink |

Dark mode: `ground` #050B15 with a radial `glow` at top centre, `panel` #0B1220 cards with a `line` border, no shadows. Light mode: `ground` #F4F7FC with a pale glow, white `panel` cards with `line` border and `shadow-card`.

**Type.** Plus Jakarta Sans only, five sizes per slide at most: headline 68, number 60–120, card title 30, body 26, label 24. Nothing under 24px. Weight 700 for headlines, numbers and titles; 400 for body; 600 for chips and labels.

**Layout.** Margins 128 left/right, 112 top, 160 bottom with a footer. Chip at the top margin, headline under it, block below, footer pinned 56px from the bottom (left: MILKYANO wordmark text; right: client or deck name · page number). Headlines never move between slides.

**Texture.** Milkyano's corner grid: 64px squares in `grid-line`, only in one or two corners, never behind text. Draw it as SVG line art (repeating gradients turn into solid blocks in Google Slides).

**Shapes.** Cards and windows `radius-card` (24px); chips, buttons, badges and split bars `radius-pill`; chart bars `radius-bar` (12px). Windows have three dots top-left and an optional status top-right (● Live).

## Parts

- **Chip** — pill, dot + label, names the block ("● The gap"). Top of every content slide.
- **Buttons** — primary: white pill (dark) or blue gradient pill (light); secondary: outline pill. Covers and the investment slide only.
- **Stat** — number + label + delta badge (▲ gain-wash / ▼ risk-wash).
- **Window** — dark panel with three dots and a status; frames any dashboard-style data.
- **Bar** — 12px radius, labelled at its end.
- **Step number** — pill with 01, 02…; active = focus fill, inactive = focus-wash.
- **Tag** — Scale (gain), Expand (focus), Keep (muted), Test (focus-soft), Cut (risk).

## Iconography

No icon set beyond simple 2px line icons in `focus` or `muted` (search, sliders, bar chart, film, trend arrow), placed in a 64px circle. Arrows are text (→). Never emoji.

## Logos

No logo files are in this system yet. Footers set "MILKYANO" in Plus Jakarta Sans 700, 3px letter-spacing, `muted`. Add the real wordmark (milkyano.com uses a custom thin serif-like wordmark) as an asset when available.
