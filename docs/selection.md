# Selection

We will be using the following DataSet to illustrate the selection capabilities:

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


## By Name

To access the persons postcode one can use the following familiar syntax:

```Scala
address.postcode
```

This returns the following DataSet:

```Scala
"postcode" -> 2000
```

!!! warning
    Accessing an element that does not exist will simply return an empty DataSet:

    address.suburb

    will return an empty DataSet:

    ( )

## By Index
To access the first phone number:

```Scala
phoneNumbers(0)
```

This returns the following DataSet:

```Scala
"item" -> "98765432"
```

!!! warning
    Accessing an element that does not exist will simply return an empty DataSet:

    address.suburb

    will return an empty DataSet:

    ( )
