# Wide vs. Narrow data

## Wide

Wide, or unstacked data is presented with each different data variable in a separate column.

| Person | Age | Weight | Height |
| :--- | :--- | :--- | :--- |
| Bob | 32 | 168 | 180 |
| Alice | 24 | 150 | 175 |
| Steve | 64 | 144 | 165 |

## Narrow

Narrow, stacked, or long data is presented with one column containing all the values and another column listing the context of the value

| Person | Variable | Value |
| :--- | :--- | :--- |
| Bob | Age | 32 |
| Bob | Weight | 168 |
| Bob | Height | 180 |
| Alice | Age | 24 |
| Alice | Weight | 150 |
| Alice | Height | 175 |
| Steve | Age | 64 |
| Steve | Weight | 144 |
| Steve | Height | 165 |

This is often easier to implement; addition of a new field does not require any changes to the structure of the table, however it can be harder for people to understand.

{% hint style="info" %}
[https://en.wikipedia.org/wiki/Wide\_and\_narrow\_data](https://en.wikipedia.org/wiki/Wide_and_narrow_data)
{% endhint %}

