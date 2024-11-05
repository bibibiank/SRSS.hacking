## Objetivo 

We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/129/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución  

```java 
──(kali㉿kali)-[~/Downloads/BasicMod1]
└─$ ls
basic.py  message.txt  message.txt.1
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/BasicMod1]
└─$ nano basic.py
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/BasicMod1]
└─$ python3 basic.py
R
0
U
N
D
_
N
_
R
0
U
N
D
_
A
D
D
1
7
E
C
2
R0UND_N_R0UND_ADD17EC2
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Downloads/BasicMod1]

picoCTF{R0UND_N_R0UND_ADD17EC2}

```

## Notas Adicionales 

### Referencias

