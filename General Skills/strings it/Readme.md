Challenge:
```
Can you find the flag in file without running it?
```
It gave a file name strings. Running ```file``` command on the file 

```
strings: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=047a5079a5f563cd0e540d28f42a37161093ffda, not stripped
```

It is a binary file runnings strings on it gave a lot of output so I pipe the command to grep ```pico```. The command was
```
strings strings | grep pico
```

It will get all the lines that have pico in it and our flag also starts with pico and it gave me the flag

flag:```picoCTF{5tRIng5_1T_827aee91}```
