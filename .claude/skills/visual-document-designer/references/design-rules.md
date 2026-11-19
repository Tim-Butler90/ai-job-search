# Design rules (editable defaults)

These are starting values. Replace any of them when the user supplies their own brand or preferences.

## Type
| Element | Default |
|---|---|
| Body | Calibri or Arial 11 pt, line spacing 1.1-1.15, space after 6 pt |
| Title | 22-26 pt bold |
| Heading 1 | 15-16 pt bold, space before 14 pt, after 4 pt |
| Heading 2 | 12-13 pt bold |
| Caption / footnote | 9 pt |
| Alignment | Left aligned, ragged right. Avoid full justification (uneven word gaps hurt readability) |

Prefer fonts that exist on most machines (Calibri, Arial, Georgia, Cambria). If the user supplies a brand font, use it only if it is installed or embeddable; otherwise tell them and fall back to a similar safe font.

## Page
- US Letter (or A4 outside North America). Margins 0.75-1 in.
- Header/footer: small (9 pt), page numbers on multi-page docs.
- Keep a clear hierarchy: one title, section headings, body. Three levels is usually enough.

## Color
- Neutral text: near-black (#1F2933) on white.
- One accent (default deep blue #1F4E79) for title rule, headings, table header fill.
- Light tint (#EEF2F6) for banded rows or callouts.
- Check contrast; white text only on dark fills.
- Print check: the document must still make sense in grayscale.

## Spacing
- Use spacing, not lines, to separate things. Keep the same gap between like elements.
- Group related items closer than unrelated ones (proximity).
- Leave white space; do not fill the page to the margin just because room exists.

## Tables
- Header row: accent fill with white bold text, or bold with a bottom border.
- Light horizontal rules only; avoid heavy grids.
- Cell padding at least 0.05 in; numbers right-aligned; text left-aligned.
- Repeat header row on page breaks; do not let rows split across pages.
- Keep tables to what fits the width; if there are too many columns, split or rotate to landscape for that section.

## Brand supplied by the user
Follow the supplied colors, fonts, and logo clearance rules exactly. If a supplied color fails contrast for body text, keep it for accents and flag the issue; do not silently change it.

## Accessibility
- Real heading styles, list styles, and table header rows.
- Alt text on any image or logo that carries meaning.
- Meaningful link text (not "click here").
- Set document title and language.
