## Objetivo 

Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext)


## Solución  
```java 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd caesar 
┌──(kali㉿kali)-[~/Downloads/caesar]
└─$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext     
--2024-10-17 14:19:13--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                   100%[==============================================>]      35  --.-KB/s    in 0s      

2024-10-17 14:19:16 (40.1 MB/s) - ‘ciphertext’ saved [35/35]
┌──(kali㉿kali)-[~/Downloads/caesar]
└─$ ls
ciphertext
┌──(kali㉿kali)-[~/Downloads/caesar]
└─$ cat ciphertext      
picoCTF{ynkooejcpdanqxeykjrbdofgkq}  
```
picoCTF{laxbbrwpcqnadkrlxweoqbstxd}


- Con CyberChef y ROT30 


```picoCTF{crossingtherubicondjneoach}```

## Notas Adicionales 

### Referencias


