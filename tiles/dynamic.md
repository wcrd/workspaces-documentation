# Dynamic

The `Dynamic Chart` is identical to the `Spline` chart except for the way it renders Mode & Status values.

## Data Bindings

See [Spline](spline.md) section for data binding details.

#### Serie Type Mapping

The dynamic chart has an additional binding field called 'Serie Type Mapping' which allows this chart to render different chart styles per series.

![](<../.gitbook/assets/image (39).png>)

**Options:**

| keyword   | chart type    |
| --------- | ------------- |
| **line**  | line chart    |
| **bar**   | column chart  |
| **point** | scatter chart |

By default, the chart style for every series is 'line'.

To force a series to render as a different chart type utilise this Serie Type Mapping field as follows:

```
<serie_name>=<chart_type_keyword>;
```

Multiple series can be separated by a ";".

![Dynamic Chart with 'bar' and 'line' serie mappings](<../.gitbook/assets/image (50).png>)
