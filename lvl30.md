    There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo via the port 2220. The password for the user bandit29-git is the same as for the user bandit29.

    Clone the repository and find the password for the next level.


I needed a hint for that. The hint is to checkout if there are any other branches

clone thr repo

lets checkout the remote branches

```shell
git branch -r
```

lets check the dev branch (may the development kinda branch)

```shell
git checkout dev
```

```shell
git log -p
```

you get the pass to next level