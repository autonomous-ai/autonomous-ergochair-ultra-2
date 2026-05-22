# CAD Files

All 3D and 2D design files for the chair.

## Folders

- `concept/` — early sketches, ideas, screenshots, references
- `source/` — editable CAD (Fusion 360, FreeCAD, SolidWorks, OnShape exports)
- `step/` — STEP files. Open in any CAD tool. Use this if you want to edit but don't have the source software.
- `stl/` — STL files ready to 3D print
- `drawings/` — 2D drawings with dimensions (PDF)

## Major Parts

| Part | Type | Notes |
|---|---|---|
| `seat-pan` | molded / CNC | foam + cover assembly mounts to bottom |
| `back-frame` | bent steel + mesh | takes lumbar bladder behind mesh |
| `headrest` | adjustable | slides on twin posts |
| `armrest-yoke` | 3D printable | takes 4D arm pad |
| `lumbar-bladder-mount` | 3D printable | holds bladder + pump line clip |
| `controller-housing` | 3D printable | ESP32 + PSU + IMU mounting |
| `caster-spider` | metal (sourced) | 5-arm chair base |
| `gas-cylinder` | sourced | class-4, 80mm stroke |

## Rules

- Always upload a STEP version next to the source file
- Put STL in `stl/` only when the part is final and tested
- Name files: `part-name_v1.step`, `part-name_v2.step`
- One part = one base name. Use version numbers, not "final", "final2", "real-final".

## Units

Millimeters. Always.
