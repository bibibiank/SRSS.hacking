## Objetivo
Use srch_strings from the sleuthkit and some terminal-fu to find a flag in this disk image: dds1-alpine.flag.img.gz

## Solución
Instalamos Sleuth Kit y Autopsy.
```java

──(kali㉿kali)-[~/Downloads]
└─$ cd diskdisksleuth 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ sudo apt install sleuthkit 
[sudo] password for kali: 
sleuthkit is already the newest version (4.12.1+dfsg-0kali6).
sleuthkit set to manually installed.
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 1357
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ sudo apt install autopsy  
autopsy is already the newest version (2.24-6kali1).
autopsy set to manually installed.
Summary:
  Upgrading: 0, Installing: 0, Removing: 0, Not Upgrading: 1357
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ ls                           
dds1-alpine.flag.img.gz
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ file dds1-alpine.flag.img.gz 
dds1-alpine.flag.img.gz: gzip compressed data, was "dds1-alpine.flag.img", last modified: Tue Mar 16 00:19:44 2021, from Unix, original size modulo 2^32 134217728
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ mmls dds1-alpine.flag.img.gz 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ srch_strings dds1-alpine.flag.img | grep pico
'dds1-alpine.flag.img': No such file
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ mmls dds1-alpine.flag.img.                   
Error stat(ing) image file (raw_open: image "dds1-alpine.flag.img." - No such file or directory)
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ gzip -d dds1-alpine.flag.img.gz
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ ls
dds1-alpine.flag.img
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ file dds1-alpine.flag.img                    
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ mmls dds1-alpine.flag.img      
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000262143   0000260096   Linux (0x83)
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/diskdisksleuth]
└─$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a69a712c}
```
## Notas Adicionales 

### Referencias