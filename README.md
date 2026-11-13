# TIMESAT GUI

TIMESAT GUI is a native Qt6 desktop application for configuring, running, and
visualizing TIMESAT time-series analyses.

This repository is the **authoritative (official) distribution channel** for
the closed-source GUI and its official release artifacts.

## Download

Download the latest desktop application from GitHub Releases:

- [https://github.com/TIMESAT/TIMESAT-GUI/releases/latest](https://github.com/TIMESAT/TIMESAT-GUI/releases/latest)

## Download satellite time series from Google Earth Engine

Use the [Time Series Explorer](https://caizhanzhang.users.earthengine.app/view/time-series-explorer)
in your web browser to obtain a CSV time series for analysis in TIMESAT GUI.
Internet access is required.

1. Open the link above and select the satellite product, vegetation index and date range.
2. Select a point on the map and wait for its time-series chart to appear.
3. Click the icon in the upper-right corner of the chart to open the chart view.
4. Choose **Download CSV** and save the file to your computer.
5. In TIMESAT GUI, open **Inputs**, use **Browse...** under **Input Data** to select
   the saved CSV, then click **Load Data**.

Before importing, check that the CSV has a header row, dates in the first column
(preferably `YYYY-MM-DD`) and numeric time-series values in the remaining columns.
Sort observations by date and remove rows with missing dates or values if necessary.

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

[https://doi.org/10.5281/zenodo.19881054](https://doi.org/10.5281/zenodo.19881054)

## Acknowledgments

- [https://www.nateko.lu.se/TIMESAT](https://www.nateko.lu.se/TIMESAT)
