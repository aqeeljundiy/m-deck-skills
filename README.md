# Agency Pitch Deck Skill

A Claude skill for building marketing-agency decks: pitches, marketing audits, performance reports, social and creative reports, growth strategies and client co-branded decks.

It gives Claude a complete deck system:

- **Design system** — light and dark mode colours with fixed meanings, one typeface (Plus Jakarta Sans), spacing, cards, chips and buttons.
- **Content blocks** — about 30 slide types for agency work: the client question, platform vs business view, measurement gaps, channel mix, portfolio, creative ranking, signals, verdicts, priorities, roadmaps, action tables, investment.
- **Chart rules** — which chart answers which question, colour by meaning, axes, overlapping and grouped bars, small multiples, one highlight per chart, annotations, no pies.
- **Numbers and words** — currency, ROAS, change and range formats, a glossary and a takeaway-headline formula.
- **Client co-branding** — how a client's brand colour slots in without breaking the system.
- **QA and export** — a checklist before hand-off and a clean path into Google Slides.

The bundled design system is based on Milkyano Digital's brand; swap `references/tokens.json` and the brand book to use your own.

## Install

**Claude Code (plugin):**

```
/plugin marketplace add aqeeljundiy/m-deck-skills
/plugin install agency-pitch-deck-skill@m-deck-skills
```

**Claude Code (manual):** copy `skills/agency-pitch-deck-skill` into `~/.claude/skills/`.

**claude.ai:** zip the `skills/agency-pitch-deck-skill` folder and upload it under Settings › Capabilities › Skills.

## Use

Ask for a deck ("make a performance report deck for <client>", "build an agency pitch for <brand>") or run `/agency-pitch-deck-skill`.

## Contents

- `skills/agency-pitch-deck-skill/SKILL.md` — workflow, hard rules, QA checklist
- `skills/agency-pitch-deck-skill/references/` — the design system: brand book, charts, content blocks, numbers and words, co-branding and export, tokens
- `skills/agency-pitch-deck-skill/references/verdict-panel.md` — the Good / Bad / Mixed verdict every analysis slide ends in (What It Means · Why · What We Do), with markup and a space budget
