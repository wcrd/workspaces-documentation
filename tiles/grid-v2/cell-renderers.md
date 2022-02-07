# Cell Renderers

## Text Box

![](<../../.gitbook/assets/image (19).png>)

The text box is the default cell renderer. It simply displays the provided value in the cell. The Text Box provides options to set the data type, cell color, and value units.

### Bindings

![](<../../.gitbook/assets/image (39).png>)

| Binding              | Description                                                                                                                                                                                                      |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Column Type**      | Data type of column                                                                                                                                                                                              |
| **Cell Color**       | Background color of the cell                                                                                                                                                                                     |
| **Date Time Format** | <p>(Conditional Field) If datatype is datetime, this binding controls how the date is rendered in the grid. <br><br>There is an additional binding that will convert given datetime into browser local time.</p> |
| **Number Format**    | (Conditional Field) If datatype is number, this binding controls how the number is displayed (leading zeros, decimal places, etc)                                                                                |
| **Units**            | Units to display for the values in the column. The unit does not affect sorting or filtering.                                                                                                                    |

### Note on Data Types

Column data types control how the filtering and sorting works for that column in the grid.

![](<../../.gitbook/assets/image (45).png>)

There are three supported datatypes:

1. **String** - provides basic text filtering and alphabetical sorting
2.  **Number** - provides numeric filtering and sorting

    The number datatype provides an additional formatting binding:\
    ![](<../../.gitbook/assets/image (51).png>)
3.  **Datetime** - provides date range filtering and chronological sorting\
    The datetime datatype provides two additional formatting bindings:\
    ![](<../../.gitbook/assets/image (34).png>)

    The first binding controls the datetime string format.\
    The second binding will convert the given datetime into the users local browser time.  This option is useful for representing data in local time vs. local site time.

### Note on Units

Units can be added to any Text Box column. Units are not considered when filtering and sorting, allowing standard column sorting behavior.

![](<../../.gitbook/assets/image (43).png>)

In the example above the column type is set to Number. This allows the column to sort in ascending order even in the presence of a unit string as shown below.

![](<../../.gitbook/assets/image (44).png>)

If the datatype was instead set to string the column would sort alphabetically.

![](<../../.gitbook/assets/image (40).png>)

## Pills

![](<../../.gitbook/assets/image (21).png>)

Coming soon.

## Progress Bar

![](<../../.gitbook/assets/image (18).png>)

Coming soon.

## Range Bar

![](<../../.gitbook/assets/image (23).png>)

Coming soon.

## Dynamic Text

![](<../../.gitbook/assets/image (22).png>)

The dynamic text renderer is similar to the standard 'Text Box' renderer, with some added design functionality.&#x20;

### Overview

The Dynamic Text renderer by default displays the cell value wrapped in a 'pill'. The user is able to configure both the _**color**_ and the _**icon**_ (optional) that is rendered.&#x20;

![](<../../.gitbook/assets/image (17).png>)

The dynamic text renderer also supports the creation of basic hyperlinks.

![](<../../.gitbook/assets/image (15).png>)

### Bindings

The Dynamic Text renderer, like the Text Box renderer, does not require any special data formats to work. It simply runs off the cell value. The Dynamic Text has the same bindings as the Text Box, with some additional settings described below:

![](<../../.gitbook/assets/image (11).png>)

| **Column Type**      | Data type of column                                                                                                                                                                                             |
| -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Color**            | Color of the pill/icon/text                                                                                                                                                                                     |
| **Icon**             | (Optional) The Icon to render on the LHS of the pill                                                                                                                                                            |
| **Date Time Format** | <p>(Conditional Field) If datatype is datetime, this binding controls how the date is rendered in the grid.<br><br>There is an additional binding that will convert given datetime into browser local time.</p> |
| **Number Format**    | (Conditional Field) If datatype is number, this binding controls how the number is displayed (leading zeros, decimal places, etc)                                                                               |
| **Units**            | Units to display for the values in the column. The unit does not affect sorting or filtering.                                                                                                                   |
| **Label**            | (Conditional Field) If datatype is URL, this binding control what text is shown in the Pill. This is a manually set static field and cannot be set from the data source currently.                              |
| **Open in new tab**  | (Conditional Field) If datatype is URL, this toggle switch controls whether the links open in the current window or in a new tab.                                                                               |

### Note on using Icons

Current icon support is still basic. We currently have access to the default set of icons from [Font Awesome](https://fontawesome.com). To use an icon, find the icon(s) of interest from Font Awesome, copy the icon name, and reference in the _**icon**_ binding as `fas:icon-name`. E.g.: the icon pictured below would be referenced as `fas:address-book`. &#x20;

![Icon from font-awesome](<../../.gitbook/assets/image (1).png>)

### Note on URL column type

1. **Additional bindings:**\
   ****The URL column type takes the cell value and converts it into a hyperlink element. This hyperlink element has additional bindings _**label**_ and _**opens in new tab**_ that control the behavior of that hyperlink element. These options apply to the entire column; it is not possible to set unique behavior per cell. If a user needs a set of links that open in the current window, and a set of links that open in a new tab, then you can either: a) create two columns in the grid, one for each style, or b) create two separate grids, one for each style. Convention is to use two separate grids as this is generally clearer from a UX perspective.\

2.  **URL value:**\
    ****The cell value can either be:&#x20;

    * _**an absolute link**_, i.e.: "https://www.google.com/"
    * _**a relative link to a Switch Asset**_, i.e.: "#/workspaces/wid=876485762-24095y23489-452y343"

    \
    Any link that is not an absolute link will be rendered as a relative link to the Switch Platform.\
    An advantage of using relative links (for intra-Switch linkages) is that it is subdomain independent, e.g. if you built the workspace in a subdomain but are accessing it through the 'root' platform, it will work as expected. There is no requirement to use relative links for intra-Switch linking.
