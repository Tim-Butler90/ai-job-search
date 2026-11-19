# Prompt framework

Fill in what matters; skip what does not. Order roughly by importance.

1. **Subject and action:** who or what, doing what. Concrete nouns.
2. **Setting:** where, time of day, season, background complexity.
3. **Composition:** framing (close-up, medium, wide), angle (eye level, overhead, low), placement (rule of thirds, centered), negative space reserved for text.
4. **Medium or camera:** photograph (lens such as 35 mm or 85 mm, depth of field), watercolor, flat vector, 3D render, paper cut, etc.
5. **Style:** era, movement, or genre described generally (for example "mid-century modern poster", "editorial flat illustration").
6. **Lighting:** soft window light, golden hour, overcast, studio softbox, rim light, high-key or low-key.
7. **Palette:** named colors or hex codes; proportions (for example 60 percent cream, 30 percent navy, 10 percent coral).
8. **Detail and texture:** grain, matte, glossy, fine linework, minimal.
9. **Format:** aspect ratio and size.
10. **Exclusions:** things to avoid (clutter, extra fingers, text, watermark), phrased as the tool expects.

## Template
```
[Subject and action], [setting], [composition and framing], [medium/camera], [style], [lighting], [palette], [texture/detail]. Aspect ratio [x:y].
Avoid: [list].
```

## Common aspect ratios
| Use | Ratio | Typical pixel size |
|---|---|---|
| Square post | 1:1 | 1080 x 1080 |
| Portrait feed | 4:5 | 1080 x 1350 |
| Story / reel cover | 9:16 | 1080 x 1920 |
| Banner / hero | 16:9 | 1920 x 1080 |
| Poster | 2:3 | 2000 x 3000 |
| Wide web header | 3:1 | 1800 x 600 |

Check the target platform's current spec if it matters; these are common values.

## Consistent sets
- **Style block:** one fixed paragraph, pasted unchanged into every prompt.
- **Variable line:** the only part that changes.
- Keep model, seed, aspect ratio, and settings identical when the tool allows.
- For recurring characters: a fixed description of face shape, hair, clothing, palette, and proportions in every prompt; use a reference image if the tool supports it.
- Change one variable at a time when iterating.

## References
- If the user supplies reference images, describe what to take from each (palette, composition, texture) and what to ignore.
- Do not ask for a copy of a specific artwork, character, or brand design.

## Text in images
Generators often garble words. Keep on-image text short, give the exact spelling, and plan to add text in a layout tool afterward when accuracy matters.

## Troubleshooting
| Problem | Likely cause | Fix |
|---|---|---|
| Cluttered result | Too many subjects or adjectives | Cut to one subject, add "minimal background" |
| Muddy colors | No palette given | State 3-4 colors or hex codes |
| Wrong mood | Lighting not specified | Name the light and time of day |
| Inconsistent set | Style described differently each time | Use a locked style block |
| Odd anatomy | Complex pose | Simplify pose, crop out hands, add to exclusions |
