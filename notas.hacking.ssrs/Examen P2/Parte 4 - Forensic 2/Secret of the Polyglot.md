## Objetivo 

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf).

## Solución  

```java
──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ wget https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf
--2024-10-27 05:36:36--  https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf           100%[==============================================>]   3.28K  --.-KB/s    in 0s      

2024-10-27 05:36:36 (71.9 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]

┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ ls
flag2of2-final.pdf
┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ file flag2of2-final.pdf   
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]

```

nos salió la ultima parte de la bandera
```java 
1n_pn9_&_pdf_90974127}
```

```java

┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ cp flag2of2-final.pdf  image.png

┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ ls
flag2of2-final.pdf  image.png

┌──(kali㉿kali)-[~/Downloads/SecretOfThePolyglot]
└─$ open image.png         
```


![[Pasted image 20241027035446.png]]

juntamos las partes

```java 
picoCTF{f1u3n7_1n_pn9_&_pdf_90974127}
```
## Notas Adicionales 

### Referencias


