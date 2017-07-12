

```HOCON

dataSource {
    type = ftp_client
    connect = "localhost"
    port = 1632
    credential {
        user = "username"
        password = "password"
    }
    query {
        read {
            remotepath = "/home/me"
            remote_file = "myfile.dat"
        }
    }
}

```