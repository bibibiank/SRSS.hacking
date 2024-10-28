## Objetivo 
'Suspicious' is written all over this disk image. Download [suspicious.dd.sda1](https://jupiter.challenges.picoctf.org/static/0d39390cff1ab51699596b6e650e7cba/suspicious.dd.sda1)

## Solución  
```java
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$ wget https://jupiter.challenges.picoctf.org/static/0d39390cff1ab51699596b6e650e7cba/suspicious.dd.sda1
--2024-10-27 05:09:21--  https://jupiter.challenges.picoctf.org/static/0d39390cff1ab51699596b6e650e7cba/suspicious.dd.sda1
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 32868864 (31M) [application/octet-stream]
Saving to: ‘suspicious.dd.sda1’

suspicious.dd.sda 100%[============>]  31.35M  9.45MB/s    in 3.3s    

2024-10-27 05:09:25 (9.45 MB/s) - ‘suspicious.dd.sda1’ saved [32868864/32868864]

                                                                       
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$ ls
suspicious.dd.sda1
                                                                       
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$ file suspicious.dd.sda1                        
suspicious.dd.sda1: Linux rev 1.0 ext3 filesystem data, UUID=fc168af0-183b-4e53-bdf3-9c1055413b40 (needs journal recovery)
                                                                       
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$ fls suspicious.dd.sda1                         
d/d 11: lost+found
d/d 2009:       boot
d/d 4017:       tce
r/r 12: suspicious-file.txt
V/V 8033:       $OrphanFiles
                                                                       
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$ icat suspicious.dd.sda1                  
Missing image name and/or address
usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
        -h: Do not display holes in sparse files
        -r: Recover deleted file
        -R: Recover deleted file and suppress recovery errors
        -s: Display slack space at end of file
        -i imgtype: The format of the image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -o imgoffset: The offset of the file system in the image (in sectors)
        -P pooltype: Pool container type (use '-P list' for supported types)
        -B pool_volume_block: Starting block (for pool volumes only)
        -S snap_id: Snapshot ID (for APFS only)
        -v: verbose to stderr
        -V: Print version
        -k password: Decryption password for encrypted volumes
                                                                       
┌──(kali㉿kali)-[~/Downloads/PitterPAtter]
└─$  xxd -s 0x200400 -l 200 suspicious.dd.sda1
00200400: 4e6f 7468 696e 6720 746f 2073 6565 2068  Nothing to see h
00200410: 6572 6521 2042 7574 2079 6f75 206d 6179  ere! But you may
00200420: 2077 616e 7420 746f 206c 6f6f 6b20 6865   want to look he
00200430: 7265 202d 2d3e 0a7d 0038 0033 0034 0036  re -->.}.8.3.4.6
00200440: 0030 0063 0061 0065 005f 0033 003c 005f  .0.c.a.e._.3.<._
00200450: 007c 004c 006d 005f 0031 0031 0031 0074  .|.L.m._.1.1.1.t
00200460: 0035 005f 0033 0062 007b 0046 0054 0043  .5._.3.b.{.F.T.C
00200470: 006f 0063 0069 0070 0000 0000 0000 0000  .o.c.i.p........
00200480: 0000 0000 0000 0000 0000 0000 0000 0000  ................
00200490: 0000 0000 0000 0000 0000 0000 0000 0000  ................
002004a0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
002004b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
002004c0: 0000 0000 0000 0000                      ........
```

sacamos la bandera de la parte derecha

```java
}.8.3.4.6.0.c.a.e._.3.<._.|.L.m._.1.1.1.t.5._.3.b.{.F.T.C.o.c.i.p..
```


en CyberChef le colocamos el texto y le aplicamos `Reverse` y `Remove whitespace` 

```java 
picoCTF{b3_5t111_mL|_<3_eac06438}
```

## Notas Adicionales 

### Referencias






