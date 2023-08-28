> The password for the next level is stored in the file data.txt and is the only line of text that occurs only once


after logging in you can find the data.txt file.

you can sort the file and output only the unique lines

uniq command only works when the input is sorted, cause it will discard the duplicate adjacent lines

you can read the man page of uniq for more info

```bash
sort data.txt | uniq -u
```

