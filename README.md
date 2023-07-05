# line-ending

```bash
$ file unix.txt
unix.txt: ASCII text

$ file windows.txt
windows.txt: ASCII text, with CRLF line terminators

$ file *.txt
unix.txt:    ASCII text
windows.txt: ASCII text, with CRLF line terminators
```

```bash
$ cat -v unix.txt
Z
Y
X

$ cat -v windows.txt
A^M
B^M
C^M
^M
```

```bash
$ unix2dos unix.txt
$ dos2unix windows.txt

$ file *.txt
unix.txt:    ASCII text, with CRLF line terminators
windows.txt: ASCII text
```

