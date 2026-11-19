---
name: visual-document-designer
description: Designs clean, accessible, professional documents (reports, one-pagers, proposals, résumés, handouts, newsletters, price sheets, forms, policies) as editable Word (.docx) files and polished PDFs. Use whenever the user wants a document to look better, asks for layout, typography, spacing, page hierarchy, clean tables, a "polished PDF", an "editable Word version", or says "make this look professional" or "format this nicely", even if they never say "design".
---

# Visual Document Designer

Turn content into a document that reads easily, prints well, and stays editable. Good document design is mostly restraint: one typeface family, a short scale of sizes, generous spacing, one accent color, and tables that carry data without decoration.

## Input requirements

Essential (ask only if missing and it changes the result):
- The content (pasted, attached, or described). Never invent facts, figures, names, or quotes to fill space.
- Document type and audience (who reads it, on screen or printed).
- Output: editable Word, PDF, or both. Default: both.

Optional, use editable defaults if absent:
- Brand colors, fonts, logo (if supplied, follow `references/design-rules.md` and keep them; do not substitute).
- Page size (default US Letter 8.5x11 in; use A4 if the user is outside North America or says so).
- Length target.

## Workflow

1. **Read the content and classify it.** Identify title, sections, tables, lists, callouts. Note anything that is missing or looks inconsistent (conflicting numbers, mismatched dates) and flag it rather than silently fixing it.
2. **Pick a design spec** from `references/design-rules.md` (type scale, margins, spacing, palette). State the spec in one short line so the user can change it (for example: "Calibri 10.5 pt body, 0.75 in margins, navy accent").
3. **Build the Word file first** because it is the editable master. Use real styles (Title, Heading 1/2, List Bullet, Table Grid based) instead of manual bold and spacing, so edits propagate. Check the environment for tools: if a `docx` skill is listed, read its SKILL.md and follow it; otherwise use python-docx. Confirm availability before relying on any library or connector, and install with pip if missing.
4. **Create the PDF from the Word file** (LibreOffice `soffice --headless --convert-to pdf`) so both match. If LibreOffice is unavailable, say so and deliver the .docx only; do not claim a PDF exists.
5. **Render and look.** Convert PDF pages to images (pdftoppm) and inspect: orphaned headings, split tables, cramped or uneven spacing, text hitting margins. Fix and rebuild.
6. **Run the quality checks** below, then deliver the files with one line on the spec used and anything flagged.

Optional tools: Canva or Adobe connectors can help only if they are connected and the user wants a design-tool file. Check availability first; never state that a connector action happened unless the tool returned success.

## Output format

Deliver: `<Name>.docx` and `<Name>.pdf`, plus a two or three line note: spec used, items flagged, what is easy to change.

## Example requests

- "Turn these notes into a clean 2-page proposal I can edit in Word and also send as a PDF."
- "My price sheet table looks messy. Make it look professional."
- "Format this policy document with proper headings and spacing. Keep fonts accessible."

## Quality checks

- Body text 10.5-12 pt (11 pt default); no text under 9 pt except footnotes.
- Contrast: dark text on light background, ratio at least 4.5:1; color is never the only carrier of meaning.
- At most two font families; at most one accent color plus neutrals.
- Headings use real styles; heading levels do not skip.
- Tables: header row repeated across pages, no vertical gridline clutter, numbers right-aligned, consistent decimals, no table split mid-row.
- No orphan headings at page bottom; no single-line widows.
- Every number, name, and date matches the source content; nothing added.
- Word file opens and edits cleanly (styles, not manual spacing); PDF matches it.
- Document language set and PDF title set so screen readers behave.
