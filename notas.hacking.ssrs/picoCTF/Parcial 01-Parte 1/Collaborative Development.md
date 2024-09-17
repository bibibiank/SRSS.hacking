
## Objetivo 

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

## Solución  

```bash


──(kali㉿kali)-[~]
└─$ cd Documents             
                                                                                   
┌──(kali㉿kali)-[~/Documents]
└─$ cd drop-in 
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ ls\    
> 
flag.py  message.py
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ cat flag.py 
print("Printing the flag...")
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git branch -a                
  feature/part-1
  feature/part-2
  feature/part-3
* main
  master
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part-
error: pathspec 'feature/part-' did not match any file(s) known to git
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ ls 
flag.py  message.py
                                       



──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout master        
error: The following untracked working tree files would be overwritten by checkout:
        message.py
Please move or remove them before you switch branches.
Aborting
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part- 
error: pathspec 'feature/part-' did not match any file(s) known to git
                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part-1
Already on 'feature/part-1'
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ python flag.py 
Printing the flag...
picoCTF{t3@mw0rk_                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ python flag.py 
Printing the flag...
m@k3s_th3_dr3@m_                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ python flag.py             
Printing the flag...
w0rk_4c24302f}
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/drop-in]

```

## Notas Adicionales 
git branch -a : cambiar de branch e ir juntando las contraseñas

### Referencias
