# Output Results

The Outputs and Jobs steps control where results are written and which output variables are produced.

![Outputs placeholder](assets/screenshots/outputs-configuration.png)

## Output Folder

Select an existing output folder before running a job. The Jobs step will not run until the output folder is valid.

Use a neutral output folder for examples and screenshots, such as `~/TIMESAT-output/`.

## Output Options

The output options include:

- Output Time Step.
- NoData Value.
- Yfit Prefix.
- VPP Prefix.

TODO: confirm recommended values for the public sample dataset.

## Phenology Outputs

The VPP Outputs table lets users enable or disable phenology outputs and edit output names.

Use **Select All** to enable all listed phenology outputs. Use **Reset Names** to restore default output names.

TODO: confirm final list and definitions of available phenology output sources.

## File Naming

The GUI indicates that files may be written using a pattern similar to:

`<prefix>_<name>_<year>_season_<n>.tif`

TODO: confirm whether this pattern applies to all raster outputs and all fitting methods.

## Phenology Parameters Table

The Phenology Parameters table displays seasonal metrics such as start of season, end of season, peak timing, amplitude, and integrals.

![Phenology table placeholder](assets/screenshots/phenology-table.png)

Use **Save** to export the table when results are available. TODO: confirm exported CSV columns and file name.

## Saved Time-Series Data

Use **Save Time Series** in the plot area to save data for the current plotted series.

TODO: confirm exact files, columns, and naming convention.

## Job Log

The Jobs step shows an output log while processing runs. Use this log to check progress and diagnose run failures.

TODO: confirm whether log files are also written to disk.
