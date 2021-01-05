Challenge:
```
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). 
NOTE: Your submission for this question will NOT be in the normal flag format. Source
```

They game me a assembly code
```
asm1:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3a2
        <+10>:  jg     0x512 <asm1+37>
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x358
        <+19>:  jne    0x50a <asm1+29>
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]
        <+24>:  add    eax,0x12
        <+27>:  jmp    0x529 <asm1+60>
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]
        <+32>:  sub    eax,0x12
        <+35>:  jmp    0x529 <asm1+60>
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x6fa
        <+44>:  jne    0x523 <asm1+54>
        <+46>:  mov    eax,DWORD PTR [ebp+0x8]
        <+49>:  sub    eax,0x12
        <+52>:  jmp    0x529 <asm1+60>
        <+54>:  mov    eax,DWORD PTR [ebp+0x8]
        <+57>:  add    eax,0x12
        <+60>:  pop    ebp
        <+61>:  ret    

```

The first 2 lines is just simply putting ```0x6fa``` to the stack. It first put the value into ebp then it moved to esp, this just means that 
this value is now in the first position in the stack now at ebp+0x8. On line 3 it is comparing ```0x3a2``` to ```0x6fa``` and on ```+10``` it is using
```jg``` which means ```jump if greater than```. Since 0x6fa is indeed greater than 0x3a2, we jump to the line given by this condition: line 37.
On line 37 there is another comparison where ```0x6fa``` is compared to ```0x6fa``` and in next line it is using ```jne``` which means ```jump if
not equal to``` but it doesn't satisfy the condition so we go to the next instruction. In instruction ```46``` it is moving ```0x6fa``` to ```eax```
and on instruction ```49``` it is substracting ```0x12``` from ```0x6fa`` which will give ```0x6e8```. You can use ```https://www.calculator.net/hex-calculator.html```
for calculation. After that on instruction ```52``` it used ```jmp``` which means ```jump to``` and given the instruction number to jump to i.e., ```60``` and on 60
the stack is popped and eax is returned. Since eax is equal to 0x6e8, that is our flag.

flag: ```0x6e8```
