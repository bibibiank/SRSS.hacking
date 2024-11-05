## Objetivo 
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución  
```bash
──(kali㉿kali)-[~]
└─$ ls
Desktop  Documents  Downloads  fondo.jpg  hacking  Music  Pictures  Public  Templates  Videos
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ cd Downloads      
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 big-zip-files.zip  'challenge(3).zip'   codebook.txt   drop-in    files.zip   level1.flag.txt.enc   level2.py
'challenge(1).zip'  'challenge(4).zip'   code.py        enc_flag   fixme1.py   level1.py
'challenge(2).zip'   challenge.zip       convertme.py   files      fixme2.py   level2.flag.txt.enc
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ python level2.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/kali/Downloads/level2.py", line 27, in <module>
    level_2_pw_check()
  File "/home/kali/Downloads/level2.py", line 17, in level_2_pw_check
    user_pw = input("Please enter correct password for flag: ")
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ nano level level2.py 
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ python level2.py    
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}



```


## Notas Adicionales 
en el codigo viene la contraseña en hexadecimal, con la ayuda de un convertidor a texto podemos decirfrarla.

### Referencias

[Hex to ASCII Text String Converter (rapidtables.com)](https://www.rapidtables.com/convert/number/hex-to-ascii.html)