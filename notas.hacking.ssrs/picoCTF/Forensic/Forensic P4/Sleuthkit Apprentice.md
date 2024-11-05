## Objetivo 
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)

## Solución  
```java 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd SleuthkitApprentice 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ wget https://artifacts.picoctf.net/c/137/disk.flag.img.gz
--2024-10-16 00:06:46--  https://artifacts.picoctf.net/c/137/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534568 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz             100%[==============================================>]  45.33M  7.29MB/s    in 7.0s    

2024-10-16 00:06:54 (6.46 MB/s) - ‘disk.flag.img.gz’ saved [47534568/47534568]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ ls
disk.flag.img.gz
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ gzip -d disk.flag.img.gz 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ ls    
disk.flag.img
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ fls -o 360448 disk.flag.img -r
d/d 451:        home
d/d 11: lost+found
d/d 12: boot
d/d 1985:       etc
+ r/r 23:       group
+ r/r 24:       group-
+ r/r 25:       shadow
+ r/r 26:       shadow-






d/d 1995:       root
+ r/r 2363:     .ash_history
+ d/d 3981:     my_folder
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
d/d 1996:       run
d/d 1997:       srv
d/d 1998:       sys
d/d 2358:       swap
V/V 31745:      $OrphanFiles
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ fls -o 360448 disk.flag.img -r 1995
r/r 2363:       .ash_history
d/d 3981:       my_folder
+ r/r * 2082(realloc):  flag.txt
+ r/r 2371:     flag.uni.txt
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ icat -o 360448 disk.flag.img 2363
apk add nano
mkdir my_folder
cd my_folder/
nano flag.txt
ls -al
iconv -f ascii -t utf16 > flag.uni.txt
l
ls -al
iconv -f ascii -t utf16 flag.txt > flag.uni.txt
ls -al
shred
shred -zu flag.txt 
ls -al
halt
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/SleuthkitApprentice]
└─$ icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_adac6cb4}


```

## Notas Adicionales 

### Referencias
