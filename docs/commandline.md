# Command Line

Data pipes runs on the JVM and can be executed as follows:

```bash
java -cp ./config:./dpipes-assembly.jar com.actio.Main
    [-c <configName.conf>]
    [-p <pipeName>]
    [-s]
```

*   -c This is used to specify the configuration file to execute. The default is application.conf.
*   -p This is used to specify which pipe to execute in the configuration file. The default pipe in the configuration is used.
*   -s The parameter will run Data pipes as a long running service, listening on a predefined port.