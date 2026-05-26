# CAD Files

All 3D and 2D design files for the chair.

## Folders

- `concept/` — early sketches, ideas, screenshots, references — **to be updated**
- `source/` — editable CAD (Fusion 360, FreeCAD, SolidWorks, OnShape exports) — **to be updated**
- `step/` — STEP files. Open in any CAD tool. **36 files present.**
- `stl/` — STL files ready to 3D print. **36 files present.**
- `thumbnails/` — isometric PNG previews of each part, one per STL (browse without a CAD tool). **36 images present.**
- `drawings/` — 2D drawings with dimensions (PDF) — **to be updated**

## Current Parts (36)

The CAD was exported in 2 batches from SolidWorks 2024 with generic `BodyN`
names. We renamed them by visually inspecting the thumbnails and using the
[product assembly guide](../docs/assembly-guide.pdf). The original body number
is preserved as a numeric suffix (`-N`) so re-labels are traceable.

### Frame & base (large structural)

| Part | Size (mm) | Notes |
|---|---|---|
| [`seat-pan-9`](thumbnails/seat-pan-9.png) | 602 × 436 | seat structural shell — high confidence |
| [`back-frame-16`](thumbnails/back-frame-16.png) | back-frame assembly |
| [`back-mesh-panel-13`](thumbnails/back-mesh-panel-13.png) | back mesh panel |
| [`back-mesh-tensioner-35`](thumbnails/back-mesh-tensioner-35.png) | 438 × 69 × 52 | curved bar with finger tabs |
| [`backrest-cover-25`](thumbnails/backrest-cover-25.png) | 42 × 194 × 65 | back-rest cover (user-identified) |
| [`seat-shell-20`](thumbnails/seat-shell-20.png) | 556 × 109 × 399 | seat outer shell (user-identified) |
| [`seat-rail-2`](thumbnails/seat-rail-2.png) | seat rail |
| [`chair-base-27`](thumbnails/chair-base-27.png) | 703 × 562 | 5-arm chair base (the `BASE` in the assembly guide) |
| [`caster-spider-14`](thumbnails/caster-spider-14.png) | 573 × 742 | back-frame inner rib structure (label kept per round-1 review) |
| [`wheel-3`](thumbnails/wheel-3.png) | caster wheel |

### Armrest & headrest

| Part | Size (mm) | Notes |
|---|---|---|
| [`armrest-arm-12`](thumbnails/armrest-arm-12.png) | armrest arm |
| [`armrest-pad-8`](thumbnails/armrest-pad-8.png) | armrest pad |
| [`armrest-pad-23`](thumbnails/armrest-pad-23.png) | 130 × 44 × 229 | second armrest pad variant (user-identified) |
| [`armrest-post-24`](thumbnails/armrest-post-24.png) | 49 × 255 × 122 | vertical arm post with mount plate (user-identified) |

### Tilt mechanism / adjustment

| Part | Size (mm) | Notes |
|---|---|---|
| [`tilt-mech-housing-18`](thumbnails/tilt-mech-housing-18.png) | tilt mechanism housing |
| [`tilt-paddle-15`](thumbnails/tilt-paddle-15.png) | tilt paddle |
| [`paddle-lever-31`](thumbnails/paddle-lever-31.png) | 48 × 21 × 25 | adjustment paddle (left/right pair with 43) |
| [`paddle-lever-43`](thumbnails/paddle-lever-43.png) | 48 × 21 × 25 | adjustment paddle (mirror of 31) |

### Sourced parts (gas lift)

| Part | Size (mm) | Notes |
|---|---|---|
| [`gas-cylinder-42`](thumbnails/gas-cylinder-42.png) | 53 × 198 × 45 | gas lift cylinder (the `GAS PUMP` in the assembly guide) |
| [`gas-bushing-30`](thumbnails/gas-bushing-30.png) | 28 × 64 × 35 | gas-cylinder bushing/spacer |
| [`gas-bushing-33`](thumbnails/gas-bushing-33.png) | 28 × 64 × 35 | gas-cylinder bushing/spacer (identical to 30) |
| [`lumbar-bladder-mount-11`](thumbnails/lumbar-bladder-mount-11.png) | mechanical lumbar support bracket (legacy name) |

### Hardware (small pins / clips / grommets)

| Part | Size (mm) | Notes |
|---|---|---|
| [`pivot-pin-22`](thumbnails/pivot-pin-22.png) | 133 × 13 × 13 | pivot pin |
| [`pivot-pin-39`](thumbnails/pivot-pin-39.png) | 232 × 30 × 25 | longer pivot pin |
| [`bushing-stack-10`](thumbnails/bushing-stack-10.png) | bushing stack |
| [`cable-clip-7`](thumbnails/cable-clip-7.png) | cable clip |
| [`grommet-29`](thumbnails/grommet-29.png) | 27 × 29 × 26 | slotted grommet |

### Unidentified — to be updated

These visually didn't match anything obvious from the assembly guide. Renaming
welcome — file an issue or PR.

`part-1`, `part-5`, `part-6`, `part-17`, `part-21`, `part-26`, `part-28`,
`part-36`, `part-37`

## Naming convention

- `<descriptive-name>-<bodyN>.{step,stl}` — kebab-case descriptive name, then the
  original `BodyN` SolidWorks export number as a numeric suffix.
- The suffix gives us traceability back to the source export; rename freely
  as long as the suffix stays.
- Future versioned parts: `part-name-v2-<bodyN>.step` (versions take an
  explicit `vN`, not `final`, `final2`, …).
- One part = one base name. Avoid `armrest-pad-final.step`.

## Rules

- Always upload a STEP version next to the editable source file
- Put STL in `stl/` only when the part is final and tested
- Re-render thumbnails when geometry changes (see `tools/` — **TBU**)

## Units

Millimeters. Always.
