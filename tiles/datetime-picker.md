# Datetime Picker

![](<../.gitbook/assets/image (44).png>)

## Data Bindings

This tile does not currently have data bindings.

{% hint style="info" %}
This tile will be getting new bindings that support:

* Custom Prefill options
* Initial values
* Selection resolutions: Datetime, Date, Week, Month, Year only.
* Point in time mode
* No prefill combo toggle
{% endhint %}



## Data Object

### Object Format

The data object for the datetime tile is as follows:

```javascript
{ 
    "DateTimeRange": { 
        "selectedRange": { 
            "start": <datetime_string>,     // e.g. 2022-07-10T21:59:00.000Z
            "end": <datetime_string>        // e.g. 2022-07-15T21:59:00.000Z
        }, 
        "selectedMode": <quickselect_enum>  // e.g. "Trailing 7 days"
    } 
}
```

### Object Methods

The Datetime picker has special methods available on its data object.

#### DateTime formatting

The `DateTimeRange.selectedRange` elements have a special method that return formatted versions of the `start` and `end` fields.

The function accepts a datetime formatter string as input. See [here ](datetime-picker.md#undefined)for datetime formatting guidance.

```javascript
// formatted start date
DateTimeRange.selectedRange.startFormat("dd.MM.yyyy")

// formatted end date
DateTimeRange.selectedRange.endFormat("yyyy/dd/MM HH:mm:ssZ")
```

