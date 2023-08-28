text from website:

    The password for the next level is stored somewhere on the server and has all of the following properties:

    owned by user bandit7
    owned by group bandit6
    33 bytes in size

you can scour the man page of find and can write the command, i did it that way.

we got something related to user, 

```bash
man find | grep user
```

and about group

```bash
man find | grep group
```

and we solved how to search by size in the previous level

```bash
find / -user bandit7 -group bandit6 -size 33c 2> /dev/null
```

> 2> /dev/null is used for the error redirection so that our output don't get clumsy with false positives