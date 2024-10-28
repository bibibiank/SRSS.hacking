
## Objetivo 

Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/195/network-dump.flag.pcap)
## Solución  
```java
┌──(kali㉿kali)-[~/Downloads/PAcketsPrimer]
└─$ wget https://artifacts.picoctf.net/c/195/network-dump.flag.pcap
--2024-10-27 04:43:21--  https://artifacts.picoctf.net/c/195/network-dump.flag.pcap
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 778 [application/octet-stream]
Saving to: ‘network-dump.flag.pcap’

network-dump.flag 100%[============>]     778  --.-KB/s    in 0s      

2024-10-27 04:43:22 (27.2 MB/s) - ‘network-dump.flag.pcap’ saved [778/778]

                                                                       
┌──(kali㉿kali)-[~/Downloads/PAcketsPrimer]
└─$ ls
network-dump.flag.pcap
                                                                       
┌──(kali㉿kali)-[~/Downloads/PAcketsPrimer]
└─$ file network-dump.flag.pcap                                 
network-dump.flag.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                       
┌──(kali㉿kali)-[~/Downloads/PAcketsPrimer]
└─$ wireshark network-dump.flag.pcap  &                            
[1] 97533
                                                                       
┌──(kali㉿kali)-[~/Downloads/PAcketsPrimer]
└─$ 



```
seleccionamos un archivo, le damos  clic derecho, luego follow y ahi nos sale la bandera, ya solo le quitamos los espacios

picoCTF{p4ck37_5h4rk_b9d53765}
## Notas Adicionales 

### Referencias
