# Tools based on HP's Quartz simulator to reduce DRAM bandwidth
### More documentation will be added soon.

#### Note: Throttling using Quartz is only supported for Intel Haswell Architectures
Step 1: Run the autocompile and install script
```
 cd  memthrottle/quartz
  ./install_quartz.sh
```

Step 2: For modifying bandwidth of throttled node, open the following file

     vim nvmemul.ini

Step 3: Change the read and write to same bandwidth values

        bandwidth:
        {
            enable = true;
            model = "/tmp/bandwidth_model";
            read = 5000;
            write = 5000;
        };
Step 4: Run the throttling script again to check the value
```
  ./install_quartz.sh
```

Step 5: When successful, you will see reduced memory bandwidth for one NUMA socket.
