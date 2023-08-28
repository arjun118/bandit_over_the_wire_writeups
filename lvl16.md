If you want to learn about ssl cetrtificates and openssl essentially I would suggesting watching the  youtube playlist below

[Playlist](https://www.youtube.com/playlist?list=PLIFyRwBY_4bTwRX__Zn4-letrtpSj1mzY)


    The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

    Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…


I still am figuring out what HEARTBEATING and Read R BLOCK essentially mean, but following the note ..you know...I got past it

> -ign_eof
inhibit shutting down the connection when end of file is reached in the input.
    
```bash
openssl s_client -connect localhost:30001 -ign_eof
```

submit the pass for this level when the prompt gets stuck at read R and you will get the pass for the next level