# Cell Renderers

## Text Box

The text box is the default cell renderer. It simply displays the provided value in the cell. Available bindings:

| Binding | Description |
| :--- | :--- |
| **Column Type** | Data type of column |
| **Cell Color** | Background color of the cell |
| **Date Time Format** | \(Conditional Field\) If datatype is datetime, this binding controls how the date is rendered in the grid.  |

## Pills

Coming soon.

## Progress Bar

Coming soon.

## Range Bar

Coming soon.

## Dynamic Text

The dynamic text renderer is similar to the standard 'Text Box' renderer, with some added design functionality. 

### Overview

The Dynamic Text renderer by default displays the cell value wrapped in a 'pill'. The user is able to configure both the _**color**_ and the _**icon**_ \(optional\) that is rendered. 

![](../../.gitbook/assets/image%20%2817%29.png)

The dynamic text renderer also supports the creation of basic hyperlinks.

![](../../.gitbook/assets/image%20%2815%29.png)

### Bindings

The Dynamic Text renderer, like the Text Box renderer, does not require any special data formats to work. It simply runs off the cell value.

![](../../.gitbook/assets/image%20%2811%29.png)

| Binding | Description |
| :--- | :--- |
| **Column Type** | Data type of column |
| **Color** | Color of the pill/icon/text |
| **Icon** | \(Optional\) The Icon to render on the LHS of the pill |
| **Date Time Format** | \(Conditional Field\) If datatype is datetime, this binding controls how the date is rendered in the grid.  |
| **Label** | \(Conditional Field\) If datatype is URL, this binding control what text is shown in the Pill. This is a manually set static field and cannot be set from the data source currently. |
| **Open in new tab** | \(Conditional Field\) If datatype is URL, this toggle switch controls whether the links open in the current window or in a new tab. |

### Note on using Icons

Current icon support is still basic. We currently have access to the default set of icons from [Font Awesome](https://fontawesome.com/). To use an icon, find the icon\(s\) of interest from Font Awesome, copy the icon name, and reference in the _**icon**_ binding as `fas:icon-name`. E.g.: the icon pictured below would be referenced as `fas:address-book`.  

![Icon from font-awesome](../../.gitbook/assets/image%20%281%29.png)

### Note on URL column type

1. **Additional bindings:** The URL column type takes the cell value and converts it into a hyperlink element. This hyperlink element has additional bindings _**label**_ and _**opens in new tab**_ that control the behavior of that hyperlink element. These options apply to the entire column; it is not possible to set unique behavior per cell. If a user needs a set of links that open in the current window, and a set of links that open in a new tab, then you can either: a\) create two columns in the grid, one for each style, or b\) create two separate grids, one for each style. Convention is to use two separate grids as this is generally clearer from a UX perspective.
2. **URL value:**  
   The cell value can either be: 

   * _**an absolute link**_, i.e.: "https://www.google.com/"
   * _**a relative link to a Switch Asset**_, i.e.: "\#/workspaces/wid=876485762-24095y23489-452y343"

   Any link that is not an absolute link will be rendered as a relative link to the Switch Platform.  
   An advantage of using relative links \(for intra-Switch linkages\) is that it is subdomain independent, e.g. if you built the workspace in a subdomain but are accessing it through the 'root' platform, it will work as expected. There is no requirement to use relative links for intra-Switch linking.

