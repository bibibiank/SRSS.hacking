## Objetivo 

This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solución  

```java 
──(kali㉿kali)-[~]
└─$ cd Downloads              
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ file flag.txt             
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced

```
convertimos el archivo txt a png

```java
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 flag.png     level3.flag.txt.enc   level3.py   RetosWeb       'server(1).py'   strings
 garden.jpg   level3.hash.bin       picoCTF     serpentine.py   server.py       warm
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ eog  flag.png
Command 'eog' not found, but can be installed with:
sudo apt install eog
Do you want to install it? (N/y)y
sudo apt install eog
[sudo] password for kali: 
Upgrading:                      
  libssl3t64 openssl

Installing:
  eog

Installing dependencies:
  gir1.2-peas-1.0          libjxl-gdk-pixbuf libpython3.12-minimal openssl-provider-legacy
  gnome-desktop3-data      libjxl0.9         libpython3.12-stdlib  webp-pixbuf-loader
  libexempi8               libpeas-1.0-0     libpython3.12t64
  libgnome-desktop-3-20t64 libpeas-common    libxkbregistry0

Suggested packages:
  eog-plugins

Summary:
  Upgrading: 2, Installing: 15, Removing: 0, Not Upgrading: 1357
  Download size: 7,392 kB / 12.3 MB
  Space needed: 41.3 MB / 63.5 GB available


```

ejecutamos el archivo png con ub¿n eog 

```java 

┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 flag.png     level3.flag.txt.enc   level3.py   RetosWeb       'server(1).py'   strings
 garden.jpg   level3.hash.bin       picoCTF     serpentine.py   server.py       warm
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ eog  flag.png
Command 'eog' not found, but can be installed with:
sudo apt install eog
Do you want to install it? (N/y)y
sudo apt install eog
[sudo] password for kali: 
Upgrading:                      
  libssl3t64 openssl

Installing:
  eog

Installing dependencies:
  gir1.2-peas-1.0          libjxl-gdk-pixbuf libpython3.12-minimal openssl-provider-legacy
  gnome-desktop3-data      libjxl0.9         libpython3.12-stdlib  webp-pixbuf-loader
  libexempi8               libpeas-1.0-0     libpython3.12t64
  libgnome-desktop-3-20t64 libpeas-common    libxkbregistry0

Suggested packages:
  eog-plugins

Summary:
  Upgrading: 2, Installing: 15, Removing: 0, Not Upgrading: 1357
  Download size: 7,392 kB / 12.3 MB
  Space needed: 41.3 MB / 63.5 GB available

```

![[Pasted image 20241003153118.png]]
## Notas Adicionales 

### Referencias

{}