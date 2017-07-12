
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