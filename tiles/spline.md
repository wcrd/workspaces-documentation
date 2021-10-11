# Spline

![](<../.gitbook/assets/image (35).png>)

## Data Bindings

### Data Source

The `Spline` chart expects **Narrow **([wide-vs.-narrow-data.md](../query-functions/overview/wide-vs.-narrow-data.md "mention")) data.

#### Useful query functions

The following query functions can be used to generate `Spline` chart data.

* [tag-pivot-interval.md](../query-functions/tag-pivot-interval.md "mention") 

### Tile Setup

Core tile setup parameters:

| **Binding**              | **Description**                                                                                   |
| ------------------------ | ------------------------------------------------------------------------------------------------- |
| _**Serie Type Mapping**_ | \[OPTIONAL]                                                                                       |
| _**Serie Name**_         | <p>Column to use to determine series <br>(one per unique value; shown in legend and on hover)</p> |
| _**X**_                  | <p>Column to use for x-axis value</p><p>(typically use 'TimestampLocalId')</p>                    |
| **Y**                    | Column to use for y-axis value                                                                    |
| **X Type**               | <p>Format of x-axis values</p><p>(Date, Number, String)(Use dropdown list)</p>                    |
| **Y Type**               | <p>Format of y-axis values</p><p>(Date, Number, String)(Use dropdown list)</p>                    |
| **X Unit**               | <p>Column to use for Unit for x-axis</p><p>(typically leave blank for datetime)</p>               |
| **Y Unit**               | <p>Column to use for Unit for y-axis</p><p>(typically use 'UnitOfMeasureAbbrev' column)</p>       |



Additional tile setup parameters:



## Data example

![Discharge Air Temperature for a selection of VAVs](<../.gitbook/assets/image (9).png>)

![](<../.gitbook/assets/image (2).png>)

_\*\* Note that a dynamic chart is shown in the image above. A dynamic chart is functionally the same as a spline chart for basic timeseries data plotted as a line._

