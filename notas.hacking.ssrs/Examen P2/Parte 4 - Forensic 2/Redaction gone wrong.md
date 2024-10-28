## Objetivo 

Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

## Solución  

```java
┌──(kali㉿kali)-[~/Downloads/RedactionGoneWrong]
└─$ ls                                               
Financial_Report_for_ABC_Labs.pdf

┌──(kali㉿kali)-[~/Downloads/RedactionGoneWrong]
└─$ file Financial_Report_for_ABC_Labs.pdf           
Financial_Report_for_ABC_Labs.pdf: PDF document, version 1.7, 1 page(s)

┌──(kali㉿kali)-[~/Downloads/RedactionGoneWrong]
└─$ open Financial_Report_for_ABC_Labs.pdf          
```

abrimos el archivo

```java
picoCTF{C4n_Y0u_S33_m3_fully}
```
## Notas Adicionales 

### Referencias
