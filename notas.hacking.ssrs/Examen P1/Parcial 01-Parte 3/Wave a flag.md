## Objetivo 

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...
## Solución  
```bash 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
picoCTF  warm
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ ./warm                 
zsh: permission denied: ./warm
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ chmod +x warm    
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ ./warm 
Hello user! Pass me a -h to learn what I can do!
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```
## Notas Adicionales 
chmod (change mod) y el parametro +x es utilizado para añadir los permisos

### Referencias

