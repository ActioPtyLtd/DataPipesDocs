# Higher Order Functions

We will be using the following DataSet to illustrate the selection capabilities:

```Scala
(
    "schoolName": "Knox",
    ["parents",
        "firstName" -> "John",
        "lastName" -> "Smith",
        ["children",
            "firstName" -> "Max",
            "lastName" -> "Smith"
        ]
    ]
)
```

## Map
To get the full name of all parents:

```Scala
parents.map(p => "fullName" -> p.firstName + " " + p.lastName)
```

## Flat Map
To get the first name of all children:

```Scala
parents.flatMap(p => p.firstName)
```

## Find
To find a parent with the last name of Smith and get the first name:

```Scala
parents.find(p => p.lastName == "Smith").firstName
```

## Group By

## Reduce Left

