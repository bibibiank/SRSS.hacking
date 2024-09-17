## Objetivo 

Fix the syntax error in the Python script to print the flag.
## Solución  

```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 big-zip-files.zip  'challenge(3).zip'   codebook.txt   drop-in    files.zip
'challenge(1).zip'  'challenge(4).zip'   code.py        enc_flag   fixme1.py
'challenge(2).zip'   challenge.zip       convertme.py   files      fixme2.py
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ nano fixme2.py 
                                                                                                                     
┌──(kali㉿kali)-[~/Downloads]
└─$ python fixme2.py 
  File "/home/kali/Downloads/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
┌──(kali㉿kali)-[~/Downloads]
└─$ nano fixme2.py 
┌──(kali㉿kali)-[~/Downloads]
└─$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
                                                    




```
## Notas Adicionales 

### Referencias
