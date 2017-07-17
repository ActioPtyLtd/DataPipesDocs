# Data Set Functions

``` Scala
def isEmpty(): Bool
```

Returns whether the data set is empty.

!!! note
    For strings, this function returns true if the string is blank or null

``` Scala
def isDefined(): Bool
```

Returns whether the data set is defined, or in other words if it is not null.


``` Scala
def toJson(): String
```
Returns the data set formatted to Json.


``` Scala
def toXml(): String
```
Returns the data set formatted to Xml.