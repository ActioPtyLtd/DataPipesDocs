# Templates

Templates perform string interpolation and follow the Scala syntax using the dollar operator with brackets required with more complex expressions:

```Scala
"$firstName $lastName lives in a suburb with postcode ${address.postcode}."
```

!!! warning
    The top level expressions used within a template will always be evaluated to a string. The empty string will be used if the expression cannot be evaluated to a string.

Templates can be used to generate XML, JSON, SQL, CSV and in general any structure that can be thought of as a string.

## XML

```xml
<root>
  <firstName>$firstName</firstName>
  <lastName>$lastName</lastName>
</root>
```

## JSON
```json
{
  "firstName": "$firstName",
  "lastName": "$lastName",
}
```
## SQL
```SQL
select * from person where firstName = '$firstName' AND lastName = '$lastName'
```

## CSV
```text
$firstName,$lastName
```
