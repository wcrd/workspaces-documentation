# Pie Chart

{% hint style="warning" %}
This Query Function is still under development
{% endhint %}

## Overview

`Pie Chart` returns sensor data in a 2D **narrow **array, with a field for the labels and values. This data source does not yet generate color mappings.

The `Pie Chart` source returns the most recent reading for each sensor it finds; i.e. it returns the 'live' data for each point. If multiple sensors are returned for the 'group by' combination, then the average value is returned.

This data source is useful for:

* Pie Charts
* Donut Charts
* Area Charts

## Parameters

| Parameter               | Description                                                                                                                                                                                                                                                                                     |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _**siteId**_            | site id guid                                                                                                                                                                                                                                                                                    |
| _**searchParams**_      | <p>ADX 'where' query</p><p>Filter ObjectProperties before fetching timeseries data.</p><p>Use this field to filter down the data to <strong>just</strong> the sensors of interest.</p>                                                                                                          |
| _**maxLookbackPeriod**_ | <p>ADX timeperiod key (i.e. 30m, 1h, 1d)</p><p>This is how far back in time the query should look to find a 'live' value for a sensor</p>                                                                                                                                                       |
| _**groupSensorsBy**_    | <p>Tag group to group sensor timeseries data by. This is effectively the dataset that the aggregation function will run over.</p><p>e.g. if I group by 'EquipmentLabel' the dataset will return the most recent sensor reading (from the set returned by searchParams) per Equipment Label.</p> |
| _**labelField**_        | Tag Group to generate labels from (all tags in tag group in current data set)                                                                                                                                                                                                                   |
| _**aggMethod**_         | <p>ADX aggregation function to process data per label by.</p><p>i.e. count(), sum(), etc.</p>                                                                                                                                                                                                   |

## Return Format

`Pie Chart` always returns the following columns:

* label
* value

#### e.g.:

![count() of ZAT SP by EquipmentLabel](<../.gitbook/assets/image (4).png>)
