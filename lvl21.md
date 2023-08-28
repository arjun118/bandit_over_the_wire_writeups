    There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).


> keep a netcat listerner running as  a background process 

```shell
echo "password_for_this_level" | nc -lp 2222
```

now connect to this listener using the given setuid binary

```shell
./suconnect 2222
```

