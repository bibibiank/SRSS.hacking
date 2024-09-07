## Objetivo 

Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso al nivel 
bandit26
s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
## Solución 


**==Solución 1: conectándose con la llave que obtuvimos en bandit25==**

``` bash 
C:\Users\chair>ssh -i llavebandit25.txt bandit26@bandit.labs.overthewire.org -p2220`
 `_                     _ _ _   ___   __`
  `_                     _ _ _   ___   __`
 `| |                   | (_) | |__ \ / /`
 `| |__   __ _ _ __   __| |_| |_   ) / /_`
 `| '_ \ / _ | '_ \ / _ | | __| / / '_ \`
 `| |_) | (_| | | | | (_| | | |_ / /| (_) |`
 `|_.__/ \__,_|_| |_|\__,_|_|\__|____\___/`
`~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             ~                                                                                                                             :shell`
`bandit26@bandit:~$`
`bandit26@bandit:~$`
`bandit26@bandit:~$`
`bandit26@bandit:~$ ls -la`
`total 44`
`drwxr-xr-x  3 root     root      4096 Jul 17 15:57 .`
`drwxr-xr-x 70 root     root      4096 Jul 17 15:58 ..`
`-rwsr-x---  1 bandit27 bandit26 14880 Jul 17 15:57 bandit27-do`
`-rw-r--r--  1 root     root       220 Mar 31 08:41 .bash_logout`
`-rw-r--r--  1 root     root      3771 Mar 31 08:41 .bashrc`
`-rw-r--r--  1 root     root       807 Mar 31 08:41 .profile`
`drwxr-xr-x  2 root     root      4096 Jul 17 15:57 .ssh`
`-rw-r-----  1 bandit26 bandit26   258 Jul 17 15:57 text.txt`
`bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27`
`upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
```

==**Solucion 2**==: ps con la contraseña s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
## Notas Adicionales 

antes de ingresar al nivel 26, debes hacer mas pequeña la terminal para que éste te lleve a "more"
una vez que estamos en more, tecleamos "v" para ir al editor de vi, una vez dentro, tecleamos ESC, despues, ```bash
:set shell = /bin/bash
``` luego `ESC : shell


### Referencias
