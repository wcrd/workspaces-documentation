# Tag Pivot \[v2]

{% hint style="info" %}
Tag Pivot \[v2] returns the same data as Tag Pivot, but has special formatting to support Grid v2 rendering features.
{% endhint %}

## Overview

`Tag Pivot` returns sensor data in a 2D **wide** array, with a field for the row labels and a field for the column headings.

The `Tag Pivot` source returns the most recent reading for each sensor it finds; i.e. it returns the 'live' data for each point. If multiple sensors are returned for the row & column combination, then the average value is returned. (If another aggregation method is desired see: [ADX Tag Pivot (Endpoint)](adx-tag-pivot-endpoint.md))

This data source is useful for:

* Grids
* Sensor Tiles
* Status Tiles

## Parameters

| Parameter                                | Description                                                                                                                                                                                                                                                                                                                              |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _**siteId**_                             | site id guid                                                                                                                                                                                                                                                                                                                             |
| _**searchParams**_                       | <p>ADX 'where' query</p><p>Filter ObjectProperties before fetching timeseries data</p>                                                                                                                                                                                                                                                   |
| _**columnField**_                        | Tag Group to pivot on (column headers)                                                                                                                                                                                                                                                                                                   |
| _**rowField**_                           | Tag Group to use for row labels                                                                                                                                                                                                                                                                                                          |
| _**maxLookbackPeriod**_                  | <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p><p>This is how far back in time the query should look to find a 'live' value for a sensor</p>                                                                                                                                                                                                |
| _**formatStatusCommandsAsProgressBars**_ | <p>Boolean: True, False</p><p>For aggregations where multiple points exist per cell, format Status and Command points into a 'Progress Bar' data format. If only one point exists per cell then 'Pill' formatted data is returned.</p><p></p><p>See <a href="../tiles/grid-v2/">Grid [v2]</a> for renderer methods and data formats.</p> |

## Return Format

2D array with column headers = column field (tag group) tags and row labels = row field (tag group) tags

| rowField       | columnFieldValue1 | ... | columnFieldValueN |
| -------------- | ----------------- | --- | ----------------- |
| rowFieldValue1 |                   |     |                   |
| ...            |                   |     |                   |
| rowFieldValue2 |                   |     |                   |

#### e.g.:

![](https://gblobscdn.gitbook.com/assets%2F-Mc36HsWK3tOtEtvSWaE%2F-McCtC4M6NdwzevtovK8%2F-McCuoJcm8ZW-QXcS86x%2Fimage.png?alt=media\&token=2e7faaa9-bf8d-4946-9002-1116fcccd25c)
