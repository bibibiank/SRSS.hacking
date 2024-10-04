## Objetivo 

There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

## Solución  
```java 

──(kali㉿kali)-[~/Downloads]
└─$ sudo gem install zsteg                          
Fetching iostruct-0.1.3.gem
Fetching zpng-0.4.5.gem
Fetching rainbow-3.1.1.gem
Fetching zsteg-0.2.13.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.1.3
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.1.3
Installing ri documentation for iostruct-0.1.3
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 1 seconds
4 gems installed
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ zsteg -a buildings.png |  grep pico                                                 
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

```

## Notas Adicionales 

zsteg-- El comando `zsteg` es una herramienta utilizada principalmente en la investigación forense digital y en la esteganografía. Sirve para detectar y extraer información oculta en imágenes, especialmente en formatos como PNG y BMP

### Referencias