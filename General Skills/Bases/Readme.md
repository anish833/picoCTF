Challenge:
```
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
```

It is a base64 strings. You can tell this by seeing the mixed alphabets of lowercase and uppercase. I used my terminal for decrypting this, the command is
```
echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
```
here ```-d``` means decode so it gave me the output ```l3arn_th3_r0p35```

Wrap it in picoCTF

flag:```picoCTF{l3arn_th3_r0p35}```
