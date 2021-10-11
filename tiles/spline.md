# Spline

## Data Bindings

The `Spline` chart expects **Narrow **([Wide vs. Narrow data](../query-functions/overview/wide-vs.-narrow-data.md)) data.

### Data binding fields

| Binding                  | Description                                                                                       |
| ------------------------ | ------------------------------------------------------------------------------------------------- |
| _**Serie Type Mapping**_ | \[OPTIONAL]                                                                                       |
| _**Serie Name**_         | <p>Column to use to determine series <br>(one per unique value; shown in legend and on hover)</p> |
| _**X**_                  | <p>Column to use for x-axis value</p><p>(typically use 'TimestampLocalId')</p>                    |
| **Y**                    | Column to use for y-axis value                                                                    |
| **X Type**               | <p>Format of x-axis values</p><p>(Date, Number, String)(Use dropdown list)</p>                    |
| **Y Type**               | <p>Format of y-axis values</p><p>(Date, Number, String)(Use dropdown list)</p>                    |
| **X Unit**               | <p>Column to use for Unit for x-axis</p><p>(typically leave blank for datetime)</p>               |
| **Y Unit**               | <p>Column to use for Unit for y-axis</p><p>(typically use 'UnitOfMeasureAbbrev' column)</p>       |

### Data example

![Discharge Air Temperature for a selection of VAVs](<../.gitbook/assets/image (1).png>)

![](<../.gitbook/assets/image (6).png>)

_Note that a dynamic chart is shown in the image above. A dynamic chart is functionally the same as a spline chart for basic timeseries data plotted as a line._

### Query functions

The query function: [Tag Pivot Interval](../query-functions/tag-pivot-interval.md) can be used to generate `Spline` (and `Dynamic Chart`) data.

## Display Bindings

Coming soon.
