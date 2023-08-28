    A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

    NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

>  do what you did in the last challenge

> checking the ownership of the running scripts would give an insight into what can be possible file we are targeting

```shell
echo I am user bandit23 | md5sum | cut -d ' ' -f 1
``` 
> you will get a hash

```shell
cat /tmp/{hash}
```

