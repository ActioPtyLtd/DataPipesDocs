# DataSets
DataSets are hierarchical data structures.
The following is an example of a DataSet representing a person object:

```Scala
("person",
  "firstName" -> "John",
  "lastName" -> "Smith",
  ("address",
    "addr1" -> "George St.",
    "addr2" -> "Sydney",
    "postcode" -> 2000),
  ["phoneNumbers",
    "item" -> "98765432",
    "item" -> "87654321",
    "item" -> "76543212"])
```

The following JSON is an identical representation of the previous DataSet.

```json
{
  "person": {
    "firstName": "John",
    "lastName": "Smith",
    "address": {
      "addr1": "George St.",
      "addr2": "Sydney",
      "postcode": 2000
    },
    "phoneNumbers": [
      "98765432",
      "87654321",
      "76543212"
    ]
  }
}
```



## Primitive DataSet Types
The following

String:

```Scala
"firstName" -> "John"
```

Numeric:
```Scala
"postcode" -> 2000
```

Date:
```Scala
"dob" -> "2000-01-01 00:00:00"
```

Boolean:
```Scala
"citizen" -> true
```

Record:
```Scala
("address",
  "addr1" -> "George St.",
  "addr2" -> "Sydney",
  "postcode" -> 2000)
```

Array:
```Scala
["phoneNumbers",
  "item" -> "98765432",
  "item" -> "87654321",
  "item" -> "76543212"]
```

Empty:
```Scala
()
```
