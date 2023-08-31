clone the repo

bascially we don't get anything from the README.md file. 
We also don't have any branches. let's check the .git directory which stores all the info


now going through the file i saw something interesting

```shell
# pack-refs with: peeled fully-peeled sorted 
59530d30d299ff2e3e9719c096ebf46a65cc1424 refs/remotes/origin/master
831aac2e2341f009e40e46392a4f5dd318483019 refs/tags/secret
```

[you can read about refs here](https://www.atlassian.com/git/tutorials/refs-and-the-reflog)


now we got a commit has, lets see what it has for us

```shell
git show 831aac2e2341f009e40e46392a4f5dd318483019
```

you get the pass for next level