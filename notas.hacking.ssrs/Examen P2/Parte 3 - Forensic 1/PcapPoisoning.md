## Objetivo 

How about some hide and seek heh? Download this [file](https://artifacts.picoctf.net/c/377/trace.pcap) and find the flag.

## Solución  
```java 
┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$ ls
trace.pcap

┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$ file trace.pcap            
trace.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Raw IPv4, capture length 65535)

┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$ wireshark trace.pcap &                                
[1] 6428

┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$ Warning: program compiled against libxml 212 using older 209

[1]  + done       wireshark trace.pcap
```

buscamos la bandera

```java 
┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$ strings trace.pcap | grep picoCTF{       
picoCTF{P64P_4N4L7S1S_SU55355FUL_31010c46}F~



┌──(kali㉿kali)-[~Downloads/pcappoisoning]
└─$
```
## Notas Adicionales 

### Referencias
