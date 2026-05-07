# Input Data

The Inputs step is used to select the data that TIMESAT GUI will analyze. Supported formats and conventions must be confirmed before final publication.

![Inputs placeholder](assets/screenshots/inputs-file-selection.png)

## Supported Input Types

TIMESAT GUI appears to support the following input types:

- Text file lists containing GeoTIFF image paths.
- GeoTIFF image stacks.
- CSV tables.
- Excel workbooks.

TODO: confirm exact supported extensions, date conventions, and required table layout.

## Image File Lists

An image file list is a text file that lists GeoTIFF files in a time series. Each non-empty line should refer to one image.

TODO: confirm whether relative paths, absolute paths, or both are recommended.

The file names or paths must contain date information that TIMESAT GUI can interpret. TODO: confirm required date format.

## GeoTIFF Image Stacks

A GeoTIFF image stack stores multiple time steps as bands in one file.

TODO: confirm required band descriptions, date conventions, NoData handling, and coordinate reference system requirements.

## Table Inputs

CSV and Excel inputs are intended for table-based time-series workflows.

TODO: confirm required columns, date format, row and column orientation, and supported file sizes.

## Optional Quality or Mask Data

Quality or mask data can be used to assign weights to observations.

For image file list workflows, the quality input is expected to be a matching text file list. For image stack workflows, the quality input is expected to be a matching GeoTIFF. TODO: confirm exact requirements.

Quality data must match the input time steps. TODO: confirm matching rules and supported quality values.

## Optional Land Cover Data

Land cover input is expected to be a GeoTIFF. TODO: confirm supported workflows, category meanings, and limitations.

## Generate Filelist

The **Generate Filelist** tool helps create text file lists from folders of GeoTIFF files.

![Filelist generator placeholder](assets/screenshots/filelist-generator.png)

The dialog includes:

- VI pattern.
- VI folder.
- Optional QA list.
- QA pattern.
- QA folder.
- Exclude pattern.

Use public sample data and neutral folders when preparing documentation screenshots.

## Large Datasets and Subareas

For large image datasets, TIMESAT GUI may require a smaller processing region before data can be loaded. Use **Select Subarea** to draw a rectangle on the map, then click **Load Data**.

TODO: confirm the public guidance for maximum practical dataset size.
