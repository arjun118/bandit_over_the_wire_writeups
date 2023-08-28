first try connecting with netcat on port 30002

```shell
nc localhost 30002
```

The below attatched forum helped me out 

https://askubuntu.com/questions/1004901/connect-via-netcat-and-send-messages-in-bash-script

so , first lets generate the seed

```shell
#! /bin/bash

for i in {1000..9999}; do
        echo "$pass_of_the_previous_level $i" >> seed.txt
done
```

```shell
nc localhost 30002 < seed.txt
```

you will get the pass