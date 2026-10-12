# Verdict panel

Every analysis slide ends in a verdict. A strong headline and a clean chart still leave the viewer asking: so is this good or bad, why, and what do we do? The verdict panel answers that on every slide, in the same place and the same order, so a client can read the deck by its verdicts alone.

## Parts

1. **Tag** — one pill:
   - `▲ Good`: `gain` on `gain-wash`. A real business gain or an opportunity worth taking.
   - `▼ Bad`: `risk` on `risk-wash`. A problem that costs money.
   - `● Mixed`: `focus` on `focus-wash`. Good and bad in the same finding.
2. **WHAT IT MEANS** — the implication for the business, in plain words. Not a restatement of the headline.
3. **WHY** — the cause, with the one number that proves it.
4. **WHAT WE DO** — the action. Point to the plan slide when the fix lives there ("slide 16").

Labels are caps, 24px, 700, `muted`. "WHAT WE DO" is in `focus`. Each text is **two lines at most, about 80 characters**. If it doesn't fit, the thought isn't sharp enough yet.

## Which slides get one

- **Analysis slides** (summary, gap, trends, campaign and product findings, retention, regions, efficiency): always.
- **Plan slides** (structure, roadmap, investment, close): never. They are the "what we do".

## Layouts

**Side panel (default).** The block goes on the left, flex:1, about 1024px. The panel goes on the right, 600px wide, with a 40px gap. Charts are redrawn for the 1024px width.

**Bottom strip.** Use this when the block needs the full width (an 8-column table, a 5-step chain). The tag sits on the left, then the three fields as equal columns in one row.

## Space budget (1920 × 1080, light mode)

- The header (chip + 2-line headline) ends at about y 327. With a 28px gap, the body has about **565px**.
- The side panel takes about 490px with two-line texts. Three-line texts push it to about 590: too tall.
- The bottom strip takes about 155px, so the block above it gets about 380px. A 7-row table at 24px fits; 8 rows does not.
- Don't put a source line on the slide. It goes in the speaker notes (`<aside>`). Keep a one-line caveat only when the slide would mislead without it.

## Markup

Side panel (swap the tag for Good / Mixed as needed):

```html
<div style="width:600px;display:flex;flex-direction:column;gap:16px;background:#FFFFFF;border:1px solid #E3E8F0;border-radius:24px;box-shadow:0 8px 24px rgba(31,95,214,0.08);padding:28px 32px">
<div style="display:flex"><p style="font-size:24px;font-weight:700;color:#C2410C;background:#FCEDE6;border-radius:999px;padding:6px 18px">▼ Bad</p></div>
<div style="display:flex;flex-direction:column;gap:6px"><p style="font-size:24px;font-weight:700;color:#5B6475">WHAT IT MEANS</p><p style="font-size:24px;line-height:1.4">[Implication in one sentence]</p></div>
<div style="display:flex;flex-direction:column;gap:6px;border-top:1px solid #E3E8F0;padding:14px 0px 0px"><p style="font-size:24px;font-weight:700;color:#5B6475">WHY</p><p style="font-size:24px;line-height:1.4">[Cause, with the number that proves it]</p></div>
<div style="display:flex;flex-direction:column;gap:6px;border-top:1px solid #E3E8F0;padding:14px 0px 0px"><p style="font-size:24px;font-weight:700;color:#1F5FD6">WHAT WE DO</p><p style="font-size:24px;line-height:1.4">[Action]</p></div>
</div>
```

Tags: Good `color:#15803D;background:#E7F6EC` · Mixed `color:#1F5FD6;background:#E8F0FD` · Bad `color:#C2410C;background:#FCEDE6`.

Bottom strip:

```html
<div style="display:flex;gap:32px;align-items:start;background:#FFFFFF;border:1px solid #E3E8F0;border-radius:24px;box-shadow:0 8px 24px rgba(31,95,214,0.08);padding:22px 32px">
<p style="font-size:24px;font-weight:700;color:#C2410C;background:#FCEDE6;border-radius:999px;padding:6px 18px">▼ Bad</p>
<div style="flex:1;display:flex;flex-direction:column;gap:6px"><p style="font-size:24px;font-weight:700;color:#5B6475">WHAT IT MEANS</p><p style="font-size:24px;line-height:1.4">[…]</p></div>
<div style="flex:1;display:flex;flex-direction:column;gap:6px"><p style="font-size:24px;font-weight:700;color:#5B6475">WHY</p><p style="font-size:24px;line-height:1.4">[…]</p></div>
<div style="flex:1;display:flex;flex-direction:column;gap:6px"><p style="font-size:24px;font-weight:700;color:#1F5FD6">WHAT WE DO</p><p style="font-size:24px;line-height:1.4">[…]</p></div>
</div>
```

## Examples (illustrative)

| Slide | Tag | What it means | Why | What we do |
|---|---|---|---|---|
| AOV trend | ▼ Bad | At last year's basket size, quarterly revenue would be ~[$__K] higher. | Spend stayed flat; the drop began when one low-price ad took over. | Separate low- and high-ticket products so Meta can't swap one for the other. |
| Customer cost | ▲ Good | New customers are cheap to win, so there's room to spend more. | [$__] of spend wins a [$__] first order; MER is [__×]. | After the rebuild, raise high-ticket budgets 20% at a time while MER holds. |
| Regions | ● Mixed | The city's average is low, but some suburbs buy like the best regions. | City averages [$__] vs [$__] nationally; four suburbs average [$__]+. | Test a high-ticket ad set on high-AOV postcodes. Small samples, so test first. |

## Cover and chips (same review)

- Cover: "<Client> <Deck type>" in the cover title (e.g. "Acme Performance<br>Marketing Audit"), chip "● Milkyano Digital · <Month Year>", then one sentence on what's inside, the period, and that it ends in recommendations. No clever line on the cover.
- Chips in Title Case: "● 02 · Spend vs Sales".
