# Editor layout

## Data Source section

Here the data source and any data source parameters are selected. Parameters are filled using **`Kusto`**.

![](<../.gitbook/assets/image (12).png>)

## Filter section

Here the data returned from the data source can be filtered before being made available to the tile bindings. Since the data is now in possession of the workspace builder the filtering expression is written in **`Javascript`**.

The filter expression needs to return a `true` or `false` value per row, with `false` rows being filtered out.

![](<../.gitbook/assets/image (13).png>)

## Tile Setup section

Here the filtered data can be used by the tile. All reference or custom formulas need to be written in **`JavaScript`**.

![](<../.gitbook/assets/image (14).png>)
