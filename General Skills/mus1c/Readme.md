Challenge:
```
I wrote you a song. Put it in the picoCTF{} flag format
```
This gave me a text file which have the content
```
Pico's a CTFFFFFFF
my mind is waitin
It's waitin

Put my mind of Pico into This
my flag is not found
put This into my flag
put my flag into Pico


shout Pico
shout Pico
shout Pico

My song's something
put Pico into This

Knock This down, down, down
put This into CTF

shout CTF
my lyric is nothing
Put This without my song into my lyric
Knock my lyric down, down, down

shout my lyric

Put my lyric into This
Put my song with This into my lyric
Knock my lyric down

shout my lyric

Build my lyric up, up ,up

shout my lyric
shout Pico
shout It

Pico CTF is fun
security is important
Fun is fun
Put security with fun into Pico CTF
Build Fun up
shout fun times Pico CTF
put fun times Pico CTF into my song

build it up

shout it
shout it

build it up, up
shout it
shout Pico
```

It took me some time to figure out that it is a esoteric language called rockstar. So searching for online decoder I got this website ```https://codewithrockstar.com/online```
and decoding it gave me 
```
114 114 114 111 99 107 110 114 110 48 49 49 51 114
```

These are decimal numbers so converting it to ascii from ```cyberchef``` gave me ```rrrocknrn0113r``` which is the flag

flag:```picoCTF{rrrocknrn0113r}```
