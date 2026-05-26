# How to Contribute

Thanks for helping. Keep it simple.

## Before You Push

Install Git LFS once. We use it for CAD, STL, STEP, and PDF.

```
brew install git-lfs       # macOS
sudo apt install git-lfs   # Linux
git lfs install
```

Then `git add` and `git commit` work normally. See `docs/git-lfs.md`.

## Upload CAD

- Put editable files in `cad/source/` (keep the original format: `.SLDPRT`, `.f3d`, `.FCStd`, etc.)
- Always export and upload a `.step` to `cad/step/` so anyone can open it
- Export `.stl` to `cad/stl/` for 3D printing
- Re-render a `cad/thumbnails/<part>.png` when geometry changes

File name format: `part-name-<bodyN>.step` (kebab-case + numeric body-export suffix).
For versioned parts: `part-name-v2-<bodyN>.step`.

## Write Assembly Notes

- The canonical assembly is the bundled PDF (`docs/assembly-guide.pdf`).
- Companion notes in `assembly/README.md`.
- Photos in `assembly/photos/`, named `step-01.jpg`, `step-02.jpg`, …

## Rules

- No big words. Write so a beginner can follow.
- Test before you push. If you can, print or build it yourself first.
- Commit messages: short and clear. One topic per Pull Request.

## License of Your Contributions

By sending a Pull Request you agree your contribution is licensed under the
same terms as the project: **CC BY-NC-SA 4.0** (free for personal/community
use, not for commercial use without permission). See [LICENSE.md](LICENSE.md)
for the plain-English summary or [LICENSE](LICENSE) for the full legal text.

## Issues

Open an Issue if:
- A file is missing or broken
- Instructions don't work
- You want to suggest a feature
- You found a bug

Use the templates in `.github/ISSUE_TEMPLATE/`.
