# STL Files

Ready to 3D print.

## Print Settings (default)

- Material: PETG (preferred for load-bearing chair parts) or PLA for non-structural housings
- Layer height: 0.2 mm
- Infill: 40% (structural: armrest-yoke, lumbar-mount); 25% (housing)
- Walls: 4 for structural, 3 for housings
- Supports: only where noted in the file name (e.g. `armrest-yoke_v1_supports.stl`)

## Structural vs cosmetic

Anything in the load path (armrest yoke, lumbar mount, headrest slider) must be PETG, ABS, or nylon — **not PLA**. PLA creeps under sustained load and the part will deform after a few weeks of use.

Override per part if needed — add a `print-notes.md` next to the STL.
