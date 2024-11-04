## Objetivo 

What can you do with this file? I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/289/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

## Solución  

```java 
┌──(kali㉿kali)-[~/Downloads/safeOpener]
└─$ wget https://artifacts.picoctf.net/c/289/SafeOpener.class
--2024-11-04 15:09:14--  https://artifacts.picoctf.net/c/289/SafeOpener.class
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class              100%[================================================>]   1.99K  --.-KB/s    in 0s      

2024-11-04 15:09:23 (38.9 MB/s) - ‘SafeOpener.class’ saved [2036/2036]

                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/safeOpener]
└─$ ls
SafeOpener.class
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/safeOpener]
└─$ file SafeOpener.class 
SafeOpener.class: compiled Java class data, version 52.0 (Java 1.8)
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/safeOpener]
└─$ strings SafeOpener.class | grep picoCTF   
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}
                                                                                                                       
┌──(kali㉿kali)-[~/Downloads/safeOpener]
└─$ 

```

picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}
## Notas Adicionales 

### Referencias
