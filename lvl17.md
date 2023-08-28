    The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

first we need find the open ports on the remote server and the corresponding services they are running

this can be done with nmap

```shell
nmap -sV localhost  -p 31000-32000 
```
> ### output
>  ```shell
>   PORT      STATE SERVICE     VERSION
>    31046/tcp open  echo
>   31518/tcp open  ssl/echo
>    31691/tcp open  echo
>    31790/tcp open  ssl/unknown
>   31960/tcp open  echo 

now we can test the ssl connection using the port 31790...

```shell
openssl s_client -connect localhost:31790 
```

after submitting the pass for this level, you will get the ssh private key for the next level