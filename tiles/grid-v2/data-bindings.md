# Data Bindings

The `Grid` (v2) tile expects **Wide **([Wide vs. Narrow data](../../query-functions/overview/wide-vs.-narrow-data.md)) data.

## Data binding fields

| Binding           | Description                                                                                          |
| ----------------- | ---------------------------------------------------------------------------------------------------- |
| **Display Name**  | Column name in grid                                                                                  |
| **Visible**       | Controls whether the column is rendered in the grid tile                                             |
| **Column Size**   | Relative size of the column compared to other columns (default=1)                                    |
| **Header Align**  | Text alignment of column header                                                                      |
| **Value Align**   | Text alignment of column cell values                                                                 |
| **Cell Renderer** | Controls how a cell is displayed. Each cell renderer has a subset of bindings that are covered below |

## Special Grid bindings

The `Grid` tile has a number of special feature compared to the other tiles: 

1. **"Cell Renderer" bindings**\
   These bindings allow a user to customize how the values (and special value objects) are displayed in the cells.
2. **"Custom Columns" bindings**\
   ****These bindings allow a user to create custom calculated columns to add to the grid. After creation these columns are treated the same as normal columns returned from the data query.
3. **"Cell Conditional Formatter" bindings**\
   ****These are technically a subset of the 'Cell Renderer' bindings; these bindings allow a user to customize the background color (read: highlighting) of each cell in the grid.

Each of these features is covered in the sections below.

## Query functions

The query function: [Tag Pivot](../../query-functions/tag-pivot.md) can be used to generate `Grid`friendly data.
