# Spline

## Data Bindings

The `Spline` chart expects **Narrow** \([Wide vs. Narrow data](../query-functions/overview/wide-vs.-narrow-data.md)\) data.

### Data binding fields

<table>
  <thead>
    <tr>
      <th style="text-align:left">Binding</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><em><b>Serie Type Mapping</b></em>
      </td>
      <td style="text-align:left">[OPTIONAL]</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>Serie Name</b></em>
      </td>
      <td style="text-align:left">Column to use to determine series
        <br />(one per unique value; shown in legend and on hover)</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>X</b></em>
      </td>
      <td style="text-align:left">
        <p>Column to use for x-axis value</p>
        <p>(typically use &apos;TimestampLocalId&apos;)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Y</b>
      </td>
      <td style="text-align:left">Column to use for y-axis value</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>X Type</b>
      </td>
      <td style="text-align:left">
        <p>Format of x-axis values</p>
        <p>(Date, Number, String)(Use dropdown list)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Y Type</b>
      </td>
      <td style="text-align:left">
        <p>Format of y-axis values</p>
        <p>(Date, Number, String)(Use dropdown list)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>X Unit</b>
      </td>
      <td style="text-align:left">
        <p>Column to use for Unit for x-axis</p>
        <p>(typically leave blank for datetime)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Y Unit</b>
      </td>
      <td style="text-align:left">
        <p>Column to use for Unit for y-axis</p>
        <p>(typically use &apos;UnitOfMeasureAbbrev&apos; column)</p>
      </td>
    </tr>
  </tbody>
</table>

### Data example

![Discharge Air Temperature for a selection of VAVs](../.gitbook/assets/image%20%289%29.png)

![](../.gitbook/assets/image%20%282%29.png)

_Note that a dynamic chart is shown in the image above. A dynamic chart is functionally the same as a spline chart for basic timeseries data plotted as a line._

### Query functions

The query function: [Tag Pivot Interval](../query-functions/tag-pivot-interval.md) can be used to generate `Spline` \(and `Dynamic Chart`\) data.

## Display Bindings

Coming soon.

