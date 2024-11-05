## Objetivo 

I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)
## Solución  


```bash
┌──(kali㉿kali)-[~]
└─$ cd Documents   
                                                                                                      
┌──(kali㉿kali)-[~/Documents]
└─$ cd drop-in 
                                                                                                      
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ ls 
flag.py  message.py  message.txt
                                                                                                      
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git log      
commit ef0b7cc6b98367fa168573c931e0f7098ef59182 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    remove sensitive info

commit ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    create flag
                                                                                                      
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout               
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ git checkout ea859bf 
Note: switching to 'ea859bf'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/drop-in]
└─$ cat message.txt 
picoCTF{s@n1t1z3_cf09a485}


```

## Notas Adicionales 

### Referencias

