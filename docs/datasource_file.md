File data sources allows one to extract the contents of files that match a regular expression. The following template is the minimum required for the use of different file types.

```HOCON

dataSource {
    type = file
    behavior = ?
    query {
        read {
            directory = "/home/me"
            filenameTemplate = "myfile.dat"
        }
    }
}

```

!!! note
    The property behavior can be set to any of the following: {csv, raw, dbf}


## Text File

```HOCON

dataSource {
    type = file
    behavior = raw
    
    query {
        read {
            directory = "/home/me"
            filenameTemplate = "fileName.txt"
        }
        create {
            directory = "/home/me"
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
    query {
        read {
            directory = "/home/me"
            filenameTemplate = "fileName.DBF"
            fields = ["C1", "C2", "C3"]
        }
    }
}

```