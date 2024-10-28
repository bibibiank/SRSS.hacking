
## Objetivo 

Download this packet capture and find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/134/capture.flag.pcap)
## Solución  

abrimos el archivo con el wire shark.

```java 
┌──(kali㉿kali)-[~/Downloads/information]
└─$ ls
capture.flag.pcap

┌──(kali㉿kali)-[~/Downloads/information]
└─$ file capture.flag.pcap 
capture.flag.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)

┌──(kali㉿kali)-[~/Downloads/information]
└─$ wireshark capture.flag.pcap &                                
[1] 6122

┌──(kali㉿kali)-[~/Downloads/information]
└─$ Warning: program compiled against libxml 212 using older 209

```

Seleccionamos un archivo > Follow > TCP Steam; aquí nos muestra una conversación en donde le envía el comando para descomprimir el archivo

```java 
Hey, how do you decrypt this file again?

You're serious?

Yeah, I'm serious

*sigh* openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123

Ok, great, thanks.

Let's use Discord next time, it's more secure.

C'mon, no one knows we use this program like this!

Whatever.

Hey.

Yeah?

Could you transfer the file to me again?

Oh great. Ok, over 9002?

Yeah, listening.

Sent it

Got it.

You're unbelievable
```

navegamos entre los paquetes donde dice Stream, en el paquete numero 2 encontramos lo siguiente:
```html
Salted__...<.P...O.r..E~cbk.......p&.}........F
```

 donde dice show data, nos dice que esta en ASCII, lo cambiamos a Raw y lo guardamos
 
```java
53616c7465645f5fd30c863ca650da1fff4fbe72a086457e63626beda615c692cdd27026ae7deea6d1e918b3d40a7f46
```

guardamos el archivo como `file.des3` 

```java
┌──(kali㉿kali)-[~/Downloads/eavesdrop]
└─$ ls 
capture.flag.pcap  file.des3
```

```java
┌──(kali㉿kali)-[~/Downloads/eavesdrop]
└─$ openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
                                                        
┌──(kali㉿kali)-[~/Downloads/eavesdrop]
└─$ ls
capture.flag.pcap  file.des3  file.txt
                                                        
┌──(kali㉿kali)-[~/Downloads/eavesdrop]
└─$ cat file.txt 


```
picoCTF{nc_73115_411_5786acc3}                                                        
## Notas Adicionales 

### Referencias
