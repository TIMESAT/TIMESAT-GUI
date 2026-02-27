# TIMESAT GUI

TIMESAT GUI is a native Qt6 desktop application for configuring, running, and
visualizing TIMESAT time-series analyses.

This repository is the **authoritative (official) distribution channel** for
the closed-source GUI and its official release artifacts.

## Download

Download the latest desktop application from GitHub Releases:

- [https://github.com/TIMESAT/TIMESAT-GUI/releases/latest](https://github.com/TIMESAT/TIMESAT-GUI/releases/latest)

## Licensing

This GUI is distributed under a **Proprietary, Research‑Only** license.
See `LICENSE` for full terms.

### Third‑Party Notices (Qt / PySide6)

Qt for Python (PySide6) is used under the LGPLv3 in the official builds.
The LGPLv3 text is bundled in the app as `LGPL-3.0.txt`.

Users may replace the Qt/PySide6 shared libraries in the app bundle.
Typical locations:

- macOS: `TIMESAT.app/Contents/Frameworks/`
- Windows: `dist/TIMESAT/` (DLLs)
- Linux: `dist/TIMESAT/` (shared objects)

See [THIRD_PARTY_NOTICES.txt](https://github.com/TIMESAT/TIMESAT-GUI/blob/main/THIRD_PARTY_NOTICES.txt) for additional dependencies and licenses.

## Citation

If you use TIMESAT in your research, please cite the corresponding release:

[https://doi.org/10.5281/zenodo.17369757](https://doi.org/10.5281/zenodo.17369757)

## Documentation Website (GitHub Pages)

The TIMESAT 4 manual is available in this repository at:

- `docs/index.md`

To publish it on GitHub Pages:

1. Push this branch to GitHub.
2. Open repository `Settings` -> `Pages`.
3. In `Build and deployment`, set `Source` to `Deploy from a branch`.
4. Select branch `main` (or your target branch) and folder `/docs`.
5. Save and wait 1-2 minutes for deployment.

After deployment, the page will be available at:

- `https://<your-org-or-user>.github.io/<repo-name>/`

## Acknowledgments

- [https://www.nateko.lu.se/TIMESAT](https://www.nateko.lu.se/TIMESAT)
