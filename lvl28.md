    There is a git repository at ssh://bandit27-git@localhost/home/bandit27-git/repo via the port 2220. The password for the user bandit27-git is the same as for the user bandit27.

    Clone the repository and find the password for the next level.

let's create a temporary directory for us to work

```shell
mkdir /tmp/lvl27
```

now lets clone the repo

> keep in mind the port number that was given, we need to specify the port in the url (you can find more about thhis in the man pages) if it is not the standard port

```shell
git clone --help
```

```shell
git clone ssh://bandit27-git@localhost:2000/home/bandit27-git/repo 
```
navigate to the repo directory and you will get the pass to next level
