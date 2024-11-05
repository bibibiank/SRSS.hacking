## Objetivo 

Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.

## Solución  
```java 
──(kali㉿kali)-[~/Downloads]
└─$ cd picker4 
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/picker4]
└─$ wget https://artifacts.picoctf.net/c/527/picker-IV.c  
--2024-11-04 15:04:54--  https://artifacts.picoctf.net/c/527/picker-IV.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 839 [application/octet-stream]
Saving to: ‘picker-IV.c’

picker-IV.c                       100%[===========================================================>]     839  --.-KB/s 

2024-11-04 15:05:02 (16.4 MB/s) - ‘picker-IV.c’ saved [839/839]

                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/picker4]
└─$ wget https://artifacts.picoctf.net/c/527/picker-IV  
--2024-11-04 15:05:11--  https://artifacts.picoctf.net/c/527/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV                         100%[===========================================================>]  16.87K  --.-KB/s 

2024-11-04 15:05:20 (107 MB/s) - ‘picker-IV’ saved [17272/17272]

                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/picker4]
└─$ ls
picker-IV  picker-IV.c
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/picker4]
└─$ readelf -a picker-IV | grep win 

No processor specific unwind information to decode
    63: 000000000040129e   150 FUNC    GLOBAL DEFAULT   15 win
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/picker4]
└─$  nc saturn.picoctf.net 51454 
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_01672a61}


```

## Notas Adicionales 

### Referencias
