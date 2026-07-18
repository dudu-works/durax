# Durax v16 manual visual QA

## Verdict

PASS

## Evidence inspected

- `reference-left-down-head.png`
- `contact-sheet.png`, 768 x 1386 PNG
- `previews/jumping.gif`, 192 x 208 GIF, 5 frames, 170 ms per frame, infinite loop
- `spritesheet-extended-final.webp`, 1536 x 2288 RGBA WebP
- `spritesheet-extended-final.png` compared row by row with v15
- `awawa-quarter-view-spec.md`
- `validation.json`, `ok: true`, no errors or warnings

## Findings

- Row 4 is not a centered symmetric frontal portrait. The head is lowered and rotated toward screen-left and down.
- The muzzle occupies the lower-left facial direction. The nose remains close to the facial center instead of projecting straight toward the viewer.
- One dominant near eye sits above the nose and looks toward the viewer. The far eye is recessed and mostly hidden, so the face does not produce two equal frontal eye contacts.
- All five frames preserve the same three-quarter head angle, nose direction, dominant-eye direction, and lowered head placement.
- The loop reads as small inhale, small inhale hold, large first `와`, partially recovered opening, large second `와`, then returns to the small inhale.
- Frame 3 remains visibly open and does not close the mouth completely.
- The two large openings are broad and laterally developed, not tall circular O shapes or thin slits.
- The muzzle stays broad and blunt. No frame creates a pointed cone, beak, or forward-stretched snout.
- The body does not jump. Every frame has the same top alpha coordinate at y 15 and the same foot baseline at y 183 inside its 192 x 208 cell.
- Horizontal alpha bounds vary only with small fur and silhouette articulation: x 18-173, 20-171, 19-172, 19-172, and 20-170. This does not create a positional jump.
- No frame is cropped. The tightest row 4 margins are 18 px left, 19 px right, 15 px top, and 25 px bottom.
- The light outer outline and dark inner outline are visible on both the black atlas preview and checkerboard contact sheet.
- Pixel comparison against v15 shows rows 0-3 and 5-10 are identical. Only row 4 changed.
- The packaged atlas passes validation at 8 columns by 11 rows with zero transparent-RGB residue, zero errors, and zero warnings.

## Non-blocking observation

- Minor fur-edge and body-width variation exists between the separately rendered row 4 poses, but the head angle, eye, nose direction, top edge, feet, and baseline remain stable at playback size.

## Blocking findings

None.
