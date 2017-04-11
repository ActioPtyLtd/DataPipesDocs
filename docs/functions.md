# Functions

## String Functions

The following functions can be used:

``` Scala
def strContains(source: String, target: String): Bool
```
Returns true if the target string can be found in the source string.

``` Scala
def substring(source: String, start: Int): String
```
Returns the remainder string beginning at index start.

## Generic Functions

``` Scala
def coalesce(xs: DataSet*): DataSet
```
Returns the first DataSet that is not empty.
