## Objetivo 
What does asm1(0x6fa) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/b41e08fc19ceb9d0466ebd68d36c5630/test.S)

## Solución  

```java 
┌──(kali㉿kali)-[~/Downloads/asm1]
└─$ cat test.S                   
asm1:
        <+0>:        push   ebp
        <+1>:        mov    ebp,esp
        <+3>:        cmp    DWORD PTR [ebp+0x8],0x3a2
        <+10>:        jg     0x512 <asm1+37>
        <+12>:        cmp    DWORD PTR [ebp+0x8],0x358
        <+19>:        jne    0x50a <asm1+29>
        <+21>:        mov    eax,DWORD PTR [ebp+0x8]
        <+24>:        add    eax,0x12
        <+27>:        jmp    0x529 <asm1+60>
        <+29>:        mov    eax,DWORD PTR [ebp+0x8]
        <+32>:        sub    eax,0x12
        <+35>:        jmp    0x529 <asm1+60>
        <+37>:        cmp    DWORD PTR [ebp+0x8],0x6fa
        <+44>:        jne    0x523 <asm1+54>
        <+46>:        mov    eax,DWORD PTR [ebp+0x8]
        <+49>:        sub    eax,0x12
        <+52>:        jmp    0x529 <asm1+60>
        <+54>:        mov    eax,DWORD PTR [ebp+0x8]
        <+57>:        add    eax,0x12
        <+60>:        pop    ebp
        <+61>:        ret    


┌──(kali㉿kali)-[~/Downloads/asm1]
└─$ python3 
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 0x6fa > 0x3a2
True
>>> 0x6fa !=  0x6fa
False
>>> hex (0x6fa-0x12)
'0x6e8'
>>> 





```

## Notas Adicionales 

### Referencias
