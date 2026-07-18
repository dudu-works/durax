# Durax v19 canonical normalization manual QA

## Verdict

PASS

## Evidence inspected

- `contact-sheet.png` and v18 contact sheet
- `previews/idle.gif`
- `previews/idle-to-awawak.gif`
- Every other GIF under `previews`: `awawak`, `failed`, `review`, `running-left`, `running-right`, `running`, and `waiting`
- `spritesheet-extended-final.webp` and PNG atlas
- `canonical-model-spec.md`
- `normalization-report.json`
- `validation.json`

All nine preview GIFs decode successfully at 192 x 208, use 170 ms frames, and loop infinitely.

## Findings

- Canonical normalization visibly reduces the cross-action size jumps present in v18. Standard-row mean visible areas now occupy the narrow 17,766 to 18,337 range reported by the normalization artifact, versus the supplied v18 range of 14,851 to 25,376.
- The widest running frames use the allowed safe-width cap. Their frame-level visible areas range from 16,272 to 18,565, retain transparent margins, and are not cropped.
- The idle loop reads in the required order: offset three-quarter front, tiny breath, head-left turn, held left blink, return to the offset front, and front blink or breath.
- Idle body, feet, scale, and bottom baseline remain stable while the head and eyes change. All six idle frames end at y 179.
- The head-left frames widen laterally because the head turns, but the seated torso and planted feet do not translate or pulse.
- The 12-frame `idle-to-awawak.gif` contains the full six-frame idle sequence, the five-frame awawak sequence, and return to idle. Idle ends at y 179 and awawak begins at y 179, with nearly identical overall width and scale. No conspicuous scale or baseline pop is visible.
- The approved v18 awawak expression and cadence remain intact after normalization: engaged offset frontal eyes, fierce brow and cheek tension, and medium-small, larger, large, recovery, largest mouth sequence.
- Failed, waiting, running, review, and directional motion semantics remain visually unchanged. Rows other than idle show the same source poses as v18, changed only by uniform scale and registration.
- Running-right and running-left retain matching eight-frame cadence and equal normalization statistics: min 16,272, max 18,565, mean 17,766. Their corresponding alpha bounds and baselines match frame by frame.
- The generic running row remains planted on y 180 with consistent scale across all six frames.
- Look rows preserve the full directional sweep. Every frame remains inside the cell; the tightest horizontal margin is 24 px and the tightest top margin is 10 px.
- The shared pale-inner and dark-outer outline remains visually consistent across normalized rows. No row gains a doubled halo or mismatched thickness.
- Validator result is clean: 1536 x 2288 RGBA v2 atlas, zero errors, zero warnings, zero transparent-RGB residue, zero opaque chroma-key pixels, and zero chroma-fringe pixels.

## Non-blocking observation

- Some running frames have smaller visible area because their long horizontal stride reaches the safe cell width before the canonical target area. The preserved transparent margin and unchanged baseline prevent clipping or a perceived scale pop.

## Blocking findings

None.
