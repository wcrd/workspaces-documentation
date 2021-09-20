# \[Depreciated\] Tag Pivot

{% hint style="danger" %}
Tag Pivot is depreciated. Please use Tag Pivot \[v2\] and it's derivatives.
{% endhint %}

## Overview

`Tag Pivot` returns sensor data in a 2D **wide** array, with a field for the row labels and a field for the column headings.

The `Tag Pivot` source returns the most recent reading for each sensor it finds; i.e. it returns the 'live' data for each point. If multiple sensors are returned for the row & column combination, then the average value is returned. \(If another aggregation method is desired see: [ADX Tag Pivot \(Endpoint\)](adx-tag-pivot-endpoint.md)\)

This data source is useful for:

* Grids \(Grid v1 only\)
* Sensor Tiles
* Status Tiles

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
      <td style="text-align:left">site id guid</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>searchParams</b></em>
      </td>
      <td style="text-align:left">
        <p>ADX &apos;where&apos; query</p>
        <p>Filter ObjectProperties before fetching timeseries data</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>columnField</b></em>
      </td>
      <td style="text-align:left">Tag Group to pivot on (column headers)</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>rowField</b></em>
      </td>
      <td style="text-align:left">Tag Group to use for row labels</td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>maxLookbackPeriod</b></em>
      </td>
      <td style="text-align:left">
        <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p>
        <p>This is how far back in time the query should look to find a &apos;live&apos;
          value for a sensor</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><em><b>formatModes</b></em>
      </td>
      <td style="text-align:left">
        <p>Convert Mode and Status points into Pill representation</p>
        <p>(options: True, False)</p>
      </td>
    </tr>
  </tbody>
</table>

## Return Format

2D array with column headers = column field \(tag group\) tags and row labels = row field \(tag group\) tags

| rowField | columnFieldValue1 | ... | columnFieldValueN |
| :--- | :--- | :--- | :--- |
| rowFieldValue1 |  |  |  |
| ... |  |  |  |
| rowFieldValue2 |  |  |  |

#### e.g.:

![rowField=EquipmentLabel; columnField=PointName](../.gitbook/assets/image%20%287%29.png)

