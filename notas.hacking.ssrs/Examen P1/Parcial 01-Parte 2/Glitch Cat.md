## Objetivo 

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.
## Solución  
```bash

biank-picoctf@webshell:~$ $ nc saturn.picoctf.net 49963
-bash: $: command not found
biank-picoctf@webshell:~$  nc saturn.picoctf.net 49963
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
^C
biank-picoctf@webshell:~$ $ nc saturn.picoctf.net 49963
-bash: $: command not found
biank-picoctf@webshell:~$  nc saturn.picoctf.net 49963
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}

```

## Notas Adicionales 
convertir los caracteres en hexadecimal que hay dentro de las llaves, a texto. Reemplazar los caracteres por el texto convertido y esa es tu flag.
### Referencias

https://www.rapidtables.com/convert/number/hex-to-ascii.html