>The password for the next level is stored in the file data.txt, which contains base64 encoded data

kali has a tool, base64 with which we can decode the base64 encoded text in command line

> base64 - base64 encode/decode data and print to standard output


```bash
base64 -d data.txt
```
