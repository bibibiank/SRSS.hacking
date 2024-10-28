## Objetivo 

Attackers have hidden information in a very large mass of data in the past, maybe they are still doing it. Download the data [here](https://artifacts.picoctf.net/c/124/anthem.flag.txt).

## Solución  

```java
──(kali㉿kali)-[~/Downloads]
└─$ mkdir LookeyHere         
                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ cd LookeyHere 
                                                                       
┌──(kali㉿kali)-[~/Downloads/LookeyHere]
└─$ wget https://artifacts.picoctf.net/c/124/anthem.flag.txt
--2024-10-27 05:05:25--  https://artifacts.picoctf.net/c/124/anthem.flag.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108668 (106K) [application/octet-stream]
Saving to: ‘anthem.flag.txt’

anthem.flag.txt   100%[============>] 106.12K  --.-KB/s    in 0.1s    

2024-10-27 05:05:25 (833 KB/s) - ‘anthem.flag.txt’ saved [108668/108668]

                                                                       
┌──(kali㉿kali)-[~/Downloads/LookeyHere]
└─$ ls
anthem.flag.txt
                                                                       
┌──(kali㉿kali)-[~/Downloads/LookeyHere]
└─$ cat anthem.flag.txt  
      ANTHEM

      by Ayn Rand


        CONTENTS

         PART ONE

         PART TWO

         PART THREE


 For the coming of that day shall I fight, I and my sons and my
      chosen friends. For the freedom of Man. For his rights. For his
      life. For his honor.

      And here, over the portals of my fort, I shall cut in the stone
      the word which is to be my beacon and my banner. The word which
      will not die, should we all perish in battle. The word which can
      never die on this earth, for it is the heart of it and the
      meaning and the glory.

      The sacred word:

      EGO



                                                                       
┌──(kali㉿kali)-[~/Downloads/LookeyHere]
└─$ cat anthem.flag.txt | grep "picoCTF"
      we think that the men of picoCTF{gr3p_15_@w3s0m3_4c479940}

```
## Notas Adicionales 

### Referencias
