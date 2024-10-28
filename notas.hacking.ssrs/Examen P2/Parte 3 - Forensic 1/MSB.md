
## Objetivo 
This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image... Download the image [here](https://artifacts.picoctf.net/c/307/Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisada.flag.png)

## Solución  

nos vamos a la pagina de stegOnline y metemos la imagen, extraemos los datos de la imagen y lo guardamos donde tenemos el reto

```java 

──(kali㉿kali)-[~/Downloads/MSB]
└─$ ls
Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisadaflag.dat   text.txt
Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisada.flag.png
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/MSB]
└─$ cat Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisadaflag.dat 
The Project Gutenberg eBook of The History of Don Quixote, by Miguel de Cervantes

This eBook is for the use of anyone anywhere in the United States and
most other parts of the world at no cost and with almost no restrictions
whatsoever. You may copy it, give it away or re-use it under the terms




┌──(kali㉿kali)-[~/Downloads/MSB]
└─$ cat Ninja-and-Prince-Genji-Ukiyoe-Utagawa-Kunisadaflag.dat    | grep  picoCTF  
picoCTF{15_y0ur_que57_qu1x071c_0r_h3r01c_b5e03bc5}


```
## Notas Adicionales 

### Referencias
https://georgeom.net/StegOnline/extract