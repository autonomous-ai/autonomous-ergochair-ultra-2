# Autonomous ErgoChair Ultra 2

A smart, sensor-driven ergonomic chair you can build at home. Open hardware, open software. No paywall.

Whether you're learning, experimenting, or building your own version, the goal is to make advanced smart hardware accessible to everyone.

## What is this?

The ErgoChair Ultra 2 is a high-back ergonomic chair with:

- Powered lumbar inflate / deflate
- Posture sensing (seat-pan pressure mat + back IMU)
- Sit-time tracking and stand-up reminders
- BLE pairing with a phone app (also exposes Wi-Fi for OTA)
- Manual recline, 4D armrests, adjustable headrest — all the mechanical features of a premium ergonomic chair

Everything in this repo: the CAD, the electronics, the firmware, the BOM, and the step-by-step build guide. No paywall.

## Repo Layout

```
cad/            3D design files
  concept/      Sketches, ideas, early drafts            [to be updated]
  source/       Editable CAD (Fusion 360, FreeCAD, ...)  [to be updated]
  step/         STEP files (works in any CAD tool)       — 36 parts
  stl/          STL files ready to 3D print              — 36 parts
  thumbnails/   Isometric PNG previews, one per STL      — 36 images
  drawings/     2D drawings, dimensions (PDF)            [to be updated]

electronics/    All electronics stuff
  schematics/   Circuit diagrams                         [to be updated]
  pcb/          PCB design files (KiCad, Gerber)         [to be updated]
  bom/          Parts list for electronics               — parts.csv present
  wiring/       Wiring diagrams, pinouts                 [to be updated]

firmware/       Code that runs on the chair controller   [to be updated]

assembly/       How to build it
  README.md     Step-by-step build instructions          — draft, present
  photos/       Step-by-step photos                      [to be updated]
  videos/       Build videos (links or files)            [to be updated]

docs/           Extra docs, guides, notes
  assembly-guide.pdf   Original Autonomous product guide — present
  git-lfs.md           How to use Git LFS                — present
  (architecture, posture-algo, BLE, OTA, ...)            [to be updated]

bom/            Full bill of materials                   — parts.csv present (suppliers TBU)
tools/          Scripts, helper tools                    [to be updated]
examples/       Example apps and integrations            [to be updated]
```

## Status at a Glance

| Area | State |
|---|---|
| Mechanical CAD (STEP / STL / thumbnails) | **36 parts uploaded** — see [`cad/README.md`](cad/README.md) |
| Product assembly guide (PDF) | **Uploaded** → [`docs/assembly-guide.pdf`](docs/assembly-guide.pdf) |
| Mechanical BOM | Skeleton CSV present; supplier links **to be updated** |
| Editable CAD source files | **To be updated** |
| 2D drawings | **To be updated** |
| Electronics schematics / PCB / wiring | **To be updated** |
| Firmware | **To be updated** |
| Build photos / videos | **To be updated** |
| Extra docs (architecture, posture algo, BLE, OTA) | **To be updated** |

`TBU` / `to be updated` markers throughout the repo point at sections that still need uploaded content. Placeholder READMEs describe what each section is for.

## Big Files: Git LFS

This repo uses **Git LFS** for CAD, STL, STEP, PCB, video, and PDF.
Install LFS once before you clone or push: see [docs/git-lfs.md](docs/git-lfs.md).

Quick:
```
brew install git-lfs     # macOS
git lfs install
git clone https://github.com/autonomous-ai/autonomous-ergochair-ultra-2.git
```

## Want to Build One?

1. Read [assembly/README.md](assembly/README.md) and the bundled [`docs/assembly-guide.pdf`](docs/assembly-guide.pdf) (original Autonomous product guide)
2. Browse parts visually in [cad/thumbnails/](cad/thumbnails/) — one PNG per CAD part
3. Get the parts from [bom/](bom/)
4. Print or order CAD parts from [cad/stl/](cad/stl/) or [cad/step/](cad/step/)
5. Build the electronics in [electronics/](electronics/) *(content TBU)*
6. Flash firmware from [firmware/](firmware/) *(content TBU)*
7. Follow the assembly steps

## Want to Help?

- Upload your CAD to [cad/source/](cad/source/) and export STEP + STL
- Add photos to [assembly/photos/](assembly/photos/)
- Open an Issue if something is broken or unclear
- Send a Pull Request with fixes or improvements

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

- Hardware, CAD, docs → **[CC BY-NC-SA 4.0](LICENSE)**
- Firmware, code → **[PolyForm Noncommercial 1.0.0](LICENSE-CODE)**

Plain-English summary: **[LICENSE.md](LICENSE.md)**
