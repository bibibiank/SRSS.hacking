## Objetivo 

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución  
```bash

──(kali㉿kali)-[~/Downloads]
└─$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py  picoCTF  strings  warm
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/kali/Downloads/level3.py", line 39, in <module>
    level_3_pw_check()
  File "/home/kali/Downloads/level3.py", line 27, in level_3_pw_check
    user_pw = input("Please enter correct password for flag: ")
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
KeyboardInterrupt

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ nano level3.py 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat level3.flag.txt.enc 
B[ZZqfN_
        ]mTU\[UmS

X
 TD                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat level3.hash.bin 
m`��TA
      45���&                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat level3.py 
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()


def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ oython level3.py 
Command 'oython' not found, did you mean:
  command 'jython' from deb jython
  command 'cython' from deb cython3
  command 'python' from deb python-is-python3
Try: sudo apt install <deb name>
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py
Please enter correct password for flag: d3ab
That password is incorrect
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
                                   

```

## Notas Adicionales 

### Referencias

