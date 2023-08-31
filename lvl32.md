clone the repo..

do what the readme file says..that is create the key.txt file and put the required 

now if you check the status using 

> git status

you will get to know that the changes made are not being tracked.

why is that?

we do this with those files which we don't want to be tracked and ofcourse don't want to be pushed into the remote repo.

we do this by addding them to .gitignore file

check the contents of gitignore

```shell
cat .gitignore
```

you can still track the file using 

```shell
git add key.txt -f
```

```shell
git commit -m "sth"
```

```shell
git push -u origin master
```

you will get the pass to next level