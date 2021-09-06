# Data Object

The data returned by the datasource is stored as a `JavaScript` object by the workspace. The exact details are not important, but there are three key `variables` that can be useful to reference in the bindings for more complex tiles.

### Data

The entire \(filtered\) dataset returned by the datasource: **Data.** Stored as an array of objects.

```javascript
Data = [
    {<row1_data>},
    {<...>},
    {<rowN_data>}
]
```

### Row

The current row from the **Data** object that the tile is processing. For tiles that don't loop through rows \(i.e. Sensor, Status, etc\) this will just be the first row from **Data**. Stored as a JavaScript object.

```javascript
Row = {<row1_data>}
```

### Cell

Only supported in the grid tile. The contents of the current cell. Stored depending on cell data type. We will cover this more in the [Grid \[v2\]](../tiles/grid-v2/) section.

