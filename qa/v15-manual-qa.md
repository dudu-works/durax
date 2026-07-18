# Durax v15 manual visual QA

## Verdict

PASS

## Evidence inspected

- `contact-sheet.png`, 768 x 1386 PNG
- `previews/jumping.gif`, 192 x 208 GIF, 5 frames, 170 ms per frame, infinite loop
- `spritesheet-extended-final.webp`, 1536 x 2288 RGBA WebP
- `spritesheet-extended-final.png` compared row by row with v14
- `awawa-frame-spec.md`
- `validation.json`, `ok: true`, no errors or warnings

## Findings

- Row 4 reads as small inhale, small inhale hold, large first `와`, partially recovered open mouth, large second `와`, then loops to the small inhale.
- Frames 0, 1, and 3 remain visibly open. Frame 3 does not close the mouth completely.
- Frames 2 and 4 are visibly wider than tall. The opening grows through the lip corners and cheeks with moderate vertical jaw travel.
- The nose tip remains centered at effectively the same depth. No frame turns the muzzle into a forward-pointing cone, beak, or stretched snout.
- The large-mouth frames retain a blunt, rounded muzzle. The cheeks expand laterally on both sides.
- Direct front eye contact is preserved across all five frames.
- Feet remain planted and the body baseline does not jump. Alpha bounds are stable: frames 0-3 use x 23 to 167 and frame 4 uses x 24 to 167; all frames end at y 183, with top varying only from y 13 to 14.
- No frame is cropped. Every row 4 frame retains at least 23 px left margin, 25 px right margin, 13 px top margin, and 25 px bottom margin inside its 192 x 208 cell.
- The light outer outline and dark inner outline are both visible against the black atlas preview and the checkerboard contact sheet.
- Pixel comparison against v14 shows rows 0-3 and 5-10 are identical. Only row 4 changed.
- The packaged atlas passes the v2 validator at 8 columns by 11 rows with zero transparent-RGB residue, zero chroma fringe, zero errors, and zero warnings.

## Non-blocking observation

- Fine fur texture changes slightly between row 4 frames because the five poses are separately rendered. The silhouette, head placement, nose position, eyes, feet, and baseline remain stable, so this does not read as a jump or anatomy projection at playback size.

## Blocking findings

None.
