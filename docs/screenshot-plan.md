# Screenshot Plan

This plan lists public documentation screenshots to capture from the public TIMESAT GUI release. Do not invent screenshots. Use only verified screenshots captured from the public release application.

All screenshot files should be stored under `docs/assets/screenshots/`.

## Screenshot Privacy Rules

Screenshots must not show:

- Private repository names.
- Local user names.
- Private file paths.
- Unpublished project folders.
- Credentials or tokens.
- Internal test data names.

Use public sample data and neutral paths where possible. TODO: confirm the official public sample dataset and preferred neutral example paths.

## Markdown Image Paths

When Markdown pages under `docs/` refer to screenshots, use relative paths from the page location. For example:

```markdown
![Main window](assets/screenshots/main-window-empty.png)
```

Do not use repository-root paths such as:

```markdown
![Main window](docs/assets/screenshots/main-window-empty.png)
```

| Suggested file name | Documentation page | GUI screen or dialog to capture | Steps to reproduce the screen | What must be visible in the screenshot | Priority |
| --- | --- | --- | --- | --- | --- |
| `docs/assets/screenshots/main-window-empty.png` | `docs/index.md` | Main window immediately after launch | Launch TIMESAT GUI and do not load data. | Application title, workflow steps, empty map or preview area, time-series area, and status bar. | required |
| `docs/assets/screenshots/inputs-file-selection.png` | `docs/input-data.md` | Inputs step with data selection controls | Open the Inputs step. | Data File, Quality File, Landcover File, Generate Filelist, Load Data, and Processing Region controls. | required |
| `docs/assets/screenshots/filelist-generator.png` | `docs/input-data.md` | Generate Filelist dialog | In the Inputs step, select Generate Filelist. | VI pattern, VI folder, optional QA controls, Exclude field, and Generate button. | recommended |
| `docs/assets/screenshots/filelist-confirmation.png` | `docs/input-data.md` | Filelist creation confirmation dialog | Use a public sample folder and generate a VI file list. TODO: confirm sample data. | Count summary for matched and unmatched files, and the confirmation question. | optional |
| `docs/assets/screenshots/map-preview-loaded.png` | `docs/quick-start.md` | Loaded image preview | Load a public image file list or GeoTIFF stack. | Map preview, selected layer controls, row and column controls, color legend, and map toolbar. | required |
| `docs/assets/screenshots/table-preview-loaded.png` | `docs/input-data.md` | Loaded table preview | Load a public CSV or Excel example. TODO: confirm table input sample. | Table preview, row and column count, and series navigation controls. | recommended |
| `docs/assets/screenshots/subarea-selection.png` | `docs/workflow.md` | Processing region selection | Load image-based data, select Select Subarea, and draw a rectangle on the map. | Selected rectangle and the status text showing selected 1-based coordinates. | recommended |
| `docs/assets/screenshots/parameters-basic.png` | `docs/parameters.md` | Parameters step with main controls | Load data, open Parameters, and leave advanced pre-processing collapsed. | Data Range, Weights, Fitting Method, Envelope Processing, Season Detection, and plot display controls. | required |
| `docs/assets/screenshots/parameters-advanced.png` | `docs/parameters.md` | Advanced pre-processing options | Open Parameters and expand More under Pre-processing. | Outlier detection, Availability Window, Base Level, and the More/Less toggle state. | recommended |
| `docs/assets/screenshots/parameters-weights.png` | `docs/parameters.md` | Quality weight table | Load compatible quality data. TODO: confirm public quality sample. | Weight mode selector, weight table columns, Add Row, and Remove Row. | recommended |
| `docs/assets/screenshots/time-series-plot.png` | `docs/workflow.md` | Time-series plot after selecting a pixel or table series | Load data, select a valid pixel or series, choose one fitting method, and allow the plot to update. | Raw data, fitted curve, optional weight or season markers, and Save Time Series control. | required |
| `docs/assets/screenshots/histogram-dialog.png` | `docs/workflow.md` | Histogram dialog | Load image data and open the histogram view from the map tools. TODO: confirm exact toolbar action. | Histogram image and Save Image button. | optional |
| `docs/assets/screenshots/outputs-configuration.png` | `docs/output-results.md` | Outputs step | Open Outputs after loading data. | Output Folder status, Output Time Step, NoData Value, Yfit Prefix, VPP Prefix, and VPP Outputs table. | required |
| `docs/assets/screenshots/vpp-output-selection.png` | `docs/output-results.md` | VPP output selection table | Open Outputs and scroll to VPP Outputs if needed. | Enable, Source, and Output Name columns, plus Select All and Reset Names buttons. | recommended |
| `docs/assets/screenshots/jobs-ready.png` | `docs/workflow.md` | Jobs step ready state | Select one fitting method and a valid output folder, then open Jobs. | CPU Threads, Memory Limit, Ready to run status, Run Subarea, Run Full Data, Stop, and Output Log. | required |
| `docs/assets/screenshots/jobs-validation-error.png` | `docs/faq.md` | Jobs step blocked by missing configuration | Open Jobs before selecting a fitting method or output folder. | Status message explaining that a fitting method and valid output folder are required. | recommended |
| `docs/assets/screenshots/jobs-running.png` | `docs/workflow.md` | Running job | Start a run using public sample data. TODO: confirm safe sample size. | Running status, disabled run buttons, Stop button, and output log messages. | recommended |
| `docs/assets/screenshots/jobs-completed.png` | `docs/output-results.md` | Completed job | Run a small public sample to completion. TODO: confirm sample data. | Completed successfully status and final output log lines. | recommended |
| `docs/assets/screenshots/phenology-table.png` | `docs/output-results.md` | Phenology Parameters table | Generate a plotted fit or completed run that populates phenology results. TODO: confirm reproducible route. | Phenology Parameters heading, Save button, and columns such as SOS Date, EOS Date, Peak Date, Amplitude, LINT, and SINT. | required |
| `docs/assets/screenshots/save-settings-dialog.png` | `docs/workflow.md` | Save Settings dialog | Open File > Save Settings. | File menu action or save dialog for settings JSON. | recommended |
| `docs/assets/screenshots/load-settings-dialog.png` | `docs/workflow.md` | Load Settings dialog | Open File > Load Settings. | Load settings dialog accepting JSON or GeoJSON settings. TODO: confirm GeoJSON use case. | optional |
| `docs/assets/screenshots/about-dialog.png` | `docs/index.md` | About TIMESAT dialog | Open Help > About TIMESAT. | Version, application description, website, and attribution text. | optional |
| `docs/assets/screenshots/license-dialog.png` | `docs/installation.md` | License dialog | Open Help > View License. | Read-only license window. | recommended |
