## Objetivo 

What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/67/challenge.zip)

## Solución  

```bash

──(kali㉿kali)-[~]
└─$ cd Downloads      
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 big-zip-files.zip  'challenge(2).zip'  'challenge(4).zip'   enc_flag   files.zip
'challenge(1).zip'  'challenge(3).zip'   challenge.zip       files
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip challenge\(4\).zip 
Archive:  challenge(4).zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/2bdd8ec87a21ba45e77bd9bed3e4893faafd0f  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls
 big-zip-files.zip  'challenge(2).zip'  'challenge(4).zip'   drop-in    files
'challenge(1).zip'  'challenge(3).zip'   challenge.zip       enc_flag   files.zip
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ cd drop-in  
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ ls
message.txt
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ cat message.txt 
This is what I was working on, but I'd need to look at my commit history to know why...                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git log
commit b92bdd8ec87a21ba45e77bd9bed3e4893faafd0f (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:29 2024 +0000

    picoCTF{t1m3m@ch1n3_5cde9075}
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/drop-in]
└─$ git checkout b92bdd8 
Note: switching to 'b92bdd8'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at b92bdd8 picoCTF{t1m3m@ch1n3_5cde9075}



```

## Notas Adicionales 

### Referencias
