
## Objetivo

crackme.py 

## Solución 
```java 
┌──(kali㉿kali)-[~/Downloads/reversing/crackme]
└─$ wget https://mercury.picoctf.net/static/f440bf2510a28914afae2947749f2db0/crackme.py
--2024-11-23 02:13:02--  https://mercury.picoctf.net/static/f440bf2510a28914afae2947749f2db0/crackme.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1463 (1.4K) [application/octet-stream]
Saving to: ‘crackme.py’

crackme.py    100%   1.43K  --.-KB/s    in 0s         

2024-11-23 02:13:02 (29.6 MB/s) - ‘crackme.py’ saved [1463/1463]

                                                       
┌──(kali㉿kali)-[~/Downloads/reversing/crackme]
└─$ ls    
crackme.py
                                                       
┌──(kali㉿kali)-[~/Downloads/reversing/crackme]
└─$ file crackme.py
crackme.py: Python script, ASCII text executable
                                                       
┌──(kali㉿kali)-[~/Downloads/reversing/crackme]
└─$  nano crackme.py
                                                       
┌──(kali㉿kali)-[~/Downloads/reversing/crackme]
└─$ python3 crackme.py 
What's your first number? 1
What's your second number? 0
The number with largest positive magnitude is 1
picoCTF{1|\/|_4_p34|\|ut_8c551048}

```