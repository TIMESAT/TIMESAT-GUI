# TIMESAT GUI Documentation Plan

This document defines the first public documentation plan for TIMESAT GUI. It is a planning document only and is not the full user manual.

All uncertain items are marked as `TODO: confirm`.

## 1. Proposed Manual Structure

The public manual should use the following structure:

- `index.md`: overview, intended audience, citation, and links to the main documentation pages.
- `installation.md`: where to download official executable releases, supported operating systems, installation steps, first launch, and license notes.
- `quick-start.md`: a minimal end-to-end workflow from input selection to result review.
- `input-data.md`: supported input data types, file list preparation, optional quality data, optional land cover data, and table input requirements.
- `sample-data.md`: public sample datasets for quick-start workflows, screenshots, and reproducible examples.
- `parameters.md`: user-facing TIMESAT parameters, recommended defaults, and guidance for selecting fitting and season detection options.
- `workflow.md`: detailed workflow for loading data, selecting a processing region, adjusting parameters, choosing outputs, and running jobs.
- `output-results.md`: expected output files, fitted time-series outputs, phenology parameter outputs, saved time-series data, logs, and interpretation notes.
- `faq.md`: common questions, troubleshooting, and known limitations.
- `changelog.md`: release notes for public executable releases.
- `screenshot-plan.md`: planned screenshots and capture requirements.

## 2. Main User Workflow

The main user workflow should be documented as:

1. Download and launch the official TIMESAT GUI executable.
2. Open the application and review the main workflow steps: Inputs, Parameters, Outputs, and Jobs.
3. Select an input data file. Supported user-facing choices appear to include text file lists, GeoTIFF image stacks, CSV files, and Excel workbooks. TODO: confirm exact supported formats and required column conventions.
4. If needed, generate a file list from folders containing vegetation index and optional quality GeoTIFF files.
5. Review the map preview or table preview after loading the input.
6. For image-based data, select a layer for preview, adjust colormap and display range if needed, and optionally choose a processing subarea.
7. Load the selected data or subarea into the analysis session.
8. Configure TIMESAT parameters in the Parameters step.
9. Select exactly one fitting method before running: Double Logistic or Smoothing Spline. TODO: confirm whether additional fitting combinations should be exposed in the public manual.
10. Review the time-series plot for the selected pixel or table series.
11. Configure the output folder, output time step, NoData value, output name prefixes, and selected phenology outputs.
12. Run either the selected subarea or the full data, depending on the intended processing extent.
13. Monitor the output log and job status.
14. Review output files and optionally save time-series data or phenology parameters from the GUI.

## 3. Required Input Data

The manual should explain the following input categories:

- Image file list: a text file listing GeoTIFF images to process as a time series. TODO: confirm whether relative paths, absolute paths, or both are recommended for public examples.
- GeoTIFF image stack: a multi-band GeoTIFF where bands represent the temporal sequence. TODO: confirm required band naming/date conventions.
- Table input: CSV or Excel table data for time-series analysis. TODO: confirm required columns, date format, and series layout.
- Optional quality or mask data: supported for image file list and image stack workflows. TODO: confirm valid quality value meanings and recommended weight mapping.
- Optional land cover GeoTIFF: available for some image-based workflows. TODO: confirm supported input modes and how classes should be interpreted.

The input-data page should also document:

- Supported file extensions.
- Expected date information in file names or bands.
- Coordinate reference system requirements for map display. TODO: confirm.
- NoData handling.
- Data size considerations and when users should select a subarea.
- Use of the file list generator, including vegetation index folders, optional quality folders, include/exclude patterns, and saved text file lists.

## Public Sample Data

Public sample data is needed before writing the full quick-start guide, capturing final screenshots, or publishing reproducible examples. The sample data should be safe to redistribute, small enough for first-time users, and representative of the main supported workflows.

The sample-data page should describe:

- Where users can download the public sample data.
- Which documentation examples use each sample dataset.
- Which screenshots can be reproduced from each sample dataset.
- Expected run time and output size for a small example. TODO: confirm.
- Any license, citation, or attribution requirements for the sample data. TODO: confirm.

The first documentation draft should use public sample data and neutral example paths wherever possible. TODO: confirm the official sample dataset.

## 4. User-Facing Parameters

The parameters page should organize controls by visible GUI section:

### Pre-processing

- Data Range: lower and upper valid values used for processing and plotting. TODO: confirm exact effect on fitting and outputs.
- More/Less advanced options:
  - Enable outlier detection.
  - Availability Window.
  - Base Level.

### Weights

- Weight mode:
  - Intervals with minimum, maximum, and weight columns.
  - Value map with value and weight columns.
- Add Row and Remove Row controls.
- Quality weights are available only when quality input has been loaded. TODO: confirm recommended quality weights for common products.

### Fitting Method

- Double Logistic (DL).
- Smoothing Spline (SP).
- Smoothing parameter for Smoothing Spline.
- The Jobs step requires exactly one fitting method before processing.

### Envelope Processing

