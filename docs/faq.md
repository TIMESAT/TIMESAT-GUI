# FAQ

This page lists common user questions and troubleshooting notes for the public TIMESAT GUI release.

## Which input formats are supported?

The GUI appears to support text file lists, GeoTIFF image stacks, CSV files, and Excel workbooks.

TODO: confirm exact supported extensions and input schemas.

## Why is the Quality File control disabled?

Quality or mask input is available only for compatible input workflows. Load a supported image input first, then select the quality file.

TODO: confirm supported quality formats.

## Why do I need to select a subarea?

Large image datasets may need a smaller processing region before loading or running. Use **Select Subarea**, draw a rectangle on the map, and click **Load Data**.

TODO: confirm the public threshold and recommended sample sizes.

## Why can I not run a job?

The Jobs step requires:

- Exactly one fitting method.
- A valid existing output folder.
- Loaded input data.

If the run buttons are disabled, check the status message in the Jobs step.

## What does “Output Folder must be an existing directory” mean?

Create the folder first, then select it in the Outputs step. The GUI expects the output folder to already exist.

## What should I do if dates cannot be parsed?

Check that input file names or stack band labels contain dates in the expected format.

TODO: confirm the required public date format.

## What should I do if quality data does not match?

Make sure the quality data has the same time steps and compatible dimensions as the input data.

TODO: confirm exact matching rules.

## Can I use land cover data?

Land cover input is planned for documentation, but supported workflows and limitations need confirmation.

TODO: confirm land cover support.

## What should I include in an issue report?

Include:

- TIMESAT GUI version.
- Operating system.
- Input type.
- A short description of what happened.
- Steps to reproduce the problem.
- Any visible error message.
- Public sample data or a minimal non-private example, if possible.

Do not include private paths, credentials, unpublished datasets, or screenshots that reveal private information.
