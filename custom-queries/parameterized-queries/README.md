# Parameterized Queries

### Overview

Queries in datasets support _**parameters. **_

**Parameters **are simply variables that are substituted out with the provided value on query execution. They are denoted by the **@** symbol in your query; e.g. @parameter1.

To parameterize a query we simply need to:

1. Replace sections of our query with @parameters          (parameterize)
2. Configure the parameters in the query settings              (configuration)

#### Example:

`@parameter1` = "enjoyable"                                                       (configuration)

**Raw:               **"Reading this document is `@parameter1`!"     (parameterize)\
**Processed:    **"Reading this document is enjoyable!"

### Setting parameter values

Parameter values can be set from the Workspace builder, meaning that our dataset queries can be controlled directly from the workspaces!

Default values for each parameter can be set in the dataset query builder. We will cover this in the next section.
