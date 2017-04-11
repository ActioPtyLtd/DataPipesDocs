# Tasks

Tasks perform some operation, usually with a side-effect, on an incoming dataset to produce an outgoing dataset. Tasks at a high level can be of either extract, transform or load type.
More specifically the following tasks are supported:

* **Extract** - Extracts data from a data source
* **Transform Term** - Transforms the data source using expressions
* **Data Source Find** - Finds data in the data source matching a criteria
* **Data Source Join** - Joins the incoming data to data from the data source using matching compound keys
* **Data Source Update** - Executes either create or update commands to the datasource depending on matching compound keys
* **Load** - Executes commands to the datasource
* **Dump** - Displays the incoming dataset on the console
* **File Dump** - Persists the incoming dataset to disk

A typical extraction task is defined as follows:

```HOCON
read_my_api {
  type = "extract"
  dataSource = ${my_datasource}
  dataSource {
    query {
      read {
        uri = ${my_datasource.base_uri}"/v1/users"
      }
    }
  }
}
```

!!! note
    The type field within the task matches one of the predefined task types.
    Also notice the data source details can be specified outside of the task so that it can be reused.
