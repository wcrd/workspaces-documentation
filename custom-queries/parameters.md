# Basic Query

## Basic Query \(from Workspace 101 training\)

Recall our typical 'live data' timeseries retrieval query from Workspaces Training 101:

```javascript
// Typical Query
ObjectProperties
| where InstallationID == "745a7ddf-d3b0-4a3d-8400-39724f15d0ad"
| where EquipmentType == "VAV" and Floor=="07" and PointName == "Zone Air Temperature"
| join kind=inner
    (
    Timeseries
    | where InstallationId == "745a7ddf-d3b0-4a3d-8400-39724f15d0ad" and Timestamp >= ago(1d)
    )
    on $left.ObjectPropertyID == $right.ObjectPropertyId
| project EquipmentLabel, EquipmentType, PointName, Value, TimestampLocalId
| summarize arg_max(TimestampLocalId, Value) by EquipmentLabel, EquipmentType, PointName
```

This query looks for sensors for the given

* Site \(InstallationID\) = 745a7ddf-d3b0-4a3d-8400-39724f15d0ad
* Equipment Type = VAV
* Floor = 07
* Point Name = Zone Air Temperature

and returns the most recent value for each sensor recorded in the last: 1 day \(1d\).

![](../.gitbook/assets/image%20%2813%29.png)

This query will always return the most recent readings for given site, sensors, equipment, and floor. This is quite a useful query, and one that we could use for other sites, sensors, equipment, or floors  ---  however writing a new dataset for each slight query variation would be a tedious and unwieldy strategy. Instead, we can use _**parameters**_ to make our queries more flexible.

