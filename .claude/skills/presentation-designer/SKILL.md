---
name: presentation-designer
description: Plans and builds presentations around an audience, a story, and one main point per slide, with evidence, charts, and speaker notes, delivered as an editable deck (PowerPoint or an available slide tool). Use whenever the user asks for a presentation, slide deck, pitch, talk, board update, training, webinar, or "slides for...", asks to restructure or improve an existing deck, or wants speaker notes, even if they only say "help me present this".
---

# Presentation Designer

A good deck is an argument, not a document on slides. Each slide makes one point, backed by evidence the audience can take in within seconds.

## Input requirements

Essential (ask only for what is missing, in one short message):
- Audience and what they should think, decide, or do afterward.
- Topic and the source material (notes, data, documents).
- Length or time slot (default: about one slide per 1-2 minutes).

Optional:
- Brand colors/fonts/logo (if supplied, apply them exactly).
- Format: .pptx (default), or a connected slide tool if the user names one.
- Tone, level of detail, whether the deck is presented live or read.

Never invent statistics, quotes, customer names, or sources. If the point needs evidence the user did not provide, mark it `[evidence needed: ...]` and ask; do not fabricate.

## Workflow

1. **Audience and goal.** State in one sentence: "After this, [audience] will [decision/action]."
2. **Story spine.** Draft the storyline as a list of slide titles written as full-sentence claims (for example "Churn doubled after the price change"), not topics ("Churn"). Use a structure from `references/story-structures.md`. Check that reading only the titles tells the story.
3. **Per-slide plan.** For each slide: the one main point, the evidence (number, chart, quote, image, example), and the speaker note. Cut or merge slides that carry no distinct point.
4. **Charts.** Choose the simplest chart that shows the comparison; label directly, start bar axes at zero, and use data the user supplied. If a `dataviz` or `data-to-report` capability is available use it for chart design; verify every plotted number against the source.
5. **Build the deck** as editable output with real text boxes and native charts where possible (check for a pptx skill or python-pptx / pptxgenjs availability first; install if missing). Put speaker notes in the notes field. Keep text large (body at least 18 pt), at most about 30-40 words per slide, plenty of whitespace.
6. **Render and look.** Convert to images, inspect each slide for overflow, overlap, contrast, and consistency; fix and rebuild.
7. **Deliver** the deck, with a short list of flagged gaps and any `[evidence needed]` items.

Optional tools: Canva, Adobe, Gamma, or other design connectors may be used only if connected and wanted. Check availability first; report only what the tool actually returned. A connector cannot be enabled by this skill.

## Output format

- Editable deck file (.pptx by default) with speaker notes.
- One-paragraph storyline summary and the audience/goal sentence.
- Flag list: missing evidence, assumptions, anything shortened.

## Example requests

- "Make a 10-slide board update from these Q3 numbers. The ask is approval for two hires."
- "Here is my 40-slide deck. Cut it to 12 and give me speaker notes."
- "I have 5 minutes at a school fundraiser. Build slides and a script."

## Quality checks

- Each slide has exactly one main point; title states it as a claim.
- Titles alone tell the story in order.
- Every number and claim traces to supplied data or is flagged.
- Charts: correct type, zero baseline for bars, direct labels, no decoration, readable at distance.
- Text sizes at least 18 pt body; contrast at least 4.5:1; consistent alignment and spacing.
- Speaker notes exist for every content slide and add context rather than repeating slide text.
- Deck is editable (native text and charts, not flattened images).
- Rendered slides checked for overflow and overlap.
