## Objetivo

I wonder what this really is... [enc](https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc) ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

## Solución

```java
┌──(kali㉿kali)-[~/Downloads/reversing]
└─$ wget https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc       
--2024-11-23 01:42:31--  https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 57 [application/octet-stream]
Saving to: ‘enc’

enc           100%      57  --.-KB/s    in 0s         

2024-11-23 01:42:31 (54.1 MB/s) - ‘enc’ saved [57/57]

                                                       
┌──(kali㉿kali)-[~/Downloads/reversing]
└─$ ls
asciiftw  crackme.py  enc
                                                       
┌──(kali㉿kali)-[~/Downloads/reversing]
└─$ cat enc          
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸弲㘶㠴挲ぽ                                                       
┌──(kali㉿kali)-[~/Downloads/reversing]
└─$ nano solve.py
                                                       
┌──(kali㉿kali)-[~/Downloads/reversing]
└─$ python3 solve.py  
Flag: picoCTF{16_bits_inst34d_of_8_26684c20}

```
Flag: picoCTF{16_bits_inst34d_of_8_26684c20}