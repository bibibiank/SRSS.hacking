## Objetivo 
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

> NOTE: if you’re a Windows user and typically use Powershell to `ssh` into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.

## Commands you may need to solve this level

ssh, cat, more, vi, ls, id, pwd
## Datos de acceso al nivel 

bandit25
iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
## Solución  

`bandit25@bandit:~$ cat /etc/passwd | grep bandit26`
`bandit26:x:11026:11026:bandit level 26:/home/bandit26:/usr/bin/showtext`
`bandit25@bandit:~$ cat /usr/bin/showtext`
`#!/bin/sh`

`export TERM=linux`

`exec more ~/text.txt`
`exit 0`




----------------------------------------------

C`:\Users\chair>ssh -i llavebandit25.txt bandit26@bandit.labs.overthewire.org -p2220`

`e: /etc/bandit_pass/bandit26"`
`s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ`
`~                                                                                                                                                                         ~                                                                                                                                                                         "/etc/bandit_pass/bandit26" [readonly] 1L, 33B                                                                                                          1,1           All`





`Vim: Caught deadly signal HUP`

`Vim: Finished.`










## Notas Adicionales 
`hacer pequeña la pestaña presionar v esc `
### Referencias
