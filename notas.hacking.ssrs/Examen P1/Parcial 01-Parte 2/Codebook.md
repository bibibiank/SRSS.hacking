## Objetivo 

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

## Solución  

```bash

┌──(kali㉿kali)-[~]
└─$ cd Downloads      
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 big-zip-files.zip  'challenge(2).zip'  'challenge(4).zip'   codebook.txt   drop-in    files
'challenge(1).zip'  'challenge(3).zip'   challenge.zip       code.py        enc_flag   files.zip
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ python code.py 
picoCTF{c0d3b00k_455157_7d102d7a}
                                                    ┌──(kali㉿kali)-[~/Downloads]
└─$ cat codebook.txt
azbycxdwevfugthsirjqkplomn


```

## Notas Adicionales 

### Referencias