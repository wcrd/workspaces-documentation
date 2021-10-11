# \[Depreciated] Tag Pivot

{% hint style="danger" %}
Tag Pivot is depreciated. Please use Tag Pivot \[v2] and it's derivatives.
{% endhint %}

## Overview

`Tag Pivot` returns sensor data in a 2D **wide** array, with a field for the row labels and a field for the column headings.

The `Tag Pivot` source returns the most recent reading for each sensor it finds; i.e. it returns the 'live' data for each point. If multiple sensors are returned for the row & column combination, then the average value is returned. (If another aggregation method is desired see: [ADX Tag Pivot (Endpoint)](adx-tag-pivot-endpoint.md))

This data source is useful for:

* Grids (Grid v1 only)
* Sensor Tiles
* Status Tiles

## Parameters

| Parameter               | Description                                                                                                                               |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| _**siteId**_            | site id guid                                                                                                                              |
| _**searchParams**_      | <p>ADX 'where' query</p><p>Filter ObjectProperties before fetching timeseries data</p>                                                    |
| _**columnField**_       | Tag Group to pivot on (column headers)                                                                                                    |
| _**rowField**_          | Tag Group to use for row labels                                                                                                           |
| _**maxLookbackPeriod**_ | <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p><p>This is how far back in time the query should look to find a 'live' value for a sensor</p> |
| _**formatModes**_       | <p>Convert Mode and Status points into Pill representation</p><p>(options: True, False)</p>                                               |

## Return Format

2D array with column headers = column field (tag group) tags and row labels = row field (tag group) tags

| rowField       | columnFieldValue1 | ... | columnFieldValueN |
| -------------- | ----------------- | --- | ----------------- |
| rowFieldValue1 |                   |     |                   |
| ...            |                   |     |                   |
| rowFieldValue2 |                   |     |                   |

#### e.g.:

![rowField=EquipmentLabel; columnField=PointName](../.gitbook/assets/image.png)
