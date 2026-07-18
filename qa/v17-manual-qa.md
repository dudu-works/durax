# Durax v17 final manual visual QA

## Verdict

PASS

## Evidence inspected

- v17 `contact-sheet.png`
- v17 `previews/jumping.gif`, 192 x 208 GIF, 5 frames, 170 ms per frame, infinite loop
- v17 `spritesheet-extended-final.webp`, 1536 x 2288 RGBA WebP
- v17 `spritesheet-extended-final.png` compared row by row with v16
- v16 `contact-sheet.png`
- `transition-outline-spec.md`
- `validation.json`, `ok: true`, no errors or warnings

## Findings

- Row 4 preserves the approved left-down three-quarter head. The muzzle remains directed toward screen-left and down, one near eye dominates above the nose, and the far eye stays recessed.
- The five-frame loop reads as small `아`, held small `아`, large first `와`, partial open recovery, large second `와`, then returns to the small opening.
- Every mouth is slightly more open than its v16 counterpart while retaining the small, large, recovery, large contrast.
- The large mouths remain wider than tall. No frame forms a tall circular O, thin slit, pointed snout, fang, or oversized tooth.
- The v17 body is a compact semi-upright seated oval with a side-on lean and gathered feet. It is visibly closer to row 0 idle than the broader, taller v16 frontal body.
- The transition from row 0 idle into row 4 is materially less abrupt than v16. The pose remains upright and active enough that it does not collapse into a flat loaf.
- Within row 4, the top and foot baseline remain stable. Frames 0-2 and 4 end at y 178, while the partial-recovery frame ends at y 179. This one-pixel fur-edge variation does not read as a body jump.
- No frame is cropped. The tightest row 4 margins are 23 px left, 24 px right, 19 px top, and 29 px bottom.
- Measured alpha boxes match the supplied evidence: idle frame 0 is `(20, 33, 168, 179)` and awawa frame 0 is `(23, 19, 168, 178)`.
- The supplied light-outline counts are comparable, idle 232 and awawa 225. Visual inspection confirms matching outline density rather than a doubled pale rim.
- Row 4 uses the same outline order as the other rows: a narrow pale inner line followed by a dark outer line. No baked double white halo, glow, sticker rim, or shadow is visible.
- Pixel comparison against v16 shows rows 0-3 and 5-10 are identical. Only row 4 changed.
- The atlas passes validation at 8 columns by 11 rows with RGBA transparency, zero transparent-RGB residue, zero chroma fringe, zero errors, and zero warnings.

## Non-blocking observation

- The recovery frame has a one-pixel lower alpha edge than the other row 4 frames. Feet remain visually planted and the GIF does not show a vertical bounce.

## Blocking findings

None.
