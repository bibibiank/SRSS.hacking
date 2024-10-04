## Objetivo 

This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.

## Solución  


ingresamos a donde tenemos la imagen guardada con un cd

después con un grep, buscamos la palabra picoCTF en la imagen, y eso nos dará la bandera
```java

└─$ cd Downloads         
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ strings garden.jpg | grep picoCTF      
Here is a flag "picoCTF{more_than_m33ts_the_3y3657BaB2C}"

```

## Notas Adicionales 

### Referencias

