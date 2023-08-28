I cannot come up with solution, 'cause i forgot the scp command

```
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
```

we get to know the sshkey.private is present in the home directory of bandit13 after logging in

after getting hold of the private key you can execute

```bash
ssh -i sshkey.private bandit13@bandit.labs.overthewire.org -p 2220
```

refer [site](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)