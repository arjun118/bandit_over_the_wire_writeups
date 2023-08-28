after loggin in using ssh, and changing the directory to "inhere" you can see some directories

text from the website:
>The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

>human-readable
1033 bytes in size
not executable


use the find command to find the file of size 1033 bytes

```bash
file . -size 1033c
```

    The suffix M denotes Megabytes that is 1048576 bytes. The other available suffixes to our disposal are:

    b – 512-byte blocks (this is the default if no suffix is used)
    c – bytes
    w – two-byte words
    k – Kilobytes
    M – Megabytes
    G – Gigabytes

[find file based on size](https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size)
