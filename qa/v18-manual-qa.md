# Durax v18 final manual visual QA

## Verdict

PASS

## Evidence inspected

- `reference-fierce-front.png`
- v18 `contact-sheet.png`
- v18 `previews/jumping.gif`, 192 x 208 GIF, 5 frames, 170 ms per frame, infinite loop
- v18 `spritesheet-extended-final.webp`, 1536 x 2288 RGBA WebP
- v18 `spritesheet-extended-final.png` compared row by row with v17
- v17 `contact-sheet.png`
- `awawak-front-spec.md`
- `validation.json`, `ok: true`, no errors or warnings

## Findings

- Row 4 engages the viewer from an offset three-quarter frontal angle. It is neither the v17 side profile nor a perfectly centered symmetric front.
- The nose sits visibly off the facial center. Both eyes are visible, the near eye is more dominant, and both pupils engage the viewer.
- The expression reads more forceful, alert, and shrill than v17. Natural fur and brow-ridge tension lowers over the glossy eyes, while cheek and lip-corner tension strengthens the mouth effort.
- The face does not use pasted human eyebrows or a cartoon brow symbol. The tension follows the animal's eye socket and fur structure.
- The sequence reads medium-small inhale, slightly larger held inhale, clearly large first `와`, medium open recovery, and the largest final `왁`.
- Frame 3 remains open and distinct from both the small inhale and large exhale frames.
- Large mouths remain wider than tall with a blunt muzzle. No frame shows a tall circular O, pointed snout, thin slit, or fang.
- The compact semi-upright idle-near body is preserved from v17. Feet remain gathered and planted.
- Row 4 baselines remain stable within one pixel: frames end at y 178 or 179. Top-edge variation follows ear and fur articulation rather than whole-body translation, and the GIF shows no vertical body jump.
- No frame is cropped. The tightest row 4 margins are 24 px left, 25 px right, 19 px top, and 29 px bottom.
- Measured alpha boxes match the supplied evidence: idle frame 0 is `(20, 33, 168, 179)` and row 4 frame 0 is `(24, 20, 166, 179)`.
- The supplied light-outline counts are comparable, idle 232 and row 4 222. Visual inspection confirms the same narrow pale-inner and dark-outer treatment as surrounding rows, without a baked second white halo.
- Pixel comparison against v17 shows rows 0-3 and 5-10 are identical. Only row 4 changed.
- All row 4 cells report zero opaque chroma-key pixels and zero chroma-fringe pixels.
- The atlas passes validation at 8 columns by 11 rows with zero transparent-RGB residue, zero errors, and zero warnings.

## Non-blocking observation

- The five separately rendered poses contain minor ear and fur-edge variation, but head direction, body placement, feet, scale, and playback baseline remain coherent.

## Blocking findings

None.
