## Objetivo 

What does asm2(0x4,0x2d) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/ceac75672637589213b952abe32c84b3/test.S)

## Solución  
```java 


┌──(kali㉿kali)-[~/Downloads/asm2]
└─$ ls                                    
test.S
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/asm2]
└─$ ls -la
total 40
drwxrwxr-x  2 kali kali  4096 Nov  5 23:54 .
drwxr-xr-x 59 kali kali 28672 Nov  5 23:54 ..
-rw-rw-r--  1 kali kali   478 Oct 26  2020 test.S
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/asm2]
└─$ cat test.S        
asm2:
        <+0>:        push   ebp
        <+1>:        mov    ebp,esp
        <+3>:        sub    esp,0x10
        <+6>:        mov    eax,DWORD PTR [ebp+0xc]
        <+9>:        mov    DWORD PTR [ebp-0x4],eax
        <+12>:        mov    eax,DWORD PTR [ebp+0x8]
        <+15>:        mov    DWORD PTR [ebp-0x8],eax
        <+18>:        jmp    0x50c <asm2+31>
        <+20>:        add    DWORD PTR [ebp-0x4],0x1
        <+24>:        add    DWORD PTR [ebp-0x8],0xd1
        <+31>:        cmp    DWORD PTR [ebp-0x8],0x5fa1
        <+38>:        jle    0x501 <asm2+20>
        <+40>:        mov    eax,DWORD PTR [ebp-0x4]
        <+43>:        leave  
        <+44>:        ret    








┌──(kali㉿kali)-[~/picoCTF/Reversing/asm2]

└─$ python3

Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux

Type "help", "copyright", "credits" or "license" for more information.

>>> int(0x5fa1)

24481

>>> int(0xd1)

209

>>> 0x5fa1 / 209

117.13397129186603

>>> int(0x2e)

46

>>> int(0xb)

11

>>> 117 + 46

163

>>> hex(163)

'0xa3'

```

  

Una vez realizadas las operaciones, obtenemos la bandera.

```
 0xa3

```



## Notas Adicionales 


### Referencias
