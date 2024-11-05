## Objetivo 

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.

## Solución  

```bash
┌──(kali㉿kali)-[~]
└─$ cd Downloads      
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ ls    
 big-zip-files.zip  'challenge(3).zip'   codebook.txt   drop-in    files.zip   level1.flag.txt.enc
'challenge(1).zip'  'challenge(4).zip'   code.py        enc_flag   fixme1.py   level1.py
'challenge(2).zip'   challenge.zip       convertme.py   files      fixme2.py
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ python level1.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/kali/Downloads/level1.py", line 28, in <module>
    level_1_pw_check()
  File "/home/kali/Downloads/level1.py", line 18, in level_1_pw_check
    user_pw = input("Please enter correct password for flag: ")
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ cat level1.flag.txt.enc 
[gE]__TgS^S

           J                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ nano level1.py 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ python level1.py       
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}

```
## Notas Adicionales 

### Referencias
