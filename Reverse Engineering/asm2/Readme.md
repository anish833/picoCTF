Challenge:
```
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). 
NOTE: Your submission for this question will NOT be in the normal flag format. Source
```

They provide a source in assembly
```
asm2:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   sub    esp,0x10
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]   eax = 0x21
        <+9>:   mov    DWORD PTR [ebp-0x4],eax   ebp-0x4 = eax = 0x21
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]   eax = 0x4
        <+15>:  mov    DWORD PTR [ebp-0x8],eax   ebp-0x8 = eax = 0x4
        <+18>:  jmp    0x509 <asm2+28>           
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0x74
        <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46
        <+35>:  jle    0x501 <asm2+20>
        <+37>:  mov    eax,DWORD PTR [ebp-0x4]
        <+40>:  leave  
        <+41>:  ret    

```
As we can see this time they are passing two arguements in the code. We can see that it is subtracting ```0x10``` from ```esp``` but we can skip the
first lines because we are interested in the position of the variable. We know that ```ebp-0x8``` is where the variable is. So as now they are passing
two values and and assembly take 4 bytes for storing so ```ebp-0xc``` will have the value ```0x21``` . From instruction ```<+6> to <+15>``` they are moving the values
to different pointers using ```eax```. The pseudo code is 
```
        <+6>:    eax = 0x21
        <+9>:    ebp-0x4 = eax = 0x21
        <+12>:   eax = 0x4
        <+15>:   ebp-0x8 = eax = 0x4
```

Now ```ebp-0x4``` have the value ```0x21``` and ```ebp-0x8``` have the value ```0x4```. On next instruction ```<+18> ``` it is jumping to instruction ```<+28>```
On instruction 28 it is compairing ```0x4 to 0xfb46``` and it uses ```jle``` which means ```jump if less than equal to``` . On jumping to instruction ```<+20>```
It is simply adding ```0x1 to 0x21``` and ```0x74 to 0x4``` after that it again goes to the comparision. So it will take time to solve it manually to I created a 
python script to do this for my

```
#!/usr/bin/env python3

a = int('0x21', 16)
b = int('0x4', 16)
c = int('0xfb46', 16)

while b <= c:
        a += int('0x1', 16)
        b += int('0x74', 16)

print(hex(a)) 
```

Running this script will give you the flag

flag: ```0x24c```
