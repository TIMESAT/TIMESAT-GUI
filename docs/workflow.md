# Workflow

This page describes the full end-user workflow for a typical TIMESAT GUI session.

## 1. Start the Application

Launch TIMESAT GUI from the public executable release. The main window should show the workflow steps: Inputs, Parameters, Outputs, and Jobs.

![Main window placeholder](assets/screenshots/main-window-empty.png)

## 2. Load Input Data

Open **Inputs** and select a data file. Depending on the dataset, this may be a text file list, GeoTIFF image stack, CSV file, or Excel workbook.

If needed, use **Generate Filelist** to create an image list from a folder of GeoTIFF files.

## 3. Review the Preview

For image data, review the map preview. Select a layer, adjust colormap, opacity, and display range if needed.

For table data, review the table preview. TODO: confirm table preview workflow.

![Map preview placeholder](assets/screenshots/map-preview-loaded.png)

## 4. Select a Processing Region

For image data, use **Select Subarea** if you want to process only part of the image or if the dataset is too large to load fully.

TODO: confirm public guidance for when a subarea is required.

## 5. Load Data

Click **Load Data** after selecting the input and optional subarea. The Parameters, Outputs, and Jobs steps become available after data is loaded.

## 6. Configure Parameters

Open **Parameters** and select one fitting method. Review the time-series plot for a selected pixel or table series.

Use parameter changes carefully. The manual will include scientific guidance after defaults and recommendations are confirmed.

## 7. Configure Outputs

Open **Outputs** and choose:

- Output folder.
- Output time step.
- NoData value.
- Fitted time-series prefix.
- Phenology output prefix.
- Phenology outputs to create.

![Outputs placeholder](assets/screenshots/outputs-configuration.png)

## 8. Run Processing

Open **Jobs**.

Set CPU threads and memory limit as appropriate for your computer. TODO: confirm public guidance for these settings.

Click:

- **Run Subarea** to process the selected region.
- **Run Full Data** to process the full dataset.
- **Stop** to request stopping a running job.

![Jobs ready placeholder](assets/screenshots/jobs-ready.png)

## 9. Review Results

When the job finishes, review the output folder and the output log. Use the Phenology Parameters table to inspect calculated seasonal metrics when available.

![Phenology table placeholder](assets/screenshots/phenology-table.png)

TODO: confirm exact result review workflow for public sample data.
