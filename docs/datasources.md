# DataSources

## Text File

```HOCON

dataSource {
    type = file
    behavior = raw
    directory = "/home/me"
    query {
        read {
            filenameTemplate = "fileName.txt"
        }
        create {
            filenameTemplate = "fileName.txt"
            header = "C1,C2,C3"
            line = "$c1,$c2,$c3"
        }
    }
}

```

## DBF File

```HOCON

dataSource {
    type = file
    behavior = DBF
    directory = "/home/me"
    query {
        read {
            filenameTemplate = "fileName.DBF"
            fields = ["C1", "C2", "C3"]
        }
    }
}

```

## REST Json

```HOCON

dataSource {
    type = rest
    credential {
        user = "me"
        password = "password"
    }
    headers {
        mykey1 = "myvalue1"
        mykey2 = "myvalue2"
    }
    query {
        read {
            uri = "https://mydomain.com/v1/users"
        }
        create {
            verb = put
            uri = "https://mydomain.com/v1/users"
            body = "$body"
        }
    }
}

```

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