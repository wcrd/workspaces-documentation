# Tag Pivot Interval

## Overview

`Tag Pivot Interval` returns a multi-series **narrow** table with trend data for selected sensors. It is similar to [Tag Pivot](tag-pivot.md) in set-up, with two additional fields.

This source also processes 'Status' and 'Command' points to show as formatted bars in the Dynamic Chart.

This data source is useful for:

* Timeseries charts

## Parameters

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parameter</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><em><b>siteId</b></em>
      </td>
      <td style="text-align:left">Site id guid</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>rowField</b></em>
      </td>
      <td style="text-align:left">Tag Group to pick series from (i.e. Equipment Label)</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>rowValue</b></em>
      </td>
      <td style="text-align:left">Tag (from Tag Group) to fetch data for</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>columnField</b></em>
      </td>
      <td style="text-align:left">Tag Group to pick sensor values from (i.e. Point Name)</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>columnValue</b></em>
      </td>
      <td style="text-align:left">Tag (from Tag Group) to fetch data for</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>periodKey</b></em>
      </td>
      <td style="text-align:left">
        <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p>
        <p>This is how much history the query should return for each sensor</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>searchEnable</b></em>
      </td>
      <td style="text-align:left">
        <p>Enables additional filtering on the data using the <em><b>searchParams</b></em> field</p>
        <p>(options: True, False)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>searchParams</b></em>
      </td>
      <td style="text-align:left">
        <p>[OPTIONAL]</p>
        <p>ADX &apos;where&apos; query</p>
        <p>Filter ObjectProperties before fetching timeseries data</p>
      </td>
    </tr>
  </tbody>
</table>

## Return Format

`Tag Pivot Interval` always returns the following columns:

* PropertyName
* DisplayName
* Value
* TimestampLocalId
* UnitOfMeasureAbbrev
* {rowField}
* {columnField}
* rValue

### e.g.:

![rowField=EquipmentType;rowValue=VAV;columnField=PointName;columnValue=Discharge Air Temperature;searchParams=&quot;Floor==&apos;07&apos;&quot;](../.gitbook/assets/image%20%289%29.png)

