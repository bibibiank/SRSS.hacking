## Objetivo 
```bash
Can you make sense of this file? 
Download the file [here](https://artifacts.picoctf.net/c/475/enc_flag).

```

## Solución  

```bash





                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RGt5TnpZM1pESjlDZz09Cg==
                          

┌──(kali㉿kali)-[~/Downloads]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNDkyNzY3ZDJ9Cg==

┌──(kali㉿kali)-[~/Downloads]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}
```

## Notas Adicionales 

### Referencias
