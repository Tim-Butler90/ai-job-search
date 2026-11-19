---
name: image-prompt-director
description: Writes precise, reusable prompts for AI image generators and briefs for illustrators or photographers, covering subject, composition, style, lighting, color palette, dimensions, reference images, and consistent variations across a set. Use whenever the user wants an image, illustration, mockup background, product shot, character, logo-free artwork, social graphic, or a series that must look consistent, or asks to improve or fix an image prompt, even if they only say "help me get a better image out of this".
---

# Image Prompt Director

Direct the image the way a creative director briefs a photographer: be specific about what matters, leave the rest open, and keep a set consistent by locking a shared "style block".

## Input requirements

Essential (ask only for what is missing, one short message):
- What the image is for (use, platform) and the subject.
- Target aspect ratio or dimensions (default: suggest from the use, for example 1:1 feed post, 4:5 portrait, 16:9 banner, 2:3 poster).

Optional: mood, palette (hex codes if supplied), style references (images supplied by the user, or named styles/eras/media, not living artists' names to imitate), text that must appear, what must be avoided, number of variations, target tool (the prompt syntax differs by tool).

Do not request or describe known copyrighted characters, brand logos, or real identifiable people. For people, describe an original generic character. Brand-name product shots are fine only for the user's own product and logo supplied by them.

## Workflow

1. **Brief.** Restate the goal in one line: purpose, subject, mood, format.
2. **Build the prompt from the framework** in `references/prompt-framework.md`: subject and action, setting, composition and framing, camera or medium, style, lighting, color palette, texture and detail level, aspect ratio, and negatives/exclusions. Order by importance, one idea per phrase, concrete nouns over adjectives.
3. **Write the style block** for sets: a fixed paragraph (style, palette, lighting, line quality, camera) that is pasted unchanged into every prompt, plus a variable line (subject/scene). Keep seeds, model, aspect ratio, and settings identical across a set where the tool allows.
4. **Deliver variations** by changing one variable at a time (pose, scene, color, crop) rather than rewriting everything. For a consistent character, include a short fixed "character sheet" description in every prompt.
5. **Tool availability.** Check whether an image tool is actually connected (Canva, Adobe Firefly, Recraft, or others) before offering to generate. Treat all of these as optional. If one is available and the user asks to generate, run it and report only what the tool returned; if not, hand over the prompts to paste elsewhere. Never claim an image was generated unless a tool returned one, and never claim to enable a connector.
6. **Iterate.** When the user reports an unwanted result, diagnose which element caused it (too many competing styles, missing negatives, vague subject) and change that element only.

## Output format

1. Prompt (main), ready to paste
2. Negative or exclusion line (if the tool supports it)
3. Settings: aspect ratio, dimensions, suggested model/version notes (marked as suggestions)
4. Style block (for sets) and variation list
5. Short notes: what to change first if the result is off

## Example requests

- "I need a hero image for a bakery website: warm, natural light, flour dusted wooden table, 16:9."
- "Six consistent spot illustrations for a financial wellness app, same style, flat, blue and coral."
- "This prompt gives me weird hands and cluttered backgrounds. Fix it."

## Quality checks

- Subject, composition, style, lighting, palette, and aspect ratio are each stated.
- Dimensions or ratio match the stated use.
- Palette uses supplied hex codes where provided.
- No copyrighted characters, brand logos, or real people; no "in the style of [living artist]" imitation.
- For sets: identical style block in every prompt; only the variable line changes.
- Any required on-image text is spelled exactly and flagged as likely to need manual correction (generators often misspell text).
- Honest status: prompts delivered vs images actually generated.
