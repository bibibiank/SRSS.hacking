## Objetivo 

We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.

## Solución  

```java 

└─$ cd reversecipher 
┌──(kali㉿kali)-[~/Downloads/reversecipher]
└─$ wget https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev
--2024-11-06 12:25:17--  https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16856 (16K) [application/octet-stream]
Saving to: ‘rev’

rev                          100%[=============================================>]  16.46K  --.-KB/s    in 0s      

2024-11-06 12:25:19 (159 MB/s) - ‘rev’ saved [16856/16856]
┌──(kali㉿kali)-[~/Downloads/reversecipher]
└─$ wget https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this
--2024-11-06 12:25:27--  https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24 [application/octet-stream]
Saving to: ‘rev_this’

rev_this                     100%[=============================================>]      24  --.-KB/s    in 0s      

2024-11-06 12:25:31 (26.2 MB/s) - ‘rev_this’ saved [24/24]
┌──(kali㉿kali)-[~/Downloads/reversecipher]
└─$ file rev  
rev: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=523d51973c11197605c76f84d4afb0fe9e59338c, not stripped
┌──(kali㉿kali)-[~/Downloads/reversecipher]
└─$ cat rev_this 
picoCTF{w1{1wq8/7376j.:}   

```
nos dio una bandera encriptada, instlamos una herramienta llamada ghidra, para desencriptar la bandera

```java 
┌──(kali㉿kali)-[~/Downloads/reversecipher]
└─$ sudo apt install ghidra     
[sudo] password for kali: 
Upgrading:                      
  openjdk-17-jre openjdk-17-jre-headless

Installing:
  ghidra

Installing dependencies:
  ghidra-data openjdk-17-jdk openjdk-17-jdk-headless
Suggested packages:
  openjdk-17-demo openjdk-17-source visualvm

Summary:
  Upgrading: 2, Installing: 4, Removing: 0, Not Upgrading: 1347
  Download size: 539 MB
  Space needed: 1,244 MB / 51.5 GB available

```

## Notas Adicionales 

### Referencias
