I am sure this can be automated but i just don't know how, still searching :)

this is how i solved this level

> 1. first i converted the hexdump to binary file using xxd

make a directory in tmp using 

> mkdir /tmp/test

then copy the data.txt to that new directory so that we can start working there

> cp data.txt /tmp/test

> 

```bash
xxd -r data.txt | comp 
``` 

from then on i checked the file type of the output using file command and turns out all of them are compressed files

the compressed file types are gz, bz2 and tar

> if the file type is gzip, first rename the output to something like filename.gz , then only you can decompress

```bash
gzip -d file.gz
``` 

same goes with bzip2

```bash
bzip2 -d file.bz2
```

for tar files

```bash
tar -xvf file
```

keep on doing this until you get the pass for the next level :(

---

refer to these blogs for more info on compression techniques in linux and may be one can solve this level in a much beter way

https://linuxhint.com/linux_file_compression/

https://www.cyberciti.biz/howto/question/general/compress-file-unix-linux-cheat-sheet.php

https://legacy.redhat.com/pub/redhat/linux/7.1/it/doc/RH-DOCS/en/rhl-gsg-en-7.1/s1-zip-tar.html
