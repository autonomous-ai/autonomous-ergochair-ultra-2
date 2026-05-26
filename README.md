# Autonomous ErgoChair Ultra 2

Open-hardware design files for the ErgoChair Ultra 2 — a fully mechanical
ergonomic chair. CAD, drawings, BOM, and assembly guide. No paywall.

## What is this?

A high-back ergonomic chair with:

- Mesh back with adjustable headrest
- Synchro-tilt mechanism with locking + adjustable tension
- Manual lumbar support
- Seat depth + seat height adjustment
- 4D armrests (height, width, depth, swivel)
- Class-4 gas lift on a 5-arm caster base

No sensors, no MCU, no firmware — this is a passive mechanical chair.

## Repo Layout

```
cad/            3D design files
  concept/      Sketches, ideas, references               [to be updated]
  source/       Editable CAD (SolidWorks, Fusion, ...)    [to be updated]
  step/         STEP files (any CAD tool)                 — 36 parts
  stl/          STL files for 3D printing                 — 36 parts
  thumbnails/   Isometric PNG previews                    — 36 images
  drawings/     2D drawings with dimensions (PDF)         [to be updated]

assembly/       How to put the chair together
  README.md     Step-by-step build notes                  — present
  photos/       Step-by-step photos                       [to be updated]
  videos/       Build videos                              [to be updated]

docs/           Extra docs and references
  assembly-guide.pdf   Original product assembly guide   — present
  git-lfs.md           How to use Git LFS                 — present

bom/            Bill of materials (parts to source)
  parts.csv     Skeleton list                             — supplier links TBU

tools/          Helper scripts (e.g. STL → thumbnail)     [to be updated]
```

## Status

| Area | State |
|---|---|
| Mechanical CAD (STEP / STL / thumbnails) | **36 parts uploaded** — see [`cad/README.md`](cad/README.md) |
| Product assembly guide (PDF) | **Uploaded** → [`docs/assembly-guide.pdf`](docs/assembly-guide.pdf) |
| Mechanical BOM | Skeleton CSV present; supplier links **to be updated** |
| Editable CAD source files | **To be updated** |
| 2D drawings | **To be updated** |
| Build photos / videos | **To be updated** |

## Big Files: Git LFS

This repo uses **Git LFS** for STEP, STL, and PDF.
Install LFS once before you clone or push: see [docs/git-lfs.md](docs/git-lfs.md).

```
brew install git-lfs     # macOS
git lfs install
git clone https://github.com/autonomous-ai/autonomous-ergochair-ultra-2.git
```

## Want to Build One?

1. Read the bundled [`docs/assembly-guide.pdf`](docs/assembly-guide.pdf) for
   the canonical assembly steps.
2. Browse parts visually in [cad/thumbnails/](cad/thumbnails/).
3. Source the parts using [bom/parts.csv](bom/parts.csv) (suppliers TBU).
4. Print or order the CAD parts from [cad/stl/](cad/stl/) or
   [cad/step/](cad/step/).
5. Follow the assembly steps.

## Want to Help?

- Upload your editable CAD to [cad/source/](cad/source/) and export STEP + STL
- Add build photos to [assembly/photos/](assembly/photos/)
- Open an Issue if something is broken or unclear
- Send a Pull Request with fixes or improvements

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## License

Hardware, CAD, and docs → **[CC BY-NC-SA 4.0](LICENSE)**

Plain-English summary: **[LICENSE.md](LICENSE.md)**
