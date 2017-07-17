# Utility Functions

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

``` Scala
def trim(str: String): String
```
The trim function eliminates leading and trailing spaces.


``` Scala
def split(str: String, regex: String): List[String]
```
Splits this string around matches of the given regular expression

## Generic Functions

``` Scala
def coalesce(xs: DataSet*): DataSet
```
Returns the first DataSet that is not empty.
