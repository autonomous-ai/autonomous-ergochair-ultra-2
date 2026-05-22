# PCB

Printed circuit board files.

Upload:
- KiCad PCB source (`.kicad_pcb`)
- Gerber zip ready for fab (e.g. `chair-main_v1_gerber.zip`)
- 3D render PNG of top and bottom (nice to have)

Naming: `board-name_v1.kicad_pcb`, `board-name_v1_gerber.zip`

Boards expected here:
- `chair-main_v1` — main controller (ESP32-S3, sensor I²C bus, pump/valve MOSFETs, LED ring header)
- `chair-power_v1` — charging + boost
