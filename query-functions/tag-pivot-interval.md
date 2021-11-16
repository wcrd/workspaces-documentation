# Tag Pivot Interval

## Overview

`Tag Pivot Interval` returns a multi-series **narrow** table with trend data for selected sensors. It is similar to [Tag Pivot](tag-pivot.md) in set-up, with two additional fields.

This source also processes 'Status' and 'Command' points to show as formatted bars in the Dynamic Chart.

This data source is useful for:

* Timeseries charts

## Parameters

| Parameter          | Description                                                                                                                                                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| _**siteId**_       | Site id guid                                                                                                                                                                                                                               |
| _**rowField**_     | Tag Group to pick series from (i.e. Equipment Label)                                                                                                                                                                                       |
| _**rowValue**_     | Tag (from Tag Group) to fetch data for                                                                                                                                                                                                     |
| _**columnField**_  | Tag Group to pick sensor values from (i.e. Point Name)                                                                                                                                                                                     |
| _**columnValue**_  | Tag (from Tag Group) to fetch data for                                                                                                                                                                                                     |
| _**periodKey**_    | <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p><p>This is how much history the query should return for each sensor</p>                                                                                                                        |
| _**searchEnable**_ | <p>Enables additional filtering on the data using the <em><strong>searchParams</strong></em> field</p><p>(options: True, False)</p>                                                                                                        |
| _**searchParams**_ | <p>[OPTIONAL]</p><p>ADX 'where' query</p><p>Filter ObjectProperties before fetching timeseries data</p><p><strong>NOTE: </strong>This field, while optional, requires that  a valid KQL statement is provided, even if it is not used.</p> |

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

#### e.g.:

![rowField=EquipmentType;rowValue=VAV;columnField=PointName;columnValue=Discharge Air Temperature;searchParams="Floor=='07'"](<../.gitbook/assets/image (9).png>)

