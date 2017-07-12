
## SQL Jdbc

```HOCON

dataSource {
        type = sql
        connect = "jdbc:postgresql://localhost/my_db?user=me&password=password"
        query {
            read = "select c1,c2 from T1"
            create = "insert into T1 values ($v1,$v2)"
        }
}

```