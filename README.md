# Milkyano Deck Skill

A Claude skill that builds Milkyano Digital decks (pitches, audits, performance, social, creative and growth reports) using the Milkyano design system: colours for light and dark mode, Plus Jakarta Sans, content blocks, chart and highlighting rules, number formats, client co-branding and Google Slides export.

## Install

**Claude Code (as a plugin):**

```
/plugin marketplace add aqeeljundiy/milkyano-deck-skill
/plugin install milkyano-deck-skill@milkyano
```

**Claude Code (manual):** copy `skills/milkyano-deck-skill` into `~/.claude/skills/`.

**claude.ai:** zip the `skills/milkyano-deck-skill` folder and upload it under Settings › Capabilities › Skills.

## Use

Ask for a Milkyano deck ("make a Milkyano performance report for <client>") or run `/milkyano-deck-skill`.

## Contents

- `skills/milkyano-deck-skill/SKILL.md` — workflow, hard rules, QA checklist
- `skills/milkyano-deck-skill/references/` — offline copy of the design system (brand book, charts, content blocks, numbers and words, co-branding and export, tokens)

The live design system and the visual guide deck are linked from `SKILL.md` (private claude.ai artifacts; share them with the team from their Share menu).
