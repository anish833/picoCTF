Challenge:
```
Decrypt this message.
```
They provide me with a text file which have the text : ```picoCTF{dspttjohuifsvcjdpoabrkttds}```
As the name of the challenge suggest it is a Caesar Cipher. So for decoding it you can use ```cyberchef``` but you have to manually set the shift so I went to the site
```https://www.dcode.fr``` which have hundreds of cipher decoders. I searched for Caeser cipher, set the mode to bruteforce as we don't know the shift and ran the content 
of the flag except the ```picoCTF``` part and got the flag.

```
picoCTF{crossingtherubiconzaqjsscr}
```
