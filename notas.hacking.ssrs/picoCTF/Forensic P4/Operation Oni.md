## Objetivo 
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.

## Solución  
```java 

┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ gzip disk.img.gz               
gzip: disk.img.gz already has .gz suffix -- unchanged
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ gzip -d disk.img.gz            
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ mmls disk.img   
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ fls disk.img -o 0000206848      
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib

                                                                                                        ┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ fls -o 0000206848 disk.img 470 -r 

r/r 2344:       .ash_history
d/d 3916:       .ssh
+ r/r 2345:     id_ed25519
+ r/r 2346:     id_ed25519.pub
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$  icat -o 0000206848 disk.img 2345   

-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ nano key_oni.txt
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ icat -o 0000206848 disk.img 2345 > key_oni.txt 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ chmod 600 key_oni.txt 
           
┌──(kali㉿kali)-[~/Downloads/OperationOni]
└─$ ssh -i key_oni.txt  -p 55333 ctf-player@saturn.picoctf.net
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_b5066e83}ctf-player@challenge:~$ 
 

```

## Notas Adicionales 

### Referencias