---
name: brand-kit-assistant
description: Applies a brand kit the user supplies (colors, fonts, logo rules, tone of voice, brand examples) consistently to documents, copy, slides, social posts, and designs, and checks drafts against it. Use whenever the user shares or describes brand guidelines, hex codes, brand fonts, a logo, or a voice guide, asks to "make this on-brand", "use our brand", "check this against our guidelines", or wants a reusable brand sheet, even if they do not say "brand kit".
---

# Brand Kit Assistant

Apply the brand the user actually supplied, and say clearly where the kit is silent. Do not invent brand rules.

## Important limit on memory

This skill does not store a brand permanently. The kit lives only in what the user provides in the current conversation, a Project's files or instructions, or an attached file. At the start of work, say where the kit is coming from. If the user wants it reusable, produce a "Brand Kit Sheet" (see `references/brand-kit-template.md`) and suggest they save it to a Project's knowledge or keep the file, and re-attach it when needed. Never say "I'll remember this".

## Input requirements

Essential:
- The kit itself, or the part available: hex/RGB/CMYK colors, font names, logo usage rules, tone-of-voice description, and any example copy or designs.
- What to apply it to (document, slide, post, email, page).

Missing pieces: list them as "Not provided" and use clearly labeled, editable defaults only for the task at hand. Do not guess a brand color from a logo image by eye and present it as official; if a color is estimated from an image, say it is estimated.

## Workflow

1. **Intake.** Build a one-screen Brand Kit Sheet from what was supplied, with sections: colors (with roles), typography, logo rules, voice, examples, and a "Not provided" list. Show it to the user briefly so they can correct it.
2. **Check feasibility.** Confirm fonts are usable (installed, embeddable, or provide a close fallback and flag it). Check text/background contrast for the supplied palette; if a supplied pair fails 4.5:1 for body text, flag it and suggest a compliant use (accent only, large text only) rather than silently changing the color.
3. **Apply.** Produce the requested deliverable with the kit: colors by role, type hierarchy, logo placement with clear space as specified, copy in the supplied voice. Use the user's examples as the reference for voice, not as text to copy.
4. **Check against the kit.** Run the checklist below and list deviations. Where the kit says nothing, say "kit silent" and name the default used.
5. **Deliver** the work plus the Brand Kit Sheet and the deviation notes.

Optional tools: Canva (brand kits/templates), Adobe (fonts, assets), and similar connectors may help only if connected. Check availability before using, and report exactly what the tool returned. These skills cannot enable a connector or grant access; if one is missing, say so and continue with files.

## Output format

- The deliverable.
- Brand Kit Sheet (source, colors, type, logo, voice, not provided).
- Deviation and flag list (contrast, font fallback, kit silent areas).

## Example requests

- "Here are our brand colors and fonts. Make this one-pager on-brand." (attached guide)
- "Our voice is friendly but precise, never salesy. Rewrite this email in that voice."
- "Check this flyer against our brand guidelines and tell me what is off."

## Quality checks

- Every color, font, and rule used is traceable to the supplied kit or labeled as a default.
- No invented logo rules, tagline, or hex codes.
- Logo is not stretched, recolored, or cropped unless the kit allows it; clear space respected.
- Contrast ratios for text meet 4.5:1 (3:1 for large text), or flagged.
- Voice matches the supplied examples; banned words from the kit are absent.
- Honest about storage: no claim of permanent memory.
- Honest about tools: no connector action claimed unless the tool succeeded.
