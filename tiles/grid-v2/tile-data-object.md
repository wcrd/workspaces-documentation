# Tile Data Object

```javascript
[TileName]: {
    Grid: {
        selectedItem: {
            id: <id>,                 //selection Key from Bindings
            value: {<row_data>},      //all key:value column pairs for row
        },
        selectedColumn: <column_name>,//field name from column binding
        selectedCell: <cell_value>,   //value from cell in grid
        selectedRow: {<row_data>}     //all key:value column pairs for row
    }
}
```
