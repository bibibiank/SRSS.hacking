## Objetivo 
This service can provide you with a random number, but can it do anything else?

Additional details will be available after launching your challenge instance.

## Solución  
```java
┌──(kali㉿kali)-[~/Downloads]
└─$ cd picker1 
                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/picker1]
└─$ wget https://artifacts.picoctf.net/c/513/picker-I.py                                               
--2024-11-04 14:28:13--  https://artifacts.picoctf.net/c/513/picker-I.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3429 (3.3K) [application/octet-stream]
Saving to: ‘picker-I.py’

picker-I.py                       100%[===========================================================>]   3.35K  --.-KB/s    in 0s      

2024-11-04 14:28:22 (63.3 MB/s) - ‘picker-I.py’ saved [3429/3429]

                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/picker1]
└─$ ls
picker-I.py
                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/picker1]
└─$ nano picker-I.py 
                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads/picker1]
└─$ nc saturn.picoctf.net 59445 
```

ingresamos la palabra win y nos dará un codigo en hexa 
```java 
Try entering "getRandomNumber" without the double quotes...
==> win
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x62 0x35 0x32 0x33 0x62 0x32 0x61 0x31 0x7d 
Try entering "getRandomNumber" without the double quotes...
==>               


```
metemos el codigo en cyberchef con   la opcion de hexadecimal, esa será la bandera

```java 
picoCTF{4_d14m0nd_1n_7h3_r0ugh_b523b2a1}
```


## Notas Adicionales 

### Referencias