- Iterations.
- Strength.
- TODO: confirm plain-language guidance for scientific users.

### Season Detection

- Seasonal Method/Par:
  - Irregular season.
  - Regular season.
- Start Method:
  - Seasonal amplitude method.
  - Absolute value method.
  - Relative amplitude method.
  - STL (Loess) method.
- Start/End Cutoff.
- TODO: confirm recommended defaults for common vegetation index workflows.

### Plot Display Options

- Raw data.
- Weight.
- Season start/end.
- Season details.
- Coarse season.
- Save Time Series.

### Output Configuration

- Output Folder.
- Output Time Step.
- NoData Value.
- Yfit Prefix.
- VPP Prefix.
- VPP Outputs table with Enable, Source, and Output Name columns.
- Select All and Reset Names.

### Job Configuration

- CPU Threads.
- Memory Limit.
- Run Subarea.
- Run Full Data.
- Stop.
- Output Log.

## 5. Expected Outputs

The output-results page should describe:

- Fitted time-series outputs, using the configured fitted-output prefix. TODO: confirm exact file names and formats.
- Phenology parameter raster outputs, using the configured VPP prefix and selected output names.
- Output file naming pattern: `<prefix>_<name>_<year>_season_<n>.tif`. TODO: confirm whether this pattern applies to all raster outputs.
- Saved phenology parameter CSV from the Phenology Parameters table.
- Saved time-series data from the plot area. TODO: confirm exact files produced when saving time-series data.
- Job output log shown in the Jobs step.
- Settings JSON files saved from the File menu.
- TODO: confirm whether any auxiliary files, temporary files, or metadata files should be documented.

## 6. Common User Errors

The FAQ and troubleshooting content should cover:

- Missing input path or selected file not found.
- Empty text file list.
- File list entries that refer to missing image files.
- File names or bands where dates cannot be parsed. TODO: confirm public date format guidance.
- Unsupported input file format.
- Quality file selected before a compatible input is loaded.
- Quality file type does not match the input workflow.
- Quality timestamps or dimensions do not match the input data.
- Land cover file type is not GeoTIFF.
- Land cover input is not supported for the selected input mode. TODO: confirm current limitation.
- Dataset or selected subarea is too large; the user must select a smaller subarea.
- Selected point is outside the loaded image or stack bounds.
- Output folder is missing or does not exist.
- More than one fitting method is selected, or no fitting method is selected.
- Attempting to save phenology parameters before any results are available.
- Attempting to save time-series data before a fit has been plotted.
- Attempting to start a job while another job is already running.
- Job finishes with a non-zero code. TODO: confirm recommended user actions for common run failures.

## 7. Missing Information That Needs Human Confirmation

The following items require confirmation before writing the full manual:

- Supported operating systems and exact executable package names.
- Installation and first-launch steps for each operating system.
- Whether command-line launch instructions should be included for public users.
- Exact supported input schemas for CSV and Excel data.
- Required date formats for image file lists and GeoTIFF stack bands.
- Recommended sample datasets for public examples.
- Public sample data location, license, and citation requirements.
- Meaning of quality or mask values and recommended weight tables.
- Land cover support, category behavior, and limitations.
- Recommended default parameter values for common scientific workflows.
- Plain-language guidance for envelope processing and season detection settings.
- Exact list and definitions of VPP output sources.
- Exact output file names and output folder structure.
- Whether batch jobs are supported for table inputs or only image-based inputs.
- Known limitations for large datasets and subarea thresholds.
- Citation text and DOI format to use in all public pages.
- License language for downloadable executables.
- Contact and support channel.

## 8. Recommended Screenshots

Recommended screenshots should be captured only from the public release application. Do not create artificial screenshots.

- `docs/assets/screenshots/main-window-empty.png`: main window at launch.
- `docs/assets/screenshots/inputs-file-selection.png`: Inputs step with input file controls.
- `docs/assets/screenshots/filelist-generator.png`: Generate Filelist dialog.
- `docs/assets/screenshots/map-preview-loaded.png`: loaded image layer with map preview.
- `docs/assets/screenshots/table-preview-loaded.png`: loaded table input preview. TODO: confirm table workflow.
- `docs/assets/screenshots/subarea-selection.png`: selected processing region.
- `docs/assets/screenshots/parameters-basic.png`: main parameter controls.
- `docs/assets/screenshots/parameters-weights.png`: quality weights controls with example quality data. TODO: confirm suitable public sample.
- `docs/assets/screenshots/time-series-plot.png`: time-series plot with fit and optional season markers.
- `docs/assets/screenshots/outputs-configuration.png`: output folder, output naming, and VPP output selection.
- `docs/assets/screenshots/jobs-ready.png`: Jobs step ready to run.
- `docs/assets/screenshots/jobs-running.png`: output log while a job is running.
- `docs/assets/screenshots/phenology-table.png`: Phenology Parameters table after plotting or running. TODO: confirm best reproducible route.
- `docs/assets/screenshots/settings-menu.png`: File menu with Save Settings and Load Settings.
