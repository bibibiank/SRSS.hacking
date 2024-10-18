## Objetivo 

The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

## Solución  
```java 

┌──(kali㉿kali)-[~/Downloads/TheNumbers]
└─$ wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png 
--2024-10-17 13:54:28--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.png              100%[==============================================>]  98.36K   224KB/s    in 0.4s    

2024-10-17 13:54:29 (224 KB/s) - ‘the_numbers.png’ saved [100721/100721]

┌──(kali㉿kali)-[~/Downloads/TheNumbers]
└─$ ls
the_numbers.png

┌──(kali㉿kali)-[~/Downloads/TheNumbers]
└─$ file the_numbers.png         
the_numbers.png: PNG image data, 774 x 433, 8-bit/color RGB, non-interlaced

┌──(kali㉿kali)-[~/Downloads/TheNumbers]
└─$ eog the_numbers.png 
```

al ejecutar `eog the_numbers.png` nos muestra esta imagen 
![[Pasted image 20241017115511.png]]

los números que nos da, es un código, lo cual debemos decodificarlo en cyberchef 

16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }

Flag: picoctf{thenumbersmason}
## Notas Adicionales 


- **A1Z26** es un cifrado por sustitución directa muy simple, donde cada letra del alfabeto se reemplaza por su número en el alfabeto.
### Referencias
