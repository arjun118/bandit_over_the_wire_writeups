>The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

actually I forgot the command essential command.

i did not check the file type before trying out grep with some regex and all, but after checking the file type it came out to be data, which means a binary file format


we got a handy command 
```bash
strings
```

>  strings - print the sequences of printable characters in files


lets pipe the output of strings command to grep using the hint given on the website

```bash
string data.txt | grep ==
```
