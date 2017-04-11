# Configuration

All datapipe scripts are persisted in the [HOCON](https://github.com/typesafehub/config/blob/master/HOCON.md) format.

## Overview
The scripts are structured into multiple blocks, namely schema, tasks, pipelines, services and startup.
```HOCON
script {
  schema { ... }
  tasks { ... }
  pipelines { ... }
  services { ... }
  startup { ... }
}
```


## Pipelines

## Pipes
