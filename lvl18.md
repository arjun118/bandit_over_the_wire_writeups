we use the diff command to compare the files line by line

you can get away with

```shell
diff passwords.old passwords.new
```

and your answer will be the second string (because passwords.new is the second command)

```shell
diff passwords.old passwords.new -y -suppress-common-lines
```

