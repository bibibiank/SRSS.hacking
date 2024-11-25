## Objetivo 

Can you decrypt this message? Decrypt this [message](https://artifacts.picoctf.net/c/158/cipher.txt) using this key "CYLAB".
## Solución  

```java
┌──(kali㉿kali)-[~/Downloads/vigenere]
└─$ wget https://artifacts.picoctf.net/c/160/cipher.txt
--2024-11-23 00:08:51--  https://artifacts.picoctf.net/c/160/cipher.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.225.222.28, 13.225.222.120, 13.225.222.125, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.225.222.28|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt    100%      43  --.-KB/s    in 0s          

2024-11-23 00:08:51 (25.9 MB/s) - ‘cipher.txt’ saved [43/43]

                                                        
┌──(kali㉿kali)-[~/Downloads/vigenere]
└─$ ls
cipher.txt
                                                        
┌──(kali㉿kali)-[~/Downloads/vigenere]
└─$ cat cipher.txt  
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_2951c89f}
                                                       
```
Nos da una bandera y con ayuda de cyberchef y la palabra clave "CYLAB" desciframos la bandera

```java
picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_2951a89h}

```
## Notas Adicionales 

### Referencias
