# Data lifecycle

All data manipulation in the Workspace builder is done using **`Javascript`**.

Data from datasets is provided to the workspace via ADX using **`Kusto`**.  

Parameters exposed to the workspace are parts of the dataset, and as such need to be written using the dataset language: **`Kusto`**. This is the only place Kusto is used in the workspace builder.

![Data lifecycle](<../.gitbook/assets/image (8).png>)
