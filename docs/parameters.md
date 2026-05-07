# Parameters

The Parameters step controls how TIMESAT fits the time series and detects seasonal metrics. This page describes the visible user controls. It does not define final scientific recommendations.

![Parameters placeholder](assets/screenshots/parameters-basic.png)

TODO: confirm recommended defaults for common vegetation index workflows.

## Pre-processing

### Data Range

The data range defines lower and upper valid values for the analysis and plot display. TODO: confirm exact effect on fitting and output generation.

### Advanced Pre-processing

Use **More** to show additional pre-processing controls:

- Enable outlier detection.
- Availability Window.
- Base Level.

TODO: confirm plain-language definitions and recommended values.

## Weights

Weights can be configured when quality information is available.

Available modes:

- Intervals: minimum, maximum, and weight.
- Value map: value and weight.

Use **Add Row** and **Remove Row** to edit the weight table.

TODO: confirm recommended quality weight tables for public sample data.

## Fitting Method

Select exactly one fitting method before running a job:

- **Double Logistic (DL)**.
- **Smoothing Spline (SP)**.

For Smoothing Spline, set the smoothing parameter. TODO: confirm recommended values and valid interpretation.

## Envelope Processing

Envelope processing includes:

- Iterations.
- Strength.

TODO: confirm scientific guidance and recommended settings.

## Season Detection

Season detection includes:

- Seasonal method: irregular season or regular season.
- Seasonal parameter.
- Start method:
  - Seasonal amplitude method.
  - Absolute value method.
  - Relative amplitude method.
  - STL (Loess) method.
- Start and end cutoff values.

TODO: confirm recommended settings for typical datasets.

## Plot Display Options

The plot area can show:

- Raw data.
- Weight.
- Season start/end.
- Season details.
- Coarse season.

Use **Save Time Series** to export data from the current plotted series. TODO: confirm exact exported files.

![Time-series plot placeholder](assets/screenshots/time-series-plot.png)
